---
description: Garantir que o conteúdo de mídia em seu site se destine conforme o esperado
title: Políticas de reprodução automática-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: borda, mídia, vídeo, áudio, reprodução automática
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 85b91a8b87d73d6fccc6eac2aa64513f283d7f21
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231532"
---
# <span data-ttu-id="06cbb-104">Políticas de reprodução automática</span><span class="sxs-lookup"><span data-stu-id="06cbb-104">Autoplay Policies</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="06cbb-105">O Microsoft Edge fornece aos clientes a capacidade de personalizar suas preferências de navegação em sites que a mídia de reprodução automática com som para minimizar distrações na Web e conservar a largura de banda.</span><span class="sxs-lookup"><span data-stu-id="06cbb-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="06cbb-106">Além disso, o Microsoft Edge automaticamente suprime a reprodução automática de mídia em guias de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="06cbb-106">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="06cbb-107">Os usuários podem personalizar o comportamento de mídia com os controles de reprodução automática [global](#global-media-autoplay-settings) e [por site](#per-site-media-autoplay-settings) , que fornecem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="06cbb-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>  

*   `Allow`  <span data-ttu-id="06cbb-108">O padrão e continuarão a reproduzir vídeos quando uma guia for exibida primeiro em primeiro plano, no caso do site.</span><span class="sxs-lookup"><span data-stu-id="06cbb-108">The default and will continue to play videos when a tab is first viewed in the foreground, at the site's discretion.</span></span>  

*   `Limit`  <span data-ttu-id="06cbb-109">Restringe a reprodução automática para funcionar apenas quando os vídeos estiverem em mudo, para que os usuários nunca fiquem surpresos com o som.</span><span class="sxs-lookup"><span data-stu-id="06cbb-109">Restricts autoplay to only work when videos are muted, so users are never surprised by sound.</span></span>  <span data-ttu-id="06cbb-110">Quando o usuário clica em qualquer lugar na página, a reprodução automática é habilitada novamente e continuará a ser permitida dentro desse domínio nessa guia.</span><span class="sxs-lookup"><span data-stu-id="06cbb-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>  

*   `Block`  <span data-ttu-id="06cbb-111">Evite o sautoplay em todos os sites até que os usuários interajam diretamente com o conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="06cbb-111">Prevent sautoplay on all sites until users directly interact with the media content.</span></span>  

## <span data-ttu-id="06cbb-112">Configurações de reprodução automática de mídia global</span><span class="sxs-lookup"><span data-stu-id="06cbb-112">Global media autoplay settings</span></span>  

<span data-ttu-id="06cbb-113">Os usuários podem controlar o comportamento de reprodução automática padrão para todos os sites em **Configuração avançada**  >  **reprodução automática de mídia**.</span><span class="sxs-lookup"><span data-stu-id="06cbb-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Configurações de reprodução automática de mídia global" lightbox="../media/autoplay_global.png":::
   <span data-ttu-id="06cbb-115">Configurações de reprodução automática de mídia global</span><span class="sxs-lookup"><span data-stu-id="06cbb-115">Global media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="06cbb-116">Configurações de reprodução automática de mídia por site</span><span class="sxs-lookup"><span data-stu-id="06cbb-116">Per-site media autoplay settings</span></span>  

<span data-ttu-id="06cbb-117">Os usuários podem controlar o comportamento da reprodução automática em cada site, na seção **permissões do site** do painel de informações do site.</span><span class="sxs-lookup"><span data-stu-id="06cbb-117">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span>  <span data-ttu-id="06cbb-118">Essa configuração pode ser encontrada clicando no ícone de informações ou no ícone de cadeado no lado esquerdo da barra de endereços e clicando em **configurações de reprodução automática de mídia** para começar.</span><span class="sxs-lookup"><span data-stu-id="06cbb-118">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on **Media autoplay settings** to get started.</span></span>  

<span data-ttu-id="06cbb-119">As configurações por site substituem a configuração global.</span><span class="sxs-lookup"><span data-stu-id="06cbb-119">Per-site settings override the global setting.</span></span>  <span data-ttu-id="06cbb-120">Por exemplo, se um usuário tiver sua configuração global definida como, `Allow` mas alterar uma configuração por site para `Block` , a reprodução automática será bloqueada para esse site.</span><span class="sxs-lookup"><span data-stu-id="06cbb-120">For example, if a user has their global setting set to `Allow` but changes a per-site setting to `Block`, autoplay will be blocked for that site.</span></span>  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Configurações de reprodução automática de mídia por site" lightbox="../media/autoplay_per-site.png":::
   <span data-ttu-id="06cbb-122">Configurações de reprodução automática de mídia por site</span><span class="sxs-lookup"><span data-stu-id="06cbb-122">Per-site media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="06cbb-123">Práticas recomendadas para desenvolvedores da Web</span><span class="sxs-lookup"><span data-stu-id="06cbb-123">Best Practices for Web Developers</span></span>  

