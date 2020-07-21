---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 04c80d3319c74d3461666b6f35fadd0481b45207
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885531"
---
# <span data-ttu-id="533e2-104">Classe Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="533e2-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="533e2-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="533e2-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="533e2-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="533e2-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="533e2-107">Essa classe é um pacote dos parâmetros mais comuns usados para criar um CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="533e2-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="533e2-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="533e2-108">Summary</span></span>

 <span data-ttu-id="533e2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="533e2-109">Members</span></span>                        | <span data-ttu-id="533e2-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="533e2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="533e2-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="533e2-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="533e2-112">Obtém ou define o valor a ser passado como o parâmetro browserExecutableFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="533e2-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="533e2-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="533e2-113">Language</span></span>](#language) | <span data-ttu-id="533e2-114">Obtém ou define o valor a ser usado para a propriedade Language do parâmetro CoreWebView2EnvironmentOptions passado para CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="533e2-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="533e2-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="533e2-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="533e2-116">Obtém ou define o valor a ser passado como o parâmetro userDataFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="533e2-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="533e2-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="533e2-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="533e2-118">Cria uma nova instância de CoreWebView2CreationProperties com dados padrão para todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="533e2-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="533e2-119">Sua principal finalidade é definir como [WebView2. creationproperties](microsoft-web-webview2-wpf-webview2.md) para personalizar o ambiente usado por um [WebView2](microsoft-web-webview2-wpf-webview2.md) durante a inicialização implícita.</span><span class="sxs-lookup"><span data-stu-id="533e2-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="533e2-120">Também é um excelente utilitário de integração do WPF que permite que os parâmetros de ambiente comumente usados sejam Propriedades de dependência e sejam criados e usados na marcação.</span><span class="sxs-lookup"><span data-stu-id="533e2-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="533e2-121">Essa classe não deve conter todas as opções de personalização de ambiente possíveis.</span><span class="sxs-lookup"><span data-stu-id="533e2-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="533e2-122">Se precisar de controle total sobre o ambiente usado por um controle WebView2, você precisará inicializar o controle explicitamente criando seu próprio ambiente com CoreWebView2Environment. createasync e transmitindo-o para [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de definir a propriedade [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="533e2-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="533e2-123">Consulte a documentação da classe [WebView2](microsoft-web-webview2-wpf-webview2.md) para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="533e2-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="533e2-124">Parte</span><span class="sxs-lookup"><span data-stu-id="533e2-124">Members</span></span>

#### <span data-ttu-id="533e2-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="533e2-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="533e2-126">Obtém ou define o valor a ser passado como o parâmetro browserExecutableFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="533e2-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="533e2-127">Cadeia de caracteres pública [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="533e2-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="533e2-128">Idioma</span><span class="sxs-lookup"><span data-stu-id="533e2-128">Language</span></span> 

<span data-ttu-id="533e2-129">Obtém ou define o valor a ser usado para a propriedade Language do parâmetro CoreWebView2EnvironmentOptions passado para CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="533e2-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="533e2-130">[linguagem](#language) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="533e2-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="533e2-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="533e2-131">UserDataFolder</span></span> 

<span data-ttu-id="533e2-132">Obtém ou define o valor a ser passado como o parâmetro userDataFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="533e2-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="533e2-133">Cadeia de caracteres pública [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="533e2-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="533e2-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="533e2-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="533e2-135">Cria uma nova instância de CoreWebView2CreationProperties com dados padrão para todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="533e2-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="533e2-136">[CoreWebView2CreationProperties](#corewebview2creationproperties)público ()</span><span class="sxs-lookup"><span data-stu-id="533e2-136">public [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

