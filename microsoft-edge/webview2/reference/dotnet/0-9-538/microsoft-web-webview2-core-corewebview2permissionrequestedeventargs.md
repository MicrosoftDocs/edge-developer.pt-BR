---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 2ad85879ccf69ccecef355ea07d311cc5a23de11
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010926"
---
# classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

