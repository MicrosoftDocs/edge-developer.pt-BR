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
ms.openlocfilehash: e0fb3f9ff7114b0c4f2a42893adabfd72e9616de
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698238"
---
# <span data-ttu-id="84b1c-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="84b1c-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="84b1c-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="84b1c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="84b1c-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="84b1c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="84b1c-107">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="84b1c-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="84b1c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="84b1c-108">Summary</span></span>

 <span data-ttu-id="84b1c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="84b1c-109">Members</span></span>                        | <span data-ttu-id="84b1c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="84b1c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="84b1c-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="84b1c-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="84b1c-112">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="84b1c-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="84b1c-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="84b1c-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="84b1c-114">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="84b1c-114">The transition state.</span></span>
[<span data-ttu-id="84b1c-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="84b1c-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="84b1c-116">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="84b1c-116">The context code.</span></span>
[<span data-ttu-id="84b1c-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="84b1c-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="84b1c-118">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="84b1c-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="84b1c-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="84b1c-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="84b1c-120">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="84b1c-120">The scan code.</span></span>
[<span data-ttu-id="84b1c-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="84b1c-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="84b1c-122">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="84b1c-122">The previous key state.</span></span>

<span data-ttu-id="84b1c-123">Consulte a documentação do WM_KEYDOWN para obter detalhes em [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="84b1c-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="84b1c-124">Parte</span><span class="sxs-lookup"><span data-stu-id="84b1c-124">Members</span></span>

#### <span data-ttu-id="84b1c-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="84b1c-125">IsExtendedKey</span></span> 

<span data-ttu-id="84b1c-126">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="84b1c-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="84b1c-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="84b1c-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="84b1c-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="84b1c-128">IsKeyReleased</span></span> 

<span data-ttu-id="84b1c-129">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="84b1c-129">The transition state.</span></span>

> <span data-ttu-id="84b1c-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="84b1c-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="84b1c-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="84b1c-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="84b1c-132">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="84b1c-132">The context code.</span></span>

> <span data-ttu-id="84b1c-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="84b1c-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="84b1c-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="84b1c-134">RepeatCount</span></span> 

<span data-ttu-id="84b1c-135">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="84b1c-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="84b1c-136">Public uint [repeatcount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="84b1c-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="84b1c-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="84b1c-137">ScanCode</span></span> 

<span data-ttu-id="84b1c-138">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="84b1c-138">The scan code.</span></span>

> <span data-ttu-id="84b1c-139">Public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="84b1c-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="84b1c-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="84b1c-140">WasKeyDown</span></span> 

<span data-ttu-id="84b1c-141">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="84b1c-141">The previous key state.</span></span>

> <span data-ttu-id="84b1c-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="84b1c-142">public int [WasKeyDown](#waskeydown)</span></span>

