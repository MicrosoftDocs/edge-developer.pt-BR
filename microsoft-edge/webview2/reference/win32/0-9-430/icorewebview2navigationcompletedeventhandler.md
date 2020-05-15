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
ms.openlocfilehash: 9a1f86bbc3f07b67cccb3c5c47fe7032bd13844e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652749"
---
# <span data-ttu-id="fdedd-104">interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fdedd-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fdedd-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="fdedd-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fdedd-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="fdedd-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="fdedd-107">O chamador implementa essa interface para receber o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="fdedd-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="fdedd-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="fdedd-108">Summary</span></span>

 <span data-ttu-id="fdedd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fdedd-109">Members</span></span>                        | <span data-ttu-id="fdedd-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="fdedd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fdedd-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="fdedd-111">Invoke</span></span>](#invoke) | <span data-ttu-id="fdedd-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="fdedd-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fdedd-113">Parte</span><span class="sxs-lookup"><span data-stu-id="fdedd-113">Members</span></span>

#### <span data-ttu-id="fdedd-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="fdedd-114">Invoke</span></span> 

<span data-ttu-id="fdedd-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="fdedd-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fdedd-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fdedd-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

