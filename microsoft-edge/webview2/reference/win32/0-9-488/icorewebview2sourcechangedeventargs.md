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
ms.openlocfilehash: 8ea9437530a7f64cc045bfbaa1cc3cc55da77732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698138"
---
# <span data-ttu-id="aa19b-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aa19b-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="aa19b-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="aa19b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="aa19b-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="aa19b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="aa19b-107">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="aa19b-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="aa19b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="aa19b-108">Summary</span></span>

 <span data-ttu-id="aa19b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="aa19b-109">Members</span></span>                        | <span data-ttu-id="aa19b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="aa19b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aa19b-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="aa19b-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="aa19b-112">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="aa19b-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="aa19b-113">Parte</span><span class="sxs-lookup"><span data-stu-id="aa19b-113">Members</span></span>

#### <span data-ttu-id="aa19b-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="aa19b-114">get_IsNewDocument</span></span> 

<span data-ttu-id="aa19b-115">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="aa19b-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="aa19b-116">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="aa19b-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

