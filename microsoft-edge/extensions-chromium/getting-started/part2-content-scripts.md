---
description: Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo
title: Criar um tutorial para extensão Parte 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: c5a17cbc55c6ccb42e06369474cd274d70742494
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579726"
---
# <a name="create-an-extension-tutorial-part-2"></a>Criar um tutorial para extensão Parte 2  
  
[Fonte do pacote de extensão concluída para esta parte][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a>Visão geral  

Este tutorial aborda as seguintes tecnologias de extensão.
*   Injetar bibliotecas JavaScript em extensão  
*   Expondo ativos de extensão às guias do navegador  
*   Incluindo páginas de conteúdo em guias de navegador existentes  
*   Ter páginas de conteúdo escutando mensagens de pop-ups e respondendo  

Você aprenderá a atualizar seu menu pop-up para substituir sua imagem de estrelas estáticas por um título e um botão HTML padrão.  Esse botão, quando selecionado, passa a imagem de estrelas, inserida na extensão, para a página de conteúdo.  Essa imagem é inserida na guia do navegador ativo. Siga as etapas abaixo para obter mais detalhes.

1.  Remova a imagem do pop-up e substitua-a por um botão  

Primeiro, atualize seu arquivo com alguma marcação direta `popup.html` que exibe um título e um botão.  Você programa esse botão em breve, mas, por enquanto, basta incluir uma referência a um arquivo JavaScript `popup.js` vazio.  Aqui está o HTML de atualização.  

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

Depois de atualizar e abrir a extensão, um pop-up será aberto com um botão de exibição.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html exibir depois de selecionar o ícone Extensão":::
   popup.html exibir depois de selecionar o ícone Extensão
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  Atualizar estratégia para exibir imagem na parte superior da guia navegador  

Depois de adicionar o botão, a próxima tarefa é fazer com que ele traga o arquivo de imagem na `images/stars.jpeg` parte superior da página de guia ativa.  

Lembre-se de que cada página de tabulação é executado em seu próprio thread. Além disso, a extensão usa um thread diferente.  Primeiro, crie um script de conteúdo injetado na página de tabulação.  Em seguida, envie uma mensagem do pop-up para o script de conteúdo em execução na página de guia. O script de conteúdo recebe a mensagem, que descreve qual imagem deve ser exibida.  

3. Criar o JavaScript pop-up para enviar uma mensagem  

Primeiro, crie e adicione código para enviar uma mensagem ao script de conteúdo ainda não criado que você deve criar e injetar momentaneamente na guia `popup/popup.js` do navegador.  Para fazer isso, o código a seguir adiciona um `onclick` evento ao botão de exibição pop-up.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

No `onclick` evento, encontre a guia do navegador atual.  Em seguida, use `chrome.tabs.sendmessage` a API de extensão para enviar uma mensagem para essa guia.  

Nessa mensagem, você deve incluir a URL da imagem que deseja exibir. Além disso, envie uma ID exclusiva para atribuir à imagem inserida.  Você pode optar por permitir que o JavaScript de inserção de conteúdo gere isso, mas por motivos que se tornam aparentes mais tarde, gere essa ID exclusiva aqui e passe-a para o script de conteúdo ainda não `popup.js` criado.  

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

4. Disponibilizar suas estrelas.jpeg em qualquer guia do navegador  

Você provavelmente está se perguntando por que, ao passar na API de extensão do chrome, você deve usar apenas passar a URL relativa sem o prefixo extra, como na `images/stars.jpeg` `chrome.extension.getURL` seção anterior.  A propósito, esse prefixo extra, retornado com `getUrl` a imagem anexada, se parece com o seguinte.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

O motivo é que você está injetando a imagem usando o `src` atributo do elemento na página de `img` conteúdo.  A página de conteúdo está sendo executado em um thread exclusivo que não é o mesmo que o thread que está executando o Extension.  Você deve expor o arquivo de imagem estática como um ativo da Web para que ele funcione corretamente.  

Adicione outra entrada no `manifest.json` arquivo para declarar que a imagem está disponível para todas as guias do navegador.  Essa entrada é a seguinte \(você deve vê-la no arquivo completo abaixo ao adicionar a declaração de script de conteúdo `manifest.json` que está chegando\).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Agora você escreveu o código em seu arquivo para enviar uma mensagem para a página de conteúdo inserida na página de tabulação ativa atual, mas você não criou e `popup.js` injetou essa página de conteúdo.  Faça isso agora.  

5.  Atualizar seu manifest.jspara conteúdo e acesso à Web  

O atualizado `manifest.json` que inclui o e é o `content-scripts` `web_accessible_resources` seguinte.  

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

A seção adicionada é `content_scripts` .  O atributo é definido como , o que significa que todos os arquivos em são injetados em todas as páginas de guia `matches` do navegador quando cada guia é `<all_urls>` `content_scripts` carregada.  Os tipos de arquivos permitidos que podem ser injetados são JavaScript e CSS.  Você também adicionou `libjquery.min.js` .  Você pode incluir isso no download mencionado na parte superior da seção.  

6. Adicionar jQuery e entender o thread associado  

Nos scripts de conteúdo que você está injetando, planeje usar jQuery \( `$` \).  Você adicionou uma versão minificada do jQuery e a colocou no pacote de Extensão como `lib\jquery.min.js` .  Esses scripts de conteúdo são executados em áreas de resquência individuais, o que significa que o jQuery injetado na página não `popup.js` é compartilhado com o conteúdo.  

Lembre-se de que, mesmo que a guia do navegador tenha JavaScript em execução na página da Web carregada, qualquer conteúdo injetado não tem acesso a isso.  Esse JavaScript injetado tem acesso ao DOM real carregado nessa guia do navegador.  

7. Adicionar o ouvinte de mensagens de script de conteúdo  

Este é o `content-scripts\content.js` arquivo que é injetado em todas as páginas de guia do navegador com base em sua `manifest.json` `content-scripts` seção.  

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

Observe que todo o JavaScript acima faz é registrar um `listener` usando o método API de `chrome.runtime.onMessage.addListener` extensão.  Esse ouvinte aguarda mensagens como as que você enviou da descrita `popup.js` anteriormente com o método `chrome.tabs.sendMessage` API de extensão.  

O primeiro parâmetro do método é uma função cujo primeiro parâmetro, a solicitação, é os detalhes da `addListener` mensagem que está sendo passada.  Lembre-se, `popup.js` de , quando você usou o `sendMessage` método, esses atributos do primeiro parâmetro `url` são e `imageDivId` .  

Quando um evento é processado pelo ouvinte, a função que é o primeiro parâmetro é executado.  O primeiro parâmetro dessa função é um objeto que tem atributos atribuídos por `sendMessage` .  Essa função simplesmente processa as três linhas de script jQuery.  

*   A primeira linha de script insere dinamicamente no header DOM uma seção que você deve atribuir como **\<style\>** `slide-image` uma classe ao `img` elemento.  
*   A segunda linha de script anexa um elemento logo abaixo da guia do navegador que tem a classe atribuída, bem como a `img` `body` `slide-image` `imageDivId` ID desse elemento de imagem.  
*   A terceira linha de script adiciona um evento que abrange toda a imagem, permitindo que o usuário selecione em qualquer lugar na imagem e essa imagem seja removida da página \(juntamente com ela é ouvinte de `click` eventos\).  

8. Adicionar funcionalidade para remover a imagem exibida quando selecionada  

Agora, quando você navega para qualquer página e seleciona o ícone **extensão,** o menu pop-up é exibido da seguinte forma.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html exibir depois de selecionar o ícone Extensão":::
   popup.html exibir depois de selecionar o ícone Extensão
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

Ao selecionar o `Display` botão, você obterá o que está abaixo.  Se você selecionar em qualquer lugar da imagem, esse elemento de imagem será removido e as páginas de tabulação voltarão ao que `stars.jpeg` foi originalmente exibido.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="A imagem que aparece no navegador":::
   A imagem que aparece no navegador
:::image-end:::

Você criou um Extension que envia com êxito uma mensagem do pop-up do ícone de extensão e inseriu dinamicamente o JavaScript em execução como conteúdo na guia navegador.  O conteúdo injetado define o elemento image para exibir suas estrelas estáticas jpeg.  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Fonte de pacote de extensão concluída | Microsoft Docs"  
