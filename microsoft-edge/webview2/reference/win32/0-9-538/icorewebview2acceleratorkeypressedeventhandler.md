---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 104291f2bbf285737311a205188a1b549906becf
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011212"
---
# <span data-ttu-id="03dc7-104">0.9.579-ICoreWebView2AcceleratorKeyPressedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="03dc7-104">0.9.579 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="03dc7-105">O chamador implementa essa interface para receber o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="03dc7-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="03dc7-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="03dc7-106">Summary</span></span>

 <span data-ttu-id="03dc7-107">Parte</span><span class="sxs-lookup"><span data-stu-id="03dc7-107">Members</span></span>                        | <span data-ttu-id="03dc7-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="03dc7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="03dc7-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="03dc7-109">Invoke</span></span>](#invoke) | <span data-ttu-id="03dc7-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="03dc7-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="03dc7-111">Parte</span><span class="sxs-lookup"><span data-stu-id="03dc7-111">Members</span></span>

#### <span data-ttu-id="03dc7-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="03dc7-112">Invoke</span></span> 

<span data-ttu-id="03dc7-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="03dc7-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="03dc7-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="03dc7-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

