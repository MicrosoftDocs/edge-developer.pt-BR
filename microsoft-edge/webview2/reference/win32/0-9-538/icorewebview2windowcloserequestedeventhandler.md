---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: 34b0f941029251824cdc108e0aca41e6eab93695
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011374"
---
# <span data-ttu-id="6c8d4-104">0.9.579-ICoreWebView2WindowCloseRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="6c8d4-104">0.9.579 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="6c8d4-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="6c8d4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6c8d4-106">Summary</span></span>

 <span data-ttu-id="6c8d4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6c8d4-107">Members</span></span>                        | <span data-ttu-id="6c8d4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6c8d4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c8d4-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="6c8d4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6c8d4-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6c8d4-111">Parte</span><span class="sxs-lookup"><span data-stu-id="6c8d4-111">Members</span></span>

#### <span data-ttu-id="6c8d4-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="6c8d4-112">Invoke</span></span> 

<span data-ttu-id="6c8d4-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6c8d4-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6c8d4-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="6c8d4-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="6c8d4-115">There are no event args and the args parameter will be null.</span></span>

