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
# Globais 

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[CompareBrowserVersions](#comparebrowserversions) | Esse método é para que qualquer pessoa queira comparar a versão corretamente para determinar qual é a versão mais recente, mais antiga ou mesma.
[CreateCoreWebView2Environment](#createcorewebview2environment) | Cria um ambiente WebView2 verde usando a versão de Borda instalada.
[CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions) | DLL Export para criar um ambiente WebView2 com uma versão personalizada do Edge, diretório de dados do usuário e/ou opções adicionais.
[GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring) | Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.

## Parte

#### CompareBrowserVersions 

> Public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int * resultado)

Esse método é para que qualquer pessoa queira comparar a versão corretamente para determinar qual é a versão mais recente, mais antiga ou mesma.

Ele pode ser usado para determinar se você deve usar o webview2 ou determinada base de recursos na versão. Define o valor do resultado para-1, 0 ou 1 se Version1 for menor que, igual ou maior do que Version2, respectivamente. Retorna E_INVALIDARG se não conseguir analisar nenhuma cadeia de caracteres de versão ou se qualquer parâmetro de entrada for nulo. A entrada pode usar diretamente o versionInfo obtido do GetAvailableCoreWebView2BrowserVersionString, as informações do canal serão ignoradas.

#### CreateCoreWebView2Environment 

> Public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler * environmentCreatedHandler)

Cria um ambiente WebView2 verde usando a versão de Borda instalada.

Isso equivale a chamar CreateCoreWebView2EnvironmentWithOptions com nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments. Consulte CreateCoreWebView2EnvironmentWithOptions para obter mais detalhes.

#### CreateCoreWebView2EnvironmentWithOptions 

> Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) * environmentoptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environmentCreatedHandler)

DLL Export para criar um ambiente WebView2 com uma versão personalizada do Edge, diretório de dados do usuário e/ou opções adicionais.

O ambiente WebView2 e todos os outros objetos WebView2 são únicos threads e têm dependências em componentes do Windows que exigem que o COM seja inicializado para um apartamento de thread único. Espera-se que o aplicativo chame CoInitializeEx antes de chamar CreateCoreWebView2EnvironmentWithOptions.

```
CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED);
```

Se CoInitializeEx não for chamado ou tiver sido chamado anteriormente com COINIT_MULTITHREADED, o CreateCoreWebView2EnvironmentWithOptions falhará com um dos seguintes erros.

```
CO_E_NOTINITIALIZED (if CoInitializeEx was not called)
RPC_E_CHANGED_MODE  (if CoInitializeEx was previously called with
                     COINIT_MULTITHREADED)
```

Use `browserExecutableFolder` para especificar se os controles WebView2 usam uma versão fixa ou instalada do tempo de execução do WebView2 que existe em um computador cliente. Para usar uma versão fixa do tempo de execução do WebView2, passe o caminho relativo da pasta que contém a versão fixa do tempo de execução do WebView2 `browserExecutableFolder` . Para criar controles WebView2 que usam a versão instalada do tempo de execução do WebView2 que existe em computadores cliente, passe uma cadeia de caracteres nula ou vazia para `browserExecutableFolder` . Nesse cenário, a API tenta encontrar uma versão compatível do WebView2 Runtime instalada no computador cliente (primeiro no nível do computador e, em seguida, por usuário) usando a preferência de canal selecionada. O caminho da versão corrigida do tempo de execução do WebView2 não deve conter `\Edge\Application\` . Quando tal caminho é usado, a API falha com ERROR_NOT_SUPPORTED.

A ordem padrão de pesquisa de canal é o tempo de execução do WebView2, beta, dev e Canárias. Quando houver uma variável de ambiente WEBVIEW2_RELEASE_CHANNEL_PREFERENCE ou valor de registro releaseChannelPreference aplicável com o valor 1, a ordem de pesquisa de canal será revertida.

userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2. O caminho pode ser um caminho de arquivo absoluto ou um caminho de arquivo relativo que é interpretado como relativo ao executável do processo atual. Caso contrário, para aplicativos UWP, a pasta de dados do usuário padrão será a pasta dados do aplicativo para o pacote; para aplicativos não UWP, a pasta de dados de usuário padrão `{Executable File Name}.WebView2` será criada no mesmo diretório ao lado do executável do aplicativo. A criação do WebView2 pode falhar se o executável estiver em execução em um diretório em que o processo não tem permissão para criar uma nova pasta. O aplicativo é responsável por limpar a pasta dados do usuário quando isso é feito.

Observe que, como um processo de navegador pode ser compartilhado entre exibições da Web, a criação do WebView falhará com o HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) se as opções especificadas não corresponderem às opções dos webviews que estão sendo executadas no processo do navegador compartilhado.

environmentCreatedHandler é o resultado do manipulador para a operação assíncrona que conterá o WebView2Environment que foi criado.

O browserExecutableFolder, o userDataFolder e o additionalBrowserArguments do environmentoptions podem ser substituídos por valores especificados em variáveis de ambiente ou no registro.

Ao criar um WebView2Environment, as seguintes variáveis de ambiente são verificadas:

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

Se uma variável de ambiente Override for encontrada, usamos os valores browserExecutableFolder e userDataFolder como substituições para os valores correspondentes nos parâmetros CreateCoreWebView2EnvironmentWithOptions. Se additionalBrowserArguments especificado na variável de ambiente ou no registro, ele será acrescentado aos valores correspinding nos parâmetros CreateCoreWebView2EnvironmentWithOptions.

Embora não seja estritamente substituições, existem variáveis de ambiente adicionais que podem ser definidas:

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Quando encontrado com um valor não vazio, isso indica que o WebView está sendo iniciado em um depurador de script. Nesse caso, o WebView emitirá um `Page.waitForDebugger` comando CDP que fará com que a execução do script dentro do WebView seja pausada durante a inicialização, até que um depurador emita um `Runtime.runIfWaitingForDebugger` comando CDP correspondente para continuar a execução. Observação: não há nenhuma chave de registro equivalente a essa variável de ambiente.

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Quando encontrado com um valor não vazio, isso indica que o WebView está sendo iniciado em um depurador de script que também dá suporte a aplicativos host que usam vários webviews. O valor é usado como o identificador de um pipe nomeado que será aberto e gravado quando um novo WebView for criado pelo aplicativo host. A carga corresponderá à do destino JSON da porta de depuração remota e pode ser usada pelo depurador externo para ser anexada a uma instância do WebView específica. O formato do pipe criado pelo depurador deve ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` onde:

