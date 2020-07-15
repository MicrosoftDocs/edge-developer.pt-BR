---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 7c10e669b4caf13f43f858e343c9bad3da155518
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878411"
---
# 0.8.355-IWebView2NavigationCompletedEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Args de evento para o evento NavigationCompleted.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | Verdadeiro quando a navegação é bem-sucedida.
[get_WebErrorStatus](#get_weberrorstatus) | O código de erro se a navegação falhar.

## Parte

#### get_IsSuccess 

Verdadeiro quando a navegação é bem-sucedida.

> [get_IsSuccess](#get_issuccess)público HRESULT (bool * IsSuccess)

Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.

#### get_WebErrorStatus 

O código de erro se a navegação falhar.

> [get_WebErrorStatus](#get_weberrorstatus)público HRESULT (WEBVIEW2_WEB_ERROR_STATUS * WEBVIEW2_WEB_ERROR_STATUS)

