---
description: Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo
title: Criar um tutorial para extensão Parte 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: 48af14c33a368a3449acb88b4dfb875ad5398e7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397913"
---
# <a name="create-an-extension-tutorial-part-2"></a><span data-ttu-id="4ca9e-104">Criar um tutorial para extensão Parte 2</span><span class="sxs-lookup"><span data-stu-id="4ca9e-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="4ca9e-105">Fonte do pacote de extensão concluída para esta parte</span><span class="sxs-lookup"><span data-stu-id="4ca9e-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a><span data-ttu-id="4ca9e-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="4ca9e-106">Overview</span></span>  

<span data-ttu-id="4ca9e-107">Este tutorial aborda as seguintes tecnologias de extensão.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="4ca9e-108">Injetar bibliotecas JavaScript em extensão</span><span class="sxs-lookup"><span data-stu-id="4ca9e-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="4ca9e-109">Expondo ativos de extensão às guias do navegador</span><span class="sxs-lookup"><span data-stu-id="4ca9e-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="4ca9e-110">Incluindo páginas de conteúdo em guias de navegador existentes</span><span class="sxs-lookup"><span data-stu-id="4ca9e-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="4ca9e-111">Ter páginas de conteúdo escutando mensagens de pop-ups e respondendo</span><span class="sxs-lookup"><span data-stu-id="4ca9e-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="4ca9e-112">Você aprenderá a atualizar seu menu pop-up para substituir sua imagem estática de início por um título e um botão HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="4ca9e-113">Esse botão, quando selecionado, passa a imagem de estrelas, inserida na extensão, para a página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="4ca9e-114">Essa imagem é inserida na guia do navegador ativo. Siga as etapas abaixo para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="4ca9e-115">Remova a imagem do pop-up e substitua-a por um botão</span><span class="sxs-lookup"><span data-stu-id="4ca9e-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="4ca9e-116">Primeiro, atualize seu arquivo com alguma marcação direta `popup.html` que exibe um título e um botão.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="4ca9e-117">Você programa esse botão em breve, mas, por enquanto, basta incluir uma referência a um arquivo JavaScript `popup.js` vazio.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="4ca9e-118">Aqui está o HTML de atualização.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="4ca9e-119">Depois de atualizar e abrir a extensão, um pop-up será aberto com um botão de exibição.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html exibir depois de selecionar o ícone Extensão":::
   <span data-ttu-id="4ca9e-121">popup.html exibir depois de selecionar o ícone Extensão</span><span class="sxs-lookup"><span data-stu-id="4ca9e-121">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="4ca9e-122">Atualizar estratégia para exibir imagem na parte superior da guia navegador</span><span class="sxs-lookup"><span data-stu-id="4ca9e-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="4ca9e-123">Depois de adicionar o botão, a próxima tarefa é fazer com que ele traga o arquivo de imagem na `images/stars.jpeg` parte superior da página de guia ativa.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="4ca9e-124">Lembre-se de que cada página de tabulação é executado em seu próprio thread.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="4ca9e-125">Além disso, a extensão usa um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="4ca9e-126">Primeiro, crie um script de conteúdo injetado na página de tabulação.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="4ca9e-127">Em seguida, envie uma mensagem do pop-up para o script de conteúdo em execução na página de guia.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="4ca9e-128">O script de conteúdo recebe a mensagem, que descreve qual imagem deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="4ca9e-129">Criar o JavaScript pop-up para enviar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="4ca9e-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="4ca9e-130">Primeiro, crie e adicione código para enviar uma mensagem ao script de conteúdo ainda não criado que você deve criar e injetar momentaneamente na guia `popup/popup.js` do navegador.  Para fazer isso, o código a seguir adiciona um `onclick` evento ao botão de exibição pop-up.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="4ca9e-131">No `onclick` evento, encontre a guia do navegador atual.  Em seguida, use `chrome.tabs.sendmessage` a API de extensão para enviar uma mensagem para essa guia.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="4ca9e-132">Nessa mensagem, você deve incluir a URL da imagem que deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="4ca9e-133">Além disso, envie uma ID exclusiva para atribuir à imagem inserida.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="4ca9e-134">Você pode optar por permitir que o JavaScript de inserção de conteúdo gere isso, mas por motivos que se tornam aparentes mais tarde, gere essa ID exclusiva aqui e passe-a para o script de conteúdo ainda não `popup.js` criado.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="4ca9e-135">O trecho de código a seguir descreve o código atualizado em `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="4ca9e-136">Além disso, passe a ID da guia atual, que é usada posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="4ca9e-137">Disponibilizar suas estrelas.jpeg em qualquer guia do navegador</span><span class="sxs-lookup"><span data-stu-id="4ca9e-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="4ca9e-138">Você provavelmente está se perguntando por que, ao passar na API de extensão do chrome, você deve usar apenas passar a URL relativa sem o prefixo extra, como na `images/stars.jpeg` `chrome.extension.getURL` seção anterior.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="4ca9e-139">A propósito, esse prefixo extra, retornado com `getUrl` a imagem anexada, se parece com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="4ca9e-140">O motivo é que você está injetando a imagem usando o `src` atributo do elemento na página de `img` conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="4ca9e-141">A página de conteúdo está sendo executado em um thread exclusivo que não é o mesmo que o thread que está executando o Extension.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="4ca9e-142">Você deve expor o arquivo de imagem estática como um ativo da Web para que ele funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="4ca9e-143">Adicione outra entrada no `manifest.json` arquivo para declarar que a imagem está disponível para todas as guias do navegador.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="4ca9e-144">Essa entrada é a seguinte \(você deve vê-la no arquivo completo abaixo ao adicionar a declaração de script de conteúdo `manifest.json` que está chegando\).</span><span class="sxs-lookup"><span data-stu-id="4ca9e-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="4ca9e-145">Agora você escreveu o código em seu arquivo para enviar uma mensagem para a página de conteúdo inserida na página de tabulação ativa atual, mas você não criou e `popup.js` injetou essa página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="4ca9e-146">Faça isso agora.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-146">Do that now.</span></span>  

5.  <span data-ttu-id="4ca9e-147">Atualizar seu manifest.jspara conteúdo e acesso à Web</span><span class="sxs-lookup"><span data-stu-id="4ca9e-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="4ca9e-148">O atualizado `manifest.json` que inclui o e é o `content-scripts` `web_accessible_resources` seguinte.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="4ca9e-149">A seção adicionada é `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="4ca9e-150">O atributo é definido como , o que significa que todos os arquivos em são injetados em todas as páginas de guia `matches` do navegador quando cada guia é `<all_urls>` `content_scripts` carregada.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="4ca9e-151">Os tipos de arquivos permitidos que podem ser injetados são JavaScript e CSS.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="4ca9e-152">Você também adicionou `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="4ca9e-153">Você pode incluir isso no download mencionado na parte superior da seção.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="4ca9e-154">Adicionar jQuery e entender o thread associado</span><span class="sxs-lookup"><span data-stu-id="4ca9e-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="4ca9e-155">Nos scripts de conteúdo que você está injetando, planeje usar jQuery \( `$` \).</span><span class="sxs-lookup"><span data-stu-id="4ca9e-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="4ca9e-156">Você adicionou uma versão minificada do jQuery e a colocou no pacote de Extensão como `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="4ca9e-157">Esses scripts de conteúdo são executados em áreas de resquência individuais, o que significa que o jQuery injetado na página não `popup.js` é compartilhado com o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="4ca9e-158">Lembre-se de que, mesmo que a guia do navegador tenha JavaScript em execução na página da Web carregada, qualquer conteúdo injetado não tem acesso a isso.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="4ca9e-159">Esse JavaScript injetado tem acesso ao DOM real carregado nessa guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="4ca9e-160">Adicionar o ouvinte de mensagens de script de conteúdo</span><span class="sxs-lookup"><span data-stu-id="4ca9e-160">Add the content script message listener</span></span>  

