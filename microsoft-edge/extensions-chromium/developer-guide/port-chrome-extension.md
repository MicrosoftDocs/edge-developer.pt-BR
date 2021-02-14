---
description: Processo de portagem da extensão do Chrome para o Microsoft Edge.
title: Fazer a portabilidade da extensão do Chrome para o Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 64a92927b9fe7658562f87f326bb9ac148991031
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327691"
---
# <span data-ttu-id="87881-104">Fazer a portabilidade de sua extensão</span><span class="sxs-lookup"><span data-stu-id="87881-104">Port your extension</span></span>  

<span data-ttu-id="87881-105">O Microsoft Edge permite que você porte sua extensão do Chrome com alterações mínimas.</span><span class="sxs-lookup"><span data-stu-id="87881-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="87881-106">As APIs de extensão e as chaves de manifesto compatíveis com o Chrome são compatíveis com código com o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="87881-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="87881-107">Para uma lista de APIs com suporte no Microsoft Edge, navegue até o suporte [à API.][ExtensionApiSupport]</span><span class="sxs-lookup"><span data-stu-id="87881-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="87881-108">Para fazer a portabilidade da extensão do Chrome, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="87881-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="87881-109">Revise as APIs de extensão do Chrome usadas em suas extensões com a lista de APIs compatíveis com as [extensões do][ExtensionApiSupport] Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="87881-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="87881-110">Se sua extensão usa APIs que não são suportadas pelo Microsoft Edge, ela pode não fazer a portabilidade diretamente.</span><span class="sxs-lookup"><span data-stu-id="87881-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="87881-111">No arquivo de manifesto, de definir `update_URL` o campo como `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="87881-111">In the manifest file, set the `update_URL` field to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="87881-112">O valor aponta para o arquivo de sua extensão no armazenamento de Complementos do Microsoft Edge e permite que o Microsoft Edge verifique `.crx` se há atualizações de extensão.</span><span class="sxs-lookup"><span data-stu-id="87881-112">The value points to the `.crx` file of your extension in the Microsoft Edge Add-ons store and allows Microsoft Edge to check for extension updates.</span></span>  
1.  <span data-ttu-id="87881-113">Se for usado no nome ou na descrição da `Chrome` extensão, renomee sua extensão usando `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="87881-113">If `Chrome` is used in either the name or the description of your extension, rebrand your extension using `Microsoft Edge`.</span></span>  <span data-ttu-id="87881-114">Para passar no processo de certificação, as alterações são necessárias.</span><span class="sxs-lookup"><span data-stu-id="87881-114">To pass the certification process, the changes are required.</span></span>  
1.  <span data-ttu-id="87881-115">Teste sua extensão para verificar se ela funciona no Microsoft Edge [ao fazer sideload da extensão.][ExtensionsGettingStartedExtensionSideloading]</span><span class="sxs-lookup"><span data-stu-id="87881-115">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="87881-116">Se você enfrentar problemas, poderá depurar suas extensões no Microsoft Edge usando o DevTools ou [entre em contato conosco.][mailtoExtensionMicrosoft]</span><span class="sxs-lookup"><span data-stu-id="87881-116">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="87881-117">Siga as [diretrizes de publicação][ExtensionsPublishPublishExtension] para publicar sua extensão na loja de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="87881-117">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="87881-118">Se sua extensão trocar mensagens com um aplicativo nativo usando, certifique-se de definir como no arquivo de manifesto do host de `chrome.runtime.connectNative` `allowed_origins` mensagens `extension://[Microsoft-Catalog-extensionID]` nativo.</span><span class="sxs-lookup"><span data-stu-id="87881-118">If your extension exchanges messages with a native app using `chrome.runtime.connectNative`, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="87881-119">A configuração permite que o aplicativo identifique sua extensão.</span><span class="sxs-lookup"><span data-stu-id="87881-119">The setting allows the app to identify your extension.</span></span>  
    
## <span data-ttu-id="87881-120">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="87881-120">Next steps</span></span>  

<span data-ttu-id="87881-121">Depois que o pacote de extensão estiver pronto para ser publicado na loja de complementos do Microsoft [Edge,][ExtensionsPublishCreateDevAccount] crie uma conta de desenvolvedor e [publique sua extensão.][ExtensionsPublishPublishExtension]</span><span class="sxs-lookup"><span data-stu-id="87881-121">After your extension package is ready to publish in the Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Suporte à API | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Fazer o sideload da extensão | Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro de desenvolvedor | Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publique sua extensão | Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamento único | Desenvolvedor do Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
