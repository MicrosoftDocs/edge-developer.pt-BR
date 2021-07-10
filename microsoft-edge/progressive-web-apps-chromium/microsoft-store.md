---
description: Tornar sua PWA mais descoberta por meio da publicação no Microsoft Store
title: Publique seu Aplicativo Web Progressivo no Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Borda, Windows, Microsoft Store
ms.openlocfilehash: 40a6b94412a0788c87f7231025809098c98f18e9
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643246"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="185f6-104">Publique seu Aplicativo Web Progressivo no Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="185f6-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="185f6-105">Publicar seu Aplicativo Web Progressivo \(PWA\) para o Microsoft Store [traz][WindowsUwpPublishIndex] as seguintes vantagens.</span><span class="sxs-lookup"><span data-stu-id="185f6-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="185f6-106">Detectabilidade</span><span class="sxs-lookup"><span data-stu-id="185f6-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="185f6-107">Os usuários procurarão naturalmente aplicativos na loja de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="185f6-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="185f6-108">Quando você publica no Microsoft Store, milhões de Windows usuários podem descobrir sua PWA juntamente com outros Windows aplicativos.</span><span class="sxs-lookup"><span data-stu-id="185f6-108">When you publish to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="185f6-109">A Loja mostra aplicativos por meio de categorias, coleções com curadoria e muito mais.</span><span class="sxs-lookup"><span data-stu-id="185f6-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="185f6-110">Os portais de descoberta de aplicativos oferecem uma experiência fácil de navegação e compras para os possíveis usuários do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185f6-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="185f6-111">Você pode até [aprimorar sua listagem da Loja][WindowsUwpPublishAppScreenshotsImages] com capturas de tela, uma imagem de herói e trailers de vídeo.</span><span class="sxs-lookup"><span data-stu-id="185f6-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="185f6-112">Confiabilidade</span><span class="sxs-lookup"><span data-stu-id="185f6-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="185f6-113">Windows clientes sabem que podem confiar em suas Microsoft Store e downloads, porque eles aderem aos rigorosos padrões de segurança e qualidade [da][LegalWindowsAgreementsStorePolicies]Microsoft.</span><span class="sxs-lookup"><span data-stu-id="185f6-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="185f6-114">Instalação fácil</span><span class="sxs-lookup"><span data-stu-id="185f6-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="185f6-115">O Microsoft Store fornece uma experiência de instalação consistente e fácil de usar em todos [os Windows 10 aplicativos][MicrosoftStoreAppsWindows].</span><span class="sxs-lookup"><span data-stu-id="185f6-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="185f6-116">Análise de aplicativos</span><span class="sxs-lookup"><span data-stu-id="185f6-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="185f6-117">O [Windows painel do Partner][WindowsUwpPublishIndex] Center [][WindowsUwpPublishAnalytics] fornece análises detalhadas sobre a saúde do aplicativo, uso e muito mais.</span><span class="sxs-lookup"><span data-stu-id="185f6-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="185f6-118">Para publicar sua PWA no Microsoft Store, nenhuma alteração de código é necessária.</span><span class="sxs-lookup"><span data-stu-id="185f6-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="185f6-119">Em vez disso, crie uma reserva de aplicativo, empacote sua PWA e envie seu pacote para a Loja.</span><span class="sxs-lookup"><span data-stu-id="185f6-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="185f6-120">As seções a seguir explicam as etapas.</span><span class="sxs-lookup"><span data-stu-id="185f6-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="185f6-121">Criar uma reserva de aplicativo</span><span class="sxs-lookup"><span data-stu-id="185f6-121">Create an app reservation</span></span>  

