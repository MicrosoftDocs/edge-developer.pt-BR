---
description: Usar o painel de emulação para testar perfis de navegador diferentes, tamanhos de tela e resoluções e coordenadas de localização do GPS
title: DevTools-emulação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, emulação de dispositivo, design responsivo, geolocalização, resolução
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561436"
---
# <span data-ttu-id="a1497-104">Emulação</span><span class="sxs-lookup"><span data-stu-id="a1497-104">Emulation</span></span>

<span data-ttu-id="a1497-105">O painel *emulação* ajuda você a:</span><span class="sxs-lookup"><span data-stu-id="a1497-105">The *Emulation* panel helps you to:</span></span>
 - <span data-ttu-id="a1497-106">Simular vários [perfis de dispositivo](#device), [navegadores](#browser-profile), [tamanhos de tela e resoluções](#display)</span><span class="sxs-lookup"><span data-stu-id="a1497-106">Simulate various [device profiles](#device), [browsers](#browser-profile), [screen sizes and resolutions](#display)</span></span>
 - <span data-ttu-id="a1497-107">Testar diferentes [configurações de localização geográfica e coordenadas](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="a1497-107">Test different [geolocation settings and coordinates](#geolocation)</span></span>

![O painel de emulação do Microsoft Edge DevTools](./media/emulation.png)

1. <span data-ttu-id="a1497-109">O botão de **configurações de emulação de persistência** salvará todas as alterações feitas nas configurações de emulação de área de trabalho padrão, mesmo quando você fechar e reabrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="a1497-109">The **Persist Emulation settings** button will save any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span> 

2. <span data-ttu-id="a1497-110">O botão **Redefinir configurações de emulação** redefinirá as configurações de emulação para o perfil do navegador *da área de trabalho* padrão e a cadeia de caracteres do agente de usuário do Microsoft Edge com GPS desativado.</span><span class="sxs-lookup"><span data-stu-id="a1497-110">The **Reset Emulation settings** button will reset your emulation settings back to the default *Desktop* browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>

3. <span data-ttu-id="a1497-111">Quando qualquer uma dessas opções for alterada do padrão, a guia **emulação** mostrará um alerta informativo para indicar que algum aspecto do comportamento do seu navegador está sendo emulado.</span><span class="sxs-lookup"><span data-stu-id="a1497-111">When any of these options are changed from the default, the **Emulation** tab will show an informational alert to indicate that some aspect of your browser's behavior is being emulated.</span></span>

## <span data-ttu-id="a1497-112">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="a1497-112">Device</span></span>

<span data-ttu-id="a1497-113">Escolha em uma lista predefinida de perfis de dispositivo do Windows que configuram automaticamente as outras opções de emulação ou especifiquem seus próprios configuation *personalizados* .</span><span class="sxs-lookup"><span data-stu-id="a1497-113">Pick from a preset list of Windows device profiles which  automatically configure the other emulation options or specify your own *Custom* configuation.</span></span> <span data-ttu-id="a1497-114">Volte para o *padrão* para redefinir todas as ferramentas de emulação.</span><span class="sxs-lookup"><span data-stu-id="a1497-114">Switch back to *Default* to reset all the emulation tools.</span></span>

## <span data-ttu-id="a1497-115">Modo</span><span class="sxs-lookup"><span data-stu-id="a1497-115">Mode</span></span>

### <span data-ttu-id="a1497-116">Perfil do navegador</span><span class="sxs-lookup"><span data-stu-id="a1497-116">Browser profile</span></span>
<span data-ttu-id="a1497-117">Uma maneira rápida de simular a página em execução em um dispositivo Windows Phone é alterar a configuração do **perfil do navegador** para *Windows Phone*.</span><span class="sxs-lookup"><span data-stu-id="a1497-117">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to *Windows Phone*.</span></span>

#### <span data-ttu-id="a1497-118">Cadeia de caracteres do agente do usuário</span><span class="sxs-lookup"><span data-stu-id="a1497-118">User agent string</span></span>

<span data-ttu-id="a1497-119">Modificar sua cadeia de caracteres de agente do usuário para imitar outro navegador é uma boa primeira etapa em erros de depuração que ocorrem somente no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a1497-119">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span> 

<span data-ttu-id="a1497-120">Os scripts de front-end e/ou back-end às vezes usam a cadeia de caracteres do agente do usuário para detectar qual navegador você está usando.</span><span class="sxs-lookup"><span data-stu-id="a1497-120">Front end and/or back end scripts sometimes use the user agent string  to detect which browser you're using.</span></span> <span data-ttu-id="a1497-121">E mesmo quando você não estiver usando a detecção do navegador em seu próprio código, talvez esteja usando uma biblioteca JavaScript ou um script do lado do servidor de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a1497-121">And even when you're not using browser detection in your own code, you may be using a third-party JavaScript library or server-side script that does.</span></span>

<span data-ttu-id="a1497-122">O problema com a detecção do navegador é que ele é usado com frequência para redimensionar ou alterar os recursos em uma página da Web com base no que o desenvolvedor que escreve o script pensa que o seu navegador pode fazer, em vez de detectar o que o seu navegador pode realmente usar para a detecção de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1497-122">The problem with browser detection is that it's often used to scale back or change the features in a webpage based on what the developer writing the script thinks your browser can do, rather than detecting what your browser can actually do using feature detection.</span></span> <span data-ttu-id="a1497-123">Isso pode causar um comportamento inesperado, porque o código direcionado para Windows Internet Explorer 8 pode ser executado de forma muito diferente no Microsoft Edge; ou um recurso que pode ser perfeitamente compatível com o seu navegador pode ser desabilitado por causa de uma pressuposição feita pelo desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="a1497-123">This can cause unexpected behavior, because code targeted at Windows Internet Explorer 8 can run very differently in Microsoft Edge; or a feature your browser is perfectly capable of supporting might be disabled because of an assumption made by the developer.</span></span>

<span data-ttu-id="a1497-124">Se a alteração da cadeia de caracteres do agente do usuário apagar o problema, é provável que a detecção do navegador seja culpado.</span><span class="sxs-lookup"><span data-stu-id="a1497-124">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>

## <span data-ttu-id="a1497-125">Vídeo</span><span class="sxs-lookup"><span data-stu-id="a1497-125">Display</span></span>

<span data-ttu-id="a1497-126">A emulação de exibição permite que você visualize seu site em diferentes tamanhos de tela e resoluções: de monitores convencionais de área de trabalho para telas de dispositivos móveis menores ou monitores de alta resolução mais recentes.</span><span class="sxs-lookup"><span data-stu-id="a1497-126">Display emulation lets you preview your site on different screen sizes and resolutions: from conventional desktop monitors to smaller mobile screens or newer high-resolution displays.</span></span>

<span data-ttu-id="a1497-127">Emulações são adaptadas para experimentar e corresponderem às dimensões físicas das telas que estão sendo emuladas.</span><span class="sxs-lookup"><span data-stu-id="a1497-127">Emulations are adapted to try and match the physical dimensions of the screens being emulated.</span></span> <span data-ttu-id="a1497-128">Os pixels emulados podem parecer compactados ou expandidos, e a emulação não é recomendada se você precisar testar o posicionamento de pixels perfeitos dos elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="a1497-128">Emulated pixels might appear compressed or expanded, and emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span> <span data-ttu-id="a1497-129">No entanto, a emulação é boa para testar designs responsivos e identificar problemas maiores de posicionamento de elementos.</span><span class="sxs-lookup"><span data-stu-id="a1497-129">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>

### <span data-ttu-id="a1497-130">Orientação</span><span class="sxs-lookup"><span data-stu-id="a1497-130">Orientation</span></span>

<span data-ttu-id="a1497-131">Escolha em modo *paisagem* ou *retrato* .</span><span class="sxs-lookup"><span data-stu-id="a1497-131">Choose from *Landscape* or *Portrait* mode.</span></span>

### <span data-ttu-id="a1497-132">Resolução</span><span class="sxs-lookup"><span data-stu-id="a1497-132">Resolution</span></span>

<span data-ttu-id="a1497-133">Escolha uma lista predefinida de resoluções de dispositivos populares ou especifique sua configuração *personalizada* . Há suporte para resoluções de até 80 polegadas e 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="a1497-133">Choose from a preset list of popular device resolutions, or specify your own *Custom* config. Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>

## <span data-ttu-id="a1497-134">Geolocalização</span><span class="sxs-lookup"><span data-stu-id="a1497-134">Geolocation</span></span>

<span data-ttu-id="a1497-135">Se o seu site usa a [API de geolocalização](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) para fornecer serviços baseados em localização, você pode testar facilmente diferentes coordenadas de GPS e Estados de sensor da conveniência da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1497-135">If your site uses the [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) to provide location-based services, you can easily test different GPS coordinates and sensor states from the convenience of your desktop.</span></span> <span data-ttu-id="a1497-136">Essas configurações substituirão todas as coordenadas reais do GPS e o estado do sensor nas máquinas que dão suporte à localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="a1497-136">These settings will override any actual GPS coordinates and the sensor state on machines that support geolocation.</span></span> 

<span data-ttu-id="a1497-137">Assim como qualquer uso de dados pessoais na Web, os usuários precisam primeiro conceder permissão a seu site para usar o local.</span><span class="sxs-lookup"><span data-stu-id="a1497-137">As with any usage of personal data on the web, your users will first need to grant your site permission to use their location.</span></span> <span data-ttu-id="a1497-138">Você pode testar como o seu site se comporta com e sem permissões de localização no painel *configurações* do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="a1497-138">You can test how your site behaves with and without location permissions from the Microsoft Edge *Settings* panel:</span></span>

<span data-ttu-id="a1497-139">**...** >  **Configurações**  >  de **Exibir configurações avançadas**  >  **Permissões**  >  de site **Gerenciar**</span><span class="sxs-lookup"><span data-stu-id="a1497-139">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>

![Gerenciar permissões de site no painel configurações do Microsoft Edge](./media/settings_manage_permissions.png)

## <span data-ttu-id="a1497-141">Teclado</span><span class="sxs-lookup"><span data-stu-id="a1497-141">Shortcuts</span></span>

| <span data-ttu-id="a1497-142">Ação</span><span class="sxs-lookup"><span data-stu-id="a1497-142">Action</span></span>                   | <span data-ttu-id="a1497-143">Atalho</span><span class="sxs-lookup"><span data-stu-id="a1497-143">Shortcut</span></span>               |
|:-------------------------|:-----------------------|
| <span data-ttu-id="a1497-144">Redefinir configurações de emulação</span><span class="sxs-lookup"><span data-stu-id="a1497-144">Reset Emulation settings</span></span> | `CTRL` + `SHIFT` + `L` |
