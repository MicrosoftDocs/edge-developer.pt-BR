---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 4111c13756783779a1ef3d223c992defadf43d66
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011531"
---
# <span data-ttu-id="7be04-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7be04-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="7be04-105">Acionado quando uma resposta de uma solicitação é recebida para um recurso da Web no WebView.</span><span class="sxs-lookup"><span data-stu-id="7be04-105">Fires when a response for a request is received for a Web resource in the webview.</span></span>

## <span data-ttu-id="7be04-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7be04-106">Summary</span></span>

 <span data-ttu-id="7be04-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7be04-107">Members</span></span>                        | <span data-ttu-id="7be04-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7be04-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7be04-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="7be04-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7be04-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7be04-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7be04-111">O host pode usar esse evento para ver a solicitação e a resposta reais para um recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="7be04-111">Host can use this event to view the actual request and response for a Web resource.</span></span> <span data-ttu-id="7be04-112">Isso inclui qualquer modificação de solicitação ou resposta feita pela pilha de rede (como a adição de cabeçalhos de autorização) após o evento WebResourceRequested para a solicitação associada ter sido acionado.</span><span class="sxs-lookup"><span data-stu-id="7be04-112">This includes any request or response modifications made by the network stack (such as adding of Authorization headers) after the WebResourceRequested event for the associated request has fired.</span></span> <span data-ttu-id="7be04-113">As modificações feitas na solicitação ou nos objetos de resposta são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="7be04-113">Modifications made to the request or response objects are ignored.</span></span>

## <span data-ttu-id="7be04-114">Parte</span><span class="sxs-lookup"><span data-stu-id="7be04-114">Members</span></span>

#### <span data-ttu-id="7be04-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="7be04-115">Invoke</span></span> 

<span data-ttu-id="7be04-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7be04-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7be04-117">Public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* Sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7be04-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span></span>

