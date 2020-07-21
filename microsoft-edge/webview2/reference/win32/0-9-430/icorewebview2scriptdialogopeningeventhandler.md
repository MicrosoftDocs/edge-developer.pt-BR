---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 31fea451b377b86eda0055a1074706ea12d9538e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884019"
---
# <span data-ttu-id="3f018-104">0.9.430-ICoreWebView2ScriptDialogOpeningEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="3f018-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="3f018-105">O chamador implementa essa interface para receber o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="3f018-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="3f018-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3f018-106">Summary</span></span>

 <span data-ttu-id="3f018-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3f018-107">Members</span></span>                        | <span data-ttu-id="3f018-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3f018-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f018-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3f018-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3f018-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3f018-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3f018-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3f018-111">Members</span></span>

#### <span data-ttu-id="3f018-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="3f018-112">Invoke</span></span> 

<span data-ttu-id="3f018-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3f018-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3f018-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3f018-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

