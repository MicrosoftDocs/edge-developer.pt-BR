---
description: Processo passo a passo para publicar extensões Edge (Chromium) na Microsoft Store.
title: Publicar uma extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607374"
---
# <span data-ttu-id="46f17-104">Publicar uma extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-104">Publish An Extension</span></span>  

<span data-ttu-id="46f17-105">Publicar sua extensão no catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \).</span><span class="sxs-lookup"><span data-stu-id="46f17-105">Publish your Extension on Microsoft Edge Addons catalog \(Microsoft Edge Addons\).</span></span>  <span data-ttu-id="46f17-106">Primeiro, você deve criar um envio no [centro de parcerias][MicrosoftPartnerCenter] e enviá-lo.</span><span class="sxs-lookup"><span data-stu-id="46f17-106">You must first create a submission on [Partner Center][MicrosoftPartnerCenter] and submit it.</span></span>  <span data-ttu-id="46f17-107">Este documento lista todos os detalhes que você deve fornecer para criar um envio de extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-107">This document lists all the details that you must provide to create an Extension submission.</span></span>  

## <span data-ttu-id="46f17-108">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="46f17-108">Before You Begin</span></span>  

*   <span data-ttu-id="46f17-109">Você deve ter uma conta de desenvolvedor ativa no [centro de parceiros][MicrosoftPartnerCenter] para enviar sua extensão em Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-109">You must have an active developer account on [Partner Center][MicrosoftPartnerCenter] to submit your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="46f17-110">Se você não tiver um, [crie uma nova conta de desenvolvedor][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="46f17-110">If you do not have one, [create a new developer account][MicrosoftPartnerCenter].</span></span>  
*   <span data-ttu-id="46f17-111">Crie um arquivo zip do seu pacote de extensão e verifique se ele contém estes arquivos:</span><span class="sxs-lookup"><span data-stu-id="46f17-111">Create a zip file of your Extension package and ensure that it contains these files:</span></span>  
    *   <span data-ttu-id="46f17-112">O arquivo de manifesto e deve definir o nome e a versão de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-112">The manifest file and it must define the name and version of your Extension.</span></span>  
    *   <span data-ttu-id="46f17-113">As imagens e outros arquivos necessários para a extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-113">The images and other files that are required for your Extension.</span></span>  


<span data-ttu-id="46f17-114">Se você não iniciou a criação de uma extensão, talvez se refira ao tutorial de [introdução][ExtensionsGettingStarted] para a criação de uma extensão Chromium do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-114">If you have not started building an Extension, you may refer to the [Getting Started][ExtensionsGettingStarted] tutorial for building a Microsoft Edge Chromium extension.</span></span>  

<span data-ttu-id="46f17-115">Para criar um envio de extensão no [Partner Center][MicrosoftPartnerCenter], siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="46f17-115">To create an Extension submission on [Partner Center][MicrosoftPartnerCenter], follow these steps.</span></span>  

## <span data-ttu-id="46f17-116">Etapa 1: iniciar um novo envio</span><span class="sxs-lookup"><span data-stu-id="46f17-116">Step 1: Start a New Submission</span></span>  

