---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 77cf5ffce5eb6fbb6d310968c998a3f65c08b11a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884215"
---
# <span data-ttu-id="02b13-104">0.9.430-ICoreWebView2DocumentTitleChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="02b13-104">0.9.430 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="02b13-105">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="02b13-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="02b13-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="02b13-106">Summary</span></span>

 <span data-ttu-id="02b13-107">Parte</span><span class="sxs-lookup"><span data-stu-id="02b13-107">Members</span></span>                        | <span data-ttu-id="02b13-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="02b13-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="02b13-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="02b13-109">Invoke</span></span>](#invoke) | <span data-ttu-id="02b13-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="02b13-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="02b13-111">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="02b13-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="02b13-112">Parte</span><span class="sxs-lookup"><span data-stu-id="02b13-112">Members</span></span>

#### <span data-ttu-id="02b13-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="02b13-113">Invoke</span></span> 

<span data-ttu-id="02b13-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="02b13-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="02b13-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="02b13-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="02b13-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="02b13-116">There are no event args and the args parameter will be null.</span></span>

