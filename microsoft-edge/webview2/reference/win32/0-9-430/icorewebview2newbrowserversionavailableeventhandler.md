---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b44724f8e18e11374f88ed2cd22711f06f59f12d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652589"
---
# <span data-ttu-id="558a7-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="558a7-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="558a7-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="558a7-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="558a7-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="558a7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="558a7-107">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="558a7-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="558a7-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="558a7-108">Summary</span></span>

 <span data-ttu-id="558a7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="558a7-109">Members</span></span>                        | <span data-ttu-id="558a7-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="558a7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="558a7-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="558a7-111">Invoke</span></span>](#invoke) | <span data-ttu-id="558a7-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="558a7-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="558a7-113">Use o método get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) para obter o novo número de versão.</span><span class="sxs-lookup"><span data-stu-id="558a7-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="558a7-114">Parte</span><span class="sxs-lookup"><span data-stu-id="558a7-114">Members</span></span>

#### <span data-ttu-id="558a7-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="558a7-115">Invoke</span></span> 

<span data-ttu-id="558a7-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="558a7-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="558a7-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="558a7-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

