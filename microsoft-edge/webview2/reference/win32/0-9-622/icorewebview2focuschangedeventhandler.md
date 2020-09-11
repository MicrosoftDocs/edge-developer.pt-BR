---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: f94e6f8323862d092bf9157061333f5e801db891
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011529"
---
# <span data-ttu-id="6e1e0-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6e1e0-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6e1e0-105">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="6e1e0-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="6e1e0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6e1e0-106">Summary</span></span>

 <span data-ttu-id="6e1e0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6e1e0-107">Members</span></span>                        | <span data-ttu-id="6e1e0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6e1e0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e1e0-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6e1e0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6e1e0-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6e1e0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6e1e0-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6e1e0-111">There are no event args for this event.</span></span>

## <span data-ttu-id="6e1e0-112">Parte</span><span class="sxs-lookup"><span data-stu-id="6e1e0-112">Members</span></span>

#### <span data-ttu-id="6e1e0-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="6e1e0-113">Invoke</span></span> 

<span data-ttu-id="6e1e0-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6e1e0-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6e1e0-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6e1e0-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="6e1e0-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="6e1e0-116">There are no event args and the args parameter will be null.</span></span>

