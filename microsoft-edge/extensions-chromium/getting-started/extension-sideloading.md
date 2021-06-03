---
description: Teste sua extensão sideloading-lo no navegador
title: Fazer sideload da extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104767"
---
# <span data-ttu-id="ce1d9-104">Fazer sideload para uma extensão</span><span class="sxs-lookup"><span data-stu-id="ce1d9-104">Sideload an extension</span></span>

<span data-ttu-id="ce1d9-105">Durante o desenvolvimento, você pode usar o navegador Microsoft Edge \(Chromium\) para executar e depurar sua extensão com segurança.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="ce1d9-106">Ao fazer sideload da extensão localmente no navegador, você pode executar e testar sua extensão.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="ce1d9-107">Este artigo explica como fazer sideload de extensões em Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="ce1d9-108">Para fazer sideload da extensão, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="ce1d9-109">Abra a página escolhendo os três pontos na parte superior do navegador e `edge://extensions` selecionando **Extensões**.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abra a página edge://extensions página":::
          <span data-ttu-id="ce1d9-111">Abra a página edge://extensions página</span><span class="sxs-lookup"><span data-stu-id="ce1d9-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="ce1d9-112">Na página gerenciamento de extensão em , a opção Modo desenvolvedor `edge://extensions` usando a alternância na parte inferior esquerda da página. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ce1d9-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Ativar o modo de desenvolvedor":::
          <span data-ttu-id="ce1d9-114">Ativar o modo de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="ce1d9-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="ce1d9-115">Ao instalar sua extensão pela primeira vez, escolha **Carregar Desempacotar**.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="ce1d9-116">Você será solicitado a solicitar o diretório com seus arquivos de origem de extensão.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="ce1d9-117">Sua extensão é instalada no navegador, semelhante às extensões instaladas na loja.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Página extensões instaladas mostrando uma extensão com sideload":::
          <span data-ttu-id="ce1d9-119">Página extensões instaladas mostrando uma extensão com sideload</span><span class="sxs-lookup"><span data-stu-id="ce1d9-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="ce1d9-120">Durante o desenvolvimento, talvez você também precise executar as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="ce1d9-121">Atualize a extensão.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-121">Update the extension.</span></span> <span data-ttu-id="ce1d9-122">Navegue `edge://extensions` até e selecione Recarregar **para** atualizar sua extensão.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="ce1d9-123">Remova a extensão do navegador.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-123">Remove the extension from your browser.</span></span> <span data-ttu-id="ce1d9-124">Navegue `edge://extensions` até e selecione em sua `Remove` extensão.</span><span class="sxs-lookup"><span data-stu-id="ce1d9-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>