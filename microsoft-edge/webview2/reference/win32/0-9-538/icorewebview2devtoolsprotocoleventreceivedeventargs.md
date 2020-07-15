---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880126"
---
# <span data-ttu-id="7f9fe-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7f9fe-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="7f9fe-105">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7f9fe-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="7f9fe-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7f9fe-106">Summary</span></span>

 <span data-ttu-id="7f9fe-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7f9fe-107">Members</span></span>                        | <span data-ttu-id="7f9fe-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7f9fe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f9fe-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7f9fe-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="7f9fe-110">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="7f9fe-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="7f9fe-111">Parte</span><span class="sxs-lookup"><span data-stu-id="7f9fe-111">Members</span></span>

#### <span data-ttu-id="7f9fe-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="7f9fe-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="7f9fe-113">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="7f9fe-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="7f9fe-114">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7f9fe-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

