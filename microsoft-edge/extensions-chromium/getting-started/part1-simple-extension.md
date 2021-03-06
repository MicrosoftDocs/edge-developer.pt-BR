---
description: Criar uma extensão que aparece na imagem do dia da NASA
title: Criar um tutorial de extensão - Parte 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: dfbe7893ce576c223d2b1d39ec21b6c5f46d8356
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397507"
---
# <a name="create-an-extension-tutorial---part-1"></a><span data-ttu-id="94474-104">Criar um tutorial de extensão - Parte 1</span><span class="sxs-lookup"><span data-stu-id="94474-104">Create an extension tutorial - Part 1</span></span>  

## <a name="overview"></a><span data-ttu-id="94474-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="94474-105">Overview</span></span>  

<span data-ttu-id="94474-106">O objetivo deste tutorial é criar uma extensão do Microsoft Edge (Chromium) começando com um diretório vazio.</span><span class="sxs-lookup"><span data-stu-id="94474-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span>  <span data-ttu-id="94474-107">Você está criando uma extensão que aparece na imagem da NASA do dia.</span><span class="sxs-lookup"><span data-stu-id="94474-107">You are building an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="94474-108">Neste tutorial, saiba como criar uma extensão concluindo as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="94474-108">In this tutorial, learn how to create an extension by completing the following actions.</span></span>  

*   <span data-ttu-id="94474-109">Criando um `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="94474-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="94474-110">Adicionando ícones.</span><span class="sxs-lookup"><span data-stu-id="94474-110">Adding icons.</span></span>  
*   <span data-ttu-id="94474-111">Abrindo uma caixa de diálogo pop-up padrão.</span><span class="sxs-lookup"><span data-stu-id="94474-111">Opening a default pop-up dialog.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="94474-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="94474-112">Before you Begin</span></span>

<span data-ttu-id="94474-113">Para testar a extensão concluída que você está criando neste tutorial, baixe o [código-fonte][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="94474-113">To test out the completed extension that you are building in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <a name="step-1-create-a-manifestjson-file"></a><span data-ttu-id="94474-114">Etapa 1: Criar um manifest.jsno arquivo</span><span class="sxs-lookup"><span data-stu-id="94474-114">Step 1: Create a manifest.json file</span></span>

<span data-ttu-id="94474-115">Cada pacote de extensão deve ter `manifest.json` um arquivo na raiz.</span><span class="sxs-lookup"><span data-stu-id="94474-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="94474-116">O manifesto fornece detalhes sobre sua extensão, a versão do pacote de extensão, o nome e a descrição da extensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="94474-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="94474-117">O trecho de código a seguir descreve as informações básicas necessárias em seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="94474-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a><span data-ttu-id="94474-118">Etapa 2: Adicionar ícones</span><span class="sxs-lookup"><span data-stu-id="94474-118">Step 2: Add icons</span></span>  

<span data-ttu-id="94474-119">Comece criando o `icons` diretório em seu projeto para armazenar os arquivos de imagem do ícone.</span><span class="sxs-lookup"><span data-stu-id="94474-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="94474-120">Os ícones são usados para a imagem de plano de fundo do botão que os usuários selecionam para iniciar a extensão.</span><span class="sxs-lookup"><span data-stu-id="94474-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Ícone na barra de ferramentas para abrir sua extensão":::
   <span data-ttu-id="94474-122">Ícone na barra de ferramentas para abrir sua extensão</span><span class="sxs-lookup"><span data-stu-id="94474-122">Icon on the toolbar to open your extension</span></span>  
:::image-end:::  

<span data-ttu-id="94474-123">Para ícones, recomendamos usar:</span><span class="sxs-lookup"><span data-stu-id="94474-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="94474-124">para ícones, mas você também pode usar `BMP` `GIF` , ou `ICO` `JPEG` formatos.</span><span class="sxs-lookup"><span data-stu-id="94474-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="94474-125">Imagens de 128 x 128 px, que são resized pelo navegador, se necessário.</span><span class="sxs-lookup"><span data-stu-id="94474-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="94474-126">Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="94474-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="94474-127">Em seguida, adicione os ícones ao `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="94474-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="94474-128">Atualize seu arquivo com as informações de ícones para `manifest.json` que ele corresponde ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="94474-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="94474-129">Os arquivos listados no código a seguir `png` estão disponíveis no arquivo de download mencionado anteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="94474-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <a name="step-3-open-a-default-pop-up-dialog"></a><span data-ttu-id="94474-130">Etapa 3: Abrir uma caixa de diálogo pop-up padrão</span><span class="sxs-lookup"><span data-stu-id="94474-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="94474-131">Agora, crie um `HTML` arquivo para ser executado quando o usuário iniciar sua extensão.</span><span class="sxs-lookup"><span data-stu-id="94474-131">Now, create a `HTML` file to run when the user launches your extension.</span></span>  <span data-ttu-id="94474-132">Crie o arquivo HTML nomeado `popup.html` em um diretório chamado `popup` .</span><span class="sxs-lookup"><span data-stu-id="94474-132">Create the HTML file named `popup.html` in a directory named `popup`.</span></span>  <span data-ttu-id="94474-133">Quando os usuários selecionam o ícone para iniciar a extensão, `popup/popup.html` é exibido como uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="94474-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="94474-134">Adicione o código do trecho de código a seguir para `popup.html` exibir a imagem de estrelas.</span><span class="sxs-lookup"><span data-stu-id="94474-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

<span data-ttu-id="94474-135">Certifique-se de adicionar o arquivo de `images/stars.jpeg` imagem à pasta de imagens.</span><span class="sxs-lookup"><span data-stu-id="94474-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="94474-136">Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="94474-136">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

<span data-ttu-id="94474-137">Por fim, certifique-se de registrar o pop-up `manifest.json` em , conforme mostrado no trecho de código a `browser_action` seguir.</span><span class="sxs-lookup"><span data-stu-id="94474-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## <a name="next-steps"></a><span data-ttu-id="94474-138">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="94474-138">Next steps</span></span>
<span data-ttu-id="94474-139">Isso é tudo o que você precisa para desenvolver uma extensão de trabalho.</span><span class="sxs-lookup"><span data-stu-id="94474-139">That is everything you need to develop a working extension.</span></span>  <span data-ttu-id="94474-140">Agora, continue fazendo sideload e teste sua extensão.</span><span class="sxs-lookup"><span data-stu-id="94474-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="94474-141">Para obter mais informações, navegue até [Sideload de uma extensão][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="94474-141">For more information, navigate to [Sideload an extension][TestExtensionSideload].</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Fonte de pacote de extensão concluída | Microsoft Docs"

[TestExtensionSideload]: ./extension-sideloading.md "Teste sua extensão (Sideloading) | Microsoft Docs"
