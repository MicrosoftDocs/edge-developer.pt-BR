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
ms.openlocfilehash: 4ae58375f0158a3876b284e16a579149dc6db9a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698358"
---
# <span data-ttu-id="5b5af-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5b5af-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="5b5af-105">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="5b5af-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="5b5af-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5b5af-106">Summary</span></span>

 <span data-ttu-id="5b5af-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5b5af-107">Members</span></span>                        | <span data-ttu-id="5b5af-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5b5af-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5b5af-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="5b5af-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="5b5af-110">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="5b5af-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="5b5af-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5b5af-111">Members</span></span>

#### <span data-ttu-id="5b5af-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="5b5af-112">get_IsNewDocument</span></span> 

<span data-ttu-id="5b5af-113">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="5b5af-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="5b5af-114">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="5b5af-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

