---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2PermissionRequestedEventHandler
ms.openlocfilehash: 809524e55a610dcd157860cfa9ed88f86ee63dca
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010037"
---
# <span data-ttu-id="8ae38-104">0.9.579-ICoreWebView2PermissionRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="8ae38-104">0.9.579 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8ae38-105">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="8ae38-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="8ae38-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="8ae38-106">Summary</span></span>

 <span data-ttu-id="8ae38-107">Parte</span><span class="sxs-lookup"><span data-stu-id="8ae38-107">Members</span></span>                        | <span data-ttu-id="8ae38-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="8ae38-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8ae38-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="8ae38-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8ae38-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8ae38-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8ae38-111">Parte</span><span class="sxs-lookup"><span data-stu-id="8ae38-111">Members</span></span>

#### <span data-ttu-id="8ae38-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="8ae38-112">Invoke</span></span> 

<span data-ttu-id="8ae38-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8ae38-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8ae38-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8ae38-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

