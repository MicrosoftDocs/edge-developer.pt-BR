---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 79af7b28b8b8ab7e2e2b6612f121208b8d917725
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010265"
---
# <span data-ttu-id="08531-104">0.9.579-ICoreWebView2DevToolsProtocolEventReceivedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="08531-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="08531-105">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="08531-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="08531-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="08531-106">Summary</span></span>

 <span data-ttu-id="08531-107">Parte</span><span class="sxs-lookup"><span data-stu-id="08531-107">Members</span></span>                        | <span data-ttu-id="08531-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="08531-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="08531-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="08531-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="08531-110">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="08531-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="08531-111">Parte</span><span class="sxs-lookup"><span data-stu-id="08531-111">Members</span></span>

#### <span data-ttu-id="08531-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="08531-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="08531-113">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="08531-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="08531-114">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="08531-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

