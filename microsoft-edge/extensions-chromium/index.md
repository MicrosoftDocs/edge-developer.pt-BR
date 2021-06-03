---
description: Uma visão geral da criação e publicação Microsoft Edge (Chromium) Extensões.
title: Visão geral Microsoft Edge extensões (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, desenvolvimento de extensões, extensões de navegador, addons, partner center, desenvolvedor, extensões de cromo
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327523"
---
# <span data-ttu-id="145ab-104">Visão geral Microsoft Edge extensões (Chromium)</span><span class="sxs-lookup"><span data-stu-id="145ab-104">Overview of Microsoft Edge (Chromium) Extensions</span></span>  

<span data-ttu-id="145ab-105">Uma extensão é um pequeno programa que você \(um desenvolvedor\) usa para adicionar ou modificar recursos para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="145ab-105">An extension is a small program that you \(a developer\) use to add or modify features for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="145ab-106">Uma extensão destina-se a melhorar a experiência de navegação diária de um usuário.</span><span class="sxs-lookup"><span data-stu-id="145ab-106">An extension is intended to improve a user's day-to-day browsing experience.</span></span>  <span data-ttu-id="145ab-107">Ele fornece funcionalidade de nicho que é importante para um público-alvo.</span><span class="sxs-lookup"><span data-stu-id="145ab-107">It provides niche functionality that is important to a target audience.</span></span>  

<span data-ttu-id="145ab-108">Você pode criar uma extensão se tiver uma ideia ou produto que se baseia em uma das seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="145ab-108">You may create an extension if you have an idea or product that is based upon either of the following conditions.</span></span>  

*   <span data-ttu-id="145ab-109">Um navegador da Web específico.</span><span class="sxs-lookup"><span data-stu-id="145ab-109">A specific web browser.</span></span>  
*   <span data-ttu-id="145ab-110">Melhorias nos recursos de páginas da Web específicas.</span><span class="sxs-lookup"><span data-stu-id="145ab-110">Improvements to features of specific webpages.</span></span>  
    
<span data-ttu-id="145ab-111">Exemplos de experiências de parceiro incluem bloqueadores de ad e gerentes de senha.</span><span class="sxs-lookup"><span data-stu-id="145ab-111">Examples of companion experiences include ad blockers and password managers.</span></span>  

<span data-ttu-id="145ab-112">Uma extensão é estruturada de forma semelhante a um aplicativo Web regular.</span><span class="sxs-lookup"><span data-stu-id="145ab-112">An extension is structured similar to a regular web app.</span></span>  <span data-ttu-id="145ab-113">No mínimo, ele deve incluir os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="145ab-113">At a minimum, it should include the following features.</span></span>

*   <span data-ttu-id="145ab-114">Um arquivo JSON de manifesto de aplicativo que contém informações básicas da plataforma.</span><span class="sxs-lookup"><span data-stu-id="145ab-114">An app manifest JSON file that contains basic platform information.</span></span>  
*   <span data-ttu-id="145ab-115">Um arquivo JavaScript que define a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="145ab-115">A JavaScript file that define functionality.</span></span>  
*   <span data-ttu-id="145ab-116">Arquivos HTML e CSS que definem a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="145ab-116">HTML and CSS files that define the user interface.</span></span>  

<span data-ttu-id="145ab-117">Para trabalhar diretamente com parte do navegador, como uma janela ou guia, você deve enviar solicitações de API e frequentemente fazer referência ao navegador pelo nome.</span><span class="sxs-lookup"><span data-stu-id="145ab-117">To work directly with part of the browser, such as a window or tab, you must send API requests and often reference the browser by name.</span></span>  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Uma extensão Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  <span data-ttu-id="145ab-119">Uma Microsoft Edge \(Chromium\)</span><span class="sxs-lookup"><span data-stu-id="145ab-119">A Microsoft Edge \(Chromium\) extension</span></span>  
:::image-end:::  

## <span data-ttu-id="145ab-120">Diretrizes básicas</span><span class="sxs-lookup"><span data-stu-id="145ab-120">Basic guidance</span></span>  

<span data-ttu-id="145ab-121">Alguns dos navegadores mais populares para criar extensões incluem Safari, Firefox, Chrome, Opera, Brave e Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="145ab-121">Some of the most popular browsers to build extensions for include Safari, Firefox, Chrome, Opera, Brave, and Microsoft Edge.</span></span>  <span data-ttu-id="145ab-122">Ótimos locais para começar os tutoriais de desenvolvimento de extensão e a pesquisa de documentação são sites hospedados pelas organizações do navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-122">Great places to begin your extension development tutorials and documentation research are sites hosted by the browser organizations.</span></span>  <span data-ttu-id="145ab-123">A tabela a seguir não é definitiva e pode ser usada como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="145ab-123">The following table isn't definitive, and may be used as a starting point.</span></span>  

| <span data-ttu-id="145ab-124">Navegador da Web</span><span class="sxs-lookup"><span data-stu-id="145ab-124">Web browser</span></span> | <span data-ttu-id="145ab-125">Chromium baseado?</span><span class="sxs-lookup"><span data-stu-id="145ab-125">Chromium-based?</span></span> | <span data-ttu-id="145ab-126">Página da Web de desenvolvimento de extensão</span><span class="sxs-lookup"><span data-stu-id="145ab-126">Extension development webpage</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="145ab-127">Safari</span><span class="sxs-lookup"><span data-stu-id="145ab-127">Safari</span></span> | <span data-ttu-id="145ab-128">Não</span><span class="sxs-lookup"><span data-stu-id="145ab-128">No</span></span> | [<span data-ttu-id="145ab-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span><span class="sxs-lookup"><span data-stu-id="145ab-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span></span>][AppleDeveloperSafariservicesAppExtensions] |  
| <span data-ttu-id="145ab-130">Firefox</span><span class="sxs-lookup"><span data-stu-id="145ab-130">Firefox</span></span> | <span data-ttu-id="145ab-131">Não</span><span class="sxs-lookup"><span data-stu-id="145ab-131">No</span></span> | [<span data-ttu-id="145ab-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span><span class="sxs-lookup"><span data-stu-id="145ab-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span></span>][MDNWebextensions] |  
| <span data-ttu-id="145ab-133">Chrome</span><span class="sxs-lookup"><span data-stu-id="145ab-133">Chrome</span></span> | <span data-ttu-id="145ab-134">Sim</span><span class="sxs-lookup"><span data-stu-id="145ab-134">Yes</span></span> | [<span data-ttu-id="145ab-135">developer.chrome.com/extensions</span><span class="sxs-lookup"><span data-stu-id="145ab-135">developer.chrome.com/extensions</span></span>][ChromeDeveloperExtensions] |  
| <span data-ttu-id="145ab-136">Opera</span><span class="sxs-lookup"><span data-stu-id="145ab-136">Opera</span></span> | <span data-ttu-id="145ab-137">Sim</span><span class="sxs-lookup"><span data-stu-id="145ab-137">Yes</span></span> | [<span data-ttu-id="145ab-138">dev.opera.com/extensions</span><span class="sxs-lookup"><span data-stu-id="145ab-138">dev.opera.com/extensions</span></span>][OperaDevExtensions] |  
| <span data-ttu-id="145ab-139">Bálsam</span><span class="sxs-lookup"><span data-stu-id="145ab-139">Brave</span></span> | <span data-ttu-id="145ab-140">Sim</span><span class="sxs-lookup"><span data-stu-id="145ab-140">Yes</span></span> | <span data-ttu-id="145ab-141">Usa [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span><span class="sxs-lookup"><span data-stu-id="145ab-141">Uses [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span></span> |  
| <span data-ttu-id="145ab-142">novo Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="145ab-142">new Microsoft Edge</span></span> | <span data-ttu-id="145ab-143">Sim</span><span class="sxs-lookup"><span data-stu-id="145ab-143">Yes</span></span> | [<span data-ttu-id="145ab-144">developer.microsoft.com/microsoft-edge/extensions</span><span class="sxs-lookup"><span data-stu-id="145ab-144">developer.microsoft.com/microsoft-edge/extensions</span></span>][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> <span data-ttu-id="145ab-145">Muitos dos tutoriais dos sites usam APIs específicas do navegador que podem não corresponder ao navegador para o qual você desenvolve.</span><span class="sxs-lookup"><span data-stu-id="145ab-145">Many of the tutorials of the sites use browser-specific APIs that may not match the browser for which you develop.</span></span>  <span data-ttu-id="145ab-146">Na maioria dos casos, uma extensão Chromium funciona como está em diferentes Chromium e as APIs funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="145ab-146">In most cases, a Chromium extension works as-is in different Chromium browsers and the APIs work as expected.</span></span>  <span data-ttu-id="145ab-147">Somente algumas APIs menos comuns podem ser estritamente específicas do navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-147">Only some less common APIs may be strictly browser-specific.</span></span>  <span data-ttu-id="145ab-148">Para links para os tutoriais, navegue até [Ver também](#see-also).</span><span class="sxs-lookup"><span data-stu-id="145ab-148">For links to the tutorials, navigate to [See also](#see-also).</span></span>  

## <span data-ttu-id="145ab-149">Por Chromium?</span><span class="sxs-lookup"><span data-stu-id="145ab-149">Why Chromium?</span></span>  

<span data-ttu-id="145ab-150">Se seu objetivo é publicar sua extensão no armazenamento de extensões para cada navegador, ela deve ser modificada para cada versão para direcionar e executar em cada ambiente de navegador distinto.</span><span class="sxs-lookup"><span data-stu-id="145ab-150">If your goal is to publish your extension in the extensions store for each browser, it must be modified for each version to target and run in each distinct browser environment.</span></span>  <span data-ttu-id="145ab-151">Por exemplo, [as extensões do Safari][AppleDeveloperSafariservicesAppExtensions] podem usar a Web e o código nativo para se comunicar com aplicativos nativos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="145ab-151">For example, [Safari extensions][AppleDeveloperSafariservicesAppExtensions] may use both web and native code to communicate with counterpart native applications.</span></span>  <span data-ttu-id="145ab-152">Os últimos quatro navegadores da tabela anterior usam o mesmo pacote de código e minimizam o requisito de manter versões paralelas.</span><span class="sxs-lookup"><span data-stu-id="145ab-152">The last four browsers in the previous table use the same code package, and minimizes the requirement to maintain parallel versions.</span></span>  <span data-ttu-id="145ab-153">Esses navegadores se baseiam no Chromium [de código aberto.][|::ref1::|Home]</span><span class="sxs-lookup"><span data-stu-id="145ab-153">These browsers are based on the [Chromium open-source project][|::ref1::|Home].</span></span>  

<span data-ttu-id="145ab-154">Crie uma Chromium para gravar a menor quantidade de código.</span><span class="sxs-lookup"><span data-stu-id="145ab-154">Create a Chromium extension to write the least amount of code.</span></span>  <span data-ttu-id="145ab-155">Ele também direciona o número máximo de armazenamentos de extensão e, por fim, o número máximo de usuários que encontram e adquirem sua extensão.</span><span class="sxs-lookup"><span data-stu-id="145ab-155">It also targets the maximum number of extension stores and ultimately the maximum number of users who find and acquire your extension.</span></span>  

<span data-ttu-id="145ab-156">O conteúdo a seguir se concentra principalmente em Chromium extensões.</span><span class="sxs-lookup"><span data-stu-id="145ab-156">The following content focuses mostly on Chromium extensions.</span></span>  

## <span data-ttu-id="145ab-157">Teste de compatibilidade e extensão do navegador</span><span class="sxs-lookup"><span data-stu-id="145ab-157">Browser compatibility and extension testing</span></span>  

<span data-ttu-id="145ab-158">Ocasionalmente, a paridade da API não existe entre Chromium navegadores.</span><span class="sxs-lookup"><span data-stu-id="145ab-158">Occasionally, API parity doesn't exist between Chromium browsers.</span></span>  <span data-ttu-id="145ab-159">Por exemplo, há diferenças nas APIs de identidade e pagamento.</span><span class="sxs-lookup"><span data-stu-id="145ab-159">For example, there are differences in the identity and payment APIs.</span></span>  <span data-ttu-id="145ab-160">Para garantir que sua extensão atenda às expectativas do cliente, revise o status da API por meio dos seguintes documentos oficiais do navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-160">To ensure your extension meets customer expectations, review API status through the following official browser docs.</span></span>  

*   [<span data-ttu-id="145ab-161">Chrome APIs</span><span class="sxs-lookup"><span data-stu-id="145ab-161">Chrome APIs</span></span>][ChromeDeveloperExtensionsApiIndex]  
*   [<span data-ttu-id="145ab-162">APIs de extensão com suporte no Opera</span><span class="sxs-lookup"><span data-stu-id="145ab-162">Extension APIs supported in Opera</span></span>][OperaDevExtensionsApis]  
*   [<span data-ttu-id="145ab-163">Extensão porta chrome para Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="145ab-163">Port Chrome extension to Microsoft Edge (Chromium)</span></span>][ExtensionsChromiumDeveloperGuidePortChrome]  
    
<span data-ttu-id="145ab-164">As APIs necessárias definem as alterações que devem ser feitas para resolver as diferenças entre cada navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-164">The APIs you require define the changes you must make to address the differences between each browser.</span></span>  <span data-ttu-id="145ab-165">Isso pode significar que você deve criar pacotes de código ligeiramente diferentes com pequenas diferenças para cada loja.</span><span class="sxs-lookup"><span data-stu-id="145ab-165">It may mean that you must create slightly different code packages with small differences for each store.</span></span>  

<span data-ttu-id="145ab-166">Para testar sua extensão em ambientes diferentes antes de enviar para um armazenamento do navegador, armazene-a no navegador enquanto a desenvolve.</span><span class="sxs-lookup"><span data-stu-id="145ab-166">To test your extension in different environments before you submit it to a browser store, sideload it into your browser while you develop it.</span></span>  

## <span data-ttu-id="145ab-167">Publicar sua extensão nos armazenamentos do navegador</span><span class="sxs-lookup"><span data-stu-id="145ab-167">Publish your extension to browser stores</span></span>  

<span data-ttu-id="145ab-168">Você pode enviar e buscar extensões de navegador nos seguintes armazenamentos de navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-168">You may submit and seek browser extensions in the following browser stores.</span></span>  

*   [<span data-ttu-id="145ab-169">Complementos do navegador Firefox</span><span class="sxs-lookup"><span data-stu-id="145ab-169">Firefox Browser Add-ons</span></span>][MozillaAddonsFirefoxExtensions]  
*   [<span data-ttu-id="145ab-170">Chrome Web Store</span><span class="sxs-lookup"><span data-stu-id="145ab-170">Chrome Web Store</span></span>][GoogleChromeWebstoreCategoryExtensions]  
*   [<span data-ttu-id="145ab-171">Addons de opera</span><span class="sxs-lookup"><span data-stu-id="145ab-171">Opera addons</span></span>][OperaAddonsExtensions]  
*   [<span data-ttu-id="145ab-172">Microsoft Edge Complementos</span><span class="sxs-lookup"><span data-stu-id="145ab-172">Microsoft Edge Add-ons</span></span>][MicrosoftEdgeAddonsCategoryExtensions]  

<span data-ttu-id="145ab-173">Alguns armazenamentos permitem baixar extensões listadas de outros navegadores.</span><span class="sxs-lookup"><span data-stu-id="145ab-173">Some stores allow you to download listed extensions from other browsers.</span></span>  <span data-ttu-id="145ab-174">No entanto, o acesso entre navegadores não é garantido pelos armazenamentos do navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-174">However, cross-browser access is not guaranteed by browser stores.</span></span>  <span data-ttu-id="145ab-175">Para garantir que seus usuários encontrem sua extensão em navegadores diferentes, você deve manter uma listagem em cada armazenamento de extensão do navegador.</span><span class="sxs-lookup"><span data-stu-id="145ab-175">To ensure your users find your extension in different browsers, you should maintain a listing on each browser extension store.</span></span>  

<span data-ttu-id="145ab-176">Os usuários podem precisar instalar sua extensão em navegadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="145ab-176">Users may need to install your extension in different browsers.</span></span> <span data-ttu-id="145ab-177">Nesse cenário, você pode migrar extensões Chromium existentes de um navegador para outro.</span><span class="sxs-lookup"><span data-stu-id="145ab-177">In this scenario, you may migrate existing Chromium extensions from one browser to another.</span></span>  

### <span data-ttu-id="145ab-178">Migrar uma extensão existente para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="145ab-178">Migrate an existing extension to Microsoft Edge</span></span>  

<span data-ttu-id="145ab-179">Se você já tiver desenvolvido uma extensão para outro navegador Chromium, você poderá enviar para o Microsoft Edge de complementos.</span><span class="sxs-lookup"><span data-stu-id="145ab-179">If you've already developed an extension for another Chromium browser, you may submit it to the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="145ab-180">Você não precisa reescrever sua extensão e deve verificar se ela funciona Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="145ab-180">You don't need to rewrite your extension, and must verify it works in Microsoft Edge.</span></span>  <span data-ttu-id="145ab-181">Ao migrar uma extensão Chromium para outros navegadores Chromium, verifique se as mesmas APIs ou alternativas estão disponíveis para o navegador de destino.</span><span class="sxs-lookup"><span data-stu-id="145ab-181">When you migrate an existing Chromium extension to other Chromium browsers, ensure the same APIs or alternatives are available for your target browser.</span></span>  

<span data-ttu-id="145ab-182">Para obter mais informações sobre como portar sua extensão do Chrome para Microsoft Edge, navegue até [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span><span class="sxs-lookup"><span data-stu-id="145ab-182">For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span></span> <span data-ttu-id="145ab-183">Após a portabilidade da extensão para o navegador de destino, a próxima etapa é publicá-la.</span><span class="sxs-lookup"><span data-stu-id="145ab-183">After you port your extension to the target browser, the next step is to publish it.</span></span>  

### <span data-ttu-id="145ab-184">Publicar no site complementos do Microsoft Edge site</span><span class="sxs-lookup"><span data-stu-id="145ab-184">Publish to the Microsoft Edge add-ons website</span></span>  

<span data-ttu-id="145ab-185">Para começar [a][MicrosoftDeveloperRegistration] publicar sua extensão no Microsoft Edge, você deve se registrar em uma conta de desenvolvedor com uma conta de email MSA para enviar sua listagem de extensão para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="145ab-185">To start publishing your extension to Microsoft Edge, you must [register for a developer account][MicrosoftDeveloperRegistration] with an MSA email account to submit your extension listing to the store.</span></span>  <span data-ttu-id="145ab-186">Uma conta de email MSA inclui `@outlook.com` , e assim por `@live.com` diante.</span><span class="sxs-lookup"><span data-stu-id="145ab-186">An MSA email account includes `@outlook.com`, `@live.com`, and so on.</span></span>  <span data-ttu-id="145ab-187">Ao escolher um endereço de email para registrar, considere se você deve transferir ou compartilhar a propriedade da extensão com outras pessoas em sua organização.</span><span class="sxs-lookup"><span data-stu-id="145ab-187">When you choose an email address to register, consider if you must transfer or share ownership of the extension with others in your organization.</span></span>  <span data-ttu-id="145ab-188">Depois que o registro for concluído, você poderá criar um novo envio de extensão para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="145ab-188">After registration is complete, you may create a new extension submission to the store.</span></span>  

<span data-ttu-id="145ab-189">Para enviar sua extensão para o armazenamento, certifique-se de fornecer os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="145ab-189">To submit your extension to the store, ensure you provide the following items.</span></span>  

*   <span data-ttu-id="145ab-190">Um arquivo morto \( `.zip` \) que contém seus arquivos de código.</span><span class="sxs-lookup"><span data-stu-id="145ab-190">An archive \(`.zip`\) file that contains your code files.</span></span>  
*   <span data-ttu-id="145ab-191">Todos os ativos visuais necessários, que incluem um logotipo e um pequeno azulejo promocional.</span><span class="sxs-lookup"><span data-stu-id="145ab-191">All required visual assets, which include a logo and small promotional tile.</span></span>  
*   <span data-ttu-id="145ab-192">Mídia promocional opcional, como capturas de tela, blocos promocionais e uma URL de vídeo.</span><span class="sxs-lookup"><span data-stu-id="145ab-192">Optional promotional media, such as screenshots, promotional tiles, and a video URL.</span></span>  
*   <span data-ttu-id="145ab-193">Informações que descrevem sua extensão, como o nome, a descrição curta e um link de política de privacidade.</span><span class="sxs-lookup"><span data-stu-id="145ab-193">Information that describes your extension such as the name, short description, and a privacy policy link.</span></span>  

> [!NOTE]
> <span data-ttu-id="145ab-194">Os diferentes armazenamentos podem ter requisitos de envio diferentes.</span><span class="sxs-lookup"><span data-stu-id="145ab-194">Different stores may have different submission requirements.</span></span>  <span data-ttu-id="145ab-195">A lista acima resume os requisitos [para][ExtensionsChromiumPublish] publicar uma extensão para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="145ab-195">The above list summarizes the [requirements][ExtensionsChromiumPublish] to publish an extension for Microsoft Edge.</span></span>  

<span data-ttu-id="145ab-196">Depois de enviar sua extensão com êxito, sua extensão passa por um processo de revisão e passa ou falha no processo de certificação.</span><span class="sxs-lookup"><span data-stu-id="145ab-196">After you've successfully submitted your extension, your extension undergoes a review process and either passes or fails the certification process.</span></span>  <span data-ttu-id="145ab-197">Os proprietários são notificados do resultado e dado as próximas etapas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="145ab-197">Owners are notified of the outcome and given next steps as required.</span></span>  <span data-ttu-id="145ab-198">Se você enviar uma atualização de extensão para o armazenamento, um novo processo de revisão será iniciado.</span><span class="sxs-lookup"><span data-stu-id="145ab-198">If you submit an extension update to the store, a new review process is started.</span></span>  

## <span data-ttu-id="145ab-199">Consulte também</span><span class="sxs-lookup"><span data-stu-id="145ab-199">See also</span></span>  

*   [<span data-ttu-id="145ab-200">Porta uma extensão do Google Chrome</span><span class="sxs-lookup"><span data-stu-id="145ab-200">Port a Google Chrome extension</span></span>][ExtensionworkshopPorting]  
*   [<span data-ttu-id="145ab-201">Criar uma extensão do Aplicativo Safari</span><span class="sxs-lookup"><span data-stu-id="145ab-201">Build a Safari App extension</span></span>][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [<span data-ttu-id="145ab-202">Sua primeira extensão (Firefox)</span><span class="sxs-lookup"><span data-stu-id="145ab-202">Your first extension (Firefox)</span></span>][MDNWebextensionsYourFirst]  
*   [<span data-ttu-id="145ab-203">Tutorial introdução (Chrome)</span><span class="sxs-lookup"><span data-stu-id="145ab-203">Get started tutorial (Chrome)</span></span>][ChromeDeveloperExtensionsGetstarted]  
*   [<span data-ttu-id="145ab-204">Começar (Opera)</span><span class="sxs-lookup"><span data-stu-id="145ab-204">Get started (Opera)</span></span>][OperaDevExtensionsGettingStarted]  
*   [<span data-ttu-id="145ab-205">Começar com extensões Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="145ab-205">Get started with Microsoft Edge (Chromium) extensions</span></span>][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Port Chrome Extension To Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Iniciando com extensões Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar uma extensão | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desenvolver extensões para Microsoft Edge | Desenvolvedor da Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Desenvolvedor da Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensões para Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensões de aplicativo safari | Desenvolvedor apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Criando uma extensão do aplicativo Safari | Desenvolvedor apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "O que são extensões? | Desenvolvedor do Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "APIs do Chrome | Desenvolvedor do Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Introdução ao Tutorial | Desenvolvedor do Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portando uma extensão do Google Chrome | Workshop de Extensão"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensões do navegador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Sua primeira extensão | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensões | Complementos para Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensões | Opera Addons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentação de extensões | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "APIs de extensão com suporte no Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Iniciando | Dev. Opera"  
