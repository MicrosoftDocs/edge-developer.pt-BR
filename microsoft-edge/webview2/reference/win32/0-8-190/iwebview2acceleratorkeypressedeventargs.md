---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 5d052488d23f3d016ba2fd71eb929d5aa2ebea6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877361"
---
# <span data-ttu-id="e04b1-104">0.8.355-IWebView2AcceleratorKeyPressedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="e04b1-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e04b1-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e04b1-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e04b1-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e04b1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="e04b1-107">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e04b1-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="e04b1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e04b1-108">Summary</span></span>

 <span data-ttu-id="e04b1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e04b1-109">Members</span></span>                        | <span data-ttu-id="e04b1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e04b1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e04b1-111">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="e04b1-111">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="e04b1-112">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="e04b1-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="e04b1-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="e04b1-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="e04b1-114">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="e04b1-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="e04b1-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="e04b1-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="e04b1-116">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e04b1-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="e04b1-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="e04b1-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="e04b1-118">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e04b1-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="e04b1-119">Cuide</span><span class="sxs-lookup"><span data-stu-id="e04b1-119">Handle</span></span>](#handle) | <span data-ttu-id="e04b1-120">Ligar para isso permitirá que o processo do navegador continue.</span><span class="sxs-lookup"><span data-stu-id="e04b1-120">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="e04b1-121">Parte</span><span class="sxs-lookup"><span data-stu-id="e04b1-121">Members</span></span>

#### <span data-ttu-id="e04b1-122">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="e04b1-122">get_KeyEventType</span></span> 

<span data-ttu-id="e04b1-123">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="e04b1-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="e04b1-124">[get_KeyEventType](#get_keyeventtype)público HRESULT (WEBVIEW2_KEY_EVENT_TYPE \* keyeventtype)</span><span class="sxs-lookup"><span data-stu-id="e04b1-124">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="e04b1-125">Esta é uma das WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="e04b1-125">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="e04b1-126">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="e04b1-126">get_VirtualKey</span></span> 

<span data-ttu-id="e04b1-127">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="e04b1-127">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="e04b1-128">público HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="e04b1-128">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="e04b1-129">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="e04b1-129">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="e04b1-130">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="e04b1-130">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="e04b1-131">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="e04b1-131">get_KeyEventLParam</span></span> 

<span data-ttu-id="e04b1-132">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e04b1-132">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="e04b1-133">público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="e04b1-133">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="e04b1-134">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="e04b1-134">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="e04b1-135">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="e04b1-135">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="e04b1-136">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e04b1-136">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="e04b1-137">público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="e04b1-137">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="e04b1-138">Cuide</span><span class="sxs-lookup"><span data-stu-id="e04b1-138">Handle</span></span> 

<span data-ttu-id="e04b1-139">Ligar para isso permitirá que o processo do navegador continue.</span><span class="sxs-lookup"><span data-stu-id="e04b1-139">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="e04b1-140">[identificador](#handle)HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="e04b1-140">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="e04b1-141">Se você passar verdadeiro, o navegador não impedirá que o navegador execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="e04b1-141">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="e04b1-142">Se o manipulador de eventos retornar sem [identificador de chamada ()](#handle), é equivalente a identificador de chamada (falso).</span><span class="sxs-lookup"><span data-stu-id="e04b1-142">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="e04b1-143">Identificador de chamada [()](#handle) após ele já ter sido chamado ou o manipulador de eventos retornado não fará nada.</span><span class="sxs-lookup"><span data-stu-id="e04b1-143">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

