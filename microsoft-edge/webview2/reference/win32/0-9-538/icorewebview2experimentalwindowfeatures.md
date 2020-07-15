---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 8b56d16e9c78738e9aa61e8c4c5b841b7fe4932f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879902"
---
# interface ICoreWebView2ExperimentalWindowFeatures 

> [!NOTE]
> Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

Recursos de janela para uma janela pop-up do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Height](#get_height) | A altura da janela.
[get_Left](#get_left) | A posição esquerda da janela. Ocorrerá se HasPosition for falso.
[get_MenuBar](#get_menubar) | Se a barra de menus deve ou não ser exibida.
[get_ScrollBars](#get_scrollbars) | Se as barras de rolagem devem ou não ser exibidas.
[get_Status](#get_status) | Se a barra de status deve ou não ser adicionada.
[get_Toolbar](#get_toolbar) | Se a barra de ferramentas do navegador deve ou não ser exibida.
[get_Top](#get_top) | A posição superior da janela. Ocorrerá se HasPosition for falso.
[get_Width](#get_width) | A largura da janela.
[HasPosition](#hasposition) | Especificou valores Left e Top.
[HasSize](#hassize) | Tem valores de altura e largura especificados.

Esses campos correspondem a ' windowFeatures ' passada para Window. Open conforme especificado na[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)

## Parte

#### get_Height 

A altura da janela.

> [get_Height](#get_height)público HRESULT (UINT32 * Height)

O valor mínimo é 100. Ocorrerá se HasSize for falso.

#### get_Left 

A posição esquerda da janela. Ocorrerá se HasPosition for falso.

> [get_Left](#get_left)público HRESULT (UINT32 * Left)

#### get_MenuBar 

Se a barra de menus deve ou não ser exibida.

> [get_MenuBar](#get_menubar)público HRESULT (bool * BarraDeMenu)

#### get_ScrollBars 

Se as barras de rolagem devem ou não ser exibidas.

> público HRESULT [get_ScrollBars](#get_scrollbars)(bool * ScrollBars)

#### get_Status 

Se a barra de status deve ou não ser adicionada.

> [get_Status](#get_status)público HRESULT (status bool *)

#### get_Toolbar 

Se a barra de ferramentas do navegador deve ou não ser exibida.

> [get_Toolbar](#get_toolbar)público HRESULT (barra de ferramentas bool *)

#### get_Top 

A posição superior da janela. Ocorrerá se HasPosition for falso.

> [get_Top](#get_top)público HRESULT (UINT32 * Top)

#### get_Width 

A largura da janela.

> público HRESULT [get_Width](#get_width)(UINT32 * Width)

O valor mínimo é 100. Ocorrerá se HasSize for falso.

#### HasPosition 

Especificou valores Left e Top.

> Public HRESULT [HasPosition](#hasposition)(bool * HasPosition)

#### HasSize 

Tem valores de altura e largura especificados.

> Public HRESULT [HasSize](#hassize)(bool * HasSize)

