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
# <span data-ttu-id="2fab8-104">Criar um tutorial de extensão parte 2</span><span class="sxs-lookup"><span data-stu-id="2fab8-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="2fab8-105">Origem do pacote de extensão concluída para esta parte</span><span class="sxs-lookup"><span data-stu-id="2fab8-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <span data-ttu-id="2fab8-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="2fab8-106">Overview</span></span>  

<span data-ttu-id="2fab8-107">Este tutorial aborda as seguintes tecnologias de extensão.</span><span class="sxs-lookup"><span data-stu-id="2fab8-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="2fab8-108">Injetando bibliotecas JavaScript na extensão</span><span class="sxs-lookup"><span data-stu-id="2fab8-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="2fab8-109">Expondo ativos de extensão a guias do navegador</span><span class="sxs-lookup"><span data-stu-id="2fab8-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="2fab8-110">Incluindo páginas de conteúdo em guias existentes do navegador</span><span class="sxs-lookup"><span data-stu-id="2fab8-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="2fab8-111">Fazer com que as páginas de conteúdo escutem mensagens de pop-ups e respondam</span><span class="sxs-lookup"><span data-stu-id="2fab8-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="2fab8-112">Você aprenderá a atualizar o menu pop-up para substituir sua imagem de início estático por um título e um botão HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="2fab8-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="2fab8-113">Quando selecionado, esse botão passa essa imagem de estrelas, que é inserida na extensão, para a página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2fab8-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="2fab8-114">Essa imagem é inserida na guia ativa do navegador. Siga as etapas abaixo para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="2fab8-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="2fab8-115">Remover a imagem do pop-up e substituí-la por um botão</span><span class="sxs-lookup"><span data-stu-id="2fab8-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="2fab8-116">Primeiro, atualize o `popup.html` arquivo com uma marcação direta que exiba um título e um botão.</span><span class="sxs-lookup"><span data-stu-id="2fab8-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="2fab8-117">Você programará esse botão em breve, mas, por enquanto, simplesmente incluirá uma referência a um arquivo JavaScript vazio `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="2fab8-118">Aqui está a atualização de HTML.</span><span class="sxs-lookup"><span data-stu-id="2fab8-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="2fab8-119">Depois de atualizar e abrir a extensão, um pop-up abre com um botão de exibição.</span><span class="sxs-lookup"><span data-stu-id="2fab8-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   <span data-ttu-id="2fab8-121">popup.htmexibição de l após pressionar o ícone de extensão</span><span class="sxs-lookup"><span data-stu-id="2fab8-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="2fab8-122">Atualizar estratégia para exibir imagem na parte superior da guia do navegador</span><span class="sxs-lookup"><span data-stu-id="2fab8-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="2fab8-123">Depois de adicionar o botão, a próxima tarefa é fazer com que ele traga o `images/stars.jpeg` arquivo de imagem na parte superior da página da guia ativa.</span><span class="sxs-lookup"><span data-stu-id="2fab8-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="2fab8-124">Lembre-se de que cada página da guia funciona em seu próprio thread.</span><span class="sxs-lookup"><span data-stu-id="2fab8-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="2fab8-125">Além disso, a extensão usa um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="2fab8-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="2fab8-126">Primeiro, crie um script de conteúdo que é injetado na página da guia.</span><span class="sxs-lookup"><span data-stu-id="2fab8-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="2fab8-127">Em seguida, envie uma mensagem do seu pop-up para esse script de conteúdo em execução na página da guia.</span><span class="sxs-lookup"><span data-stu-id="2fab8-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="2fab8-128">O script de conteúdo recebe a mensagem, que descreve qual imagem deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="2fab8-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="2fab8-129">Criar o JavaScript pop-up para enviar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="2fab8-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="2fab8-130">Primeiro, crie `popup/popup.js` e adicione código para enviar uma mensagem para o script de conteúdo ainda não criado que você deve criar e injetar momentaneamente na guia do navegador.  Para fazer isso, o código a seguir adiciona um `onclick` evento ao seu botão pop-up de exibição.</span><span class="sxs-lookup"><span data-stu-id="2fab8-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="2fab8-131">No `onclick` evento, localize a guia atual do navegador.  Em seguida, use a `chrome.tabs.sendmessage` API de extensão para enviar uma mensagem para essa guia.</span><span class="sxs-lookup"><span data-stu-id="2fab8-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="2fab8-132">Nessa mensagem, você deve incluir a URL para a imagem que você deseja exibir.</span><span class="sxs-lookup"><span data-stu-id="2fab8-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="2fab8-133">Além disso, envie uma ID exclusiva para atribuir à imagem inserida.</span><span class="sxs-lookup"><span data-stu-id="2fab8-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="2fab8-134">Você pode optar por permitir que o JavaScript de inserção de conteúdo gere isso, mas por motivos que se tornam aparentes mais tarde, gere essa identificação exclusiva aqui `popup.js` e passe-a para o script de conteúdo ainda não criado.</span><span class="sxs-lookup"><span data-stu-id="2fab8-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="2fab8-135">O trecho de código a seguir descreve o código atualizado em `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="2fab8-136">Além disso, passe a ID da guia atual, que é usada posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="2fab8-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="2fab8-137">Disponibilizar seus estrelas. jpeg em qualquer guia do navegador</span><span class="sxs-lookup"><span data-stu-id="2fab8-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="2fab8-138">Provavelmente, você deve estar se perguntando por que, quando você passar, `images/stars.jpeg` deve usar a `chrome.extension.getURL` API de extensão Chrome em vez de apenas transmitir a URL relativa sem o prefixo adicional, como na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="2fab8-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="2fab8-139">A propósito, esse prefixo extra, retornado por `getUrl` com a imagem anexada tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="2fab8-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="2fab8-140">O motivo é que você está injetando a imagem usando o `src` atributo do `img` elemento na página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2fab8-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="2fab8-141">A página de conteúdo está em execução em um thread exclusivo que não é igual ao thread que executa a extensão.</span><span class="sxs-lookup"><span data-stu-id="2fab8-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="2fab8-142">Você deve expor o arquivo de imagem estática como um ativo da Web para que ele funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="2fab8-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="2fab8-143">Adicione outra entrada no `manifest.json` arquivo para declarar que a imagem está disponível para todas as guias do navegador.</span><span class="sxs-lookup"><span data-stu-id="2fab8-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="2fab8-144">Essa entrada é a seguinte \ (você deve vê-la no `manifest.json` arquivo completo abaixo quando adiciona a declaração de script de conteúdo que está chegando \).</span><span class="sxs-lookup"><span data-stu-id="2fab8-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="2fab8-145">Agora você escreveu o código em seu `popup.js` arquivo para enviar uma mensagem para a página de conteúdo que está inserida na página da guia ativa atual, mas você não criou e injetau essa página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2fab8-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="2fab8-146">Faça isso agora.</span><span class="sxs-lookup"><span data-stu-id="2fab8-146">Do that now.</span></span>  

