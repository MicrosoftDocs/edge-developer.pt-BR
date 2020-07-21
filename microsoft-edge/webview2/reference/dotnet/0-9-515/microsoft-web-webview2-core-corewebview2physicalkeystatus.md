---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884586"
---
# 0.9.515-estrutura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[IsExtendedKey](#isextendedkey) | Indica se a chave é uma chave estendida.
[IsKeyReleased](#iskeyreleased) | O estado de transição.
[IsMenuKeyDown](#ismenukeydown) | O código de contexto.
[RepeatCount](#repeatcount) | A contagem de repetição para a mensagem atual.
[ScanCode](#scancode) | O código de digitalização.
[WasKeyDown](#waskeydown) | O estado de chave anterior.

Consulte a documentação do WM_KEYDOWN para obter detalhes em [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .

## Parte

#### IsExtendedKey 

Indica se a chave é uma chave estendida.

> public int [IsExtendedKey](#isextendedkey)

#### IsKeyReleased 

O estado de transição.

> public int [IsKeyReleased](#iskeyreleased)

#### IsMenuKeyDown 

O código de contexto.

> public int [IsMenuKeyDown](#ismenukeydown)

#### RepeatCount 

A contagem de repetição para a mensagem atual.

> Public uint [repeatcount](#repeatcount)

#### ScanCode 

O código de digitalização.

> Public uint [ScanCode](#scancode)

#### WasKeyDown 

O estado de chave anterior.

> public int [WasKeyDown](#waskeydown)

