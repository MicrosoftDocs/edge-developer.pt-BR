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
ms.openlocfilehash: 1e1fb60935c1706ab8d9ffb21d06186bfea3f6d0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652350"
---
# <span data-ttu-id="d68e5-104">Globais</span><span class="sxs-lookup"><span data-stu-id="d68e5-104">Globals</span></span> 

## <span data-ttu-id="d68e5-105">Resumo</span><span class="sxs-lookup"><span data-stu-id="d68e5-105">Summary</span></span>

 <span data-ttu-id="d68e5-106">Parte</span><span class="sxs-lookup"><span data-stu-id="d68e5-106">Members</span></span>                        | <span data-ttu-id="d68e5-107">Descrições</span><span class="sxs-lookup"><span data-stu-id="d68e5-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d68e5-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="d68e5-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="d68e5-109">Esse método é para que qualquer pessoa queira comparar a versão corretamente para determinar qual é a versão mais recente, mais antiga ou mesma.</span><span class="sxs-lookup"><span data-stu-id="d68e5-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="d68e5-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="d68e5-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="d68e5-111">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="d68e5-112">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="d68e5-112">CreateCoreWebView2EnvironmentWithDetails</span></span>](#createcorewebview2environmentwithdetails) | <span data-ttu-id="d68e5-113">Esta API será removida na próxima versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="d68e5-113">This API is going to be removed in next SDK release.</span></span>
[<span data-ttu-id="d68e5-114">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="d68e5-114">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="d68e5-115">DLL Export para criar um ambiente WebView2 com uma versão personalizada do Edge, diretório de dados do usuário e/ou opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="d68e5-115">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="d68e5-116">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="d68e5-116">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="d68e5-117">Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-117">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="d68e5-118">Parte</span><span class="sxs-lookup"><span data-stu-id="d68e5-118">Members</span></span>

#### <span data-ttu-id="d68e5-119">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="d68e5-119">CompareBrowserVersions</span></span> 

> <span data-ttu-id="d68e5-120">Public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int \* resultado)</span><span class="sxs-lookup"><span data-stu-id="d68e5-120">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="d68e5-121">Esse método é para que qualquer pessoa queira comparar a versão corretamente para determinar qual é a versão mais recente, mais antiga ou mesma.</span><span class="sxs-lookup"><span data-stu-id="d68e5-121">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="d68e5-122">Ele pode ser usado para determinar se você deve usar o webview2 ou determinada base de recursos na versão.</span><span class="sxs-lookup"><span data-stu-id="d68e5-122">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="d68e5-123">Define o valor do resultado para-1, 0 ou 1 se Version1 for menor que, igual ou maior do que Version2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d68e5-123">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="d68e5-124">Retorna E_INVALIDARG se não conseguir analisar nenhuma cadeia de caracteres de versão ou se qualquer parâmetro de entrada for nulo.</span><span class="sxs-lookup"><span data-stu-id="d68e5-124">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="d68e5-125">A entrada pode usar diretamente o versionInfo obtido do GetAvailableCoreWebView2BrowserVersionString, as informações do canal serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="d68e5-125">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="d68e5-126">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="d68e5-126">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="d68e5-127">Public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="d68e5-127">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="d68e5-128">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-128">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="d68e5-129">Isso equivale a chamar CreateCoreWebView2EnvironmentWithOptions com nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="d68e5-129">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="d68e5-130">Consulte CreateCoreWebView2EnvironmentWithOptions para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="d68e5-130">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="d68e5-131">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="d68e5-131">CreateCoreWebView2EnvironmentWithDetails</span></span> 

> <span data-ttu-id="d68e5-132">Public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR AdditionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="d68e5-132">public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, PCWSTR additionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="d68e5-133">Esta API será removida na próxima versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="d68e5-133">This API is going to be removed in next SDK release.</span></span>

<span data-ttu-id="d68e5-134">Use CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="d68e5-134">Please use CreateCoreWebView2EnvironmentWithOptions.</span></span>

