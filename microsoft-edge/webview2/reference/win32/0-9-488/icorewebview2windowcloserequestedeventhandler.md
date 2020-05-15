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
ms.openlocfilehash: 889728489b6c4b06cd224915a0e12ee0a4144653
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652395"
---
# <span data-ttu-id="c1df6-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c1df6-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c1df6-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="c1df6-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="c1df6-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c1df6-106">Summary</span></span>

 <span data-ttu-id="c1df6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c1df6-107">Members</span></span>                        | <span data-ttu-id="c1df6-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c1df6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1df6-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c1df6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c1df6-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c1df6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c1df6-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c1df6-111">Members</span></span>

#### <span data-ttu-id="c1df6-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="c1df6-112">Invoke</span></span> 

<span data-ttu-id="c1df6-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c1df6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c1df6-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c1df6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c1df6-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="c1df6-115">There are no event args and the args parameter will be null.</span></span>

