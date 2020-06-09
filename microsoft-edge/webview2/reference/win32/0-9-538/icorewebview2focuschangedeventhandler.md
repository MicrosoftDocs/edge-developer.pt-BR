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
ms.openlocfilehash: 6fc29b620df5bcd265a7576e4b7ca1c7ebd73e6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698339"
---
# <span data-ttu-id="ca647-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ca647-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ca647-105">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="ca647-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="ca647-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ca647-106">Summary</span></span>

 <span data-ttu-id="ca647-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ca647-107">Members</span></span>                        | <span data-ttu-id="ca647-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ca647-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca647-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ca647-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ca647-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ca647-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ca647-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="ca647-111">There are no event args for this event.</span></span>

## <span data-ttu-id="ca647-112">Parte</span><span class="sxs-lookup"><span data-stu-id="ca647-112">Members</span></span>

#### <span data-ttu-id="ca647-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="ca647-113">Invoke</span></span> 

<span data-ttu-id="ca647-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ca647-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ca647-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ca647-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ca647-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="ca647-116">There are no event args and the args parameter will be null.</span></span>

