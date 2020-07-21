---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 237179df5ef704fb88516780696f3a9c10c9a198
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884663"
---
# <span data-ttu-id="c220d-104">0.8.355-IWebView2ZoomFactorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="c220d-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c220d-105">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="c220d-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="c220d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c220d-106">Summary</span></span>

 <span data-ttu-id="c220d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c220d-107">Members</span></span>                        | <span data-ttu-id="c220d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c220d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c220d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c220d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c220d-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c220d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c220d-111">Use a propriedade IWebView2WebView. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="c220d-111">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="c220d-112">Parte</span><span class="sxs-lookup"><span data-stu-id="c220d-112">Members</span></span>

#### <span data-ttu-id="c220d-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="c220d-113">Invoke</span></span> 

<span data-ttu-id="c220d-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c220d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c220d-115">[chamada](#invoke)a Public HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c220d-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="c220d-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="c220d-116">There are no event args and the args parameter will be null.</span></span>

