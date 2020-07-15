---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 798c3ce0a3eeddad651668124d6a263d0672a391
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877837"
---
# 0.9.430-ICoreWebView2NewWindowRequestedEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento NewWindowRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | O URI de destino do NewWindowRequest.
[put_NewWindow](#put_newwindow) | Define uma WebView como resultado da NewWindowRequest.
[get_NewWindow](#get_newwindow) | Obtém a nova janela.
[put_Handled](#put_handled) | Define se o NewWindowRequestedEvent é manipulado pelo host.
[get_Handled](#get_handled) | Obtém se a NewWindowRequestedEvent é manipulada pelo host.
[get_IsUserInitiated](#get_isuserinitiated) | IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.
[GetDeferral](#getdeferral) | Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.

O evento é acionado quando o conteúdo de WebView solicitado para abrir uma nova janela (por meio de Window. Open () etc.)

## Parte

#### get_Uri 

O URI de destino do NewWindowRequest.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### put_NewWindow 

Define uma WebView como resultado da NewWindowRequest.

> público HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) * NewWindow)

O WebView de destino não deve ser navegado. Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.

#### get_NewWindow 

Obtém a nova janela.

> público HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) * * NewWindow)

#### put_Handled 

Define se o NewWindowRequestedEvent é manipulado pelo host.

> [put_Handled](#put_handled)público HRESULT (bool manipulado)

Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto. Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada. O padrão é falso.

#### get_Handled 

Obtém se a NewWindowRequestedEvent é manipulada pelo host.

> [get_Handled](#get_handled)público HRESULT (bool * manipulado)

#### get_IsUserInitiated 

IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.

> [get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool * IsUserInitiated)

#### GetDeferral 

Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.

> público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * adiamento)

Você pode usar o objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para concluir a solicitação de abertura de janela posteriormente. Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.

