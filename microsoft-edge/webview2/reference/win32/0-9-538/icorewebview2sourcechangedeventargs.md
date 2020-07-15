---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 3e622a8fb5b8ed43e5a23eaab8bd0aa61ed7d193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879398"
---
# interface ICoreWebView2SourceChangedEventArgs 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

Argumentos de evento para o evento SourceChanged.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | True se a página à qual está sendo acessada for um novo documento.

## Parte

#### get_IsNewDocument 

True se a página à qual está sendo acessada for um novo documento.

> [get_IsNewDocument](#get_isnewdocument)público HRESULT (bool * IsNewDocument)

