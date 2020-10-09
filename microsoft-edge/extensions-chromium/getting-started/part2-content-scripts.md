---
description: Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo
title: Criar um tutorial de extensão parte 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 755b70635c93d7331ef3ac985625ba7ac5689679
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104711"
---
# Criar um tutorial de extensão parte 2  
  
[Origem do pacote de extensão concluída para esta parte][ArchiveExtensionGettingStartedPart2]    

## Visão geral  

Este tutorial aborda as seguintes tecnologias de extensão.
*   Injetando bibliotecas JavaScript na extensão  
*   Expondo ativos de extensão a guias do navegador  
*   Incluindo páginas de conteúdo em guias existentes do navegador  
*   Fazer com que as páginas de conteúdo escutem mensagens de pop-ups e respondam  

Você aprenderá a atualizar o menu pop-up para substituir sua imagem de início estático por um título e um botão HTML padrão.  Quando selecionado, esse botão passa essa imagem de estrelas, que é inserida na extensão, para a página de conteúdo.  Essa imagem é inserida na guia ativa do navegador. Siga as etapas abaixo para obter mais detalhes.

1.  Remover a imagem do pop-up e substituí-la por um botão  

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
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Depois de atualizar e abrir a extensão, um pop-up abre com um botão de exibição.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   popup.htmexibição de l após pressionar o ícone de extensão
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  Atualizar estratégia para exibir imagem na parte superior da guia do navegador  

Depois de adicionar o botão, a próxima tarefa é fazer com que ele traga o `images/stars.jpeg` arquivo de imagem na parte superior da página da guia ativa.  

Lembre-se de que cada página da guia funciona em seu próprio thread. Além disso, a extensão usa um thread diferente.  Primeiro, crie um script de conteúdo que é injetado na página da guia.  Em seguida, envie uma mensagem do seu pop-up para esse script de conteúdo em execução na página da guia. O script de conteúdo recebe a mensagem, que descreve qual imagem deve ser exibida.  

3. Criar o JavaScript pop-up para enviar uma mensagem  

Primeiro, crie `popup/popup.js` e adicione código para enviar uma mensagem para o script de conteúdo ainda não criado que você deve criar e injetar momentaneamente na guia do navegador.  Para fazer isso, o código a seguir adiciona um `onclick` evento ao seu botão pop-up de exibição.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

No `onclick` evento, localize a guia atual do navegador.  Em seguida, use a `chrome.tabs.sendmessage` API de extensão para enviar uma mensagem para essa guia.  

Nessa mensagem, você deve incluir a URL para a imagem que você deseja exibir. Além disso, envie uma ID exclusiva para atribuir à imagem inserida.  Você pode optar por permitir que o JavaScript de inserção de conteúdo gere isso, mas por motivos que se tornam aparentes mais tarde, gere essa identificação exclusiva aqui `popup.js` e passe-a para o script de conteúdo ainda não criado.  

O trecho de código a seguir descreve o código atualizado em `popup/popup.js` .  Além disso, passe a ID da guia atual, que é usada posteriormente neste artigo.  

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

4. Disponibilizar seus estrelas. jpeg em qualquer guia do navegador  

Provavelmente, você deve estar se perguntando por que, quando você passar, `images/stars.jpeg` deve usar a `chrome.extension.getURL` API de extensão Chrome em vez de apenas transmitir a URL relativa sem o prefixo adicional, como na seção anterior.  A propósito, esse prefixo extra, retornado por `getUrl` com a imagem anexada tem a seguinte aparência:  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

O motivo é que você está injetando a imagem usando o `src` atributo do `img` elemento na página de conteúdo.  A página de conteúdo está em execução em um thread exclusivo que não é igual ao thread que executa a extensão.  Você deve expor o arquivo de imagem estática como um ativo da Web para que ele funcione corretamente.  

Adicione outra entrada no `manifest.json` arquivo para declarar que a imagem está disponível para todas as guias do navegador.  Essa entrada é a seguinte \ (você deve vê-la no `manifest.json` arquivo completo abaixo quando adiciona a declaração de script de conteúdo que está chegando \).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Agora você escreveu o código em seu `popup.js` arquivo para enviar uma mensagem para a página de conteúdo que está inserida na página da guia ativa atual, mas você não criou e injetau essa página de conteúdo.  Faça isso agora.  

5.  Atualize o seu manifest.jspara obter conteúdo e acesso à Web  

A atualização `manifest.json` que inclui o `content-scripts` e `web_accessible_resources` é a seguinte.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to show the NASA picture of the day.",
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

A seção que você adicionou está `content_scripts` .  O `matches` atributo é definido como `<all_urls>` , o que significa que todos os arquivos `content_scripts` são injetados em todas as páginas da guia do navegador quando cada guia é carregada.  Os tipos de arquivos permitidos que podem ser injetados são JavaScript e CSS.  Você também adicionou `libjquery.min.js` .  Você pode incluir isso do download mencionado na parte superior da seção.  

6. Adicionar jQuery e noções básicas sobre o thread associado  

Nos scripts de conteúdo que você está injetando, planeje o uso do jQuery \ ( `$` \).  Você adicionou uma versão minified do jQuery e a coloca em seu pacote de extensão como `lib\jquery.min.js` .  Esses scripts de conteúdo são executados em caixas de proteção individuais, o que significa que o jQuery injetado na `popup.js` página não é compartilhado com o conteúdo.  

Lembre-se de que, mesmo se a guia do navegador tiver JavaScript em execução na página da Web carregada, qualquer conteúdo injetado não terá acesso a isso.  Que injetado JavaScript apenas tem acesso ao DOM real carregado na guia do navegador.  

7. Adicionar o ouvinte de mensagem de script de conteúdo  

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

*   A primeira linha de script insere dinamicamente no cabeçalho DOM uma **\<style\>** seção que você deve atribuir como uma `slide-image` classe ao seu `img` elemento.  
*   A segunda linha de script acrescenta um `img` elemento logo abaixo da `body` Guia do navegador que tem a `slide-image` classe atribuída, bem como a `imageDivId` ID do elemento da imagem.  
*   A terceira linha de script adiciona um `click` evento que abrange toda a imagem, permitindo que o usuário selecione qualquer lugar na imagem e essa imagem seja removida da página \ (juntamente com é ouvinte de evento \).  

8. Adicionar funcionalidade para remover a imagem exibida quando selecionada  

Agora, quando você navegar em qualquer página e selecionar o ícone da **extensão** , o menu pop-up será exibido da seguinte maneira.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   popup.htmexibição de l após pressionar o ícone de extensão
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Ao selecionar o `Display` botão, você obtém o que está abaixo.  Se você selecionar qualquer lugar da `stars.jpeg` imagem, esse elemento de imagem será removido e as páginas da guia serão recolhidas para o que foi exibido originalmente.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão"  