<span data-ttu-id="4ca9e-161">Este é o `content-scripts\content.js` arquivo que é injetado em todas as páginas de guia do navegador com base em sua `manifest.json` `content-scripts` seção.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="4ca9e-162">Observe que todo o JavaScript acima faz é registrar um `listener` usando o método API de `chrome.runtime.onMessage.addListener` extensão.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="4ca9e-163">Esse ouvinte aguarda mensagens como as que você enviou da descrita `popup.js` anteriormente com o método `chrome.tabs.sendMessage` API de extensão.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="4ca9e-164">O primeiro parâmetro do método é uma função cujo primeiro parâmetro, a solicitação, é os detalhes da `addListener` mensagem que está sendo passada.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="4ca9e-165">Lembre-se, `popup.js` de , quando você usou o `sendMessage` método, esses atributos do primeiro parâmetro `url` são e `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="4ca9e-166">Quando um evento é processado pelo ouvinte, a função que é o primeiro parâmetro é executado.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="4ca9e-167">O primeiro parâmetro dessa função é um objeto que tem atributos atribuídos por `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="4ca9e-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="4ca9e-168">Essa função simplesmente processa as três linhas de script jQuery.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="4ca9e-169">A primeira linha de script insere dinamicamente no header DOM uma seção que você deve atribuir como **\<style\>** `slide-image` uma classe ao `img` elemento.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="4ca9e-170">A segunda linha de script anexa um elemento logo abaixo da guia do navegador que tem a classe atribuída, bem como a `img` `body` `slide-image` `imageDivId` ID desse elemento de imagem.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="4ca9e-171">A terceira linha de script adiciona um evento que abrange toda a imagem, permitindo que o usuário selecione em qualquer lugar na imagem e essa imagem seja removida da página \(juntamente com ela é ouvinte de `click` eventos\).</span><span class="sxs-lookup"><span data-stu-id="4ca9e-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="4ca9e-172">Adicionar funcionalidade para remover a imagem exibida quando selecionada</span><span class="sxs-lookup"><span data-stu-id="4ca9e-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="4ca9e-173">Agora, quando você navega para qualquer página e seleciona o ícone **extensão,** o menu pop-up é exibido da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html exibir depois de selecionar o ícone Extensão":::
   <span data-ttu-id="4ca9e-175">popup.html exibir depois de selecionar o ícone Extensão</span><span class="sxs-lookup"><span data-stu-id="4ca9e-175">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="4ca9e-176">Ao selecionar o `Display` botão, você obterá o que está abaixo.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="4ca9e-177">Se você selecionar em qualquer lugar da imagem, esse elemento de imagem será removido e as páginas de tabulação voltarão ao que `stars.jpeg` foi originalmente exibido.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="A imagem que aparece no navegador":::
   <span data-ttu-id="4ca9e-179">A imagem que aparece no navegador</span><span class="sxs-lookup"><span data-stu-id="4ca9e-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="4ca9e-180">Você criou um Extension que envia com êxito uma mensagem do pop-up do ícone de extensão e inseriu dinamicamente o JavaScript em execução como conteúdo na guia navegador.  O conteúdo injetado define o elemento image para exibir suas estrelas estáticas jpeg.</span><span class="sxs-lookup"><span data-stu-id="4ca9e-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Fonte de pacote de extensão concluída | Microsoft Docs"  
