---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698294"
---
# <span data-ttu-id="36601-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="36601-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="36601-105">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="36601-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="36601-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="36601-106">Summary</span></span>

 <span data-ttu-id="36601-107">Parte</span><span class="sxs-lookup"><span data-stu-id="36601-107">Members</span></span>                        | <span data-ttu-id="36601-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="36601-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="36601-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="36601-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="36601-110">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="36601-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="36601-111">Parte</span><span class="sxs-lookup"><span data-stu-id="36601-111">Members</span></span>

#### <span data-ttu-id="36601-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="36601-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="36601-113">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="36601-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="36601-114">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="36601-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

