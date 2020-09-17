---
description: Introdução às extensões 2
title: Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: fd2276c069116a7f69f06ae50f201e284b60f3ea
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016726"
---
# Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo  

<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart2]  
-->  

## Visão geral  

Na parte 2, você aprende a atualizar o menu pop-up para não mostrar a imagem de estrelas estática que havia antes, mas para substituir essa imagem por um título e um botão HTML padrão.  Quando selecionado, esse botão passa essa imagem de estrelas, que é inserida na extensão, para a página de conteúdo.  Essa imagem é inserida na guia ativa do navegador.  

*   Tecnologias de extensão abordadas neste guia  
    *   Injetando bibliotecas JavaScript na extensão  
    *   Expondo ativos de extensão a guias do navegador  
    *   Incluindo páginas de conteúdo em guias existentes do navegador  
    *   Fazer com que as páginas de conteúdo escutem mensagens de pop-ups e respondam  

## Remover a imagem do pop-up e substituí-la por um botão  

Primeiro, atualize o `popup.html` arquivo com uma marcação direta que exiba um título e um botão.  Você programará esse botão em breve, mas, por enquanto, simplesmente incluirá uma referência a um arquivo JavaScript vazio `popup.js` .  Aqui está a atualização de HTML.  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA Picture of the Day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Depois de atualizar a extensão e selecionar o ícone de inicialização da extensão, o seguinte pop-up inclui um botão de exibição.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   popup.htmexibição de l após pressionar o ícone de extensão
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## Estratégia atualizada para exibir imagem na parte superior da guia do navegador  

Depois de adicionar o botão, a próxima tarefa é fazer com que ele traga o `images/stars.jpeg` arquivo de imagem na parte superior da página da guia ativa.  

Lembre-se de que cada página da guia tem um thread exclusivo e a extensão tem um thread separado.  Portanto, primeiro você deve criar um script de conteúdo e injetar esse script na página da guia.  Depois de fazer isso, você deve enviar uma mensagem do seu pop-up para esse script de conteúdo em execução na página da guia que informa que o script de conteúdo é a imagem a ser mostrada e como mostrá-la.  

## Criando o JavaScript pop-up para enviar uma mensagem  

Primeiro, crie `popup/popup.js` e adicione código para enviar uma mensagem para o script de conteúdo ainda não criado que você deve criar e injetar momentaneamente na guia do navegador.  Para fazer isso, o código a seguir adiciona um `onclick` evento ao seu botão pop-up de exibição.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

No `onclick` evento, o que você deve fazer é encontrar a guia atual do navegador \ (se houver apenas uma aberta).  Depois disso, quando encontrar essa guia, use a `chrome.tabs.sendmessage` API de extensão para enviar uma mensagem para essa guia.  

Nessa mensagem, você deve incluir a URL da imagem que você deseja exibir e deseja enviar uma ID exclusiva que deve ser atribuída a essa imagem inserida.  Você pode optar por permitir que o JavaScript de inserção de conteúdo gere isso, mas por motivos que se tornam aparentes mais tarde, gere essa identificação exclusiva aqui `popup.js` e passe-a para o script de conteúdo ainda não criado.  

Aqui está o `popup/popup.js` arquivo atualizado.  Além disso, passe a ID da guia atual que você deve precisar em uma seção posterior, mas por enquanto, não será usado.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

## Disponibilizar seus estrelas. jpeg em qualquer guia do navegador  

Provavelmente, você deve estar se perguntando por que, quando você passar, `images/stars.jpeg` deve usar a `chrome.extension.getURL` API de extensão Chrome em vez de apenas transmitir a URL relativa sem o prefixo adicional, como na seção anterior.  A propósito, esse prefixo extra, retornado por `getUrl` com a imagem anexada tem a seguinte aparência:  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

O motivo é que você está injetando a imagem usando o `src` atributo do `img` elemento na página de conteúdo.  A página de conteúdo está em execução em um thread exclusivo que não é igual ao thread que executa a extensão.  Você deve expor o arquivo de imagem estática como um ativo da Web para que ele funcione corretamente.  

