---
description: Use a ferramenta Mídia para exibir informações e depurar os media players por guia do navegador.
title: Exibir e depurar informações de players de mídia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7680faa13f65a2ea6f0a8b085316b5ed67bfdaba
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398403"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="view-and-debug-media-players-information"></a><span data-ttu-id="0da6f-104">Exibir e depurar informações de players de mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-104">View and debug media players information</span></span>  

<span data-ttu-id="0da6f-105">Use a **ferramenta Mídia** no Microsoft Edge DevTools para exibir informações e depurar os media players por guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="0da6f-105">Use the **Media** tool in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <a name="open-the-media-tool"></a><span data-ttu-id="0da6f-106">Abra a ferramenta Mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-106">Open the Media tool</span></span>  

<span data-ttu-id="0da6f-107">A **ferramenta Mídia** é o principal local no DevTools para inspecionar o media player de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="0da6f-107">The **Media** tool is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="0da6f-108">[Abra DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="0da6f-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="0da6f-109">Para abrir o **painel Mídia,** escolha **Personalizar e controlar DevTools** `...`  >  **Mais ferramentas**  >  **Mídia**.</span><span class="sxs-lookup"><span data-stu-id="0da6f-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Painel de mídia" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="0da6f-111">**Painel de** mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <a name="view-media-players-information"></a><span data-ttu-id="0da6f-112">Exibir informações de media players</span><span class="sxs-lookup"><span data-stu-id="0da6f-112">View media players information</span></span>  

1.  <span data-ttu-id="0da6f-113">Navegue até uma página da Web com um media player, como a página da Web a seguir.</span><span class="sxs-lookup"><span data-stu-id="0da6f-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="0da6f-114">Maximizando a produtividade com as Ferramentas de Desenvolvedor de Borda</span><span class="sxs-lookup"><span data-stu-id="0da6f-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="0da6f-115">No menu **Jogadores,** um media player é exibido.</span><span class="sxs-lookup"><span data-stu-id="0da6f-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="0da6f-116">Escolha o player.</span><span class="sxs-lookup"><span data-stu-id="0da6f-116">Choose the player.</span></span>  <span data-ttu-id="0da6f-117">O **painel Propriedades** exibe as propriedades do media player.</span><span class="sxs-lookup"><span data-stu-id="0da6f-117">The **Properties** panel displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propriedades de mídia" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="0da6f-119">Propriedades de mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0da6f-120">Para exibir todos os eventos do media player, escolha o **painel Eventos.**</span><span class="sxs-lookup"><span data-stu-id="0da6f-120">To view all the media player events, choose the **Events** panel.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Eventos de mídia" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="0da6f-122">Eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0da6f-123">Para exibir os logs de mensagens do media player, escolha o **painel Mensagens.**</span><span class="sxs-lookup"><span data-stu-id="0da6f-123">To view the media player message logs, choose the **Messages** panel.</span></span>  <span data-ttu-id="0da6f-124">Você pode filtrar as mensagens por nível de log ou cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0da6f-124">You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mensagens de mídia" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="0da6f-126">Mensagens de mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-126">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0da6f-127">No painel **Linha do** Tempo, a reprodução de mídia e o status do buffer são exibidos ao vivo.</span><span class="sxs-lookup"><span data-stu-id="0da6f-127">On the **Timeline** panel, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Linha do tempo da mídia" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="0da6f-129">Linha do tempo da mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-129">Media timeline</span></span>  
    :::image-end:::  
    
### <a name="remote-debugging"></a><span data-ttu-id="0da6f-130">Depuração remota</span><span class="sxs-lookup"><span data-stu-id="0da6f-130">Remote debugging</span></span>  

<span data-ttu-id="0da6f-131">Exibir as informações dos media players em um dispositivo Android do computador Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="0da6f-131">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="0da6f-132">Para configurar a depuração remota, navegue até [Começar com dispositivos Android de depuração remota.][DevtoolsGuideChromiumRemoteDebuggingIndex]</span><span class="sxs-lookup"><span data-stu-id="0da6f-132">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="0da6f-133">Exibir as informações dos media players remotamente.</span><span class="sxs-lookup"><span data-stu-id="0da6f-133">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a><span data-ttu-id="0da6f-134">Ocultar e mostrar jogadores de mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-134">Hide and show media players</span></span>  

<span data-ttu-id="0da6f-135">Às vezes, você pode executar mais de um media player em uma página da Web ou usar a mesma guia do navegador para navegar em diferentes páginas da Web, cada uma com media players.</span><span class="sxs-lookup"><span data-stu-id="0da6f-135">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="0da6f-136">Você pode optar por ocultar \(ou mostrar\) cada media player para uma experiência de depuração mais fácil.</span><span class="sxs-lookup"><span data-stu-id="0da6f-136">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="0da6f-137">Navegue até várias páginas da Web de vídeo diferentes usando a mesma guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="0da6f-137">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="0da6f-138">Para ocultar media players, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="0da6f-138">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="0da6f-139">Para ocultar um media player, passe o mouse em um media player, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Ocultar player**.</span><span class="sxs-lookup"><span data-stu-id="0da6f-139">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="0da6f-140">Para ocultar todos os outros media players, passe o mouse em um media player, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Ocultar todos os outros**.</span><span class="sxs-lookup"><span data-stu-id="0da6f-140">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ocultar media players" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="0da6f-142">Ocultar media players</span><span class="sxs-lookup"><span data-stu-id="0da6f-142">Hide media players</span></span>  
    :::image-end:::  
    
## <a name="export-media-player-information"></a><span data-ttu-id="0da6f-143">Exportar informações do media player</span><span class="sxs-lookup"><span data-stu-id="0da6f-143">Export media player information</span></span>  

1.  <span data-ttu-id="0da6f-144">Para baixar as informações do media player como um arquivo JSON, passe o mouse em um media player, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar informações do player**.</span><span class="sxs-lookup"><span data-stu-id="0da6f-144">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportar informações de mídia" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="0da6f-146">Exportar informações de mídia</span><span class="sxs-lookup"><span data-stu-id="0da6f-146">Export media information</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0da6f-147">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0da6f-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra o Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximizando a produtividade com as ferramentas de desenvolvedor de borda | Bing Video"  

> [!NOTE]
> <span data-ttu-id="0da6f-151">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0da6f-151">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0da6f-152">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="0da6f-152">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0da6f-154">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0da6f-154">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

