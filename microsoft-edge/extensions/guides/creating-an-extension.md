---
description: Saiba como criar uma extensão do Microsoft Edge
title: Criando uma extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683648"
---
# <span data-ttu-id="698a1-104">Criando uma extensão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="698a1-104">Creating A Microsoft Edge Extension</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="698a1-105">Neste guia, aprenda a criar uma extensão para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="698a1-105">In this guide, learn to create an extension for Microsoft Edge.</span></span>  <span data-ttu-id="698a1-106">Este exemplo de extensão permite manipular um CSS específico para páginas [docs.Microsoft.com][MicrosoftDocs] , incluindo a criação de um arquivo de manifesto, a interface do usuário e scripts de tela de fundo e de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="698a1-106">This example extension allows you to manipulate specific CSS for [docs.microsoft.com][MicrosoftDocs] pages including walking you through creation of a manifest file, the user interface, and background and content scripts.</span></span>  

:::image type="complex" source="../media/color-changer_header.png" alt-text="O corpo do Docs.microsoft.com é alterado para azul":::
   <span data-ttu-id="698a1-108">O corpo do Docs.microsoft.com é alterado para azul</span><span class="sxs-lookup"><span data-stu-id="698a1-108">Docs.microsoft.com body changed to blue</span></span>
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

<span data-ttu-id="698a1-109">Este tutorial pressupõe que você tenha noções básicas sobre o que é uma extensão de navegador e como ela funciona.</span><span class="sxs-lookup"><span data-stu-id="698a1-109">This tutorial assumes you have basic understanding of what a browser extension is and how it work.</span></span>  <span data-ttu-id="698a1-110">Para obter mais imformation sobre os blocos de construção para extensões, consulte [anatomia de uma extensão][MDNAnatomyExtension].</span><span class="sxs-lookup"><span data-stu-id="698a1-110">For more imformation about the building blocks for extensions, see [Anatomy of an extension][MDNAnatomyExtension].</span></span>  

<span data-ttu-id="698a1-111">Baixe o código para o [exemplo completo no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="698a1-111">Download the code for the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="698a1-112">Criando o arquivo de manifesto</span><span class="sxs-lookup"><span data-stu-id="698a1-112">Building the manifest file</span></span>  

<span data-ttu-id="698a1-113">Para começar, crie um diretório para a sua extensão e nomeie-o `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="698a1-113">To begin, create a directory for your extension and name it `color-changer`.</span></span>  

<span data-ttu-id="698a1-114">Na `color-changer` pasta, crie um arquivo chamado `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="698a1-114">Inside the `color-changer` folder, create a file named `manifest.json`.</span></span>  <span data-ttu-id="698a1-115">O `manifest.json` arquivo é necessário para todas as extensões e fornece informações importantes para a extensão, variando do nome da extensão às permissões.</span><span class="sxs-lookup"><span data-stu-id="698a1-115">The `manifest.json` file is required for all extensions and provides important information for the extension, ranging from the extension name to the permissions.</span></span>  

> [!NOTE] 
> <span data-ttu-id="698a1-116">Este guia o orienta através de todas as chaves de manifesto que você deve usar neste guia, mas para obter uma lista de todas as chaves de manifesto recomendadas e compatíveis, consulte [chaves de manifesto com suporte][ExtensionsApisupportManifestKeys].</span><span class="sxs-lookup"><span data-stu-id="698a1-116">This guide walks you through all the manifest keys you must use in this guide, but for a list of all supported and recommended manifest keys, see [Supported manifest keys][ExtensionsApisupportManifestKeys].</span></span>  

<span data-ttu-id="698a1-117">Dentro `manifest.json` , adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="698a1-117">Inside `manifest.json`, add the following code.</span></span>  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### <span data-ttu-id="698a1-118">Definições da chave do manifesto</span><span class="sxs-lookup"><span data-stu-id="698a1-118">Manifest key definitions</span></span>  

| <span data-ttu-id="698a1-119">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-119">Key</span></span> | <span data-ttu-id="698a1-120">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-120">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="698a1-121">name</span><span class="sxs-lookup"><span data-stu-id="698a1-121">name</span></span>][MDNManifestjsonName] | <span data-ttu-id="698a1-122">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-122">The name of the extension.</span></span>  |  
| [<span data-ttu-id="698a1-123">autor</span><span class="sxs-lookup"><span data-stu-id="698a1-123">author</span></span>][MDNManifestjsonAuthor] | <span data-ttu-id="698a1-124">O autor da extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-124">The author of the extension.</span></span>  |  
| [<span data-ttu-id="698a1-125">version</span><span class="sxs-lookup"><span data-stu-id="698a1-125">version</span></span>][MDNManifestjsonVersion] | <span data-ttu-id="698a1-126">O número da versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-126">The extension version number.</span></span>  |  
| [<span data-ttu-id="698a1-127">description</span><span class="sxs-lookup"><span data-stu-id="698a1-127">description</span></span>][MDNManifestjsonDescription] | <span data-ttu-id="698a1-128">A descrição da extensão exibida na seção sobre do menu extensão no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="698a1-128">The description of the extension displayed in the About section of the extension menu in Microsoft Edge.</span></span>  |  
| [<span data-ttu-id="698a1-129">Elas</span><span class="sxs-lookup"><span data-stu-id="698a1-129">permissions</span></span>][MDNManifestjsonPermissions] | <span data-ttu-id="698a1-130">Uma matriz de cadeias de caracteres que solicitam permissões para a extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-130">An array of strings requesting permissions for the extension.</span></span>  <span data-ttu-id="698a1-131">Para sua extensão, você está solicitando permissões para ver os sites visitados \ ("guias" \) e para atualizar o conteúdo em URLs correspondentes a " `*://docs.microsoft.com/*` ".</span><span class="sxs-lookup"><span data-stu-id="698a1-131">For your extension, you are requesting permissions to see the websites visited \("tabs"\) and to update content on URLs matching "`*://docs.microsoft.com/*`".</span></span>  |  
| [<span data-ttu-id="698a1-132">browser_action</span><span class="sxs-lookup"><span data-stu-id="698a1-132">browser_action</span></span>][MDNManifestjsonBrowserAction] | <span data-ttu-id="698a1-133">Contém as informações para um ícone.</span><span class="sxs-lookup"><span data-stu-id="698a1-133">Contains the information for an icon.</span></span> <span data-ttu-id="698a1-134">O ícone é colocado na barra de ferramentas do Microsoft Edge, à direita da barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="698a1-134">The icon is placed on the Microsoft Edge toolbar, to the right of the address bar.</span></span>  |  

