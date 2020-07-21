---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883725"
---
# 0.9.430-ICoreWebView2NavigationCompletedEventArgs de interface 

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
[get_WebErrorStatus](#get_weberrorstatus) | O código de erro se a navegação falhar.
[get_NavigationId](#get_navigationid) | A ID da navegação.

## Parte

#### get_IsSuccess 

Verdadeiro quando a navegação é bem-sucedida.

> [get_IsSuccess](#get_issuccess)público HRESULT (bool * IsSuccess)

Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.

#### get_WebErrorStatus 

O código de erro se a navegação falhar.

> [get_WebErrorStatus](#get_weberrorstatus)público HRESULT (CORE_WEBVIEW2_WEB_ERROR_STATUS * CORE_WEBVIEW2_WEB_ERROR_STATUS)

#### get_NavigationId 

A ID da navegação.

> [get_NavigationId](#get_navigationid)público HRESULT (UINT64 * navigation_id)

