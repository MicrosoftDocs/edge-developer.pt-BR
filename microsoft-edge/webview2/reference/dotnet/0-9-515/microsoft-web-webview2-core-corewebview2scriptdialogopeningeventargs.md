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
ms.openlocfilehash: 1359e9472455acf2949cc329de4280ad970a3b68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697305"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Args de evento para o evento ScriptDialogOpening.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[DefaultText](#defaulttext) | O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.
[Tipo](#kind) | O tipo de caixa de diálogo JavaScript.
[Mensagem](#message) | A mensagem da caixa de diálogo.
[ResultText](#resulttext) | O valor de retorno da função do prompt JavaScript se Accept for chamado.
[Uri](#uri) | O URI da página que solicitou a caixa de diálogo.
[Aceitar](#accept) | O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.
[GetDeferral](#getdeferral) | Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.

## Parte

#### DefaultText 

O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.

> Cadeia de caracteres de [texto](#defaulttext) público

Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.

#### Tipo 

O tipo de caixa de diálogo JavaScript.

> [tipo](#kind) de CoreWebView2ScriptDialogKind público

Aceite, confirme, avise ou beforeunload.

#### Mensagem 

A mensagem da caixa de diálogo.

> [mensagem](#message) de cadeia de caracteres pública

Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.

#### ResultText 

O valor de retorno da função do prompt JavaScript se Accept for chamado.

> Cadeia de caracteres pública [ResultText](#resulttext)

Isso é ignorado para tipos de diálogo diferentes de prompt. Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.

#### Uri 

O URI da página que solicitou a caixa de diálogo.

> [URI](#uri) da cadeia de caracteres pública

#### Aceitar 

O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.

> [aceitação](#accept)de void público ()

Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado. E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.

#### GetDeferral 

Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.

> Public CoreWebView2Deferral [getadiamento](#getdeferral)()

Você pode usá-lo para concluir o evento mais tarde.

