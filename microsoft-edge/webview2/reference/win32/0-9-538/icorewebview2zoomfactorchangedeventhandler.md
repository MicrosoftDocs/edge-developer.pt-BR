---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: c941629ab8ee87c0c964b00798878bb69265669a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011388"
---
# <span data-ttu-id="4c2ed-104">0.9.579-ICoreWebView2ZoomFactorChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="4c2ed-104">0.9.579 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4c2ed-105">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="4c2ed-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="4c2ed-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4c2ed-106">Summary</span></span>

 <span data-ttu-id="4c2ed-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4c2ed-107">Members</span></span>                        | <span data-ttu-id="4c2ed-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4c2ed-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c2ed-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="4c2ed-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4c2ed-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4c2ed-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4c2ed-111">Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="4c2ed-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="4c2ed-112">Parte</span><span class="sxs-lookup"><span data-stu-id="4c2ed-112">Members</span></span>

#### <span data-ttu-id="4c2ed-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="4c2ed-113">Invoke</span></span> 

<span data-ttu-id="4c2ed-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4c2ed-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4c2ed-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4c2ed-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="4c2ed-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="4c2ed-116">There are no event args and the args parameter will be null.</span></span>

