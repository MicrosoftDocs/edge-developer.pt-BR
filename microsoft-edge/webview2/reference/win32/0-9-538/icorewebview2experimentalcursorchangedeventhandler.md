---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: f58279d1a3c404715be5aad8bf1be5ef120e1d94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880000"
---
# <span data-ttu-id="3eb21-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3eb21-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3eb21-105">Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="3eb21-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3eb21-106">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="3eb21-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="3eb21-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="3eb21-107">Summary</span></span>

 <span data-ttu-id="3eb21-108">Parte</span><span class="sxs-lookup"><span data-stu-id="3eb21-108">Members</span></span>                        | <span data-ttu-id="3eb21-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="3eb21-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3eb21-110">Invocar</span><span class="sxs-lookup"><span data-stu-id="3eb21-110">Invoke</span></span>](#invoke) | <span data-ttu-id="3eb21-111">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3eb21-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3eb21-112">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="3eb21-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="3eb21-113">Parte</span><span class="sxs-lookup"><span data-stu-id="3eb21-113">Members</span></span>

#### <span data-ttu-id="3eb21-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="3eb21-114">Invoke</span></span> 

<span data-ttu-id="3eb21-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3eb21-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3eb21-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3eb21-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3eb21-117">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="3eb21-117">There are no event args and the args parameter will be null.</span></span>

