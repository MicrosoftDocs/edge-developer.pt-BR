---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Globais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 37a7d89dbd7d13befe5a07c72fc8baa750775108
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011568"
---
# <span data-ttu-id="df345-104">Globais</span><span class="sxs-lookup"><span data-stu-id="df345-104">Globals</span></span> 

## <span data-ttu-id="df345-105">Resumo</span><span class="sxs-lookup"><span data-stu-id="df345-105">Summary</span></span>

 <span data-ttu-id="df345-106">Parte</span><span class="sxs-lookup"><span data-stu-id="df345-106">Members</span></span>                        | <span data-ttu-id="df345-107">Descrições</span><span class="sxs-lookup"><span data-stu-id="df345-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="df345-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="df345-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="df345-109">Esse método é para que qualquer pessoa queira comparar a versão corretamente para determinar qual é a versão mais recente, mais antiga ou mesma.</span><span class="sxs-lookup"><span data-stu-id="df345-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="df345-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="df345-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="df345-111">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="df345-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="df345-112">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="df345-112">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="df345-113">DLL Export para criar um ambiente WebView2 com uma versão personalizada do Edge, diretório de dados do usuário e/ou opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="df345-113">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="df345-114">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="df345-114">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="df345-115">Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="df345-115">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="df345-116">Parte</span><span class="sxs-lookup"><span data-stu-id="df345-116">Members</span></span>

#### <span data-ttu-id="df345-117">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="df345-117">CompareBrowserVersions</span></span> 

> <span data-ttu-id="df345-118">Public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int \* resultado)</span><span class="sxs-lookup"><span data-stu-id="df345-118">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="df345-119">Esse método é para que qualquer pessoa queira comparar a versão corretamente para determinar qual é a versão mais recente, mais antiga ou mesma.</span><span class="sxs-lookup"><span data-stu-id="df345-119">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="df345-120">Ele pode ser usado para determinar se você deve usar o webview2 ou determinada base de recursos na versão.</span><span class="sxs-lookup"><span data-stu-id="df345-120">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="df345-121">Define o valor do resultado para-1, 0 ou 1 se Version1 for menor que, igual ou maior do que Version2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="df345-121">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="df345-122">Retorna E_INVALIDARG se não conseguir analisar nenhuma cadeia de caracteres de versão ou se qualquer parâmetro de entrada for nulo.</span><span class="sxs-lookup"><span data-stu-id="df345-122">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="df345-123">A entrada pode usar diretamente o versionInfo obtido do GetAvailableCoreWebView2BrowserVersionString, as informações do canal serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="df345-123">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="df345-124">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="df345-124">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="df345-125">Public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="df345-125">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span></span>

<span data-ttu-id="df345-126">Cria um ambiente WebView2 verde usando a versão de Borda instalada.</span><span class="sxs-lookup"><span data-stu-id="df345-126">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="df345-127">Isso equivale a chamar CreateCoreWebView2EnvironmentWithOptions com nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="df345-127">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="df345-128">Consulte CreateCoreWebView2EnvironmentWithOptions para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="df345-128">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="df345-129">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="df345-129">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="df345-130">Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentoptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="df345-130">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span></span>

<span data-ttu-id="df345-131">DLL Export para criar um ambiente WebView2 com uma versão personalizada do Edge, diretório de dados do usuário e/ou opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="df345-131">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="df345-132">O ambiente WebView2 e todos os outros objetos WebView2 são únicos threads e têm dependências em componentes do Windows que exigem que o COM seja inicializado para um apartamento de thread único.</span><span class="sxs-lookup"><span data-stu-id="df345-132">The WebView2 environment and all other WebView2 objects are single threaded and have dependencies on Windows components that require COM to be initialized for a single-threaded apartment.</span></span> <span data-ttu-id="df345-133">Espera-se que o aplicativo chame CoInitializeEx antes de chamar CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="df345-133">The application is expected to call CoInitializeEx before calling CreateCoreWebView2EnvironmentWithOptions.</span></span>

