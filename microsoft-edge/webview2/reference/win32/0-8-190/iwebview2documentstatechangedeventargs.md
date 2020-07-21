---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886119"
---
# <span data-ttu-id="b5635-104">0.8.355-IWebView2DocumentStateChangedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="b5635-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="b5635-105">Args de evento para o evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="b5635-105">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="b5635-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b5635-106">Summary</span></span>

 <span data-ttu-id="b5635-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b5635-107">Members</span></span>                        | <span data-ttu-id="b5635-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b5635-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b5635-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="b5635-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="b5635-110">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="b5635-110">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="b5635-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="b5635-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="b5635-112">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="b5635-112">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="b5635-113">Parte</span><span class="sxs-lookup"><span data-stu-id="b5635-113">Members</span></span>

#### <span data-ttu-id="b5635-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="b5635-114">get_IsNewDocument</span></span> 

<span data-ttu-id="b5635-115">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="b5635-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="b5635-116">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="b5635-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="b5635-117">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="b5635-117">get_IsErrorPage</span></span> 

<span data-ttu-id="b5635-118">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="b5635-118">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="b5635-119">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="b5635-119">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

