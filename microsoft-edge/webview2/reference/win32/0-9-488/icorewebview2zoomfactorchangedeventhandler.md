---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: e2469dd9a587735efcf88a48e0ce950cb4f85239
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652640"
---
# <span data-ttu-id="53b66-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="53b66-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="53b66-105">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="53b66-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="53b66-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="53b66-106">Summary</span></span>

 <span data-ttu-id="53b66-107">Parte</span><span class="sxs-lookup"><span data-stu-id="53b66-107">Members</span></span>                        | <span data-ttu-id="53b66-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="53b66-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="53b66-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="53b66-109">Invoke</span></span>](#invoke) | <span data-ttu-id="53b66-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="53b66-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="53b66-111">Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="53b66-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="53b66-112">Parte</span><span class="sxs-lookup"><span data-stu-id="53b66-112">Members</span></span>

#### <span data-ttu-id="53b66-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="53b66-113">Invoke</span></span> 

<span data-ttu-id="53b66-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="53b66-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="53b66-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="53b66-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="53b66-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="53b66-116">There are no event args and the args parameter will be null.</span></span>

