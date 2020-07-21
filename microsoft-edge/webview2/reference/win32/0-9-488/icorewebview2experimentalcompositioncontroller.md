---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: ddb3fce4f3f9799bcfaf8a9aa297c3207392f916
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884537"
---
# <span data-ttu-id="7f985-104">0.9.515-ICoreWebView2ExperimentalCompositionController de interface</span><span class="sxs-lookup"><span data-stu-id="7f985-104">0.9.515 - interface ICoreWebView2ExperimentalCompositionController</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="7f985-105">Essa interface é uma extensão da interface ICoreWebView2Controller para dar suporte à hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="7f985-105">This interface is an extension of the ICoreWebView2Controller interface to support visual hosting.</span></span>

## <span data-ttu-id="7f985-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7f985-106">Summary</span></span>

 <span data-ttu-id="7f985-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7f985-107">Members</span></span>                        | <span data-ttu-id="7f985-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7f985-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f985-109">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="7f985-109">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="7f985-110">Adicione um manipulador de eventos para o evento CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f985-110">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="7f985-111">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="7f985-111">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="7f985-112">Uma função auxiliar para converter um ponteiroid recebido do sistema em um [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="7f985-112">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="7f985-113">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="7f985-113">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="7f985-114">O cursor atual que o WebView imagina que deveria estar.</span><span class="sxs-lookup"><span data-stu-id="7f985-114">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="7f985-115">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="7f985-115">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="7f985-116">O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="7f985-116">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="7f985-117">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="7f985-117">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="7f985-118">Retorna o provedor de automação da interface do usuário da WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-118">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="7f985-119">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="7f985-119">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="7f985-120">Defina a propriedade RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="7f985-120">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="7f985-121">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="7f985-121">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="7f985-122">Remover um manipulador de eventos adicionado anteriormente com add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f985-122">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="7f985-123">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="7f985-123">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="7f985-124">Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especificará a quantidade de movimento da roda.</span><span class="sxs-lookup"><span data-stu-id="7f985-124">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="7f985-125">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="7f985-125">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="7f985-126">O SendPointerInput aceita entrada de toque ou ponteiro de caneta de tipos definidos em COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="7f985-126">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="7f985-127">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="7f985-127">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="7f985-128">Matriz que representa uma transformação 3D.</span><span class="sxs-lookup"><span data-stu-id="7f985-128">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="7f985-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="7f985-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="7f985-130">Tipo de evento de mouse usado pelo SendMouseInput para transmitir o tipo de evento de mouse sendo enviado ao WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-130">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="7f985-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="7f985-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="7f985-132">Teclas virtuais de evento de mouse associadas a um COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="7f985-132">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="7f985-133">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="7f985-133">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="7f985-134">Tipo de evento ponteiro usado pelo SendPointerInput para transmitir o tipo de evento ponteiro sendo enviado ao WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-134">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="7f985-135">Um objeto que implementa a interface ICoreWebView2ExperimentalCompositionController também implementa ICoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7f985-135">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement ICoreWebView2Controller.</span></span> <span data-ttu-id="7f985-136">Espera-se que os chamadores usem ICoreWebView2Controller para redimensionar, visibilidade, foco e assim por diante e, em seguida, usar o ICoreWebView2ExperimentalCompositionController para se conectar a uma árvore de composição e fornecer a entrada para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-136">Callers are expected to use ICoreWebView2Controller for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="7f985-137">Parte</span><span class="sxs-lookup"><span data-stu-id="7f985-137">Members</span></span>

#### <span data-ttu-id="7f985-138">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="7f985-138">add_CursorChanged</span></span> 

