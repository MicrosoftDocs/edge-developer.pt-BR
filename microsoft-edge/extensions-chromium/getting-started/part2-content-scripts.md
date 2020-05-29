---
description: Extensões sendo iniciadas parte 1
title: Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: b37184f0188b72ec868ab3de3f2341c0694ee42c
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683641"
---
# <span data-ttu-id="7d1fb-104">Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página usando scripts de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7d1fb-104">Dynamically Insert NASA Picture Below The Page Body Tag Using Content Scripts</span></span>  
  
[<span data-ttu-id="7d1fb-105">Origem do pacote de extensão concluída para esta parte</span><span class="sxs-lookup"><span data-stu-id="7d1fb-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]  

## <span data-ttu-id="7d1fb-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="7d1fb-106">Overview</span></span>  

<span data-ttu-id="7d1fb-107">Na parte 2, você aprende a atualizar o menu pop-up para não mostrar a imagem de estrelas estática que havia antes, mas para substituir essa imagem por um título e um botão HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-107">In part 2, you learn to update your pop-up menu to not show the static stars image you had before, but to replace that image with a title and a standard HTML button.</span></span>  <span data-ttu-id="7d1fb-108">Quando selecionado, esse botão passa essa imagem de estrelas, que é inserida na extensão, para a página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-108">That button, when selected, passes that stars image, which is embedded in the Extension, to the content page.</span></span>  <span data-ttu-id="7d1fb-109">Essa imagem é inserida na guia ativa do navegador.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-109">That image, is inserted into the active browser tab.</span></span>  

*   <span data-ttu-id="7d1fb-110">Tecnologias de extensão abordadas neste guia</span><span class="sxs-lookup"><span data-stu-id="7d1fb-110">Extension technologies covered in this guide</span></span>  
    *   <span data-ttu-id="7d1fb-111">Injetando bibliotecas JavaScript na extensão</span><span class="sxs-lookup"><span data-stu-id="7d1fb-111">Injecting JavaScript libraries into Extension</span></span>  
    *   <span data-ttu-id="7d1fb-112">Expondo ativos de extensão a guias do navegador</span><span class="sxs-lookup"><span data-stu-id="7d1fb-112">Exposing Extension assets to browser tabs</span></span>  
    *   <span data-ttu-id="7d1fb-113">Incluindo páginas de conteúdo em guias existentes do navegador</span><span class="sxs-lookup"><span data-stu-id="7d1fb-113">Including content pages in existing browser tabs</span></span>  
    *   <span data-ttu-id="7d1fb-114">Fazer com que as páginas de conteúdo escutem mensagens de pop-ups e respondam</span><span class="sxs-lookup"><span data-stu-id="7d1fb-114">Having content pages listen for messages from pop-ups and respond</span></span>  

## <span data-ttu-id="7d1fb-115">Remover a imagem do pop-up e substituí-la por um botão</span><span class="sxs-lookup"><span data-stu-id="7d1fb-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="7d1fb-116">Primeiro, atualize o `popup.html` arquivo com uma marcação direta que exiba um título e um botão.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="7d1fb-117">Você programará esse botão em breve, mas, por enquanto, simplesmente incluirá uma referência a um arquivo JavaScript vazio `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-117">You program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="7d1fb-118">Aqui está a atualização de HTML.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="7d1fb-119">Depois de atualizar a extensão e selecionar o ícone de inicialização da extensão, o seguinte pop-up inclui um botão de exibição.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-119">After updating your Extension and selecting the Extension launch icon, the have the following pop-up includes a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="pop-up. html exibido após pressionar o ícone de extensão":::
   <span data-ttu-id="7d1fb-121">pop-up. html exibido após pressionar o ícone de extensão</span><span class="sxs-lookup"><span data-stu-id="7d1fb-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## <span data-ttu-id="7d1fb-122">Estratégia atualizada para exibir imagem na parte superior da guia do navegador</span><span class="sxs-lookup"><span data-stu-id="7d1fb-122">Updated strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="7d1fb-123">Depois de adicionar o botão, a próxima tarefa é fazer com que ele traga o `images/stars.jpeg` arquivo de imagem na parte superior da página da guia ativa.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="7d1fb-124">Lembre-se de que cada página da guia tem um thread exclusivo e a extensão tem um thread separado.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-124">Remember, each tab page has a unique own thread and the Extension has a separate thread.</span></span>  <span data-ttu-id="7d1fb-125">Portanto, primeiro você deve criar um script de conteúdo e injetar esse script na página da guia.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-125">So, you must first create a content script and inject that content script into the tab page.</span></span>  <span data-ttu-id="7d1fb-126">Depois de fazer isso, você deve enviar uma mensagem do seu pop-up para esse script de conteúdo em execução na página da guia que informa que o script de conteúdo é a imagem a ser mostrada e como mostrá-la.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-126">Once you do that, you must send a message from your pop-up to that content script running on the tab page telling that content script what image to show, and how to show it.</span></span>  

## <span data-ttu-id="7d1fb-127">Criando o JavaScript pop-up para enviar uma mensagem</span><span class="sxs-lookup"><span data-stu-id="7d1fb-127">Creating the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="7d1fb-128">Primeiro, crie `popup/popup.js` e adicione código para enviar uma mensagem para o script de conteúdo ainda não criado que você deve criar e injetar momentaneamente na guia do navegador.  Para fazer isso, o código a seguir adiciona um `onclick` evento ao seu botão pop-up de exibição.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-128">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="7d1fb-129">No `onclick` evento, o que você deve fazer é encontrar a guia atual do navegador \ (se houver apenas uma aberta).</span><span class="sxs-lookup"><span data-stu-id="7d1fb-129">In the `onclick` event, what you must do is find the current browser tab \(if there is only one open it is that one\).</span></span>  <span data-ttu-id="7d1fb-130">Depois disso, quando encontrar essa guia, use a `chrome.tabs.sendmessage` API de extensão para enviar uma mensagem para essa guia.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-130">Then, once you find that tab, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="7d1fb-131">Nessa mensagem, você deve incluir a URL da imagem que você deseja exibir e deseja enviar uma ID exclusiva que deve ser atribuída a essa imagem inserida.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-131">In that message you must include the URL to the image you want to display, and you want to send a unique ID that should be assigned to that inserted image.</span></span>  <span data-ttu-id="7d1fb-132">Você pode optar por permitir que o JavaScript de inserção de conteúdo gere isso, mas por motivos que se tornam aparentes mais tarde, gere essa identificação exclusiva aqui `popup.js` e passe-a para o script de conteúdo ainda não criado.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-132">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="7d1fb-133">Aqui está o `popup/popup.js` arquivo atualizado.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-133">Here is your updated `popup/popup.js` file.</span></span>  <span data-ttu-id="7d1fb-134">Além disso, passe a ID da guia atual que você deve precisar em uma seção posterior, mas por enquanto, não será usado.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-134">Also, pass in the current tab ID which you should need in a later section but for now, is not be used.</span></span>  

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

## <span data-ttu-id="7d1fb-135">Disponibilizar seus estrelas. jpeg em qualquer guia do navegador</span><span class="sxs-lookup"><span data-stu-id="7d1fb-135">Making your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="7d1fb-136">Provavelmente, você deve estar se perguntando por que, quando você passar, `images/stars.jpeg` deve usar a `chrome.extension.getURL` API de extensão Chrome em vez de apenas transmitir a URL relativa sem o prefixo adicional, como na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-136">You are probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="7d1fb-137">A propósito, esse prefixo extra, retornado por `getUrl` com a imagem anexada tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="7d1fb-137">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="7d1fb-138">O motivo é que você está injetando a imagem usando o `src` atributo do `img` elemento na página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-138">The reason is that you are injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="7d1fb-139">A página de conteúdo está em execução em um thread exclusivo que não é igual ao thread que executa a extensão.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-139">The content page is running on a unique thread that is not the same as the thread running the Extension.</span></span>  <span data-ttu-id="7d1fb-140">Você deve expor o arquivo de imagem estática como um ativo da Web para que ele funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-140">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="7d1fb-141">Para fazer isso, você deve adicionar outra entrada no `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-141">To do that, you must add another entry in the `manifest.json` file.</span></span>  <span data-ttu-id="7d1fb-142">Você deve declarar a imagem para ser acessível em qualquer guia do navegador.  Essa entrada é a seguinte \ (você deve vê-la no `manifest.json` arquivo completo abaixo quando adiciona a declaração de script de conteúdo que está chegando \).</span><span class="sxs-lookup"><span data-stu-id="7d1fb-142">You must declare the image to be accessible from any browser tab.  That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="7d1fb-143">Agora você escreveu o código em seu `popup.js` arquivo para enviar uma mensagem para a página de conteúdo que está inserida na página da guia ativa atual, mas você não criou e injetau essa página de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-143">You have now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you have not created and injected that content page.</span></span>  <span data-ttu-id="7d1fb-144">Faça isso agora.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-144">Do that now.</span></span>  

## <span data-ttu-id="7d1fb-145">Atualizando o manifest. JSON para conteúdo e Web Access</span><span class="sxs-lookup"><span data-stu-id="7d1fb-145">Updating your manifest.json for content and web access</span></span>  

<span data-ttu-id="7d1fb-146">A atualização `manifest.json` que inclui o `content-scripts` e `web_accessible_resources` é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-146">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="7d1fb-147">A seção que você adicionou está `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-147">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="7d1fb-148">O atributo `matches` é definido para `<all_urls>` significar que todos os arquivos mencionados na seção **content_scripts** são injetados em todas as páginas da guia do navegador quando cada um é carregado.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-148">The attribute `matches` set to `<all_urls>` means that all the files mention in the **content_scripts** section is injected into all browser tab pages when each are loaded.</span></span>  <span data-ttu-id="7d1fb-149">Os tipos permitidos de arquivos que podem ser injetados aqui são JavaScript e CSS.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-149">The allowable types of files that are able to be injected here are javascript and css.</span></span>  <span data-ttu-id="7d1fb-150">Você também adicionou `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-150">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="7d1fb-151">Você pode incluir isso do download mencionado na parte superior da seção.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-151">You are able to include that from the download mentioned at the top of the section.</span></span>  

## <span data-ttu-id="7d1fb-152">Adicionando o jQuery e compreendendo o thread associado</span><span class="sxs-lookup"><span data-stu-id="7d1fb-152">Adding jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="7d1fb-153">Nos scripts de conteúdo que você estiver injetando, planeje o uso do jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="7d1fb-153">In the content scripts you are injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="7d1fb-154">Você adicionou uma versão minified do jQuery e a coloca em seu pacote de extensão como `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-154">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="7d1fb-155">Esses scripts de conteúdo são executados em uma área restrita de classificações individuais, o que significa que o jQuery injetado na `popup.js` página não compartilha com o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-155">These content scripts run in an individual sandbox of sorts, which means that the jQuery injected into the `popup.js` page does not share with the content.</span></span>  

<span data-ttu-id="7d1fb-156">Lembre-se de que, mesmo se a guia do navegador tiver JavaScript em execução na página da Web carregada, qualquer conteúdo injetado não terá acesso a isso.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-156">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected does not have access to that.</span></span>  <span data-ttu-id="7d1fb-157">Que injetado JavaScript apenas tem acesso ao DOM real carregado na guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-157">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

## <span data-ttu-id="7d1fb-158">Adicionando o ouvinte de mensagem de script de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7d1fb-158">Adding the content script message listener</span></span>  

<span data-ttu-id="7d1fb-159">Aqui está `content-scripts\content.js` um arquivo que é injetado em cada página da guia do navegador com base na sua `manifest.json` `content-scripts` seção.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-159">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="7d1fb-160">Observe que todas as opções JavaScript a seguir são registradas `listener` usando o `chrome.runtime.onMessage.addListener` método de API de extensão.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-160">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="7d1fb-161">Esse ouvinte aguarda mensagens como a que você enviou do `popup.js` descrito anteriormente com o método de `chrome.tabs.sendMessage` API de extensão.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-161">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="7d1fb-162">O primeiro parâmetro do `addListener` método é uma função cujo primeiro parâmetro, solicitação, é o detalhe da mensagem que está sendo transmitida.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-162">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="7d1fb-163">Lembre-se, de `popup.js` quando você usou o `sendMessage` método, esses atributos do primeiro parâmetro são `url` e `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-163">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="7d1fb-164">Quando um evento é processado pelo ouvinte, a função que é o primeiro parâmetro é executada.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-164">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="7d1fb-165">O primeiro parâmetro dessa função é um objeto com atributos como atribuído por `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-165">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="7d1fb-166">Essa função simplesmente processa as três linhas de script do jQuery.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-166">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="7d1fb-167">A primeira insere dinamicamente no cabeçalho DOM uma **\<style\>** seção que você deve atribuir como uma `slide-image` classe ao `img` elemento.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-167">The first dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="7d1fb-168">O segundo, acrescenta um `img` elemento à direita abaixo da `body` Guia do navegador que tem a `slide-image` classe atribuída, bem como a `imageDivId` ID do elemento da imagem.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-168">The second, appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="7d1fb-169">O terceiro adiciona um `click` evento que abrange toda a imagem, permitindo que o usuário selecione qualquer local na imagem e essa imagem seja removida da página \ (juntamente com é ouvinte de evento \).</span><span class="sxs-lookup"><span data-stu-id="7d1fb-169">The third adds a `click` event that covers the entire image allowing the user to select any place on the image and that image is be removed from the page \(along with it is event listener\).</span></span>  

## <span data-ttu-id="7d1fb-170">Adicionando funcionalidade para remover a imagem exibida quando selecionada</span><span class="sxs-lookup"><span data-stu-id="7d1fb-170">Adding functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="7d1fb-171">Agora, quando você navegar em qualquer página e selecionar o ícone da **extensão** , o menu pop-up será exibido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-171">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="pop-up. html exibido após pressionar o ícone de extensão":::
   <span data-ttu-id="7d1fb-173">pop-up. html exibido após pressionar o ícone de extensão</span><span class="sxs-lookup"><span data-stu-id="7d1fb-173">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="7d1fb-174">Ao selecionar o `Display` botão, você obtém o que está abaixo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-174">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="7d1fb-175">Se você selecionar qualquer lugar da `stars.jpeg` imagem, esse elemento de imagem será removido e as páginas da guia serão recolhidas para o que foi exibido originalmente.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-175">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="A imagem exibida no navegador":::
   <span data-ttu-id="7d1fb-177">A imagem exibida no navegador</span><span class="sxs-lookup"><span data-stu-id="7d1fb-177">The image showing in browser</span></span>
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

<span data-ttu-id="7d1fb-178">Você criou uma extensão que envia com sucesso uma mensagem do pop-up de ícone de extensão para o JavaScript inserido dinamicamente executando como conteúdo na guia do navegador.  Que o conteúdo injetado define o elemento Image para exibir seu JPEG de estrelas estática.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-178">You have now created an Extension that successfully sends a message from the Extension icon pop-up, to the dynamically inserted JavaScript running as content on the browser tab.  That injected content set the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Fonte do pacote de extensão concluída para esta parte | Documentos da Microsoft"  