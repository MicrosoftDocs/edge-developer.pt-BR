---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 2eb2749b71cd9be9dfd25bb686b4ea57e728f179
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883978"
---
# <span data-ttu-id="c22ae-104">0.9.430-ICoreWebView2SourceChangedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="c22ae-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="c22ae-105">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="c22ae-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="c22ae-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c22ae-106">Summary</span></span>

 <span data-ttu-id="c22ae-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c22ae-107">Members</span></span>                        | <span data-ttu-id="c22ae-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c22ae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c22ae-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="c22ae-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="c22ae-110">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="c22ae-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="c22ae-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c22ae-111">Members</span></span>

#### <span data-ttu-id="c22ae-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="c22ae-112">get_IsNewDocument</span></span> 

<span data-ttu-id="c22ae-113">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="c22ae-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="c22ae-114">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="c22ae-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

