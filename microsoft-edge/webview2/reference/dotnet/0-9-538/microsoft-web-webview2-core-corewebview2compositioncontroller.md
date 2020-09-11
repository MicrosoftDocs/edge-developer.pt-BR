---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2CompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2CompositionController
ms.openlocfilehash: 8dccf532bed55d91a1b9f4d1edb2831fc07d0f82
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011094"
---
# <span data-ttu-id="f96dd-104">classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2CompositionController</span><span class="sxs-lookup"><span data-stu-id="f96dd-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2CompositionController class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="f96dd-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f96dd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f96dd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f96dd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f96dd-107">Essa classe é uma extensão da classe CoreWebView2Controller para dar suporte à hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="f96dd-107">This class is an extension of the CoreWebView2Controller class to support visual hosting.</span></span>

## <span data-ttu-id="f96dd-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f96dd-108">Summary</span></span>

 <span data-ttu-id="f96dd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f96dd-109">Members</span></span>                        | <span data-ttu-id="f96dd-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f96dd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f96dd-111">Cursor</span><span class="sxs-lookup"><span data-stu-id="f96dd-111">Cursor</span></span>](#cursor) | <span data-ttu-id="f96dd-112">O cursor atual que o WebView imagina que deveria estar.</span><span class="sxs-lookup"><span data-stu-id="f96dd-112">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="f96dd-113">CursorChanged</span><span class="sxs-lookup"><span data-stu-id="f96dd-113">CursorChanged</span></span>](#cursorchanged) | <span data-ttu-id="f96dd-114">O evento é acionado quando o WebView pensa que o cursor deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="f96dd-114">The event fires when WebView thinks the cursor should be changed.</span></span>
[<span data-ttu-id="f96dd-115">RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="f96dd-115">RootVisualTarget</span></span>](#rootvisualtarget) | <span data-ttu-id="f96dd-116">O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="f96dd-116">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="f96dd-117">UIAProvider</span><span class="sxs-lookup"><span data-stu-id="f96dd-117">UIAProvider</span></span>](#uiaprovider) | <span data-ttu-id="f96dd-118">Retorna o provedor de automação da interface do usuário da WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-118">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="f96dd-119">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="f96dd-119">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="f96dd-120">Uma função auxiliar para converter um ponteiroid recebido do sistema em um CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="f96dd-120">A helper function to convert a pointerId received from the system into a CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="f96dd-121">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="f96dd-121">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="f96dd-122">Se eventKind for CoreWebView2MouseEventKind. HorizontalWheel ou CoreWebView2MouseEventKind. wheel, mouseData especificará a quantidade de movimento da roda.</span><span class="sxs-lookup"><span data-stu-id="f96dd-122">If eventKind is CoreWebView2MouseEventKind.HorizontalWheel or CoreWebView2MouseEventKind.Wheel, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="f96dd-123">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="f96dd-123">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="f96dd-124">SendPointerInput aceita entrada de ponteiro de toque ou caneta de tipos definidos em CoreWebView2PointerEventKind.</span><span class="sxs-lookup"><span data-stu-id="f96dd-124">SendPointerInput accepts touch or pen pointer input of types defined in CoreWebView2PointerEventKind.</span></span>

## <span data-ttu-id="f96dd-125">Parte</span><span class="sxs-lookup"><span data-stu-id="f96dd-125">Members</span></span>

#### <span data-ttu-id="f96dd-126">Cursor</span><span class="sxs-lookup"><span data-stu-id="f96dd-126">Cursor</span></span> 

<span data-ttu-id="f96dd-127">O cursor atual que o WebView imagina que deveria estar.</span><span class="sxs-lookup"><span data-stu-id="f96dd-127">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="f96dd-128">[cursor](#cursor) de IntPtr público</span><span class="sxs-lookup"><span data-stu-id="f96dd-128">public IntPtr [Cursor](#cursor)</span></span>

<span data-ttu-id="f96dd-129">O cursor deve ser definido no WM_SETCURSOR pelo mouse. SetCursor ou definido no HWND pai/ancestral correspondente da WebView a SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="f96dd-129">The cursor should be set in WM_SETCURSOR through Mouse.SetCursor or set on the corresponding parent/ancestor HWND of the WebView through SetClassLongPtr.</span></span> <span data-ttu-id="f96dd-130">O HCURSOR pode ser liberado para que CopyCursor/DestroyCursor seja recomendado para manter sua própria cópia se você estiver fazendo mais do que configurar imediatamente o cursor.</span><span class="sxs-lookup"><span data-stu-id="f96dd-130">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="f96dd-131">CursorChanged</span><span class="sxs-lookup"><span data-stu-id="f96dd-131">CursorChanged</span></span> 

<span data-ttu-id="f96dd-132">O evento é acionado quando o WebView pensa que o cursor deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="f96dd-132">The event fires when WebView thinks the cursor should be changed.</span></span>

> <span data-ttu-id="f96dd-133">objeto<-EventHandler de evento público > [CursorChanged](#cursorchanged)</span><span class="sxs-lookup"><span data-stu-id="f96dd-133">public event EventHandler< object > [CursorChanged](#cursorchanged)</span></span>

<span data-ttu-id="f96dd-134">Por exemplo, quando o cursor do mouse é o cursor padrão no momento, mas é movido sobre o texto, ele pode tentar mudar para o cursor IBeam.</span><span class="sxs-lookup"><span data-stu-id="f96dd-134">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

#### <span data-ttu-id="f96dd-135">RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="f96dd-135">RootVisualTarget</span></span> 

<span data-ttu-id="f96dd-136">O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="f96dd-136">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="f96dd-137">[RootVisualTarget](#rootvisualtarget) de objeto público</span><span class="sxs-lookup"><span data-stu-id="f96dd-137">public object [RootVisualTarget](#rootvisualtarget)</span></span>

<span data-ttu-id="f96dd-138">Esse visual é onde o WebView irá conectar sua árvore visual.</span><span class="sxs-lookup"><span data-stu-id="f96dd-138">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="f96dd-139">O aplicativo usa esse visual para posicionar a WebView dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f96dd-139">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="f96dd-140">O aplicativo ainda precisa usar a propriedade Bounds para dimensionar o WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-140">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="f96dd-141">A propriedade RootVisualTarget pode ser uma IDCompositionVisual ou uma Windows:: UI:: composição:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="f96dd-141">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="f96dd-142">O WebView irá conectar sua árvore visual ao Visual fornecido antes de retornar do setter da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f96dd-142">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="f96dd-143">O aplicativo precisa confirmar seu dispositivo definindo a propriedade RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="f96dd-143">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="f96dd-144">A propriedade RootVisualTarget dá suporte a ser definida como nullptr para desconectar o WebView da árvore visual do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f96dd-144">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span>

#### <span data-ttu-id="f96dd-145">UIAProvider</span><span class="sxs-lookup"><span data-stu-id="f96dd-145">UIAProvider</span></span> 

<span data-ttu-id="f96dd-146">Retorna o provedor de automação da interface do usuário da WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-146">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="f96dd-147">[UIAProvider](#uiaprovider) de objeto público</span><span class="sxs-lookup"><span data-stu-id="f96dd-147">public object [UIAProvider](#uiaprovider)</span></span>

#### <span data-ttu-id="f96dd-148">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="f96dd-148">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="f96dd-149">Uma função auxiliar para converter um ponteiroid recebido do sistema em um CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="f96dd-149">A helper function to convert a pointerId received from the system into a CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="f96dd-150">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(Ponteiroid uint, IntPtr ParentWindow, Matrix4x4 Transform)</span><span class="sxs-lookup"><span data-stu-id="f96dd-150">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint PointerId, IntPtr ParentWindow, Matrix4x4 transform)</span></span>

<span data-ttu-id="f96dd-151">parentWindow é o HWND que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-151">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="f96dd-152">Isso pode ser qualquer HWND na árvore HWND que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-152">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="f96dd-153">O CoreWebView2Matrix4x4 é a transformação desse HWND para o WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-153">The CoreWebView2Matrix4x4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="f96dd-154">O CoreWebView2PointerInfo retornado é usado no SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="f96dd-154">The returned CoreWebView2PointerInfo is used in SendPointerInfo.</span></span> <span data-ttu-id="f96dd-155">O tipo de ponteiro deve ser Pen ou touch, ou a função falhará.</span><span class="sxs-lookup"><span data-stu-id="f96dd-155">The pointer type must be either pen or touch or the function will fail.</span></span>

#### <span data-ttu-id="f96dd-156">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="f96dd-156">SendMouseInput</span></span> 

<span data-ttu-id="f96dd-157">Se eventKind for CoreWebView2MouseEventKind. HorizontalWheel ou CoreWebView2MouseEventKind. wheel, mouseData especificará a quantidade de movimento da roda.</span><span class="sxs-lookup"><span data-stu-id="f96dd-157">If eventKind is CoreWebView2MouseEventKind.HorizontalWheel or CoreWebView2MouseEventKind.Wheel, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="f96dd-158">public void [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind, [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) virtualKeys, uint mouseData, Point Point)</span><span class="sxs-lookup"><span data-stu-id="f96dd-158">public void [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind, [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) virtualKeys, uint mouseData, Point point)</span></span>

<span data-ttu-id="f96dd-159">Um valor positivo indica que a roda foi girada para frente, longe do usuário; um valor negativo indica que a roda foi girada para trás, em direção ao usuário.</span><span class="sxs-lookup"><span data-stu-id="f96dd-159">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="f96dd-160">Um clique em roda é definido como WHEEL_DELTA, que é 120.</span><span class="sxs-lookup"><span data-stu-id="f96dd-160">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="f96dd-161">Se eventKind for CoreWebView2MouseEventKind. XButtonDoubleClick CoreWebView2MouseEventKind. XButtonDown ou CoreWebView2MouseEventKind. XButtonUp, mouseData especificará quais botões X foram pressionados ou liberados.</span><span class="sxs-lookup"><span data-stu-id="f96dd-161">If eventKind is CoreWebView2MouseEventKind.XButtonDoubleClick CoreWebView2MouseEventKind.XButtonDown, or CoreWebView2MouseEventKind.XButtonUp, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="f96dd-162">Esse valor deve ser 1 se o primeiro botão X for pressionado/liberado e 2 se o segundo botão X for pressionado/liberado.</span><span class="sxs-lookup"><span data-stu-id="f96dd-162">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="f96dd-163">Se eventKind for CoreWebView2MouseEventKind. leave, virtualKeys, mouseData e Point deverão ser zero.</span><span class="sxs-lookup"><span data-stu-id="f96dd-163">If eventKind is CoreWebView2MouseEventKind.Leave, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="f96dd-164">Se eventKind for qualquer outro valor, então mouseData deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f96dd-164">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="f96dd-165">O ponto deve estar no espaço de coordenadas do cliente da WebView.</span><span class="sxs-lookup"><span data-stu-id="f96dd-165">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="f96dd-166">Para acompanhar eventos do mouse que começam na WebView e podem ser movidos para fora do WebView e do aplicativo host, é recomendável chamar SetCapture e ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="f96dd-166">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="f96dd-167">Para descartar pop-ups de foco, também é recomendável enviar mensagens de WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="f96dd-167">To dismiss hover popups, it is also recommended to send WM_MOUSELEAVE messages.</span></span>

#### <span data-ttu-id="f96dd-168">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="f96dd-168">SendPointerInput</span></span> 

<span data-ttu-id="f96dd-169">SendPointerInput aceita entrada de ponteiro de toque ou caneta de tipos definidos em CoreWebView2PointerEventKind.</span><span class="sxs-lookup"><span data-stu-id="f96dd-169">SendPointerInput accepts touch or pen pointer input of types defined in CoreWebView2PointerEventKind.</span></span>

> <span data-ttu-id="f96dd-170">public void [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) EventType, [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="f96dd-170">public void [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) eventType, [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)</span></span>

<span data-ttu-id="f96dd-171">Qualquer entrada de ponteiro do sistema deve ser convertida em um CoreWebView2PointerInfo primeiro.</span><span class="sxs-lookup"><span data-stu-id="f96dd-171">Any pointer input from the system must be converted into a CoreWebView2PointerInfo first.</span></span>

