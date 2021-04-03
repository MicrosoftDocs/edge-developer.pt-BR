---
description: Os recursos experimentais mais recentes no Microsoft Edge para Aplicativos Web
title: Recursos experimentais | Aplicativos Web Progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474947"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="6bb16-104">Recursos experimentais em PWAs (Progressive Web Apps)</span><span class="sxs-lookup"><span data-stu-id="6bb16-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="6bb16-105">O Microsoft Edge fornece acesso a recursos experimentais que ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="6bb16-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="6bb16-106">Para determinar se cada recurso está pronto e quando lançar cada um, teste e [forneça comentários.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="6bb16-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="6bb16-107">Os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, mas os recursos experimentais mais recentes estão disponíveis apenas no canal Canary do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6bb16-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="6bb16-108">Ativar recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="6bb16-108">Turn on experimental features</span></span>  

<span data-ttu-id="6bb16-109">Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6bb16-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="6bb16-110">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6bb16-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="6bb16-111">Certifique-se de usar uma versão do Microsoft Edge que tenha o Experimento listado neste artigo.</span><span class="sxs-lookup"><span data-stu-id="6bb16-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="6bb16-112">Navegue até [Recursos Experimentais](#features-that-are-available-to-test).</span><span class="sxs-lookup"><span data-stu-id="6bb16-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="6bb16-113">Navegue até `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="6bb16-114">Navegue até o experimento relevante.</span><span class="sxs-lookup"><span data-stu-id="6bb16-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="6bb16-115">Escolha o menu suspenso ao lado da descrição do experimento e escolha `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Escolha Habilitado para ativar um experimento" lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="6bb16-117">Escolha **Habilitado para** ativar um experimento</span><span class="sxs-lookup"><span data-stu-id="6bb16-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6bb16-118">Cada experimento geralmente tem um menu suspenso para escolher os seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="6bb16-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="6bb16-119">Se um recurso experimental não tiver uma entrada em **Experimentos,** serão fornecidas instruções para iniciar o Microsoft Edge com esse recurso usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="6bb16-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="6bb16-120">Reinicie o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6bb16-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="6bb16-121">Avaliações de Origem</span><span class="sxs-lookup"><span data-stu-id="6bb16-121">Origin Trials</span></span>  