<span data-ttu-id="185f6-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] é o hub para você enviar seu aplicativo para o Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="185f6-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="185f6-123">Para criar uma reserva de aplicativo, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="185f6-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="185f6-124">Para exibir seus programas inscritos, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="185f6-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="185f6-125">Entre no Windows Partner Center com sua conta da Microsoft e navegue até o [Painel do Partner Center][MicrosoftPartnerDashboardHome].</span><span class="sxs-lookup"><span data-stu-id="185f6-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="185f6-126">Navegue **até Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="185f6-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="185f6-127">Se **Windows & Xbox** for exibido, seu aplicativo já está inscrito.</span><span class="sxs-lookup"><span data-stu-id="185f6-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="185f6-128">Se **Windows & Xbox** não for exibido, escolha **Adicionar programa**.</span><span class="sxs-lookup"><span data-stu-id="185f6-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Adicionar um programa no painel Windows Partner Center" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="185f6-130">Adicionar um programa no painel Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="185f6-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="185f6-131">Para se inscrever no programa de desenvolvedor, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="185f6-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="185f6-132">Navegue **até Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="185f6-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="185f6-133">Escolha **Começar.**</span><span class="sxs-lookup"><span data-stu-id="185f6-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="185f6-134">Siga os avisos.</span><span class="sxs-lookup"><span data-stu-id="185f6-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="185f6-135">Agora, sua conta está inscrita no programa de desenvolvedor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="185f6-135">Now, your account is enrolled in the app developer program.</span></span> <span data-ttu-id="185f6-136">Para criar uma reserva de aplicativo, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="185f6-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="185f6-137">Navegue **até Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="185f6-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="185f6-138">Escolha **Visão geral**Criar um novo  >  **aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="185f6-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="185f6-139">Digite o nome do aplicativo no prompt.</span><span class="sxs-lookup"><span data-stu-id="185f6-139">Type the name of your app in the prompt.</span></span>  
    1.  <span data-ttu-id="185f6-140">Escolha `Reserve product name` .</span><span class="sxs-lookup"><span data-stu-id="185f6-140">Choose `Reserve product name`.</span></span>  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Criar uma reserva de aplicativo no Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="185f6-142">Criar uma reserva de aplicativo no Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="185f6-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="185f6-143">Para exibir os detalhes do editor para uso na seção [Pacote de PWA,](#package-your-pwa-for-the-store) escolha **Product management**  >  **Product Identity**.</span><span class="sxs-lookup"><span data-stu-id="185f6-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa-for-the-store) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copie as informações do seu editor Windows Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="185f6-145">Copie as informações do seu editor Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="185f6-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="185f6-146">Copie e salve os seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="185f6-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="185f6-147">ID do pacote</span><span class="sxs-lookup"><span data-stu-id="185f6-147">Package ID</span></span>**  
    *   **<span data-ttu-id="185f6-148">Publisher ID</span><span class="sxs-lookup"><span data-stu-id="185f6-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="185f6-149">Publisher Nome para exibição</span><span class="sxs-lookup"><span data-stu-id="185f6-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa-for-the-store"></a><span data-ttu-id="185f6-150">Empacote seu PWA para a Loja</span><span class="sxs-lookup"><span data-stu-id="185f6-150">Package your PWA for the Store</span></span> 

<span data-ttu-id="185f6-151">Agora que você tem as informações de publicação do aplicativo, gere um pacote Windows aplicativo para sua PWA.</span><span class="sxs-lookup"><span data-stu-id="185f6-151">Now that you have your app publishing information, generate a Windows app package for your PWA.</span></span>

