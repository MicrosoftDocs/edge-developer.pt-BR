---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698240"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Args de evento para o evento NewWindowRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Handled](#handled) | Se o NewWindowRequestedEvent é manipulado pelo host.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.
[NewWindow](#newwindow) | Obtém a nova janela.
[Uri](#uri) | O URI de destino do NewWindowRequest.
[WindowFeatures](#windowfeatures) | Recursos de janela especificados pela chamada Window. Open.
[GetDeferral](#getdeferral) | Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.

O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)

## Parte

#### Handled 

Se o NewWindowRequestedEvent é manipulado pelo host.

> bool público [manipulado](#handled)

Se for falso e não houver um NewWindow definido, o WebView abrirá uma janela pop-up e ele será retornado como WindowProxy aberto. Se definido como verdadeiro e não houver NewWindow definido para uma chamada Window. Open, o WindowProxy aberto será para um objeto de janela fictício e nenhuma janela será carregada. O padrão é falso.

#### IsUserInitiated 

IsUserInitiated é verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, por exemplo, clicar em uma marca de âncora com destino.

> Public bool [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Obtém a nova janela.

> CoreWebView2 de [NewWindow](#newwindow) público

#### Uri 

O URI de destino do NewWindowRequest.

> [URI](#uri) da cadeia de caracteres pública

O WebView de destino não deve ser navegado. Se NewWindow estiver definido, sua janela de nível superior retornará como o WindowProxy aberto.

#### WindowFeatures 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Recursos de janela especificados pela chamada Window. Open.

> CoreWebView2WindowFeatures público [WindowFeatures](#windowfeatures)

Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.

#### GetDeferral 

Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.

> Public CoreWebView2Deferral [getadiamento](#getdeferral)()

Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de abertura de janela posteriormente. Embora esse evento seja adiado, a janela aberta será retornada um WindowProxy para uma janela não navegada, que navegará quando o adiamento estiver concluído.

