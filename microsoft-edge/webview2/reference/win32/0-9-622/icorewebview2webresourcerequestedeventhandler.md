---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 6aa36c8b28a3e47a796324987687ab23179aae10
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011427"
---
# <span data-ttu-id="681ef-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="681ef-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="681ef-105">Acionado quando uma solicitação de URL (por meio de rede, arquivo etc.) é feita no WebView para um filtro de contexto de recurso de correspondência de recursos da Web e a URL especificada em AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="681ef-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="681ef-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="681ef-106">Summary</span></span>

 <span data-ttu-id="681ef-107">Parte</span><span class="sxs-lookup"><span data-stu-id="681ef-107">Members</span></span>                        | <span data-ttu-id="681ef-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="681ef-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="681ef-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="681ef-109">Invoke</span></span>](#invoke) | <span data-ttu-id="681ef-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="681ef-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="681ef-111">O host pode exibir e modificar a solicitação ou fornecer uma resposta em um padrão semelhante para HTTP, caso em que a solicitação foi completada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="681ef-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="681ef-112">Isso pode não conter os cabeçalhos de solicitação que são adicionados pela pilha de rede, como cabeçalhos de autorização.</span><span class="sxs-lookup"><span data-stu-id="681ef-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="681ef-113">Parte</span><span class="sxs-lookup"><span data-stu-id="681ef-113">Members</span></span>

#### <span data-ttu-id="681ef-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="681ef-114">Invoke</span></span> 

<span data-ttu-id="681ef-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="681ef-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="681ef-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="681ef-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

