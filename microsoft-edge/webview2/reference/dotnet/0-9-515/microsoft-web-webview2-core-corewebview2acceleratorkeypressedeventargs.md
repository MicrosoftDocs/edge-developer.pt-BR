---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b0df25ffe3b00267dfff15cd50d1d3db6a7e38bb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698215"
---
# <span data-ttu-id="8d957-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8d957-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="8d957-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="8d957-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8d957-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8d957-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="8d957-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8d957-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8d957-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="8d957-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8d957-109">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="8d957-109">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="8d957-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="8d957-110">Summary</span></span>

 <span data-ttu-id="8d957-111">Parte</span><span class="sxs-lookup"><span data-stu-id="8d957-111">Members</span></span>                        | <span data-ttu-id="8d957-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="8d957-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8d957-113">Handled</span><span class="sxs-lookup"><span data-stu-id="8d957-113">Handled</span></span>](#handled) | <span data-ttu-id="8d957-114">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="8d957-114">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="8d957-115">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="8d957-115">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="8d957-116">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="8d957-116">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="8d957-117">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="8d957-117">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="8d957-118">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8d957-118">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="8d957-119">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8d957-119">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="8d957-120">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8d957-120">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="8d957-121">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="8d957-121">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="8d957-122">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="8d957-122">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="8d957-123">Parte</span><span class="sxs-lookup"><span data-stu-id="8d957-123">Members</span></span>

#### <span data-ttu-id="8d957-124">Handled</span><span class="sxs-lookup"><span data-stu-id="8d957-124">Handled</span></span> 

<span data-ttu-id="8d957-125">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="8d957-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="8d957-126">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="8d957-126">public bool [Handled](#handled)</span></span>

<span data-ttu-id="8d957-127">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="8d957-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="8d957-128">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="8d957-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="8d957-129">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="8d957-129">KeyEventKind</span></span> 

<span data-ttu-id="8d957-130">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="8d957-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="8d957-131">[CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) público [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="8d957-131">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="8d957-132">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="8d957-132">KeyEventLParam</span></span> 

<span data-ttu-id="8d957-133">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8d957-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="8d957-134">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="8d957-134">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="8d957-135">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="8d957-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="8d957-136">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8d957-136">PhysicalKeyStatus</span></span> 

<span data-ttu-id="8d957-137">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8d957-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="8d957-138">[CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) público [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="8d957-138">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="8d957-139">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="8d957-139">VirtualKey</span></span> 

<span data-ttu-id="8d957-140">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="8d957-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="8d957-141">Public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="8d957-141">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="8d957-142">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="8d957-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="8d957-143">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="8d957-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

