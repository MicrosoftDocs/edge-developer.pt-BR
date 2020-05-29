---
description: Garantir que o conteúdo de mídia em seu site se destine conforme o esperado
title: Guia de desenvolvimento-políticas de reprodução automática
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 9/17/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: borda, mídia, vídeo, áudio, reprodução automática
ms.custom: seodec18
ms.openlocfilehash: 397c6f0a22359dbfab7c44370b0429147b7c9834
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560567"
---
# <span data-ttu-id="eba66-104">Políticas de reprodução automática</span><span class="sxs-lookup"><span data-stu-id="eba66-104">Autoplay Policies</span></span>

<span data-ttu-id="eba66-105">O Microsoft Edge fornece aos clientes a capacidade de personalizar suas preferências de navegação em sites que a mídia de reprodução automática com som para minimizar distrações na Web e conservar a largura de banda.</span><span class="sxs-lookup"><span data-stu-id="eba66-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="eba66-106">Adicionalmente, o Microsoft Edge suprime automaticamente a reprodução automática de mídia em guias de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="eba66-106">Additionaly, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="eba66-107">Os usuários podem personalizar o comportamento de mídia com os controles de reprodução automática [global](#global-media-autoplay-settings) e [por site](#per-site-media-autoplay-settings) , que fornecem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="eba66-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>

- <span data-ttu-id="eba66-108">**Permitir** é o padrão e continuará a reproduzir vídeos quando uma guia for exibida primeiro em primeiro plano, na critério do site.</span><span class="sxs-lookup"><span data-stu-id="eba66-108">**Allow**  is the default and will continue to play videos when a tab is first viewed in the foreground, at the site’s discretion.</span></span>

- <span data-ttu-id="eba66-109">**Limit** restringirá a reprodução automática para funcionar apenas quando os vídeos estiverem em mudo, para que os usuários nunca fiquem surpresos com o som.</span><span class="sxs-lookup"><span data-stu-id="eba66-109">**Limit** will restrict autoplay to only work when videos are muted, so users are never surprised by sound.</span></span> <span data-ttu-id="eba66-110">Quando o usuário clica em qualquer lugar na página, a reprodução automática é habilitada novamente e continuará a ser permitida dentro desse domínio nessa guia.</span><span class="sxs-lookup"><span data-stu-id="eba66-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>

- <span data-ttu-id="eba66-111">**Bloquear** irá impedir a reprodução automática em todos os sites até que os usuários interajam diretamente com o conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eba66-111">**Block** will prevent autoplay on all sites until users directly interact with the media content.</span></span>

## <span data-ttu-id="eba66-112">Configurações de reprodução automática de mídia global</span><span class="sxs-lookup"><span data-stu-id="eba66-112">Global media autoplay settings</span></span>

<span data-ttu-id="eba66-113">Os usuários podem controlar o comportamento de reprodução automática padrão para todos os sites em **Configuração avançada**  >  **reprodução automática de mídia**.</span><span class="sxs-lookup"><span data-stu-id="eba66-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>

![Configurações de reprodução automática de mídia global](../media/autoplay_global.png)

## <span data-ttu-id="eba66-115">Configurações de reprodução automática de mídia por site</span><span class="sxs-lookup"><span data-stu-id="eba66-115">Per-site media autoplay settings</span></span>

<span data-ttu-id="eba66-116">Os usuários podem controlar o comportamento da reprodução automática em cada site, na seção **permissões do site** do painel de informações do site.</span><span class="sxs-lookup"><span data-stu-id="eba66-116">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span> <span data-ttu-id="eba66-117">Essa configuração pode ser encontrada clicando no ícone de informações ou no ícone de cadeado no lado esquerdo da barra de endereços e clicando em "configurações de reprodução automática de mídia" para começar.</span><span class="sxs-lookup"><span data-stu-id="eba66-117">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on “Media autoplay settings” to get started.</span></span>

<span data-ttu-id="eba66-118">As configurações por site substituem a configuração global.</span><span class="sxs-lookup"><span data-stu-id="eba66-118">Per-site settings override the global setting.</span></span> <span data-ttu-id="eba66-119">Por exemplo, se um usuário tiver sua configuração global definida como "permitir", mas alterar uma configuração por site para "bloquear", a reprodução automática será bloqueada para esse site.</span><span class="sxs-lookup"><span data-stu-id="eba66-119">For example, if a user has their global setting set to “Allow” but changes a per-site setting to “Block”, autoplay will be blocked for that site.</span></span>

