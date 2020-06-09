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
ms.openlocfilehash: 4ba3a5acd293b67947622ef4a409319164a23d35
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698026"
---
# <span data-ttu-id="0b0fb-104">interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0b0fb-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0b0fb-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0b0fb-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0b0fb-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="0b0fb-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="0b0fb-107">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0b0fb-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="0b0fb-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0b0fb-108">Summary</span></span>

 <span data-ttu-id="0b0fb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0b0fb-109">Members</span></span>                        | <span data-ttu-id="0b0fb-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0b0fb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b0fb-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="0b0fb-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0b0fb-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="0b0fb-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0b0fb-113">Parte</span><span class="sxs-lookup"><span data-stu-id="0b0fb-113">Members</span></span>

#### <span data-ttu-id="0b0fb-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="0b0fb-114">Invoke</span></span> 

<span data-ttu-id="0b0fb-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="0b0fb-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0b0fb-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0b0fb-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

