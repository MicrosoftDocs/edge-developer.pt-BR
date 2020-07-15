---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878796"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

