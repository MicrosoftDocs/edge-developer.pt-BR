---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Saiba como você pode usar o recurso de mensagens nativas para que sua extensão se comunique com um aplicativo UWP complementar.
title: Extensões-pacotes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 23c97f366db527cae2672d6ad46fa666583f6398
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561191"
---
# <span data-ttu-id="4057b-104">Empacotando extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4057b-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="4057b-105">Por fim, você concluiu a extensão e está pronto para empacotá-la.</span><span class="sxs-lookup"><span data-stu-id="4057b-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="4057b-106">Você pode estar se perguntando quais são as próximas etapas para obter isso em mãos de usuários em potencial.</span><span class="sxs-lookup"><span data-stu-id="4057b-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="4057b-107">Este guia destina-se a ensinar como fazer exatamente isso.</span><span class="sxs-lookup"><span data-stu-id="4057b-107">This guide is intended to teach you how to do just that.</span></span>

<span data-ttu-id="4057b-108">O guia de empacotamento de extensão é abrangente, pois ele abrange tudo o que você gostaria de saber sobre empacotamento, até mesmo os detalhes detalhados.</span><span class="sxs-lookup"><span data-stu-id="4057b-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="4057b-109">Se você não quiser aprender tudo que precisa saber sobre o empacotamento da extensão, você está com sorte.</span><span class="sxs-lookup"><span data-stu-id="4057b-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="4057b-110">Adicionamos suporte para extensões ao ManifoldJS, uma ferramenta de nó de código-fonte Open. js que usa a maioria do seu pacote de Woes ausente.</span><span class="sxs-lookup"><span data-stu-id="4057b-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>

> [!NOTE]
> <span data-ttu-id="4057b-111">No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="4057b-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="4057b-112">Entre [em contato conosco](https://aka.ms/extension-request) com suas solicitações para fazer parte da Microsoft Store, e consideraremos você para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="4057b-112">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>


<span data-ttu-id="4057b-113">Use a estrutura de tópicos do processo abaixo para mapear sua aventura de embalagem!</span><span class="sxs-lookup"><span data-stu-id="4057b-113">Use the process outline below to map out your packaging adventure!</span></span>


## [<span data-ttu-id="4057b-114">Extensões no centro de desenvolvimento do Windows</span><span class="sxs-lookup"><span data-stu-id="4057b-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)

<span data-ttu-id="4057b-115">Não importa qual rota de criação de pacotes você escolhe, manual ou ManifoldJS, a primeira etapa é registrar-se para uma conta de desenvolvedor do Windows e reservar o (s) nome (s) de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="4057b-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>

<span data-ttu-id="4057b-116">Depois de fazer isso, você pode se mover para [criar e testar pacotes de extensão](./packaging/creating-and-testing-extension-packages.md) para saber como o AppXs é criado e empacotar manualmente a extensão ou ir para a rota mais fácil e ir para [usar o ManifoldJS para extensões de pacote](./packaging/using-ManifoldJS-to-package-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4057b-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4057b-117">Depois que tiver chegado para nós e tiver sido aprovado para ter sua extensão na Microsoft Store, confira a lista de [verificação de envio de aplicativo](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span><span class="sxs-lookup"><span data-stu-id="4057b-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>


## [<span data-ttu-id="4057b-118">Criando e testando pacotes de extensão</span><span class="sxs-lookup"><span data-stu-id="4057b-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)

<span data-ttu-id="4057b-119">Esta seção do guia percorre a criação manual do pacote de extensão após a [configuração da sua conta de desenvolvedor do Windows e reservava o nome (s) da extensão](./packaging/extensions-in-the-windows-Dev-Center.md).</span><span class="sxs-lookup"><span data-stu-id="4057b-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="4057b-120">Se você está curioso para ver os detalhes mais finos do empacotamento de uma extensão, faça uma leitura.</span><span class="sxs-lookup"><span data-stu-id="4057b-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>

<span data-ttu-id="4057b-121">Também está incluída informações sobre como [testar e descompactar uma extensão empacotada](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span><span class="sxs-lookup"><span data-stu-id="4057b-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="4057b-122">Essas informações são relevantes mesmo que você tenha saído da rota de embalagem do ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="4057b-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>

## [<span data-ttu-id="4057b-123">Localizando pacotes de extensão</span><span class="sxs-lookup"><span data-stu-id="4057b-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)
<span data-ttu-id="4057b-124">A etapa de localização do pacote cai entre a criação do arquivo appxmanifest. xml e a execução do comando final para empacotar a extensão.</span><span class="sxs-lookup"><span data-stu-id="4057b-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>
<span data-ttu-id="4057b-125">Isso permite que você indique quais idiomas são compatíveis com as suas extensões na listagem da Microsoft Store e em qual idioma o nome da extensão é exibido no Windows.</span><span class="sxs-lookup"><span data-stu-id="4057b-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>

<span data-ttu-id="4057b-126">Você pode ir para [localizar o nome e a descrição da Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) nesta seção do guia se a extensão não oferecer suporte a vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="4057b-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>

## [<span data-ttu-id="4057b-127">Usar o ManifoldJS para extensões de pacote</span><span class="sxs-lookup"><span data-stu-id="4057b-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)

<span data-ttu-id="4057b-128">A rota da ferramenta para empacotar sua extensão, o ManifoldJS irá empacotar a extensão em um encaixe com o mínimo de esforço no seu fim.</span><span class="sxs-lookup"><span data-stu-id="4057b-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="4057b-129">Forneça alguns ativos Windows/Microsoft Store após preencher algumas propriedades de AppXManifest, e sua extensão será empacotada em qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="4057b-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>

<span data-ttu-id="4057b-130">Depois que sua extensão estiver empacotada, consulte a seção [teste](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de como criar e testar a extensão do Microsoft Edge para saber como Sideload-la ou desempacotá-la.</span><span class="sxs-lookup"><span data-stu-id="4057b-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>


## [<span data-ttu-id="4057b-131">Executando o kit de certificação de aplicativos Windows</span><span class="sxs-lookup"><span data-stu-id="4057b-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)

<span data-ttu-id="4057b-132">Depois que você tiver uma extensão empacotada, poderá executá-la por meio do kit de certificação de aplicativos Windows.</span><span class="sxs-lookup"><span data-stu-id="4057b-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="4057b-133">Isso fará com que vários testes sejam executados em seu pacote de extensão para garantir que ele esteja pronto para a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="4057b-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>
