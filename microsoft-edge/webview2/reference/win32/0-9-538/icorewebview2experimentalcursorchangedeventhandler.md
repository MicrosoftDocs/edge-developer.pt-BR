---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 67d0e6e05fb3640e141ec1ae7193746a1200bbd0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884880"
---
# <span data-ttu-id="914a9-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="914a9-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="914a9-105">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="914a9-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="914a9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="914a9-106">Summary</span></span>

 <span data-ttu-id="914a9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="914a9-107">Members</span></span>                        | <span data-ttu-id="914a9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="914a9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="914a9-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="914a9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="914a9-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="914a9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="914a9-111">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="914a9-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="914a9-112">Parte</span><span class="sxs-lookup"><span data-stu-id="914a9-112">Members</span></span>

#### <span data-ttu-id="914a9-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="914a9-113">Invoke</span></span> 

<span data-ttu-id="914a9-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="914a9-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="914a9-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="914a9-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="914a9-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="914a9-116">There are no event args and the args parameter will be null.</span></span>

