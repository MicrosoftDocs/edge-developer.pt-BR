---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 22c5e558238e4542ebe70855c3d20837838bebb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883956"
---
# <span data-ttu-id="ccedb-104">0.9.430-ICoreWebView2ZoomFactorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="ccedb-104">0.9.430 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ccedb-105">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ccedb-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="ccedb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ccedb-106">Summary</span></span>

 <span data-ttu-id="ccedb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ccedb-107">Members</span></span>                        | <span data-ttu-id="ccedb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ccedb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ccedb-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ccedb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ccedb-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ccedb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ccedb-111">Use a propriedade ICoreWebView2Host. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="ccedb-111">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="ccedb-112">Parte</span><span class="sxs-lookup"><span data-stu-id="ccedb-112">Members</span></span>

#### <span data-ttu-id="ccedb-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="ccedb-113">Invoke</span></span> 

<span data-ttu-id="ccedb-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ccedb-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ccedb-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ccedb-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="ccedb-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="ccedb-116">There are no event args and the args parameter will be null.</span></span>

