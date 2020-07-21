---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 2e12f96307b86fe4c3416c4bde2379869b269cb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884355"
---
# <span data-ttu-id="e69ec-104">0.9.430-ICoreWebView2AcceleratorKeyPressedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="e69ec-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="e69ec-105">O chamador implementa essa interface para receber o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e69ec-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="e69ec-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e69ec-106">Summary</span></span>

 <span data-ttu-id="e69ec-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e69ec-107">Members</span></span>                        | <span data-ttu-id="e69ec-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e69ec-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e69ec-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e69ec-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e69ec-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="e69ec-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e69ec-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e69ec-111">Members</span></span>

#### <span data-ttu-id="e69ec-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="e69ec-112">Invoke</span></span> 

<span data-ttu-id="e69ec-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="e69ec-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e69ec-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e69ec-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