5.  <span data-ttu-id="2fab8-147">Atualize o seu manifest.jspara obter conteúdo e acesso à Web</span><span class="sxs-lookup"><span data-stu-id="2fab8-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="2fab8-148">A atualização `manifest.json` que inclui o `content-scripts` e `web_accessible_resources` é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="2fab8-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="2fab8-149">A seção que você adicionou está `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="2fab8-150">O `matches` atributo é definido como `<all_urls>` , o que significa que todos os arquivos `content_scripts` são injetados em todas as páginas da guia do navegador quando cada guia é carregada.</span><span class="sxs-lookup"><span data-stu-id="2fab8-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="2fab8-151">Os tipos de arquivos permitidos que podem ser injetados são JavaScript e CSS.</span><span class="sxs-lookup"><span data-stu-id="2fab8-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="2fab8-152">Você também adicionou `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="2fab8-153">Você pode incluir isso do download mencionado na parte superior da seção.</span><span class="sxs-lookup"><span data-stu-id="2fab8-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="2fab8-154">Adicionar jQuery e noções básicas sobre o thread associado</span><span class="sxs-lookup"><span data-stu-id="2fab8-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="2fab8-155">Nos scripts de conteúdo que você está injetando, planeje o uso do jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="2fab8-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="2fab8-156">Você adicionou uma versão minified do jQuery e a coloca em seu pacote de extensão como `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="2fab8-157">Esses scripts de conteúdo são executados em caixas de proteção individuais, o que significa que o jQuery injetado na `popup.js` página não é compartilhado com o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2fab8-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="2fab8-158">Lembre-se de que, mesmo se a guia do navegador tiver JavaScript em execução na página da Web carregada, qualquer conteúdo injetado não terá acesso a isso.</span><span class="sxs-lookup"><span data-stu-id="2fab8-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="2fab8-159">Que injetado JavaScript apenas tem acesso ao DOM real carregado na guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="2fab8-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="2fab8-160">Adicionar o ouvinte de mensagem de script de conteúdo</span><span class="sxs-lookup"><span data-stu-id="2fab8-160">Add the content script message listener</span></span>  

