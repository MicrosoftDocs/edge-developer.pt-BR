---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: bd63bda6b7835ff5edb30b8b1b22f877f4c96e14
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697592"
---
# <span data-ttu-id="99262-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="99262-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="99262-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="99262-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="99262-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="99262-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="99262-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="99262-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="99262-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="99262-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="99262-109">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="99262-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="99262-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="99262-110">Summary</span></span>

 <span data-ttu-id="99262-111">Parte</span><span class="sxs-lookup"><span data-stu-id="99262-111">Members</span></span>                        | <span data-ttu-id="99262-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="99262-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99262-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="99262-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="99262-114">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="99262-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="99262-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="99262-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="99262-116">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="99262-116">The transition state.</span></span>
[<span data-ttu-id="99262-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="99262-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="99262-118">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="99262-118">The context code.</span></span>
[<span data-ttu-id="99262-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="99262-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="99262-120">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="99262-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="99262-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="99262-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="99262-122">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="99262-122">The scan code.</span></span>
[<span data-ttu-id="99262-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="99262-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="99262-124">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="99262-124">The previous key state.</span></span>

<span data-ttu-id="99262-125">Consulte a documentação do WM_KEYDOWN para obter detalhes em [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="99262-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="99262-126">Parte</span><span class="sxs-lookup"><span data-stu-id="99262-126">Members</span></span>

#### <span data-ttu-id="99262-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="99262-127">IsExtendedKey</span></span> 

<span data-ttu-id="99262-128">Indica se a chave é uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="99262-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="99262-129">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="99262-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="99262-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="99262-130">IsKeyReleased</span></span> 

<span data-ttu-id="99262-131">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="99262-131">The transition state.</span></span>

> <span data-ttu-id="99262-132">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="99262-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="99262-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="99262-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="99262-134">O código de contexto.</span><span class="sxs-lookup"><span data-stu-id="99262-134">The context code.</span></span>

> <span data-ttu-id="99262-135">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="99262-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="99262-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="99262-136">RepeatCount</span></span> 

<span data-ttu-id="99262-137">A contagem de repetição para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="99262-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="99262-138">Public uint [repeatcount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="99262-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="99262-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="99262-139">ScanCode</span></span> 

<span data-ttu-id="99262-140">O código de digitalização.</span><span class="sxs-lookup"><span data-stu-id="99262-140">The scan code.</span></span>

> <span data-ttu-id="99262-141">Public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="99262-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="99262-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="99262-142">WasKeyDown</span></span> 

<span data-ttu-id="99262-143">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="99262-143">The previous key state.</span></span>

> <span data-ttu-id="99262-144">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="99262-144">public int [WasKeyDown](#waskeydown)</span></span>

