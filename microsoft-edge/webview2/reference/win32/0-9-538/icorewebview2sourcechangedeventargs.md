---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: b9350db7d59c0369bfb16d10e30a23ef3f6bffa5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010449"
---
# <span data-ttu-id="a69af-104">0.9.579-ICoreWebView2SourceChangedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="a69af-104">0.9.579 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="a69af-105">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="a69af-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="a69af-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="a69af-106">Summary</span></span>

 <span data-ttu-id="a69af-107">Parte</span><span class="sxs-lookup"><span data-stu-id="a69af-107">Members</span></span>                        | <span data-ttu-id="a69af-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="a69af-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a69af-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="a69af-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="a69af-110">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="a69af-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="a69af-111">Parte</span><span class="sxs-lookup"><span data-stu-id="a69af-111">Members</span></span>

#### <span data-ttu-id="a69af-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="a69af-112">get_IsNewDocument</span></span> 

<span data-ttu-id="a69af-113">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="a69af-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="a69af-114">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="a69af-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

