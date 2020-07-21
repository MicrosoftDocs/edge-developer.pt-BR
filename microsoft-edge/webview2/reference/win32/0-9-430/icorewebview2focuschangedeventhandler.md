---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: ff7c4fb51916d17df3fddc3d183fe8831029703a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884145"
---
# <span data-ttu-id="52bdb-104">0.9.430-ICoreWebView2FocusChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="52bdb-104">0.9.430 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="52bdb-105">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="52bdb-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="52bdb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="52bdb-106">Summary</span></span>

 <span data-ttu-id="52bdb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="52bdb-107">Members</span></span>                        | <span data-ttu-id="52bdb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="52bdb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52bdb-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="52bdb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="52bdb-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="52bdb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="52bdb-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="52bdb-111">There are no event args for this event.</span></span>

## <span data-ttu-id="52bdb-112">Parte</span><span class="sxs-lookup"><span data-stu-id="52bdb-112">Members</span></span>

#### <span data-ttu-id="52bdb-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="52bdb-113">Invoke</span></span> 

<span data-ttu-id="52bdb-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="52bdb-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="52bdb-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="52bdb-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="52bdb-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="52bdb-116">There are no event args and the args parameter will be null.</span></span>

