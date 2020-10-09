---
description: Criar uma extensão que exibe a imagem da NASA do dia
title: Criar um tutorial de extensão-parte 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 3809bfac714621cf97184127132487ed93958a2f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104704"
---
# <span data-ttu-id="a5542-104">Criar um tutorial de extensão-parte 1</span><span class="sxs-lookup"><span data-stu-id="a5542-104">Create an extension tutorial - Part 1</span></span>  

## <span data-ttu-id="a5542-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a5542-105">Overview</span></span>  

<span data-ttu-id="a5542-106">A meta deste tutorial é criar uma extensão do Microsoft Edge (Chromium) a partir de um diretório vazio.</span><span class="sxs-lookup"><span data-stu-id="a5542-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span> <span data-ttu-id="a5542-107">Criaremos uma extensão que exibe a imagem da NASA do dia.</span><span class="sxs-lookup"><span data-stu-id="a5542-107">We'll build an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="a5542-108">Neste tutorial, você aprenderá a criar uma extensão por:</span><span class="sxs-lookup"><span data-stu-id="a5542-108">In this tutorial, you'll learn how to create an extension by:</span></span>

*   <span data-ttu-id="a5542-109">Criando um `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5542-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="a5542-110">Adicionando ícones.</span><span class="sxs-lookup"><span data-stu-id="a5542-110">Adding icons.</span></span>  
*   <span data-ttu-id="a5542-111">Abrir uma caixa de diálogo pop-up padrão.</span><span class="sxs-lookup"><span data-stu-id="a5542-111">Opening a default pop-up dialog.</span></span>  

## <span data-ttu-id="a5542-112">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="a5542-112">Before you Begin</span></span>

<span data-ttu-id="a5542-113">Se quiser testar a extensão concluída que você criará neste tutorial, baixe o [código-fonte][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="a5542-113">If you'd like to test out the completed extension that you'll build in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <span data-ttu-id="a5542-114">Etapa 1: criar um `manifest.json` arquivo</span><span class="sxs-lookup"><span data-stu-id="a5542-114">Step 1: Create a `manifest.json` file</span></span>

<span data-ttu-id="a5542-115">Cada pacote de extensão deve ter um `manifest.json` arquivo na raiz.</span><span class="sxs-lookup"><span data-stu-id="a5542-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="a5542-116">O manifesto fornece detalhes da extensão, a versão do pacote de extensão, o nome e a descrição da extensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a5542-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="a5542-117">O trecho de código a seguir destaca as informações básicas necessárias no seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5542-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <span data-ttu-id="a5542-118">Etapa 2: Adicionar ícones</span><span class="sxs-lookup"><span data-stu-id="a5542-118">Step 2: Add icons</span></span>  

<span data-ttu-id="a5542-119">Comece criando o `icons` diretório em seu projeto para armazenar os arquivos de imagem do ícone.</span><span class="sxs-lookup"><span data-stu-id="a5542-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="a5542-120">Os ícones são usados para a imagem de plano de fundo do botão que os usuários selecionam para iniciar a extensão.</span><span class="sxs-lookup"><span data-stu-id="a5542-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Ícone na barra de ferramentas para abrir a extensão":::
   <span data-ttu-id="a5542-122">Ícone na barra de ferramentas para abrir a extensão</span><span class="sxs-lookup"><span data-stu-id="a5542-122">Icon on the toolbar to open your extension</span></span>
:::image-end:::

<span data-ttu-id="a5542-123">Para ícones, recomendamos usar:</span><span class="sxs-lookup"><span data-stu-id="a5542-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="a5542-124">Formatar para ícones, mas você também pode usar `BMP` , `GIF` `ICO` ou `JPEG` formatos.</span><span class="sxs-lookup"><span data-stu-id="a5542-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="a5542-125">Imagens que são 128 x 128 px, que são redimensionadas pelo navegador, se necessário.</span><span class="sxs-lookup"><span data-stu-id="a5542-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="a5542-126">Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5542-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="a5542-127">Em seguida, adicione os ícones ao `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5542-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="a5542-128">Atualize o `manifest.json` arquivo com as informações dos ícones para que ele corresponda ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5542-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="a5542-129">Os `png` arquivos listados no código a seguir estão disponíveis no arquivo de download mencionado anteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="a5542-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

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

## <span data-ttu-id="a5542-130">Etapa 3: abrir uma caixa de diálogo pop-up padrão</span><span class="sxs-lookup"><span data-stu-id="a5542-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="a5542-131">Agora, crie um `HTML` arquivo que seja executado quando o usuário iniciar a extensão.</span><span class="sxs-lookup"><span data-stu-id="a5542-131">Now, create a `HTML` file that's run when the user launches your extension.</span></span>  <span data-ttu-id="a5542-132">Crie o arquivo HTML chamado `popup.html` em um diretório chamado `popup` .</span><span class="sxs-lookup"><span data-stu-id="a5542-132">Create the HTML file called `popup.html` in a directory called `popup`.</span></span>  <span data-ttu-id="a5542-133">Quando os usuários selecionam o ícone para iniciar a extensão, ele `popup/popup.html` é exibido como uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="a5542-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="a5542-134">Adicione o código do trecho de código a seguir para `popup.html` exibir a imagem de estrelas.</span><span class="sxs-lookup"><span data-stu-id="a5542-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="a5542-135">Certifique-se de adicionar o arquivo de imagem `images/stars.jpeg` à pasta images.</span><span class="sxs-lookup"><span data-stu-id="a5542-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="a5542-136">Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5542-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="a5542-137">Por fim, certifique-se de registrar o pop-up em `manifest.json` `browser_action` , conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5542-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <span data-ttu-id="a5542-138">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a5542-138">Next steps</span></span>
<span data-ttu-id="a5542-139">Isso é tudo o que você precisa para desenvolver uma extensão funcional.</span><span class="sxs-lookup"><span data-stu-id="a5542-139">That's everything you need to develop a working extension.</span></span> <span data-ttu-id="a5542-140">Agora, continue em Sideload e teste a extensão.</span><span class="sxs-lookup"><span data-stu-id="a5542-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="a5542-141">Para obter mais informações, consulte [Sideload uma extensão][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="a5542-141">For more information, see [Sideload an extension][TestExtensionSideload].</span></span>  


<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Fonte do pacote de extensão concluída | Documentos da Microsoft"

[TestExtensionSideload]: ./extension-sideloading.md "Testar sua extensão (Sideload) | Documentos da Microsoft"
