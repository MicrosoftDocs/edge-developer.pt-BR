---
description: Mover usuários para o Microsoft Edge do Internet Explorer
title: Mover usuários para o Microsoft Edge do Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web, Internet Explorer
ms.openlocfilehash: c2106955ed79bd28dc1f847dee220944bb014689
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461133"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a><span data-ttu-id="a4085-104">Mover usuários para o Microsoft Edge do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a4085-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="a4085-105">Muitos sites modernos têm designs incompatíveis com o Internet Explorer \(IE\).</span><span class="sxs-lookup"><span data-stu-id="a4085-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="a4085-106">Quando um usuário do IE visita um site público incompatível, o usuário pode receber uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a4085-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="a4085-107">A mensagem afirma que o site é incompatível com o navegador.</span><span class="sxs-lookup"><span data-stu-id="a4085-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="a4085-108">Depois que a mensagem for exibida, o usuário deverá alternar manualmente para um navegador moderno.</span><span class="sxs-lookup"><span data-stu-id="a4085-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="a4085-109">Para minimizar as interrupções, a partir da versão 84, o Microsoft Edge oferece suporte a um novo recurso que redireciona automaticamente os usuários.</span><span class="sxs-lookup"><span data-stu-id="a4085-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="a4085-110">Quando um usuário do IE navega para um site incompatível com o IE, o Windows redireciona automaticamente o usuário para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4085-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="a4085-111">Para revisar os sites na lista, navegue até [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="a4085-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="a4085-112">Este artigo descreve os seguintes conceitos.</span><span class="sxs-lookup"><span data-stu-id="a4085-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="a4085-113">Por que um site é adicionado à lista</span><span class="sxs-lookup"><span data-stu-id="a4085-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="a4085-114">A experiência do usuário para redirecionamento</span><span class="sxs-lookup"><span data-stu-id="a4085-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="a4085-115">Solicitar uma atualização para a lista</span><span class="sxs-lookup"><span data-stu-id="a4085-115">Request an update to the list</span></span>  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a><span data-ttu-id="a4085-116">Por que um site é adicionado à lista de compatibilidade do IE?</span><span class="sxs-lookup"><span data-stu-id="a4085-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="a4085-117">A Lista de compatibilidade do IE só adiciona um site quando as ações a seguir ocorrem.</span><span class="sxs-lookup"><span data-stu-id="a4085-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="a4085-118">Mostra a um usuário do IE uma mensagem sugerindo que o usuário deve usar um navegador diferente por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="a4085-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="a4085-119">O proprietário solicita adicionar o site à lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="a4085-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <a name="redirection-experience"></a><span data-ttu-id="a4085-120">Experiência de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="a4085-120">Redirection experience</span></span>

