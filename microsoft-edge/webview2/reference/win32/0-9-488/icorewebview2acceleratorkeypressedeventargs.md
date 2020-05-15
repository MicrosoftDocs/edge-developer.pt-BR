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
ms.openlocfilehash: 10311cf26b66e824447461530f1ce0870ea01ceb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652463"
---
# <span data-ttu-id="557cd-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="557cd-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="557cd-105">Args de evento para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="557cd-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="557cd-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="557cd-106">Summary</span></span>

 <span data-ttu-id="557cd-107">Parte</span><span class="sxs-lookup"><span data-stu-id="557cd-107">Members</span></span>                        | <span data-ttu-id="557cd-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="557cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="557cd-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="557cd-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="557cd-110">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="557cd-110">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="557cd-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="557cd-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="557cd-112">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="557cd-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="557cd-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="557cd-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="557cd-114">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="557cd-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="557cd-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="557cd-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="557cd-116">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="557cd-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="557cd-117">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="557cd-117">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="557cd-118">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="557cd-118">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="557cd-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="557cd-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="557cd-120">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="557cd-120">Sets the Handled property.</span></span>

## <span data-ttu-id="557cd-121">Parte</span><span class="sxs-lookup"><span data-stu-id="557cd-121">Members</span></span>

#### <span data-ttu-id="557cd-122">get_Handled</span><span class="sxs-lookup"><span data-stu-id="557cd-122">get_Handled</span></span> 

<span data-ttu-id="557cd-123">Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.</span><span class="sxs-lookup"><span data-stu-id="557cd-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="557cd-124">[get_Handled](#get_handled)público HRESULT (bool \* manipulado)</span><span class="sxs-lookup"><span data-stu-id="557cd-124">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="557cd-125">Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora.</span><span class="sxs-lookup"><span data-stu-id="557cd-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="557cd-126">Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="557cd-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="557cd-127">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="557cd-127">get_KeyEventKind</span></span> 

<span data-ttu-id="557cd-128">O tipo de evento Key que causou o evento a ser disparado.</span><span class="sxs-lookup"><span data-stu-id="557cd-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="557cd-129">público HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="557cd-129">public HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="557cd-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="557cd-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="557cd-131">O valor de LPARAM que acompanha a mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="557cd-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="557cd-132">público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="557cd-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="557cd-133">Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="557cd-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="557cd-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="557cd-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="557cd-135">Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="557cd-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="557cd-136">público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="557cd-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="557cd-137">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="557cd-137">get_VirtualKey</span></span> 

<span data-ttu-id="557cd-138">O código da chave virtual Win32 da chave que foi pressionada ou liberada.</span><span class="sxs-lookup"><span data-stu-id="557cd-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="557cd-139">público HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="557cd-139">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="557cd-140">Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '.</span><span class="sxs-lookup"><span data-stu-id="557cd-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="557cd-141">Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="557cd-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="557cd-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="557cd-142">put_Handled</span></span> 

<span data-ttu-id="557cd-143">Define a propriedade Handled.</span><span class="sxs-lookup"><span data-stu-id="557cd-143">Sets the Handled property.</span></span>

> <span data-ttu-id="557cd-144">[put_Handled](#put_handled)público HRESULT (bool manipulado)</span><span class="sxs-lookup"><span data-stu-id="557cd-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

