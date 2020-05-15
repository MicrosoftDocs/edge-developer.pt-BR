---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: be8f475d4c1a886a92b46144f2bffde2d49dc9d4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652663"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2Environment 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Isso representa o ambiente WebView2.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | As informações de versão do navegador do CoreWebView2Environment atual, incluindo o nome do canal, se não for o canal estável.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | O evento NewBrowserVersionAvailable é acionado quando uma versão mais recente do navegador do Edge é instalada e está disponível para uso pelo WebView2.
[CreateAsync](#createasync) | Cria um ambiente WebView2 verde usando a versão de Borda instalada.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Criar de forma assíncrona um novo WebView.
[CreateWebResourceResponse](#createwebresourceresponse) | Crie um novo objeto de resposta de recurso da Web.

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

#### CreateAsync 

Cria um ambiente WebView2 verde usando a versão de Borda instalada.

> tarefas assíncronas públicas< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [createasync](#createasync)(cadeia de caracteres browserExecutableFolder, Cadeia de caracteres userDataFolder, opções de CoreWebView2EnvironmentOptions)

##### Parâmetros
* `browserExecutableFolder` O caminho relativo para a pasta que contém a borda incorporada. 

* `userDataFolder` userDataFolder pode ser especificado para alterar o local da pasta de dados do usuário padrão para WebView2. 

* `options` Opções usadas para criar o ambiente WebView2.

#### CreateCoreWebView2ControllerAsync 

Criar de forma assíncrona um novo WebView.

> tarefas assíncronas públicas< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

parentWindow é o HWND no qual a WebView deve ser exibida e da qual receber a entrada. O WebView irá adicionar uma janela filho à janela fornecida durante a criação do WebView. A ordem Z e outras coisas afetadas pela ordem das janelas irmãs serão afetadas de acordo com isso.

É recomendável que o aplicativo defina a ID do modelo do usuário do aplicativo para o processo ou a janela do aplicativo. Se nenhum for definido, durante a criação do WebView, uma ID do modelo do usuário do aplicativo gerado será definida como a janela raiz do parentWindow.

#### CreateWebResourceResponse 

Crie um novo objeto de resposta de recurso da Web.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(conteúdo Stream, defaultstatuscode, String ReasonPhrase, cabeçalhos de cadeia de caracteres)

Os cabeçalhos são a cadeia de caracteres de cabeçalho de resposta bruta delimitada pela nova linha. Também é possível criar esse objeto com uma cadeia de caracteres de cabeçalhos vazia e usar o CoreWebView2HttpResponseHeaders para construir os cabeçalhos linha por linha. Para obter informações sobre outros parâmetros, consulte CoreWebView2WebResourceResponse.
