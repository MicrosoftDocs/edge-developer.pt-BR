---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 17ed4a578234a056a7e6ff347829a12e39fa93bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010919"
---
# 0.9.579-estrutura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus 

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