<span data-ttu-id="46f17-117">Acesse o [painel do desenvolvedor][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="46f17-117">Go to your [developer dashboard][MicrosoftPartnerCenter].</span></span>  <span data-ttu-id="46f17-118">Na página Visão geral, clique em **criar nova extensão**.</span><span class="sxs-lookup"><span data-stu-id="46f17-118">From the Overview page, click **Create new extension**.</span></span>  

## <span data-ttu-id="46f17-119">Etapa 2: carregar o arquivo zip da extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-119">Step 2: Upload Your Extension Zip File</span></span>  

<span data-ttu-id="46f17-120">A página do **pacote** é onde você carrega o arquivo zip para o envio da extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-120">The **Package** page is where you upload the zip file for your Extension submission.</span></span>  <span data-ttu-id="46f17-121">Você só pode carregar um pacote por vez, portanto, se sua extensão não estiver completa, você pode carregar um pacote do trabalho em andamento e atualizar a qualquer momento antes de publicá-lo.</span><span class="sxs-lookup"><span data-stu-id="46f17-121">You may only upload one package at a time, so if your Extension is not complete you may upload a work-in-progress package and update at any time before you publish it.</span></span>  <span data-ttu-id="46f17-122">Certifique-se de que seu pacote contém o `manifest.json` arquivo e está funcionando bem no Microsoft Edge antes de carregá-lo.</span><span class="sxs-lookup"><span data-stu-id="46f17-122">Be sure that your package contains the `manifest.json` file and is working fine on Microsoft Edge prior to uploading.</span></span>  
<span data-ttu-id="46f17-123">Carregue o pacote arrastando-o para o campo de carregamento ou selecionando **procurar seus arquivos**.</span><span class="sxs-lookup"><span data-stu-id="46f17-123">Upload the package by dragging it into the upload field or by selecting **Browse your files**.</span></span>  <span data-ttu-id="46f17-124">A página pacote valida o arquivo zip Extensions e exibe o **status de êxito ou falha do seu carregamento**.</span><span class="sxs-lookup"><span data-stu-id="46f17-124">The Package page validates the Extensions zip file and displays that **success or failure status of your upload**.</span></span>  <span data-ttu-id="46f17-125">Se o pacote passar na validação; Ele foi carregado com êxito e você vê uma mensagem de êxito.</span><span class="sxs-lookup"><span data-stu-id="46f17-125">If the package passes validation; it is uploaded successfully and you see a success message.</span></span>  <span data-ttu-id="46f17-126">Se o pacote falhar na validação; o pacote não é aceito e você vê uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="46f17-126">If the package fails validation; the package is not accepted and you see an error message.</span></span>  <span data-ttu-id="46f17-127">Se houver erros no pacote, resolva os problemas e tente carregá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="46f17-127">If there are errors in the package, resolve the issues and try uploading it again.</span></span>  

<span data-ttu-id="46f17-128">Após o upload bem-sucedido, examine os detalhes da extensão e clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="46f17-128">After successful upload, review your Extension details and click **Next** to proceed.</span></span>  

## <span data-ttu-id="46f17-129">Etapa 3: fornecer detalhes de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="46f17-129">Step 3: Provide Availability details</span></span>  

### <span data-ttu-id="46f17-130">Definir visibilidade</span><span class="sxs-lookup"><span data-stu-id="46f17-130">Define Visibility</span></span>  

<span data-ttu-id="46f17-131">Selecione uma opção de **visibilidade** para definir a audiência que pode descobrir e adquirir a extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-131">Select a **Visibility** option to define the audience who may discover and acquire your Extension.</span></span>  <span data-ttu-id="46f17-132">Isso lhe dá a opção de especificar se os usuários devem encontrar a extensão nos Complementos do Microsoft Edge ou ver a listagem.</span><span class="sxs-lookup"><span data-stu-id="46f17-132">This gives you the option to specify whether users should find your Extension in Microsoft Edge Addons or see the listing at all.</span></span>  <span data-ttu-id="46f17-133">Atualmente, você tem duas opções em visibilidade:</span><span class="sxs-lookup"><span data-stu-id="46f17-133">Currently, you have two options under visibility:</span></span>  

*   `Public`  
    <span data-ttu-id="46f17-134">Essa é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="46f17-134">This is the default option.</span></span>  
    <span data-ttu-id="46f17-135">Se você selecionar `Public` , sua extensão estará disponível e detectável para todos os complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-135">If you select `Public`, your Extension is available and discoverable to everyone in Microsoft Edge Addons.</span></span>  <span data-ttu-id="46f17-136">Deixe essa opção selecionada se desejar que a extensão seja listada nos Complementos do Microsoft Edge para os usuários encontrarem através de pesquisa, navegação e o link direto da extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-136">Leave this option selected if you want your Extension to be listed in Microsoft Edge Addons for users to find via searching, browsing, and the direct link of your Extension.</span></span>  

*   `Hidden`  
    <span data-ttu-id="46f17-137">Se você selecionar `Hidden` , a extensão ficará oculta nos Complementos do Microsoft Edge dos usuários que estão procurando ou navegando; você deve compartilhar a URL da sua listagem para distribuir a extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-137">If you select `Hidden`, your Extension is hidden in Microsoft Edge Addons from users searching or browsing; you must share your listing URL to distribute your Extension.</span></span>  <span data-ttu-id="46f17-138">Os usuários que têm o link direto para a listagem podem baixá-lo no Microsoft Edge \ (talvez você encontre a URL da sua listagem na página **visão geral de extensão** do envio de extensão \).</span><span class="sxs-lookup"><span data-stu-id="46f17-138">Users who have the direct link to the listing may download it on Microsoft Edge \(you may find your listing URL under **Extension Overview** page of Extension submission\).</span></span>  

> [!NOTE]
> <span data-ttu-id="46f17-139">Se você enviar uma extensão como **pública** e posteriormente alterá-la para **particular**, os usuários que instalaram a extensão quando ele foi público continuarão a ter acesso e receber atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="46f17-139">If you submit an Extension as **Public** and later change it to **Private**, Users who installed the Extension when it was public continue to have access and receive future updates.</span></span>  

### <span data-ttu-id="46f17-140">Definir mercados</span><span class="sxs-lookup"><span data-stu-id="46f17-140">Define markets</span></span>  

<span data-ttu-id="46f17-141">Você deve definir os mercados específicos em que está oferecendo a extensão, selecione **Mostrar opções** na seção **mercados** na página **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="46f17-141">You must define the specific markets in which you are offering your Extension, select **Show options** in the **Markets** section on the **Availability** page.</span></span>  <span data-ttu-id="46f17-142">A janela pop-up seleção de mercado é exibida, onde você deve escolher os mercados.</span><span class="sxs-lookup"><span data-stu-id="46f17-142">The Market selection pop-up window is displayed, where you should choose the markets.</span></span>  <span data-ttu-id="46f17-143">Por padrão, todos os mercados são selecionados, incluindo quaisquer **mercados futuros** que possam ser adicionados mais tarde.</span><span class="sxs-lookup"><span data-stu-id="46f17-143">By default, all markets are selected, including any **future markets** that may be added later.</span></span>  <span data-ttu-id="46f17-144">Você pode cancelar a seleção de mercados individuais para excluí-los, ou pode clicar em **desmarcar tudo** e adicionar mercados individuais à sua escolha.</span><span class="sxs-lookup"><span data-stu-id="46f17-144">You may deselect individual markets to exclude them, or you may click **Unselect all** and then add individual markets of your choice.</span></span>  

> [!NOTE]
> <span data-ttu-id="46f17-145">Se os usuários já tiverem a extensão em um determinado mercado e você remover esse mercado posteriormente, os usuários que já tiverem a extensão nesse mercado poderão continuar a usá-lo, mas não receberão as atualizações posteriores que você enviar.</span><span class="sxs-lookup"><span data-stu-id="46f17-145">If users already have your Extension in a certain market, and you later remove that market, users who already has the Extension in that market may continue to use it, but they do not get the later updates you submit.</span></span>  

<span data-ttu-id="46f17-146">Clique em **salvar** para ir para a seção **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="46f17-146">Click **Save** to proceed to **Properties** section.</span></span>  

## <span data-ttu-id="46f17-147">Etapa 4: selecionar propriedades para a extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-147">Step 4: Select Properties for Your Extension</span></span>  

### <span data-ttu-id="46f17-148">Propriedades de extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-148">Extension properties</span></span>  

*   [<span data-ttu-id="46f17-149">Categoria</span><span class="sxs-lookup"><span data-stu-id="46f17-149">Category</span></span>](#category)  
*   [<span data-ttu-id="46f17-150">Requisitos da política de privacidade</span><span class="sxs-lookup"><span data-stu-id="46f17-150">Privacy policy requirements</span></span>](#privacy-policy-requirements)  
*   [<span data-ttu-id="46f17-151">URL da política de privacidade</span><span class="sxs-lookup"><span data-stu-id="46f17-151">Privacy policy URL</span></span>](#privacy-policy-url)  
*   [<span data-ttu-id="46f17-152">URL do site</span><span class="sxs-lookup"><span data-stu-id="46f17-152">Website URL</span></span>](#website-url)  
*   [<span data-ttu-id="46f17-153">URL de suporte/endereço de email</span><span class="sxs-lookup"><span data-stu-id="46f17-153">Support URL/email address</span></span>](#support-urlemail-address)  
*   [<span data-ttu-id="46f17-154">Classificação de extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-154">Extension Rating</span></span>](#extension-rating)  

#### <span data-ttu-id="46f17-155">Categoria</span><span class="sxs-lookup"><span data-stu-id="46f17-155">Category</span></span>  

<span data-ttu-id="46f17-156">Listar a extensão na categoria certa ajuda os usuários a encontrar sua extensão facilmente e a entender mais sobre isso.</span><span class="sxs-lookup"><span data-stu-id="46f17-156">Listing your Extension in the right category helps users find your Extension easily and understand more about it.</span></span>  <span data-ttu-id="46f17-157">Selecione uma categoria que melhor descreva a extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-157">Select a Category that best describes your Extension.</span></span>  

<span data-ttu-id="46f17-158">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-158">**Possible Values**:</span></span>  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### <span data-ttu-id="46f17-159">Requisitos da política de privacidade</span><span class="sxs-lookup"><span data-stu-id="46f17-159">Privacy policy requirements</span></span>  

<span data-ttu-id="46f17-160">Indique se sua extensão acessa, coleta ou transmite qualquer informação pessoal.</span><span class="sxs-lookup"><span data-stu-id="46f17-160">Indicate whether your Extension accesses, collects, or transmits any personal information.</span></span>  

> [!NOTE]
> <span data-ttu-id="46f17-161">Se a sua extensão exigir uma política de privacidade e você não tiver fornecido uma, seu envio poderá falhar na certificação.</span><span class="sxs-lookup"><span data-stu-id="46f17-161">If your Extension requires a privacy policy and you have not provided one, your submission may fail certification.</span></span>  

<span data-ttu-id="46f17-162">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-162">**Possible Values**:</span></span>  

*   `No`<span data-ttu-id="46f17-163">: Uma URL de política de privacidade é opcional.</span><span class="sxs-lookup"><span data-stu-id="46f17-163">:  A privacy policy URL is optional.</span></span>  
*   `Yes`<span data-ttu-id="46f17-164">: É preciso uma URL de política de privacidade.</span><span class="sxs-lookup"><span data-stu-id="46f17-164">:  A privacy policy URL is required.</span></span>  

#### <span data-ttu-id="46f17-165">URL da política de privacidade</span><span class="sxs-lookup"><span data-stu-id="46f17-165">Privacy policy URL</span></span>  

<span data-ttu-id="46f17-166">Você é responsável por assegurar que sua extensão esteja em conformidade com as leis e regulamentos de privacidade, e para fornecer uma URL de política de privacidade válida, se necessário.</span><span class="sxs-lookup"><span data-stu-id="46f17-166">You are responsible for ensuring your Extension complies with privacy laws and regulations, and for providing a valid privacy policy URL, if required.</span></span>  <span data-ttu-id="46f17-167">Você deve fornecer uma URL de política de privacidade se qualquer informação pessoal estiver sendo acessada, transmitida ou coletada pela extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-167">You must provide a privacy policy URL if any personal information is being accessed, transmitted, or collected by your Extension.</span></span>  
<span data-ttu-id="46f17-168">Para determinar se sua extensão requer uma política de privacidade, examine o [contrato de desenvolvedor do Microsoft Edge][MicrosoftAppDeveloperAgreement] e o [documento de políticas de desenvolvimento de catálogos de Complementos do Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="46f17-168">To determine if your Extension requires a privacy policy, review the [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] and the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="46f17-169">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-169">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="46f17-170">URL do site</span><span class="sxs-lookup"><span data-stu-id="46f17-170">Website URL</span></span>  

<span data-ttu-id="46f17-171">Essa propriedade é opcional.</span><span class="sxs-lookup"><span data-stu-id="46f17-171">This property is Optional.</span></span>  
<span data-ttu-id="46f17-172">A URL da página da Web para sua extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-172">The URL of the web page for your Extension.</span></span>  <span data-ttu-id="46f17-173">Esta URL deve apontar para uma página em seu próprio site, não para a listagem da Web para sua extensão nos Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-173">This URL must point to a page on your own website, not the web listing for your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="46f17-174">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-174">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="46f17-175">URL de suporte/endereço de email</span><span class="sxs-lookup"><span data-stu-id="46f17-175">Support URL/email address</span></span>  

<span data-ttu-id="46f17-176">Essa propriedade é opcional.</span><span class="sxs-lookup"><span data-stu-id="46f17-176">This property is Optional.</span></span>  
<span data-ttu-id="46f17-177">A URL da página da Web em que os usuários vão para dar suporte à sua extensão ou a um endereço de email para o contatarem para obter suporte.</span><span class="sxs-lookup"><span data-stu-id="46f17-177">The URL of the web page where users go for support with your Extension, or an email address to contact you for support.</span></span>  <span data-ttu-id="46f17-178">Você inclui informações de suporte para todos os envios, para que seus usuários saibam como obter suporte de você.</span><span class="sxs-lookup"><span data-stu-id="46f17-178">You include support information for all submissions, so that your users know how to get support from you.</span></span>  

<span data-ttu-id="46f17-179">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-179">**Possible Values**:</span></span>  

*   `{email_address}`  
*   `{url}`  

#### <span data-ttu-id="46f17-180">Classificação de extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-180">Extension Rating</span></span>  

<span data-ttu-id="46f17-181">A classificação da extensão nos ajuda a determinar a idade do público-alvo da sua extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-181">Extension rating helps us determine the age of the target audience of your Extension.</span></span>  
<span data-ttu-id="46f17-182">Para ajudá-lo a determinar se suas extensões têm um conteúdo maduro, examine o [documento de políticas de desenvolvimento de catálogos de Complementos do Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="46f17-182">To help you determine if your Extensions has a mature content, review the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="46f17-183">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-183">**Possible Values**:</span></span>  

*   <span data-ttu-id="46f17-184">Adulto \ (caixa de seleção \): Marque esta caixa se sua extensão contiver qualquer conteúdo maduro.</span><span class="sxs-lookup"><span data-stu-id="46f17-184">Mature \(checkbox\): Check this box if your Extension contains any mature content.</span></span>  <span data-ttu-id="46f17-185">Se você selecionar adulto para a sua extensão, sua listagem estará disponível com uma marca separada para indicar que a extensão contém conteúdo maduro.</span><span class="sxs-lookup"><span data-stu-id="46f17-185">If you select mature for your Extension, your listing is available with a separate tag to indicate that the Extension contains mature content.</span></span>  

<span data-ttu-id="46f17-186">Clique em **salvar** para passar para a seção de listagem.</span><span class="sxs-lookup"><span data-stu-id="46f17-186">Click **Save** to proceed to listing section.</span></span>  

## <span data-ttu-id="46f17-187">Etapa 5: adicionar informações de listagens para a extensão</span><span class="sxs-lookup"><span data-stu-id="46f17-187">Step 5: Add Listings Information for Your Extension</span></span>  

<span data-ttu-id="46f17-188">Estas são as informações que os usuários visualizam ao exibir sua listagem em Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-188">This is the information that users see when viewing your listing in Microsoft Edge Addons.</span></span>  <span data-ttu-id="46f17-189">Muitos dos campos em uma listagem são opcionais, mas sugerimos fornecer o máximo de informações possível para destacar a sua listagem.  O mínimo necessário para sua listagem nos Complementos do Microsoft Edge ser considerado concluído é a [Descrição do texto](#description), o [logotipo da extensão](#store-logo)e o [bloco promocional pequeno](#small-promotional-tile) em cada idioma mencionado em seu pacote de extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-189">Many of the fields in a listing are optional, but we suggest providing as much information as possible to make your listing stand out.  The minimum required for your listing in Microsoft Edge Addons to be considered complete is the [text description](#description), [Extension logo](#store-logo), and [small promotional tile](#small-promotional-tile) in each language mentioned in your Extension package.</span></span>  

### <span data-ttu-id="46f17-190">Campos de listagem da loja</span><span class="sxs-lookup"><span data-stu-id="46f17-190">Store Listing fields</span></span>  

*   [<span data-ttu-id="46f17-191">Idiomas da listagem da Loja</span><span class="sxs-lookup"><span data-stu-id="46f17-191">Store listing languages</span></span>](#store-listing-languages)  
*   [<span data-ttu-id="46f17-192">Nome de exibição da loja</span><span class="sxs-lookup"><span data-stu-id="46f17-192">Store display name</span></span>](#store-display-name)  
*   [<span data-ttu-id="46f17-193">Descrição</span><span class="sxs-lookup"><span data-stu-id="46f17-193">Description</span></span>](#description)  
*   [<span data-ttu-id="46f17-194">Logotipo da loja</span><span class="sxs-lookup"><span data-stu-id="46f17-194">Store logo</span></span>](#store-logo)  
*   [<span data-ttu-id="46f17-195">Bloco promocional pequeno</span><span class="sxs-lookup"><span data-stu-id="46f17-195">Small promotional tile</span></span>](#small-promotional-tile)  
*   [<span data-ttu-id="46f17-196">Mídia</span><span class="sxs-lookup"><span data-stu-id="46f17-196">Media</span></span>](#media)  
*   [<span data-ttu-id="46f17-197">Descrição breve</span><span class="sxs-lookup"><span data-stu-id="46f17-197">Short description</span></span>](#short-description)  
*   [<span data-ttu-id="46f17-198">Termos de pesquisa</span><span class="sxs-lookup"><span data-stu-id="46f17-198">Search terms</span></span>](#search-terms)  

#### <span data-ttu-id="46f17-199">Idiomas da listagem da Loja</span><span class="sxs-lookup"><span data-stu-id="46f17-199">Store listing languages</span></span>  

<span data-ttu-id="46f17-200">Se o pacote de extensão oferecer suporte a vários idiomas, a extensão deverá ter uma página de listagem para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="46f17-200">If your Extension package supports multiple languages, your Extension must have a listing page for each one.</span></span>  
<span data-ttu-id="46f17-201">Você deve preencher detalhes da lista \ (descrição de texto, imagens e assim por diante \) para cada idioma separadamente, mesmo se estiver usando o mesmo conteúdo para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="46f17-201">You must complete listing details \(text description, images, and so on\) for each language separately even if you are using the same content for each language.</span></span>  <span data-ttu-id="46f17-202">Se a extensão for localizada em mais de um idioma, esses idiomas serão exibidos na parte superior da página de listagem.</span><span class="sxs-lookup"><span data-stu-id="46f17-202">If your Extension is localized in more than one language, those languages are displayed at the top of listing page.</span></span>  

1.  <span data-ttu-id="46f17-203">Selecione um nome de idioma na lista suspensa **idiomas** .</span><span class="sxs-lookup"><span data-stu-id="46f17-203">Select any one language name from **Languages** drop-down list.</span></span>  
1.  <span data-ttu-id="46f17-204">Preencha os detalhes da listagem.</span><span class="sxs-lookup"><span data-stu-id="46f17-204">Fill the listing details.</span></span>  
1.  <span data-ttu-id="46f17-205">Clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="46f17-205">Click **Save**.</span></span>  
1.  <span data-ttu-id="46f17-206">Repita o procedimento para todos os seus idiomas suportados.</span><span class="sxs-lookup"><span data-stu-id="46f17-206">Repeat for all of your supported languages.</span></span>  

> [!NOTE]
> <span data-ttu-id="46f17-207">Para adicionar ou remover idiomas para sua listagem nos Complementos do Microsoft Edge, você deve modificar a lista de idiomas com suporte no seu pacote de extensão e carregá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="46f17-207">To add or remove languages for your listing in Microsoft Edge Addons, you must modify the list of languages supported by your Extension package and re-upload it.</span></span>  

<span data-ttu-id="46f17-208">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-208">**Possible Values**:</span></span>  

*   `English (United States)`<span data-ttu-id="46f17-209">: Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="46f17-209">:  This is the default value.</span></span>  <span data-ttu-id="46f17-210">Se você não mencionar qualquer idioma em seu pacote, definimos seu idioma padrão para inglês \ (Estados Unidos \) e você deve fornecer uma listagem em inglês \ (Estados Unidos \).</span><span class="sxs-lookup"><span data-stu-id="46f17-210">If you do not mention any language in your package, we set your default language to English \(United States\) and you must provide a listing in English \(United States\).</span></span>  
*   `{language}` <span data-ttu-id="46f17-211">\(`{Country}`\)</span><span class="sxs-lookup"><span data-stu-id="46f17-211">\(`{Country}`\)</span></span>  

#### <span data-ttu-id="46f17-212">Nome de exibição da loja</span><span class="sxs-lookup"><span data-stu-id="46f17-212">Store display name</span></span>  

<span data-ttu-id="46f17-213">O nome da extensão conforme mencionado no manifesto do pacote de extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-213">The name of Extension as mentioned in your Extension package manifest.</span></span>  

> [!NOTE]
> <span data-ttu-id="46f17-214">Para editar o nome, você deve atualizar o manifesto em seu pacote de extensão e carregá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="46f17-214">To edit the name, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="46f17-215">Descrição</span><span class="sxs-lookup"><span data-stu-id="46f17-215">Description</span></span>  

<span data-ttu-id="46f17-216">Este campo é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46f17-216">This field is required.</span></span>  
<span data-ttu-id="46f17-217">A descrição para seus usuários do que sua extensão faz.</span><span class="sxs-lookup"><span data-stu-id="46f17-217">The description for your users of what your Extension does.</span></span>  

<span data-ttu-id="46f17-218">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-218">**Possible Values**:</span></span>  

*   <span data-ttu-id="46f17-219">{plain_text}: menos de 10.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="46f17-219">{plain_text}: Less than 10,000 characters.</span></span>  

#### <span data-ttu-id="46f17-220">Logotipo da loja</span><span class="sxs-lookup"><span data-stu-id="46f17-220">Store logo</span></span>  

<span data-ttu-id="46f17-221">Este campo é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46f17-221">This field is required.</span></span>  
<span data-ttu-id="46f17-222">Uma imagem do 1:1 para o seu logotipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="46f17-222">A 1:1 image for your Extension logo.</span></span>  

<span data-ttu-id="46f17-223">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-223">**Possible Values**:</span></span>  

*   <span data-ttu-id="46f17-224">128px x 128px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="46f17-224">128px x 128px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="46f17-225">150px x 140px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="46f17-225">150px x 140px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="46f17-226">300px x 300px, PNG \ (. png \): o tamanho recomendado.</span><span class="sxs-lookup"><span data-stu-id="46f17-226">300px x 300px, PNG \(.png\):  The recommended size.</span></span>  

#### <span data-ttu-id="46f17-227">Bloco promocional pequeno</span><span class="sxs-lookup"><span data-stu-id="46f17-227">Small promotional tile</span></span>  

<span data-ttu-id="46f17-228">Este campo é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="46f17-228">This field is required.</span></span>  
<span data-ttu-id="46f17-229">Um bloco promocional de tamanho pequeno.</span><span class="sxs-lookup"><span data-stu-id="46f17-229">A small size promotional tile.</span></span>  <span data-ttu-id="46f17-230">Sua listagem será exibida neste bloco.</span><span class="sxs-lookup"><span data-stu-id="46f17-230">Your listing is displayed on this tile.</span></span>  

<span data-ttu-id="46f17-231">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-231">**Possible Values**:</span></span>  

*   <span data-ttu-id="46f17-232">440px x 280X, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="46f17-232">440px x 280x, PNG \(.png\)</span></span>  

#### <span data-ttu-id="46f17-233">Mídia</span><span class="sxs-lookup"><span data-stu-id="46f17-233">Media</span></span>  

<span data-ttu-id="46f17-234">Este campo é opcional.</span><span class="sxs-lookup"><span data-stu-id="46f17-234">This field is optional.</span></span>  
<span data-ttu-id="46f17-235">Você deve fornecer esses ativos para ajudar a exibir seu produto com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="46f17-235">You should provide these assets to help display your product more effectively.</span></span>  

*   <span data-ttu-id="46f17-236">Capturas de tela</span><span class="sxs-lookup"><span data-stu-id="46f17-236">Screenshots</span></span>  
    <span data-ttu-id="46f17-237">As imagens da extensão que descrevem o que a extensão faz.</span><span class="sxs-lookup"><span data-stu-id="46f17-237">The images of your Extension that describe what your Extension does.</span></span>  
    
*   <span data-ttu-id="46f17-238">Blocos de promoção grandes</span><span class="sxs-lookup"><span data-stu-id="46f17-238">Large promotion tiles</span></span>  
    <span data-ttu-id="46f17-239">Um bloco promocional grande para apresentar a extensão mais proeminente em Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-239">A large promotional tile to be feature your Extension more prominently in Microsoft Edge Addons.</span></span>  
    
*   <span data-ttu-id="46f17-240">URL de vídeo do YouTube</span><span class="sxs-lookup"><span data-stu-id="46f17-240">YouTube video URL</span></span>  
    <span data-ttu-id="46f17-241">Uma [URL de vídeo do YouTube válida para a extensão][MicrosoftEdgeAddonsUploadYouTubeVideo].</span><span class="sxs-lookup"><span data-stu-id="46f17-241">A valid [YouTube video URL for your Extension][MicrosoftEdgeAddonsUploadYouTubeVideo].</span></span>  <span data-ttu-id="46f17-242">Seu vídeo deve ter uma boa qualidade e comprimento mínimo.</span><span class="sxs-lookup"><span data-stu-id="46f17-242">Your video should be good quality and minimal length.</span></span>  <span data-ttu-id="46f17-243">Seu vídeo do YouTube deve passar certificação antes de publicar sua extensão nos Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-243">Your YouTube video must pass certification before publishing your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="46f17-244">Verifique se o seu vídeo do YouTube está de acordo com o [documento de políticas de desenvolvimento de catálogos de Complementos do Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="46f17-244">Verify that your YouTube video complies with the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="46f17-245">**Valores possíveis**:</span><span class="sxs-lookup"><span data-stu-id="46f17-245">**Possible Values**:</span></span>  

*   <span data-ttu-id="46f17-246">10 capturas de tela no máximo.</span><span class="sxs-lookup"><span data-stu-id="46f17-246">10 Screenshots maximum.</span></span>  
    *   <span data-ttu-id="46f17-247">640 PX x 480px, PNG \ (. png \): capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="46f17-247">640px x 480px, PNG \(.png\):  Screenshots.</span></span>  
    *   <span data-ttu-id="46f17-248">1280px x 800px, PNG \ (. png \): capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="46f17-248">1280px x 800px, PNG \(.png\):  Screenshots.</span></span>  
*   <span data-ttu-id="46f17-249">1400px x 560px, PNG \ (. png \): blocos grandes de promoção.</span><span class="sxs-lookup"><span data-stu-id="46f17-249">1400px x 560px, PNG \(.png\):  Large promotion tiles.</span></span>  
*   <span data-ttu-id="46f17-250">60 segundos ou mais curto e 2 GB ou menor, URL de vídeo do YouTube.</span><span class="sxs-lookup"><span data-stu-id="46f17-250">60 seconds or shorter and 2GB or smaller, YouTube video URL.</span></span>  

#### <span data-ttu-id="46f17-251">Descrição breve</span><span class="sxs-lookup"><span data-stu-id="46f17-251">Short description</span></span>  

<span data-ttu-id="46f17-252">Uma descrição curta e curta que pode ser usada na parte superior da listagem do seu produto.</span><span class="sxs-lookup"><span data-stu-id="46f17-252">A short, catchy description that may be used at the top of the listing for your product.</span></span>  <span data-ttu-id="46f17-253">Se não for fornecido, as primeiras linhas da descrição mais longa serão usadas em vez disso.</span><span class="sxs-lookup"><span data-stu-id="46f17-253">If not provided, the first few lines from your longer description are used instead.</span></span>  <span data-ttu-id="46f17-254">Como a descrição também aparece abaixo desse texto, você deve fornecer uma breve descrição com texto diferente para que sua listagem seja menos repetitiva.</span><span class="sxs-lookup"><span data-stu-id="46f17-254">Because your description also appears below this text, you should provide a short description with different text so that your listing is less repetitive.</span></span>  <span data-ttu-id="46f17-255">A breve descrição da extensão é separada diretamente do arquivo de manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="46f17-255">The Short description of your Extension is picked directly from the manifest file of your package.</span></span>  

> [!NOTE]
> <span data-ttu-id="46f17-256">Para editar a descrição resumida, você deve atualizar o manifesto em seu pacote de extensão e carregá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="46f17-256">To edit the short description, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="46f17-257">Termos de pesquisa</span><span class="sxs-lookup"><span data-stu-id="46f17-257">Search terms</span></span>  

<span data-ttu-id="46f17-258">Termos de pesquisa são palavras únicas ou frases curtas que não são exibidas para os usuários, mas ajudam a torná-la detectável nos Complementos do Microsoft Edge quando os usuários pesquisam usando esses termos.</span><span class="sxs-lookup"><span data-stu-id="46f17-258">Search terms are single words or short phrases that are not displayed to users but help make your Extension discoverable in Microsoft Edge Addons when users search using those terms.</span></span>  

<span data-ttu-id="46f17-259">**Requisitos**:</span><span class="sxs-lookup"><span data-stu-id="46f17-259">**Requirements**:</span></span>  

*   <span data-ttu-id="46f17-260">7 ou menos termos de pesquisa</span><span class="sxs-lookup"><span data-stu-id="46f17-260">7 or fewer search terms</span></span>  
*   <span data-ttu-id="46f17-261">30 ou menos caracteres por termo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="46f17-261">30 or fewer characters per search term</span></span>  
*   <span data-ttu-id="46f17-262">21 ou menos palavras para termos de pesquisa combinados</span><span class="sxs-lookup"><span data-stu-id="46f17-262">21 or fewer words for combined search terms</span></span>  

<span data-ttu-id="46f17-263">Clique em **salvar** para continuar para salvar a seção de listagem.</span><span class="sxs-lookup"><span data-stu-id="46f17-263">Click **Save** to proceed to save your listing section.</span></span>  <span data-ttu-id="46f17-264">Clique em **publicar** para fornecer detalhes de envio.</span><span class="sxs-lookup"><span data-stu-id="46f17-264">Click **Publish** to provide submission details.</span></span>  

## <span data-ttu-id="46f17-265">Etapa 6: concluir o envio e clicar em publicar</span><span class="sxs-lookup"><span data-stu-id="46f17-265">Step 6: Complete your submission and click Publish</span></span>  

<span data-ttu-id="46f17-266">A página opções de envio do processo de envio de extensão é onde você fornece mais informações para nos ajudar a testar o produto corretamente.</span><span class="sxs-lookup"><span data-stu-id="46f17-266">The Submission options page of the Extension submission process is where you provide more information to help us test your product properly.</span></span>  <span data-ttu-id="46f17-267">Essa é uma etapa opcional, mas é recomendável para muitos envios.</span><span class="sxs-lookup"><span data-stu-id="46f17-267">This is an optional step, but it is recommended for many submissions.</span></span>  

### <span data-ttu-id="46f17-268">Opções de suspensão de publicação</span><span class="sxs-lookup"><span data-stu-id="46f17-268">Publishing hold options</span></span>  

<span data-ttu-id="46f17-269">Por padrão, o envio é publicado assim que ele passa a certificação.</span><span class="sxs-lookup"><span data-stu-id="46f17-269">By default, your submission is published as soon as it passes certification.</span></span>  <span data-ttu-id="46f17-270">Você pode optar por colocar uma espera na publicação do envio até uma data específica.</span><span class="sxs-lookup"><span data-stu-id="46f17-270">You may choose to place a hold on publishing your submission until a specific date.</span></span>  <span data-ttu-id="46f17-271">As opções desta seção são descritas a seguir.</span><span class="sxs-lookup"><span data-stu-id="46f17-271">The options in this section are described below.</span></span>  

*   **<span data-ttu-id="46f17-272">Publicar o envio assim que ele passar na certificação</span><span class="sxs-lookup"><span data-stu-id="46f17-272">Publish your submission as soon as it passes certification</span></span>**  

    <span data-ttu-id="46f17-273">Esta é a seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="46f17-273">This is the default selection.</span></span>  <span data-ttu-id="46f17-274">Isso significa que seu envio começa o processo de publicação assim que passa a certificação</span><span class="sxs-lookup"><span data-stu-id="46f17-274">It means that your submission begins the publishing process as soon as it passes certification</span></span>  

*   **<span data-ttu-id="46f17-275">Iniciar a publicação de seu envio em uma data específica</span><span class="sxs-lookup"><span data-stu-id="46f17-275">Start publishing your submission on a certain date</span></span>**  

    <span data-ttu-id="46f17-276">Escolha **iniciar a publicação do envio em uma determinada data** para garantir que o envio não seja publicado até uma data específica.</span><span class="sxs-lookup"><span data-stu-id="46f17-276">Choose **Start publishing your submission on a certain date** to ensure that the submission is not published until a specific date.</span></span>  <span data-ttu-id="46f17-277">Com essa opção, seu envio é lançado o mais rápido possível em ou após a data que você especificar.</span><span class="sxs-lookup"><span data-stu-id="46f17-277">With this option, your submission is released as soon as possible on or after the date you specify.</span></span>  <span data-ttu-id="46f17-278">A data deve ser pelo menos 24 horas no futuro.</span><span class="sxs-lookup"><span data-stu-id="46f17-278">The date must be at least 24 hours in the future.</span></span>  <span data-ttu-id="46f17-279">Juntamente com a data, você pode especificar a hora em que o envio deve começar a ser publicado.</span><span class="sxs-lookup"><span data-stu-id="46f17-279">Along with the date, you may specify the time at which the submission should begin to be published.</span></span>  

### <span data-ttu-id="46f17-280">Notas para certificação</span><span class="sxs-lookup"><span data-stu-id="46f17-280">Notes for certification</span></span>  

<span data-ttu-id="46f17-281">À medida que você envia a extensão, tem a opção de usar a página anotações para certificação para fornecer informações adicionais aos testadores de certificação.</span><span class="sxs-lookup"><span data-stu-id="46f17-281">As you submit your Extension, you have the option to use the Notes for certification page to provide additional information to the certification testers.</span></span>  <span data-ttu-id="46f17-282">Essas informações ajudam a garantir que sua extensão seja testada corretamente.</span><span class="sxs-lookup"><span data-stu-id="46f17-282">This information helps ensure that your Extension is tested correctly.</span></span>  <span data-ttu-id="46f17-283">Se não pudermos testar completamente o envio, pode haver falha na certificação.</span><span class="sxs-lookup"><span data-stu-id="46f17-283">If we are not able to fully test your submission, it may fail certification.</span></span>  

<span data-ttu-id="46f17-284">Certifique-se de incluir o seguinte \ (se aplicável à sua extensão \):</span><span class="sxs-lookup"><span data-stu-id="46f17-284">Make sure to include the following \(if applicable for your Extension\):</span></span>  

*   <span data-ttu-id="46f17-285">Nomes de usuário e senhas para contas de teste.</span><span class="sxs-lookup"><span data-stu-id="46f17-285">User names and passwords for test accounts.</span></span>  
*   <span data-ttu-id="46f17-286">Etapas para acessar recursos ocultos ou bloqueados.</span><span class="sxs-lookup"><span data-stu-id="46f17-286">Steps to access hidden or locked features.</span></span>  
*   <span data-ttu-id="46f17-287">Diferenças esperadas no comportamento com base na região ou em outras configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="46f17-287">Expected differences in behavior based on region or other user settings.</span></span>  
*   <span data-ttu-id="46f17-288">Informações sobre o que mudou em uma atualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46f17-288">Information about what changed in an app update.</span></span>  
*   <span data-ttu-id="46f17-289">Qualquer outra coisa que você acha que os testadores devem entender sobre o seu envio.</span><span class="sxs-lookup"><span data-stu-id="46f17-289">Anything else you think testers must understand about your submission.</span></span>  

<span data-ttu-id="46f17-290">Depois de concluir os detalhes acima, clique em **publicar** para enviar sua extensão nos Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="46f17-290">After completing the above details, click **Publish** to submit your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="46f17-291">Quando terminar de criar o envio para a extensão e clicar em **publicar**, o envio entrará na etapa de certificação.</span><span class="sxs-lookup"><span data-stu-id="46f17-291">When you finish creating the submission for your Extension and click **Publish**, the submission enters the certification step.</span></span>  <span data-ttu-id="46f17-292">Geralmente, esse processo é concluído dentro de alguns dias, mas em alguns casos pode levar até sete dias úteis.</span><span class="sxs-lookup"><span data-stu-id="46f17-292">This process usually is completed within a couple of days, though in some cases it may take up to 7 business days.</span></span>  <span data-ttu-id="46f17-293">Depois que seu envio for aprovado na certificação, sua extensão será publicada nos Complementos do Microsoft Edge, a menos que você tenha selecionado as opções de retenção de publicação para especificar que ele não deve ser liberado até uma determinada data.</span><span class="sxs-lookup"><span data-stu-id="46f17-293">After your submission passes certification, your Extension is published in Microsoft Edge Addons unless you selected the Publishing hold options to specify that it should not be released until a certain date.</span></span>  <span data-ttu-id="46f17-294">Você será notificado quando o envio for publicado, e o status da extensão no painel mudará para `In the Store` .</span><span class="sxs-lookup"><span data-stu-id="46f17-294">You are notified when your submission is published, and the status of your Extension in the dashboard changes to `In the Store`.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introdução ao Microsoft Edge \ (Chromium \) extensões | Documentos da Microsoft"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Carregar um vídeo do YouTube | Documentos da Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Políticas de desenvolvedor de catálogo de Complementos do Microsoft Edge | Documentos da Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de desenvolvedor de aplicativos | Documentos da Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Central de parceiros"  
