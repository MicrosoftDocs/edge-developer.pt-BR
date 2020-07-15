---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: a3e8a958a70820bf32bd3a76acc9ee503f568438
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877753"
---
# <span data-ttu-id="f41f8-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="f41f8-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

> [!NOTE]
> <span data-ttu-id="f41f8-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f41f8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f41f8-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="f41f8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f41f8-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f41f8-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f41f8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f41f8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f41f8-109">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="f41f8-109">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="f41f8-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="f41f8-110">Summary</span></span>

 <span data-ttu-id="f41f8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f41f8-111">Members</span></span>                        | <span data-ttu-id="f41f8-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="f41f8-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f41f8-113">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="f41f8-113">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="f41f8-114">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="f41f8-114">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="f41f8-115">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f41f8-115">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="f41f8-116">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="f41f8-116">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="f41f8-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="f41f8-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="f41f8-118">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="f41f8-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="f41f8-119">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="f41f8-119">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="f41f8-120">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="f41f8-120">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="f41f8-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f41f8-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="f41f8-122">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="f41f8-122">Create a new web resource response object.</span></span>

<span data-ttu-id="f41f8-123">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="f41f8-123">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="f41f8-124">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="f41f8-124">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="f41f8-125">Parte</span><span class="sxs-lookup"><span data-stu-id="f41f8-125">Members</span></span>

#### <span data-ttu-id="f41f8-126">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="f41f8-126">BrowserVersionString</span></span> 

<span data-ttu-id="f41f8-127">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="f41f8-127">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="f41f8-128">Cadeia de caracteres pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="f41f8-128">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="f41f8-129">Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="f41f8-129">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="f41f8-130">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="f41f8-130">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="f41f8-131">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f41f8-131">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="f41f8-132">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="f41f8-132">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="f41f8-133">objeto<-EventHandler de evento público > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="f41f8-133">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="f41f8-134">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="f41f8-134">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="f41f8-135">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="f41f8-135">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="f41f8-136">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="f41f8-136">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="f41f8-137">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="f41f8-137">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="f41f8-138">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f41f8-138">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="f41f8-139">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="f41f8-139">CreateAsync</span></span> 

<span data-ttu-id="f41f8-140">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="f41f8-140">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="f41f8-141">tarefa assíncrona estática pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(cadeia de caracteres browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions opções)</span><span class="sxs-lookup"><span data-stu-id="f41f8-141">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="f41f8-142">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f41f8-142">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="f41f8-143">O caminho relativo para a pasta que contém a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="f41f8-143">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="f41f8-144">userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2.</span><span class="sxs-lookup"><span data-stu-id="f41f8-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="f41f8-145">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="f41f8-145">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="f41f8-146">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="f41f8-146">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="f41f8-147">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="f41f8-147">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="f41f8-148">tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="f41f8-148">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="f41f8-149">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="f41f8-149">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="f41f8-150">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="f41f8-150">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="f41f8-151">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="f41f8-151">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="f41f8-152">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f41f8-152">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="f41f8-153">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="f41f8-153">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="f41f8-154">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f41f8-154">CreateWebResourceResponse</span></span> 

<span data-ttu-id="f41f8-155">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="f41f8-155">Create a new web resource response object.</span></span>

> <span data-ttu-id="f41f8-156">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="f41f8-156">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="f41f8-157">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="f41f8-157">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="f41f8-158">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="f41f8-158">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="f41f8-159">Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="f41f8-159">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

