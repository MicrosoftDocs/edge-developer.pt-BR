---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: c6b1f1c62da5aa5ef64693575abb9cb46ac13851
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011510"
---
# <span data-ttu-id="7b3b4-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="7b3b4-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="7b3b4-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7b3b4-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7b3b4-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7b3b4-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7b3b4-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="7b3b4-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7b3b4-108">Summary</span></span>

 <span data-ttu-id="7b3b4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7b3b4-109">Members</span></span>                        | <span data-ttu-id="7b3b4-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7b3b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7b3b4-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="7b3b4-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="7b3b4-112">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="7b3b4-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7b3b4-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="7b3b4-114">NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso por meio do WebView2.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="7b3b4-115">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7b3b4-115">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="7b3b4-116">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-116">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="7b3b4-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7b3b4-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="7b3b4-118">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="7b3b4-119">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="7b3b4-119">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="7b3b4-120">Crie uma CoreWebView2PointerInfo vazia.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-120">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="7b3b4-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7b3b4-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="7b3b4-122">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-122">Create a new web resource response object.</span></span>
[<span data-ttu-id="7b3b4-123">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="7b3b4-123">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="7b3b4-124">Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-124">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="7b3b4-125">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-125">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="7b3b4-126">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-126">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

<span data-ttu-id="7b3b4-127">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-127">WebViews created from an environment run on the browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="7b3b4-128">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-128">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="7b3b4-129">Parte</span><span class="sxs-lookup"><span data-stu-id="7b3b4-129">Members</span></span>

#### <span data-ttu-id="7b3b4-130">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="7b3b4-130">BrowserVersionString</span></span> 

<span data-ttu-id="7b3b4-131">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-131">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="7b3b4-132">Cadeia de caracteres pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-132">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="7b3b4-133">Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-133">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="7b3b4-134">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-134">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="7b3b4-135">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7b3b4-135">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="7b3b4-136">NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso por meio do WebView2.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-136">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="7b3b4-137">objeto<-EventHandler de evento público > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-137">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="7b3b4-138">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-138">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="7b3b4-139">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-139">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="7b3b4-140">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-140">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="7b3b4-141">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-141">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="7b3b4-142">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-142">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="7b3b4-143">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7b3b4-143">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7b3b4-144">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-144">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="7b3b4-145">tarefas assíncronas públicas< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-145">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="7b3b4-146">parentWindow é o HWND no qual o aplicativo conectará a árvore visual do WebView.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-146">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="7b3b4-147">Esse será o HWND que o aplicativo receberá a entrada de ponteiro/mouse para o WebView (e será necessário usar SendMouseInput/SendPointerInput para encaminhar).</span><span class="sxs-lookup"><span data-stu-id="7b3b4-147">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="7b3b4-148">Se o aplicativo mover a árvore visual da WebView para abaixo de uma janela diferente, então precisará definir CoreWebView2CompositionController. ParentWindow para atualizar o novo HWND pai da árvore visual.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-148">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="7b3b4-149">Defina a propriedade RootVisualTarget no CoreWebView2CompositionController criado para fornecer um Visual para hospedar a árvore visual do navegador.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-149">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="7b3b4-150">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="7b3b4-151">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="7b3b4-152">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7b3b4-152">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="7b3b4-153">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-153">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="7b3b4-154">tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-154">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="7b3b4-155">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-155">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="7b3b4-156">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-156">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="7b3b4-157">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-157">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="7b3b4-158">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-158">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="7b3b4-159">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-159">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="7b3b4-160">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="7b3b4-160">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7b3b4-161">Crie uma CoreWebView2PointerInfo vazia.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-161">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="7b3b4-162">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="7b3b4-162">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="7b3b4-163">O CoreWebView2PointerInfo retornado precisa ser preenchido com todas as informações relevantes antes de chamar SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-163">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="7b3b4-164">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7b3b4-164">CreateWebResourceResponse</span></span> 

<span data-ttu-id="7b3b4-165">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-165">Create a new web resource response object.</span></span>

> <span data-ttu-id="7b3b4-166">Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-166">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="7b3b4-167">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-167">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="7b3b4-168">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-168">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="7b3b4-169">Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-169">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="7b3b4-170">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="7b3b4-170">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7b3b4-171">Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="7b3b4-171">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="7b3b4-172">[GetProviderForHwnd](#getproviderforhwnd)de objeto público (IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="7b3b4-172">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