![Configurações de reprodução automática de mídia por site](../media/autoplay_per-site.png)
 
## <span data-ttu-id="eba66-121">Práticas recomendadas para desenvolvedores da Web</span><span class="sxs-lookup"><span data-stu-id="eba66-121">Best Practices for Web Developers</span></span>

<span data-ttu-id="eba66-122">Veja como garantir uma boa experiência do usuário com mídia hospedada em seu site:</span><span class="sxs-lookup"><span data-stu-id="eba66-122">Here's how to ensure a good user experience with media hosted on your site:</span></span>

- <span data-ttu-id="eba66-123">Suponha que cada uso de um elemento de mídia ouvirá exija um gesto do usuário para iniciar a reprodução (, pois os usuários podem bloquear a reprodução automática em qualquer point-in-time) e planejar de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="eba66-123">Assume  each use of a media element wil require a user gesture to start the playback (as users can block autoplay at any point in time) and plan accordingly.</span></span>  <span data-ttu-id="eba66-124">Políticas de reprodução automática global e por site aplicam-se a todos os `<audio>` `<video>` elementos, independentemente de como eles são usados no seu site</span><span class="sxs-lookup"><span data-stu-id="eba66-124">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>

- <span data-ttu-id="eba66-125">Verifique se os controles de mídia estão sempre presentes na mídia de site e no conteúdo do anúncio.</span><span class="sxs-lookup"><span data-stu-id="eba66-125">Ensure that media controls are always present on both site media and ad content.</span></span> <span data-ttu-id="eba66-126">Isso dará aos usuários a capacidade de reiniciar a reprodução se a reprodução automática estiver bloqueada na página.</span><span class="sxs-lookup"><span data-stu-id="eba66-126">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>

- <span data-ttu-id="eba66-127">Avalie como a reprodução automática pode afetar a experiência dos usuários no seu site e considere o uso da reprodução automática de forma a minimizar a reprodução de mídia indesejada.</span><span class="sxs-lookup"><span data-stu-id="eba66-127">Evaluate how autoplay may affect users’ experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span> <span data-ttu-id="eba66-128">Se a reprodução automática for uma parte crucial da sua experiência, considere o uso de conteúdo sem áudio para iniciar e permitir que o usuário o ative.</span><span class="sxs-lookup"><span data-stu-id="eba66-128">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span> <span data-ttu-id="eba66-129">Para que o conteúdo seja ativado para a reprodução automática, a fonte de áudio deve ser ativada ou desativada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="eba66-129">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span> <span data-ttu-id="eba66-130">Caso contrário, o elemento não será considerado mudo.</span><span class="sxs-lookup"><span data-stu-id="eba66-130">Otherwise the element will not be considered as muted.</span></span>

- <span data-ttu-id="eba66-131">A menos que seja absolutamente necessário fazer o contrário, use os controles nativos do navegador para reprodução de mídia.</span><span class="sxs-lookup"><span data-stu-id="eba66-131">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span> <span data-ttu-id="eba66-132">Isso irá assegurar uma experiência consistente para os usuários.</span><span class="sxs-lookup"><span data-stu-id="eba66-132">This will ensure a consistent experience for users.</span></span> <span data-ttu-id="eba66-133">Se você estiver criando controles personalizados em vez disso, verifique se os controles de mídia estão sempre presentes e se seus controles reagir corretamente à supressão da reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="eba66-133">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>

### <span data-ttu-id="eba66-134">Delegação de iframe</span><span class="sxs-lookup"><span data-stu-id="eba66-134">Iframe delegation</span></span>

<span data-ttu-id="eba66-135">A reprodução automática em uma `<iframe>` herdará a permissão de reprodução automática da página pai, independentemente da origem do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eba66-135">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span> <span data-ttu-id="eba66-136">Em um cenário de playlist em que cada arquivo de mídia é hospedado por um iframe separado, o usuário só precisaria iniciar uma reprodução uma vez para toda a playlist.</span><span class="sxs-lookup"><span data-stu-id="eba66-136">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>

### <span data-ttu-id="eba66-137">Detectando quando a reprodução automática é permitida</span><span class="sxs-lookup"><span data-stu-id="eba66-137">Detecting when autoplay is allowed</span></span>

<span data-ttu-id="eba66-138">Você pode ajustar os controles de reprodução para exibir o estado correto quando a reprodução automática estiver bloqueada examinando a promessa retornada pela `play()` função no elemento de mídia:</span><span class="sxs-lookup"><span data-stu-id="eba66-138">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>

```Javascript

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
