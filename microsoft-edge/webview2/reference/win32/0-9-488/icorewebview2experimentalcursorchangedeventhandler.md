---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 6fbcc82409791bc3d2da3bb2f7985732cb344a97
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880623"
---
# <span data-ttu-id="ef373-104">0.9.515-ICoreWebView2ExperimentalCursorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="ef373-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ef373-105">Esta é uma API experimental que é fornecida com a versão 0.9.488 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="ef373-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ef373-106">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ef373-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="ef373-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="ef373-107">Summary</span></span>

 <span data-ttu-id="ef373-108">Parte</span><span class="sxs-lookup"><span data-stu-id="ef373-108">Members</span></span>                        | <span data-ttu-id="ef373-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="ef373-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef373-110">Invocar</span><span class="sxs-lookup"><span data-stu-id="ef373-110">Invoke</span></span>](#invoke) | <span data-ttu-id="ef373-111">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ef373-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ef373-112">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="ef373-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="ef373-113">Parte</span><span class="sxs-lookup"><span data-stu-id="ef373-113">Members</span></span>

#### <span data-ttu-id="ef373-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="ef373-114">Invoke</span></span> 

<span data-ttu-id="ef373-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ef373-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ef373-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ef373-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ef373-117">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="ef373-117">There are no event args and the args parameter will be null.</span></span>

