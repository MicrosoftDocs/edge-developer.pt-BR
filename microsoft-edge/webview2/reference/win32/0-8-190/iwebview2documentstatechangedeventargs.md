---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 2ef38857b06c14eb9808452a33fa23b24855f055
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878558"
---
# <span data-ttu-id="bf718-104">0.8.355-IWebView2DocumentStateChangedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="bf718-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="bf718-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="bf718-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="bf718-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="bf718-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="bf718-107">Args de evento para o evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="bf718-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="bf718-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="bf718-108">Summary</span></span>

 <span data-ttu-id="bf718-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bf718-109">Members</span></span>                        | <span data-ttu-id="bf718-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="bf718-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bf718-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bf718-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="bf718-112">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="bf718-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="bf718-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="bf718-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="bf718-114">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="bf718-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="bf718-115">Parte</span><span class="sxs-lookup"><span data-stu-id="bf718-115">Members</span></span>

#### <span data-ttu-id="bf718-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="bf718-116">get_IsNewDocument</span></span> 

<span data-ttu-id="bf718-117">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="bf718-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="bf718-118">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="bf718-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="bf718-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="bf718-119">get_IsErrorPage</span></span> 

<span data-ttu-id="bf718-120">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="bf718-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="bf718-121">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="bf718-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

