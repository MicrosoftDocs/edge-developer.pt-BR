---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: 906b09ad99d6d6d9e74c52c0582584b9e46f74ba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010534"
---
# 0.9.579-ICoreWebView2ContentLoadingEventHandler de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber o evento ContentLoading.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) * WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) * args)

