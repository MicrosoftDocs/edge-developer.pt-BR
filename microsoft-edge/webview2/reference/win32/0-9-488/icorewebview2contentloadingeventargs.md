---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652630"
---
# interface ICoreWebView2ContentLoadingEventArgs 

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

