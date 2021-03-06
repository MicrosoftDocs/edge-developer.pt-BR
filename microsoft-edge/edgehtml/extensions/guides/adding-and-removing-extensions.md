---
description: Saiba como adicionar e remover extensões, bem como mover o botão da extensão ao lado da barra de endereços.
title: Adicionando e removendo extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento para a web, html, css, javascript, desenvolvedor, extensão
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2ef75e76795d527935a84913528506bfa042e56f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398872"
---
# <a name="adding-moving-and-removing-extensions-for-microsoft-edge"></a><span data-ttu-id="89b3f-104">Adicionar, mover e remover extensões para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="89b3f-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="89b3f-105">O suporte ao Microsoft Edge para extensões foi introduzido na **Atualização de Aniversário do Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span>  <span data-ttu-id="89b3f-106">Se você estiver desenvolvendo uma extensão do Microsoft Edge e deseja carregá-la, ou se você já a tiver e agora quiser removê-la, confira as etapas abaixo.</span><span class="sxs-lookup"><span data-stu-id="89b3f-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>  
<span data-ttu-id="89b3f-107">Também estão incluídos detalhes sobre como alterar o local do ícone de extensão no navegador.</span><span class="sxs-lookup"><span data-stu-id="89b3f-107">Also included are details on how to change your extension icon's location in the browser.</span></span>  

## <a name="adding-an-extension"></a><span data-ttu-id="89b3f-108">Adicionar uma extensão</span><span class="sxs-lookup"><span data-stu-id="89b3f-108">Adding an extension</span></span>  

1.  <span data-ttu-id="89b3f-109">Abra o Microsoft Edge e `about:flags` digite na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="89b3f-109">Open Microsoft Edge and type `about:flags` into the address bar.</span></span>  
1.  <span data-ttu-id="89b3f-110">Marque a caixa de seleção **Habilitar recursos da extensão do desenvolvedor**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-110">Select the **Enable extension developer features** checkbox.</span></span>  
    
    ![about:flags ativa os recursos do desenvolvedor](../media/sideload-aboutflags.png)  
    
    > [!NOTE]
    > <span data-ttu-id="89b3f-112">Se você não tiver a Atualização de Aniversário do Windows 10 ou posterior, essa opção não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="89b3f-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>  
    
1.  <span data-ttu-id="89b3f-113">Selecione **Mais (...)** para abrir o menu.</span><span class="sxs-lookup"><span data-stu-id="89b3f-113">Select **More (...)** to open the menu.</span></span>  
    
    ![botão mais](../media/morebutton.png)  
    
1.  <span data-ttu-id="89b3f-115">Selecione **Extensões** no menu.</span><span class="sxs-lookup"><span data-stu-id="89b3f-115">Select **Extensions** from the menu.</span></span>  
    
1.  <span data-ttu-id="89b3f-116">Selecione o botão **Extensão de carregamento**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-116">Select the **Load extension** button.</span></span>  
    
    ![selecionar a extensão de carregamento](../media/sideload-load-extension.png)  
    
1.  <span data-ttu-id="89b3f-118">Navegue até a pasta da extensão e selecione o botão **Selecionar pasta**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>  
    
    ![selecionar a pasta de extensão a ser carregada](../media/sideload-select-extension.png)  
    
    > [!NOTE]
    > <span data-ttu-id="89b3f-120">Se você encontrar uma mensagem de erro ao carregar a extensão, confira a página [solução de problemas](../troubleshooting.md) para obter ajuda.</span><span class="sxs-lookup"><span data-stu-id="89b3f-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](../troubleshooting.md) page for guidance.</span></span>  
    
**<span data-ttu-id="89b3f-121">Pronto!</span><span class="sxs-lookup"><span data-stu-id="89b3f-121">You're all set!</span></span> <span data-ttu-id="89b3f-122">Agora você deverá ver a extensão listada no painel extensão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="89b3f-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**  

![extensão no painel extensão](../media/sideload-extension-installed.png)  

