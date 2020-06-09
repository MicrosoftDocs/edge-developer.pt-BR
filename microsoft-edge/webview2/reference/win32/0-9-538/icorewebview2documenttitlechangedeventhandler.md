---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2908ad851a7899d2ea053bfa50616c8b244bca6c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698288"
---
# <span data-ttu-id="c0211-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c0211-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c0211-105">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="c0211-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="c0211-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c0211-106">Summary</span></span>

 <span data-ttu-id="c0211-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c0211-107">Members</span></span>                        | <span data-ttu-id="c0211-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c0211-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0211-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c0211-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c0211-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c0211-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c0211-111">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="c0211-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="c0211-112">Parte</span><span class="sxs-lookup"><span data-stu-id="c0211-112">Members</span></span>

#### <span data-ttu-id="c0211-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="c0211-113">Invoke</span></span> 

<span data-ttu-id="c0211-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c0211-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c0211-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c0211-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c0211-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="c0211-116">There are no event args and the args parameter will be null.</span></span>