```
CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED);
```

<span data-ttu-id="df345-134">Se CoInitializeEx não for chamado ou tiver sido chamado anteriormente com COINIT_MULTITHREADED, o CreateCoreWebView2EnvironmentWithOptions falhará com um dos seguintes erros.</span><span class="sxs-lookup"><span data-stu-id="df345-134">If CoInitializeEx was not called or has been previously called with COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions will fail with one of the following errors.</span></span>

```
CO_E_NOTINITIALIZED (if CoInitializeEx was not called)
RPC_E_CHANGED_MODE  (if CoInitializeEx was previously called with
                     COINIT_MULTITHREADED)
```

<span data-ttu-id="df345-135">Use `browserExecutableFolder` para especificar se os controles WebView2 usam uma versão fixa ou instalada do tempo de execução do WebView2 que existe em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="df345-135">Use `browserExecutableFolder` to specify whether WebView2 controls use a fixed or installed version of the WebView2 Runtime that exists on a client machine.</span></span> <span data-ttu-id="df345-136">Para usar uma versão fixa do tempo de execução do WebView2, passe o caminho relativo da pasta que contém a versão fixa do tempo de execução do WebView2 `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="df345-136">To use a fixed version of the WebView2 Runtime, pass the relative path of the folder that contains the fixed version of the WebView2 Runtime to `browserExecutableFolder`.</span></span> <span data-ttu-id="df345-137">Para criar controles WebView2 que usam a versão instalada do tempo de execução do WebView2 que existe em computadores cliente, passe uma cadeia de caracteres nula ou vazia para `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="df345-137">To create WebView2 controls that use the installed version of the WebView2 Runtime that exists on client machines, pass a null or empty string to `browserExecutableFolder`.</span></span> <span data-ttu-id="df345-138">Nesse cenário, a API tenta encontrar uma versão compatível do WebView2 Runtime instalada no computador cliente (primeiro no nível do computador e, em seguida, por usuário) usando a preferência de canal selecionada.</span><span class="sxs-lookup"><span data-stu-id="df345-138">In this scenario, the API tries to find a compatible version of the WebView2 Runtime that is installed on the client machine (first at the machine level, and then per user) using the selected channel preference.</span></span> <span data-ttu-id="df345-139">O caminho da versão corrigida do tempo de execução do WebView2 não deve conter `\Edge\Application\` .</span><span class="sxs-lookup"><span data-stu-id="df345-139">The path of fixed version of the WebView2 Runtime should not contain `\Edge\Application\`.</span></span> <span data-ttu-id="df345-140">Quando tal caminho é usado, a API falha com ERROR_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="df345-140">When such a path is used, the API will fail with ERROR_NOT_SUPPORTED.</span></span>

<span data-ttu-id="df345-141">A ordem padrão de pesquisa de canal é o tempo de execução do WebView2, beta, dev e Canárias.</span><span class="sxs-lookup"><span data-stu-id="df345-141">The default channel search order is the WebView2 Runtime, Beta, Dev, and Canary.</span></span> <span data-ttu-id="df345-142">Quando houver uma variável de ambiente WEBVIEW2_RELEASE_CHANNEL_PREFERENCE ou valor de registro releaseChannelPreference aplicável com o valor 1, a ordem de pesquisa de canal será revertida.</span><span class="sxs-lookup"><span data-stu-id="df345-142">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="df345-143">userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2.</span><span class="sxs-lookup"><span data-stu-id="df345-143">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="df345-144">O caminho pode ser um caminho de arquivo absoluto ou um caminho de arquivo relativo que é interpretado como relativo ao executável do processo atual.</span><span class="sxs-lookup"><span data-stu-id="df345-144">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="df345-145">Caso contrário, para aplicativos UWP, a pasta de dados do usuário padrão será a pasta dados do aplicativo para o pacote; para aplicativos não UWP, a pasta de dados de usuário padrão `{Executable File Name}.WebView2` será criada no mesmo diretório ao lado do executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df345-145">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="df345-146">A criação do WebView2 pode falhar se o executável estiver em execução em um diretório em que o processo não tem permissão para criar uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="df345-146">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="df345-147">O aplicativo é responsável por limpar a pasta dados do usuário quando isso é feito.</span><span class="sxs-lookup"><span data-stu-id="df345-147">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="df345-148">Observe que, como um processo de navegador pode ser compartilhado entre exibições da Web, a criação do WebView falhará com o HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) se as opções especificadas não corresponderem às opções dos webviews que estão sendo executadas no processo do navegador compartilhado.</span><span class="sxs-lookup"><span data-stu-id="df345-148">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="df345-149">environmentCreatedHandler é o resultado do manipulador para a operação assíncrona que conterá o WebView2Environment que foi criado.</span><span class="sxs-lookup"><span data-stu-id="df345-149">environmentCreatedHandler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="df345-150">O browserExecutableFolder, o userDataFolder e o additionalBrowserArguments do environmentoptions podem ser substituídos por valores especificados em variáveis de ambiente ou no registro.</span><span class="sxs-lookup"><span data-stu-id="df345-150">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="df345-151">Ao criar um WebView2Environment, as seguintes variáveis de ambiente são verificadas:</span><span class="sxs-lookup"><span data-stu-id="df345-151">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="df345-152">Se uma variável de ambiente Override for encontrada, usamos os valores browserExecutableFolder e userDataFolder como substituições para os valores correspondentes nos parâmetros CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="df345-152">If an override environment variable is found then we use the browserExecutableFolder and userDataFolder values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span> <span data-ttu-id="df345-153">Se additionalBrowserArguments especificado na variável de ambiente ou no registro, ele será acrescentado aos valores correspinding nos parâmetros CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="df345-153">If additionalBrowserArguments specified in environment variable or in the registry, it will be appended to the correspinding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="df345-154">Embora não seja estritamente substituições, existem variáveis de ambiente adicionais que podem ser definidas:</span><span class="sxs-lookup"><span data-stu-id="df345-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="df345-155">Quando encontrado com um valor não vazio, isso indica que o WebView está sendo iniciado em um depurador de script.</span><span class="sxs-lookup"><span data-stu-id="df345-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="df345-156">Nesse caso, o WebView emitirá um `Page.waitForDebugger` comando CDP que fará com que a execução do script dentro do WebView seja pausada durante a inicialização, até que um depurador emita um `Runtime.runIfWaitingForDebugger` comando CDP correspondente para continuar a execução.</span><span class="sxs-lookup"><span data-stu-id="df345-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="df345-157">Observação: não há nenhuma chave de registro equivalente a essa variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="df345-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="df345-158">Quando encontrado com um valor não vazio, isso indica que o WebView está sendo iniciado em um depurador de script que também dá suporte a aplicativos host que usam vários webviews.</span><span class="sxs-lookup"><span data-stu-id="df345-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="df345-159">O valor é usado como o identificador de um pipe nomeado que será aberto e gravado quando um novo WebView for criado pelo aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="df345-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="df345-160">A carga corresponderá à do destino JSON da porta de depuração remota e pode ser usada pelo depurador externo para ser anexada a uma instância do WebView específica.</span><span class="sxs-lookup"><span data-stu-id="df345-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="df345-161">O formato do pipe criado pelo depurador deve ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` onde:</span><span class="sxs-lookup"><span data-stu-id="df345-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="df345-162">é o nome de arquivo exe do aplicativo host, por exemplo, WebView2Example.exe</span><span class="sxs-lookup"><span data-stu-id="df345-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="df345-163">é o valor definido para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="df345-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="df345-164">Para habilitar a depuração dos destinos identificados pela JSON, você também precisará definir a variável de ambiente WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` onde:</span><span class="sxs-lookup"><span data-stu-id="df345-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="df345-165">é a porta na qual o servidor CDP será ligado.</span><span class="sxs-lookup"><span data-stu-id="df345-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="df345-166">Lembre-se de que definir as variáveis de ambiente WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER e WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS fará com que os webviews hospedados em seu aplicativo e seu conteúdo sejam expostos a aplicativos de terceiros, como depuradores.</span><span class="sxs-lookup"><span data-stu-id="df345-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="df345-167">Observação: não há nenhuma chave de registro equivalente a essa variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="df345-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="df345-168">Se nenhuma dessas variáveis de ambiente existir, o registro será examinado em seguida.</span><span class="sxs-lookup"><span data-stu-id="df345-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="df345-169">Os seguintes valores do registro são verificados:</span><span class="sxs-lookup"><span data-stu-id="df345-169">The following registry values are checked:</span></span>