<span data-ttu-id="7f985-139">Adicione um manipulador de eventos para o evento CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f985-139">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="7f985-140">Public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7f985-140">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7f985-141">O evento é acionado quando o WebView pensa que o cursor deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="7f985-141">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="7f985-142">Por exemplo, quando o cursor do mouse é o cursor padrão no momento, mas é movido sobre o texto, ele pode tentar mudar para o cursor IBeam.</span><span class="sxs-lookup"><span data-stu-id="7f985-142">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### <span data-ttu-id="7f985-143">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="7f985-143">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="7f985-144">Uma função auxiliar para converter um ponteiroid recebido do sistema em um [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="7f985-144">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="7f985-145">Public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(ponteiroid uint, HWND ParentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="7f985-145">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="7f985-146">parentWindow é o HWND que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-146">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="7f985-147">Isso pode ser qualquer HWND na árvore HWND que contém o WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-147">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="7f985-148">O COREWEBVIEW2_MATRIX_4X4 é a transformação daquele HWND para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-148">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="7f985-149">O [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) retornado é usado no SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="7f985-149">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="7f985-150">O tipo de ponteiro deve ser Pen ou touch, ou a função falhará.</span><span class="sxs-lookup"><span data-stu-id="7f985-150">The pointer type must be either pen or touch or the function will fail.</span></span>



#### <span data-ttu-id="7f985-151">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="7f985-151">get_Cursor</span></span> 

<span data-ttu-id="7f985-152">O cursor atual que o WebView imagina que deveria estar.</span><span class="sxs-lookup"><span data-stu-id="7f985-152">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="7f985-153">público HRESULT [get_Cursor](#get_cursor)(hCursor \* cursor)</span><span class="sxs-lookup"><span data-stu-id="7f985-153">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="7f985-154">O cursor deve ser definido em WM_SETCURSOR por meio de:: SetCursor ou definido no HWND pai/ancestral correspondente da WebView a:: SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="7f985-154">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="7f985-155">O HCURSOR pode ser liberado para que CopyCursor/DestroyCursor seja recomendado para manter sua própria cópia se você estiver fazendo mais do que configurar imediatamente o cursor.</span><span class="sxs-lookup"><span data-stu-id="7f985-155">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="7f985-156">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="7f985-156">get_RootVisualTarget</span></span> 

<span data-ttu-id="7f985-157">O RootVisualTarget é um Visual na árvore visual do aplicativo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="7f985-157">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="7f985-158">público HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \* \* destino)</span><span class="sxs-lookup"><span data-stu-id="7f985-158">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="7f985-159">Esse visual é onde o WebView irá conectar sua árvore visual.</span><span class="sxs-lookup"><span data-stu-id="7f985-159">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="7f985-160">O aplicativo usa esse visual para posicionar a WebView dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f985-160">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="7f985-161">O aplicativo ainda precisa usar a propriedade Bounds para dimensionar o WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-161">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="7f985-162">A propriedade RootVisualTarget pode ser uma IDCompositionVisual ou uma Windows:: UI:: composição:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="7f985-162">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="7f985-163">O WebView irá conectar sua árvore visual ao Visual fornecido antes de retornar do setter da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7f985-163">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="7f985-164">O aplicativo precisa confirmar seu dispositivo definindo a propriedade RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="7f985-164">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="7f985-165">A propriedade RootVisualTarget dá suporte a ser definida como nullptr para desconectar o WebView da árvore visual do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f985-165">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### <span data-ttu-id="7f985-166">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="7f985-166">get_UIAProvider</span></span> 

<span data-ttu-id="7f985-167">Retorna o provedor de automação da interface do usuário da WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-167">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="7f985-168">público HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \* \* provedor)</span><span class="sxs-lookup"><span data-stu-id="7f985-168">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="7f985-169">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="7f985-169">put_RootVisualTarget</span></span> 

<span data-ttu-id="7f985-170">Defina a propriedade RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="7f985-170">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="7f985-171">público HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* destino)</span><span class="sxs-lookup"><span data-stu-id="7f985-171">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="7f985-172">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="7f985-172">remove_CursorChanged</span></span> 

<span data-ttu-id="7f985-173">Remover um manipulador de eventos adicionado anteriormente com add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f985-173">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="7f985-174">[remove_CursorChanged](#remove_cursorchanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7f985-174">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7f985-175">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="7f985-175">SendMouseInput</span></span> 

