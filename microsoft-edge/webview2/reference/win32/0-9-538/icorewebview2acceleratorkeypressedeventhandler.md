---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 26bbc2a5c55ebe5a9b7519a87b01c4dd17af375c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879559"
---
# <span data-ttu-id="4ec51-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4ec51-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="4ec51-105">O chamador implementa essa interface para receber o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="4ec51-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="4ec51-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4ec51-106">Summary</span></span>

 <span data-ttu-id="4ec51-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4ec51-107">Members</span></span>                        | <span data-ttu-id="4ec51-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4ec51-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4ec51-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="4ec51-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4ec51-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4ec51-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4ec51-111">Parte</span><span class="sxs-lookup"><span data-stu-id="4ec51-111">Members</span></span>

#### <span data-ttu-id="4ec51-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="4ec51-112">Invoke</span></span> 

<span data-ttu-id="4ec51-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4ec51-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4ec51-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4ec51-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

