---
description: Processo de portabilidade da extensão Chrome para o Microsoft Edge.
title: Extensão do Chrome de porta para a Microsoft (Chromium) Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 794e8806a95ce0a70069c65c306c30131b01e24d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561312"
---
# <span data-ttu-id="78219-104">Extensão Chrome de porta para a Microsoft \ (Chromium \) Edge</span><span class="sxs-lookup"><span data-stu-id="78219-104">Port Chrome Extension To Microsoft \(Chromium\) Edge</span></span>  

<span data-ttu-id="78219-105">O processo de portabilidade de uma extensão do Chrome para o Microsoft Edge é muito simples.</span><span class="sxs-lookup"><span data-stu-id="78219-105">The process of porting a Chrome Extension to Microsoft Edge is very straightforward.</span></span>  <span data-ttu-id="78219-106">Extensões escritas para Chromium, na maioria dos casos, são executadas no Microsoft Edge com alterações mínimas.</span><span class="sxs-lookup"><span data-stu-id="78219-106">Extensions written for Chromium, in most cases, run on Microsoft Edge with minimal changes.</span></span>  <span data-ttu-id="78219-107">As APIs de extensão e as chaves de manifesto aceitas pelo Chrome são compatíveis com o código com o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="78219-107">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="78219-108">No entanto, o Microsoft Edge não é compatível com as seguintes APIs de extensão:</span><span class="sxs-lookup"><span data-stu-id="78219-108">However, Microsoft Edge does not support the following Extension APIs:</span></span>  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> <span data-ttu-id="78219-109">O usuário deve estar conectado ao Microsoft Edge usando uma conta do MSA ou AAD para usar a `chrome.identity.getProfileUserInfo` API.</span><span class="sxs-lookup"><span data-stu-id="78219-109">The user must be signed into Microsoft Edge using an MSA or AAD account in order to use the `chrome.identity.getProfileUserInfo` API.</span></span>  <span data-ttu-id="78219-110">Se o usuário estiver conectado ao Microsoft Edge usando o **anúncio local**, a API retornará `null` para os valores de email e ID.</span><span class="sxs-lookup"><span data-stu-id="78219-110">If the user is signed into Microsoft Edge using **On-premise AD**, the API returns `null` for the email and ID values.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="78219-111">**Pagamentos**: o Microsoft Edge não oferece suporte direto a uma extensão que use [pagamentos da loja da Web Chrome][ChromeDeveloperWebStorePayments] devido à necessidade de usar a `identity.getAuthtoken` solicitação para obter o token para que os usuários conectados enviem a solicitação de API de licenciamento baseado em REST.</span><span class="sxs-lookup"><span data-stu-id="78219-111">**Payments**:  Microsoft Edge does not directly support an Extension that uses [Chrome Web Store payments][ChromeDeveloperWebStorePayments] due to the requirement to use the `identity.getAuthtoken` request to get the token for signed-in users to send the REST-based licensing API request.</span></span>  <span data-ttu-id="78219-112">O Microsoft Edge não é compatível com a `getAuthtoken` solicitação, portanto, esse fluxo não funciona.</span><span class="sxs-lookup"><span data-stu-id="78219-112">Microsoft Edge does not support the `getAuthtoken` request, so this flow does not work.</span></span>  

<span data-ttu-id="78219-113">Para portar a sua extensão Chrome, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="78219-113">To port your Chrome Extension, follow these steps:</span></span>  

1.  <span data-ttu-id="78219-114">Examine as APIs de extensão do Chrome usadas nas extensões.</span><span class="sxs-lookup"><span data-stu-id="78219-114">Review the Chrome Extension APIs used in your Extensions.</span></span>  <span data-ttu-id="78219-115">Se você estiver usando recursos ou APIs que não são compatíveis com o Microsoft Edge, talvez não seja possível portar a extensão.</span><span class="sxs-lookup"><span data-stu-id="78219-115">If you are using features or APIs that are not supported by Microsoft Edge, you may not be able to port your Extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="78219-116">A `getAuthToken` API não funciona com o Microsoft Edge, mas você pode usar `launchWebAuthFlow` para buscar um token OAuth2 para autenticar usuários.</span><span class="sxs-lookup"><span data-stu-id="78219-116">The `getAuthToken` API does not work with Microsoft Edge, however you may use `launchWebAuthFlow` to fetch an OAuth2 token to authenticate users.</span></span>  
    
1.  <span data-ttu-id="78219-117">Se você estiver usando `Chrome` no nome ou na descrição da extensão, remarcando a extensão para `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="78219-117">If you are using `Chrome` in the name or description of your Extension, re-brand the Extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="78219-118">Você deve passar no processo de certificação.</span><span class="sxs-lookup"><span data-stu-id="78219-118">You must pass the certification process.</span></span>  
    
1.  <span data-ttu-id="78219-119">Teste sua extensão para verificar se ela funciona no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="78219-119">Test your Extension to check if it works in Microsoft Edge.</span></span>  <span data-ttu-id="78219-120">A primeira etapa para fazer isso é garantir que você tenha recursos de desenvolvedor de extensão ativados.</span><span class="sxs-lookup"><span data-stu-id="78219-120">The first step to do this is to ensure that you have Extension developer features turned on.</span></span>  <span data-ttu-id="78219-121">Isso permite que você carregue arquivos de extensão no Microsoft Edge para poder testar a extensão durante o seu desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="78219-121">This enables you to side load Extension files in Microsoft Edge so that you are able to test your Extension while developing it.</span></span>  
    
1.  <span data-ttu-id="78219-122">Se tiver problemas, depure as extensões no Microsoft Edge usando o DevTools ou [entre em contato conosco][mailtoExtensionPartnerOpsMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="78219-122">If you have any issues, debug your Extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionPartnerOpsMicrosoft].</span></span>  
    
1.  <span data-ttu-id="78219-123">Agora, a extensão é refinada e está pronta para ser empacotada.</span><span class="sxs-lookup"><span data-stu-id="78219-123">Now your Extension is finally polished up and ready to be packaged.</span></span>  <span data-ttu-id="78219-124">Se você quiser se preparar para enviar para o catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \), não será necessário empacotar a extensão.</span><span class="sxs-lookup"><span data-stu-id="78219-124">If you wish to prepare for submission to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\), you do not need to package your Extension.</span></span>  <span data-ttu-id="78219-125">Além disso, siga nossas [diretrizes de publicação][ExtensionsPublishExtension] para publicar sua extensão em Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="78219-125">Further, follow our [publishing guidelines][ExtensionsPublishExtension] to publish your Extension on Microsoft Edge Addons.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="78219-126">Se sua extensão trocar mensagens com um aplicativo nativo usando `chrome.runtime.connectNative` API, certifique-se de que você definiu `allowedorigins` para " `extension://[Microsoft-Catalog-extensionID]` " em seu arquivo de manifesto do seu host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="78219-126">If your Extension exchanges messages with a native application using `chrome.runtime.connectNative` API, ensure that you set `allowedorigins` to "`extension://[Microsoft-Catalog-extensionID]`" in your native messaging host manifest file.</span></span>  <span data-ttu-id="78219-127">Isso permite que o aplicativo identifique a extensão.</span><span class="sxs-lookup"><span data-stu-id="78219-127">This enables the app to identify the Extension.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Publicar uma extensão"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamentos unidirecionais-Google Chrome"  
