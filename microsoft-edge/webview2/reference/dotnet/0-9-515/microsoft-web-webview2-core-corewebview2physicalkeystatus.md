---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: bd63bda6b7835ff5edb30b8b1b22f877f4c96e14
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697592"
---
# Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

