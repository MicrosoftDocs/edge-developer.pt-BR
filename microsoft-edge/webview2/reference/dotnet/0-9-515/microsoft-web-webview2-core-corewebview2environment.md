---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 305b25c8db209da4f1e2e54169231ce568e9f5cb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885029"
---
# <span data-ttu-id="a4876-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="a4876-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="a4876-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a4876-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a4876-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a4876-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a4876-107">Isso representa o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="a4876-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="a4876-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a4876-108">Summary</span></span>

 <span data-ttu-id="a4876-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a4876-109">Members</span></span>                        | <span data-ttu-id="a4876-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a4876-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a4876-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a4876-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="a4876-112">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="a4876-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="a4876-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a4876-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="a4876-114">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="a4876-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="a4876-115">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="a4876-115">CreateAsync</span></span>](#createasync) | <span data-ttu-id="a4876-116">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="a4876-116">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="a4876-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a4876-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="a4876-118">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="a4876-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="a4876-119">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a4876-119">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="a4876-120">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="a4876-120">Create a new web resource response object.</span></span>

<span data-ttu-id="a4876-121">Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente.</span><span class="sxs-lookup"><span data-stu-id="a4876-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="a4876-122">Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.</span><span class="sxs-lookup"><span data-stu-id="a4876-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="a4876-123">Parte</span><span class="sxs-lookup"><span data-stu-id="a4876-123">Members</span></span>

#### <span data-ttu-id="a4876-124">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a4876-124">BrowserVersionString</span></span> 

<span data-ttu-id="a4876-125">As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="a4876-125">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="a4876-126">Cadeia de caracteres pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="a4876-126">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="a4876-127">Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="a4876-127">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="a4876-128">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="a4876-128">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="a4876-129">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a4876-129">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="a4876-130">O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.</span><span class="sxs-lookup"><span data-stu-id="a4876-130">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="a4876-131">objeto<-EventHandler de evento público > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="a4876-131">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="a4876-132">Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView.</span><span class="sxs-lookup"><span data-stu-id="a4876-132">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="a4876-133">Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="a4876-133">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="a4876-134">Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="a4876-134">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="a4876-135">Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro.</span><span class="sxs-lookup"><span data-stu-id="a4876-135">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="a4876-136">Ou simplesmente solicitar que o usuário reinicie o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4876-136">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="a4876-137">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="a4876-137">CreateAsync</span></span> 

<span data-ttu-id="a4876-138">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="a4876-138">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="a4876-139">tarefa assíncrona estática pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(cadeia de caracteres browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions opções)</span><span class="sxs-lookup"><span data-stu-id="a4876-139">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="a4876-140">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4876-140">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="a4876-141">O caminho relativo para a pasta que contém a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="a4876-141">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="a4876-142">userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2.</span><span class="sxs-lookup"><span data-stu-id="a4876-142">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="a4876-143">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="a4876-143">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="a4876-144">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a4876-144">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="a4876-145">Criar de forma assíncrona um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="a4876-145">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="a4876-146">tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="a4876-146">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="a4876-147">parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="a4876-147">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="a4876-148">O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView.</span><span class="sxs-lookup"><span data-stu-id="a4876-148">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="a4876-149">A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.</span><span class="sxs-lookup"><span data-stu-id="a4876-149">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="a4876-150">É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4876-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="a4876-151">Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.</span><span class="sxs-lookup"><span data-stu-id="a4876-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="a4876-152">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a4876-152">CreateWebResourceResponse</span></span> 

<span data-ttu-id="a4876-153">Crie um novo objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="a4876-153">Create a new web resource response object.</span></span>

> <span data-ttu-id="a4876-154">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="a4876-154">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="a4876-155">Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha.</span><span class="sxs-lookup"><span data-stu-id="a4876-155">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="a4876-156">Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha.</span><span class="sxs-lookup"><span data-stu-id="a4876-156">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="a4876-157">Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="a4876-157">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

