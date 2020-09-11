---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 17ed4a578234a056a7e6ff347829a12e39fa93bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010919"
---
# <span data-ttu-id="d2cc7-104">0.9.579-estrutura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="d2cc7-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="d2cc7-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d2cc7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d2cc7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d2cc7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d2cc7-107">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="d2cc7-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d2cc7-108">Summary</span></span>

 <span data-ttu-id="d2cc7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d2cc7-109">Members</span></span>                        | <span data-ttu-id="d2cc7-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d2cc7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2cc7-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="d2cc7-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="d2cc7-112">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="d2cc7-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="d2cc7-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="d2cc7-114">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-114">The transition state.</span></span>
[<span data-ttu-id="d2cc7-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="d2cc7-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="d2cc7-116">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-116">The context code.</span></span>
[<span data-ttu-id="d2cc7-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="d2cc7-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="d2cc7-118">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="d2cc7-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="d2cc7-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="d2cc7-120">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-120">The scan code.</span></span>
[<span data-ttu-id="d2cc7-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="d2cc7-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="d2cc7-122">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-122">The previous key state.</span></span>

<span data-ttu-id="d2cc7-123">Consulte a documentação do WM_KEYDOWN para obter detalhes em [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="d2cc7-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="d2cc7-124">Parte</span><span class="sxs-lookup"><span data-stu-id="d2cc7-124">Members</span></span>

#### <span data-ttu-id="d2cc7-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="d2cc7-125">IsExtendedKey</span></span> 

<span data-ttu-id="d2cc7-126">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="d2cc7-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="d2cc7-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="d2cc7-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="d2cc7-128">IsKeyReleased</span></span> 

<span data-ttu-id="d2cc7-129">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-129">The transition state.</span></span>

> <span data-ttu-id="d2cc7-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="d2cc7-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="d2cc7-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="d2cc7-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="d2cc7-132">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-132">The context code.</span></span>

> <span data-ttu-id="d2cc7-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="d2cc7-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="d2cc7-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="d2cc7-134">RepeatCount</span></span> 

<span data-ttu-id="d2cc7-135">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="d2cc7-136">Public uint [repeatcount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="d2cc7-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="d2cc7-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="d2cc7-137">ScanCode</span></span> 

<span data-ttu-id="d2cc7-138">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-138">The scan code.</span></span>

> <span data-ttu-id="d2cc7-139">Public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="d2cc7-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="d2cc7-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="d2cc7-140">WasKeyDown</span></span> 

<span data-ttu-id="d2cc7-141">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="d2cc7-141">The previous key state.</span></span>

> <span data-ttu-id="d2cc7-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="d2cc7-142">public int [WasKeyDown](#waskeydown)</span></span>

