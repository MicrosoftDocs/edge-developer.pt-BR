---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: e7fbc952a44bdd38e6e59c46adafb8e71b7904b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652621"
---
# <span data-ttu-id="38ab5-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="38ab5-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="38ab5-105">Args de evento para o evento DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="38ab5-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="38ab5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="38ab5-106">Summary</span></span>

 <span data-ttu-id="38ab5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="38ab5-107">Members</span></span>                        | <span data-ttu-id="38ab5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="38ab5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38ab5-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="38ab5-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="38ab5-110">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="38ab5-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="38ab5-111">Parte</span><span class="sxs-lookup"><span data-stu-id="38ab5-111">Members</span></span>

#### <span data-ttu-id="38ab5-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="38ab5-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="38ab5-113">O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="38ab5-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="38ab5-114">público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="38ab5-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

