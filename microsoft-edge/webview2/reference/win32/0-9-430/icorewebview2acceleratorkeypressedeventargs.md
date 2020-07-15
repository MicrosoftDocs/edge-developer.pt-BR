---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: e7a512201c1ef7917a54b93dbd06587294e76f78
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881176"
---
# <span data-ttu-id="8b95a-104">0.9.430-ICoreWebView2AcceleratorKeyPressedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="8b95a-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8b95a-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8b95a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8b95a-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8b95a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="8b95a-107">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="8b95a-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="8b95a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8b95a-108">Summary</span></span>

 <span data-ttu-id="8b95a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8b95a-109">Members</span></span>                        | <span data-ttu-id="8b95a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8b95a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b95a-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="8b95a-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="8b95a-112">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="8b95a-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="8b95a-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="8b95a-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="8b95a-114">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="8b95a-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="8b95a-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="8b95a-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="8b95a-116">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8b95a-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="8b95a-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8b95a-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="8b95a-118">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8b95a-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="8b95a-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="8b95a-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="8b95a-120">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="8b95a-120">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="8b95a-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="8b95a-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="8b95a-122">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="8b95a-122">Sets the Handled property.</span></span>

## <span data-ttu-id="8b95a-123">Parte</span><span class="sxs-lookup"><span data-stu-id="8b95a-123">Members</span></span>

#### <span data-ttu-id="8b95a-124">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="8b95a-124">get_KeyEventKind</span></span> 

<span data-ttu-id="8b95a-125">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="8b95a-125">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="8b95a-126">público HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="8b95a-126">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="8b95a-127">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="8b95a-127">get_VirtualKey</span></span> 

<span data-ttu-id="8b95a-128">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="8b95a-128">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="8b95a-129">público HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="8b95a-129">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="8b95a-130">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="8b95a-130">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="8b95a-131">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="8b95a-131">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="8b95a-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="8b95a-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="8b95a-133">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8b95a-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="8b95a-134">público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="8b95a-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="8b95a-135">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="8b95a-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="8b95a-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8b95a-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="8b95a-137">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="8b95a-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="8b95a-138">público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="8b95a-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="8b95a-139">get_Handled</span><span class="sxs-lookup"><span data-stu-id="8b95a-139">get_Handled</span></span> 

<span data-ttu-id="8b95a-140">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="8b95a-140">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="8b95a-141">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="8b95a-141">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="8b95a-142">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="8b95a-142">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="8b95a-143">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="8b95a-143">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="8b95a-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="8b95a-144">put_Handled</span></span> 

<span data-ttu-id="8b95a-145">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="8b95a-145">Sets the Handled property.</span></span>

> <span data-ttu-id="8b95a-146">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="8b95a-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

