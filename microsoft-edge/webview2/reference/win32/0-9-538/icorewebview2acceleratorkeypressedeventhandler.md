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
ms.openlocfilehash: 05dd401064635a6b20f1936b1efaac025b45749f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698312"
---
# <span data-ttu-id="ef6cd-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ef6cd-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="ef6cd-105">O chamador implementa essa interface para receber o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ef6cd-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="ef6cd-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ef6cd-106">Summary</span></span>

 <span data-ttu-id="ef6cd-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ef6cd-107">Members</span></span>                        | <span data-ttu-id="ef6cd-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ef6cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef6cd-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ef6cd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ef6cd-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ef6cd-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ef6cd-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ef6cd-111">Members</span></span>

#### <span data-ttu-id="ef6cd-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="ef6cd-112">Invoke</span></span> 

<span data-ttu-id="ef6cd-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ef6cd-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ef6cd-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ef6cd-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