```
[{Root}]\Software\Policies\Microsoft\Edge\WebView2\browserExecutableFolder
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\releaseChannelPreference
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\additionalBrowserArguments
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\userDataFolder
"{AppId}"=""
```

<span data-ttu-id="df345-170">browserExecutableFolder e releaseChannelPreference podem ser configurados usando a política de grupo em modelos administrativos > Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="df345-170">browserExecutableFolder and releaseChannelPreference can be configured using group policy under Administrative Templates > Microsoft Edge WebView2.</span></span> <span data-ttu-id="df345-171">O local do registro antigo será preterido em breve:</span><span class="sxs-lookup"><span data-stu-id="df345-171">The old registry location will be deprecated soon:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="df345-172">No cenário improvável em que algumas instâncias do WebView são abertas durante uma atualização do navegador, poderíamos acabar bloqueando a exclusão de navegadores de bordas antigas.</span><span class="sxs-lookup"><span data-stu-id="df345-172">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="df345-173">Para evitar a falta de espaço em disco, uma nova criação do WebView falhará com o próximo erro se detectar que há muitas versões antigas presentes.</span><span class="sxs-lookup"><span data-stu-id="df345-173">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="df345-174">O número máximo padrão de versões de Borda permitido é 20.</span><span class="sxs-lookup"><span data-stu-id="df345-174">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="df345-175">O número máximo de versões de borda antigas permitidas pode ser substituído pelo valor da variável de ambiente a seguir.</span><span class="sxs-lookup"><span data-stu-id="df345-175">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="df345-176">Se a WebView depender de uma borda instalada e ela for desinstalada, haverá falha na criação subsequente com o próximo erro</span><span class="sxs-lookup"><span data-stu-id="df345-176">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="df345-177">Primeiro, verificamos com root como HKLM e depois HKCU.</span><span class="sxs-lookup"><span data-stu-id="df345-177">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="df345-178">AppId é definido primeiro como a ID do modelo do usuário do aplicativo do processo do chamador e, se não houver nenhuma chave do registro correspondente, a AppId será definida como o nome do executável do processo do chamador ou, se não for uma chave do registro, ' \* '.</span><span class="sxs-lookup"><span data-stu-id="df345-178">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="df345-179">Se uma chave de substituição do registro for encontrada, usamos os valores do registro browserExecutableFolder e userDataFolder como substituições e acrescentamos valores do registro additionalBrowserArguments para os valores correspondentes nos parâmetros CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="df345-179">If an override registry key is found, then we use the browserExecutableFolder and userDataFolder registry values as replacements and append additionalBrowserArguments registry values for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="df345-180">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="df345-180">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="df345-181">Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="df345-181">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="df345-182">Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.</span><span class="sxs-lookup"><span data-stu-id="df345-182">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="df345-183">Os nomes dos canais são beta, dev e Canárias.</span><span class="sxs-lookup"><span data-stu-id="df345-183">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="df345-184">Se houver uma substituição para o browserExecutableFolder ou para a preferência de canal, a substituição será usada.</span><span class="sxs-lookup"><span data-stu-id="df345-184">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="df345-185">Se não houver uma substituição, o parâmetro passado para GetAvailableCoreWebView2BrowserVersionString será usado.</span><span class="sxs-lookup"><span data-stu-id="df345-185">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>

