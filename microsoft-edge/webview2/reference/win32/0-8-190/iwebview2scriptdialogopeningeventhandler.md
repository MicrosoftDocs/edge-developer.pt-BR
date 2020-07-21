---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 58e76c377d8d5709c006cb3a4da2e0edf73ec8fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884908"
---
# <span data-ttu-id="2473f-104">0.8.355-IWebView2ScriptDialogOpeningEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="2473f-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="2473f-105">O chamador implementa essa interface para receber o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="2473f-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="2473f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="2473f-106">Summary</span></span>

 <span data-ttu-id="2473f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="2473f-107">Members</span></span>                        | <span data-ttu-id="2473f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="2473f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2473f-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="2473f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2473f-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2473f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2473f-111">Parte</span><span class="sxs-lookup"><span data-stu-id="2473f-111">Members</span></span>

#### <span data-ttu-id="2473f-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="2473f-112">Invoke</span></span> 

<span data-ttu-id="2473f-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2473f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2473f-114">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2473f-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

