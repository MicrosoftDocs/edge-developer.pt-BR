---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: 16af4247c494d1d09155110755d7936487f2e84e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011520"
---
# <span data-ttu-id="83ebc-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="83ebc-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

<span data-ttu-id="83ebc-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="83ebc-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="83ebc-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="83ebc-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="83ebc-107">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="83ebc-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="83ebc-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="83ebc-108">Summary</span></span>

 <span data-ttu-id="83ebc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="83ebc-109">Members</span></span>                        | <span data-ttu-id="83ebc-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="83ebc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="83ebc-111">Handled</span><span class="sxs-lookup"><span data-stu-id="83ebc-111">Handled</span></span>](#handled) | <span data-ttu-id="83ebc-112">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="83ebc-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="83ebc-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="83ebc-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="83ebc-114">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="83ebc-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="83ebc-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="83ebc-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="83ebc-116">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="83ebc-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="83ebc-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="83ebc-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="83ebc-118">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="83ebc-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="83ebc-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="83ebc-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="83ebc-120">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="83ebc-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="83ebc-121">Parte</span><span class="sxs-lookup"><span data-stu-id="83ebc-121">Members</span></span>

#### <span data-ttu-id="83ebc-122">Handled</span><span class="sxs-lookup"><span data-stu-id="83ebc-122">Handled</span></span> 

<span data-ttu-id="83ebc-123">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="83ebc-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="83ebc-124">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="83ebc-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="83ebc-125">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="83ebc-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="83ebc-126">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="83ebc-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="83ebc-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="83ebc-127">KeyEventKind</span></span> 

<span data-ttu-id="83ebc-128">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="83ebc-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="83ebc-129">[CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) público [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="83ebc-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="83ebc-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="83ebc-130">KeyEventLParam</span></span> 

<span data-ttu-id="83ebc-131">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="83ebc-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="83ebc-132">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="83ebc-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="83ebc-133">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="83ebc-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="83ebc-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="83ebc-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="83ebc-135">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="83ebc-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="83ebc-136">[CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) público [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="83ebc-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="83ebc-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="83ebc-137">VirtualKey</span></span> 

<span data-ttu-id="83ebc-138">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="83ebc-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="83ebc-139">Public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="83ebc-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="83ebc-140">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="83ebc-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="83ebc-141">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="83ebc-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

