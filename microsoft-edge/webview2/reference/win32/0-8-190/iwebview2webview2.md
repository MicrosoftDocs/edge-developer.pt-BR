---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884727"
---
# <span data-ttu-id="538bc-104">0.8.355-IWebView2WebView2 de interface</span><span class="sxs-lookup"><span data-stu-id="538bc-104">0.8.355 - interface IWebView2WebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="538bc-105">Funcionalidades adicionais implementadas pelo objeto WebView primário.</span><span class="sxs-lookup"><span data-stu-id="538bc-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="538bc-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="538bc-106">Summary</span></span>

 <span data-ttu-id="538bc-107">Parte</span><span class="sxs-lookup"><span data-stu-id="538bc-107">Members</span></span>                        | <span data-ttu-id="538bc-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="538bc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="538bc-109">Parar</span><span class="sxs-lookup"><span data-stu-id="538bc-109">Stop</span></span>](#stop) | <span data-ttu-id="538bc-110">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="538bc-110">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="538bc-111">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="538bc-111">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="538bc-112">Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="538bc-112">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="538bc-113">Parte</span><span class="sxs-lookup"><span data-stu-id="538bc-113">Members</span></span>

#### <span data-ttu-id="538bc-114">Parar</span><span class="sxs-lookup"><span data-stu-id="538bc-114">Stop</span></span> 

<span data-ttu-id="538bc-115">Interrompa todas as navegações e buscas de recursos pendentes.</span><span class="sxs-lookup"><span data-stu-id="538bc-115">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="538bc-116">público- [limite](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="538bc-116">public HRESULT [Stop](#stop)()</span></span>

