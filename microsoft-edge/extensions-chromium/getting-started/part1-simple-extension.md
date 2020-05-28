---
description: Extensões sendo iniciadas parte 1
title: Criar uma extensão simples que é exibida na imagem de NASA do dia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: dd5c1dab0cb9b54b79be7d2728cb9bfde0945185
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683620"
---
# <span data-ttu-id="0776a-104">Criar uma extensão simples que é exibida na imagem de NASA do dia</span><span class="sxs-lookup"><span data-stu-id="0776a-104">Build A Simple Extension That Pops Up NASA Picture Of The Day</span></span>  

[<span data-ttu-id="0776a-105">Origem do pacote de extensão concluída para esta parte</span><span class="sxs-lookup"><span data-stu-id="0776a-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart1]  

## <span data-ttu-id="0776a-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0776a-106">Overview</span></span>  

<span data-ttu-id="0776a-107">Na parte 1, o objetivo é criar uma extensão Chromium de borda muito simples, começando com um diretório vazio.</span><span class="sxs-lookup"><span data-stu-id="0776a-107">In part 1, the goal is to build a very simple Edge Chromium Extension starting with an empty directory.</span></span>  <span data-ttu-id="0776a-108">A meta para esta extensão é concluir as tarefas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-108">The goal for this Extension is to complete the following tasks.</span></span>  

*   <span data-ttu-id="0776a-109">Criar ícones para a extensão que podem ser usadas em vários locais e em diferentes tamanhos</span><span class="sxs-lookup"><span data-stu-id="0776a-109">Create icons for the Extension that may be used in multiple places and in different sizes</span></span>  
*   <span data-ttu-id="0776a-110">Criar um `manifest.json` arquivo simples</span><span class="sxs-lookup"><span data-stu-id="0776a-110">Create a simple `manifest.json` file</span></span>  
*   <span data-ttu-id="0776a-111">Exibir um ícone de inicialização quando selecionado exibe uma janela pop-up contendo a imagem da NASA do dia</span><span class="sxs-lookup"><span data-stu-id="0776a-111">Display a launch icon that when selected displays a pop-up window containing the NASA picture of the day</span></span>  

## <span data-ttu-id="0776a-112">Noções básicas sobre o arquivo de manifesto</span><span class="sxs-lookup"><span data-stu-id="0776a-112">The manifest file basics</span></span>  

<span data-ttu-id="0776a-113">Cada pacote de extensão deve ter um `manifest.json` arquivo na raiz.</span><span class="sxs-lookup"><span data-stu-id="0776a-113">Every Extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="0776a-114">Você deve pensar nisso como o plano gráfico da extensão.</span><span class="sxs-lookup"><span data-stu-id="0776a-114">You should think of this as the blueprint for the Extension.</span></span>  <span data-ttu-id="0776a-115">Ele informa ao mecanismo de navegador qual versão da API de extensão a extensão espera, o nome e a descrição da extensão e muitos outros detalhes, muitos dos quais são abordados neste guia de introdução à extensão de várias partes.</span><span class="sxs-lookup"><span data-stu-id="0776a-115">It tells the browser engine what version of the Extension API the Extension expects, the name and description of the Extension, and lots of other details, many of which are discussed in this multi-part Extension Getting Started guide.</span></span>  

<span data-ttu-id="0776a-116">Veja a seguir uma simples</span><span class="sxs-lookup"><span data-stu-id="0776a-116">Below is the simple</span></span>  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## <span data-ttu-id="0776a-117">Configuração de ícones de extensão</span><span class="sxs-lookup"><span data-stu-id="0776a-117">Extension icons setup</span></span>  

<span data-ttu-id="0776a-118">Em seguida, adicione alguns ícones ao `manifest.json` arquivo \ (e crie um novo `/icons` diretório com os arquivos de ícones \).</span><span class="sxs-lookup"><span data-stu-id="0776a-118">Next add some icons to `manifest.json` file \(and create a new `/icons` directory with the icons files\).</span></span>  <span data-ttu-id="0776a-119">Os ícones são usados para a imagem de plano de fundo do botão que o usuário seleciona para iniciar a extensão \ (se houver um \) e outros locais apropriados.</span><span class="sxs-lookup"><span data-stu-id="0776a-119">The icons are used for the background image of the button the user selects to launch the extension \(if there is one\), and other places that are appropriate.</span></span>  

`PNG` <span data-ttu-id="0776a-120">é o formato recomendado, mas você também pode usar `BMP` , `GIF` `ICO` e `JPEG` .</span><span class="sxs-lookup"><span data-stu-id="0776a-120">is the recommended format, but you may also use `BMP`, `GIF`, `ICO` and `JPEG`.</span></span>  <span data-ttu-id="0776a-121">Recomenda-se sempre ter pelo menos um ícone de tamanho de pixels de 128 x 128 e o navegador o redimensiona automaticamente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="0776a-121">It is recommended to always have at least a 128x128 pixels size icon and the browser automatically resizes it as necessary.</span></span>  

<span data-ttu-id="0776a-122">A estrutura do diretório deve ter a aparência do diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-122">Your directory structure should look like the following diagram.</span></span>  

<!--  
:::image type="complex" source="./media/part1-heirarchy.png" alt-text="Directory Structure":::
   Directory Structure
:::image-end:::
-->  

<!--![Directory Structure][ImagePart1Heirarchy]  -->  

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="0776a-123">O `manifest.json` arquivo atualizado deve aparecer da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="0776a-123">Your updated `manifest.json` file should appear as follows.</span></span>  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

> [!NOTE]
> <span data-ttu-id="0776a-124">Os arquivos de ícone `png` listados no código anterior estão disponíveis no download do zip, mencionado na parte superior desta página.</span><span class="sxs-lookup"><span data-stu-id="0776a-124">The icon `png` files listed previous code are available in the zip download mentioned at the top of this page.</span></span>  

## <span data-ttu-id="0776a-125">Adicionar uma caixa de diálogo pop-up padrão</span><span class="sxs-lookup"><span data-stu-id="0776a-125">Adding a default pop-up dialog</span></span>  

<span data-ttu-id="0776a-126">Agora, crie um `HTML` arquivo que seja executado automaticamente quando o usuário selecionar o ícone de extensão.</span><span class="sxs-lookup"><span data-stu-id="0776a-126">Now, create an `HTML` file that is automatically run when the user selects on the extension icon.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Ícone de selo da barra de ferramentas":::
   <span data-ttu-id="0776a-128">Ícone de selo da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="0776a-128">Toolbar Badge Icon</span></span>
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

<span data-ttu-id="0776a-129">O arquivo HTML é chamado `popup/popup.html` .</span><span class="sxs-lookup"><span data-stu-id="0776a-129">The HTML file is named `popup/popup.html`.</span></span>  <span data-ttu-id="0776a-130">Selecionar o ícone de extensão é iniciado `popup/popup.html` como uma caixa de diálogo modal que fica ativa até você selecionar fora da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0776a-130">Selecting the Extension icon launches `popup/popup.html` as modal dialog that stays up until you select outside the dialog.</span></span>  

<span data-ttu-id="0776a-131">Para isso, registre o arquivo como um pop-up padrão no `manifest.json` `browser_action` no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-131">For this, register the file as a default pop-up in the `manifest.json` under `browser_action` in the following code.</span></span>  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium Extension to show the NASA Picture of the Day.",
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

<span data-ttu-id="0776a-132">No `popup` diretório, adicione o arquivo `popup.html` e faça com que ele renderize a imagem de estrelas.</span><span class="sxs-lookup"><span data-stu-id="0776a-132">In the `popup` directory , add the file `popup.html` and have it render the stars image.</span></span>  <span data-ttu-id="0776a-133">Aqui está o `popup.html` arquivo.</span><span class="sxs-lookup"><span data-stu-id="0776a-133">Here is the `popup.html` file.</span></span>  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA Picture of the Day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="stars" />
        </div>
    </body>
</html>
```  

 <span data-ttu-id="0776a-134">Além disso, adicione um arquivo de imagem `images/stars.jpeg` referenciado no `popup.html` arquivo.</span><span class="sxs-lookup"><span data-stu-id="0776a-134">Also, add an image file `images/stars.jpeg` that is referenced in the `popup.html` file.</span></span>  

<span data-ttu-id="0776a-135">A estrutura de diretório para o exemplo de extensão é exibida no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-135">The directory structure for the example Extension is displayed in the following diagram.</span></span>  

<!--  
:::image type="complex" source="./media/part1-heirarchy1.png" alt-text="Directory Structure for Extension":::
   Directory Structure for Extension
:::image-end:::
-->  

<!--![Directory Structure for Extension][ImagePart1Heirarchy1]  -->  

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

> [!NOTE]
> <span data-ttu-id="0776a-136">O `images/stars.jpeg` arquivo listado na imagem anterior está disponível no [zip download][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="0776a-136">The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].</span></span>  

<span data-ttu-id="0776a-137">Isso é tudo o que você precisa para criar uma extensão em funcionamento.</span><span class="sxs-lookup"><span data-stu-id="0776a-137">That is everything you need to build a working Extension.</span></span>  <span data-ttu-id="0776a-138">Tudo o que resta para é testá-lo.</span><span class="sxs-lookup"><span data-stu-id="0776a-138">All that is left to is test it.</span></span>  

<span data-ttu-id="0776a-139">A seção a seguir explica como carregar a extensão \ (às vezes chamado de carregamento lateral \) no navegador Microsoft Edge \ (Chromium \) para testá-la.</span><span class="sxs-lookup"><span data-stu-id="0776a-139">The next section explains how to load the Extension \(sometimes called side loading\) into the Microsoft Edge \(Chromium\) browser to test it.</span></span>  

## <span data-ttu-id="0776a-140">Executar a extensão localmente no navegador ao desenvolver \ (carregando \)</span><span class="sxs-lookup"><span data-stu-id="0776a-140">Run your Extension locally in your browser while developing it \(side-loading\)</span></span>  

<span data-ttu-id="0776a-141">O navegador Microsoft Edge \ (Chromium \) fornece uma maneira segura e simples para você executar e depurar as extensões durante o desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="0776a-141">The Microsoft Edge \(Chromium\) browser provides a safe and simple way for you to run as well as debug your Extensions while you are developing.</span></span>  

<span data-ttu-id="0776a-142">O processo é muito simples.</span><span class="sxs-lookup"><span data-stu-id="0776a-142">The process is quite simple.</span></span>  <span data-ttu-id="0776a-143">Primeiro você deve selecionar os três pontos na parte superior do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="0776a-143">You must first select the three dots at the top of your browser.</span></span>  <span data-ttu-id="0776a-144">Em seguida, escolha no `Extensions` menu de contexto, como mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-144">Next, choose `Extensions` from the context menu as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Escolher extensões":::
   <span data-ttu-id="0776a-146">Escolher extensões</span><span class="sxs-lookup"><span data-stu-id="0776a-146">Choose Extensions</span></span>
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

<span data-ttu-id="0776a-147">Quando estiver na página **extensões** , conforme mostrado na imagem a seguir, habilite o **modo de desenvolvedor** habilitando a alternância na parte inferior esquerda da página, como mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-147">When you are on the **Extensions** page as shown in the following image, enable the **Developer mode** by enabling the toggle at the bottom left of the page as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Habilitar o modo de desenvolvedor":::
   <span data-ttu-id="0776a-149">Habilitar o modo de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="0776a-149">Enable Developer Mode</span></span>
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## <span data-ttu-id="0776a-150">Instalando e atualizando extensões de carregamento lado a lado</span><span class="sxs-lookup"><span data-stu-id="0776a-150">Installing and updating side-loaded Extensions</span></span>  

<span data-ttu-id="0776a-151">Na primeira vez que você quiser instalar a extensão, escolha a `Load Unpacked` opção conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="0776a-151">The first time you want to install your Extension, you choose the `Load Unpacked` option as shown in the following image.</span></span>  <span data-ttu-id="0776a-152">Isso solicitará a você um diretório em que você tem o arquivo de ativos de extensão por meio do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0776a-152">This prompts you for a directory where you have your Extension assets file by file.</span></span>  <span data-ttu-id="0776a-153">Isso instalará a extensão como se você a tivesse baixado de uma loja.</span><span class="sxs-lookup"><span data-stu-id="0776a-153">This installs the Extension as if you had downloaded it from a store.</span></span>  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Extensões instaladas":::
   <span data-ttu-id="0776a-155">Extensões instaladas</span><span class="sxs-lookup"><span data-stu-id="0776a-155">Installed Extensions</span></span>
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

<span data-ttu-id="0776a-156">Depois de instalar a extensão, você pode atualizá-la selecionando o `Reload` botão abaixo de sua lista de extensão.</span><span class="sxs-lookup"><span data-stu-id="0776a-156">After you install your Extension, you may update it by selecting the `Reload` button under your Extension listing.</span></span>  

<span data-ttu-id="0776a-157">Para remover a extensão do seu navegador, clique no `Remove` botão na parte inferior da listagem de extensão.</span><span class="sxs-lookup"><span data-stu-id="0776a-157">To remove the Extension from your browser, click the `Remove` button on the bottom of the Extension listing.</span></span>  

## <span data-ttu-id="0776a-158">Extensões de depuração</span><span class="sxs-lookup"><span data-stu-id="0776a-158">Debugging Extensions</span></span>  

<span data-ttu-id="0776a-159">Extensões de depuração é muito fácil e dão suporte a todos os recursos no Edge Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="0776a-159">Debugging Extensions is quite easy and supports all of the features in Edge Chromium DevTools.</span></span>  <span data-ttu-id="0776a-160">Esses detalhes no entanto não são abordados neste guia de introdução, mas são muito importantes para criar extensões com êxito.</span><span class="sxs-lookup"><span data-stu-id="0776a-160">Those details however are not covered in this getting started guide but are very important to successfully build Extensions.</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Fonte do pacote de extensão concluída para esta parte | Documentos da Microsoft"  
