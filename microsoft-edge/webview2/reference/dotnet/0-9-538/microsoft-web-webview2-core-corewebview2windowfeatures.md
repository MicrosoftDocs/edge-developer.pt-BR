---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879650"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures 

> [!NOTE]
> Esta é uma [API experimental](../../../concepts/versioning.md#experimental-apis) fornecida com o SDK versão [0.9.538-pré-lançamento](../../../releasenotes.md#09538).

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

