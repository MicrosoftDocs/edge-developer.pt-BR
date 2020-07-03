---
ms.assetid: ''
description: Experimente com segurança um período de tempo fixo e forneça comentários sobre novos recursos da plataforma.
title: Avaliações de Origem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, tentativas de origem, desenvolvedor
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846522"
---
# <span data-ttu-id="2e6a1-104">Usar testes de origem no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e6a1-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="2e6a1-105">Os desenvolvedores podem usar avaliações de origem para experimentar APIs experimentais em sites ativos por um período limitado de tempo.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="2e6a1-106">Ao usar avaliações de origem, os usuários do Microsoft Edge que acessam o site podem executar um código que usa APIs experimentais.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="2e6a1-107">Para acessar as APIs experimentais em cada computador de usuário, você não precisa ir para `edge://flags` e ativar os sinalizadores de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="2e6a1-108">Para obter mais informações, consulte [APIs experimentales][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="2e6a1-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="2e6a1-109">Além disso, você pode fornecer comentários sobre o design da API, seus casos de uso ou sua experiência ao usar as APIs para engenheiros de navegador e a Comunidade padrão da Web.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <span data-ttu-id="2e6a1-110">Comece a usar os testes de origem</span><span class="sxs-lookup"><span data-stu-id="2e6a1-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="2e6a1-111">Para obter mais informações sobre as APIs experimentais disponíveis no Microsoft Edge, consulte [console de desenvolvedor de tentativas de origem do Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="2e6a1-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="2e6a1-112">Certifique-se de que você revisar os requisitos mínimos de versão do Microsoft Edge e a data de término da avaliação para avaliar a adequação do uso das APIs experimentais em seu site.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="2e6a1-113">Um experimento poderá terminar antes do planejado se qualquer uma das seguintes situações ocorrer.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="2e6a1-114">Um incidente de segurança importante.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-114">A major security incident.</span></span>  
> *   <span data-ttu-id="2e6a1-115">Se forem coletados comentários suficientes que indicam que é preciso fazer um novo design para atender às necessidades dos desenvolvedores da Web.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="2e6a1-116">Em ambos os casos, um e-mail de notificação é enviado a todos os desenvolvedores atualmente registrados no experimento.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <span data-ttu-id="2e6a1-117">Registre-se para obter uma avaliação de uma API experimental</span><span class="sxs-lookup"><span data-stu-id="2e6a1-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="2e6a1-118">Use as etapas a seguir para se registrar para uma avaliação experimental de uma API experimental.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="2e6a1-119">Acesse a página do [console do desenvolvedor de Microsoft Edge originies][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="2e6a1-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="2e6a1-120">Escolha o botão registrar em qualquer um dos experimentos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="2e6a1-121">Conecte-se ao console do desenvolvedor usando seu nome de usuário e senha do GitHub.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="2e6a1-122">Escolha **autorizar MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="2e6a1-123">Preencha o formulário.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2e6a1-124">Para registrar um único ou todos os subdomínios, escolha definir a `Do you need to match all subdomains for the provided origin?` configuração como `Yes` .</span><span class="sxs-lookup"><span data-stu-id="2e6a1-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="2e6a1-125">Por exemplo, `https://dev.contoso.com` é um único domínio e `https://*.contoso.com` usa um curinga para representar todos os subdomínios.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="2e6a1-126">Os seguintes formatos de origem não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="2e6a1-127">Especificando uma subpasta na origem.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="2e6a1-128">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="2e6a1-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="2e6a1-129">Usar uma origem com parâmetros de cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="2e6a1-130">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="2e6a1-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="2e6a1-131">Escolha **aceitar e registrar**.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-131">Choose **ACCEPT and REGISTER**.</span></span>  

### <span data-ttu-id="2e6a1-132">Aplicar seu token</span><span class="sxs-lookup"><span data-stu-id="2e6a1-132">Apply your token</span></span>  

<span data-ttu-id="2e6a1-133">Um token é gerado instantaneamente e exibido na página do [console de desenvolvedor de origem do Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="2e6a1-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="2e6a1-134">Para começar a usar a avaliação no seu site, use um dos seguintes métodos para aplicar o token à sua página.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="2e6a1-135">Adicione o `origin-trial` valor do atributo e seu token à `meta` marca em cada página que usa a API experimental.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="2e6a1-136">Adicione `Origin-Trial` ao cabeçalho de resposta http do seu servidor.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="2e6a1-137">Seu token é válido por 6 semanas.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="2e6a1-138">Antes do término do período de teste, os e-mails dos lembretes são enviados para você, que solicitam seus comentários e pedem que você considere a renovação de sua avaliação antes de o token expirar.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <span data-ttu-id="2e6a1-139">Recusar um experimento</span><span class="sxs-lookup"><span data-stu-id="2e6a1-139">Opt out of an experiment</span></span>  

<span data-ttu-id="2e6a1-140">Para cancelar um experimento, use um dos seguintes métodos para remover o token.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="2e6a1-141">Remova a `meta` marca de cada página que usou a API experimental.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="2e6a1-142">Remover `Origin-Trial` do cabeçalho de resposta http do seu servidor.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <span data-ttu-id="2e6a1-143">Detectar recursos experimentais e fornecer um fallback</span><span class="sxs-lookup"><span data-stu-id="2e6a1-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="2e6a1-144">Ao usar APIs experimentais, certifique-se de fornecer uma experiência de trabalho para todos os visitantes do seu site.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="2e6a1-145">Os visitantes podem usar navegadores que não dão suporte a APIs experimentadas que você adicionou ao seu código.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="2e6a1-146">Além disso, se o token expirar antes de ser renovado, a API experimental não estará mais disponível, o que pode resultar em erros.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="2e6a1-147">Para evitar essa situação, verifique se você detecta recursos disponíveis no seu navegador.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="2e6a1-148">Para obter mais informações, consulte [implementando a detecção de recursos][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="2e6a1-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <span data-ttu-id="2e6a1-149">Mapa de origens permitidas</span><span class="sxs-lookup"><span data-stu-id="2e6a1-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="2e6a1-150">O portal de avaliações de origem do Microsoft Edge hoje só oferece suporte a origens habilitadas para SSL, o que significa que os sites devem ter HTTPS devidamente implementados para se registrarem para um experimento.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="2e6a1-151">No futuro, as seguintes origens seguras são planejadas.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="2e6a1-152">Registre-se `http://localhost` como a origem de seus experimentos.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="2e6a1-153">Para usar `http://localhost` o hoje, vá para `edge://flags` e defina o experimento como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="2e6a1-154">Use extensões com `extensions://` origens prefixadas para se cadastrar em experimentos.</span><span class="sxs-lookup"><span data-stu-id="2e6a1-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Console de desenvolvedor de tentativas de origem do Microsoft Edge | Documentos da Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementando a detecção de recursos | MDN"  
