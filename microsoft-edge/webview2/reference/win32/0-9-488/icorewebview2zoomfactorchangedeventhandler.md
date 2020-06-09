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
ms.openlocfilehash: 64211bf99873ef2e2a41aaf2fb9453e892f6536a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698103"
---
# <span data-ttu-id="7b404-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7b404-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7b404-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7b404-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7b404-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7b404-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7b404-107">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7b404-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="7b404-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7b404-108">Summary</span></span>

 <span data-ttu-id="7b404-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7b404-109">Members</span></span>                        | <span data-ttu-id="7b404-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7b404-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7b404-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="7b404-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7b404-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7b404-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7b404-113">Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="7b404-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="7b404-114">Parte</span><span class="sxs-lookup"><span data-stu-id="7b404-114">Members</span></span>

#### <span data-ttu-id="7b404-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="7b404-115">Invoke</span></span> 

<span data-ttu-id="7b404-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7b404-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7b404-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7b404-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="7b404-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="7b404-118">There are no event args and the args parameter will be null.</span></span>

