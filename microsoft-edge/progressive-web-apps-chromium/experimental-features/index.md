---
description: Os recursos experimentais mais recentes no Microsoft Edge para Aplicativos Web
title: Recursos experimentais | Aplicativos Web Progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 5ab2ab0a727d1eb52f61a01ea64b52bc1c09abce
ms.sourcegitcommit: f6a3ab7b13adf05dbe7a4bf65ee67c9b0f6fab95
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11482142"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="126ae-104">Recursos experimentais em PWAs (Progressive Web Apps)</span><span class="sxs-lookup"><span data-stu-id="126ae-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="126ae-105">O Microsoft Edge fornece acesso a recursos experimentais que ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="126ae-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="126ae-106">Para determinar se cada recurso está pronto e quando lançar cada um, teste e [forneça comentários.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="126ae-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="126ae-107">Os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, mas os recursos experimentais mais recentes estão disponíveis apenas no canal Canary do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="126ae-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="126ae-108">Ativar recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="126ae-108">Turn on experimental features</span></span>  

<span data-ttu-id="126ae-109">Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="126ae-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="126ae-110">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="126ae-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="126ae-111">Certifique-se de usar uma versão do Microsoft Edge que tenha o Experimento listado neste artigo.</span><span class="sxs-lookup"><span data-stu-id="126ae-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="126ae-112">Navegue até [Recursos Experimentais](#features-that-are-available-to-test).</span><span class="sxs-lookup"><span data-stu-id="126ae-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="126ae-113">Navegue até `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="126ae-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="126ae-114">Navegue até o experimento relevante.</span><span class="sxs-lookup"><span data-stu-id="126ae-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="126ae-115">Escolha o menu suspenso ao lado da descrição do experimento e escolha `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="126ae-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Escolha Habilitado para ativar um experimento" lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="126ae-117">Escolha **Habilitado para** ativar um experimento</span><span class="sxs-lookup"><span data-stu-id="126ae-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="126ae-118">Cada experimento geralmente tem um menu suspenso para escolher os seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="126ae-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="126ae-119">Se um recurso experimental não tiver uma entrada em **Experimentos,** serão fornecidas instruções para iniciar o Microsoft Edge com esse recurso usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="126ae-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="126ae-120">Reinicie o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="126ae-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="126ae-121">Avaliações de Origem</span><span class="sxs-lookup"><span data-stu-id="126ae-121">Origin Trials</span></span>  

