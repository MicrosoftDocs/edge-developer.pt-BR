---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: 05b8a10c723ae57b2c95551f4d5043f3336eba3b
ms.sourcegitcommit: 65db518273b3cd69f1b3c528809600719b9b70aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016323"
---
# <span data-ttu-id="1598b-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="1598b-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="1598b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1598b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1598b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="1598b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1598b-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="1598b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="1598b-108">Summary</span></span>

 <span data-ttu-id="1598b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1598b-109">Members</span></span>                        | <span data-ttu-id="1598b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="1598b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1598b-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1598b-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="1598b-112">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="1598b-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="1598b-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1598b-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="1598b-114">NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso por meio do WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="1598b-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="1598b-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="1598b-116">Compare as versões do navegador para determinar se elas correspondem ou são diferentes.</span><span class="sxs-lookup"><span data-stu-id="1598b-116">Compare browser versions to determine if they match or are different.</span></span>
[<span data-ttu-id="1598b-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="1598b-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="1598b-118">Cria um ambiente WebView2 verde usando a versão instalada do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1598b-118">Creates an evergreen WebView2 Environment using the installed version of Microsoft Edge.</span></span>
[<span data-ttu-id="1598b-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1598b-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="1598b-120">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="1598b-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="1598b-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1598b-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="1598b-122">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="1598b-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="1598b-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="1598b-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="1598b-124">Crie uma CoreWebView2PointerInfo vazia.</span><span class="sxs-lookup"><span data-stu-id="1598b-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="1598b-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1598b-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="1598b-126">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="1598b-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="1598b-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1598b-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="1598b-128">Obter informações sobre a versão do navegador.</span><span class="sxs-lookup"><span data-stu-id="1598b-128">Get the browser version information.</span></span>
[<span data-ttu-id="1598b-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="1598b-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="1598b-130">Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="1598b-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="1598b-131">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="1598b-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="1598b-132">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="1598b-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

## <span data-ttu-id="1598b-133">Parte</span><span class="sxs-lookup"><span data-stu-id="1598b-133">Members</span></span>

#### <span data-ttu-id="1598b-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1598b-134">BrowserVersionString</span></span> 

<span data-ttu-id="1598b-135">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="1598b-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="1598b-136">Cadeia de caracteres pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="1598b-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="1598b-137">Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="1598b-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="1598b-138">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="1598b-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="1598b-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1598b-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="1598b-140">NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso por meio do WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-140">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="1598b-141">objeto<-EventHandler de evento público > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="1598b-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="1598b-142">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="1598b-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="1598b-143">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="1598b-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="1598b-144">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="1598b-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="1598b-145">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="1598b-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="1598b-146">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1598b-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="1598b-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="1598b-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="1598b-148">Compare as versões do navegador para determinar se elas correspondem ou são diferentes.</span><span class="sxs-lookup"><span data-stu-id="1598b-148">Compare browser versions to determine if they match or are different.</span></span>

> <span data-ttu-id="1598b-149">public static int [CompareBrowserVersions](#comparebrowserversions)(String Version1, String Version2)</span><span class="sxs-lookup"><span data-stu-id="1598b-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="1598b-150">Retorna-1, 0 ou 1 dependendo se a primeira versão for menor que, igual a ou maior que a segunda versão sendo comparada.</span><span class="sxs-lookup"><span data-stu-id="1598b-150">Returns -1, 0 or 1 depending on whether the first version is less than, equal to or greater than the second version being compared.</span></span>

<span data-ttu-id="1598b-151">A entrada pode usar diretamente o versionInfo obtido do GetAvailableCoreWebView2BrowserVersionString, as informações do canal serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="1598b-151">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

##### <span data-ttu-id="1598b-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1598b-152">Parameters</span></span>
* `version1` <span data-ttu-id="1598b-153">A primeira versão a comparar.</span><span class="sxs-lookup"><span data-stu-id="1598b-153">The first version to compare.</span></span> 

* `version2` <span data-ttu-id="1598b-154">A segunda versão a comparar.</span><span class="sxs-lookup"><span data-stu-id="1598b-154">The second version to compare.</span></span>

#### <span data-ttu-id="1598b-155">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="1598b-155">CreateAsync</span></span> 

<span data-ttu-id="1598b-156">Cria um ambiente WebView2 verde usando a versão instalada do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1598b-156">Creates an evergreen WebView2 Environment using the installed version of Microsoft Edge.</span></span>

> <span data-ttu-id="1598b-157">tarefa assíncrona estática pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(cadeia de caracteres browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions opções)</span><span class="sxs-lookup"><span data-stu-id="1598b-157">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="1598b-158">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1598b-158">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="1598b-159">O caminho relativo para a pasta que contém a versão fixa do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-159">The relative path to the folder that contains the fixed version of the WebView2 Runtime.</span></span> 

* `userDataFolder` <span data-ttu-id="1598b-160">userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-160">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="1598b-161">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-161">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="1598b-162">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1598b-162">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1598b-163">Crie assincronamente um novo WebView para uso com hospedagem Visual.</span><span class="sxs-lookup"><span data-stu-id="1598b-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="1598b-164">tarefas assíncronas públicas< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="1598b-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1598b-165">parentWindow é o HWND no qual o aplicativo conectará a árvore visual do WebView.</span><span class="sxs-lookup"><span data-stu-id="1598b-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="1598b-166">Esse será o HWND que o aplicativo receberá a entrada de ponteiro/mouse para o WebView (e será necessário usar SendMouseInput/SendPointerInput para encaminhar).</span><span class="sxs-lookup"><span data-stu-id="1598b-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="1598b-167">Se o aplicativo mover a árvore visual da WebView para abaixo de uma janela diferente, então precisará definir CoreWebView2CompositionController. ParentWindow para atualizar o novo HWND pai da árvore visual.</span><span class="sxs-lookup"><span data-stu-id="1598b-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="1598b-168">Defina a propriedade RootVisualTarget no CoreWebView2CompositionController criado para fornecer um Visual para hospedar a árvore visual do navegador.</span><span class="sxs-lookup"><span data-stu-id="1598b-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="1598b-169">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1598b-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1598b-170">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1598b-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1598b-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1598b-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="1598b-172">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="1598b-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="1598b-173">tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="1598b-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1598b-174">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="1598b-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="1598b-175">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="1598b-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="1598b-176">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="1598b-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="1598b-177">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1598b-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1598b-178">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1598b-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1598b-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="1598b-179">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1598b-180">Crie uma CoreWebView2PointerInfo vazia.</span><span class="sxs-lookup"><span data-stu-id="1598b-180">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="1598b-181">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="1598b-181">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="1598b-182">O CoreWebView2PointerInfo retornado precisa ser preenchido com todas as informações relevantes antes de chamar SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="1598b-182">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="1598b-183">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1598b-183">CreateWebResourceResponse</span></span> 

<span data-ttu-id="1598b-184">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="1598b-184">Create a new web resource response object.</span></span>

> <span data-ttu-id="1598b-185">Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="1598b-185">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="1598b-186">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="1598b-186">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="1598b-187">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="1598b-187">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="1598b-188">Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="1598b-188">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="1598b-189">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1598b-189">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="1598b-190">Obter informações sobre a versão do navegador.</span><span class="sxs-lookup"><span data-stu-id="1598b-190">Get the browser version information.</span></span>

> <span data-ttu-id="1598b-191">Cadeia de caracteres de cadeia estática [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(cadeia de caracteres browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="1598b-191">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

<span data-ttu-id="1598b-192">Você também receberá o nome do canal se o canal não for um canal estável.</span><span class="sxs-lookup"><span data-stu-id="1598b-192">You also get the channel name if the channel is not a stable channel.</span></span> <span data-ttu-id="1598b-193">Se você usar o tempo de execução WebView2, nenhum nome de canal será retornado.</span><span class="sxs-lookup"><span data-stu-id="1598b-193">If you use the WebView2 Runtime, no channel name is returned.</span></span>

##### <span data-ttu-id="1598b-194">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1598b-194">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="1598b-195">O caminho relativo para a pasta que contém a versão fixa do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="1598b-195">The relative path to the folder that contains the fixed version of the WebView2 Runtime.</span></span>

#### <span data-ttu-id="1598b-196">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="1598b-196">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1598b-197">Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.</span><span class="sxs-lookup"><span data-stu-id="1598b-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="1598b-198">[GetProviderForHwnd](#getproviderforhwnd)de objeto público (IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="1598b-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>