<span data-ttu-id="2fab8-161">Aqui está `content-scripts\content.js` um arquivo que é injetado em cada página da guia do navegador com base na sua `manifest.json` `content-scripts` seção.</span><span class="sxs-lookup"><span data-stu-id="2fab8-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="2fab8-162">Observe que todas as opções JavaScript a seguir são registradas `listener` usando o `chrome.runtime.onMessage.addListener` método de API de extensão.</span><span class="sxs-lookup"><span data-stu-id="2fab8-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="2fab8-163">Esse ouvinte aguarda mensagens como a que você enviou do `popup.js` descrito anteriormente com o método de `chrome.tabs.sendMessage` API de extensão.</span><span class="sxs-lookup"><span data-stu-id="2fab8-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="2fab8-164">O primeiro parâmetro do `addListener` método é uma função cujo primeiro parâmetro, solicitação, é o detalhe da mensagem que está sendo transmitida.</span><span class="sxs-lookup"><span data-stu-id="2fab8-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="2fab8-165">Lembre-se, de `popup.js` quando você usou o `sendMessage` método, esses atributos do primeiro parâmetro são `url` e `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="2fab8-166">Quando um evento é processado pelo ouvinte, a função que é o primeiro parâmetro é executada.</span><span class="sxs-lookup"><span data-stu-id="2fab8-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="2fab8-167">O primeiro parâmetro dessa função é um objeto com atributos como atribuído por `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="2fab8-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="2fab8-168">Essa função simplesmente processa as três linhas de script do jQuery.</span><span class="sxs-lookup"><span data-stu-id="2fab8-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="2fab8-169">A primeira linha de script insere dinamicamente no cabeçalho DOM uma **\<style\>** seção que você deve atribuir como uma `slide-image` classe ao seu `img` elemento.</span><span class="sxs-lookup"><span data-stu-id="2fab8-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="2fab8-170">A segunda linha de script acrescenta um `img` elemento logo abaixo da `body` Guia do navegador que tem a `slide-image` classe atribuída, bem como a `imageDivId` ID do elemento da imagem.</span><span class="sxs-lookup"><span data-stu-id="2fab8-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="2fab8-171">A terceira linha de script adiciona um `click` evento que abrange toda a imagem, permitindo que o usuário selecione qualquer lugar na imagem e essa imagem seja removida da página \ (juntamente com é ouvinte de evento \).</span><span class="sxs-lookup"><span data-stu-id="2fab8-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="2fab8-172">Adicionar funcionalidade para remover a imagem exibida quando selecionada</span><span class="sxs-lookup"><span data-stu-id="2fab8-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="2fab8-173">Agora, quando você navegar em qualquer página e selecionar o ícone da **extensão** , o menu pop-up será exibido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="2fab8-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   <span data-ttu-id="2fab8-175">popup.htmexibição de l após pressionar o ícone de extensão</span><span class="sxs-lookup"><span data-stu-id="2fab8-175">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="2fab8-176">Ao selecionar o `Display` botão, você obtém o que está abaixo.</span><span class="sxs-lookup"><span data-stu-id="2fab8-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="2fab8-177">Se você selecionar qualquer lugar da `stars.jpeg` imagem, esse elemento de imagem será removido e as páginas da guia serão recolhidas para o que foi exibido originalmente.</span><span class="sxs-lookup"><span data-stu-id="2fab8-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="popup.htmexibição de l após pressionar o ícone de extensão":::
   <span data-ttu-id="2fab8-179">A imagem exibida no navegador</span><span class="sxs-lookup"><span data-stu-id="2fab8-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="2fab8-180">Você criou uma extensão que envia uma mensagem com êxito do ícone de extensão pop-up e JavaScript inserido dinamicamente executando como conteúdo na guia do navegador.  O conteúdo injetado define o elemento Image para exibir seu JPEG de estrelas estática.</span><span class="sxs-lookup"><span data-stu-id="2fab8-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Fonte do pacote de extensão concluída | Documentos da Microsoft"  
