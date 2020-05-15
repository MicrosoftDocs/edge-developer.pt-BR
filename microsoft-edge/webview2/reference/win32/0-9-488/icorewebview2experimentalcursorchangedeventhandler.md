---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 9c8cd627275a98382f079bc4f64dd7f565d46630
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652731"
---
# <span data-ttu-id="6c4ff-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6c4ff-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6c4ff-105">Esta é uma API experimental que é fornecida com a versão 0.9.488 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="6c4ff-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6c4ff-106">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="6c4ff-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="6c4ff-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="6c4ff-107">Summary</span></span>

 <span data-ttu-id="6c4ff-108">Parte</span><span class="sxs-lookup"><span data-stu-id="6c4ff-108">Members</span></span>                        | <span data-ttu-id="6c4ff-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="6c4ff-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c4ff-110">Invocar</span><span class="sxs-lookup"><span data-stu-id="6c4ff-110">Invoke</span></span>](#invoke) | <span data-ttu-id="6c4ff-111">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6c4ff-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6c4ff-112">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="6c4ff-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="6c4ff-113">Parte</span><span class="sxs-lookup"><span data-stu-id="6c4ff-113">Members</span></span>

#### <span data-ttu-id="6c4ff-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="6c4ff-114">Invoke</span></span> 

<span data-ttu-id="6c4ff-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="6c4ff-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6c4ff-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6c4ff-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="6c4ff-117">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="6c4ff-117">There are no event args and the args parameter will be null.</span></span>

