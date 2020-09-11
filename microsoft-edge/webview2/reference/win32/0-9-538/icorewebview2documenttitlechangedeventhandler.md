---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 674b97cce835721f3ffa622115d237ef81939a91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010275"
---
# <span data-ttu-id="3eaad-104">0.9.579-ICoreWebView2DocumentTitleChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="3eaad-104">0.9.579 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3eaad-105">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="3eaad-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="3eaad-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3eaad-106">Summary</span></span>

 <span data-ttu-id="3eaad-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3eaad-107">Members</span></span>                        | <span data-ttu-id="3eaad-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3eaad-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3eaad-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3eaad-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3eaad-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3eaad-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3eaad-111">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="3eaad-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="3eaad-112">Parte</span><span class="sxs-lookup"><span data-stu-id="3eaad-112">Members</span></span>

#### <span data-ttu-id="3eaad-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="3eaad-113">Invoke</span></span> 

<span data-ttu-id="3eaad-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3eaad-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3eaad-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3eaad-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3eaad-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="3eaad-116">There are no event args and the args parameter will be null.</span></span>

