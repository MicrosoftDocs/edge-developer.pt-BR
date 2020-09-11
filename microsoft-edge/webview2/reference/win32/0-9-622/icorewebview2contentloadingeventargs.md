---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 229389c6859363ef9a7c3fbf7719dbe30a061875
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011609"
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

> [get_NavigationId](#get_navigationid)público HRESULT (UINT64 * navigationid)

