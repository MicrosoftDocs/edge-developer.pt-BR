---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 03c67160e9c10db7cf3fc88b7ecf2c84c30c4129
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011416"
---
# <span data-ttu-id="e703e-104">0.9.579-ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="e703e-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="e703e-105">Acionado quando uma resposta de uma solicitação é recebida para um recurso da Web no WebView.</span><span class="sxs-lookup"><span data-stu-id="e703e-105">Fires when a response for a request is received for a Web resource in the webview.</span></span>

## <span data-ttu-id="e703e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e703e-106">Summary</span></span>

 <span data-ttu-id="e703e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e703e-107">Members</span></span>                        | <span data-ttu-id="e703e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e703e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e703e-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e703e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e703e-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="e703e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e703e-111">O host pode usar esse evento para ver a solicitação e a resposta reais para um recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="e703e-111">Host can use this event to view the actual request and response for a Web resource.</span></span> <span data-ttu-id="e703e-112">Isso inclui qualquer modificação de solicitação ou resposta feita pela pilha de rede (como a adição de cabeçalhos de autorização) após o evento WebResourceRequested para a solicitação associada ter sido acionado.</span><span class="sxs-lookup"><span data-stu-id="e703e-112">This includes any request or response modifications made by the network stack (such as adding of Authorization headers) after the WebResourceRequested event for the associated request has fired.</span></span> <span data-ttu-id="e703e-113">As modificações feitas na solicitação ou nos objetos de resposta são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="e703e-113">Modifications made to the request or response objects are ignored.</span></span>

## <span data-ttu-id="e703e-114">Parte</span><span class="sxs-lookup"><span data-stu-id="e703e-114">Members</span></span>

#### <span data-ttu-id="e703e-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="e703e-115">Invoke</span></span> 

<span data-ttu-id="e703e-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="e703e-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e703e-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* Sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e703e-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span></span>