#### <span data-ttu-id="d68e5-135">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="d68e5-135">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="d68e5-136">Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentoptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="d68e5-136">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="d68e5-137">DLL Export para criar um ambiente WebView2 com uma versão personalizada do Edge, diretório de dados do usuário e/ou opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="d68e5-137">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="d68e5-138">browserExecutableFolder é o caminho relativo para a pasta que contém a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-138">browserExecutableFolder is the relative path to the folder that contains the embedded Edge.</span></span> <span data-ttu-id="d68e5-139">A borda incorporada pode ser obtida copiando a versão nomeada pasta de uma borda instalada, como 73.0.52.0 subpasta de uma borda 73.0.52.0 instalada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-139">The embedded Edge can be obtained by copying the version named folder of an installed Edge, like 73.0.52.0 sub folder of an installed 73.0.52.0 Edge.</span></span> <span data-ttu-id="d68e5-140">A pasta deve ter msedge. exe, msedge. dll e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d68e5-140">The folder should have msedge.exe, msedge.dll, and so on.</span></span> <span data-ttu-id="d68e5-141">Use uma cadeia de caracteres nula ou vazia para browserExecutableFolder para criar WebView usando o Edge instalado no computador, caso em que a API tentará localizar uma versão compatível do Edge instalada no computador de acordo com a preferência de canal que tenta encontrar a instalação por usuário e, em seguida, por instalação por computador.</span><span class="sxs-lookup"><span data-stu-id="d68e5-141">Use null or empty string for browserExecutableFolder to create WebView using Edge installed on the machine, in which case the API will try to find a compatible version of Edge installed on the machine according to the channel preference trying to find first per user install and then per machine install.</span></span>

