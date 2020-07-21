---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 91cd4245ff6c75e72457410211deefd9ab7f09d1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883690"
---
# <span data-ttu-id="3b5f5-104">0.9.515-ICoreWebView2ZoomFactorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="3b5f5-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3b5f5-105">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="3b5f5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3b5f5-106">Summary</span></span>

 <span data-ttu-id="3b5f5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3b5f5-107">Members</span></span>                        | <span data-ttu-id="3b5f5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3b5f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b5f5-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3b5f5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3b5f5-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3b5f5-111">Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="3b5f5-112">Parte</span><span class="sxs-lookup"><span data-stu-id="3b5f5-112">Members</span></span>

#### <span data-ttu-id="3b5f5-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="3b5f5-113">Invoke</span></span> 

<span data-ttu-id="3b5f5-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3b5f5-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3b5f5-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3b5f5-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="3b5f5-116">There are no event args and the args parameter will be null.</span></span>

