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
ms.openlocfilehash: dd9365fb8fb0215b3090928c8edb59575c6247fe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652688"
---
# <span data-ttu-id="31414-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="31414-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="31414-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="31414-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="31414-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="31414-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="31414-107">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="31414-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="31414-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="31414-108">Summary</span></span>

 <span data-ttu-id="31414-109">Parte</span><span class="sxs-lookup"><span data-stu-id="31414-109">Members</span></span>                        | <span data-ttu-id="31414-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="31414-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="31414-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="31414-111">Invoke</span></span>](#invoke) | <span data-ttu-id="31414-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="31414-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="31414-113">Use a propriedade ICoreWebView2Host. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="31414-113">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="31414-114">Parte</span><span class="sxs-lookup"><span data-stu-id="31414-114">Members</span></span>

#### <span data-ttu-id="31414-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="31414-115">Invoke</span></span> 

<span data-ttu-id="31414-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="31414-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="31414-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="31414-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="31414-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="31414-118">There are no event args and the args parameter will be null.</span></span>