<span data-ttu-id="d68e5-142">A ordem padrão de pesquisa de canal é estável, beta, dev e Canárias.</span><span class="sxs-lookup"><span data-stu-id="d68e5-142">The default channel search order is stable, beta, dev, and canary.</span></span> <span data-ttu-id="d68e5-143">Quando houver uma variável de ambiente WEBVIEW2_RELEASE_CHANNEL_PREFERENCE ou valor de registro releaseChannelPreference aplicável com o valor 1, a ordem de pesquisa de canal será revertida.</span><span class="sxs-lookup"><span data-stu-id="d68e5-143">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="d68e5-144">userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2.</span><span class="sxs-lookup"><span data-stu-id="d68e5-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="d68e5-145">O caminho pode ser um caminho de arquivo absoluto ou um caminho de arquivo relativo que é interpretado como relativo ao executável do processo atual.</span><span class="sxs-lookup"><span data-stu-id="d68e5-145">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="d68e5-146">Caso contrário, para aplicativos UWP, a pasta de dados do usuário padrão será a pasta dados do aplicativo para o pacote; para aplicativos não UWP, a pasta de dados de usuário padrão `{Executable File Name}.WebView2` será criada no mesmo diretório ao lado do executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d68e5-146">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="d68e5-147">A criação do WebView2 pode falhar se o executável estiver em execução em um diretório em que o processo não tem permissão para criar uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="d68e5-147">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="d68e5-148">O aplicativo é responsável por limpar a pasta dados do usuário quando isso é feito.</span><span class="sxs-lookup"><span data-stu-id="d68e5-148">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="d68e5-149">Observe que, como um processo de navegador pode ser compartilhado entre exibições da Web, a criação do WebView falhará com o HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) se as opções especificadas não corresponderem às opções dos webviews que estão sendo executadas no processo do navegador compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d68e5-149">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="d68e5-150">environment_created_handler é o resultado do manipulador para a operação assíncrona que conterá a WebView2Environment que foi criada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-150">environment_created_handler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="d68e5-151">O browserExecutableFolder, o userDataFolder e o additionalBrowserArguments do environmentoptions podem ser substituídos por valores especificados em variáveis de ambiente ou no registro.</span><span class="sxs-lookup"><span data-stu-id="d68e5-151">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="d68e5-152">Ao criar um WebView2Environment, as seguintes variáveis de ambiente são verificadas:</span><span class="sxs-lookup"><span data-stu-id="d68e5-152">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="d68e5-153">Se uma variável de ambiente Override for encontrada, usamos os valores browserExecutableFolder, userDataFolder e additionalBrowserArguments como substituições para os valores correspondentes nos parâmetros CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="d68e5-153">If an override environment variable is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="d68e5-154">Embora não seja estritamente substituições, existem variáveis de ambiente adicionais que podem ser definidas:</span><span class="sxs-lookup"><span data-stu-id="d68e5-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="d68e5-155">Quando encontrado com um valor não vazio, isso indica que o WebView está sendo iniciado em um depurador de script.</span><span class="sxs-lookup"><span data-stu-id="d68e5-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="d68e5-156">Nesse caso, o WebView emitirá um `Page.waitForDebugger` comando CDP que fará com que a execução do script dentro do WebView seja pausada durante a inicialização, até que um depurador emita um `Runtime.runIfWaitingForDebugger` comando CDP correspondente para continuar a execução.</span><span class="sxs-lookup"><span data-stu-id="d68e5-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="d68e5-157">Observação: não há nenhuma chave de registro equivalente a essa variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="d68e5-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="d68e5-158">Quando encontrado com um valor não vazio, isso indica que o WebView está sendo iniciado em um depurador de script que também dá suporte a aplicativos host que usam vários webviews.</span><span class="sxs-lookup"><span data-stu-id="d68e5-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="d68e5-159">O valor é usado como o identificador de um pipe nomeado que será aberto e gravado quando um novo WebView for criado pelo aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="d68e5-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="d68e5-160">A carga corresponderá à do destino JSON da porta de depuração remota e pode ser usada pelo depurador externo para ser anexada a uma instância do WebView específica.</span><span class="sxs-lookup"><span data-stu-id="d68e5-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="d68e5-161">O formato do pipe criado pelo depurador deve ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` onde:</span><span class="sxs-lookup"><span data-stu-id="d68e5-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="d68e5-162">é o nome de arquivo exe do aplicativo host, por exemplo, WebView2Example. exe</span><span class="sxs-lookup"><span data-stu-id="d68e5-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="d68e5-163">é o valor definido para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="d68e5-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="d68e5-164">Para habilitar a depuração dos destinos identificados pela JSON, você também precisará definir a variável de ambiente WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` onde:</span><span class="sxs-lookup"><span data-stu-id="d68e5-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="d68e5-165">é a porta na qual o servidor CDP será ligado.</span><span class="sxs-lookup"><span data-stu-id="d68e5-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="d68e5-166">Lembre-se de que definir as variáveis de ambiente WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER e WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS fará com que os webviews hospedados em seu aplicativo e seu conteúdo sejam expostos a aplicativos de terceiros, como depuradores.</span><span class="sxs-lookup"><span data-stu-id="d68e5-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="d68e5-167">Observação: não há nenhuma chave de registro equivalente a essa variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="d68e5-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="d68e5-168">Se nenhuma dessas variáveis de ambiente existir, o registro será examinado em seguida.</span><span class="sxs-lookup"><span data-stu-id="d68e5-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="d68e5-169">As seguintes chaves do registro estão marcadas:</span><span class="sxs-lookup"><span data-stu-id="d68e5-169">The following registry keys are checked:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="d68e5-170">No cenário improvável em que algumas instâncias do WebView são abertas durante uma atualização do navegador, poderíamos acabar bloqueando a exclusão de navegadores de bordas antigas.</span><span class="sxs-lookup"><span data-stu-id="d68e5-170">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="d68e5-171">Para evitar a falta de espaço em disco, uma nova criação do WebView falhará com o próximo erro se detectar que há muitas versões antigas presentes.</span><span class="sxs-lookup"><span data-stu-id="d68e5-171">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="d68e5-172">O número máximo padrão de versões de Borda permitido é 20.</span><span class="sxs-lookup"><span data-stu-id="d68e5-172">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="d68e5-173">O número máximo de versões de borda antigas permitidas pode ser substituído pelo valor da variável de ambiente a seguir.</span><span class="sxs-lookup"><span data-stu-id="d68e5-173">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="d68e5-174">Se a WebView depender de uma borda instalada e ela for desinstalada, haverá falha na criação subsequente com o próximo erro</span><span class="sxs-lookup"><span data-stu-id="d68e5-174">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="d68e5-175">Primeiro, verificamos com root como HKLM e depois HKCU.</span><span class="sxs-lookup"><span data-stu-id="d68e5-175">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="d68e5-176">AppId é definido primeiro como a ID do modelo do usuário do aplicativo do processo do chamador e, se não houver nenhuma chave do registro correspondente, a AppId será definida como o nome do executável do processo do chamador ou, se não for uma chave do registro, ' \* '.</span><span class="sxs-lookup"><span data-stu-id="d68e5-176">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="d68e5-177">Se uma chave de substituição do registro for encontrada, usamos os valores do registro browserExecutableFolder, userDataFolder e additionalBrowserArguments como substituições para os valores correspondentes nos parâmetros CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="d68e5-177">If an override registry key is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments registry values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="d68e5-178">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="d68e5-178">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="d68e5-179">Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="d68e5-179">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="d68e5-180">Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-180">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="d68e5-181">Os nomes dos canais são beta, dev e Canárias.</span><span class="sxs-lookup"><span data-stu-id="d68e5-181">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="d68e5-182">Se houver uma substituição para o browserExecutableFolder ou para a preferência de canal, a substituição será usada.</span><span class="sxs-lookup"><span data-stu-id="d68e5-182">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="d68e5-183">Se não houver uma substituição, o parâmetro passado para GetAvailableCoreWebView2BrowserVersionString será usado.</span><span class="sxs-lookup"><span data-stu-id="d68e5-183">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>

