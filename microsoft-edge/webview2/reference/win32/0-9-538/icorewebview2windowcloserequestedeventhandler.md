---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: fcfdb3b28f4f1d1e1d1159e6664cb898613d0601
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879958"
---
# <span data-ttu-id="efdb6-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="efdb6-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="efdb6-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="efdb6-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="efdb6-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="efdb6-106">Summary</span></span>

 <span data-ttu-id="efdb6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="efdb6-107">Members</span></span>                        | <span data-ttu-id="efdb6-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="efdb6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="efdb6-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="efdb6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="efdb6-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="efdb6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="efdb6-111">Parte</span><span class="sxs-lookup"><span data-stu-id="efdb6-111">Members</span></span>

#### <span data-ttu-id="efdb6-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="efdb6-112">Invoke</span></span> 

<span data-ttu-id="efdb6-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="efdb6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="efdb6-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="efdb6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="efdb6-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="efdb6-115">There are no event args and the args parameter will be null.</span></span>

