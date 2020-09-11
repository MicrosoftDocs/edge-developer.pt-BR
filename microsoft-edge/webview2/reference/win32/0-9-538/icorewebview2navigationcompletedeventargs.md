---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: 482137fd0ffa10c60381d5b0f3dc3d7db6f9fdf7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011290"
---
# 0.9.579-ICoreWebView2NavigationCompletedEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Args de evento para o evento NavigationCompleted.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | Verdadeiro quando a navegação é bem-sucedida.
[get_NavigationId](#get_navigationid) | A ID da navegação.
[get_WebErrorStatus](#get_weberrorstatus) | O código de erro se a navegação falhar.

## Parte

#### get_IsSuccess 

Verdadeiro quando a navegação é bem-sucedida.

> [get_IsSuccess](#get_issuccess)público HRESULT (bool * IsSuccess)

Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.

#### get_NavigationId 

A ID da navegação.

> [get_NavigationId](#get_navigationid)público HRESULT (UINT64 * navigation_id)

#### get_WebErrorStatus 

O código de erro se a navegação falhar.

> [get_WebErrorStatus](#get_weberrorstatus)público HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS * COREWEBVIEW2_WEB_ERROR_STATUS)