<span data-ttu-id="a4085-121">Ao redirecionar para o Microsoft Edge, o usuário é mostrado a caixa de diálogo única na próxima captura de tela.</span><span class="sxs-lookup"><span data-stu-id="a4085-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="a4085-122">A caixa de diálogo fornece ao usuário as seguintes informações.</span><span class="sxs-lookup"><span data-stu-id="a4085-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="a4085-123">Ele explica por que o site está sendo redirecionado.</span><span class="sxs-lookup"><span data-stu-id="a4085-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="a4085-124">Ele solicita ao usuário consentimento para copiar dados de navegação e preferências do IE para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4085-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a4085-125">Os dados de navegação a seguir são importados.</span><span class="sxs-lookup"><span data-stu-id="a4085-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="a4085-126">Favoritos</span><span class="sxs-lookup"><span data-stu-id="a4085-126">Favorites</span></span>  
      *   <span data-ttu-id="a4085-127">Senhas</span><span class="sxs-lookup"><span data-stu-id="a4085-127">Passwords</span></span>  
      *   <span data-ttu-id="a4085-128">Mecanismos de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a4085-128">Search engines</span></span>  
      *   <span data-ttu-id="a4085-129">Abrir guias</span><span class="sxs-lookup"><span data-stu-id="a4085-129">Open tabs</span></span>  
      *   <span data-ttu-id="a4085-130">Histórico</span><span class="sxs-lookup"><span data-stu-id="a4085-130">History</span></span>  
      *   <span data-ttu-id="a4085-131">Configurações</span><span class="sxs-lookup"><span data-stu-id="a4085-131">Settings</span></span>  
      *   <span data-ttu-id="a4085-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="a4085-132">Cookies</span></span>  
      *   <span data-ttu-id="a4085-133">A Home Page</span><span class="sxs-lookup"><span data-stu-id="a4085-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notificação de navegação e prompt para importar dados e preferências" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="a4085-135">Notificação de navegação e prompt para importar dados e preferências</span><span class="sxs-lookup"><span data-stu-id="a4085-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="a4085-136">Se o usuário não consentir escolhendo a caixa de seleção Sempre trazer meus dados de  navegação e preferências do **Internet Explorer,** o usuário poderá escolher Continuar a navegação para continuar a sessão   de navegação.</span><span class="sxs-lookup"><span data-stu-id="a4085-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="a4085-137">Por fim, um banner de incompatibilidade de site é exibido na barra de endereços para cada redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a4085-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="a4085-138">Um exemplo de uma faixa de incompatibilidade de site é exibido na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4085-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificação sobre sites modernos e prompt para definir o Microsoft Edge como navegador padrão ou explorar o Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="a4085-140">Notificação sobre sites modernos e prompt para definir o Microsoft Edge como navegador padrão ou explorar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4085-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="a4085-141">A faixa de incompatibilidade do site fornece os seguintes detalhes para o usuário.</span><span class="sxs-lookup"><span data-stu-id="a4085-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="a4085-142">Recomenda que o usuário alternar para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4085-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="a4085-143">Oferece para definir o Microsoft Edge como o navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="a4085-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="a4085-144">Oferece ao usuário a opção de explorar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4085-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="a4085-145">Quando um site é redirecionado do Internet Explorer para o Microsoft Edge, ocorre uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="a4085-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="a4085-146">Se a guia IE ativa não tiver conteúdo anterior, ela será fechada.</span><span class="sxs-lookup"><span data-stu-id="a4085-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="a4085-147">Se a guia do IE ativo tiver conteúdo anterior, ela navegará até a página de suporte da Microsoft que explica por que o site foi [redirecionado para o Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span><span class="sxs-lookup"><span data-stu-id="a4085-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="a4085-148">Após um redirecionamento, os usuários podem continuar a usar o IE para sites que não estão na lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="a4085-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <a name="request-an-update-to-the-ie-compatibility-list"></a><span data-ttu-id="a4085-149">Solicitar uma atualização para a lista de compatibilidade do IE</span><span class="sxs-lookup"><span data-stu-id="a4085-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="a4085-150">A lista de compatibilidade do IE é um arquivo XML no [microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="a4085-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="a4085-151">A lista é atualizada regularmente em resposta a solicitações de desenvolvedores de sites e usuários para que os sites tenham sido adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="a4085-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="a4085-152">As atualizações da lista são baixadas automaticamente para máquinas de usuário.</span><span class="sxs-lookup"><span data-stu-id="a4085-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="a4085-153">Envie as informações a seguir [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que seu site seja adicionado ou removido da lista de compatibilidade do IE.</span><span class="sxs-lookup"><span data-stu-id="a4085-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="a4085-154">Nome do proprietário</span><span class="sxs-lookup"><span data-stu-id="a4085-154">Owner name</span></span>  
*   <span data-ttu-id="a4085-155">Título corporativo</span><span class="sxs-lookup"><span data-stu-id="a4085-155">Corporate title</span></span>  
*   <span data-ttu-id="a4085-156">Email</span><span class="sxs-lookup"><span data-stu-id="a4085-156">Email address</span></span>  
*   <span data-ttu-id="a4085-157">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="a4085-157">Company name</span></span>  
*   <span data-ttu-id="a4085-158">Rua</span><span class="sxs-lookup"><span data-stu-id="a4085-158">Street address</span></span>  
*   <span data-ttu-id="a4085-159">Endereço do site</span><span class="sxs-lookup"><span data-stu-id="a4085-159">Website address</span></span>  
    
<span data-ttu-id="a4085-160">A lista de compatibilidade do IE é atualizada dentro de uma semana.</span><span class="sxs-lookup"><span data-stu-id="a4085-160">The IE compatibility list is updated within a week.</span></span>

> [!NOTE]
> <span data-ttu-id="a4085-161">A lista de compatibilidade do IE foi projetada para funcionar somente com sites públicos.</span><span class="sxs-lookup"><span data-stu-id="a4085-161">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envie um email para ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Precisa do Microsoft Edge list v1 xml | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "O site que você estava tentando alcançar não funciona com o Internet Explorer | Microsoft Office Suporte"  
