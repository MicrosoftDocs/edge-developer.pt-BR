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
ms.openlocfilehash: dc6af50c8e02bf556a5d6245be03bbe030fee9d6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698235"
---
# <span data-ttu-id="89b85-104">interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="89b85-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="89b85-105">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="89b85-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="89b85-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="89b85-106">Summary</span></span>

 <span data-ttu-id="89b85-107">Parte</span><span class="sxs-lookup"><span data-stu-id="89b85-107">Members</span></span>                        | <span data-ttu-id="89b85-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="89b85-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89b85-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="89b85-109">Invoke</span></span>](#invoke) | <span data-ttu-id="89b85-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="89b85-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="89b85-111">Parte</span><span class="sxs-lookup"><span data-stu-id="89b85-111">Members</span></span>

#### <span data-ttu-id="89b85-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="89b85-112">Invoke</span></span> 

<span data-ttu-id="89b85-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="89b85-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="89b85-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="89b85-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

