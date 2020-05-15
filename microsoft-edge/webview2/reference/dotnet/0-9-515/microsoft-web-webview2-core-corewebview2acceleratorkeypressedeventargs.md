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
ms.openlocfilehash: ef2eb16f6ba0186494400e6190d316ea503f9f16
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652673"
---
# <span data-ttu-id="7af76-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7af76-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

<span data-ttu-id="7af76-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7af76-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7af76-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="7af76-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7af76-107">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7af76-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="7af76-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7af76-108">Summary</span></span>

 <span data-ttu-id="7af76-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7af76-109">Members</span></span>                        | <span data-ttu-id="7af76-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7af76-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7af76-111">Handled</span><span class="sxs-lookup"><span data-stu-id="7af76-111">Handled</span></span>](#handled) | <span data-ttu-id="7af76-112">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="7af76-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="7af76-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="7af76-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="7af76-114">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="7af76-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="7af76-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="7af76-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="7af76-116">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="7af76-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="7af76-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="7af76-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="7af76-118">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="7af76-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="7af76-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="7af76-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="7af76-120">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="7af76-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="7af76-121">Parte</span><span class="sxs-lookup"><span data-stu-id="7af76-121">Members</span></span>

#### <span data-ttu-id="7af76-122">Handled</span><span class="sxs-lookup"><span data-stu-id="7af76-122">Handled</span></span> 

<span data-ttu-id="7af76-123">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="7af76-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="7af76-124">bool público [manipulado](#handled)</span><span class="sxs-lookup"><span data-stu-id="7af76-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="7af76-125">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="7af76-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="7af76-126">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="7af76-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="7af76-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="7af76-127">KeyEventKind</span></span> 

<span data-ttu-id="7af76-128">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="7af76-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="7af76-129">[CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) público [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="7af76-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="7af76-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="7af76-130">KeyEventLParam</span></span> 

<span data-ttu-id="7af76-131">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="7af76-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="7af76-132">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="7af76-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="7af76-133">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="7af76-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="7af76-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="7af76-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="7af76-135">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="7af76-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="7af76-136">[CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) público [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="7af76-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="7af76-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="7af76-137">VirtualKey</span></span> 

<span data-ttu-id="7af76-138">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="7af76-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="7af76-139">Public uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="7af76-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="7af76-140">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="7af76-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="7af76-141">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="7af76-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

