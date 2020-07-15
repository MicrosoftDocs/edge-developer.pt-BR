---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: a5dd8dc0b504faad7c02669ae464ca1ef75c88af
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880777"
---
# 0.9.515-ICoreWebView2ContentLoadingEventArgs de interface 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Args de evento para o evento ContentLoading.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | Verdadeiro se o conteúdo carregado for uma página de erro.
[get_NavigationId](#get_navigationid) | A ID da navegação.

## Parte

#### get_IsErrorPage 

Verdadeiro se o conteúdo carregado for uma página de erro.

> [get_IsErrorPage](#get_iserrorpage)público HRESULT (bool * IsErrorPage)

#### get_NavigationId 

A ID da navegação.

> [get_NavigationId](#get_navigationid)público HRESULT (UINT64 * navigation_id)

