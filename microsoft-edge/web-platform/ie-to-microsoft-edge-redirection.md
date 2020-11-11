---
description: Mover usuários para o Microsoft Edge do Internet Explorer
title: Mover usuários para o Microsoft Edge do Internet Explorer
author: MSEdgeTeam
ms.date: 11/06/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web, Internet Explorer
ms.openlocfilehash: 2e1488359e405247e290ad8f6300c480a7e20af6
ms.sourcegitcommit: 6ef48c8cda392c6bf8217cff5f696ac620d10739
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163207"
---
# <span data-ttu-id="41b43-104">Mover usuários para o Microsoft Edge do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="41b43-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="41b43-105">Muitos sites modernos têm designs que são incompatíveis com o Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="41b43-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="41b43-106">Quando um usuário do IE visita um site público incompatível, o usuário pode receber uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="41b43-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="41b43-107">A mensagem informa que o site é incompatível com o navegador.</span><span class="sxs-lookup"><span data-stu-id="41b43-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="41b43-108">Depois que a mensagem é exibida, o usuário deve alternar manualmente para um navegador moderno.</span><span class="sxs-lookup"><span data-stu-id="41b43-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="41b43-109">Para minimizar as interrupções, começando com a versão 84, o Microsoft Edge aceita uma nova funcionalidade que redireciona os usuários automaticamente.</span><span class="sxs-lookup"><span data-stu-id="41b43-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="41b43-110">Quando um usuário do IE navega para um site que é incompatível com o IE, o Windows redireciona automaticamente o usuário para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="41b43-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="41b43-111">Para revisar os sites na lista, navegue até a [lista necessária do Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="41b43-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="41b43-112">Este artigo descreve os conceitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="41b43-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="41b43-113">A experiência do usuário para redirecionamento</span><span class="sxs-lookup"><span data-stu-id="41b43-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="41b43-114">Como solicitar uma atualização à lista</span><span class="sxs-lookup"><span data-stu-id="41b43-114">How to request an update to the list</span></span>  
    
## <span data-ttu-id="41b43-115">Por que um site foi adicionado à lista de compatibilidade do IE?</span><span class="sxs-lookup"><span data-stu-id="41b43-115">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="41b43-116">A lista de compatibilidade do IE adiciona apenas um site quando as seguintes ações ocorrem.</span><span class="sxs-lookup"><span data-stu-id="41b43-116">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="41b43-117">Mostra um usuário do IE que uma mensagem sugerindo o usuário deve usar um navegador diferente por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="41b43-117">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="41b43-118">As solicitações de proprietário para adicionar o site à lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="41b43-118">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="41b43-119">Atualizar a lista de compatibilidade do IE</span><span class="sxs-lookup"><span data-stu-id="41b43-119">Update the IE compatibility list</span></span>  

<span data-ttu-id="41b43-120">A lista de compatibilidade do IE é um arquivo XML no [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="41b43-120">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="41b43-121">A lista é atualizada regularmente em resposta a solicitações de desenvolvedor de usuário e de site para que os sites sejam adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="41b43-121">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="41b43-122">As atualizações da lista são baixadas automaticamente para computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="41b43-122">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="41b43-123">Envie por email as informações a seguir para [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que o seu site seja adicionado ou removido da lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="41b43-123">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="41b43-124">Nome do proprietário</span><span class="sxs-lookup"><span data-stu-id="41b43-124">Owner name</span></span>  
*   <span data-ttu-id="41b43-125">Título corporativo</span><span class="sxs-lookup"><span data-stu-id="41b43-125">Corporate title</span></span>  
*   <span data-ttu-id="41b43-126">Email</span><span class="sxs-lookup"><span data-stu-id="41b43-126">Email address</span></span>  
*   <span data-ttu-id="41b43-127">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="41b43-127">Company name</span></span>  
*   <span data-ttu-id="41b43-128">Rua</span><span class="sxs-lookup"><span data-stu-id="41b43-128">Street address</span></span>  
*   <span data-ttu-id="41b43-129">Endereço do site</span><span class="sxs-lookup"><span data-stu-id="41b43-129">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="41b43-130">A lista de compatibilidade do IE foi projetada para funcionar somente com sites públicos.</span><span class="sxs-lookup"><span data-stu-id="41b43-130">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar um email para ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "É preciso ter o Microsoft Edge List v1 XML | Microsoft Edge"  
