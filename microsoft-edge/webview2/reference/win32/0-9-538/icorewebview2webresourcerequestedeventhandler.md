---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 3cdafae6480a3bf6e3a5bf96f7e7fba1ae8cc77c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884516"
---
# <span data-ttu-id="34f00-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="34f00-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="34f00-105">Acionado quando uma solicitação de URL (por meio de rede, arquivo etc.) é feita no WebView para um filtro de contexto de recurso de correspondência de recursos da Web e a URL especificada em AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="34f00-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="34f00-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="34f00-106">Summary</span></span>

 <span data-ttu-id="34f00-107">Parte</span><span class="sxs-lookup"><span data-stu-id="34f00-107">Members</span></span>                        | <span data-ttu-id="34f00-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="34f00-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34f00-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="34f00-109">Invoke</span></span>](#invoke) | <span data-ttu-id="34f00-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="34f00-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="34f00-111">O host pode exibir e modificar a solicitação ou fornecer uma resposta em um padrão semelhante para HTTP, caso em que a solicitação foi completada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="34f00-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="34f00-112">Isso pode não conter os cabeçalhos de solicitação que são adicionados pela pilha de rede, como cabeçalhos de autorização.</span><span class="sxs-lookup"><span data-stu-id="34f00-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="34f00-113">Parte</span><span class="sxs-lookup"><span data-stu-id="34f00-113">Members</span></span>

#### <span data-ttu-id="34f00-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="34f00-114">Invoke</span></span> 

<span data-ttu-id="34f00-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="34f00-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="34f00-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="34f00-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

