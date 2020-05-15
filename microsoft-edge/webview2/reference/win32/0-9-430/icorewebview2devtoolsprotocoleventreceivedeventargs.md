---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 5292acf08102afdda33da43575b2e0e584247ecb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652506"
---
# <span data-ttu-id="f0aa4-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f0aa4-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f0aa4-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f0aa4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f0aa4-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="f0aa4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="f0aa4-107">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="f0aa4-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="f0aa4-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f0aa4-108">Summary</span></span>

 <span data-ttu-id="f0aa4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f0aa4-109">Members</span></span>                        | <span data-ttu-id="f0aa4-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f0aa4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0aa4-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="f0aa4-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="f0aa4-112">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="f0aa4-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="f0aa4-113">Parte</span><span class="sxs-lookup"><span data-stu-id="f0aa4-113">Members</span></span>

#### <span data-ttu-id="f0aa4-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="f0aa4-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="f0aa4-115">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="f0aa4-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="f0aa4-116">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f0aa4-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

