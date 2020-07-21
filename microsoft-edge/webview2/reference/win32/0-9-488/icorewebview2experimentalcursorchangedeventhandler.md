---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: ee6de606d6ed8a9e00dbdacee9bb07b341a6d04e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886483"
---
# <span data-ttu-id="1583a-104">0.9.515-ICoreWebView2ExperimentalCursorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="1583a-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1583a-105">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="1583a-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="1583a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1583a-106">Summary</span></span>

 <span data-ttu-id="1583a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1583a-107">Members</span></span>                        | <span data-ttu-id="1583a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1583a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1583a-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="1583a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1583a-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="1583a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1583a-111">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="1583a-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="1583a-112">Parte</span><span class="sxs-lookup"><span data-stu-id="1583a-112">Members</span></span>

#### <span data-ttu-id="1583a-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="1583a-113">Invoke</span></span> 

<span data-ttu-id="1583a-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="1583a-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1583a-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1583a-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="1583a-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="1583a-116">There are no event args and the args parameter will be null.</span></span>

