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
ms.openlocfilehash: e80dca6411534968822d9994f9911828a4fddeeb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652577"
---
# <span data-ttu-id="35ffd-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="35ffd-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="35ffd-105">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="35ffd-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="35ffd-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="35ffd-106">Summary</span></span>

 <span data-ttu-id="35ffd-107">Parte</span><span class="sxs-lookup"><span data-stu-id="35ffd-107">Members</span></span>                        | <span data-ttu-id="35ffd-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="35ffd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35ffd-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="35ffd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="35ffd-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="35ffd-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="35ffd-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="35ffd-111">There are no event args for this event.</span></span>

## <span data-ttu-id="35ffd-112">Parte</span><span class="sxs-lookup"><span data-stu-id="35ffd-112">Members</span></span>

#### <span data-ttu-id="35ffd-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="35ffd-113">Invoke</span></span> 

<span data-ttu-id="35ffd-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="35ffd-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="35ffd-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="35ffd-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="35ffd-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="35ffd-116">There are no event args and the args parameter will be null.</span></span>

