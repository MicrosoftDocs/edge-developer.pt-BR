---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 3e622a8fb5b8ed43e5a23eaab8bd0aa61ed7d193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879398"
---
# <span data-ttu-id="7745d-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7745d-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="7745d-105">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="7745d-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="7745d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7745d-106">Summary</span></span>

 <span data-ttu-id="7745d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7745d-107">Members</span></span>                        | <span data-ttu-id="7745d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7745d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7745d-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="7745d-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="7745d-110">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="7745d-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="7745d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="7745d-111">Members</span></span>

#### <span data-ttu-id="7745d-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="7745d-112">get_IsNewDocument</span></span> 

<span data-ttu-id="7745d-113">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="7745d-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="7745d-114">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="7745d-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

