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
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Isso representa o ambiente WebView2.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.
[CompareBrowserVersions](#comparebrowserversions) | Compare as versões do navegador corretamente para determinar qual é a versão mais recente, antiga ou mesma.
[CreateAsync](#createasync) | Cria um ambiente WebView2 verde usando a versão de Borda instalada.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Crie assincronamente um novo WebView para uso com hospedagem Visual.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Criar de forma assíncrona um novo WebView.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Crie uma CoreWebView2ExperimentalPointerInfo vazia.
[CreateWebResourceResponse](#createwebresourceresponse) | Crie um novo objeto de resposta de recurso da Web.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.
[GetProviderForHwnd](#getproviderforhwnd) | Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.

Webviews criados a partir de um ambiente são executados no processo do navegador especificado com parâmetros de ambiente, e os objetos criados a partir de um ambiente devem ser usados no mesmo ambiente. Não é garantido que o uso em ambientes diferentes seja compatível e possa falhar.

## Parte

#### BrowserVersionString 

As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.

> Cadeia de caracteres pública [BrowserVersionString](#browserversionstring)

Isso corresponde ao formato da API GetAvailableCoreWebView2BrowserVersionString. Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.

#### NewBrowserVersionAvailable 

O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.

> objeto<-EventHandler de evento público > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Para usar a versão mais recente do navegador, você deve criar um novo ambiente e WebView. Esse evento só será acionado para uma nova versão do mesmo canal de borda em que o código está sendo executado. Quando não estiver sendo executado com a borda instalada, nenhum evento será acionado.

Como uma pasta de dados do usuário só pode ser usada por um processo de navegador por vez, se você quiser usar a mesma pasta de dados do usuário no webviews usando a nova versão do navegador, será necessário fechar o ambiente e os webviews que estão usando a versão mais antiga do navegador primeiro. Ou simplesmente solicitar que o usuário reinicie o aplicativo.

#### CompareBrowserVersions 

Compare as versões do navegador corretamente para determinar qual é a versão mais recente, antiga ou mesma.

> public static int [CompareBrowserVersions](#comparebrowserversions)(String Version1, String Version2)

Retorna-1, 0 ou 1 dependendo se Version1 é menor que, igual a ou maior que Version2, respectivamente.

##### Parâmetros
* `version1` Uma das cadeias de caracteres da versão a comparar. 

* `version2` A outra cadeia de caracteres de versão a comparar.

#### CreateAsync 

Cria um ambiente WebView2 verde usando a versão de Borda instalada.

> tarefa assíncrona estática pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(cadeia de caracteres browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions opções)

##### Parâmetros
* `browserExecutableFolder` O caminho relativo para a pasta que contém a borda incorporada. 

* `userDataFolder` userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2. 

* `options` Opções usadas para criar o ambiente WebView2.

#### CreateCoreWebView2CompositionControllerAsync 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Crie assincronamente um novo WebView para uso com hospedagem Visual.

> tarefas assíncronas públicas< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)

parentWindow é o HWND no qual o aplicativo conectará a árvore visual do WebView. Esse será o HWND que o aplicativo receberá a entrada de ponteiro/mouse para o WebView (e será necessário usar SendMouseInput/SendPointerInput para encaminhar). Se o aplicativo mover a árvore visual da WebView para abaixo de uma janela diferente, então precisará definir CoreWebView2CompositionController. ParentWindow para atualizar o novo HWND pai da árvore visual.

Defina a propriedade RootVisualTarget no CoreWebView2CompositionController criado para fornecer um Visual para hospedar a árvore visual do navegador.

É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo. Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.

#### CreateCoreWebView2ControllerAsync 

Criar de forma assíncrona um novo WebView.

> tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada. O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView. A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.

É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo. Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.

#### CreateCoreWebView2PointerInfo 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Crie uma CoreWebView2ExperimentalPointerInfo vazia.

> Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()

O CoreWebView2ExperimentalPointerInfo retornado precisa ser preenchido com todas as informações relevantes antes de chamar SendPointerInput.

#### CreateWebResourceResponse 

Crie um novo objeto de resposta de recurso da Web.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)

Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha. Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha. Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.

#### GetAvailableBrowserVersionString 

Obtenha as informações da versão do navegador, incluindo o nome do canal, se não for o canal estável ou a borda incorporada.

> Cadeia de caracteres de cadeia estática [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(cadeia de caracteres browserExecutableFolder)

##### Parâmetros
* `browserExecutableFolder` O caminho relativo para a pasta que contém a borda incorporada.

#### GetProviderForHwnd 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Retorna o provedor de automação da interface do usuário para o CoreWebView2CompositionController que corresponde ao HWND fornecido.

> [GetProviderForHwnd](#getproviderforhwnd)de objeto público (IntPtr HWND)