<span data-ttu-id="06cbb-124">Veja como garantir uma boa experiência do usuário com mídia hospedada em seu site:</span><span class="sxs-lookup"><span data-stu-id="06cbb-124">Here's how to ensure a good user experience with media hosted on your site:</span></span>  

*   <span data-ttu-id="06cbb-125">Suponha que cada uso de um elemento de mídia ouvirá exija um gesto do usuário para iniciar a reprodução \(à medida que os usuários podem bloquear a reprodução automática em qualquer point-in-time \) e planeje-se adequadamente.</span><span class="sxs-lookup"><span data-stu-id="06cbb-125">Assume each use of a media element wil require a user gesture to start the playback \(as users can block autoplay at any point in time\) and plan accordingly.</span></span>  <span data-ttu-id="06cbb-126">Políticas de reprodução automática global e por site aplicam-se a todos os `<audio>` `<video>` elementos, independentemente de como eles são usados no seu site</span><span class="sxs-lookup"><span data-stu-id="06cbb-126">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>  

*   <span data-ttu-id="06cbb-127">Verifique se os controles de mídia estão sempre presentes na mídia de site e no conteúdo do anúncio.</span><span class="sxs-lookup"><span data-stu-id="06cbb-127">Ensure that media controls are always present on both site media and ad content.</span></span>  <span data-ttu-id="06cbb-128">Isso dará aos usuários a capacidade de reiniciar a reprodução se a reprodução automática estiver bloqueada na página.</span><span class="sxs-lookup"><span data-stu-id="06cbb-128">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>  

*   <span data-ttu-id="06cbb-129">Avalie como a reprodução automática pode afetar a experiência dos usuários no seu site e considere o uso da reprodução automática de forma a minimizar a reprodução de mídia indesejada.</span><span class="sxs-lookup"><span data-stu-id="06cbb-129">Evaluate how autoplay may affect users' experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span>  <span data-ttu-id="06cbb-130">Se a reprodução automática for uma parte crucial da sua experiência, considere o uso de conteúdo sem áudio para iniciar e permitir que o usuário o ative.</span><span class="sxs-lookup"><span data-stu-id="06cbb-130">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span>  <span data-ttu-id="06cbb-131">Para que o conteúdo seja ativado para a reprodução automática, a fonte de áudio deve ser ativada ou desativada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="06cbb-131">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span>  <span data-ttu-id="06cbb-132">Caso contrário, o elemento não será considerado mudo.</span><span class="sxs-lookup"><span data-stu-id="06cbb-132">Otherwise the element will not be considered as muted.</span></span>  

*   <span data-ttu-id="06cbb-133">A menos que seja absolutamente necessário fazer o contrário, use os controles nativos do navegador para reprodução de mídia.</span><span class="sxs-lookup"><span data-stu-id="06cbb-133">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span>  <span data-ttu-id="06cbb-134">Isso irá assegurar uma experiência consistente para os usuários.</span><span class="sxs-lookup"><span data-stu-id="06cbb-134">This will ensure a consistent experience for users.</span></span>  <span data-ttu-id="06cbb-135">Se você estiver criando controles personalizados em vez disso, verifique se os controles de mídia estão sempre presentes e se seus controles reagir corretamente à supressão da reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="06cbb-135">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>  

### <span data-ttu-id="06cbb-136">Delegação de iframe</span><span class="sxs-lookup"><span data-stu-id="06cbb-136">Iframe delegation</span></span>  

<span data-ttu-id="06cbb-137">A reprodução automática em uma `<iframe>` herdará a permissão de reprodução automática da página pai, independentemente da origem do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="06cbb-137">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span>  <span data-ttu-id="06cbb-138">Em um cenário de playlist em que cada arquivo de mídia é hospedado por um iframe separado, o usuário só precisaria iniciar uma reprodução uma vez para toda a playlist.</span><span class="sxs-lookup"><span data-stu-id="06cbb-138">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>  

### <span data-ttu-id="06cbb-139">Detectando quando a reprodução automática é permitida</span><span class="sxs-lookup"><span data-stu-id="06cbb-139">Detecting when autoplay is allowed</span></span>  

<span data-ttu-id="06cbb-140">Você pode ajustar os controles de reprodução para exibir o estado correto quando a reprodução automática estiver bloqueada examinando a promessa retornada pela `play()` função no elemento de mídia:</span><span class="sxs-lookup"><span data-stu-id="06cbb-140">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  
