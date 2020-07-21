---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: c42e353c80335b6dccdad49b470e68fa5ae2f559
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884250"
---
# <span data-ttu-id="8b3c1-104">0.9.430-ICoreWebView2DevToolsProtocolEventReceivedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="8b3c1-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="8b3c1-105">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="8b3c1-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="8b3c1-106">Summary</span></span>

 <span data-ttu-id="8b3c1-107">Parte</span><span class="sxs-lookup"><span data-stu-id="8b3c1-107">Members</span></span>                        | <span data-ttu-id="8b3c1-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="8b3c1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b3c1-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="8b3c1-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="8b3c1-110">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="8b3c1-111">Parte</span><span class="sxs-lookup"><span data-stu-id="8b3c1-111">Members</span></span>

#### <span data-ttu-id="8b3c1-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="8b3c1-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="8b3c1-113">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="8b3c1-114">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="8b3c1-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

