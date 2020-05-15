---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 5d810b4261d139eb867240a060df76126e70ade4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652753"
---
# <span data-ttu-id="6a770-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6a770-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6a770-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6a770-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6a770-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="6a770-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="6a770-107">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="6a770-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="6a770-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6a770-108">Summary</span></span>

 <span data-ttu-id="6a770-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6a770-109">Members</span></span>                        | <span data-ttu-id="6a770-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6a770-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a770-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="6a770-111">Invoke</span></span>](#invoke) | <span data-ttu-id="6a770-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a770-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6a770-113">Parte</span><span class="sxs-lookup"><span data-stu-id="6a770-113">Members</span></span>

#### <span data-ttu-id="6a770-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="6a770-114">Invoke</span></span> 

<span data-ttu-id="6a770-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a770-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6a770-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6a770-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

