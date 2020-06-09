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
ms.openlocfilehash: 0d02fb1c8605bc6817085748154055cdfa489da8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698353"
---
# <span data-ttu-id="2ac1c-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2ac1c-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="2ac1c-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2ac1c-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="2ac1c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="2ac1c-106">Summary</span></span>

 <span data-ttu-id="2ac1c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="2ac1c-107">Members</span></span>                        | <span data-ttu-id="2ac1c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="2ac1c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ac1c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="2ac1c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2ac1c-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2ac1c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2ac1c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="2ac1c-111">Members</span></span>

#### <span data-ttu-id="2ac1c-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="2ac1c-112">Invoke</span></span> 

<span data-ttu-id="2ac1c-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2ac1c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2ac1c-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2ac1c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="2ac1c-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="2ac1c-115">There are no event args and the args parameter will be null.</span></span>

