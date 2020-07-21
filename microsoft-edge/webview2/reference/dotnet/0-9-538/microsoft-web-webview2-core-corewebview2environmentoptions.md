---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
ms.openlocfilehash: 705e030caba03227749002bad8c9777197839a28
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885559"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Opções usadas para criar o ambiente WebView2.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[AdditionalBrowserArguments](#additionalbrowserarguments) | AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.
[IsSingleSignOnUsingOSPrimaryAccountEnabled](#issinglesignonusingosprimaryaccountenabled) | A propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.
[Idioma](#language) | O idioma padrão com o qual o WebView será executado.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.
[CoreWebView2EnvironmentOptions](#corewebview2environmentoptions) | Inicializa uma nova instância da classe CoreWebView2EnvironmentOptions.

Uma implementação padrão é fornecida em WebView2EnvironmentOptions. h.

## Parte

#### AdditionalBrowserArguments 

AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.

> Cadeia de caracteres pública [AdditionalBrowserArguments](#additionalbrowserarguments)

Eles serão passados para o processo do navegador como parte da linha de comando. Consulte [executar Chromium com sinalizadores](https://aka.ms/RunChromiumWithFlags) para obter mais informações sobre as opções de linha de comando para o processo do navegador. Se o aplicativo for iniciado com uma linha de comando Alternar `--edge-webview-switches=xxx` o valor dessa opção (xxx no exemplo acima) também será acrescentado à linha de comando do processo do navegador. Determinadas opções `--user-data-dir` , como são internas e importantes para o WebView. Essas opções serão ignoradas, mesmo que especificado. Se as mesmas opções forem especificadas várias vezes, o último WINS. Não há nenhuma tentativa de mesclar os valores diferentes da mesma opção, exceto para recursos desabilitados e habilitados. Os recursos especificados por `--enable-features` e `--disable-features` serão mesclados com uma lógica simples: os recursos serão a União dos recursos e recursos internos especificados e, se um recurso estiver desabilitado, ele será removido da lista de recursos habilitados. O valor da linha de comando do processo de aplicativo é `--edge-webview-switches` processado após o parâmetro additionalBrowserArguments ser processado. Certos recursos são desabilitados internamente e não podem ser habilitados. Se a análise falhar para as opções especificadas, elas serão ignoradas. Padrão é executar o processo do navegador sem sinalizadores extras.

#### IsSingleSignOnUsingOSPrimaryAccountEnabled 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

A propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.

> Public bool [IsSingleSignOnUsingOSPrimaryAccountEnabled](#issinglesignonusingosprimaryaccountenabled)

O padrão é desabilitado. Os aplicativos da plataforma universal do Windows também devem declarar o [recurso restrito](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO para que o logon único funcione.

#### Idioma 

O idioma padrão com o qual o WebView será executado.

> [linguagem](#language) de cadeia de caracteres pública

Ele se aplica a UIs do navegador, como menus de contexto e caixas de diálogo. Ele também se aplica ao cabeçalho HTTP Accept-Languages que o WebView envia para sites da Web. Ele está no formato de `language[-country]` onde `language` está o código de duas letras da ISO 639 e `country` é o código de duas letras da ISO 3166.

#### TargetCompatibleBrowserVersion 

A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.

> Cadeia de caracteres pública [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)

Esse padrão é o Edge WebView2 versão do tempo de execução que corresponde à versão do SDK que o aplicativo está usando. O formato desse valor é o mesmo que o formato da propriedade BrowserVersionString e outros valores BrowserVersion. Somente a parte de versão do valor BrowserVersion é respeitada. O sufixo do canal, se existir, será ignorado. A versão do Edge WebView2 os binários do tempo de execução realmente usados podem ser diferentes do TargetCompatibleBrowserVersion especificado. Eles são garantidos apenas como compatíveis. Você pode verificar a versão real na propriedade BrowserVersionString no CoreWebView2Environment.

#### CoreWebView2EnvironmentOptions 

Inicializa uma nova instância da classe CoreWebView2EnvironmentOptions.

> Public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(cadeia de caracteres additionalBrowserArguments, linguagem de cadeia de caracteres, targetCompatibleBrowserVersion de cadeia de caracteres)

##### Parâmetros
* `additionalBrowserArguments` AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView. 

* `language` O idioma padrão com o qual o WebView será executado. 

* `targetCompatibleBrowserVersion` A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.