* `{app_name}` é o nome de arquivo exe do aplicativo host, por exemplo, WebView2Example.exe

* `{pipe_name}` é o valor definido para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Para habilitar a depuração dos destinos identificados pela JSON, você também precisará definir a variável de ambiente WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` onde:

* `{port_num}` é a porta na qual o servidor CDP será ligado.

Lembre-se de que definir as variáveis de ambiente WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER e WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS fará com que os webviews hospedados em seu aplicativo e seu conteúdo sejam expostos a aplicativos de terceiros, como depuradores.

Observação: não há nenhuma chave de registro equivalente a essa variável de ambiente.

Se nenhuma dessas variáveis de ambiente existir, o registro será examinado em seguida. Os seguintes valores do registro são verificados:

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

browserExecutableFolder e releaseChannelPreference podem ser configurados usando a política de grupo em modelos administrativos > Microsoft Edge WebView2. O local do registro antigo será preterido em breve:

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

No cenário improvável em que algumas instâncias do WebView são abertas durante uma atualização do navegador, poderíamos acabar bloqueando a exclusão de navegadores de bordas antigas. Para evitar a falta de espaço em disco, uma nova criação do WebView falhará com o próximo erro se detectar que há muitas versões antigas presentes.

```
ERROR_DISK_FULL
```

O número máximo padrão de versões de Borda permitido é 20.

O número máximo de versões de borda antigas permitidas pode ser substituído pelo valor da variável de ambiente a seguir.

```
WEBVIEW2_MAX_INSTANCES
```

Se a WebView depender de uma borda instalada e ela for desinstalada, haverá falha na criação subsequente com o próximo erro

```
ERROR_PRODUCT_UNINSTALLED
```

Primeiro, verificamos com root como HKLM e depois HKCU. AppId é definido primeiro como a ID do modelo do usuário do aplicativo do processo do chamador e, se não houver nenhuma chave do registro correspondente, a AppId será definida como o nome do executável do processo do chamador ou, se não for uma chave do registro, ' * '. Se uma chave de substituição do registro for encontrada, usamos os valores do registro browserExecutableFolder e userDataFolder como substituições e acrescentamos valores do registro additionalBrowserArguments para os valores correspondentes nos parâmetros CreateCoreWebView2EnvironmentWithOptions.

#### GetAvailableCoreWebView2BrowserVersionString 

> Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr * versionInfo)

Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.

Os nomes dos canais são beta, dev e Canárias. Se houver uma substituição para o browserExecutableFolder ou para a preferência de canal, a substituição será usada. Se não houver uma substituição, o parâmetro passado para GetAvailableCoreWebView2BrowserVersionString será usado.

