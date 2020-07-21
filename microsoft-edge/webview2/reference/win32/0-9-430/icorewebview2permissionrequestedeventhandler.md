---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 41fac4533a96e39da261516f91b96fbf00775af3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886420"
---
# <span data-ttu-id="f8981-104">0.9.430-ICoreWebView2PermissionRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="f8981-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f8981-105">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f8981-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="f8981-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f8981-106">Summary</span></span>

 <span data-ttu-id="f8981-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f8981-107">Members</span></span>                        | <span data-ttu-id="f8981-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f8981-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8981-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f8981-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f8981-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f8981-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f8981-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f8981-111">Members</span></span>

#### <span data-ttu-id="f8981-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="f8981-112">Invoke</span></span> 

<span data-ttu-id="f8981-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f8981-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f8981-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2PermissionRequestedEventArgs](ICoreWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f8981-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2PermissionRequestedEventArgs](ICoreWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

