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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698378"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Recursos de janela para uma janela pop-up do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Comprimento](#height) | A altura da janela.
[Esquerda](#left) | A posição esquerda da janela.
[Menus](#menubar) | Se a barra de menus deve ou não ser exibida.
[Barras](#scrollbars) | Se as barras de rolagem devem ou não ser exibidas.
[Status](#status) | Se a barra de status deve ou não ser adicionada.
[Barra de ferramentas](#toolbar) | Se a barra de ferramentas do navegador deve ou não ser exibida.
[Superior](#top) | A posição superior da janela.
[Largura](#width) | A largura da janela.
[HasPosition](#hasposition) | Especificou valores Left e Top.
[HasSize](#hassize) | Tem valores de altura e largura especificados.

## Parte

#### Comprimento 

A altura da janela.

> [altura](#height) do uint público

#### Esquerda 

A posição esquerda da janela.

> público uint [esquerdo](#left)

Ocorrerá se HasPosition for falso.

#### Menus 

Se a barra de menus deve ou não ser exibida.

> [menus](#menubar) int público

#### Barras 

Se as barras de rolagem devem ou não ser exibidas.

> Barras de [rolagem](#scrollbars) públicas de int

#### Status 

Se a barra de status deve ou não ser adicionada.

> [status](#status) de int público

#### Barra de ferramentas 

Se a barra de ferramentas do navegador deve ou não ser exibida.

> Barra de [ferramentas](#toolbar) público int

#### Superior 

A posição superior da janela.

> pública uint [superior](#top)

Ocorrerá se HasPosition for falso.

#### Largura 

A largura da janela.

> [largura](#width) do uint público

#### HasPosition 

Especificou valores Left e Top.

> public int [HasPosition](#hasposition)()

#### HasSize 

Tem valores de altura e largura especificados.

> public int [HasSize](#hassize)()

