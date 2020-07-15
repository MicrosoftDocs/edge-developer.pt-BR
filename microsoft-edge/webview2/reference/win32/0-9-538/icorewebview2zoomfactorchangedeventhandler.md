---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 74cd0451e111780078714b17e5bd1097c56d6b2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877571"
---
# <span data-ttu-id="8e052-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8e052-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="8e052-105">O chamador implementa essa interface para receber eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="8e052-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="8e052-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="8e052-106">Summary</span></span>

 <span data-ttu-id="8e052-107">Parte</span><span class="sxs-lookup"><span data-stu-id="8e052-107">Members</span></span>                        | <span data-ttu-id="8e052-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="8e052-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8e052-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="8e052-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8e052-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8e052-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="8e052-111">Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="8e052-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="8e052-112">Parte</span><span class="sxs-lookup"><span data-stu-id="8e052-112">Members</span></span>

#### <span data-ttu-id="8e052-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="8e052-113">Invoke</span></span> 

<span data-ttu-id="8e052-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8e052-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8e052-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="8e052-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="8e052-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="8e052-116">There are no event args and the args parameter will be null.</span></span>

