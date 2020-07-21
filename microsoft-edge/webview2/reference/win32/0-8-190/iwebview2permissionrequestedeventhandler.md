---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: aeb6e2e25ca9f8c454f5dff891f2c488591d2a48
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884929"
---
# <span data-ttu-id="32c41-104">0.8.355-IWebView2PermissionRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="32c41-104">0.8.355 - interface IWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="32c41-105">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="32c41-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="32c41-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="32c41-106">Summary</span></span>

 <span data-ttu-id="32c41-107">Parte</span><span class="sxs-lookup"><span data-stu-id="32c41-107">Members</span></span>                        | <span data-ttu-id="32c41-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="32c41-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="32c41-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="32c41-109">Invoke</span></span>](#invoke) | <span data-ttu-id="32c41-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="32c41-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="32c41-111">Parte</span><span class="sxs-lookup"><span data-stu-id="32c41-111">Members</span></span>

#### <span data-ttu-id="32c41-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="32c41-112">Invoke</span></span> 

<span data-ttu-id="32c41-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="32c41-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="32c41-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="32c41-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