> [!NOTE]
> <span data-ttu-id="89b3f-124">As extensões não assinadas são desativadas automaticamente nas inicializações subsequentes do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="89b3f-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span>  <span data-ttu-id="89b3f-125">Quando o navegador inserir um estado ocioso \(após aproximadamente 10 segundos de inatividade\) você verá a seguinte notificação na parte inferior da janela.</span><span class="sxs-lookup"><span data-stu-id="89b3f-125">When the browser enters an idle state \(after approximately 10 seconds of inactivity\) you will see the following notification at the bottom of the window.</span></span>  ![<span data-ttu-id="89b3f-126">notificação arriscada ](../media/riskynotification.png) Para ativar as extensões não atribuídas, clique **em Ativar de qualquer maneira**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-126">risky notification](../media/riskynotification.png) To turn on the unsigned extensions, click **Turn on anyway**.</span></span>  

## <a name="moving-the-extension-button"></a><span data-ttu-id="89b3f-127">Mover o botão extensão</span><span class="sxs-lookup"><span data-stu-id="89b3f-127">Moving the extension button</span></span>  

<span data-ttu-id="89b3f-128">Dependendo das configurações da extensão, ela pode aparecer no menu **Mais (...)**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>  

![menu ações](../media/browseraction.png)  

<span data-ttu-id="89b3f-130">Se você quiser mover o botão para fora desse menu para facilitar o acesso:</span><span class="sxs-lookup"><span data-stu-id="89b3f-130">If you want to move the button out of this menu for easier access:</span></span>  

1.  <span data-ttu-id="89b3f-131">Clicar com o botão direito do mouse no botão extensão.</span><span class="sxs-lookup"><span data-stu-id="89b3f-131">Right-click the extension button.</span></span>  
1.  <span data-ttu-id="89b3f-132">Selecione **Mostrar botão ao lado da barra de endereços**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-132">Select **Show button next to address bar**.</span></span>  
    
    ![menu de contexto no menu ações](../media/browseraction_contextmenu.png)  
    
<span data-ttu-id="89b3f-134">Como alternativa, você pode fazer isso na página de detalhes das extensões:</span><span class="sxs-lookup"><span data-stu-id="89b3f-134">Alternatively, you may do this from the extensions details page:</span></span>  

1.  <span data-ttu-id="89b3f-135">Clique no botão extensão.</span><span class="sxs-lookup"><span data-stu-id="89b3f-135">Click on the extension button.</span></span>  
1.  <span data-ttu-id="89b3f-136">Alterne **Mostrar botão ao lado da barra de endereços** para ativado.</span><span class="sxs-lookup"><span data-stu-id="89b3f-136">Toggle **Show button next to address bar** to on.</span></span>  
    
    ![Mostrar botão de alternância ativado](../media/show-button-toggle.png)  
    
> [!NOTE]
> <span data-ttu-id="89b3f-138">Você sempre poderá mover o botão de volta para o menu**Mais (...)** clicando com o botão direito do mouse nele e desmarcando **Mostrar ao lado da barra de endereços** ou acessando a página detalhes da extensão e alternando **Mostrar botão ao lado da barra de endereços** para desativado.</span><span class="sxs-lookup"><span data-stu-id="89b3f-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>  

## <a name="removing-an-extension"></a><span data-ttu-id="89b3f-139">Remover uma extensão</span><span class="sxs-lookup"><span data-stu-id="89b3f-139">Removing an extension</span></span>  

1.  <span data-ttu-id="89b3f-140">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="89b3f-140">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="89b3f-141">Selecione **Mais (...)** para abrir o menu.</span><span class="sxs-lookup"><span data-stu-id="89b3f-141">Select **More (...)** to open the menu.</span></span>  
1.  <span data-ttu-id="89b3f-142">Selecione **Extensões** no menu.</span><span class="sxs-lookup"><span data-stu-id="89b3f-142">Select **Extensions** from the menu.</span></span>  
1.  <span data-ttu-id="89b3f-143">Clique com o botão direito do mouse na extensão que você deseja remover e selecione **Remover**ou selecione a extensão e clique no botão **Remover**.</span><span class="sxs-lookup"><span data-stu-id="89b3f-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>  
    
    ![Remover no menu ações](../media/remove.png)  
    
**<span data-ttu-id="89b3f-145">A extensão deve desaparecer da lista no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="89b3f-145">The extension should disappear from the list in Microsoft Edge.</span></span>**  
