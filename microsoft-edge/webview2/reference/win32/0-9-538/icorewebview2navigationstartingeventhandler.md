---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: bec7596457800713eda5286c4ea1584bcfe9ed35
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011255"
---
# 0.9.579-ICoreWebView2NavigationStartingEventHandler de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber o evento NavigationStarting.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) * Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) * args)