<span data-ttu-id="126ae-122">O Microsoft Edge às vezes usa testes de origem para testar recursos para domínios ou sites específicos.</span><span class="sxs-lookup"><span data-stu-id="126ae-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="126ae-123">Talvez você queira usar uma avaliação de origem para seu site para aplicar um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="126ae-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="126ae-124">Se você for um proprietário de site, poderá se inscrever em uma avaliação de origem.</span><span class="sxs-lookup"><span data-stu-id="126ae-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="126ae-125">Uma avaliação de origem fornece recursos para uma porcentagem de usuários do Microsoft Edge que visitam seu site.</span><span class="sxs-lookup"><span data-stu-id="126ae-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="126ae-126">Para obter mais informações sobre as avaliação de origem, navegue até [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="126ae-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="126ae-127">Os recursos experimentais são constantemente atualizados e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="126ae-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="126ae-128">Para desativar um recurso experimental, navegue até [Ativar recursos experimentais,](#turn-on-experimental-features)navegue até o experimento e escolha `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="126ae-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="126ae-129">Recursos disponíveis para teste</span><span class="sxs-lookup"><span data-stu-id="126ae-129">Features that are available to test</span></span>  

<span data-ttu-id="126ae-130">A lista a seguir descreve os novos recursos experimentais do aplicativo Web que estão disponíveis para testar e validar no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="126ae-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="126ae-131">Recurso</span><span class="sxs-lookup"><span data-stu-id="126ae-131">Feature</span></span> | <span data-ttu-id="126ae-132">Versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="126ae-132">Microsoft Edge version</span></span> | <span data-ttu-id="126ae-133">Plataforma</span><span class="sxs-lookup"><span data-stu-id="126ae-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="126ae-134">Tratamento de protocolo URI</span><span class="sxs-lookup"><span data-stu-id="126ae-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="126ae-135">91 ou posterior</span><span class="sxs-lookup"><span data-stu-id="126ae-135">91 or later</span></span> | <span data-ttu-id="126ae-136">Windows</span><span class="sxs-lookup"><span data-stu-id="126ae-136">Windows</span></span> |    
| [<span data-ttu-id="126ae-137">Manipulação de link de URL</span><span class="sxs-lookup"><span data-stu-id="126ae-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="126ae-138">91 ou posterior</span><span class="sxs-lookup"><span data-stu-id="126ae-138">91 or later</span></span> | <span data-ttu-id="126ae-139">Windows</span><span class="sxs-lookup"><span data-stu-id="126ae-139">Windows</span></span>|
| [<span data-ttu-id="126ae-140">Sobreposição de Controles de Janela para Aplicativos de Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="126ae-140">Window Controls Overlay for Desktop Apps</span></span>](#window-controls-overlay-for-installed-desktop-web-apps) | <span data-ttu-id="126ae-141">91 ou posterior</span><span class="sxs-lookup"><span data-stu-id="126ae-141">91 or later</span></span> | <span data-ttu-id="126ae-142">Windows 10</span><span class="sxs-lookup"><span data-stu-id="126ae-142">Windows 10</span></span>|   
| [<span data-ttu-id="126ae-143">Executar no logon do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="126ae-143">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="126ae-144">88 ou posterior</span><span class="sxs-lookup"><span data-stu-id="126ae-144">88 or later</span></span> | <span data-ttu-id="126ae-145">Todas</span><span class="sxs-lookup"><span data-stu-id="126ae-145">All</span></span> |  
| [<span data-ttu-id="126ae-146">Atalhos</span><span class="sxs-lookup"><span data-stu-id="126ae-146">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="126ae-147">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="126ae-147">87 or later</span></span> | <span data-ttu-id="126ae-148">Todas</span><span class="sxs-lookup"><span data-stu-id="126ae-148">All</span></span> |  
| [<span data-ttu-id="126ae-149">Tratamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="126ae-149">File Handling</span></span>](#file-handling) | <span data-ttu-id="126ae-150">83 ou posterior</span><span class="sxs-lookup"><span data-stu-id="126ae-150">83 or later</span></span> | <span data-ttu-id="126ae-151">Toda a área de trabalho</span><span class="sxs-lookup"><span data-stu-id="126ae-151">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="126ae-152">Tratamento de protocolo URI</span><span class="sxs-lookup"><span data-stu-id="126ae-152">URI Protocol Handling</span></span>  

<span data-ttu-id="126ae-153">Um identificador de recurso uniforme \(URI\) pode ser usado para definir mais do que apenas links para páginas da Web e conteúdo da Web usando o protocolo HTTP ou FTP.</span><span class="sxs-lookup"><span data-stu-id="126ae-153">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="126ae-154">URIs podem ser usadas para descrever links para qualquer coisa que você codificar em um esquema.</span><span class="sxs-lookup"><span data-stu-id="126ae-154">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="126ae-155">Por exemplo, o protocolo é usado para descrever um link de email e o sistema operacional \(OS\) ou navegador decide qual página da Web ou `mailto://` aplicativo deve lidar com esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="126ae-155">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="126ae-156">Para obter mais informações sobre o suporte baseado em navegador existente, navegue até manipuladores de protocolo [baseados na Web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]</span><span class="sxs-lookup"><span data-stu-id="126ae-156">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="126ae-157">Esse recurso permite que você conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="126ae-157">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="126ae-158">Registrar seu PWA com o sistema operacional host usando o manifesto do seu aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="126ae-158">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="126ae-159">Declare que um PWA lida com um protocolo URI específico</span><span class="sxs-lookup"><span data-stu-id="126ae-159">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="126ae-160">Depois de registrar um PWA como um manipulador de protocolo, quando um usuário escolhe um hiperlink com um esquema específico, como ou de um navegador ou um aplicativo nativo, o PWA registrado é ativado pelo sistema operacional e recebe o `mailto://` `web+music://` URI.</span><span class="sxs-lookup"><span data-stu-id="126ae-160">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="126ae-161">Esse recurso exige que você atualize o manifesto do aplicativo Web para incluir uma matriz, na matriz que você `protocol_handlers` precisa especificar dois campos:</span><span class="sxs-lookup"><span data-stu-id="126ae-161">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="126ae-162">: O protocolo para lidar com a solicitação, por exemplo `mailto` ou `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="126ae-162">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="126ae-163">: O URI HTTPS no escopo do aplicativo que lida com o protocolo.</span><span class="sxs-lookup"><span data-stu-id="126ae-163">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="126ae-164">No futuro, o URI começando com o esquema de manipuladores de protocolo é planejado para substituir o `%s` token.</span><span class="sxs-lookup"><span data-stu-id="126ae-164">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="126ae-165">Atualize seu manifesto para dar suporte ao protocolo que você deseja registrar.</span><span class="sxs-lookup"><span data-stu-id="126ae-165">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="126ae-166">Depois de ativar esse recurso, o Microsoft Edge conclui as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="126ae-166">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="126ae-167">Detecta alterações no manifesto</span><span class="sxs-lookup"><span data-stu-id="126ae-167">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="126ae-168">Registra o aplicativo para o protocolo</span><span class="sxs-lookup"><span data-stu-id="126ae-168">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="126ae-169">Se mais de um aplicativo registrar um protocolo, o usuário será apresentado com um prompt.</span><span class="sxs-lookup"><span data-stu-id="126ae-169">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="126ae-170">O usuário escolhe o aplicativo apropriado na lista apresentada pelo sistema operacional ou navegador.</span><span class="sxs-lookup"><span data-stu-id="126ae-170">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="126ae-171">Para visualizar a manipulação de protocolo no Microsoft Edge no Windows, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e ause o Suporte a Manipuladores de Protocolo de **Desktop Web Apps.**</span><span class="sxs-lookup"><span data-stu-id="126ae-171">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop Web Apps support Protocol Handlers**.</span></span>  

<span data-ttu-id="126ae-172">Para obter mais informações sobre a avaliação de origem em execução para manipuladores de protocolo, navegue até Registrar para Registro para Registro do Manipulador [de Protocolo web][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span><span class="sxs-lookup"><span data-stu-id="126ae-172">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="126ae-173">Manifesto de Exemplo</span><span class="sxs-lookup"><span data-stu-id="126ae-173">Example Manifest</span></span>

<span data-ttu-id="126ae-174">Neste exemplo, um manifesto do aplicativo Web declara que o aplicativo deve ser registrado para lidar com os protocolos `web+jngl` e `web+jnglstore` .</span><span class="sxs-lookup"><span data-stu-id="126ae-174">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

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
 
## <a name="url-link-handling"></a><span data-ttu-id="126ae-175">Manipulação de link de URL</span><span class="sxs-lookup"><span data-stu-id="126ae-175">URL Link Handling</span></span>  

<span data-ttu-id="126ae-176">Um localizador de recursos uniforme \(URL\) é um tipo de URI.</span><span class="sxs-lookup"><span data-stu-id="126ae-176">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="126ae-177">Crie uma experiência mais envolvente quando os Aplicativos Web Progressivos \(PWAs\) se registrarem como manipuladores para URIs https.</span><span class="sxs-lookup"><span data-stu-id="126ae-177">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="126ae-178">PWAs podem solicitar o lançamento quando URIs associados são ativados.</span><span class="sxs-lookup"><span data-stu-id="126ae-178">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="126ae-179">Por exemplo, se um usuário escolher um link para uma notícia de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="126ae-179">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="126ae-180">Um PWA associado para exibir notícias é automaticamente lançado para manipular a ativação do link.</span><span class="sxs-lookup"><span data-stu-id="126ae-180">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="126ae-181">Esse recurso permite que você registre um PWA com o navegador usando o manifesto do aplicativo Web e declare que o navegador lida com links específicos.</span><span class="sxs-lookup"><span data-stu-id="126ae-181">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="126ae-182">Para registrar um PWA com o navegador, adicione o `url_handlers` membro opcional ao arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="126ae-182">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="126ae-183">O `url_handlers` membro é um que grupos as `object[]` origens de URIs que o aplicativo deseja manipular.</span><span class="sxs-lookup"><span data-stu-id="126ae-183">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="126ae-184">A manipulação de links é validada pelo navegador usando um arquivo JSON localizado `web-app-origin-association` na origem.</span><span class="sxs-lookup"><span data-stu-id="126ae-184">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="126ae-185">O arquivo de origem ajusta ainda mais os caminhos incluídos ou excluídos na origem.</span><span class="sxs-lookup"><span data-stu-id="126ae-185">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="126ae-186">Para obter instruções detalhadas sobre como testar o manipulador de URL, navegue até [PWAs como Manipuladores de URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]</span><span class="sxs-lookup"><span data-stu-id="126ae-186">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="126ae-187">Para visualizar a manipulação de link de URL no Microsoft Edge no Windows, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e ause a **Manipulação de URL do PWA da Área**de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-187">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL  Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="126ae-188">Exemplo do url_handlers no manifesto</span><span class="sxs-lookup"><span data-stu-id="126ae-188">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="126ae-189">O trecho de código a seguir é um exemplo de manifesto do aplicativo Web com o `url_handlers` membro.</span><span class="sxs-lookup"><span data-stu-id="126ae-189">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

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

<span data-ttu-id="126ae-190">Um PWA corresponde a um URI para manipulação de URL se o URI corresponde a uma das cadeias de caracteres de origem e o navegador valida que a origem concorda em permitir que esse aplicativo manipular esse `url_handlers` URI.</span><span class="sxs-lookup"><span data-stu-id="126ae-190">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="126ae-191">O membro contém uma origem que abrange o escopo e outras origens não `url_handlers` relacionadas do PWA solicitando.</span><span class="sxs-lookup"><span data-stu-id="126ae-191">The `url_handlers` member contains an origin that encompasses the scope and other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="126ae-192">Não restringir URIs ao mesmo escopo ou domínio que o PWA solicitante permite usar nomes de domínio diferentes para o mesmo conteúdo, mas lidar com eles com o mesmo PWA.</span><span class="sxs-lookup"><span data-stu-id="126ae-192">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="126ae-193">Correspondência de caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="126ae-193">Wildcard matching</span></span>  

<span data-ttu-id="126ae-194">Use o caractere curinga \( `*` \) para corresponder a um ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="126ae-194">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="126ae-195">Um prefixo curinga é usado nas cadeias de caracteres de origem do `url_handlers` membro para corresponder a subdomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="126ae-195">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="126ae-196">O prefixo deve `*.` ser para esse uso.</span><span class="sxs-lookup"><span data-stu-id="126ae-196">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="126ae-197">O `https` esquema é assumido quando você usa um prefixo curinga.</span><span class="sxs-lookup"><span data-stu-id="126ae-197">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="126ae-198">Por exemplo, o `url_handlers` valor do membro é definido como corresponde e , mas não corresponde `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="126ae-198">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a><span data-ttu-id="126ae-199">Sobreposição de Controles de Janela para aplicativos Web da área de trabalho instalados</span><span class="sxs-lookup"><span data-stu-id="126ae-199">Window Controls Overlay for installed desktop web apps</span></span>  

<span data-ttu-id="126ae-200">Para criar uma barra de título imersiva como um aplicativo nativo \*\*\*\* para seu aplicativo Web instalado na área de trabalho, o recurso Sobreposição de Controles de Janela conclui as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="126ae-200">To create an immersive title bar like a native app for your desktop installed web app, the **Window Controls Overlay** feature completes the following actions.</span></span>  
    
1.  <span data-ttu-id="126ae-201">Remove a barra de título reservada do sistema.</span><span class="sxs-lookup"><span data-stu-id="126ae-201">Removes the system reserved title bar.</span></span>  <span data-ttu-id="126ae-202">Geralmente, ela abrange a largura do quadro do cliente.</span><span class="sxs-lookup"><span data-stu-id="126ae-202">It usually spans the width of the client frame.</span></span>  
1.  <span data-ttu-id="126ae-203">Substitui-o por uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="126ae-203">Replaces it with an overlay.</span></span>  <span data-ttu-id="126ae-204">Ele contém apenas os controles críticos de janela necessários para que um usuário controle a própria janela.</span><span class="sxs-lookup"><span data-stu-id="126ae-204">It contains just the critical system required window controls necessary for a user to control the window itself.</span></span>  
    
<span data-ttu-id="126ae-205">Depois que ele fornece uma sobreposição, toda a área do cliente Web estará disponível para você usar.</span><span class="sxs-lookup"><span data-stu-id="126ae-205">After it provides an overlay, the entire web client area is available for you to use.</span></span>  <span data-ttu-id="126ae-206">Esse recurso inclui uma atualização de manifesto.</span><span class="sxs-lookup"><span data-stu-id="126ae-206">This feature includes a manifest update.</span></span>  <span data-ttu-id="126ae-207">Ele fornece maneiras de determinar o tamanho e a posição da sobreposição para ajudá-lo a organizar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="126ae-207">It provides ways for you to determine the size and position of the overlay to help you arrange content.</span></span>  

<span data-ttu-id="126ae-208">Para visualizar as Sobreposições de Controles de Janela no [](#turn-on-experimental-features) Microsoft Edge para Windows 10, navegue até Ativar recursos experimentais e navegue até **Desktop PWA Window Controls Overlay**.</span><span class="sxs-lookup"><span data-stu-id="126ae-208">To preview the Window Controls Overlays in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.</span></span>   

### <a name="examples-of-title-bar-area-customization"></a><span data-ttu-id="126ae-209">Exemplos de personalização da área da barra de títulos</span><span class="sxs-lookup"><span data-stu-id="126ae-209">Examples of title bar area customization</span></span>  

<span data-ttu-id="126ae-210">Esse recurso se baseia na capacidade em aplicativos nativos de personalizar a barra de título.</span><span class="sxs-lookup"><span data-stu-id="126ae-210">This feature is based on the ability in native apps to customize the title bar.</span></span>  <span data-ttu-id="126ae-211">Você pode personalizar uma barra de título para ações ou notificações importantes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="126ae-211">You may customize a title bar for important app actions or notifications.</span></span>  <span data-ttu-id="126ae-212">Revise os exemplos a seguir para o Microsoft Visual Studio Code e o Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="126ae-212">Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.</span></span>  

#### <a name="visual-studio-code"></a><span data-ttu-id="126ae-213">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="126ae-213">Visual Studio Code</span></span>  

<span data-ttu-id="126ae-214">O Microsoft Visual Studio Code é um editor popular criado em Eletrônica que acompanha várias plataformas de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-214">Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.</span></span>  

<span data-ttu-id="126ae-215">O exemplo a seguir exibe como Visual Studio Code usa a barra de título para maximizar a propriedade de tela disponível para incluir o nome do arquivo atual e a estrutura de menu de nível superior na barra de título.</span><span class="sxs-lookup"><span data-stu-id="126ae-215">The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.</span></span>  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Um exemplo da barra de título no Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   <span data-ttu-id="126ae-217">Um exemplo da barra de título no Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="126ae-217">An example of the title bar in Visual Studio Code</span></span>  
:::image-end:::  

#### <a name="microsoft-teams"></a><span data-ttu-id="126ae-218">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="126ae-218">Microsoft Teams</span></span>  

<span data-ttu-id="126ae-219">Ferramenta de colaboração e comunicação do local de trabalho O Microsoft Teams também é criado com o Eletrônica e está disponível em várias plataformas de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-219">Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.</span></span>  <span data-ttu-id="126ae-220">No exemplo a seguir, o Microsoft Teams exibe e botões de navegação, uma caixa de pesquisa `back` `forward` e controles de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="126ae-220">In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.</span></span>  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Um exemplo da barra de título no Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   <span data-ttu-id="126ae-222">Um exemplo da barra de título no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="126ae-222">An example of the title bar in Microsoft Teams</span></span>  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a><span data-ttu-id="126ae-223">Controles de janela de sobreposição em uma janela sem quadros</span><span class="sxs-lookup"><span data-stu-id="126ae-223">Overlay Window Controls on a Frameless Window</span></span>  

<span data-ttu-id="126ae-224">Para maximizar a área acessível para conteúdo da Web, o navegador cria uma janela sem quadros.</span><span class="sxs-lookup"><span data-stu-id="126ae-224">To maximize the addressable area for web content, the browser creates a frameless window.</span></span>  <span data-ttu-id="126ae-225">Uma janela sem quadros remove toda a interface do usuário do navegador, exceto os controles de janela fornecidos como uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="126ae-225">A frameless window removes all browser UI, except for the window controls provided as an overlay.</span></span>  <span data-ttu-id="126ae-226">A sobreposição de controles de janela permite que os usuários ainda minimizem, maximizem, restaurem e fechem o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="126ae-226">The window controls overlay allows users to still minimize, maximize, restore, and close the app.</span></span>  <span data-ttu-id="126ae-227">Ele também fornece acesso a controles relevantes do navegador usando o menu do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-227">It also provides access to relevant browser controls using the web app menu.</span></span>  <span data-ttu-id="126ae-228">Para navegadores baseados em Chromium, a sobreposição inclui os seguintes controles.</span><span class="sxs-lookup"><span data-stu-id="126ae-228">For Chromium-based browsers, the overlay includes the following controls.</span></span>  

*   <span data-ttu-id="126ae-229">Uma região arrastável com a mesma largura e altura de cada um dos botões de controle de janela</span><span class="sxs-lookup"><span data-stu-id="126ae-229">A draggable region the same width and height of each of the window control buttons</span></span>  
*   <span data-ttu-id="126ae-230">O **botão Configurações e** mais \(...\)</span><span class="sxs-lookup"><span data-stu-id="126ae-230">The **Settings and more** \(...\) button</span></span>  
*   <span data-ttu-id="126ae-231">Os botões de controle de janela minimizam, maximizam, restauram e fecham</span><span class="sxs-lookup"><span data-stu-id="126ae-231">The window control buttons minimize, maximize, restore, and close</span></span>  
    
<span data-ttu-id="126ae-232">Além dos controles listados anteriormente, a interface do usuário exibida na sobreposição é resized dinamicamente nos seguintes cenários.</span><span class="sxs-lookup"><span data-stu-id="126ae-232">Besides the previously listed controls, the UI displayed in the overlay is dynamically resized in the following scenarios.</span></span>  

*   <span data-ttu-id="126ae-233">Quando um aplicativo Web instalado é lançado, a origem da página \*\*\*\* da Web é exibida à esquerda do menu Configurações e mais \(...\) por alguns segundos e desaparece.</span><span class="sxs-lookup"><span data-stu-id="126ae-233">When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.</span></span>  
*   <span data-ttu-id="126ae-234">Se um usuário interagir com \*\*\*\* uma extensão usando o menu Configurações e mais \(...\), o ícone da extensão será exibido na sobreposição à esquerda do menu de três pontos.</span><span class="sxs-lookup"><span data-stu-id="126ae-234">If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.</span></span>  <span data-ttu-id="126ae-235">Depois de sair de qualquer caixa de diálogo de extensão, o ícone será removido da sobreposição.</span><span class="sxs-lookup"><span data-stu-id="126ae-235">After you exit any extension dialog, the icon is removed from the overlay.</span></span>  
    
| <span data-ttu-id="126ae-236">Direção do idioma</span><span class="sxs-lookup"><span data-stu-id="126ae-236">Language direction</span></span> | <span data-ttu-id="126ae-237">Local de sobreposição</span><span class="sxs-lookup"><span data-stu-id="126ae-237">Overlay location</span></span> | <span data-ttu-id="126ae-238">Detalhes</span><span class="sxs-lookup"><span data-stu-id="126ae-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="126ae-239">Da esquerda para a direita \(LTR\)</span><span class="sxs-lookup"><span data-stu-id="126ae-239">Left-to-right \(LTR\)</span></span> | <span data-ttu-id="126ae-240">Superior esquerdo da área do cliente</span><span class="sxs-lookup"><span data-stu-id="126ae-240">Upper left of the client area</span></span> | <span data-ttu-id="126ae-241">Os controles são invertida</span><span class="sxs-lookup"><span data-stu-id="126ae-241">The controls are flipped</span></span> |  
| <span data-ttu-id="126ae-242">Da direita para a esquerda \(RTL\)</span><span class="sxs-lookup"><span data-stu-id="126ae-242">Right-to-left \(RTL\)</span></span> | <span data-ttu-id="126ae-243">Canto superior direito da área do cliente</span><span class="sxs-lookup"><span data-stu-id="126ae-243">Upper right corner of the client area</span></span> |  |  

> [!IMPORTANT]
> <span data-ttu-id="126ae-244">A sobreposição está sempre sobre o índice Z do conteúdo da Web e aceita todas as entradas do usuário sem fluí-la para o conteúdo da Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-244">The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.</span></span>  

### <a name="working-around-the-window-controls-overlay"></a><span data-ttu-id="126ae-245">Trabalhando ao redor da Sobreposição de Controles de Janela</span><span class="sxs-lookup"><span data-stu-id="126ae-245">Working around the Window Controls Overlay</span></span>  

<span data-ttu-id="126ae-246">O conteúdo da Web deve estar ciente da área reservada para a sobreposição de controles.</span><span class="sxs-lookup"><span data-stu-id="126ae-246">Your web content must be aware of the reserved area for the controls overlay.</span></span>  <span data-ttu-id="126ae-247">Verifique se a área reservada não espera interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="126ae-247">Ensure the reserved area doesn't expect user interaction.</span></span>  <span data-ttu-id="126ae-248">Consulte o navegador para o retângulo delimitador e a visibilidade da sobreposição de controles.</span><span class="sxs-lookup"><span data-stu-id="126ae-248">Query the browser for the bounding rectangle and visibility of the controls overlay.</span></span>  <span data-ttu-id="126ae-249">As informações são fornecidas por meio de APIs JavaScript e variáveis de ambiente CSS.</span><span class="sxs-lookup"><span data-stu-id="126ae-249">The information is provided to you through JavaScript APIs and CSS environment variables.</span></span>  

#### <a name="javascript-apis"></a><span data-ttu-id="126ae-250">JavaScript APIs</span><span class="sxs-lookup"><span data-stu-id="126ae-250">JavaScript APIs</span></span>  

<span data-ttu-id="126ae-251">Um novo objeto na propriedade permite consultar o `windowControlsOverlay` `window.navigator` retângulo delimitante da sobreposição de controles.</span><span class="sxs-lookup"><span data-stu-id="126ae-251">A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.</span></span>  

<span data-ttu-id="126ae-252">O `windowControlsOverlay` objeto tem os dois objetos a seguir.</span><span class="sxs-lookup"><span data-stu-id="126ae-252">The `windowControlsOverlay` object has the following two objects.</span></span>  

*   `getBoundingClientRect()` <span data-ttu-id="126ae-253">retorna um `DOMRect` objeto.</span><span class="sxs-lookup"><span data-stu-id="126ae-253">returns a `DOMRect` object.</span></span>  <span data-ttu-id="126ae-254">O `DOMRect` objeto representa a área sob a sobreposição de controles da janela.</span><span class="sxs-lookup"><span data-stu-id="126ae-254">The `DOMRect` object represents the area under the window controls overlay.</span></span>  
*   `visible` <span data-ttu-id="126ae-255">é um booleano que indica que a sobreposição de controles é renderizada e exibida.</span><span class="sxs-lookup"><span data-stu-id="126ae-255">is a boolean that indicates that the controls overlay is rendered and displayed.</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="126ae-256">Por motivos de privacidade, `windowControlsOverlay` o não está acessível a elementos no `iframe` conteúdo da Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-256">For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.</span></span>  

<span data-ttu-id="126ae-257">Sempre que a sobreposição é ressada, um evento é executado no objeto para notificar o cliente para `geometrychange` `navigator.windowControlsOverlay` recalcular o layout de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="126ae-257">Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.</span></span>  <span data-ttu-id="126ae-258">O layout de conteúdo recalculado baseia-se no novo retângulo delimitante da sobreposição.</span><span class="sxs-lookup"><span data-stu-id="126ae-258">The recalculated content layout is based on the new bounding rectangle of the overlay.</span></span>  

#### <a name="css-environment-variables"></a><span data-ttu-id="126ae-259">Variáveis de ambiente CSS</span><span class="sxs-lookup"><span data-stu-id="126ae-259">CSS Environment Variables</span></span>  

<span data-ttu-id="126ae-260">Além da API JavaScript, você pode usar CSS para consultar o retângulo delimitante da sobreposição de controles.</span><span class="sxs-lookup"><span data-stu-id="126ae-260">Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.</span></span>  <span data-ttu-id="126ae-261">Use as quatro novas variáveis de ambiente CSS a seguir para realizar a consulta.</span><span class="sxs-lookup"><span data-stu-id="126ae-261">Use the following four new CSS environment variables to accomplish to query.</span></span>  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a><span data-ttu-id="126ae-262">Definir regiões arrastáveis no conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="126ae-262">Define Draggable Regions in Web Content</span></span>  

<span data-ttu-id="126ae-263">Os usuários esperam pegar e arrastar a região superior de uma janela.</span><span class="sxs-lookup"><span data-stu-id="126ae-263">Users expect to grab and drag the upper region of a window.</span></span>  <span data-ttu-id="126ae-264">Para acomodar a expectativa, declare partes específicas do conteúdo da Web como arrastáveis.</span><span class="sxs-lookup"><span data-stu-id="126ae-264">To accommodate the expectation, declare specific parts of the web content as draggable.</span></span>  
<span data-ttu-id="126ae-265">Para especificar que um elemento é arrastável, use a propriedade CSS proprietária do `-webkit-app-region` WebKit.</span><span class="sxs-lookup"><span data-stu-id="126ae-265">To specify an element is draggable, use the WebKit-proprietary `-webkit-app-region` CSS property.</span></span>  <span data-ttu-id="126ae-266">O grupo de trabalho CSS continua os esforços para padronizar a `app-region` propriedade.</span><span class="sxs-lookup"><span data-stu-id="126ae-266">The CSS working group continues efforts to standardize the `app-region` property.</span></span>  

### <a name="custom-title-bar-example"></a><span data-ttu-id="126ae-267">Exemplo da barra de título personalizada</span><span class="sxs-lookup"><span data-stu-id="126ae-267">Custom title bar example</span></span>  

<span data-ttu-id="126ae-268">O exemplo a seguir exibe como os novos recursos criam um aplicativo Web com uma barra de título personalizada.</span><span class="sxs-lookup"><span data-stu-id="126ae-268">The following example displays how the new features create a web app with a custom title bar.</span></span>  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Exemplo de uma barra de título personalizada no Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   <span data-ttu-id="126ae-270">Exemplo de uma barra de título personalizada no Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="126ae-270">Example of a custom title bar in Microsoft Teams</span></span>  
:::image-end:::  

#### <a name="manifestwebmanifest"></a><span data-ttu-id="126ae-271">manifest.webmanifest</span><span class="sxs-lookup"><span data-stu-id="126ae-271">manifest.webmanifest</span></span>  

<span data-ttu-id="126ae-272">No manifesto, de definir `display_override` matriz como  `window-controls-overlay` .</span><span class="sxs-lookup"><span data-stu-id="126ae-272">In the manifest, set `display_override` array to  `window-controls-overlay`.</span></span>  <span data-ttu-id="126ae-273">De definir `theme_color` a para sua escolha de cor para a barra de título.</span><span class="sxs-lookup"><span data-stu-id="126ae-273">Set the `theme_color` to your choice of color for the title bar.</span></span>  <span data-ttu-id="126ae-274">De definir o modo de exibição como um fallback apropriado para quando ou `display_override` `window-controls-overlay` não for suportado.</span><span class="sxs-lookup"><span data-stu-id="126ae-274">Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.</span></span>  

<span data-ttu-id="126ae-275">O trecho de código a seguir inclui as atualizações de manifesto recomendadas.</span><span class="sxs-lookup"><span data-stu-id="126ae-275">The following code snippet includes the recommended manifest updates.</span></span>  

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

### <a name="indexhtml"></a><span data-ttu-id="126ae-276">index.html</span><span class="sxs-lookup"><span data-stu-id="126ae-276">index.html</span></span>  

<span data-ttu-id="126ae-277">As IDs a seguir representam as duas principais regiões da página da Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-277">The following IDs represent the two main regions of the webpage.</span></span>  

*   `titleBarContainer`  
*   `mainContent`  
    
<span data-ttu-id="126ae-278">O `div` elemento com a `titleBar` ID é definido como e o elemento filho da caixa de pesquisa `draggable` é definido como `input` `nonDraggable` .</span><span class="sxs-lookup"><span data-stu-id="126ae-278">The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.</span></span>  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

<span data-ttu-id="126ae-279">No elemento `div` com a ID, o com a ID representa a parte visível da área da barra de `titleBarContainer` `div` `titleBar` título.</span><span class="sxs-lookup"><span data-stu-id="126ae-279">In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.</span></span>  

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
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a><span data-ttu-id="126ae-280">style.css</span><span class="sxs-lookup"><span data-stu-id="126ae-280">style.css</span></span>  

<span data-ttu-id="126ae-281">As regiões arrastáveis e não arrastáveis são definidas usando `-webkit-app-region: drag` e `-webkit-app-region: no-drag` .</span><span class="sxs-lookup"><span data-stu-id="126ae-281">The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.</span></span>  

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

<span data-ttu-id="126ae-282">Para o `body` elemento, as margens são definidas para garantir que a barra de título atinja `0` as bordas da janela.</span><span class="sxs-lookup"><span data-stu-id="126ae-282">For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.</span></span>  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

<span data-ttu-id="126ae-283">A ID usa e define como , que anexa o contêiner à `titleBarContainer` parte superior da página da `position: absolute` `top` `titlebar-area-inset-top` Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-283">The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.</span></span>  <span data-ttu-id="126ae-284">O será definido como e retornará para se a sobreposição de controles de janela `bottom` não estiver `titlebar-area-inset-bottom` `100% - var(--fallback-title-bar-height)` visível.</span><span class="sxs-lookup"><span data-stu-id="126ae-284">The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.</span></span>  <span data-ttu-id="126ae-285">A cor de plano de fundo `titleBarContainer` da ID é a mesma que `theme_color` a .</span><span class="sxs-lookup"><span data-stu-id="126ae-285">The background color of the `titleBarContainer` ID is the same as the `theme_color`.</span></span>  <span data-ttu-id="126ae-286">A largura é definida como , para que o elemento preencha a largura da página da Web e flua sob a sobreposição quando estiver visível para uma `100%` `div` aparência contígua.</span><span class="sxs-lookup"><span data-stu-id="126ae-286">The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.</span></span>  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

<span data-ttu-id="126ae-287">A `titleBar` ID também usa `position: absolute` e a anexa à parte superior da `top: titlebar-area-inset-top` janela.</span><span class="sxs-lookup"><span data-stu-id="126ae-287">The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.</span></span>  <span data-ttu-id="126ae-288">Por padrão, ele consome a largura total da janela.</span><span class="sxs-lookup"><span data-stu-id="126ae-288">By default, it consumes the full width of the window.</span></span>  <span data-ttu-id="126ae-289">As `left` bordas e são `right` definidas como e, respectivamente, ambas voltam para quando os valores não são `titlebar-area-inset-left` `titlebar-area-inset-right` `0` definidos.</span><span class="sxs-lookup"><span data-stu-id="126ae-289">The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.</span></span>  <span data-ttu-id="126ae-290">Ele também define para impedir qualquer tentativa de arrastar a janela consumida, em vez disso, `user-select: none` realça o texto no `div` elemento.</span><span class="sxs-lookup"><span data-stu-id="126ae-290">It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.</span></span>  

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

<span data-ttu-id="126ae-291">O contêiner para a ID também é fixo e anexado `mainContent` à parte inferior da página da `position: absolute` Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-291">The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.</span></span>  <span data-ttu-id="126ae-292">O `height` é definido como e recua para preencher o espaço restante abaixo da barra de `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` título.</span><span class="sxs-lookup"><span data-stu-id="126ae-292">The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.</span></span>  <span data-ttu-id="126ae-293">Ele define `overflow-y: scroll` para permitir que o conteúdo role verticalmente no contêiner.</span><span class="sxs-lookup"><span data-stu-id="126ae-293">It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.</span></span>  

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

<span data-ttu-id="126ae-294">Para os casos em que o navegador não dá suporte à sobreposição de controles de janela, uma variável CSS é adicionada para definir uma altura padrão para a barra de título.</span><span class="sxs-lookup"><span data-stu-id="126ae-294">For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.</span></span>  <span data-ttu-id="126ae-295">Os limites das IDs e são definidos inicialmente para preencher toda a área do cliente, e você não precisa alterá-la se a sobreposição não for `titleBarContainer` `mainContent` suportada.</span><span class="sxs-lookup"><span data-stu-id="126ae-295">The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.</span></span>  

<span data-ttu-id="126ae-296">O trecho de código a seguir inclui todas as atualizações CSS recomendadas.</span><span class="sxs-lookup"><span data-stu-id="126ae-296">The following code snippet includes all the recommended CSS updates.</span></span>

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

## <a name="run-on-os-login"></a><span data-ttu-id="126ae-297">Executar logon no sistema operacional</span><span class="sxs-lookup"><span data-stu-id="126ae-297">Run On OS Login</span></span>  

<span data-ttu-id="126ae-298">Esse recurso permite configurar seu aplicativo para iniciar automaticamente quando o usuário faz logor no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="126ae-298">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="126ae-299">Várias classes de aplicativos aproveitam a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="126ae-299">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="126ae-300">As classes de aplicativos incluem email, chat, painel de monitoramento e aplicativos de exibição de dados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="126ae-300">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="126ae-301">A funcionalidade permite que um usuário se envolva com os aplicativos assim que o usuário faz logor no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="126ae-301">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="126ae-302">Esse recurso inicia automaticamente o PWA da mesma maneira que é iniciado manualmente.</span><span class="sxs-lookup"><span data-stu-id="126ae-302">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="126ae-303">**Executar no logon do sistema** operacional é um [recurso poderoso.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="126ae-303">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="126ae-304">Os usuários devem decidir se ativarão o recurso para o aplicativo Web instalado.</span><span class="sxs-lookup"><span data-stu-id="126ae-304">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="126ae-305">Ativar o logon do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="126ae-305">Turn on Run On OS Login</span></span>  

<span data-ttu-id="126ae-306">Para visualizar os **recursos de Logon** do [](#turn-on-experimental-features) sistema operacional Run On para o PWA, navegue até Ativar recursos experimentais e a ativar PWAs da Área de Trabalho **executados no logon do sistema operacional**.</span><span class="sxs-lookup"><span data-stu-id="126ae-306">To preview the **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Ativar os PWAs da Área de Trabalho executados no experimento de logon do sistema operacional" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="126ae-308">Ativar os **PWAs da Área de Trabalho executados no experimento de logon do sistema** operacional</span><span class="sxs-lookup"><span data-stu-id="126ae-308">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="126ae-309">Ativar o recurso para o aplicativo Web instalado</span><span class="sxs-lookup"><span data-stu-id="126ae-309">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="126ae-310">Para ativar o `Start app when you sign in` recurso de um PWA instalado,</span><span class="sxs-lookup"><span data-stu-id="126ae-310">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="126ae-311">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="126ae-311">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="126ae-312">Navegue até `edge://apps` .</span><span class="sxs-lookup"><span data-stu-id="126ae-312">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="126ae-313">Passe o mouse em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="126ae-313">Hover on your app.</span></span>  
1.  <span data-ttu-id="126ae-314">Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Iniciar aplicativo ao entrar**.</span><span class="sxs-lookup"><span data-stu-id="126ae-314">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Use o menu contextual para ativar o aplicativo Iniciar ao entrar no recurso no Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="126ae-316">Use o menu contextual para ativar o aplicativo **Iniciar ao entrar no** recurso no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="126ae-316">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="126ae-317">Atalhos</span><span class="sxs-lookup"><span data-stu-id="126ae-317">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="126ae-318">é um novo membro do arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="126ae-318">is a new member of the manifest file.</span></span>  <span data-ttu-id="126ae-319">Ele permite definir links para partes, páginas da Web principais ou ações em seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="126ae-319">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="126ae-320">O Microsoft Windows o integra como **Jumplists.**</span><span class="sxs-lookup"><span data-stu-id="126ae-320">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="126ae-321">**As listas de opções** definem menus pop-up que aparecem quando você em um dos seguintes elementos da interface do usuário e abre um menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="126ae-321">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="126ae-322">Um tile no Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="126ae-322">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="126ae-323">Um ícone na barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="126ae-323">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="126ae-324">Quando um usuário invoca um atalho, o usuário navega até o endereço especificado pelo `url` membro do atalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-324">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Um exemplo de Listas de Saltos no Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="126ae-326">Um exemplo de **Listas de Saltos** no Windows 10</span><span class="sxs-lookup"><span data-stu-id="126ae-326">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="126ae-327">Atalhos no arquivo De manifesto</span><span class="sxs-lookup"><span data-stu-id="126ae-327">Shortcuts in the Manifest file</span></span>  

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

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="126ae-328">Propriedades de atalhos</span><span class="sxs-lookup"><span data-stu-id="126ae-328">Properties of shortcuts</span></span>  

<span data-ttu-id="126ae-329">As propriedades a seguir definem cada atalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-329">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="126ae-330">Propriedade</span><span class="sxs-lookup"><span data-stu-id="126ae-330">Property</span></span> | <span data-ttu-id="126ae-331">Detalhes</span><span class="sxs-lookup"><span data-stu-id="126ae-331">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="126ae-332">Uma cadeia de caracteres que é exibida para o usuário em **Listas de saltos** ou no menu contextual.</span><span class="sxs-lookup"><span data-stu-id="126ae-332">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="126ae-333">Uma cadeia de caracteres exibida quando há espaço insuficiente para exibir o nome completo do atalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-333">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="126ae-334">Uma cadeia de caracteres que descreve a finalidade do atalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-334">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="126ae-335">Ele pode ser acessado por tecnologia assistida.</span><span class="sxs-lookup"><span data-stu-id="126ae-335">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="126ae-336">O URI no aplicativo Web que é aberto quando o atalho é ativado.</span><span class="sxs-lookup"><span data-stu-id="126ae-336">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="126ae-337">Um conjunto de ícones que representa o atalho.</span><span class="sxs-lookup"><span data-stu-id="126ae-337">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="126ae-338">Tratamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="126ae-338">File Handling</span></span>  

<span data-ttu-id="126ae-339">A capacidade de se registrar como um manipulador de tipo de arquivo está na fase de experimentação.</span><span class="sxs-lookup"><span data-stu-id="126ae-339">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="126ae-340">Você pode especificar os tipos de arquivo que seu aplicativo lida em uma entrada de manifesto.</span><span class="sxs-lookup"><span data-stu-id="126ae-340">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="126ae-341">Durante a instalação, o sistema operacional host do usuário registra seu aplicativo como um manipulador de arquivos para os tipos de arquivo listados.</span><span class="sxs-lookup"><span data-stu-id="126ae-341">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="126ae-342">Verifique a existência do recurso no código de inicialização de seus aplicativos e `launchQueue` que ele lida com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="126ae-342">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="126ae-343">Os navegadores baseados em Chromium estão testando e moldando esse recurso.</span><span class="sxs-lookup"><span data-stu-id="126ae-343">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="126ae-344">Para obter mais informações, incluindo exemplos de código, navegue até [Permitir que os aplicativos Web sejam manipuladores de arquivos][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="126ae-344">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="126ae-345">Para visualizar o tratamento de arquivos no Microsoft Edge para Windows 10, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e a api **de manipulação de arquivos.**</span><span class="sxs-lookup"><span data-stu-id="126ae-345">To preview file handling in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="126ae-346">Fornecendo comentários sobre recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="126ae-346">Providing feedback on experimental features</span></span>  

<span data-ttu-id="126ae-347">Para fornecer comentários sobre experimentos de aplicativo Web do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="126ae-347">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="126ae-348">Envie seus comentários **usando Configurações e Mais** \( `...` \) > Enviar comentários para a **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="126ae-348">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="126ae-349">Selecione `Alt` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="126ae-349">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentários do seu PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="126ae-351">Enviar comentários do seu PWA</span><span class="sxs-lookup"><span data-stu-id="126ae-351">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Testes de origem | Desenvolvedor do Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registre-se no Registro do Manipulador de Protocolo do Aplicativo Web | Desenvolvedor da Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Manipuladores de protocolo baseados na Web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Recurso poderoso - Permissões | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs como manipuladores de URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que os aplicativos Web sejam manipuladores de arquivos | web.dev"  