#### <span data-ttu-id="698a1-135">definições de chave browser_action</span><span class="sxs-lookup"><span data-stu-id="698a1-135">browser_action Key definitions</span></span>  

| <span data-ttu-id="698a1-136">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-136">Key</span></span> | <span data-ttu-id="698a1-137">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-137">Details</span></span> |  
|:--- |:--- |  
| `default_icon` | <span data-ttu-id="698a1-138">O ícone usado na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="698a1-138">The icon that is used in the toolbar.</span></span>  |  
| `default_title` | <span data-ttu-id="698a1-139">O texto que é exibido quando um usuário passa o mouse sobre o ícone na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="698a1-139">The text that is displayed when a user hovers over the icon in the toolbar.</span></span>  |  
| `default_popup` | <span data-ttu-id="698a1-140">O caminho para o arquivo HTML da janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="698a1-140">The path to the HTML file for the pop-up window.</span></span>  |  

<span data-ttu-id="698a1-141">Agora que você criou o arquivo de manifesto, precisa de uma interface do usuário para a extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-141">Now that you have created the manifest file, you need a user interface for the extension.</span></span>  

## <span data-ttu-id="698a1-142">Criando o pop-up</span><span class="sxs-lookup"><span data-stu-id="698a1-142">Creating the pop-up</span></span>  

<span data-ttu-id="698a1-143">Para sua extensão, crie um pop-up para a interface do usuário, como abaixo.</span><span class="sxs-lookup"><span data-stu-id="698a1-143">For your extension, create a pop-up for the user interface, like below.</span></span>  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="A interface pop-up da extensão":::
   <span data-ttu-id="698a1-145">A interface pop-up da extensão</span><span class="sxs-lookup"><span data-stu-id="698a1-145">The pop-up interface of the extension</span></span>
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

