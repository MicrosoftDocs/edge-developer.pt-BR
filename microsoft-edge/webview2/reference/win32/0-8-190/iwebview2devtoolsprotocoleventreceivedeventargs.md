---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 0df2ea043a95c8cca24c0b9bbe3091c490b4ea3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878600"
---
# <span data-ttu-id="462e2-104">0.8.355-IWebView2DevToolsProtocolEventReceivedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="462e2-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="462e2-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="462e2-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="462e2-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="462e2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="462e2-107">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="462e2-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="462e2-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="462e2-108">Summary</span></span>

 <span data-ttu-id="462e2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="462e2-109">Members</span></span>                        | <span data-ttu-id="462e2-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="462e2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="462e2-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="462e2-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="462e2-112">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="462e2-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="462e2-113">Parte</span><span class="sxs-lookup"><span data-stu-id="462e2-113">Members</span></span>

#### <span data-ttu-id="462e2-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="462e2-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="462e2-115">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="462e2-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="462e2-116">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="462e2-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

