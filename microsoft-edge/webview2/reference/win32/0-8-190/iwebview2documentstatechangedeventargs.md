---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652592"
---
# <span data-ttu-id="aace1-104">interface IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aace1-104">interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="aace1-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="aace1-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="aace1-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="aace1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="aace1-107">Args de evento para o evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="aace1-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="aace1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="aace1-108">Summary</span></span>

 <span data-ttu-id="aace1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="aace1-109">Members</span></span>                        | <span data-ttu-id="aace1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="aace1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aace1-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="aace1-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="aace1-112">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="aace1-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="aace1-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="aace1-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="aace1-114">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="aace1-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="aace1-115">Parte</span><span class="sxs-lookup"><span data-stu-id="aace1-115">Members</span></span>

#### <span data-ttu-id="aace1-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="aace1-116">get_IsNewDocument</span></span> 

<span data-ttu-id="aace1-117">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="aace1-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="aace1-118">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="aace1-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="aace1-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="aace1-119">get_IsErrorPage</span></span> 

<span data-ttu-id="aace1-120">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="aace1-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="aace1-121">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="aace1-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

