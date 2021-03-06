---
description: Saiba mais sobre como você pode empacotá-la.
title: Extensões - Empacotamento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398494"
---
# <a name="packaging-microsoft-edge-extensions"></a><span data-ttu-id="5e478-104">Empacotando extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5e478-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="5e478-105">Portanto, você finalmente concluiu sua extensão e está pronto para empacotá-la.</span><span class="sxs-lookup"><span data-stu-id="5e478-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="5e478-106">Você pode estar se perguntando quais são as próximas etapas para obter isso nas mãos de usuários em potencial.</span><span class="sxs-lookup"><span data-stu-id="5e478-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="5e478-107">Este guia destina-se a ensinar como fazer exatamente isso.</span><span class="sxs-lookup"><span data-stu-id="5e478-107">This guide is intended to teach you how to do just that.</span></span>  

<span data-ttu-id="5e478-108">O guia de empacotamento de extensão é abrangente, já que aborda tudo o que você gostaria de saber sobre empacotamento, mesmo os detalhes mais finos e abrangentes.</span><span class="sxs-lookup"><span data-stu-id="5e478-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="5e478-109">Se você não quiser saber tudo o que há para saber sobre como empacotar sua extensão, você está com sorte.</span><span class="sxs-lookup"><span data-stu-id="5e478-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="5e478-110">Adicionamos suporte para extensões ao ManifoldJS, uma ferramenta de Node.js de código aberto que tira a maioria dos problemas de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="5e478-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>  

> [!NOTE]
> <span data-ttu-id="5e478-111">No momento, enviar uma extensão do Microsoft Edge à Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="5e478-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="5e478-112">[Entre em contato conosco com](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) suas solicitações para fazer parte da Microsoft Store e consideraremos você para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="5e478-112">[Reach out to us](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>  

<span data-ttu-id="5e478-113">Use o contorno do processo abaixo para mapear sua aventura de empacotamento!</span><span class="sxs-lookup"><span data-stu-id="5e478-113">Use the process outline below to map out your packaging adventure!</span></span>  

## [<a name="extensions-in-the-windows-dev-center"></a><span data-ttu-id="5e478-114">Extensões no Centro de Desenvolvimento do Windows</span><span class="sxs-lookup"><span data-stu-id="5e478-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)  

<span data-ttu-id="5e478-115">Independentemente de qual rota de criação de pacote você escolher, manual ou ManifoldJS, a primeira etapa é registrar uma conta do Desenvolvedor do Windows e reservar os nomes da extensão.</span><span class="sxs-lookup"><span data-stu-id="5e478-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>  

<span data-ttu-id="5e478-116">Depois de fazer isso, você pode [](./packaging/creating-and-testing-extension-packages.md) ir para Criar e testar pacotes de extensão para saber como os AppXs são criados e empacotar manualmente sua extensão, ou ir para a rota mais fácil e ir para [Usando ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)para extensões de pacote.</span><span class="sxs-lookup"><span data-stu-id="5e478-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="5e478-117">Depois de entrar em contato conosco e ter sido aprovado para ter sua extensão na Microsoft Store, confira a lista de verificação de [envio de aplicativos](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span><span class="sxs-lookup"><span data-stu-id="5e478-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>  


## [<a name="creating-and-testing-extension-packages"></a><span data-ttu-id="5e478-118">Criar e testar pacotes de extensão</span><span class="sxs-lookup"><span data-stu-id="5e478-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)  

<span data-ttu-id="5e478-119">Esta seção do guia percorre a criação manual do pacote de extensão depois que você configurar sua conta do Desenvolvedor do Windows e reservou seus nomes [de extensão.](./packaging/extensions-in-the-windows-Dev-Center.md)</span><span class="sxs-lookup"><span data-stu-id="5e478-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="5e478-120">Se você estiver curioso sobre os detalhes mais finos de empacotamento de uma extensão, leia isso.</span><span class="sxs-lookup"><span data-stu-id="5e478-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>  

<span data-ttu-id="5e478-121">Também estão incluídas informações sobre como testar [e desempacotar uma extensão empacotada.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)</span><span class="sxs-lookup"><span data-stu-id="5e478-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="5e478-122">Essas informações são relevantes mesmo que você tenha feito a rota de empacotamento ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="5e478-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>  

## [<a name="localizing-extension-packages"></a><span data-ttu-id="5e478-123">Localizando pacotes de extensão</span><span class="sxs-lookup"><span data-stu-id="5e478-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)  

<span data-ttu-id="5e478-124">A etapa de localização do pacote se enquadra entre a criação do arquivo appxmanifest.xml e a execução do comando final para empacotar sua extensão.</span><span class="sxs-lookup"><span data-stu-id="5e478-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>  
<span data-ttu-id="5e478-125">Isso permite que você indique quais idiomas suas extensões suportam na listagem da Microsoft Store e qual idioma o nome da sua extensão aparece no Windows.</span><span class="sxs-lookup"><span data-stu-id="5e478-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>  

<span data-ttu-id="5e478-126">Você pode ir [para Localização de nome](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) e descrição para a Microsoft Store nesta seção do guia se sua extensão não dá suporte a vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="5e478-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>  

## [<a name="using-manifoldjs-to-package-extensions"></a><span data-ttu-id="5e478-127">Usar ManifoldJS para extensões de pacote</span><span class="sxs-lookup"><span data-stu-id="5e478-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)  

<span data-ttu-id="5e478-128">A rota da ferramenta para empacotar sua extensão, ManifoldJS empacota sua extensão em um snap com o mínimo esforço em sua extremidade.</span><span class="sxs-lookup"><span data-stu-id="5e478-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="5e478-129">Forneça alguns ativos da Windows/Microsoft Store depois de preencher algumas propriedades do AppXManifest e sua extensão será empacotada em pouco tempo.</span><span class="sxs-lookup"><span data-stu-id="5e478-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>  

<span data-ttu-id="5e478-130">Depois que sua extensão for [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) empacotada, consulte a seção de teste de Criação e teste da extensão do Microsoft Edge para saber como fazer sideload ou desempacotar.</span><span class="sxs-lookup"><span data-stu-id="5e478-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>  

## [<a name="running-the-windows-app-certification-kit"></a><span data-ttu-id="5e478-131">Executar o Kit de Certificação de Aplicativos Windows</span><span class="sxs-lookup"><span data-stu-id="5e478-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)  

<span data-ttu-id="5e478-132">Depois de ter uma extensão empacotada, você pode, em seguida, execute-a por meio do Kit de Certificação de Aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="5e478-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="5e478-133">Isso executará vários testes no pacote de extensão para garantir que ele esteja pronto para a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5e478-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>  
