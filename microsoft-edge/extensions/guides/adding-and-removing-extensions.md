---
description: Saiba como adicionar e remover extensões, bem como mover um botão de extensão ao lado da barra de endereços.
title: Adicionando e removendo extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, extensão
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561230"
---
# <span data-ttu-id="916b2-104">Adicionar, mover e remover extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="916b2-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="916b2-105">O suporte do Microsoft Edge para extensões foi apresentado na **atualização de aniversário do Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="916b2-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="916b2-106">Se você estiver desenvolvendo uma extensão do Microsoft Edge e quiser carregá-la, ou se já tiver e agora deseja removê-la, Confira as etapas abaixo.</span><span class="sxs-lookup"><span data-stu-id="916b2-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="916b2-107">Também estão incluídos detalhes sobre como alterar o local do ícone de extensão no navegador.</span><span class="sxs-lookup"><span data-stu-id="916b2-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="916b2-108">Adicionando uma extensão</span><span class="sxs-lookup"><span data-stu-id="916b2-108">Adding an extension</span></span>

1. <span data-ttu-id="916b2-109">Abra o Microsoft Edge e digite ' about: flags ' na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="916b2-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="916b2-110">Marque a caixa de seleção **habilitar recursos de desenvolvedor de extensão** .</span><span class="sxs-lookup"><span data-stu-id="916b2-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![sobre: indicadores ative os recursos de desenvolvedor](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="916b2-112">Se você não tiver a atualização de aniversário do Windows 10 ou posterior, essa opção não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="916b2-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="916b2-113">Selecione **mais (...)** para abrir o menu.</span><span class="sxs-lookup"><span data-stu-id="916b2-113">Select **More (...)** to open the menu.</span></span>

   ![botão mais](./../media/morebutton.png)  

4. <span data-ttu-id="916b2-115">Selecione **extensões** no menu.</span><span class="sxs-lookup"><span data-stu-id="916b2-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="916b2-116">Selecione o botão **carregar extensão** .</span><span class="sxs-lookup"><span data-stu-id="916b2-116">Select the **Load extension** button.</span></span>

   ![selecionando a extensão de carga](./../media/sideload-load-extension.png)

6. <span data-ttu-id="916b2-118">Navegue até a pasta da extensão e selecione o botão **Selecionar pasta** .</span><span class="sxs-lookup"><span data-stu-id="916b2-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![selecionando a pasta de extensão para carregar](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="916b2-120">Se você encontrar uma mensagem de erro ao carregar a extensão, consulte a página de [solução de problemas](./../troubleshooting.md) para obter orientação.</span><span class="sxs-lookup"><span data-stu-id="916b2-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="916b2-121">Tudo pronto!</span><span class="sxs-lookup"><span data-stu-id="916b2-121">You're all set!</span></span> <span data-ttu-id="916b2-122">Agora você deve ver a extensão listada no painel extensão da Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="916b2-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![extensão no painel de extensão](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="916b2-124">As extensões não assinadas são desativadas automaticamente em inicializações subsequentes do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="916b2-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="916b2-125">Quando o navegador entra em um estado ocioso (após cerca de 10 segundos de inatividade), você verá a seguinte notificação na parte inferior da janela.</span><span class="sxs-lookup"><span data-stu-id="916b2-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="916b2-126">notificação arriscada ](./../media/riskynotification.png) para ativar as extensões não assinadas, clique em "ativar de qualquer maneira".</span><span class="sxs-lookup"><span data-stu-id="916b2-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="916b2-127">Movendo o botão extensão</span><span class="sxs-lookup"><span data-stu-id="916b2-127">Moving the extension button</span></span>
<span data-ttu-id="916b2-128">Dependendo das configurações da extensão, ela pode aparecer no menu **mais (...)** .</span><span class="sxs-lookup"><span data-stu-id="916b2-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![menu ações](./../media/browseraction.png)  


<span data-ttu-id="916b2-130">Se você quiser mover o botão para o menu para facilitar o acesso:</span><span class="sxs-lookup"><span data-stu-id="916b2-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="916b2-131">Clique com o botão direito do mouse no botão extensão.</span><span class="sxs-lookup"><span data-stu-id="916b2-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="916b2-132">Selecione o **botão Mostrar ao lado da barra de endereços**.</span><span class="sxs-lookup"><span data-stu-id="916b2-132">Select **Show button next to address bar**.</span></span>

   ![menu ações](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="916b2-134">Você também pode fazer isso na página de detalhes de extensões:</span><span class="sxs-lookup"><span data-stu-id="916b2-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="916b2-135">Clique no botão extensão.</span><span class="sxs-lookup"><span data-stu-id="916b2-135">Click on the extension button.</span></span>
2. <span data-ttu-id="916b2-136">Botão de alternância de **mostrar ao lado da barra de endereços** para ativado.</span><span class="sxs-lookup"><span data-stu-id="916b2-136">Toggle **Show button next to address bar** to on.</span></span>

   ![botão de alternância Mostrar ativado](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="916b2-138">Você sempre pode mover o botão de volta para o menu **mais (...)** clicando com o botão direito do mouse nele e desmarcando **mostrar ao lado da barra de endereços** ou acessando a página detalhes da extensão e alternando **Mostrar botão ao lado de barra de endereços** para desativar.</span><span class="sxs-lookup"><span data-stu-id="916b2-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="916b2-139">Removendo uma extensão</span><span class="sxs-lookup"><span data-stu-id="916b2-139">Removing an extension</span></span>

1. <span data-ttu-id="916b2-140">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="916b2-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="916b2-141">Selecione **mais (...)** para abrir o menu.</span><span class="sxs-lookup"><span data-stu-id="916b2-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="916b2-142">Selecione **extensões** no menu.</span><span class="sxs-lookup"><span data-stu-id="916b2-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="916b2-143">Clique com o botão direito do mouse na extensão que você deseja remover e selecione **remover**ou selecione a extensão e clique no botão **remover** .</span><span class="sxs-lookup"><span data-stu-id="916b2-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![menu ações](./../media/remove.png)  

**<span data-ttu-id="916b2-145">A extensão deve desaparecer da lista no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="916b2-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
