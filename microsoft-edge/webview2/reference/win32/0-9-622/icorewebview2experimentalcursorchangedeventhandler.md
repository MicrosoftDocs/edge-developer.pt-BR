---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 246fc6d23a003a346a20055fbf083421a6fb1b26
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011501"
---
# <span data-ttu-id="c4890-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c4890-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c4890-105">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="c4890-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="c4890-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c4890-106">Summary</span></span>

 <span data-ttu-id="c4890-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c4890-107">Members</span></span>                        | <span data-ttu-id="c4890-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c4890-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4890-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c4890-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c4890-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c4890-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c4890-111">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="c4890-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="c4890-112">Parte</span><span class="sxs-lookup"><span data-stu-id="c4890-112">Members</span></span>

#### <span data-ttu-id="c4890-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="c4890-113">Invoke</span></span> 

<span data-ttu-id="c4890-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c4890-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c4890-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c4890-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c4890-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="c4890-116">There are no event args and the args parameter will be null.</span></span>

