---
description: Usar o painel de emulação para testar perfis de navegador diferentes, tamanhos de tela e resoluções e coordenadas de localização do GPS
title: DevTools-emulação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, emulação de dispositivo, design responsivo, geolocalização, resolução
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231483"
---
# <span data-ttu-id="af212-104">Emulação</span><span class="sxs-lookup"><span data-stu-id="af212-104">Emulation</span></span>  

> [!NOTE]
> <span data-ttu-id="af212-105">O novo Microsoft Edge é criado usando o Chromium e começa na versão 75.</span><span class="sxs-lookup"><span data-stu-id="af212-105">The new Microsoft Edge is built using Chromium, and starts at version 75.</span></span>  <span data-ttu-id="af212-106">Para obter mais informações, [Baixe o novo Microsoft Edge][MicrosoftNewEdge]e experimente as novas [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromium].</span><span class="sxs-lookup"><span data-stu-id="af212-106">For more information, [download the new Microsoft Edge][MicrosoftNewEdge], and try out the new [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromium].</span></span>  
> 
> <span data-ttu-id="af212-107">Para emular diferentes dispositivos, navegadores, tamanhos de tela e resoluções no novo DevTools, navegue para [emular dispositivos móveis no Microsoft Edge \ (Chromium \) devtools][DevtoolsGuideChromiumDeviceMode].</span><span class="sxs-lookup"><span data-stu-id="af212-107">To emulate different devices, browsers, screen sizes, and resolutions in the new DevTools, navigate to [Emulate Mobile Devices in Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span></span>  

<span data-ttu-id="af212-108">O painel **emulação** ajuda nas seguintes atividades.</span><span class="sxs-lookup"><span data-stu-id="af212-108">The **Emulation** panel helps with the following activities.</span></span>    

*   <span data-ttu-id="af212-109">Simular vários [perfis de dispositivo](#device), [navegadores](#browser-profile)e [tamanhos de tela e resoluções](#display)</span><span class="sxs-lookup"><span data-stu-id="af212-109">Simulate various [device profiles](#device), [browsers](#browser-profile), and [screen sizes and resolutions](#display)</span></span>  
*   <span data-ttu-id="af212-110">Testar diferentes [configurações de localização geográfica e coordenadas](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="af212-110">Test different [geolocation settings and coordinates](#geolocation)</span></span>  

:::image type="complex" source="./media/emulation.png" alt-text="O painel de emulação do Microsoft Edge DevTools" lightbox="./media/emulation.png":::
   <span data-ttu-id="af212-112">O painel de **emulação** do Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="af212-112">The Microsoft Edge DevTools **Emulation** panel</span></span>  
:::image-end:::  

1.  <span data-ttu-id="af212-113">O botão de **configurações de emulação de persistência** salva todas as alterações feitas nas configurações de emulação de área de trabalho padrão, mesmo quando você fecha e reabre o devtools.</span><span class="sxs-lookup"><span data-stu-id="af212-113">The **Persist Emulation settings** button saves any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span>  

1.  <span data-ttu-id="af212-114">O botão **Redefinir configurações de emulação** redefine as configurações de emulação de volta para o perfil do navegador da área de trabalho padrão e a cadeia de caracteres do agente de usuário do Microsoft Edge com GPS desativado.</span><span class="sxs-lookup"><span data-stu-id="af212-114">The **Reset Emulation settings** button resets your emulation settings back to the default Desktop browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>  

1.  <span data-ttu-id="af212-115">Quando qualquer uma dessas opções for alterada do padrão, a guia **emulação** exibirá um alerta informativo para indicar que algum aspecto do comportamento do seu navegador está sendo emulado.</span><span class="sxs-lookup"><span data-stu-id="af212-115">When any of these options are changed from the default, the **Emulation** tab displays an informational alert to indicate that some aspect of the behavior of your browser is being emulated.</span></span>  

## <span data-ttu-id="af212-116">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="af212-116">Device</span></span>  

<span data-ttu-id="af212-117">Escolha uma lista predefinida de perfis de dispositivo do Windows que configuram automaticamente as outras opções de emulação ou especifiquem sua própria configuração **personalizada** .</span><span class="sxs-lookup"><span data-stu-id="af212-117">Pick from a preset list of Windows device profiles that automatically configure the other emulation options or specify your own **Custom** configuration.</span></span>  <span data-ttu-id="af212-118">Volte para o **padrão** para redefinir todas as ferramentas de emulação.</span><span class="sxs-lookup"><span data-stu-id="af212-118">Switch back to **Default** to reset all the emulation tools.</span></span>  

## <span data-ttu-id="af212-119">Modo</span><span class="sxs-lookup"><span data-stu-id="af212-119">Mode</span></span>  

### <span data-ttu-id="af212-120">Perfil do navegador</span><span class="sxs-lookup"><span data-stu-id="af212-120">Browser profile</span></span>  

<span data-ttu-id="af212-121">Uma maneira rápida de simular a página em execução em um dispositivo Windows Phone é alterar a configuração do **perfil do navegador** para **Windows Phone**.</span><span class="sxs-lookup"><span data-stu-id="af212-121">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to **Windows Phone**.</span></span>  

#### <span data-ttu-id="af212-122">Cadeia de caracteres do agente do usuário</span><span class="sxs-lookup"><span data-stu-id="af212-122">User agent string</span></span>  

<span data-ttu-id="af212-123">Modificar sua cadeia de caracteres de agente do usuário para imitar outro navegador é uma boa primeira etapa em erros de depuração que ocorrem somente no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af212-123">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span>  

<span data-ttu-id="af212-124">Os scripts usam a cadeia de caracteres do agente do usuário para detectar qual navegador é usado.</span><span class="sxs-lookup"><span data-stu-id="af212-124">Scripts use the user agent string to detect which browser is used.</span></span>  <span data-ttu-id="af212-125">O script pode ser front-end, back-end ou front-end e back-end.</span><span class="sxs-lookup"><span data-stu-id="af212-125">Script may be front-end, back-end, or front-end and back-end.</span></span>  <span data-ttu-id="af212-126">Embora o código não use a detecção do navegador, o código pode herdar de uma biblioteca JavaScript ou script do lado do servidor de terceiros.</span><span class="sxs-lookup"><span data-stu-id="af212-126">Although your code does not use browser detection, your code may inherit it from a third-party JavaScript library or server-side script.</span></span>  

<span data-ttu-id="af212-127">O problema com a detecção do navegador é que você pode redimensionar \ (ou alterar \) recursos em sua página da Web usando pressuposições sobre recursos do navegador.</span><span class="sxs-lookup"><span data-stu-id="af212-127">The problem with browser detection is that you may scale-back \(or change\) features in your webpage using assumptions about browser capabilities.</span></span> <span data-ttu-id="af212-128">Em vez disso, você deve considerar o uso da detecção de recursos para detectar os recursos do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="af212-128">Instead, you should consider using feature detection to detect the capabilities of your browser.</span></span>  <span data-ttu-id="af212-129">Um comportamento inesperado pode ocorrer devido a uma das seguintes situações.</span><span class="sxs-lookup"><span data-stu-id="af212-129">Unexpected behavior may occur because of one of the following situations.</span></span>  

*   <span data-ttu-id="af212-130">O código direcionado para Windows Internet Explorer 8 pode funcionar de forma diferente no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af212-130">Code targeted at Windows Internet Explorer 8 may run differently in Microsoft Edge.</span></span>  
*   <span data-ttu-id="af212-131">Um recurso ao qual o seu navegador deve oferecer suporte está desabilitado, devido a uma pressuposição feita pelo desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="af212-131">A feature that your browser should support is disabled, because of an assumption made by the developer.</span></span>  

<span data-ttu-id="af212-132">Se a alteração da cadeia de caracteres do agente do usuário apagar o problema, é provável que a detecção do navegador seja culpado.</span><span class="sxs-lookup"><span data-stu-id="af212-132">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>  

## <span data-ttu-id="af212-133">Vídeo</span><span class="sxs-lookup"><span data-stu-id="af212-133">Display</span></span>  

<span data-ttu-id="af212-134">Emulação de exibição para visualizar o site em diferentes tamanhos de tela e resoluções.</span><span class="sxs-lookup"><span data-stu-id="af212-134">Display emulation to preview your site on different screen sizes and resolutions.</span></span>  

*   <span data-ttu-id="af212-135">monitores convencionais para área de trabalho</span><span class="sxs-lookup"><span data-stu-id="af212-135">conventional desktop monitors</span></span>  
*   <span data-ttu-id="af212-136">telas móveis menores</span><span class="sxs-lookup"><span data-stu-id="af212-136">smaller mobile screens</span></span>  
*   <span data-ttu-id="af212-137">monitores de alta resolução mais recentes</span><span class="sxs-lookup"><span data-stu-id="af212-137">newer high-resolution displays</span></span>  

<span data-ttu-id="af212-138">Emulações são adaptadas para tentar corresponderem às dimensões físicas das telas que estão sendo emuladas.</span><span class="sxs-lookup"><span data-stu-id="af212-138">Emulations are adapted to try to match the physical dimensions of the screens being emulated.</span></span>  <span data-ttu-id="af212-139">Os pixels emulados podem aparecer compactados ou expandidos.</span><span class="sxs-lookup"><span data-stu-id="af212-139">Emulated pixels may appear compressed or expanded.</span></span> <span data-ttu-id="af212-140">A emulação não será recomendada se você precisar testar o posicionamento perfeito de pixels dos elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="af212-140">Emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span>  <span data-ttu-id="af212-141">No entanto, a emulação é boa para testar designs responsivos e identificar problemas maiores de posicionamento de elementos.</span><span class="sxs-lookup"><span data-stu-id="af212-141">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>  

### <span data-ttu-id="af212-142">Orientação</span><span class="sxs-lookup"><span data-stu-id="af212-142">Orientation</span></span>  

<span data-ttu-id="af212-143">Escolha em modo **paisagem** ou **retrato** .</span><span class="sxs-lookup"><span data-stu-id="af212-143">Choose from **Landscape** or **Portrait** mode.</span></span>  

### <span data-ttu-id="af212-144">Resolução</span><span class="sxs-lookup"><span data-stu-id="af212-144">Resolution</span></span>  

<span data-ttu-id="af212-145">Escolha uma lista predefinida de resoluções de dispositivos populares ou especifique sua configuração **personalizada** .  Há suporte para resoluções de até 80 polegadas e 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="af212-145">Choose from a preset list of popular device resolutions, or specify your own **Custom** config.  Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>  

## <span data-ttu-id="af212-146">Geolocalização</span><span class="sxs-lookup"><span data-stu-id="af212-146">Geolocation</span></span>  

<span data-ttu-id="af212-147">Se o seu site usa a [API geolocalização][MdnGeolocationUsing] para fornecer serviços baseados em localização, as seguintes atividades estão disponíveis na conveniência da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="af212-147">If your website uses the [Geolocation API][MdnGeolocationUsing] to provide location-based services, the following activities are available from the convenience of your desktop.</span></span>  

*   <span data-ttu-id="af212-148">testar facilmente diferentes coordenadas do GPS</span><span class="sxs-lookup"><span data-stu-id="af212-148">easily test different GPS coordinates</span></span>  
*   <span data-ttu-id="af212-149">testar facilmente diferentes Estados do sensor</span><span class="sxs-lookup"><span data-stu-id="af212-149">easily test different sensor states</span></span>  

<span data-ttu-id="af212-150">As configurações substituem todas as coordenadas reais do GPS e o estado do sensor em dispositivos que dão suporte a geolocalização.</span><span class="sxs-lookup"><span data-stu-id="af212-150">The settings override any actual GPS coordinates and the sensor state on devices that support geolocation.</span></span>  

<span data-ttu-id="af212-151">Seu site deve solicitar e receber permissão de um usuário antes de usar o local do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af212-151">Your website must request and be granted permission from a user before using the device location.</span></span>  <span data-ttu-id="af212-152">Teste como o seu site se comporta com e sem permissões de localização no painel **configurações** do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af212-152">Test how your site behaves with and without location permissions from the Microsoft Edge **Settings** panel.</span></span>  

<span data-ttu-id="af212-153">**...** >  **Configurações**  >  de **Exibir configurações avançadas**  >  **Permissões**  >  de site **Gerenciar**</span><span class="sxs-lookup"><span data-stu-id="af212-153">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Gerenciar permissões de site no painel configurações do Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   <span data-ttu-id="af212-155">Gerenciar permissões de site no painel **configurações** do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="af212-155">Manage website permissions from the Microsoft Edge **Settings** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="af212-156">Atalhos</span><span class="sxs-lookup"><span data-stu-id="af212-156">Shortcuts</span></span>

| <span data-ttu-id="af212-157">Ação</span><span class="sxs-lookup"><span data-stu-id="af212-157">Action</span></span>  | <span data-ttu-id="af212-158">Atalho</span><span class="sxs-lookup"><span data-stu-id="af212-158">Shortcut</span></span>  |  
|:--- |:--- |  
| <span data-ttu-id="af212-159">Redefinir configurações de emulação</span><span class="sxs-lookup"><span data-stu-id="af212-159">Reset Emulation settings</span></span> | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Baixar novo navegador Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API de geolocalização | MDN"  
