---
description: Testar a extensão por meio de Sideload no navegador
title: Sideload sua extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104767"
---
# <span data-ttu-id="abf97-104">Sideload uma extensão</span><span class="sxs-lookup"><span data-stu-id="abf97-104">Sideload an extension</span></span>

<span data-ttu-id="abf97-105">Durante o desenvolvimento, você pode usar o navegador Microsoft Edge \(Chromium \) para executar e depurar a extensão com segurança.</span><span class="sxs-lookup"><span data-stu-id="abf97-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="abf97-106">Ao fazer o Sideload da sua extensão localmente no seu navegador, você pode executar e testar a extensão.</span><span class="sxs-lookup"><span data-stu-id="abf97-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="abf97-107">Este artigo explica como Sideload extensões para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abf97-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="abf97-108">Para Sideload a extensão, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="abf97-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="abf97-109">Para abrir a `edge://extensions` página, escolha os três pontos na parte superior do seu navegador e, em seguida, selecione **extensões**.</span><span class="sxs-lookup"><span data-stu-id="abf97-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abrir a página edge://extensions":::
          <span data-ttu-id="abf97-111">Abrir a página edge://extensions</span><span class="sxs-lookup"><span data-stu-id="abf97-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="abf97-112">Na página Gerenciamento de extensão `edge://extensions` , ative o **modo de desenvolvedor** usando o botão de alternância na parte inferior esquerda da página.</span><span class="sxs-lookup"><span data-stu-id="abf97-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Abrir a página edge://extensions":::
          <span data-ttu-id="abf97-114">Ativar o modo de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="abf97-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="abf97-115">Ao instalar a extensão pela primeira vez, escolha **carregar desempacotada**.</span><span class="sxs-lookup"><span data-stu-id="abf97-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="abf97-116">Você será solicitado a fornecer o diretório com seus arquivos de origem de extensão.</span><span class="sxs-lookup"><span data-stu-id="abf97-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="abf97-117">Sua extensão é instalada em seu navegador, semelhante às extensões instaladas a partir da loja.</span><span class="sxs-lookup"><span data-stu-id="abf97-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Abrir a página edge://extensions":::
          <span data-ttu-id="abf97-119">Página de extensões instaladas mostrando uma extensão Sideload</span><span class="sxs-lookup"><span data-stu-id="abf97-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="abf97-120">Durante o desenvolvimento, você também pode precisar executar as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="abf97-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="abf97-121">Atualize a extensão.</span><span class="sxs-lookup"><span data-stu-id="abf97-121">Update the extension.</span></span> <span data-ttu-id="abf97-122">Navegue até `edge://extensions` e, em seguida, selecione **recarregar** para atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="abf97-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="abf97-123">Remova a extensão do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="abf97-123">Remove the extension from your browser.</span></span> <span data-ttu-id="abf97-124">Navegue até `edge://extensions` e selecione `Remove` na extensão.</span><span class="sxs-lookup"><span data-stu-id="abf97-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>