Para fazer isso, você deve adicionar outra entrada no `manifest.json` arquivo.  Você deve declarar a imagem para ser acessível em qualquer guia do navegador.  Essa entrada é a seguinte \ (você deve vê-la no `manifest.json` arquivo completo abaixo quando adiciona a declaração de script de conteúdo que está chegando \).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Agora você escreveu o código em seu `popup.js` arquivo para enviar uma mensagem para a página de conteúdo que está inserida na página da guia ativa atual, mas você não criou e injetau essa página de conteúdo.  Faça isso agora.  

## Como atualizar o seu manifest.jspara acesso ao conteúdo e à Web  

A atualização `manifest.json` que inclui o `content-scripts` e `web_accessible_resources` é a seguinte.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

A seção que você adicionou está `content_scripts` .  O atributo `matches` é definido para `<all_urls>` significar que todos os arquivos mencionados na seção **content_scripts** são injetados em todas as páginas da guia do navegador quando cada um é carregado.  Os tipos permitidos de arquivos que podem ser injetados aqui são JavaScript e CSS.  Você também adicionou `libjquery.min.js` .  Você pode incluir isso do download mencionado na parte superior da seção.  

## Adicionando o jQuery e compreendendo o thread associado  

Nos scripts de conteúdo que você estiver injetando, planeje o uso do jQuery \ ( `$` \).  Você adicionou uma versão minified do jQuery e a coloca em seu pacote de extensão como `lib\jquery.min.js` .  Esses scripts de conteúdo são executados em uma área restrita de classificações individuais, o que significa que o jQuery injetado na `popup.js` página não compartilha com o conteúdo.  

Lembre-se de que, mesmo se a guia do navegador tiver JavaScript em execução na página da Web carregada, qualquer conteúdo injetado não terá acesso a isso.  Que injetado JavaScript apenas tem acesso ao DOM real carregado na guia do navegador.  

## Adicionando o ouvinte de mensagem de script de conteúdo  

Aqui está `content-scripts\content.js` um arquivo que é injetado em cada página da guia do navegador com base na sua `manifest.json` `content-scripts` seção.  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

Observe que todas as opções JavaScript a seguir são registradas `listener` usando o `chrome.runtime.onMessage.addListener` método de API de extensão.  Esse ouvinte aguarda mensagens como a que você enviou do `popup.js` descrito anteriormente com o método de `chrome.tabs.sendMessage` API de extensão.  

O primeiro parâmetro do `addListener` método é uma função cujo primeiro parâmetro, solicitação, é o detalhe da mensagem que está sendo transmitida.  Lembre-se, de `popup.js` quando você usou o `sendMessage` método, esses atributos do primeiro parâmetro são `url` e `imageDivId` .  

Quando um evento é processado pelo ouvinte, a função que é o primeiro parâmetro é executada.  O primeiro parâmetro dessa função é um objeto com atributos como atribuído por `sendMessage` .  Essa função simplesmente processa as três linhas de script do jQuery.  

*   A primeira insere dinamicamente no cabeçalho DOM uma **\<style\>** seção que você deve atribuir como uma `slide-image` classe ao `img` elemento.  
*   O segundo, acrescenta um `img` elemento à direita abaixo da `body` Guia do navegador que tem a `slide-image` classe atribuída, bem como a `imageDivId` ID do elemento da imagem.  
*   O terceiro adiciona um `click` evento que abrange toda a imagem, permitindo que o usuário selecione qualquer local na imagem e essa imagem seja removida da página \ (juntamente com é ouvinte de evento \).  

## Adicionando funcionalidade para remover a imagem exibida quando selecionada  

Agora, quando você navegar em qualquer página e selecionar o ícone da **extensão** , o menu pop-up será exibido da seguinte maneira.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   popup.htmexibição de l após pressionar o ícone de extensão
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Ao selecionar o `Display` botão, você obtém o que está abaixo.  Se você selecionar qualquer lugar da `stars.jpeg` imagem, esse elemento de imagem será removido e as páginas da guia serão recolhidas para o que foi exibido originalmente.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="A imagem exibida no navegador":::
   A imagem exibida no navegador
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

Você criou uma extensão que envia com sucesso uma mensagem do pop-up de ícone de extensão para o JavaScript inserido dinamicamente executando como conteúdo na guia do navegador.  Que o conteúdo injetado define o elemento Image para exibir seu JPEG de estrelas estática.  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Fonte do pacote de extensão concluída para esta parte | Documentos da Microsoft"  
