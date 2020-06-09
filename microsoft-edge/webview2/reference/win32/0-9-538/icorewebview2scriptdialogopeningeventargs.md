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
ms.openlocfilehash: 94a008af5a66109add56cec7fd0969d4e20d8ca8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698385"
---
# interface ICoreWebView2ScriptDialogOpeningEventArgs 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

Args de evento para o evento ScriptDialogOpening.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Aceitar](#accept) | O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.
[get_DefaultText](#get_defaulttext) | O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.
[get_Kind](#get_kind) | O tipo de caixa de diálogo JavaScript.
[get_Message](#get_message) | A mensagem da caixa de diálogo.
[get_ResultText](#get_resulttext) | O valor de retorno da função do prompt JavaScript se Accept for chamado.
[get_Uri](#get_uri) | O URI da página que solicitou a caixa de diálogo.
[GetDeferral](#getdeferral) | Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .
[put_ResultText](#put_resulttext) | Defina a propriedade ResultText.

## Parte

#### Aceitar 

O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.

> público HRESULT [Accept](#accept)()

Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado. E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.

#### get_DefaultText 

O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.

> público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR * DefaultText)

Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.

#### get_Kind 

O tipo de caixa de diálogo JavaScript.

> [get_Kind](#get_kind)público HRESULT (COREWEBVIEW2_SCRIPT_DIALOG_KIND * Kind)

Aceite, confirme, avise ou beforeunload.

#### get_Message 

A mensagem da caixa de diálogo.

> Public HRESULT [get_Message](#get_message)(mensagem LPWSTR *)

Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.

#### get_ResultText 

O valor de retorno da função do prompt JavaScript se Accept for chamado.

> público HRESULT [get_ResultText](#get_resulttext)(LPWSTR * ResultText)

Isso é ignorado para tipos de diálogo diferentes de prompt. Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.

#### get_Uri 

O URI da página que solicitou a caixa de diálogo.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### GetDeferral 

Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .

> público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * adiamento)

Você pode usá-lo para concluir o evento mais tarde.

#### put_ResultText 

Defina a propriedade ResultText.

> Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)

