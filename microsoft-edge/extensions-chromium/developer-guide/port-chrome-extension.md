---
description: Processo de portabilidade da extensão Chrome para o Microsoft Edge.
title: Extensão Chrome de porta para Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195156"
---
# <span data-ttu-id="3474b-104">Portar a extensão</span><span class="sxs-lookup"><span data-stu-id="3474b-104">Port your extension</span></span>  

<span data-ttu-id="3474b-105">O Microsoft Edge permite que você porte a extensão do Chrome com alterações mínimas.</span><span class="sxs-lookup"><span data-stu-id="3474b-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="3474b-106">As APIs de extensão e as chaves de manifesto aceitas pelo Chrome são compatíveis com o código com o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3474b-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="3474b-107">Para obter uma lista de APIs com suporte no Microsoft Edge, navegue até [suporte à API][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="3474b-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="3474b-108">Para portar sua extensão Chrome, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="3474b-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="3474b-109">Examine as APIs de extensão do Chrome usadas em suas extensões com a lista de [APIs com suporte][ExtensionApiSupport] do Microsoft Edge Extensions.</span><span class="sxs-lookup"><span data-stu-id="3474b-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3474b-110">Se sua extensão usa APIs que não são suportadas pelo Microsoft Edge, talvez não sejam portadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="3474b-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="3474b-111">Se o nome `Chrome` estiver sendo usado no nome ou na descrição da extensão, remarcando a extensão para `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="3474b-111">If the name `Chrome` is being used in either the name or the description of the extension, rebrand the extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="3474b-112">Esta etapa é necessária para passar no processo de certificação.</span><span class="sxs-lookup"><span data-stu-id="3474b-112">This step is required to pass the certification process.</span></span>  
1.  <span data-ttu-id="3474b-113">Teste sua extensão para verificar se ela funciona no Microsoft Edge por meio [de Sideload na extensão][ExtensionsGettingStartedExtensionSideloading].</span><span class="sxs-lookup"><span data-stu-id="3474b-113">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="3474b-114">Se enfrentar algum problema, você pode depurar as extensões no Microsoft Edge usando o DevTools ou [entrar em contato conosco][mailtoExtensionMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="3474b-114">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="3474b-115">Siga as [diretrizes de publicação][ExtensionsPublishPublishExtension] para publicar sua extensão no repositório Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3474b-115">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3474b-116">Se a extensão trocar mensagens com um aplicativo nativo usando `chrome.runtime.connectNative` API, certifique-se de que você definiu `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` no seu arquivo de manifesto do seu host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="3474b-116">If the extension exchanges messages with a native app using `chrome.runtime.connectNative` API, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="3474b-117">Isso permite que o aplicativo identifique a extensão.</span><span class="sxs-lookup"><span data-stu-id="3474b-117">This enables the app to identify the extension.</span></span>  
    
## <span data-ttu-id="3474b-118">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3474b-118">Next steps</span></span>  

<span data-ttu-id="3474b-119">Depois que o pacote de extensão estiver pronto para ser publicado no repositório Complementos do Microsoft Edge, [crie uma conta de desenvolvedor][ExtensionsPublishCreateDevAccount] e [publique a extensão][ExtensionsPublishPublishExtension].</span><span class="sxs-lookup"><span data-stu-id="3474b-119">Once your extension package is ready to be published to Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Suporte à API | Documentos da Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Sideload sua extensão | Documentos da Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro do desenvolvedor | Documentos da Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar sua extensão | Documentos da Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamentos de uso único | Desenvolvedor Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
