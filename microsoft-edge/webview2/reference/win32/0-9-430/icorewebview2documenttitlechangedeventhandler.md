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
ms.openlocfilehash: 428bf795edbfc7df843f9d100502e65c45440412
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652534"
---
# <span data-ttu-id="80961-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="80961-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="80961-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="80961-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="80961-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="80961-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="80961-107">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="80961-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="80961-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="80961-108">Summary</span></span>

 <span data-ttu-id="80961-109">Parte</span><span class="sxs-lookup"><span data-stu-id="80961-109">Members</span></span>                        | <span data-ttu-id="80961-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="80961-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="80961-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="80961-111">Invoke</span></span>](#invoke) | <span data-ttu-id="80961-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="80961-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="80961-113">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="80961-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="80961-114">Parte</span><span class="sxs-lookup"><span data-stu-id="80961-114">Members</span></span>

#### <span data-ttu-id="80961-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="80961-115">Invoke</span></span> 

<span data-ttu-id="80961-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="80961-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="80961-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="80961-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="80961-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="80961-118">There are no event args and the args parameter will be null.</span></span>

