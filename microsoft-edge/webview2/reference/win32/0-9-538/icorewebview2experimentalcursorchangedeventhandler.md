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
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698278"
---
# <span data-ttu-id="f7017-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7017-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f7017-105">Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="f7017-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f7017-106">O chamador implementa essa interface para receber eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="f7017-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="f7017-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="f7017-107">Summary</span></span>

 <span data-ttu-id="f7017-108">Parte</span><span class="sxs-lookup"><span data-stu-id="f7017-108">Members</span></span>                        | <span data-ttu-id="f7017-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="f7017-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7017-110">Invocar</span><span class="sxs-lookup"><span data-stu-id="f7017-110">Invoke</span></span>](#invoke) | <span data-ttu-id="f7017-111">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f7017-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f7017-112">Use a propriedade cursor para obter o novo cursor.</span><span class="sxs-lookup"><span data-stu-id="f7017-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="f7017-113">Parte</span><span class="sxs-lookup"><span data-stu-id="f7017-113">Members</span></span>

#### <span data-ttu-id="f7017-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="f7017-114">Invoke</span></span> 

<span data-ttu-id="f7017-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f7017-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f7017-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f7017-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f7017-117">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="f7017-117">There are no event args and the args parameter will be null.</span></span>

