---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2PermissionRequestedEventHandler
ms.openlocfilehash: 549c7bf780535a889529aa8f7e87a097cae88c3a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879419"
---
# <span data-ttu-id="c8d4f-104">interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c8d4f-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c8d4f-105">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="c8d4f-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="c8d4f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c8d4f-106">Summary</span></span>

 <span data-ttu-id="c8d4f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c8d4f-107">Members</span></span>                        | <span data-ttu-id="c8d4f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c8d4f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c8d4f-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c8d4f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c8d4f-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c8d4f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c8d4f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c8d4f-111">Members</span></span>

#### <span data-ttu-id="c8d4f-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="c8d4f-112">Invoke</span></span> 

<span data-ttu-id="c8d4f-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c8d4f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c8d4f-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c8d4f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