<span data-ttu-id="6bb16-122">O Microsoft Edge às vezes usa testes de origem para testar recursos para domínios ou sites específicos.</span><span class="sxs-lookup"><span data-stu-id="6bb16-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="6bb16-123">Talvez você queira usar uma avaliação de origem para seu site para aplicar um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="6bb16-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="6bb16-124">Se você for um proprietário de site, poderá se inscrever em uma avaliação de origem.</span><span class="sxs-lookup"><span data-stu-id="6bb16-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="6bb16-125">Uma avaliação de origem fornece recursos para uma porcentagem de usuários do Microsoft Edge que visitam seu site.</span><span class="sxs-lookup"><span data-stu-id="6bb16-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="6bb16-126">Para obter mais informações sobre as avaliação de origem, navegue até [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="6bb16-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="6bb16-127">Os recursos experimentais são constantemente atualizados e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="6bb16-128">Para desativar um recurso experimental, navegue até [Ativar recursos experimentais,](#turn-on-experimental-features)navegue até o experimento e escolha `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="6bb16-129">Recursos disponíveis para teste</span><span class="sxs-lookup"><span data-stu-id="6bb16-129">Features that are available to test</span></span>  

<span data-ttu-id="6bb16-130">A lista a seguir descreve os novos recursos experimentais do aplicativo Web que estão disponíveis para testar e validar no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6bb16-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="6bb16-131">Recurso</span><span class="sxs-lookup"><span data-stu-id="6bb16-131">Feature</span></span> | <span data-ttu-id="6bb16-132">Versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6bb16-132">Microsoft Edge version</span></span> | <span data-ttu-id="6bb16-133">Plataforma</span><span class="sxs-lookup"><span data-stu-id="6bb16-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="6bb16-134">Tratamento de protocolo URI</span><span class="sxs-lookup"><span data-stu-id="6bb16-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="6bb16-135">91 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6bb16-135">91 or later</span></span> | <span data-ttu-id="6bb16-136">Windows</span><span class="sxs-lookup"><span data-stu-id="6bb16-136">Windows</span></span> |    
| [<span data-ttu-id="6bb16-137">Manipulação de link de URL</span><span class="sxs-lookup"><span data-stu-id="6bb16-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="6bb16-138">91 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6bb16-138">91 or later</span></span> | <span data-ttu-id="6bb16-139">Windows</span><span class="sxs-lookup"><span data-stu-id="6bb16-139">Windows</span></span>|  
| [<span data-ttu-id="6bb16-140">Executar no logon do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6bb16-140">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="6bb16-141">88 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6bb16-141">88 or later</span></span> | <span data-ttu-id="6bb16-142">Todas</span><span class="sxs-lookup"><span data-stu-id="6bb16-142">All</span></span> |  
| [<span data-ttu-id="6bb16-143">Atalhos</span><span class="sxs-lookup"><span data-stu-id="6bb16-143">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="6bb16-144">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6bb16-144">87 or later</span></span> | <span data-ttu-id="6bb16-145">Todas</span><span class="sxs-lookup"><span data-stu-id="6bb16-145">All</span></span> |  
| [<span data-ttu-id="6bb16-146">Tratamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="6bb16-146">File Handling</span></span>](#file-handling) | <span data-ttu-id="6bb16-147">83 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6bb16-147">83 or later</span></span> | <span data-ttu-id="6bb16-148">Toda a área de trabalho</span><span class="sxs-lookup"><span data-stu-id="6bb16-148">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="6bb16-149">Tratamento de protocolo URI</span><span class="sxs-lookup"><span data-stu-id="6bb16-149">URI Protocol Handling</span></span>  

<span data-ttu-id="6bb16-150">Um identificador de recurso uniforme \(URI\) pode ser usado para definir mais do que apenas links para páginas da Web e conteúdo da Web usando o protocolo HTTP ou FTP.</span><span class="sxs-lookup"><span data-stu-id="6bb16-150">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="6bb16-151">URIs podem ser usadas para descrever links para qualquer coisa que você codificar em um esquema.</span><span class="sxs-lookup"><span data-stu-id="6bb16-151">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="6bb16-152">Por exemplo, o protocolo é usado para descrever um link de email e o sistema operacional \(OS\) ou navegador decide qual página da Web ou `mailto://` aplicativo deve lidar com esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="6bb16-152">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="6bb16-153">Para obter mais informações sobre o suporte baseado em navegador existente, navegue até manipuladores de protocolo [baseados na Web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]</span><span class="sxs-lookup"><span data-stu-id="6bb16-153">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="6bb16-154">Esse recurso permite que você conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="6bb16-154">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="6bb16-155">Registrar seu PWA com o sistema operacional host usando o manifesto do seu aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="6bb16-155">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="6bb16-156">Declare que um PWA lida com um protocolo URI específico</span><span class="sxs-lookup"><span data-stu-id="6bb16-156">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="6bb16-157">Depois de registrar um PWA como um manipulador de protocolo, quando um usuário escolhe um hiperlink com um esquema específico, como ou de um navegador ou um aplicativo nativo, o PWA registrado é ativado pelo sistema operacional e recebe o `mailto://` `web+music://` URI.</span><span class="sxs-lookup"><span data-stu-id="6bb16-157">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="6bb16-158">Esse recurso exige que você atualize o manifesto do aplicativo Web para incluir uma matriz, na matriz que você `protocol_handlers` precisa especificar dois campos:</span><span class="sxs-lookup"><span data-stu-id="6bb16-158">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="6bb16-159">: O protocolo para lidar com a solicitação, por exemplo `mailto` ou `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-159">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="6bb16-160">: O URI HTTPS no escopo do aplicativo que lida com o protocolo.</span><span class="sxs-lookup"><span data-stu-id="6bb16-160">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="6bb16-161">No futuro, o URI começando com o esquema de manipuladores de protocolo é planejado para substituir o `%s` token.</span><span class="sxs-lookup"><span data-stu-id="6bb16-161">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="6bb16-162">Atualize seu manifesto para dar suporte ao protocolo que você deseja registrar.</span><span class="sxs-lookup"><span data-stu-id="6bb16-162">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="6bb16-163">Depois de ativar esse recurso, o Microsoft Edge conclui as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="6bb16-163">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="6bb16-164">Detecta alterações no manifesto</span><span class="sxs-lookup"><span data-stu-id="6bb16-164">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="6bb16-165">Registra o aplicativo para o protocolo</span><span class="sxs-lookup"><span data-stu-id="6bb16-165">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="6bb16-166">Se mais de um aplicativo registrar um protocolo, o usuário será apresentado com um prompt.</span><span class="sxs-lookup"><span data-stu-id="6bb16-166">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="6bb16-167">O usuário escolhe o aplicativo apropriado na lista apresentada pelo sistema operacional ou navegador.</span><span class="sxs-lookup"><span data-stu-id="6bb16-167">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="6bb16-168">Para visualizar a manipulação de protocolo no Microsoft Edge no Windows, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e ause o Suporte a Manipuladores de Protocolo de **Desktop Web Apps.**</span><span class="sxs-lookup"><span data-stu-id="6bb16-168">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop Web Apps support Protocol Handlers**.</span></span>  

<span data-ttu-id="6bb16-169">Para obter mais informações sobre a avaliação de origem em execução para manipuladores de protocolo, navegue até Registrar para Registro para Registro do Manipulador [de Protocolo web][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span><span class="sxs-lookup"><span data-stu-id="6bb16-169">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="6bb16-170">Manifesto de Exemplo</span><span class="sxs-lookup"><span data-stu-id="6bb16-170">Example Manifest</span></span>

<span data-ttu-id="6bb16-171">Neste exemplo, um manifesto do aplicativo Web declara que o aplicativo deve ser registrado para lidar com os protocolos `web+jngl` e `web+jnglstore` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-171">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a><span data-ttu-id="6bb16-172">Manipulação de link de URL</span><span class="sxs-lookup"><span data-stu-id="6bb16-172">URL Link Handling</span></span>  

<span data-ttu-id="6bb16-173">Um localizador de recursos uniforme \(URL\) é um tipo de URI.</span><span class="sxs-lookup"><span data-stu-id="6bb16-173">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="6bb16-174">Crie uma experiência mais envolvente quando os Aplicativos Web Progressivos \(PWAs\) se registrarem como manipuladores para URIs https.</span><span class="sxs-lookup"><span data-stu-id="6bb16-174">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="6bb16-175">PWAs podem solicitar o lançamento quando URIs associados são ativados.</span><span class="sxs-lookup"><span data-stu-id="6bb16-175">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="6bb16-176">Por exemplo, se um usuário escolher um link para uma notícia de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6bb16-176">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="6bb16-177">Um PWA associado para exibir notícias é automaticamente lançado para manipular a ativação do link.</span><span class="sxs-lookup"><span data-stu-id="6bb16-177">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="6bb16-178">Esse recurso permite que você registre um PWA com o navegador usando o manifesto do aplicativo Web e declare que o navegador lida com links específicos.</span><span class="sxs-lookup"><span data-stu-id="6bb16-178">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="6bb16-179">Para registrar um PWA com o navegador, adicione o `url_handlers` membro opcional ao arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="6bb16-179">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="6bb16-180">O `url_handlers` membro é um que grupos as `object[]` origens de URIs que o aplicativo deseja manipular.</span><span class="sxs-lookup"><span data-stu-id="6bb16-180">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="6bb16-181">A manipulação de links é validada pelo navegador usando um arquivo JSON localizado `web-app-origin-association` na origem.</span><span class="sxs-lookup"><span data-stu-id="6bb16-181">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="6bb16-182">O arquivo de origem ajusta ainda mais os caminhos incluídos ou excluídos na origem.</span><span class="sxs-lookup"><span data-stu-id="6bb16-182">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="6bb16-183">Para obter instruções detalhadas sobre como testar o manipulador de URL, navegue até [PWAs como Manipuladores de URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]</span><span class="sxs-lookup"><span data-stu-id="6bb16-183">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="6bb16-184">Para visualizar a manipulação de link de URL no Microsoft Edge no Windows, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e ause a **Manipulação de URL do PWA da Área**de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-184">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL  Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="6bb16-185">Exemplo do url_handlers no manifesto</span><span class="sxs-lookup"><span data-stu-id="6bb16-185">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="6bb16-186">O trecho de código a seguir é um exemplo de manifesto do aplicativo Web com o `url_handlers` membro.</span><span class="sxs-lookup"><span data-stu-id="6bb16-186">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

<span data-ttu-id="6bb16-187">Um PWA corresponde a um URI para manipulação de URL se o URI corresponde a uma das cadeias de caracteres de origem e o navegador valida que a origem concorda em permitir que esse aplicativo manipular esse `url_handlers` URI.</span><span class="sxs-lookup"><span data-stu-id="6bb16-187">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="6bb16-188">O membro contém uma origem que abrange o escopo e também outras origens não `url_handlers` relacionadas do PWA solicitando.</span><span class="sxs-lookup"><span data-stu-id="6bb16-188">The `url_handlers` member contains an origin that encompasses the scope and also other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="6bb16-189">Não restringir URIs ao mesmo escopo ou domínio que o PWA solicitante permite usar nomes de domínio diferentes para o mesmo conteúdo, mas lidar com eles com o mesmo PWA.</span><span class="sxs-lookup"><span data-stu-id="6bb16-189">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="6bb16-190">Correspondência de caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="6bb16-190">Wildcard matching</span></span>  

<span data-ttu-id="6bb16-191">Use o caractere curinga \( `*` \) para corresponder a um ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="6bb16-191">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="6bb16-192">Um prefixo curinga é usado nas cadeias de caracteres de origem do `url_handlers` membro para corresponder a subdomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="6bb16-192">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="6bb16-193">O prefixo deve `*.` ser para esse uso.</span><span class="sxs-lookup"><span data-stu-id="6bb16-193">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="6bb16-194">O `https` esquema é assumido quando você usa um prefixo curinga.</span><span class="sxs-lookup"><span data-stu-id="6bb16-194">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="6bb16-195">Por exemplo, o `url_handlers` valor do membro é definido como corresponde e , mas não corresponde `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-195">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  
-->  

## <a name="run-on-os-login"></a><span data-ttu-id="6bb16-196">Executar logon no sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6bb16-196">Run On OS Login</span></span>  

<span data-ttu-id="6bb16-197">Esse recurso permite configurar seu aplicativo para iniciar automaticamente quando o usuário faz logor no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6bb16-197">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="6bb16-198">Várias classes de aplicativos aproveitam a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="6bb16-198">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="6bb16-199">As classes de aplicativos incluem email, chat, painel de monitoramento e aplicativos de exibição de dados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6bb16-199">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="6bb16-200">A funcionalidade permite que um usuário se envolva com os aplicativos assim que o usuário faz logor no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6bb16-200">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="6bb16-201">Esse recurso inicia automaticamente o PWA da mesma maneira que é iniciado manualmente.</span><span class="sxs-lookup"><span data-stu-id="6bb16-201">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="6bb16-202">**Executar no logon do sistema** operacional é um [recurso poderoso.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="6bb16-202">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="6bb16-203">Os usuários devem decidir se ativarão o recurso para o aplicativo Web instalado.</span><span class="sxs-lookup"><span data-stu-id="6bb16-203">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="6bb16-204">Ativar o logon do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6bb16-204">Turn on Run On OS Login</span></span>  

<span data-ttu-id="6bb16-205">Para ativar os **recursos de Logon** do [](#turn-on-experimental-features) sistema operacional Run On para o seu PWA, navegue até Ativar recursos experimentais e a ativar PWAs da Área de Trabalho **executados no logon do sistema operacional.**</span><span class="sxs-lookup"><span data-stu-id="6bb16-205">To turn on **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Ativar os PWAs da Área de Trabalho executados no experimento de logon do sistema operacional" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="6bb16-207">Ativar os **PWAs da Área de Trabalho executados no experimento de logon do sistema** operacional</span><span class="sxs-lookup"><span data-stu-id="6bb16-207">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="6bb16-208">Ativar o recurso para o aplicativo Web instalado</span><span class="sxs-lookup"><span data-stu-id="6bb16-208">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="6bb16-209">Para ativar o `Start app when you sign in` recurso de um PWA instalado,</span><span class="sxs-lookup"><span data-stu-id="6bb16-209">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="6bb16-210">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6bb16-210">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="6bb16-211">Navegue até `edge://apps` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-211">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="6bb16-212">Passe o mouse em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bb16-212">Hover on your app.</span></span>  
1.  <span data-ttu-id="6bb16-213">Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Iniciar aplicativo ao entrar**.</span><span class="sxs-lookup"><span data-stu-id="6bb16-213">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Use o menu contextual para ativar o aplicativo Iniciar ao entrar no recurso no Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="6bb16-215">Use o menu contextual para ativar o aplicativo **Iniciar ao entrar no** recurso no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6bb16-215">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="6bb16-216">Atalhos</span><span class="sxs-lookup"><span data-stu-id="6bb16-216">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="6bb16-217">é um novo membro do arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="6bb16-217">is a new member of the manifest file.</span></span>  <span data-ttu-id="6bb16-218">Ele permite definir links para partes, páginas da Web principais ou ações em seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6bb16-218">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="6bb16-219">O Microsoft Windows o integra como **Jumplists.**</span><span class="sxs-lookup"><span data-stu-id="6bb16-219">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="6bb16-220">**As listas de opções** definem menus pop-up que aparecem quando você em um dos seguintes elementos da interface do usuário e abre um menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="6bb16-220">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="6bb16-221">Um tile no Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="6bb16-221">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="6bb16-222">Um ícone na barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="6bb16-222">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="6bb16-223">Quando um usuário invoca um atalho, o usuário navega até o endereço especificado pelo `url` membro do atalho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-223">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Um exemplo de Listas de Saltos no Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="6bb16-225">Um exemplo de **Listas de Saltos** no Windows 10</span><span class="sxs-lookup"><span data-stu-id="6bb16-225">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="6bb16-226">Atalhos no arquivo De manifesto</span><span class="sxs-lookup"><span data-stu-id="6bb16-226">Shortcuts in the Manifest file</span></span>  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="6bb16-227">Propriedades de atalhos</span><span class="sxs-lookup"><span data-stu-id="6bb16-227">Properties of shortcuts</span></span>  

<span data-ttu-id="6bb16-228">As propriedades a seguir definem cada atalho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-228">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="6bb16-229">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6bb16-229">Property</span></span> | <span data-ttu-id="6bb16-230">Detalhes</span><span class="sxs-lookup"><span data-stu-id="6bb16-230">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="6bb16-231">Uma cadeia de caracteres que é exibida para o usuário em **Listas de saltos** ou no menu contextual.</span><span class="sxs-lookup"><span data-stu-id="6bb16-231">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="6bb16-232">Uma cadeia de caracteres exibida quando há espaço insuficiente para exibir o nome completo do atalho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-232">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="6bb16-233">Uma cadeia de caracteres que descreve a finalidade do atalho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-233">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="6bb16-234">Ele pode ser acessado por tecnologia assistida.</span><span class="sxs-lookup"><span data-stu-id="6bb16-234">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="6bb16-235">O URI no aplicativo Web que é aberto quando o atalho é ativado.</span><span class="sxs-lookup"><span data-stu-id="6bb16-235">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="6bb16-236">Um conjunto de ícones que representa o atalho.</span><span class="sxs-lookup"><span data-stu-id="6bb16-236">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="6bb16-237">Tratamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="6bb16-237">File Handling</span></span>  

<span data-ttu-id="6bb16-238">A capacidade de se registrar como um manipulador de tipo de arquivo está na fase de experimentação.</span><span class="sxs-lookup"><span data-stu-id="6bb16-238">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="6bb16-239">Você pode especificar os tipos de arquivo que seu aplicativo lida em uma entrada de manifesto.</span><span class="sxs-lookup"><span data-stu-id="6bb16-239">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="6bb16-240">Durante a instalação, o sistema operacional host do usuário registra seu aplicativo como um manipulador de arquivos para os tipos de arquivo listados.</span><span class="sxs-lookup"><span data-stu-id="6bb16-240">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="6bb16-241">Verifique a existência do recurso no código de inicialização de seus aplicativos e `launchQueue` que ele lida com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bb16-241">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="6bb16-242">Os navegadores baseados em Chromium estão testando e moldando esse recurso.</span><span class="sxs-lookup"><span data-stu-id="6bb16-242">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="6bb16-243">Para obter mais informações, incluindo exemplos de código, navegue até [Permitir que os aplicativos Web sejam manipuladores de arquivos][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="6bb16-243">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="6bb16-244">Para visualizar o tratamento de arquivos no Microsoft Edge para OSs da área de trabalho, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e a api **de manipulação de arquivos.**</span><span class="sxs-lookup"><span data-stu-id="6bb16-244">To preview file handling in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="6bb16-245">Fornecendo comentários sobre recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="6bb16-245">Providing feedback on experimental features</span></span>  

<span data-ttu-id="6bb16-246">Para fornecer comentários sobre experimentos de aplicativo Web do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6bb16-246">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="6bb16-247">Envie seus comentários **usando Configurações e Mais** \( `...` \) > Enviar comentários para a **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="6bb16-247">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="6bb16-248">Selecione `Alt` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="6bb16-248">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentários do seu PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="6bb16-250">Enviar comentários do seu PWA</span><span class="sxs-lookup"><span data-stu-id="6bb16-250">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Testes de origem | Desenvolvedor do Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registre-se no Registro do Manipulador de Protocolo do Aplicativo Web | Desenvolvedor da Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Manipuladores de protocolo baseados na Web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Recurso poderoso - Permissões | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs como manipuladores de URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que os aplicativos Web sejam manipuladores de arquivos | web.dev"  
