---
description: Mover usuários para o Microsoft Edge do Internet Explorer
title: Mover usuários para o Microsoft Edge do Internet Explorer
author: MSEdgeTeam
ms.date: 11/04/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web, Internet Explorer
ms.openlocfilehash: 48f0f4121fb444d80603dcbb408397679c64753d
ms.sourcegitcommit: 7b4441b7656c8317139650f904b70cc87797d37e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154326"
---
# <span data-ttu-id="34baa-104">Mover usuários para o Microsoft Edge do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="34baa-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="34baa-105">Muitos sites modernos têm designs que são incompatíveis com o Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="34baa-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="34baa-106">Quando um usuário do IE visita um site público incompatível, o usuário pode receber uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="34baa-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="34baa-107">A mensagem informa que o site é incompatível com o navegador.</span><span class="sxs-lookup"><span data-stu-id="34baa-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="34baa-108">Depois que a mensagem é exibida, o usuário deve alternar manualmente para um navegador moderno.</span><span class="sxs-lookup"><span data-stu-id="34baa-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="34baa-109">Para minimizar as interrupções, começando com a versão 84, o Microsoft Edge aceita uma nova funcionalidade que redireciona os usuários automaticamente.</span><span class="sxs-lookup"><span data-stu-id="34baa-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="34baa-110">Quando um usuário do IE navega para um site que é incompatível com o IE, o Windows redireciona automaticamente o usuário para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="34baa-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="34baa-111">Para revisar os sites na lista, navegue até a [lista necessária do Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="34baa-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="34baa-112">Este artigo descreve os conceitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="34baa-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="34baa-113">A experiência do usuário para redirecionamento</span><span class="sxs-lookup"><span data-stu-id="34baa-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="34baa-114">Como adicionar seu site à lista de compatibilidade do IE</span><span class="sxs-lookup"><span data-stu-id="34baa-114">How to add your website to the IE compatibility list</span></span>  
*   <span data-ttu-id="34baa-115">Como remover seu site da lista de compatibilidade do IE</span><span class="sxs-lookup"><span data-stu-id="34baa-115">How to remove your website from the IE compatibility list</span></span>  
    
## <span data-ttu-id="34baa-116">Por que um site foi adicionado à lista de compatibilidade do IE?</span><span class="sxs-lookup"><span data-stu-id="34baa-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="34baa-117">A lista de compatibilidade do IE adiciona apenas um site quando as seguintes ações ocorrem.</span><span class="sxs-lookup"><span data-stu-id="34baa-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="34baa-118">Mostra um usuário do IE que uma mensagem sugerindo o usuário deve usar um navegador diferente por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="34baa-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="34baa-119">As solicitações de proprietário para adicionar o site à lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="34baa-119">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="34baa-120">Atualizar a lista de compatibilidade do IE</span><span class="sxs-lookup"><span data-stu-id="34baa-120">Update the IE compatibility list</span></span>  

<span data-ttu-id="34baa-121">A lista de compatibilidade do IE é um arquivo XML no [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="34baa-121">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="34baa-122">A lista é atualizada regularmente em resposta a solicitações de desenvolvedores de sites e usuários para que os sites sejam adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="34baa-122">The list is regularly updated in response to user's and website developers requests to have websites added or removed.</span></span>  <span data-ttu-id="34baa-123">As atualizações da lista são baixadas automaticamente para computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="34baa-123">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="34baa-124">Envie por email as informações a seguir para [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que o seu site seja adicionado ou removido da lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="34baa-124">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="34baa-125">Nome do proprietário</span><span class="sxs-lookup"><span data-stu-id="34baa-125">Owner name</span></span>  
*   <span data-ttu-id="34baa-126">Título corporativo</span><span class="sxs-lookup"><span data-stu-id="34baa-126">Corporate title</span></span>  
*   <span data-ttu-id="34baa-127">Email</span><span class="sxs-lookup"><span data-stu-id="34baa-127">Email address</span></span>  
*   <span data-ttu-id="34baa-128">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="34baa-128">Company name</span></span>  
*   <span data-ttu-id="34baa-129">Rua</span><span class="sxs-lookup"><span data-stu-id="34baa-129">Street address</span></span>  
*   <span data-ttu-id="34baa-130">Endereço do site</span><span class="sxs-lookup"><span data-stu-id="34baa-130">Website address</span></span>  
<!--  *   Telephone number  -->  
<!--  *   Target platform \(desktop, phone, Xbox\)  -->  
    
<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar um email para ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "É preciso ter o Microsoft Edge List v1 XML | Microsoft Edge"  
