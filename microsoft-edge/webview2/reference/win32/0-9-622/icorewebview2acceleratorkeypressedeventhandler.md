---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 15ad3a4afb76ea8068066097340af204b45fe416
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011579"
---
# <span data-ttu-id="f0d6a-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f0d6a-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="f0d6a-105">O chamador implementa essa interface para receber o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="f0d6a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f0d6a-106">Summary</span></span>

 <span data-ttu-id="f0d6a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f0d6a-107">Members</span></span>                        | <span data-ttu-id="f0d6a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f0d6a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0d6a-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="f0d6a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f0d6a-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f0d6a-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f0d6a-111">Members</span></span>

#### <span data-ttu-id="f0d6a-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="f0d6a-112">Invoke</span></span> 

<span data-ttu-id="f0d6a-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f0d6a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f0d6a-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f0d6a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

