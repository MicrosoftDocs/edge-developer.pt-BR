---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 02128001f208f15d4e33c1f3f2cef6c8d662d357
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652629"
---
# <span data-ttu-id="7ffaa-104">interface ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="7ffaa-104">interface ICoreWebView2Controller</span></span> 

```
interface ICoreWebView2Controller
  : public IUnknown
```

<span data-ttu-id="7ffaa-105">Essa interface é o proprietário do objeto CoreWebView2 e fornece suporte para redimensionar, mostrar e ocultar, enfocar e outras funcionalidades relacionadas à janela e composição.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-105">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="7ffaa-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7ffaa-106">Summary</span></span>

 <span data-ttu-id="7ffaa-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7ffaa-107">Members</span></span>                        | <span data-ttu-id="7ffaa-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7ffaa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7ffaa-109">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7ffaa-109">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="7ffaa-110">Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-110">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="7ffaa-111">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-111">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="7ffaa-112">Adicione um manipulador de eventos para o evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-112">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="7ffaa-113">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-113">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="7ffaa-114">Adicione um manipulador de eventos para o evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-114">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="7ffaa-115">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7ffaa-115">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="7ffaa-116">Adicione um manipulador de eventos para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-116">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="7ffaa-117">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7ffaa-117">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="7ffaa-118">Adicione um manipulador de eventos para o evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-118">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="7ffaa-119">Fechar</span><span class="sxs-lookup"><span data-stu-id="7ffaa-119">Close</span></span>](#close) | <span data-ttu-id="7ffaa-120">Fecha a WebView e limpa a instância do navegador subjacente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-120">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="7ffaa-121">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="7ffaa-121">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="7ffaa-122">Os limites da WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-122">The webview bounds.</span></span>
[<span data-ttu-id="7ffaa-123">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7ffaa-123">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="7ffaa-124">Obtém a CoreWebView2 associada a este CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-124">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="7ffaa-125">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7ffaa-125">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="7ffaa-126">A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-126">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="7ffaa-127">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7ffaa-127">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="7ffaa-128">A janela pai fornecida pelo aplicativo que este WebView usa para renderizar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-128">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="7ffaa-129">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7ffaa-129">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="7ffaa-130">O fator de zoom para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-130">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="7ffaa-131">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-131">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="7ffaa-132">Mover o foco para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-132">Move focus into WebView.</span></span>
[<span data-ttu-id="7ffaa-133">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="7ffaa-133">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="7ffaa-134">Esta é uma notificação separada dos limites que dizem ao WebView que o HWND pai (ou qualquer ancestral) moveu.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-134">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="7ffaa-135">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="7ffaa-135">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="7ffaa-136">Defina a propriedade Bounds.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-136">Set the Bounds property.</span></span>
[<span data-ttu-id="7ffaa-137">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7ffaa-137">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="7ffaa-138">Defina a propriedade IsVisible.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-138">Set the IsVisible property.</span></span>
[<span data-ttu-id="7ffaa-139">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7ffaa-139">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="7ffaa-140">Defina a janela pai para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-140">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="7ffaa-141">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7ffaa-141">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="7ffaa-142">Defina a propriedade ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-142">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="7ffaa-143">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7ffaa-143">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="7ffaa-144">Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-144">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="7ffaa-145">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-145">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="7ffaa-146">Remover um manipulador de eventos adicionado anteriormente com add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-146">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="7ffaa-147">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-147">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="7ffaa-148">Remover um manipulador de eventos adicionado anteriormente com add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-148">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="7ffaa-149">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7ffaa-149">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="7ffaa-150">Remover um manipulador de eventos adicionado anteriormente com add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-150">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="7ffaa-151">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7ffaa-151">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="7ffaa-152">Remover um manipulador de eventos adicionado anteriormente com add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-152">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="7ffaa-153">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7ffaa-153">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="7ffaa-154">Atualize as propriedades Bounds e ZoomFactor ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-154">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="7ffaa-155">O CoreWebView2Controller é proprietário do CoreWebView2 e, se todas as referências à CoreWebView2Controller ficarem ausentes, o WebView será fechado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-155">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="7ffaa-156">Parte</span><span class="sxs-lookup"><span data-stu-id="7ffaa-156">Members</span></span>

#### <span data-ttu-id="7ffaa-157">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7ffaa-157">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="7ffaa-158">Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-158">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="7ffaa-159">Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-159">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7ffaa-160">AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-160">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="7ffaa-161">Uma tecla é considerada um acelerador se:</span><span class="sxs-lookup"><span data-stu-id="7ffaa-161">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="7ffaa-162">A tecla CTRL ou Alt está sendo mantida no momento ou</span><span class="sxs-lookup"><span data-stu-id="7ffaa-162">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="7ffaa-163">a tecla pressionada não é mapeada para um caractere.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-163">the pressed key does not map to a character.</span></span> <span data-ttu-id="7ffaa-164">Algumas teclas específicas nunca são consideradas aceleradores, como Shift.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-164">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="7ffaa-165">A tecla escape é sempre considerada um acelerador.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-165">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="7ffaa-166">Os eventos chave repetido com repetição causada pela manutenção da tecla para baixo também acionarão esse evento.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-166">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="7ffaa-167">Você pode filtrá-los verificando os argumentos do evento KeyEventLParam ou PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-167">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="7ffaa-168">No modo de janela, esse manipulador de eventos é chamado sincronicamente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-168">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="7ffaa-169">Até que você chame Handle () nos argumentos do evento ou o manipulador de eventos seja retornado, o processo do navegador será bloqueado e as chamadas COM saída cruzada de processo não funcionarão com RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-169">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="7ffaa-170">No entanto, todos os métodos de API CoreWebView2 funcionarão.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-170">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="7ffaa-171">No modo sem janela, o manipulador de eventos é chamado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-171">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="7ffaa-172">A entrada adicional não entrará em contato com o navegador até que o manipulador de eventos retorne ou manipule () seja chamado, mas o processo do navegador em si não será bloqueado, e as chamadas COM de saída funcionarão normalmente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-172">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="7ffaa-173">É recomendável chamar Handle (TRUE), como o mais cedo possível, se souber que deseja manipular a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-173">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="7ffaa-174">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-174">add_GotFocus</span></span> 

<span data-ttu-id="7ffaa-175">Adicione um manipulador de eventos para o evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-175">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="7ffaa-176">Public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-176">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7ffaa-177">GotFocus é acionado quando o WebView tem foco.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-177">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="7ffaa-178">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-178">add_LostFocus</span></span> 

<span data-ttu-id="7ffaa-179">Adicione um manipulador de eventos para o evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-179">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="7ffaa-180">Public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-180">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7ffaa-181">LostFocus é acionado quando o WebView perdeu o foco.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-181">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="7ffaa-182">No caso em que o evento MoveFocusRequested é acionado, o foco continua no WebView quando o evento MoveFocusRequested é acionado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-182">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="7ffaa-183">O foco perdido só será acionado depois que o código do aplicativo ou a ação padrão do conjunto de eventos MoveFocusRequested se concentrar em uma exibição de exibição ausente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-183">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="7ffaa-184">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7ffaa-184">add_MoveFocusRequested</span></span> 

<span data-ttu-id="7ffaa-185">Adicione um manipulador de eventos para o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-185">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="7ffaa-186">Public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-186">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7ffaa-187">MoveFocusRequested é acionado quando o usuário tenta Tab no WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-187">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="7ffaa-188">O foco da WebView não mudou quando esse evento é acionado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-188">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="7ffaa-189">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7ffaa-189">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="7ffaa-190">Adicione um manipulador de eventos para o evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-190">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="7ffaa-191">Public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-191">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7ffaa-192">O evento é acionado quando a propriedade ZoomFactor da WebView é alterada.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-192">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="7ffaa-193">O evento pode ser acionado porque o chamador modificou a propriedade ZoomFactor ou porque o usuário modificou manualmente o zoom.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-193">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="7ffaa-194">Quando ela é modificada pelo chamador por meio da propriedade ZoomFactor, o fator de zoom interno é atualizado imediatamente e não haverá um evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-194">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="7ffaa-195">O WebView associa o último fator de zoom usado para cada site.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-195">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="7ffaa-196">Portanto, é possível que o fator de zoom mude ao navegar para uma página diferente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-196">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="7ffaa-197">Quando o fator de zoom muda devido a isso, o evento ZoomFactorChanged é acionado logo após o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-197">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="7ffaa-198">Fechar</span><span class="sxs-lookup"><span data-stu-id="7ffaa-198">Close</span></span> 

<span data-ttu-id="7ffaa-199">Fecha a WebView e limpa a instância do navegador subjacente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-199">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="7ffaa-200">público HRESULT [fechar](#close)()</span><span class="sxs-lookup"><span data-stu-id="7ffaa-200">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="7ffaa-201">A limpeza da instância do navegador liberará os recursos que alimentam o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-201">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="7ffaa-202">A instância do navegador será encerrada se não houver outros webviews que o usam.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-202">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="7ffaa-203">Depois de chamar Close, todas as chamadas de método falharão e os manipuladores de eventos deixarão de ser acionados.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-203">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="7ffaa-204">Especificamente, a WebView liberará suas referências a seus manipuladores de eventos quando Close for chamado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-204">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="7ffaa-205">Fechar é chamado implicitamente quando o CoreWebView2Controller perde sua referência final e é destruido.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-205">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="7ffaa-206">Mas é uma prática recomendada chamar o fechamento explicitamente para evitar qualquer ciclo acidental de referências entre o WebView e o código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-206">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="7ffaa-207">Especificamente, se você capturar uma referência ao WebView em um manipulador de eventos, criará um ciclo de referência entre o WebView e o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-207">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="7ffaa-208">Chamar Close irá interromper esse ciclo liberando todos os manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-208">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="7ffaa-209">Mas para evitar essa situação, é recomendável que a chamada seja fechada explicitamente no WebView e não Capture uma referência para o WebView para garantir que o WebView possa ser limpo corretamente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-209">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="7ffaa-210">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="7ffaa-210">get_Bounds</span></span> 

<span data-ttu-id="7ffaa-211">Os limites da WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-211">The webview bounds.</span></span>

> <span data-ttu-id="7ffaa-212">Associação Pública HRESULT [get_Bounds](#get_bounds)(Rect \*)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-212">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="7ffaa-213">Os limites são relativos ao HWND pai.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-213">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="7ffaa-214">O aplicativo tem duas maneiras de posicionar um WebView:</span><span class="sxs-lookup"><span data-stu-id="7ffaa-214">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="7ffaa-215">Crie um HWND filho que seja o HWND pai do WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-215">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="7ffaa-216">Posicione esta janela onde o WebView deve estar.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-216">Position this window where the WebView should be.</span></span> <span data-ttu-id="7ffaa-217">Nesse caso, use (0, 0) para o canto superior esquerdo Bound's do WebView (o deslocamento).</span><span class="sxs-lookup"><span data-stu-id="7ffaa-217">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="7ffaa-218">Use a janela mais superior do aplicativo como o HWND pai do WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-218">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="7ffaa-219">Defina o Bound's canto superior esquerdo da WebView para que o WebView esteja posicionado corretamente no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-219">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="7ffaa-220">Os valores do limite estão no espaço de coordenadas do host.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-220">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="7ffaa-221">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7ffaa-221">get_CoreWebView2</span></span> 

<span data-ttu-id="7ffaa-222">Obtém a CoreWebView2 associada a este CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-222">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="7ffaa-223">Public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-223">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="7ffaa-224">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7ffaa-224">get_IsVisible</span></span> 

<span data-ttu-id="7ffaa-225">A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-225">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="7ffaa-226">[get_IsVisible](#get_isvisible)público HRESULT (bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-226">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="7ffaa-227">Se IsVisible estiver definido como false, o WebView será transparente e não será renderizado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-227">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="7ffaa-228">No entanto, isso não afetará a janela que contém o WebView (o parâmetro HWND que foi passado para CreateCoreWebView2Controller).</span><span class="sxs-lookup"><span data-stu-id="7ffaa-228">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="7ffaa-229">Se você quiser que essa janela desapareça também, chame o recurso de janela diretamente, além de modificar a propriedade IsVisible.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-229">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="7ffaa-230">A WebView como uma janela filho não obterá mensagens de janela quando a janela superior for minimizada ou restaurada.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-230">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="7ffaa-231">Por motivo de desempenho, o desenvolvedor deve definir a propriedade IsVisible do WebView como false quando a janela do aplicativo é minimizada e retomada como true quando a janela do aplicativo for restaurada.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-231">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="7ffaa-232">A janela do aplicativo pode fazer isso ao manipular SC_MINIMIZE e SC_RESTORE comando ao receber WM_SYSCOMMAND mensagem.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-232">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="7ffaa-233">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7ffaa-233">get_ParentWindow</span></span> 

<span data-ttu-id="7ffaa-234">A janela pai fornecida pelo aplicativo que este WebView usa para renderizar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-234">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="7ffaa-235">Public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-235">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="7ffaa-236">Esta API inicialmente retorna a janela passada para CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-236">This API initially returns the window passed into CreateCoreWebView2Controller.</span></span>

#### <span data-ttu-id="7ffaa-237">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7ffaa-237">get_ZoomFactor</span></span> 

<span data-ttu-id="7ffaa-238">O fator de zoom para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-238">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="7ffaa-239">público HRESULT [get_ZoomFactor](#get_zoomfactor)(duplo \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-239">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="7ffaa-240">Observe que a alteração do fator de zoom pode fazer com que o `window.innerWidth/innerHeight` layout da página seja alterado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-240">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="7ffaa-241">Um fator de zoom aplicado pelo host chamando ZoomFactor se torna o novo zoom padrão para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-241">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="7ffaa-242">Esse fator de zoom se aplica a navegações e é o fator de zoom que é retornado quando o usuário pressiona Ctrl + 0.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-242">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="7ffaa-243">Quando o fator de zoom é alterado pelo usuário (resultante do aplicativo que recebe ZoomFactorChanged), esse zoom se aplica apenas à página atual.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-243">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="7ffaa-244">O zoom aplicado pelo usuário é somente para a página atual e é redefinido em uma navegação.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-244">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="7ffaa-245">Não é permitido especificar um zoomFactor menor ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-245">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="7ffaa-246">WebView também tem um intervalo de fator de zoom interno com suporte.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-246">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="7ffaa-247">Quando um fator de zoom especificado estiver fora desse intervalo, ele será normalizado para estar dentro do intervalo, e um evento ZoomFactorChanged será acionado para o fator de zoom aplicado real.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-247">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="7ffaa-248">Quando essa faixa de normalização acontece, a propriedade ZoomFactor relata o fator de zoom especificado durante a modificação anterior da propriedade ZoomFactor até que o evento ZoomFactorChanged seja recebido após o WebView se aplicar o fator de zoom normalizado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-248">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="7ffaa-249">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-249">MoveFocus</span></span> 

<span data-ttu-id="7ffaa-250">Mover o foco para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-250">Move focus into WebView.</span></span>

> <span data-ttu-id="7ffaa-251">Public HRESULT [MoveFocus](#movefocus)(motivo COREWEBVIEW2_MOVE_FOCUS_REASON)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-251">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON reason)</span></span>

<span data-ttu-id="7ffaa-252">O WebView receberá o foco e o foco será definido como elemento correspondente na página hospedada na WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-252">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="7ffaa-253">Para motivo programático, o foco é definido como elemento prefoco anteriormente ou o elemento padrão se não houver nenhum elemento focalizado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-253">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="7ffaa-254">Para o próximo motivo, o foco é definido como o primeiro elemento.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-254">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="7ffaa-255">Para o motivo anterior, o foco é definido como o último elemento.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-255">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="7ffaa-256">A WebView também pode ter o foco por meio da interação do usuário, como clicar em um WebView ou Tab.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-256">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="7ffaa-257">Para tabulação, o aplicativo pode chamar MoveFocus com o próximo ou o anterior para alinhar-se com Tab e Shift + Tab, respectivamente, quando decide que o WebView é o próximo elemento que pode ser tabulado.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-257">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="7ffaa-258">Ou, o aplicativo pode chamar IsDialogMessage como parte de seu loop de mensagem para permitir que a plataforma manipule a Tabulação automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-258">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="7ffaa-259">A plataforma irá girar por todas as janelas com WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-259">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="7ffaa-260">Quando a WebView se concentrar no IsDialogMessage, o foco será inserido internamente no primeiro ou último elemento para Tab e Shift + Tab respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-260">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="7ffaa-261">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="7ffaa-261">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="7ffaa-262">Esta é uma notificação separada dos limites que dizem ao WebView que o HWND pai (ou qualquer ancestral) moveu.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-262">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="7ffaa-263">Public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="7ffaa-263">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="7ffaa-264">Isso é necessário para acessibilidade e determinadas caixas de diálogo no WebView para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-264">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="7ffaa-265">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="7ffaa-265">put_Bounds</span></span> 

<span data-ttu-id="7ffaa-266">Defina a propriedade Bounds.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-266">Set the Bounds property.</span></span>

> <span data-ttu-id="7ffaa-267">[put_Bounds](#put_bounds)público HRESULT (limites Rect)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-267">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### <span data-ttu-id="7ffaa-268">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7ffaa-268">put_IsVisible</span></span> 

<span data-ttu-id="7ffaa-269">Defina a propriedade IsVisible.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-269">Set the IsVisible property.</span></span>

> <span data-ttu-id="7ffaa-270">público HRESULT [put_IsVisible](#put_isvisible)(bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-270">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="7ffaa-271">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7ffaa-271">put_ParentWindow</span></span> 

<span data-ttu-id="7ffaa-272">Defina a janela pai para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-272">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="7ffaa-273">[put_ParentWindow](#put_parentwindow)público HRESULT (HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-273">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="7ffaa-274">Isso fará com que o WebView retenha o pai da janela para a janela recém fornecida.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-274">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="7ffaa-275">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7ffaa-275">put_ZoomFactor</span></span> 

<span data-ttu-id="7ffaa-276">Defina a propriedade ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-276">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="7ffaa-277">público HRESULT [put_ZoomFactor](#put_zoomfactor)(ZoomFactor duplo)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-277">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="7ffaa-278">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7ffaa-278">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="7ffaa-279">Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-279">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="7ffaa-280">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-280">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7ffaa-281">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-281">remove_GotFocus</span></span> 

<span data-ttu-id="7ffaa-282">Remover um manipulador de eventos adicionado anteriormente com add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-282">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="7ffaa-283">[remove_GotFocus](#remove_gotfocus)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-283">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7ffaa-284">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7ffaa-284">remove_LostFocus</span></span> 

<span data-ttu-id="7ffaa-285">Remover um manipulador de eventos adicionado anteriormente com add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-285">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="7ffaa-286">[remove_LostFocus](#remove_lostfocus)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-286">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7ffaa-287">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7ffaa-287">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="7ffaa-288">Remover um manipulador de eventos adicionado anteriormente com add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-288">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="7ffaa-289">[remove_MoveFocusRequested](#remove_movefocusrequested)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-289">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7ffaa-290">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7ffaa-290">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="7ffaa-291">Remover um manipulador de eventos adicionado anteriormente com add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-291">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="7ffaa-292">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-292">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7ffaa-293">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7ffaa-293">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="7ffaa-294">Atualize as propriedades Bounds e ZoomFactor ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-294">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="7ffaa-295">Public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(limites Rect, zoomFactor duplo)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-295">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds, double zoomFactor)</span></span>

<span data-ttu-id="7ffaa-296">Esta operação é atômica da perspectiva do host.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-296">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="7ffaa-297">Após retornar dessa função, as propriedades Bounds e ZoomFactor terão ambos sido atualizadas se a função for bem-sucedida ou nenhuma será atualizada se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-297">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="7ffaa-298">Se os limites e ZoomFactor forem atualizados com a mesma escala (ou seja, os limites e ZoomFactor forem ambos duplicados), a página não verá uma alteração em Window. innerWidth/innerHeight e o WebView renderizará o conteúdo no novo tamanho e será aplicado sem renderizações intermediárias.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-298">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="7ffaa-299">Essa função também pode ser usada para atualizar apenas um de ZoomFactor ou limites passando o novo valor para um e o valor atual para o outro.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-299">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```

