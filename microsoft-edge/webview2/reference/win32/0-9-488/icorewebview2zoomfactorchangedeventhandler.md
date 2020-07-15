---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d4e565db43e9f528b690ab32a784bfd5e40f787b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877284"
---
# <span data-ttu-id="ce317-104">0.9.515-ICoreWebView2ZoomFactorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="ce317-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ce317-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ce317-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ce317-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ce317-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ce317-107">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="ce317-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="ce317-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ce317-108">Summary</span></span>

 <span data-ttu-id="ce317-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ce317-109">Members</span></span>                        | <span data-ttu-id="ce317-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ce317-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ce317-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="ce317-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ce317-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ce317-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ce317-113">Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="ce317-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="ce317-114">Parte</span><span class="sxs-lookup"><span data-stu-id="ce317-114">Members</span></span>

#### <span data-ttu-id="ce317-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="ce317-115">Invoke</span></span> 

<span data-ttu-id="ce317-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ce317-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ce317-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ce317-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ce317-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="ce317-118">There are no event args and the args parameter will be null.</span></span>

