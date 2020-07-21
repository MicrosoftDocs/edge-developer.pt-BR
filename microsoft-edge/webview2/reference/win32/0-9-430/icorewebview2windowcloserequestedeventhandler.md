---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 98f3e114e52dd9b8a044e34e7f24067c0b68148b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884579"
---
# <span data-ttu-id="57c22-104">0.9.430-ICoreWebView2WindowCloseRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="57c22-104">0.9.430 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="57c22-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="57c22-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="57c22-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="57c22-106">Summary</span></span>

 <span data-ttu-id="57c22-107">Parte</span><span class="sxs-lookup"><span data-stu-id="57c22-107">Members</span></span>                        | <span data-ttu-id="57c22-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="57c22-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57c22-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="57c22-109">Invoke</span></span>](#invoke) | <span data-ttu-id="57c22-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="57c22-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="57c22-111">Parte</span><span class="sxs-lookup"><span data-stu-id="57c22-111">Members</span></span>

#### <span data-ttu-id="57c22-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="57c22-112">Invoke</span></span> 

<span data-ttu-id="57c22-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="57c22-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="57c22-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="57c22-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="57c22-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="57c22-115">There are no event args and the args parameter will be null.</span></span>

