---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 25d11995dd305a1958d6252c2ddf3afdb313fad1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697179"
---
# <span data-ttu-id="de999-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="de999-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="de999-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="de999-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="de999-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="de999-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="de999-107">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="de999-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="de999-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="de999-108">Summary</span></span>

 <span data-ttu-id="de999-109">Parte</span><span class="sxs-lookup"><span data-stu-id="de999-109">Members</span></span>                        | <span data-ttu-id="de999-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="de999-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="de999-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="de999-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="de999-112">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="de999-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="de999-113">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="de999-113">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="de999-114">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="de999-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="de999-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="de999-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="de999-116">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="de999-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="de999-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="de999-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="de999-118">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="de999-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="de999-119">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="de999-119">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="de999-120">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="de999-120">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="de999-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="de999-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="de999-122">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="de999-122">Sets the Handled property.</span></span>

## <span data-ttu-id="de999-123">Parte</span><span class="sxs-lookup"><span data-stu-id="de999-123">Members</span></span>

#### <span data-ttu-id="de999-124">get_Handled</span><span class="sxs-lookup"><span data-stu-id="de999-124">get_Handled</span></span> 

<span data-ttu-id="de999-125">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="de999-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="de999-126">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="de999-126">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="de999-127">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="de999-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="de999-128">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="de999-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="de999-129">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="de999-129">get_KeyEventKind</span></span> 

<span data-ttu-id="de999-130">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="de999-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="de999-131">público HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="de999-131">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="de999-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="de999-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="de999-133">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="de999-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="de999-134">público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="de999-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="de999-135">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="de999-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="de999-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="de999-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="de999-137">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="de999-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="de999-138">público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="de999-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="de999-139">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="de999-139">get_VirtualKey</span></span> 

<span data-ttu-id="de999-140">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="de999-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="de999-141">público HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="de999-141">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="de999-142">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="de999-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="de999-143">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="de999-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="de999-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="de999-144">put_Handled</span></span> 

<span data-ttu-id="de999-145">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="de999-145">Sets the Handled property.</span></span>

> <span data-ttu-id="de999-146">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="de999-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

