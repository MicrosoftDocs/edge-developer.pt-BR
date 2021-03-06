---
ms.assetid: ''
description: Experimente com segurança por um período de tempo fixo e forneça comentários sobre os novos recursos da plataforma.
title: Avaliações de Origem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, css, avaliação de origem, desenvolvedor
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397542"
---
# <a name="use-origin-trials-in-microsoft-edge"></a><span data-ttu-id="960d6-104">Usar testes de origem no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="960d6-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="960d6-105">Os desenvolvedores podem usar testes de origem para experimentar APIs experimentais em sites ao vivo por um período limitado de tempo.</span><span class="sxs-lookup"><span data-stu-id="960d6-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="960d6-106">Ao usar as avaliação de origem, os usuários do Microsoft Edge que visitam seu site podem executar um código que usa APIs experimentais.</span><span class="sxs-lookup"><span data-stu-id="960d6-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="960d6-107">Para acessar as APIs experimentais em cada máquina de usuário, você não precisa ir e `edge://flags` ativar sinalizadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="960d6-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="960d6-108">Para obter mais informações, navegue até [APIs experimentais.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="960d6-108">For more information, navigate to [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="960d6-109">Além disso, você pode fornecer comentários sobre o design da API, seus casos de uso ou sua experiência usando as APIs para engenheiros de navegador e a comunidade padrão da Web.</span><span class="sxs-lookup"><span data-stu-id="960d6-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <a name="get-started-using-origin-trials"></a><span data-ttu-id="960d6-110">Começar a usar as avaliação de origem</span><span class="sxs-lookup"><span data-stu-id="960d6-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="960d6-111">Para obter mais informações sobre as APIs experimentais disponíveis no Microsoft Edge, navegue até [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="960d6-111">For more information about the experimental APIs available in Microsoft Edge, navigate to [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="960d6-112">Verifique os requisitos mínimos de versão para o Microsoft Edge e a data de término da avaliação para avaliar a adequação do uso das APIs experimentais em seu site.</span><span class="sxs-lookup"><span data-stu-id="960d6-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="960d6-113">Um experimento pode terminar antes do planejado se qualquer uma das seguintes situações ocorrer.</span><span class="sxs-lookup"><span data-stu-id="960d6-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="960d6-114">Um incidente de segurança grave.</span><span class="sxs-lookup"><span data-stu-id="960d6-114">A major security incident.</span></span>  
> *   <span data-ttu-id="960d6-115">Se os comentários suficientes são coletados que indicam que um grande redesenho é necessário para atender às necessidades dos desenvolvedores da Web.</span><span class="sxs-lookup"><span data-stu-id="960d6-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="960d6-116">Em ambos os casos, um email de notificação é enviado para todos os desenvolvedores atualmente inscritos no experimento.</span><span class="sxs-lookup"><span data-stu-id="960d6-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <a name="register-for-a-trial-of-an-experimental-api"></a><span data-ttu-id="960d6-117">Registrar-se para uma avaliação de uma API experimental</span><span class="sxs-lookup"><span data-stu-id="960d6-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="960d6-118">Use as etapas a seguir para registrar uma avaliação de uma API experimental.</span><span class="sxs-lookup"><span data-stu-id="960d6-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="960d6-119">Visite a [página Console do Desenvolvedor de Avaliação de Origem do Microsoft Edge.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="960d6-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="960d6-120">Escolha o botão Registrar em qualquer um dos experimentos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="960d6-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="960d6-121">Entre no Console do Desenvolvedor usando seu nome de usuário e senha do GitHub.</span><span class="sxs-lookup"><span data-stu-id="960d6-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="960d6-122">Escolha **Autorizar o MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="960d6-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="960d6-123">Preencha o formulário.</span><span class="sxs-lookup"><span data-stu-id="960d6-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="960d6-124">Para registrar um único ou todos os subdomas, escolha definir a `Do you need to match all subdomains for the provided origin?` configuração como `Yes` .</span><span class="sxs-lookup"><span data-stu-id="960d6-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="960d6-125">Por exemplo, `https://dev.contoso.com` é um único domínio e usa um `https://*.contoso.com` curinga para representar todos os subdomas.</span><span class="sxs-lookup"><span data-stu-id="960d6-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="960d6-126">Os seguintes formatos de origem não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="960d6-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="960d6-127">Especificando uma subpasta na origem.</span><span class="sxs-lookup"><span data-stu-id="960d6-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="960d6-128">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="960d6-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="960d6-129">Usando uma origem com parâmetros de cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="960d6-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="960d6-130">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="960d6-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="960d6-131">Escolha **ACEITAR e REGISTRAR**.</span><span class="sxs-lookup"><span data-stu-id="960d6-131">Choose **ACCEPT and REGISTER**.</span></span>  
    
### <a name="apply-your-token"></a><span data-ttu-id="960d6-132">Aplicar seu token</span><span class="sxs-lookup"><span data-stu-id="960d6-132">Apply your token</span></span>  

<span data-ttu-id="960d6-133">Um token é gerado instantaneamente e exibido na página Console do Desenvolvedor de Avaliação de Origem do [Microsoft Edge.][DeveloperMicrsoftEdgeOriginTrials]</span><span class="sxs-lookup"><span data-stu-id="960d6-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="960d6-134">Para começar a usar a avaliação em seu site, use um dos métodos a seguir para aplicar o token à sua página.</span><span class="sxs-lookup"><span data-stu-id="960d6-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="960d6-135">Adicione o `origin-trial` valor do atributo e seu token à marca em cada página que usa a API `meta` experimental.</span><span class="sxs-lookup"><span data-stu-id="960d6-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="960d6-136">Adicione `Origin-Trial` ao cabeçalho de resposta HTTP do seu servidor.</span><span class="sxs-lookup"><span data-stu-id="960d6-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="960d6-137">Seu token é válido por 6 semanas.</span><span class="sxs-lookup"><span data-stu-id="960d6-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="960d6-138">Antes do final da avaliação, os emails de lembrete são enviados para você que solicitam seus comentários e solicitam que você considere a renovação da avaliação antes que seu token expire.</span><span class="sxs-lookup"><span data-stu-id="960d6-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <a name="opt-out-of-an-experiment"></a><span data-ttu-id="960d6-139">Não participar de um experimento</span><span class="sxs-lookup"><span data-stu-id="960d6-139">Opt out of an experiment</span></span>  

<span data-ttu-id="960d6-140">Para não participar de um experimento, use um dos métodos a seguir para remover seu token.</span><span class="sxs-lookup"><span data-stu-id="960d6-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="960d6-141">Remova a `meta` marca de cada página que usou a API experimental.</span><span class="sxs-lookup"><span data-stu-id="960d6-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="960d6-142">Remova `Origin-Trial` do cabeçalho de resposta HTTP do seu servidor.</span><span class="sxs-lookup"><span data-stu-id="960d6-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a><span data-ttu-id="960d6-143">Detectar recursos experimentais e fornecer um fallback</span><span class="sxs-lookup"><span data-stu-id="960d6-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="960d6-144">Ao usar APIs experimentais, certifique-se de fornecer uma experiência de trabalho para todos os visitantes do seu site.</span><span class="sxs-lookup"><span data-stu-id="960d6-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="960d6-145">Os visitantes podem usar navegadores que não suportam as APIs experimentais que você adicionou ao código.</span><span class="sxs-lookup"><span data-stu-id="960d6-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="960d6-146">Além disso, se o token expirar antes de renová-lo, a API experimental não estará mais disponível, o que pode resultar em erros.</span><span class="sxs-lookup"><span data-stu-id="960d6-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="960d6-147">Para evitar essa situação, certifique-se de detectar recursos disponíveis no navegador.</span><span class="sxs-lookup"><span data-stu-id="960d6-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="960d6-148">Para obter mais informações, navegue até [Implementando a detecção de recursos][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="960d6-148">For more information, navigate to [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <a name="roadmap-for-allowed-origins"></a><span data-ttu-id="960d6-149">Roteiro para Origens Permitidas</span><span class="sxs-lookup"><span data-stu-id="960d6-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="960d6-150">O portal de Avaliação de Origem do Microsoft Edge atualmente só dá suporte a Origens Habilitadas para SSL, o que significa que os sites devem ter HTTPS implementado corretamente para registrar um experimento.</span><span class="sxs-lookup"><span data-stu-id="960d6-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="960d6-151">No futuro, as seguintes origens seguras são planejadas.</span><span class="sxs-lookup"><span data-stu-id="960d6-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="960d6-152">`http://localhost`Registre-se como a origem de seus experimentos.</span><span class="sxs-lookup"><span data-stu-id="960d6-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="960d6-153">Para usar `http://localhost` hoje, navegue até `edge://flags` e de definir o experimento como **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="960d6-153">To use `http://localhost` today, navigate to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="960d6-154">Use extensões com `extensions://` origens prefixadas para se registrar em experimentos.</span><span class="sxs-lookup"><span data-stu-id="960d6-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementando a detecção de recursos | MDN"  
