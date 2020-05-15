---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652695"
---
# <span data-ttu-id="e3159-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e3159-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="e3159-105">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="e3159-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="e3159-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e3159-106">Summary</span></span>

 <span data-ttu-id="e3159-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e3159-107">Members</span></span>                        | <span data-ttu-id="e3159-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e3159-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3159-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="e3159-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="e3159-110">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="e3159-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="e3159-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e3159-111">Members</span></span>

#### <span data-ttu-id="e3159-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="e3159-112">get_IsNewDocument</span></span> 

<span data-ttu-id="e3159-113">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="e3159-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="e3159-114">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="e3159-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

