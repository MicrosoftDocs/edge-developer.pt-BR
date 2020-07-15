---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: fc952437a9d5ffa7bb709bb6fb322438851babcd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879895"
---
# <span data-ttu-id="b68c5-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b68c5-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b68c5-105">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="b68c5-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="b68c5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b68c5-106">Summary</span></span>

 <span data-ttu-id="b68c5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b68c5-107">Members</span></span>                        | <span data-ttu-id="b68c5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b68c5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b68c5-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b68c5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b68c5-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b68c5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b68c5-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="b68c5-111">There are no event args for this event.</span></span>

## <span data-ttu-id="b68c5-112">Parte</span><span class="sxs-lookup"><span data-stu-id="b68c5-112">Members</span></span>

#### <span data-ttu-id="b68c5-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="b68c5-113">Invoke</span></span> 

<span data-ttu-id="b68c5-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b68c5-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b68c5-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b68c5-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="b68c5-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="b68c5-116">There are no event args and the args parameter will be null.</span></span>

