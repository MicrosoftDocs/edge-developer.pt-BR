---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2PermissionRequestedEventHandler
ms.openlocfilehash: 5d906c85cf36ccf270d9af342e329e1d969ff494
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011571"
---
# <span data-ttu-id="bbbfc-104">interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bbbfc-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="bbbfc-105">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="bbbfc-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="bbbfc-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="bbbfc-106">Summary</span></span>

 <span data-ttu-id="bbbfc-107">Parte</span><span class="sxs-lookup"><span data-stu-id="bbbfc-107">Members</span></span>                        | <span data-ttu-id="bbbfc-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="bbbfc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bbbfc-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="bbbfc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bbbfc-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="bbbfc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="bbbfc-111">Parte</span><span class="sxs-lookup"><span data-stu-id="bbbfc-111">Members</span></span>

#### <span data-ttu-id="bbbfc-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="bbbfc-112">Invoke</span></span> 

<span data-ttu-id="bbbfc-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="bbbfc-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bbbfc-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="bbbfc-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