<span data-ttu-id="698a1-146">Crie um arquivo chamado `popup.html` na raiz da `color-changer` pasta.</span><span class="sxs-lookup"><span data-stu-id="698a1-146">Create a file named `popup.html` in the root of your `color-changer` folder.</span></span>  <span data-ttu-id="698a1-147">Cole o código a seguir em `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="698a1-147">Paste the following code into `popup.html`.</span></span>  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="698a1-148">No `popup.html` , você cria um título, um parágrafo e três botões \ (AliceBlue, Cornsilk e reset \).</span><span class="sxs-lookup"><span data-stu-id="698a1-148">In `popup.html`, you create a title, a paragraph, and three buttons \(Aliceblue, Cornsilk, and Reset\).</span></span>  

<span data-ttu-id="698a1-149">Agora, crie uma pasta chamada `css` e dentro crie um arquivo chamado `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="698a1-149">Now create a folder named `css` and inside create a file named `styles.css`.</span></span>  <span data-ttu-id="698a1-150">Adicione os estilos abaixo.</span><span class="sxs-lookup"><span data-stu-id="698a1-150">Add the styles below.</span></span>  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

<span data-ttu-id="698a1-151">Esse CSS dá à nossa extensão alguns estilos básicos.</span><span class="sxs-lookup"><span data-stu-id="698a1-151">This CSS gives our extension some basic styles.</span></span>  <span data-ttu-id="698a1-152">Sinta-se à vontade para adicionar mais estilos para personalizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-152">Feel free to add more styles to customize your extension.</span></span>  

<span data-ttu-id="698a1-153">Em seguida, você deve criar o arquivo JavaScript que interage com o pop-up.</span><span class="sxs-lookup"><span data-stu-id="698a1-153">Next, you must create the JavaScript file that interacts with the pop-up.</span></span>  <span data-ttu-id="698a1-154">Crie uma `js` pasta e um arquivo nomeado `popup.js` dentro.</span><span class="sxs-lookup"><span data-stu-id="698a1-154">Create a `js` folder and a file named `popup.js` inside.</span></span>  <span data-ttu-id="698a1-155">Atualize `popup.js` com o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="698a1-155">Update `popup.js` with the following code.</span></span>  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

<span data-ttu-id="698a1-156">No `popup.js` , a API de [guias][MDNApiTabs] permite que você interaja com as guias do navegador e injeta scripts e estilos no conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="698a1-156">In `popup.js`, the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span></span>  <span data-ttu-id="698a1-157">Usando o método [Tabs. insertCSS ()][MDNApiTabsInsertcss] , você INJETA a CSS especificada na página que altera o cabeçalho em [docs.Microsoft.com][MicrosoftDocs] para uma cor diferente quando o botão especificado é clicado.</span><span class="sxs-lookup"><span data-stu-id="698a1-157">Using the [tabs.insertCSS()][MDNApiTabsInsertcss] method, you inject the specified CSS into the page which changes the header on [docs.microsoft.com][MicrosoftDocs] to a different color when the specified button is clicked.</span></span>  

<span data-ttu-id="698a1-158">Agora que você tem a funcionalidade pop-up básica, adicione ícones à extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-158">Now that you have the basic pop-up functionality, add icons to the extension.</span></span>  

## <span data-ttu-id="698a1-159">Adicionando ícones</span><span class="sxs-lookup"><span data-stu-id="698a1-159">Adding icons</span></span>  

