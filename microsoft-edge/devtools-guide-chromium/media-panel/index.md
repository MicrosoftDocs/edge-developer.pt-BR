---
description: Use o painel mídia para ver informações e depurar a guia media players por navegador.
title: Exibir e depurar informações do media players
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: dfcf17861c0296e347007bc3a1a02a2b80661e6f
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11105168"
---
# <span data-ttu-id="35ac3-104">Exibir e depurar informações do media players</span><span class="sxs-lookup"><span data-stu-id="35ac3-104">View and debug media players information</span></span>  

<span data-ttu-id="35ac3-105">Use o painel **mídia** no Microsoft Edge devtools para exibir informações e depurar a guia media players por navegador.</span><span class="sxs-lookup"><span data-stu-id="35ac3-105">Use the **Media** panel in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <span data-ttu-id="35ac3-106">Abrir o painel mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-106">Open the Media panel</span></span>  

<span data-ttu-id="35ac3-107">O painel **mídia** é o local principal no devtools para inspecionar o Media Player de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="35ac3-107">The **Media** panel is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="35ac3-108">[Abra o devtools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="35ac3-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="35ac3-109">Para abrir o painel **mídia** , escolha **Personalizar e controle devtools** `...`  >  **mais ferramentas**de  >  **mídia**.</span><span class="sxs-lookup"><span data-stu-id="35ac3-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="35ac3-111">Painel **mídia**</span><span class="sxs-lookup"><span data-stu-id="35ac3-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="35ac3-112">Ver as informações do media players</span><span class="sxs-lookup"><span data-stu-id="35ac3-112">View media players information</span></span>  

1.  <span data-ttu-id="35ac3-113">Navegue até uma página da Web com um Media Player, como a página da Web a seguir.</span><span class="sxs-lookup"><span data-stu-id="35ac3-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="35ac3-114">Maximizar a produtividade com as ferramentas de desenvolvedor Edge</span><span class="sxs-lookup"><span data-stu-id="35ac3-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="35ac3-115">No menu **jogadores** , é exibido um player de mídia.</span><span class="sxs-lookup"><span data-stu-id="35ac3-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="35ac3-116">Selecione o jogador.</span><span class="sxs-lookup"><span data-stu-id="35ac3-116">Select the player.</span></span>  <span data-ttu-id="35ac3-117">A guia **Propriedades** exibe as propriedades do Media Player.</span><span class="sxs-lookup"><span data-stu-id="35ac3-117">The **Properties** tab displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="35ac3-119">Propriedades da mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35ac3-120">Para ver todos os eventos do Media Player, escolha a guia **Events (eventos** ).</span><span class="sxs-lookup"><span data-stu-id="35ac3-120">To view all the media player events, choose the **Events** tab.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="35ac3-122">Eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35ac3-123">Para exibir os logs de mensagens do Media Player, escolha a guia **mensagens** .  Você pode filtrar as mensagens por nível de log ou cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35ac3-123">To view the media player message logs, choose the **Messages** tab.  You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="35ac3-125">Mensagens de mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-125">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35ac3-126">Na guia **linha do tempo** , a reprodução de mídia e o status do buffer são exibidos ao vivo.</span><span class="sxs-lookup"><span data-stu-id="35ac3-126">On the **Timeline** tab, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="35ac3-128">Linha do tempo de mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-128">Media timeline</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="35ac3-129">Depuração remota</span><span class="sxs-lookup"><span data-stu-id="35ac3-129">Remote debugging</span></span>  

<span data-ttu-id="35ac3-130">Exiba as informações do Media Player em um dispositivo Android a partir de seu computador com Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="35ac3-130">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="35ac3-131">Para configurar a depuração remota, navegue até [introdução à depuração remota de dispositivos Android][DevtoolsGuideChromiumRemoteDebuggingIndex].</span><span class="sxs-lookup"><span data-stu-id="35ac3-131">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="35ac3-132">Exiba as informações do Media Player remotamente.</span><span class="sxs-lookup"><span data-stu-id="35ac3-132">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <span data-ttu-id="35ac3-133">Ocultar e mostrar media players</span><span class="sxs-lookup"><span data-stu-id="35ac3-133">Hide and show media players</span></span>  

<span data-ttu-id="35ac3-134">Às vezes, você executa mais de um Media Player em uma página da Web ou usa a mesma guia do navegador para navegar por páginas da Web diferentes, cada uma com media players.</span><span class="sxs-lookup"><span data-stu-id="35ac3-134">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="35ac3-135">Você pode optar por ocultar \ (ou mostrar \) cada Player de mídia para ter uma experiência de depuração mais fácil.</span><span class="sxs-lookup"><span data-stu-id="35ac3-135">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="35ac3-136">Navegue até várias páginas da Web de vídeo diferentes usando a mesma guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="35ac3-136">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="35ac3-137">Para ocultar players de mídia, execute uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="35ac3-137">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="35ac3-138">Para ocultar um Media Player, passe o mouse sobre um Media Player, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **ocultar Player**.</span><span class="sxs-lookup"><span data-stu-id="35ac3-138">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="35ac3-139">Para ocultar todos os outros media players, passe o mouse em um Media Player, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **ocultar todos os outros**.</span><span class="sxs-lookup"><span data-stu-id="35ac3-139">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="35ac3-141">Ocultar players de mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-141">Hide media players</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="35ac3-142">Exportar informações do player de mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-142">Export media player information</span></span>  

1.  <span data-ttu-id="35ac3-143">Para baixar as informações do Media Player como um arquivo JSON, passe o mouse em um player de mídia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **salvar informações do jogador**.</span><span class="sxs-lookup"><span data-stu-id="35ac3-143">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Painel mídia" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="35ac3-145">Exportar informações de mídia</span><span class="sxs-lookup"><span data-stu-id="35ac3-145">Export media information</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="35ac3-146">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="35ac3-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir o Microsoft Edge DevTools"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Introdução à depuração remota de dispositivos Android | Documentos da Microsoft"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximizar a produtividade com as ferramentas de desenvolvedor Edge | Vídeo do Bing"  

> [!NOTE]
> <span data-ttu-id="35ac3-150">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="35ac3-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="35ac3-151">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="35ac3-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="35ac3-153">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="35ac3-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

