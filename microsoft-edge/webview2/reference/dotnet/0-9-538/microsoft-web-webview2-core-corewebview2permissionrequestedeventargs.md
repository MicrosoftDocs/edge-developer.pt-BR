---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 58d87d1815b81969c4424eacfcec26ffe425192e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698239"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Args de evento para o evento PermissionRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.
[PermissionKind](#permissionkind) | O tipo da permissão que é solicitada.
[Estado](#state) | O status de uma solicitação de permissão, ou seja,
[Uri](#uri) | A origem do conteúdo da Web que solicita a permissão.
[GetDeferral](#getdeferral) | Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.

## Parte

#### IsUserInitiated 

Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.

> Public bool [IsUserInitiated](#isuserinitiated)

Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.

#### PermissionKind 

O tipo da permissão que é solicitada.

> CoreWebView2PermissionKind público [PermissionKind](#permissionkind)

#### Estado 

O status de uma solicitação de permissão, ou seja,

> [estado](#state) CoreWebView2PermissionState público

se a solicitação é concedida.

O valor padrão é CoreWebView2PermissionState. default.

#### Uri 

A origem do conteúdo da Web que solicita a permissão.

> [URI](#uri) da cadeia de caracteres pública

#### GetDeferral 

Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.

> Public CoreWebView2Deferral [getadiamento](#getdeferral)()

O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.