<span data-ttu-id="698a1-160">Os ícones são usados para representar a extensão na barra de ferramentas do navegador, o menu extensões e outros locais.</span><span class="sxs-lookup"><span data-stu-id="698a1-160">Icons are used to represent the extension in the browser toolbar, the extensions menu, and other places.</span></span>  <span data-ttu-id="698a1-161">Baixe os [ícones da extensão no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span><span class="sxs-lookup"><span data-stu-id="698a1-161">Download the [icons for your extension on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span></span> <span data-ttu-id="698a1-162">Para obter mais informações sobre ícones de extensão no Microsoft Edge, consulte [Guia de design][ExtensionsGuidesDesignIcons].</span><span class="sxs-lookup"><span data-stu-id="698a1-162">For more information about extension icons in Microsoft Edge, see [Design Guide][ExtensionsGuidesDesignIcons].</span></span>  

<span data-ttu-id="698a1-163">Depois de baixar os ícones de extensão, salve os ícones em uma `images` pasta dentro `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="698a1-163">After you download the extension icons, save the icons in an `images` folder inside `color-changer`.</span></span>  

<span data-ttu-id="698a1-164">O ícone que aparece na barra de ferramentas é definido usando-se `default_icon` dentro da chave [browser_action][MDNManifestjsonBrowserAction] , que você já adicionou ao arquivo de manifesto em uma seção anterior.</span><span class="sxs-lookup"><span data-stu-id="698a1-164">The icon that appears in the toolbar is set using `default_icon` inside of the [browser_action][MDNManifestjsonBrowserAction] key, which you already added to your manifest file in an earlier section.</span></span>  

<span data-ttu-id="698a1-165">A `icons` chave define quais ícones devem ser usados nos menus de configurações de extensões.</span><span class="sxs-lookup"><span data-stu-id="698a1-165">The `icons` key defines which icons should be used in the Extensions settings menus.</span></span>  <span data-ttu-id="698a1-166">Abaixo, você está especificando vários ícones com diferentes tamanhos para fazer uma conta com diferentes resoluções de tela.</span><span class="sxs-lookup"><span data-stu-id="698a1-166">Below, you are specifying multiple icons with different sizes to account for different screen resolutions.</span></span>  <span data-ttu-id="698a1-167">O nome dos ícones `25` e `48` a altura em pixels dos ícones.</span><span class="sxs-lookup"><span data-stu-id="698a1-167">The name of the icons, `25` and `48` are the heights in pixels of the icons.</span></span>  

<span data-ttu-id="698a1-168">No arquivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , inclua uma chave de nível superior para `icons` .</span><span class="sxs-lookup"><span data-stu-id="698a1-168">In the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file, include a top-level key for `icons`.</span></span>  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### <span data-ttu-id="698a1-169">Definições da chave do manifesto</span><span class="sxs-lookup"><span data-stu-id="698a1-169">Manifest Key definitions</span></span>  

| <span data-ttu-id="698a1-170">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-170">Key</span></span> | <span data-ttu-id="698a1-171">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-171">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="698a1-172">ícones</span><span class="sxs-lookup"><span data-stu-id="698a1-172">icons</span></span>][MDNManifestjsonIcons] | <span data-ttu-id="698a1-173">Os ícones da extensão com pares chave-valor do tamanho da imagem em `px` e o caminho da imagem em relação ao diretório raiz da extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-173">The icons for your extension with key-value pairs of image size in `px` and image path relative to the root directory of the extension.</span></span> |  

> [!NOTE]
> <span data-ttu-id="698a1-174">Use os ícones nomeados `inactive##.png` localizados na pasta imagens mais adiante neste guia.</span><span class="sxs-lookup"><span data-stu-id="698a1-174">Use the icons named `inactive##.png` located in the images folder later in this guide.</span></span>  

## <span data-ttu-id="698a1-175">Testando a extensão</span><span class="sxs-lookup"><span data-stu-id="698a1-175">Testing the extension</span></span>  

<span data-ttu-id="698a1-176">Agora que você adicionou a interface do usuário e os ícones criados, teste a extensão.</span><span class="sxs-lookup"><span data-stu-id="698a1-176">Now that you have added the user interface and created icons, test your extension.</span></span>  <span data-ttu-id="698a1-177">Siga as etapas para [Adicionar uma extensão][ExtensionsGuidesAddingRemovingExtensionsAdding] ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="698a1-177">Walk through the steps for [Adding an extension][ExtensionsGuidesAddingRemovingExtensionsAdding] to Microsoft Edge.</span></span>  <span data-ttu-id="698a1-178">Depois, retorne a este guia.</span><span class="sxs-lookup"><span data-stu-id="698a1-178">Afterwards, return to this guide.</span></span>  

<span data-ttu-id="698a1-179">Depois de adicionar a extensão, navegue até qualquer página do [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="698a1-179">After you add your extension, navigate to any [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="698a1-180">Você deve ver o pop-up a seguir depois de clicar na ação do navegador.</span><span class="sxs-lookup"><span data-stu-id="698a1-180">You should see the following pop-up after clicking on the browser action.</span></span>  <span data-ttu-id="698a1-181">A cor do corpo da [docs.Microsoft.com][MicrosoftDocs] também deve mudar de cor.</span><span class="sxs-lookup"><span data-stu-id="698a1-181">The color of the [docs.microsoft.com][MicrosoftDocs] body should also change color.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="O cabeçalho Docs.microsoft.com mudou para AliceBlue":::
         <span data-ttu-id="698a1-183">O cabeçalho Docs.microsoft.com mudou para AliceBlue</span><span class="sxs-lookup"><span data-stu-id="698a1-183">Docs.microsoft.com header changed to Aliceblue</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="O cabeçalho Docs.microsoft.com mudou para Cornsilk":::
         <span data-ttu-id="698a1-185">O cabeçalho Docs.microsoft.com mudou para Cornsilk</span><span class="sxs-lookup"><span data-stu-id="698a1-185">Docs.microsoft.com header changed to Cornsilk</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

<span data-ttu-id="698a1-186">Se você encontrar erros ou funcionalidades que não funcionam, consulte o guia de [extensões de depuração][ExtensionsGuidesDebuggingExtensions] ou baixe a [amostra completa no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="698a1-186">If you encounter any errors or functionality that does not work, see the [Debugging extensions][ExtensionsGuidesDebuggingExtensions] guide or download the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="698a1-187">Adicionando conteúdo e scripts em segundo plano</span><span class="sxs-lookup"><span data-stu-id="698a1-187">Adding content and background scripts</span></span>  

<span data-ttu-id="698a1-188">Siga um passo adiante e adicione lógica para desabilitar a extensão de trabalhar em páginas fora do domínio do [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="698a1-188">Go one step further and add logic to disable the extension from working on pages outside the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  

<span data-ttu-id="698a1-189">Primeiro, você deve criar um [script de conteúdo][MDNContentScripts].</span><span class="sxs-lookup"><span data-stu-id="698a1-189">You must first create a [content script][MDNContentScripts].</span></span>  <span data-ttu-id="698a1-190">Em seguida, você deve criar scripts de conteúdo que são executados no contexto de uma determinada página da Web, podem acessar o conteúdo de uma página da Web e podem se comunicar com scripts em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="698a1-190">Next, you must create content scripts that run in the context of a particular web page, are able to access the content of a web page, and are able to communicate with background scripts.</span></span>  <span data-ttu-id="698a1-191">No seu `js` diretório, crie um arquivo denominado `content.js` e adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="698a1-191">Inside of your `js` directory, create a file named `content.js` and add the following code.</span></span>  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

<span data-ttu-id="698a1-192">Esse script Obtém a URL da página atual `document.location.href` e verifica se a página atual está no domínio [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="698a1-192">This script gets the URL of the current page through `document.location.href` and verifies whether the current page is on the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  <span data-ttu-id="698a1-193">Se a página não estiver no domínio [docs.Microsoft.com][MicrosoftDocs] \ (por exemplo, [https://www.bing.com/][|::ref1::|] \), os caminhos para os ícones inativos \ (ícones em cinza \) serão enviados para o script em segundo plano usando o [tempo de execução. SendMessage ()][MDNApiRuntimeSendmessage].</span><span class="sxs-lookup"><span data-stu-id="698a1-193">If the page is not on the [docs.microsoft.com][MicrosoftDocs] domain \(for example  [https://www.bing.com/][|::ref1::|]\), the paths to the inactive icons \(grayed out icons\) are sent to the background script using [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span></span>  

<span data-ttu-id="698a1-194">Você deve atualizar o arquivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] para incluir a chave a seguir `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="698a1-194">You must update the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file to include the following `content_scripts` key.</span></span>  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### <span data-ttu-id="698a1-195">Definições da chave do manifesto</span><span class="sxs-lookup"><span data-stu-id="698a1-195">Manifest Key definitions</span></span>  

| <span data-ttu-id="698a1-196">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-196">Key</span></span> | <span data-ttu-id="698a1-197">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-197">Details</span></span> |  
|:--- |:---- |  
| [<span data-ttu-id="698a1-198">content_scripts</span><span class="sxs-lookup"><span data-stu-id="698a1-198">content_scripts</span></span>][MDNManifestjsonContentScripts] | <span data-ttu-id="698a1-199">Contém as informações sobre quais scripts de conteúdo o navegador deve carregar.</span><span class="sxs-lookup"><span data-stu-id="698a1-199">Contains the information about which content scripts the browser should load.</span></span> |  

#### <span data-ttu-id="698a1-200">definições de chave content_scripts</span><span class="sxs-lookup"><span data-stu-id="698a1-200">content_scripts Key definitions</span></span>  

| <span data-ttu-id="698a1-201">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-201">Key</span></span> | <span data-ttu-id="698a1-202">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-202">Details</span></span> |  
|:--- |:---- |  
| `matches` <span data-ttu-id="698a1-203">\ (obrigatório \)</span><span class="sxs-lookup"><span data-stu-id="698a1-203">\(required\)</span></span> | <span data-ttu-id="698a1-204">O padrão de URL correspondente antes de carregar o script de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="698a1-204">The URL pattern to match prior to loading the content script.</span></span> |  
| `js` | <span data-ttu-id="698a1-205">O script que deve ser carregado em URLs correspondentes.</span><span class="sxs-lookup"><span data-stu-id="698a1-205">The script that should be loaded on matching URLs.</span></span> |  
| `run_at` | <span data-ttu-id="698a1-206">Especifica onde os arquivos JavaScript da `js` chave são injetados.</span><span class="sxs-lookup"><span data-stu-id="698a1-206">Specifies where the JavaScript files from the `js` key are injected.</span></span> |  

<span data-ttu-id="698a1-207">Em seguida, você deve criar um [script de tela de fundo][MDNAnatomyExtensionBackgroundScripts].</span><span class="sxs-lookup"><span data-stu-id="698a1-207">Next, you must create a [background script][MDNAnatomyExtensionBackgroundScripts].</span></span>  <span data-ttu-id="698a1-208">Os scripts em segundo plano são executados em segundo plano do navegador, executados independentemente do tempo de vida de uma página da Web ou janela do navegador e podem se comunicar com scripts de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="698a1-208">Background scripts run in the background of the browser, run independently of the lifetime of a web page or browser window, and are able to communicate with content scripts.</span></span>  

<span data-ttu-id="698a1-209">Na sua `js` pasta, crie um arquivo denominado `background.js` e adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="698a1-209">Inside of your `js` folder, create a file named `background.js` and add the following code.</span></span>  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

<span data-ttu-id="698a1-210">O método [Runtime. onMessage][MDNApiRuntimeOnmessage] escuta o [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] do script de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="698a1-210">The [runtime.onMessage][MDNApiRuntimeOnmessage] method listens for [runtime.sendMessage()][MDNApiRuntimeSendmessage] from the content script.</span></span>  <span data-ttu-id="698a1-211">Se o domínio da página não for [docs.Microsoft.com][MicrosoftDocs], o método [BrowserAction. SetIcon ()][MDNApiBrowseractionSeticon] define os caminhos dos ícones para as imagens inativas.</span><span class="sxs-lookup"><span data-stu-id="698a1-211">If the domain of the page is not [docs.microsoft.com][MicrosoftDocs], then [browserAction.setIcon()][MDNApiBrowseractionSeticon] method sets the icon paths to the inactive images.</span></span>  

<span data-ttu-id="698a1-212">O script também desabilita a ação do navegador \ ([BrowserAction. Disable][MDApiBrowseractionDisable]\), para que os usuários não sejam capazes de clicar na ação do navegador fora de uma página do [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="698a1-212">The script also disables the browser action \([browserAction.disable][MDApiBrowseractionDisable]\), so that users are not able to click on the browser action outside of a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  

<span data-ttu-id="698a1-213">Você deve adicionar o script de tela de fundo ao arquivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .</span><span class="sxs-lookup"><span data-stu-id="698a1-213">You must add the background script to the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file.</span></span>  <span data-ttu-id="698a1-214">Adicione a chave a seguir `background` ao seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="698a1-214">Add the following `background` key to your manifest.</span></span>  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### <span data-ttu-id="698a1-215">Definições da chave do manifesto</span><span class="sxs-lookup"><span data-stu-id="698a1-215">Manifest Key definitions</span></span>  

| <span data-ttu-id="698a1-216">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-216">Key</span></span> | <span data-ttu-id="698a1-217">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-217">Details</span></span>|  
|:--- |:--- |  
| [<span data-ttu-id="698a1-218">tela de fundo</span><span class="sxs-lookup"><span data-stu-id="698a1-218">background</span></span>][MDNManifestjsonBackground] | <span data-ttu-id="698a1-219">Contém os scripts em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="698a1-219">Contains the background scripts.</span></span> |  

#### <span data-ttu-id="698a1-220">definições da chave em segundo plano</span><span class="sxs-lookup"><span data-stu-id="698a1-220">background Key definitions</span></span>  

| <span data-ttu-id="698a1-221">Chave</span><span class="sxs-lookup"><span data-stu-id="698a1-221">Key</span></span> | <span data-ttu-id="698a1-222">Detalhes</span><span class="sxs-lookup"><span data-stu-id="698a1-222">Details</span></span> |  
|:--- |:--- |  
| `scripts` | <span data-ttu-id="698a1-223">O caminho para um arquivo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="698a1-223">The path to a JavaScript file.</span></span> |  
| `persistent` <span data-ttu-id="698a1-224">(obrigatório)</span><span class="sxs-lookup"><span data-stu-id="698a1-224">(required)</span></span> | <span data-ttu-id="698a1-225">Isso deve ser definido como `true` ou `false` .</span><span class="sxs-lookup"><span data-stu-id="698a1-225">This must be set to `true` or `false`.</span></span>  <span data-ttu-id="698a1-226">Se definido como `true` , o script de plano de fundo é carregado e persiste para toda a seção de navegação.</span><span class="sxs-lookup"><span data-stu-id="698a1-226">If set to `true`, the background script is loaded and persists for the entire browsing section.</span></span>  <span data-ttu-id="698a1-227">Se definido como `false` , o script em segundo plano é carregado com um atraso e persiste para a sessão de navegação.</span><span class="sxs-lookup"><span data-stu-id="698a1-227">If set to `false`, the background script is loaded with a delay and persists for the browsing session.</span></span> |  

<span data-ttu-id="698a1-228">Recarregue a extensão e teste novamente.</span><span class="sxs-lookup"><span data-stu-id="698a1-228">Reload your extension and test again.</span></span>  <span data-ttu-id="698a1-229">Para recarregar a extensão: clique em **...** para obter configurações e mais no Microsoft Edge, clique em **extensões**, clique em sua extensão \ (**alterador de cor**\) e clique em **recarregar extensão**.</span><span class="sxs-lookup"><span data-stu-id="698a1-229">To reload your extension: click the **...** for settings and more in Microsoft Edge, click **Extensions**, click on your extension \(**Color Changer**\), and click **Reload extension**.</span></span>  

<span data-ttu-id="698a1-230">Agora, abra uma nova guia ou atualize uma guia existente que não seja uma página do [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="698a1-230">Now, open a new tab or refresh an existing tab that is not a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="698a1-231">Você deve ver o ícone inativo e não pode clicar na ação do navegador.</span><span class="sxs-lookup"><span data-stu-id="698a1-231">You should see the inactive icon and not be able to click on the browser action.</span></span>  

<span data-ttu-id="698a1-232">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="698a1-232">Congratulations!</span></span>  <span data-ttu-id="698a1-233">Você criou uma extensão para o Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="698a1-233">You created an extension for Microsoft Edge!</span></span>  <span data-ttu-id="698a1-234">Veja a [amostra completa no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="698a1-234">View the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  <span data-ttu-id="698a1-235">Continue lendo para saber mais sobre as extensões.</span><span class="sxs-lookup"><span data-stu-id="698a1-235">Continue reading to learn more about extensions.</span></span>  

## <span data-ttu-id="698a1-236">Gravando uma extensão mais complexa</span><span class="sxs-lookup"><span data-stu-id="698a1-236">Writing a more complex extension</span></span>  

<span data-ttu-id="698a1-237">Deseja escrever uma extensão mais complexa?</span><span class="sxs-lookup"><span data-stu-id="698a1-237">Want to write a more complex extension?</span></span>  <span data-ttu-id="698a1-238">Dê uma olhada na extensão Beastify em MDN no artigo, [sua segunda extensão][MDNYourSecondWebextension].</span><span class="sxs-lookup"><span data-stu-id="698a1-238">Take a look at the Beastify extension on MDN in the article, [Your second extension][MDNYourSecondWebextension].</span></span>  <span data-ttu-id="698a1-239">O modelo de extensão para o Microsoft Edge difere ligeiramente do modelo de extensão do Firefox, a extensão Beastify criada na [sua segunda extensão][MDNYourSecondWebextension] foi adaptada para funcionar no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="698a1-239">The extension model for Microsoft Edge differs slightly from the extension model for Firefox, the Beastify extension created in [Your second extension][MDNYourSecondWebextension] was adapted to function in Microsoft Edge.</span></span>  <span data-ttu-id="698a1-240">Dê uma olhada no [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span><span class="sxs-lookup"><span data-stu-id="698a1-240">Check it out on [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span></span>  

<span data-ttu-id="698a1-241">Ao percorrer o artigo sobre MDN, [sua segunda extensão][MDNYourSecondWebextension], lembre-se das seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="698a1-241">While walking through the article on MDN, [Your second extension][MDNYourSecondWebextension], keep in mind the following sections.</span></span>  

### <span data-ttu-id="698a1-242">APIs</span><span class="sxs-lookup"><span data-stu-id="698a1-242">APIs</span></span>  

<span data-ttu-id="698a1-243">Consulte a página [APIs com suporte][ExtensionsAPIsupportApis] para obter uma lista de APIs de extensões com suporte no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="698a1-243">See the [Supported APIs][ExtensionsAPIsupportApis] page for a list of supported extensions APIs in Microsoft Edge.</span></span>  

### <span data-ttu-id="698a1-244">Tamanhos de ícone</span><span class="sxs-lookup"><span data-stu-id="698a1-244">Icon sizes</span></span>  

<span data-ttu-id="698a1-245">Os tamanhos de ícone de extensão preferencial para o Microsoft Edge são `20px` , `25px` , `30px` , e `40px` .</span><span class="sxs-lookup"><span data-stu-id="698a1-245">Preferred extension icon sizes for Microsoft Edge are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="698a1-246">Outros tamanhos compatíveis são `19px` , `35px` e `38px` .</span><span class="sxs-lookup"><span data-stu-id="698a1-246">Other supported sizes are `19px`, `35px`, and `38px`.</span></span>  <span data-ttu-id="698a1-247">Para obter mais informações sobre tamanhos de ícone e práticas recomendadas, consulte o guia de [design][ExtensionsGuidesDesign] .</span><span class="sxs-lookup"><span data-stu-id="698a1-247">For more info on icon sizes and best practices, see the [Design][ExtensionsGuidesDesign] guide.</span></span>  

### <span data-ttu-id="698a1-248">JavaScript</span><span class="sxs-lookup"><span data-stu-id="698a1-248">JavaScript</span></span>  

<span data-ttu-id="698a1-249">O modelo de extensão do Microsoft Edge não oferece suporte a promessas de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="698a1-249">The extension model for Microsoft Edge does not support JavaScript Promises.</span></span>  <span data-ttu-id="698a1-250">Em vez disso, use retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="698a1-250">Instead, use callbacks.</span></span>  <span data-ttu-id="698a1-251">Para obter mais exemplos de como usar retornos de chamada em uma extensão, dê uma olhada nas demonstrações [rápidas de impressão][GithubMicrosoftEdgeExtensionsDemosQuickPrint] e [troca de texto][GithubMicrosoftEdgeExtensionsDemosTextSwap] .</span><span class="sxs-lookup"><span data-stu-id="698a1-251">For more examples of using callbacks in an extension, take a look at the  [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] and [Text Swap][GithubMicrosoftEdgeExtensionsDemosTextSwap] demos.</span></span>  

<span data-ttu-id="698a1-252">Percorra o exemplo de [impressão rápida][GithubMicrosoftEdgeExtensionsDemosQuickPrint] no vídeo a seguir.</span><span class="sxs-lookup"><span data-stu-id="698a1-252">Walk through the [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] example in the following video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### <span data-ttu-id="698a1-253">Manifest. JSON</span><span class="sxs-lookup"><span data-stu-id="698a1-253">Manifest.json</span></span>  

*   <span data-ttu-id="698a1-254">A `author` chave é necessária no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="698a1-254">The `author` key is required in Microsoft Edge</span></span>  
*   <span data-ttu-id="698a1-255">`activeTab`Não há suporte para a chave no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="698a1-255">The `activeTab` key is not supported in Microsoft Edge</span></span>  

<span data-ttu-id="698a1-256">Para obter mais informações sobre [extensões do navegador][MDNBrowserExtensions], consulte [MDN Web docs][MDNWebDocs].</span><span class="sxs-lookup"><span data-stu-id="698a1-256">For more information on [Browser Extensions][MDNBrowserExtensions], see [MDN web docs][MDNWebDocs].</span></span>  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Adicionando uma extensão-adicionando, movendo e removendo extensões do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Extensões de depuração | Documentos da Microsoft"  
[ExtensionsGuidesDesign]: ./design.md "Diretrizes de design para extensões do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Ícones – diretrizes de design para extensões do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md "APIs com suporte | Documentos da Microsoft"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Chaves de manifesto com suporte | Documentos da Microsoft"  

[MicrosoftDocs]: https://docs.microsoft.com "Documentos da Microsoft"  

[MDNWebDocs]: https://developer.mozilla.org "Documentos da Web do MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Extensões do navegador | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomia de uma extensão | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Scripts em segundo plano-anatomia de uma extensão | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "BrowserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserAction. SetIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onMessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "guias-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de conteúdo | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "Author-manifest. JSON | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "plano de fundo-manifesto. JSON | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest. JSON | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Descrição-manifest. JSON | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "ícones-manifest. JSON | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest. JSON | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "permissões-manifest. JSON | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "versão-manifest. JSON | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Sua segunda extensão | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Alterador de cor-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Imagens-alterador de cor-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest. JSON-alterador de cor-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Impressão rápida-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Troca de texto-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
