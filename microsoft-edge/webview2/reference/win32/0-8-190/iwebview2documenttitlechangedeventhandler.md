---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 0dc9886bc2282d08855ccb40cb8b06b4ffadb659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886106"
---
# <span data-ttu-id="dc162-104">0.8.355-IWebView2DocumentTitleChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="dc162-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="dc162-105">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="dc162-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="dc162-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="dc162-106">Summary</span></span>

 <span data-ttu-id="dc162-107">Parte</span><span class="sxs-lookup"><span data-stu-id="dc162-107">Members</span></span>                        | <span data-ttu-id="dc162-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="dc162-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc162-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="dc162-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dc162-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="dc162-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="dc162-111">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="dc162-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="dc162-112">Parte</span><span class="sxs-lookup"><span data-stu-id="dc162-112">Members</span></span>

#### <span data-ttu-id="dc162-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="dc162-113">Invoke</span></span> 

<span data-ttu-id="dc162-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="dc162-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dc162-115">[chamada](#invoke)a Public HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="dc162-115">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="dc162-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="dc162-116">There are no event args and the args parameter will be null.</span></span>

