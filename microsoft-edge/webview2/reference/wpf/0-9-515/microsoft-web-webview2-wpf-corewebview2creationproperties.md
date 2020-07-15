---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 72c85df7d2d58d74cf27e04eb7128fdfa14ca2d9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880252"
---
# <span data-ttu-id="5982c-104">Classe Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="5982c-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="5982c-105">Namespace: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="5982c-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="5982c-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="5982c-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="5982c-107">Essa classe é um pacote dos parâmetros mais comuns usados para criar um CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="5982c-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="5982c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="5982c-108">Summary</span></span>

 <span data-ttu-id="5982c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5982c-109">Members</span></span>                        | <span data-ttu-id="5982c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="5982c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5982c-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="5982c-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="5982c-112">Obtém ou define o valor a ser passado como o parâmetro browserExecutableFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="5982c-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="5982c-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="5982c-113">Language</span></span>](#language) | <span data-ttu-id="5982c-114">Obtém ou define o valor a ser usado para a propriedade Language do parâmetro CoreWebView2EnvironmentOptions passado para CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="5982c-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="5982c-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="5982c-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="5982c-116">Obtém ou define o valor a ser passado como o parâmetro userDataFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="5982c-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="5982c-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="5982c-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="5982c-118">Cria uma nova instância de CoreWebView2CreationProperties com dados padrão para todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="5982c-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="5982c-119">Sua principal finalidade é definir como [WebView2. creationproperties](microsoft-web-webview2-wpf-webview2.md) para personalizar o ambiente usado por um [WebView2](microsoft-web-webview2-wpf-webview2.md) durante a inicialização implícita.</span><span class="sxs-lookup"><span data-stu-id="5982c-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="5982c-120">Também é um excelente utilitário de integração do WPF que permite que os parâmetros de ambiente comumente usados sejam Propriedades de dependência e sejam criados e usados na marcação.</span><span class="sxs-lookup"><span data-stu-id="5982c-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="5982c-121">Essa classe não deve conter todas as opções de personalização de ambiente possíveis.</span><span class="sxs-lookup"><span data-stu-id="5982c-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="5982c-122">Se precisar de controle total sobre o ambiente usado por um controle WebView2, você precisará inicializar o controle explicitamente criando seu próprio ambiente com CoreWebView2Environment. createasync e transmitindo-o para [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de definir a propriedade [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="5982c-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="5982c-123">Consulte a documentação da classe [WebView2](microsoft-web-webview2-wpf-webview2.md) para obter uma visão geral de inicialização.</span><span class="sxs-lookup"><span data-stu-id="5982c-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="5982c-124">Parte</span><span class="sxs-lookup"><span data-stu-id="5982c-124">Members</span></span>

#### <span data-ttu-id="5982c-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="5982c-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="5982c-126">Obtém ou define o valor a ser passado como o parâmetro browserExecutableFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="5982c-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="5982c-127">Cadeia de caracteres pública [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="5982c-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="5982c-128">Idioma</span><span class="sxs-lookup"><span data-stu-id="5982c-128">Language</span></span> 

<span data-ttu-id="5982c-129">Obtém ou define o valor a ser usado para a propriedade Language do parâmetro CoreWebView2EnvironmentOptions passado para CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="5982c-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="5982c-130">[linguagem](#language) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="5982c-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="5982c-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="5982c-131">UserDataFolder</span></span> 

<span data-ttu-id="5982c-132">Obtém ou define o valor a ser passado como o parâmetro userDataFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.</span><span class="sxs-lookup"><span data-stu-id="5982c-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="5982c-133">Cadeia de caracteres pública [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="5982c-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="5982c-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="5982c-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="5982c-135">Cria uma nova instância de CoreWebView2CreationProperties com dados padrão para todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="5982c-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="5982c-136">[CoreWebView2CreationProperties](#corewebview2creationproperties)público ()</span><span class="sxs-lookup"><span data-stu-id="5982c-136">public  [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