<span data-ttu-id="7f985-176">Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especificará a quantidade de movimento da roda.</span><span class="sxs-lookup"><span data-stu-id="7f985-176">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="7f985-177">Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, Point Point)</span><span class="sxs-lookup"><span data-stu-id="7f985-177">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="7f985-178">Um valor positivo indica que a roda foi girada para frente, longe do usuário; um valor negativo indica que a roda foi girada para trás, em direção ao usuário.</span><span class="sxs-lookup"><span data-stu-id="7f985-178">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="7f985-179">Um clique em roda é definido como WHEEL_DELTA, que é 120.</span><span class="sxs-lookup"><span data-stu-id="7f985-179">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="7f985-180">Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN ou COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, então mouseData especificará quais botões X foram pressionados ou liberados.</span><span class="sxs-lookup"><span data-stu-id="7f985-180">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="7f985-181">Esse valor deve ser 1 se o primeiro botão X for pressionado/liberado e 2 se o segundo botão X for pressionado/liberado.</span><span class="sxs-lookup"><span data-stu-id="7f985-181">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="7f985-182">Se eventKind for COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData e Point deverão ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f985-182">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="7f985-183">Se eventKind for qualquer outro valor, então mouseData deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f985-183">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="7f985-184">O ponto deve estar no espaço de coordenadas do cliente da WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-184">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="7f985-185">Para acompanhar eventos do mouse que começam na WebView e podem ser movidos para fora do WebView e do aplicativo host, é recomendável chamar SetCapture e ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="7f985-185">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="7f985-186">Para descartar pop-ups de foco, também é recomendável enviar mensagens de WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="7f985-186">To dismiss hover popups, it is also recommended to send WM_MOUSELEAVE messages.</span></span> 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### <span data-ttu-id="7f985-187">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="7f985-187">SendPointerInput</span></span> 

