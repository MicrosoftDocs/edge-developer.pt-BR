---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: 79bc9908d0fd12d4606311b959cbc6bc0c384c2d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878915"
---
# <span data-ttu-id="a1fd3-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="a1fd3-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="a1fd3-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a1fd3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a1fd3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a1fd3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a1fd3-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="a1fd3-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a1fd3-108">Summary</span></span>

 <span data-ttu-id="a1fd3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a1fd3-109">Members</span></span>                        | <span data-ttu-id="a1fd3-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a1fd3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1fd3-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a1fd3-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="a1fd3-112">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="a1fd3-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a1fd3-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="a1fd3-114">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="a1fd3-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="a1fd3-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="a1fd3-116">Compare as versões do navegador corretamente para determinar qual é a versão mais recente, antiga ou mesma.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="a1fd3-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="a1fd3-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="a1fd3-118">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="a1fd3-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a1fd3-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="a1fd3-120">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="a1fd3-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a1fd3-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="a1fd3-122">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="a1fd3-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="a1fd3-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="a1fd3-124">Crie uma CoreWebView2ExperimentalPointerInfo vazia.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-124">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>
[<span data-ttu-id="a1fd3-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a1fd3-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="a1fd3-126">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="a1fd3-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a1fd3-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="a1fd3-128">Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="a1fd3-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="a1fd3-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="a1fd3-130">Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="a1fd3-131">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="a1fd3-132">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="a1fd3-133">Parte</span><span class="sxs-lookup"><span data-stu-id="a1fd3-133">Members</span></span>

#### <span data-ttu-id="a1fd3-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a1fd3-134">BrowserVersionString</span></span> 

<span data-ttu-id="a1fd3-135">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="a1fd3-136">Cadeia de caracteres pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="a1fd3-137">Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="a1fd3-138">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="a1fd3-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a1fd3-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="a1fd3-140">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="a1fd3-141">objeto<-EventHandler de evento público > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="a1fd3-142">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="a1fd3-143">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="a1fd3-144">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="a1fd3-145">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="a1fd3-146">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="a1fd3-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="a1fd3-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="a1fd3-148">Compare as versões do navegador corretamente para determinar qual é a versão mais recente, antiga ou mesma.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="a1fd3-149">public static int [CompareBrowserVersions](#comparebrowserversions)(String Version1, String Version2)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="a1fd3-150">Retorna-1, 0 ou 1 dependendo se Version1 é menor que, igual a ou maior que Version2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="a1fd3-151">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1fd3-151">Parameters</span></span>
* `version1` <span data-ttu-id="a1fd3-152">Uma das cadeias de caracteres da versão a comparar.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="a1fd3-153">A outra cadeia de caracteres de versão a comparar.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-153">The other version string to compare.</span></span>

#### <span data-ttu-id="a1fd3-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="a1fd3-154">CreateAsync</span></span> 

<span data-ttu-id="a1fd3-155">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="a1fd3-156">tarefa assíncrona estática pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(cadeia de caracteres browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions opções)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="a1fd3-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1fd3-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="a1fd3-158">O caminho relativo para a pasta que contém a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="a1fd3-159">userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="a1fd3-160">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="a1fd3-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a1fd3-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

> [!NOTE]
> <span data-ttu-id="a1fd3-162">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="a1fd3-162">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="a1fd3-163">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="a1fd3-164">tarefas assíncronas públicas< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="a1fd3-165">parentWindow é o HWND no qual o aplicativo conectará a árvore visual do WebView.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="a1fd3-166">Esse será o HWND que o aplicativo receberá a entrada de ponteiro/mouse para o WebView (e será necessário usar SendMouseInput/SendPointerInput para encaminhar).</span><span class="sxs-lookup"><span data-stu-id="a1fd3-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="a1fd3-167">Se o aplicativo mover a árvore visual da WebView para abaixo de uma janela diferente, então precisará definir CoreWebView2CompositionController. ParentWindow para atualizar o novo HWND pai da árvore visual.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="a1fd3-168">Defina a propriedade RootVisualTarget no CoreWebView2CompositionController criado para fornecer um Visual para hospedar a árvore visual do navegador.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="a1fd3-169">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="a1fd3-170">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="a1fd3-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a1fd3-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="a1fd3-172">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="a1fd3-173">tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="a1fd3-174">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="a1fd3-175">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="a1fd3-176">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="a1fd3-177">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="a1fd3-178">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="a1fd3-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="a1fd3-179">CreateCoreWebView2PointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="a1fd3-180">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="a1fd3-180">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="a1fd3-181">Crie uma CoreWebView2ExperimentalPointerInfo vazia.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-181">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>

> <span data-ttu-id="a1fd3-182">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="a1fd3-182">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="a1fd3-183">O CoreWebView2ExperimentalPointerInfo retornado precisa ser preenchido com todas as informações relevantes antes de chamar SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-183">The returned CoreWebView2ExperimentalPointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="a1fd3-184">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a1fd3-184">CreateWebResourceResponse</span></span> 

<span data-ttu-id="a1fd3-185">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-185">Create a new web resource response object.</span></span>

> <span data-ttu-id="a1fd3-186">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-186">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="a1fd3-187">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-187">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="a1fd3-188">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-188">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="a1fd3-189">Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-189">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="a1fd3-190">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a1fd3-190">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="a1fd3-191">Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-191">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="a1fd3-192">Cadeia de caracteres de cadeia estática [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(cadeia de caracteres browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-192">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="a1fd3-193">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1fd3-193">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="a1fd3-194">O caminho relativo para a pasta que contém a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-194">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="a1fd3-195">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="a1fd3-195">GetProviderForHwnd</span></span> 

> [!NOTE]
> <span data-ttu-id="a1fd3-196">Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="a1fd3-196">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="a1fd3-197">Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="a1fd3-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="a1fd3-198">[GetProviderForHwnd](#getproviderforhwnd)de objeto público (IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="a1fd3-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

