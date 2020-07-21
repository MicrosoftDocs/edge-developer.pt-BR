---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885048"
---
# <span data-ttu-id="e4786-104">0.8.355-IWebView2AcceleratorKeyPressedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="e4786-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="e4786-105">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e4786-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="e4786-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e4786-106">Summary</span></span>

 <span data-ttu-id="e4786-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e4786-107">Members</span></span>                        | <span data-ttu-id="e4786-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e4786-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4786-109">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="e4786-109">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="e4786-110">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="e4786-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="e4786-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="e4786-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="e4786-112">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="e4786-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="e4786-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="e4786-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="e4786-114">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e4786-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="e4786-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="e4786-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="e4786-116">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e4786-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="e4786-117">Cuide</span><span class="sxs-lookup"><span data-stu-id="e4786-117">Handle</span></span>](#handle) | <span data-ttu-id="e4786-118">Ligar para isso permitirá que o processo do navegador continue.</span><span class="sxs-lookup"><span data-stu-id="e4786-118">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="e4786-119">Parte</span><span class="sxs-lookup"><span data-stu-id="e4786-119">Members</span></span>

#### <span data-ttu-id="e4786-120">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="e4786-120">get_KeyEventType</span></span> 

<span data-ttu-id="e4786-121">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="e4786-121">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="e4786-122">[get_KeyEventType](#get_keyeventtype)público HRESULT (WEBVIEW2_KEY_EVENT_TYPE \* keyeventtype)</span><span class="sxs-lookup"><span data-stu-id="e4786-122">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="e4786-123">Esta é uma das WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="e4786-123">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="e4786-124">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="e4786-124">get_VirtualKey</span></span> 

<span data-ttu-id="e4786-125">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="e4786-125">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="e4786-126">público HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="e4786-126">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="e4786-127">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="e4786-127">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="e4786-128">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="e4786-128">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="e4786-129">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="e4786-129">get_KeyEventLParam</span></span> 

<span data-ttu-id="e4786-130">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e4786-130">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="e4786-131">público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="e4786-131">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="e4786-132">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="e4786-132">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="e4786-133">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="e4786-133">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="e4786-134">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="e4786-134">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="e4786-135">público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="e4786-135">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="e4786-136">Cuide</span><span class="sxs-lookup"><span data-stu-id="e4786-136">Handle</span></span> 

<span data-ttu-id="e4786-137">Ligar para isso permitirá que o processo do navegador continue.</span><span class="sxs-lookup"><span data-stu-id="e4786-137">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="e4786-138">[identificador](#handle)HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="e4786-138">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="e4786-139">Se você passar verdadeiro, o navegador não impedirá que o navegador execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="e4786-139">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="e4786-140">Se o manipulador de eventos retornar sem [identificador de chamada ()](#handle), é equivalente a identificador de chamada (falso).</span><span class="sxs-lookup"><span data-stu-id="e4786-140">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="e4786-141">Identificador de chamada [()](#handle) após ele já ter sido chamado ou o manipulador de eventos retornado não fará nada.</span><span class="sxs-lookup"><span data-stu-id="e4786-141">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

