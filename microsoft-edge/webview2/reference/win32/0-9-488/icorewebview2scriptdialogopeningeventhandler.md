---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 90721fff94948c632c1bb19d861ffc7d4911faff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884761"
---
# <span data-ttu-id="b3d03-104">0.9.515-ICoreWebView2ScriptDialogOpeningEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="b3d03-104">0.9.515 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="b3d03-105">O chamador implementa essa interface para receber o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="b3d03-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="b3d03-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b3d03-106">Summary</span></span>

 <span data-ttu-id="b3d03-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b3d03-107">Members</span></span>                        | <span data-ttu-id="b3d03-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b3d03-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3d03-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b3d03-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b3d03-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d03-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b3d03-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b3d03-111">Members</span></span>

#### <span data-ttu-id="b3d03-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="b3d03-112">Invoke</span></span> 

<span data-ttu-id="b3d03-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3d03-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b3d03-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b3d03-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

