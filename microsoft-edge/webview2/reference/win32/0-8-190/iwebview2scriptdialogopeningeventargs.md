---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885790"
---
# 0.8.355-IWebView2ScriptDialogOpeningEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Argumentos de evento para o evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | O URI da página que solicitou a caixa de diálogo.
[get_Kind](#get_kind) | O tipo de caixa de diálogo JavaScript.
[get_Message](#get_message) | A mensagem da caixa de diálogo.
[Aceitar](#accept) | O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.
[get_DefaultText](#get_defaulttext) | O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.
[get_ResultText](#get_resulttext) | O valor de retorno da função do prompt JavaScript se Accept for chamado.
[put_ResultText](#put_resulttext) | Defina a propriedade ResultText.
[GetDeferral](#getdeferral) | Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .

## Parte

#### get_Uri 

O URI da página que solicitou a caixa de diálogo.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### get_Kind 

O tipo de caixa de diálogo JavaScript.

> [get_Kind](#get_kind)público HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND * Kind)

#### get_Message 

A mensagem da caixa de diálogo.

> Public HRESULT [get_Message](#get_message)(mensagem LPWSTR *)

Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt.

#### Aceitar 

O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.

> público HRESULT [Accept](#accept)()

De JavaScript isso significa que a função Confirm retornará true se Accept for chamado. E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.

#### get_DefaultText 

O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.

> público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.

#### get_ResultText 

O valor de retorno da função do prompt JavaScript se Accept for chamado.

> público HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Isso é ignorado para tipos de diálogo diferentes de prompt. Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.

#### put_ResultText 

Defina a propriedade ResultText.

> Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)

#### GetDeferral 

Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .

> público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * adiamento)

Você pode usá-lo para concluir o evento mais tarde.

