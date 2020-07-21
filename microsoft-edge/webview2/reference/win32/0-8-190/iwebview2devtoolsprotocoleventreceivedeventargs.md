---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 920d95b737a15926e6de33cfed0ee9a98eeade78
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886149"
---
# <span data-ttu-id="5dec9-104">0.8.355-IWebView2DevToolsProtocolEventReceivedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="5dec9-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="5dec9-105">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="5dec9-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="5dec9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5dec9-106">Summary</span></span>

 <span data-ttu-id="5dec9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5dec9-107">Members</span></span>                        | <span data-ttu-id="5dec9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5dec9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5dec9-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="5dec9-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="5dec9-110">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5dec9-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="5dec9-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5dec9-111">Members</span></span>

#### <span data-ttu-id="5dec9-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="5dec9-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="5dec9-113">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="5dec9-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="5dec9-114">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="5dec9-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