<span data-ttu-id="185f6-152">Para gerar um pacote de aplicativos, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="185f6-152">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="185f6-153">Navegue [até PWA Builder][PwabuilderMain].</span><span class="sxs-lookup"><span data-stu-id="185f6-153">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="185f6-154">Digite a URL do seu PWA.</span><span class="sxs-lookup"><span data-stu-id="185f6-154">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="185f6-155">Escolha **Iniciar**  >  **Criar Minhas PWA**  >  **Windows**  >  **Opções**.</span><span class="sxs-lookup"><span data-stu-id="185f6-155">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="185f6-156">Colar os seguintes valores que você salvou na seção [Criar uma reserva de](#create-an-app-reservation) aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185f6-156">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="185f6-157">ID do pacote</span><span class="sxs-lookup"><span data-stu-id="185f6-157">Package ID</span></span>**  
    *   **<span data-ttu-id="185f6-158">Publisher ID</span><span class="sxs-lookup"><span data-stu-id="185f6-158">Publisher ID</span></span>**  
    *   **<span data-ttu-id="185f6-159">Publisher Nome para exibição</span><span class="sxs-lookup"><span data-stu-id="185f6-159">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Colar informações do editor no PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="185f6-161">Colar informações do editor no PWABuilder</span><span class="sxs-lookup"><span data-stu-id="185f6-161">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="185f6-162">Escolha **Feito**.</span><span class="sxs-lookup"><span data-stu-id="185f6-162">Choose **Done**.</span></span>  
1.  <span data-ttu-id="185f6-163">Para baixar o pacote Windows aplicativo, escolha **Baixar**.</span><span class="sxs-lookup"><span data-stu-id="185f6-163">To download your Windows app package, choose **Download**.</span></span>

<span data-ttu-id="185f6-164">Seu download é um `.zip` arquivo morto que contém um arquivo e um `.msixbundle` `.classic.appxbundle` arquivo.</span><span class="sxs-lookup"><span data-stu-id="185f6-164">Your download is a `.zip` archive that contains an `.msixbundle` file and a `.classic.appxbundle` file.</span></span>  <span data-ttu-id="185f6-165">Os dois pacotes de aplicativos permitem que PWA a sua versão seja executado em uma ampla variedade de Windows versões.</span><span class="sxs-lookup"><span data-stu-id="185f6-165">The two app packages allow your PWA to run on a wide variety of Windows versions.</span></span>  <span data-ttu-id="185f6-166">Para obter mais informações, navegue até [O que é um pacote clássico?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span><span class="sxs-lookup"><span data-stu-id="185f6-166">For more information, navigate to [What is a classic package?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="185f6-167">Enviar seu pacote de aplicativos para a Loja</span><span class="sxs-lookup"><span data-stu-id="185f6-167">Submit your app package to the Store</span></span>  

<span data-ttu-id="185f6-168">Para enviar seu aplicativo para a Loja, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="185f6-168">To submit your app to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="185f6-169">Navegue [até Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="185f6-169">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="185f6-170">Escolha seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185f6-170">Choose your app.</span></span>  
1.  <span data-ttu-id="185f6-171">Escolha **Iniciar seu Envio**.</span><span class="sxs-lookup"><span data-stu-id="185f6-171">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Iniciar um novo envio de aplicativo no Windows Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="185f6-173">Iniciar um novo envio de aplicativo no Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="185f6-173">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="185f6-174">Preencha os prompts a seguir para obter informações sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185f6-174">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="185f6-175">pricing</span><span class="sxs-lookup"><span data-stu-id="185f6-175">pricing</span></span>  
    *   <span data-ttu-id="185f6-176">classificação etária</span><span class="sxs-lookup"><span data-stu-id="185f6-176">age rating</span></span>  
    *   <span data-ttu-id="185f6-177">e mais</span><span class="sxs-lookup"><span data-stu-id="185f6-177">and more</span></span>  
        
1.  <span data-ttu-id="185f6-178">No prompt **Pacotes,** escolha os arquivos e os `.msixbundle` que você gerou na seção Pacote de `.classic.appxbundle` [PWA.](#package-your-pwa-for-the-store)</span><span class="sxs-lookup"><span data-stu-id="185f6-178">On the **Packages** prompt, choose the `.msixbundle` and the `.classic.appxbundle` files you generated in the [Package your PWA](#package-your-pwa-for-the-store) section.</span></span>  
    
<span data-ttu-id="185f6-179">Depois que você concluir seu envio, seu aplicativo será revisado, normalmente entre 24 e 48 horas.</span><span class="sxs-lookup"><span data-stu-id="185f6-179">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="185f6-180">Depois de receber aprovação, PWA seu Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="185f6-180">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

### <a name="measure-usage-of-your-store-installed-pwa"></a><span data-ttu-id="185f6-181">Medir o uso do seu PWA</span><span class="sxs-lookup"><span data-stu-id="185f6-181">Measure usage of your Store-installed PWA</span></span>

<span data-ttu-id="185f6-182">Quando o PWA é inicializado inicialmente, se o PWA foi instalado a partir do Microsoft Store, o Microsoft Edge inclui o seguinte header com a solicitação para a primeira navegação do seu `Referer` aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="185f6-182">When your PWA is initially launched, if the PWA was installed from the Microsoft Store, Microsoft Edge includes the following `Referer` header with the request for the first navigation of your web app.</span></span>

```
Referer: app-info://platform/microsoft-store
```

<span data-ttu-id="185f6-183">Use esse recurso para medir o tráfego distinto do seu PWA.</span><span class="sxs-lookup"><span data-stu-id="185f6-183">Use this feature to measure distinct traffic from your Store-installed PWA.</span></span>  <span data-ttu-id="185f6-184">Com base no tráfego, você pode ajustar o conteúdo do aplicativo para melhorar a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="185f6-184">Based on the traffic, you can adjust your app’s content to improve the user experience.</span></span>  <span data-ttu-id="185f6-185">Esse recurso é acessível ao código do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="185f6-185">This feature is accessible to both client and server code.</span></span>

<span data-ttu-id="185f6-186">Esse recurso foi introduzido na Microsoft Edge versão 91.</span><span class="sxs-lookup"><span data-stu-id="185f6-186">This feature was introduced in Microsoft Edge version 91.</span></span>

## <a name="see-also"></a><span data-ttu-id="185f6-187">Consulte também</span><span class="sxs-lookup"><span data-stu-id="185f6-187">See also</span></span>  

<span data-ttu-id="185f6-188">O PWABuilder fornece mais documentação para ajudá-lo a obter PWA no Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="185f6-188">PWABuilder provides more documentation to help you get your PWA in the Microsoft Store.</span></span>  

*   [<span data-ttu-id="185f6-189">Testar e enviar seu pacote PWA aplicativo</span><span class="sxs-lookup"><span data-stu-id="185f6-189">Test and submit your PWA app package</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [<span data-ttu-id="185f6-190">Publicar um novo PWA na Loja</span><span class="sxs-lookup"><span data-stu-id="185f6-190">Publish a new PWA to the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [<span data-ttu-id="185f6-191">Atualizar um aplicativo da Loja existente para um PWA</span><span class="sxs-lookup"><span data-stu-id="185f6-191">Update an existing Store app to a PWA</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [<span data-ttu-id="185f6-192">Recomendações de imagem para PWAs na Loja</span><span class="sxs-lookup"><span data-stu-id="185f6-192">Image recommendations for PWAs in the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [<span data-ttu-id="185f6-193">Explicador de empacotamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="185f6-193">App packaging explainer</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store Políticas | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analisar o desempenho do aplicativo | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de tela, imagens e trailers do aplicativo | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar Windows aplicativos e jogos | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Home | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para parceiros | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Aplicativos | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modelo de aplicativo hospedado | Windows Blog do Desenvolvedor"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "O que é um pacote clássico? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recomendações de imagem para Windows PWA pacotes | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Próximas etapas para obter seu PWA no Microsoft Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publicar um novo aplicativo na loja | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Atualizar um aplicativo existente na loja | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
