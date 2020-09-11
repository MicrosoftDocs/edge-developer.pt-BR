---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: 9be4a2da9e29dec69f8cc50eef10d5f99e6c5cd4
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010870"
---
# classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