<span data-ttu-id="7f985-188">O SendPointerInput aceita entrada de toque ou ponteiro de caneta de tipos definidos em COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="7f985-188">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="7f985-189">Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="7f985-189">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="7f985-190">Qualquer entrada de ponteiro do sistema deve ser convertida em um [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) primeiro.</span><span class="sxs-lookup"><span data-stu-id="7f985-190">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="7f985-191">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="7f985-191">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="7f985-192">Matriz que representa uma transformação 3D.</span><span class="sxs-lookup"><span data-stu-id="7f985-192">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="7f985-193">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="7f985-193">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="7f985-194">Essa transformação é usada para calcular as coordenadas corretas ao chamar CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="7f985-194">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="7f985-195">Isso equivale a um D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="7f985-195">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="7f985-196">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="7f985-196">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="7f985-197">Tipo de evento de mouse usado pelo SendMouseInput para transmitir o tipo de evento de mouse sendo enviado ao WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-197">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="7f985-198">Enumeração [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span><span class="sxs-lookup"><span data-stu-id="7f985-198">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="7f985-199">Valores</span><span class="sxs-lookup"><span data-stu-id="7f985-199">Values</span></span>                         | <span data-ttu-id="7f985-200">Descrições</span><span class="sxs-lookup"><span data-stu-id="7f985-200">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="7f985-201">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="7f985-201">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="7f985-202">Evento de rolagem da roda horizontal do mouse, WM_MOUSEHWHEEL.</span><span class="sxs-lookup"><span data-stu-id="7f985-202">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="7f985-203">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="7f985-203">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="7f985-204">Botão esquerdo do mouse de clique duplo, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="7f985-204">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="7f985-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="7f985-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="7f985-206">Botão esquerdo do mouse, evento WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="7f985-206">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="7f985-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="7f985-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="7f985-208">Botão esquerdo evento do mouse, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="7f985-208">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="7f985-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="7f985-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="7f985-210">Evento Leave do mouse, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="7f985-210">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="7f985-211">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="7f985-211">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="7f985-212">Botão do meio clique duas vezes em evento de mouse WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="7f985-212">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="7f985-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="7f985-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="7f985-214">Botão do meio evento do mouse, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="7f985-214">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="7f985-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="7f985-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="7f985-216">Botão médio do evento do mouse, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="7f985-216">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="7f985-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="7f985-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="7f985-218">Evento de movimentação do mouse, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="7f985-218">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="7f985-219">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="7f985-219">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="7f985-220">Botão direito do mouse clique duas vezes em evento do mouse WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="7f985-220">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="7f985-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="7f985-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="7f985-222">Botão direito do mouse sobre o evento WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="7f985-222">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="7f985-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="7f985-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="7f985-224">Botão direito do mouse sobre o evento WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="7f985-224">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="7f985-225">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="7f985-225">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="7f985-226">Evento de rolagem da roda do mouse, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="7f985-226">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="7f985-227">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="7f985-227">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="7f985-228">Primeiro ou segundo botão X clique duas vezes em evento do mouse WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="7f985-228">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="7f985-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="7f985-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="7f985-230">Botão do mouse sobre o botão primeiro ou segundo X desligado WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="7f985-230">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="7f985-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="7f985-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="7f985-232">O evento de mouse do primeiro ou segundo botão X para cima WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="7f985-232">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="7f985-233">Os valores desse enum são alinhados com as mensagens WM_ \* da janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="7f985-233">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="7f985-234">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="7f985-234">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="7f985-235">Teclas virtuais de evento de mouse associadas a um COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="7f985-235">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="7f985-236">Enumeração [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span><span class="sxs-lookup"><span data-stu-id="7f985-236">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="7f985-237">Valores</span><span class="sxs-lookup"><span data-stu-id="7f985-237">Values</span></span>                         | <span data-ttu-id="7f985-238">Descrições</span><span class="sxs-lookup"><span data-stu-id="7f985-238">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="7f985-239">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="7f985-239">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="7f985-240">Nenhuma tecla adicional pressionada.</span><span class="sxs-lookup"><span data-stu-id="7f985-240">No additional keys pressed.</span></span>
<span data-ttu-id="7f985-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="7f985-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="7f985-242">O botão esquerdo do mouse está abaixo MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="7f985-242">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="7f985-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="7f985-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="7f985-244">O botão direito do mouse está abaixo MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="7f985-244">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="7f985-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="7f985-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="7f985-246">A tecla SHIFT está inativa, MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="7f985-246">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="7f985-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="7f985-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="7f985-248">A tecla CTRL está inoperante, MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="7f985-248">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="7f985-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="7f985-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="7f985-250">O botão do meio do mouse está baixo, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="7f985-250">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="7f985-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="7f985-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="7f985-252">O primeiro botão X está baixo, MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="7f985-252">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="7f985-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="7f985-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="7f985-254">O segundo botão X está baixo, MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="7f985-254">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="7f985-255">Esses valores podem ser combinados em um sinalizador de bit se mais de uma chave virtual for pressionada para o evento.</span><span class="sxs-lookup"><span data-stu-id="7f985-255">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="7f985-256">Os valores dessa enumeração se alinham com as teclas de mouse MK_ \* correspondentes.</span><span class="sxs-lookup"><span data-stu-id="7f985-256">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="7f985-257">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="7f985-257">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="7f985-258">Tipo de evento ponteiro usado pelo SendPointerInput para transmitir o tipo de evento ponteiro sendo enviado ao WebView.</span><span class="sxs-lookup"><span data-stu-id="7f985-258">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="7f985-259">Enumeração [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span><span class="sxs-lookup"><span data-stu-id="7f985-259">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="7f985-260">Valores</span><span class="sxs-lookup"><span data-stu-id="7f985-260">Values</span></span>                         | <span data-ttu-id="7f985-261">Descrições</span><span class="sxs-lookup"><span data-stu-id="7f985-261">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="7f985-262">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="7f985-262">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="7f985-263">Corresponde a WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="7f985-263">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="7f985-264">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="7f985-264">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="7f985-265">Corresponde a WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="7f985-265">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="7f985-266">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="7f985-266">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="7f985-267">Corresponde a WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="7f985-267">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="7f985-268">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="7f985-268">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="7f985-269">Corresponde a WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="7f985-269">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="7f985-270">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="7f985-270">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="7f985-271">Corresponde a WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="7f985-271">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="7f985-272">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7f985-272">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="7f985-273">Corresponde a WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="7f985-273">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="7f985-274">Os valores desse enum são alinhados com as mensagens WM_POINTER \* da janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="7f985-274">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

