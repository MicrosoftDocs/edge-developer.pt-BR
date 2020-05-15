---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 1168749b27488831d914a4f64c0830f39d53415f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652760"
---
# <span data-ttu-id="60893-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="60893-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="60893-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="60893-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="60893-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="60893-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="60893-107">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="60893-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="60893-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="60893-108">Summary</span></span>

 <span data-ttu-id="60893-109">Parte</span><span class="sxs-lookup"><span data-stu-id="60893-109">Members</span></span>                        | <span data-ttu-id="60893-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="60893-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="60893-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="60893-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="60893-112">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="60893-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="60893-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="60893-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="60893-114">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="60893-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="60893-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="60893-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="60893-116">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="60893-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="60893-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="60893-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="60893-118">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="60893-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="60893-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="60893-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="60893-120">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="60893-120">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="60893-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="60893-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="60893-122">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="60893-122">Sets the Handled property.</span></span>

## <span data-ttu-id="60893-123">Parte</span><span class="sxs-lookup"><span data-stu-id="60893-123">Members</span></span>

#### <span data-ttu-id="60893-124">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="60893-124">get_KeyEventKind</span></span> 

<span data-ttu-id="60893-125">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="60893-125">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="60893-126">público HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="60893-126">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="60893-127">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="60893-127">get_VirtualKey</span></span> 

<span data-ttu-id="60893-128">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="60893-128">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="60893-129">público HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="60893-129">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="60893-130">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="60893-130">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="60893-131">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="60893-131">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="60893-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="60893-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="60893-133">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="60893-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="60893-134">público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="60893-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="60893-135">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="60893-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="60893-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="60893-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="60893-137">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="60893-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="60893-138">público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="60893-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="60893-139">get_Handled</span><span class="sxs-lookup"><span data-stu-id="60893-139">get_Handled</span></span> 

<span data-ttu-id="60893-140">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="60893-140">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="60893-141">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="60893-141">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="60893-142">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="60893-142">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="60893-143">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="60893-143">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="60893-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="60893-144">put_Handled</span></span> 

<span data-ttu-id="60893-145">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="60893-145">Sets the Handled property.</span></span>

> <span data-ttu-id="60893-146">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="60893-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

