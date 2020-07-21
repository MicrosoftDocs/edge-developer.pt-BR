---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884586"
---
# <span data-ttu-id="b7b8f-104">0.9.515-estrutura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="b7b8f-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="b7b8f-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b7b8f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b7b8f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b7b8f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b7b8f-107">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="b7b8f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b7b8f-108">Summary</span></span>

 <span data-ttu-id="b7b8f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b7b8f-109">Members</span></span>                        | <span data-ttu-id="b7b8f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b7b8f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7b8f-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b7b8f-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="b7b8f-112">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="b7b8f-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b7b8f-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="b7b8f-114">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-114">The transition state.</span></span>
[<span data-ttu-id="b7b8f-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b7b8f-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="b7b8f-116">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-116">The context code.</span></span>
[<span data-ttu-id="b7b8f-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b7b8f-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="b7b8f-118">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="b7b8f-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b7b8f-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="b7b8f-120">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-120">The scan code.</span></span>
[<span data-ttu-id="b7b8f-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b7b8f-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="b7b8f-122">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-122">The previous key state.</span></span>

<span data-ttu-id="b7b8f-123">Consulte a documentação do WM_KEYDOWN para obter detalhes em [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="b7b8f-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="b7b8f-124">Parte</span><span class="sxs-lookup"><span data-stu-id="b7b8f-124">Members</span></span>

#### <span data-ttu-id="b7b8f-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b7b8f-125">IsExtendedKey</span></span> 

<span data-ttu-id="b7b8f-126">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="b7b8f-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="b7b8f-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="b7b8f-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b7b8f-128">IsKeyReleased</span></span> 

<span data-ttu-id="b7b8f-129">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-129">The transition state.</span></span>

> <span data-ttu-id="b7b8f-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="b7b8f-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="b7b8f-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b7b8f-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="b7b8f-132">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-132">The context code.</span></span>

> <span data-ttu-id="b7b8f-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="b7b8f-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="b7b8f-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b7b8f-134">RepeatCount</span></span> 

<span data-ttu-id="b7b8f-135">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="b7b8f-136">Public uint [repeatcount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="b7b8f-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="b7b8f-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b7b8f-137">ScanCode</span></span> 

<span data-ttu-id="b7b8f-138">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-138">The scan code.</span></span>

> <span data-ttu-id="b7b8f-139">Public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="b7b8f-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="b7b8f-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b7b8f-140">WasKeyDown</span></span> 

<span data-ttu-id="b7b8f-141">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="b7b8f-141">The previous key state.</span></span>

> <span data-ttu-id="b7b8f-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="b7b8f-142">public int [WasKeyDown](#waskeydown)</span></span>

