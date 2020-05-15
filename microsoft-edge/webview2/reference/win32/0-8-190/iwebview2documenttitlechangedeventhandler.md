---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 69d8f410c7d9e7c4a8b1dc526babf535a372048f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652588"
---
# <span data-ttu-id="cfead-104">interface IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="cfead-104">interface IWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="cfead-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="cfead-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="cfead-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="cfead-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="cfead-107">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="cfead-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="cfead-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="cfead-108">Summary</span></span>

 <span data-ttu-id="cfead-109">Parte</span><span class="sxs-lookup"><span data-stu-id="cfead-109">Members</span></span>                        | <span data-ttu-id="cfead-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="cfead-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cfead-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="cfead-111">Invoke</span></span>](#invoke) | <span data-ttu-id="cfead-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="cfead-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="cfead-113">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="cfead-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="cfead-114">Parte</span><span class="sxs-lookup"><span data-stu-id="cfead-114">Members</span></span>

#### <span data-ttu-id="cfead-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="cfead-115">Invoke</span></span> 

<span data-ttu-id="cfead-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="cfead-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="cfead-117">[chamada](#invoke)a Public HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="cfead-117">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="cfead-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="cfead-118">There are no event args and the args parameter will be null.</span></span>

