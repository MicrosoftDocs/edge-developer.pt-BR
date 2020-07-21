---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 3a9af31477e7b4155bece55ec2faef85efccbd0d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884978"
---
# <span data-ttu-id="70e9b-104">0.8.355-IWebView2NewVersionAvailableEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="70e9b-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="70e9b-105">O chamador implementa essa interface para receber eventos NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="70e9b-105">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="70e9b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="70e9b-106">Summary</span></span>

 <span data-ttu-id="70e9b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="70e9b-107">Members</span></span>                        | <span data-ttu-id="70e9b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="70e9b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70e9b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="70e9b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="70e9b-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="70e9b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="70e9b-111">Use o método get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) para obter o novo número de versão.</span><span class="sxs-lookup"><span data-stu-id="70e9b-111">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="70e9b-112">Parte</span><span class="sxs-lookup"><span data-stu-id="70e9b-112">Members</span></span>

#### <span data-ttu-id="70e9b-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="70e9b-113">Invoke</span></span> 

<span data-ttu-id="70e9b-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="70e9b-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="70e9b-115">[chamada](#invoke)a Public HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="70e9b-115">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

