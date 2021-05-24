---
description: Este artigo fornece documentação sobre as dicas Microsoft Edge cliente do agente de usuário e a cadeia de caracteres de agente do usuário
title: Como detectar o Microsoft Edge em seu site
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user agent string, ua string, ua overrides, user-agent client hints, user agent client hints, ua client hints, ua ch
ms.openlocfilehash: 1957bb5bd33d9d921d8a12e16a4a52a23836027b
ms.sourcegitcommit: e90bbc210b5d510004bbc2145d49e14fe72ed54b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/20/2021
ms.locfileid: "11578773"
---
# <a name="how-to-detect-microsoft-edge-in-your-website"></a><span data-ttu-id="9457e-104">Como detectar o Microsoft Edge em seu site</span><span class="sxs-lookup"><span data-stu-id="9457e-104">How to detect Microsoft Edge in your website</span></span>  

<span data-ttu-id="9457e-105">Os navegadores fornecem mecanismos para que os sites detectem informações do navegador, como a marca e o número da versão.</span><span class="sxs-lookup"><span data-stu-id="9457e-105">Browsers provide mechanisms for websites to detect browser information such as brand and version number.</span></span>  <span data-ttu-id="9457e-106">Os mecanismos também detectam outras características de dispositivo, como o sistema operacional host.</span><span class="sxs-lookup"><span data-stu-id="9457e-106">The mechanisms also detect other device characteristics like the host operating system.</span></span>  <span data-ttu-id="9457e-107">Dois desses mecanismos suportados no Microsoft Edge são [User-Agent Client Hints](#user-agent-client-hints) e [User-Agent strings](#user-agent-string).</span><span class="sxs-lookup"><span data-stu-id="9457e-107">Two such mechanisms supported on Microsoft Edge are [User-Agent Client Hints](#user-agent-client-hints) and [User-Agent strings](#user-agent-string).</span></span>  <span data-ttu-id="9457e-108">Após décadas de uso, User-Agent cadeias de caracteres estão desatualizadas e têm um histórico longo como causa de problemas de compatibilidade de site.</span><span class="sxs-lookup"><span data-stu-id="9457e-108">After decades of use, User-Agent strings are outdated and have a long history as the cause of website compatibility issues.</span></span>  <span data-ttu-id="9457e-109">Em vez disso, Microsoft Edge equipe recomenda que você use um mecanismo aprimorado para recuperar informações do navegador chamadas [User-Agent Client Hints](#user-agent-client-hints).</span><span class="sxs-lookup"><span data-stu-id="9457e-109">Instead, the Microsoft Edge team recommends you use an improved mechanism to retrieve browser information named [User-Agent Client Hints](#user-agent-client-hints).</span></span>  <span data-ttu-id="9457e-110">Este artigo descreve os dois mecanismos que Microsoft Edge suporte para recuperar informações do agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="9457e-110">This article outlines the two mechanisms Microsoft Edge supports for retrieving user agent information.</span></span>  

|  | <span data-ttu-id="9457e-111">Lado do servidor</span><span class="sxs-lookup"><span data-stu-id="9457e-111">Server-side</span></span> | <span data-ttu-id="9457e-112">Lado do cliente</span><span class="sxs-lookup"><span data-stu-id="9457e-112">Client-side</span></span> |  
|:--- |:--- |:--- | 
| <span data-ttu-id="9457e-113">**Dicas de cliente de** agente de usuário \(recommended\)</span><span class="sxs-lookup"><span data-stu-id="9457e-113">**User-Agent Client Hints** \(recommended\)</span></span> | `Sec-CH-UA` <span data-ttu-id="9457e-114">Cabeçalho HTTPS</span><span class="sxs-lookup"><span data-stu-id="9457e-114">HTTPS header</span></span> | `navigator.userAgentData` <span data-ttu-id="9457e-115">Método JavaScript</span><span class="sxs-lookup"><span data-stu-id="9457e-115">JavaScript method</span></span> |  
| <span data-ttu-id="9457e-116">**Cadeia de caracteres user-agent** \(legacy\)</span><span class="sxs-lookup"><span data-stu-id="9457e-116">**User-Agent string** \(legacy\)</span></span> | `User-Agent` <span data-ttu-id="9457e-117">Cabeçalho HTTPS</span><span class="sxs-lookup"><span data-stu-id="9457e-117">HTTPS header</span></span> | `navigator.userAgent` <span data-ttu-id="9457e-118">Método JavaScript</span><span class="sxs-lookup"><span data-stu-id="9457e-118">JavaScript method</span></span> |  

<span data-ttu-id="9457e-119">A Microsoft recomenda que você use a detecção [de recursos][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] sempre que possível pelos seguintes motivos.</span><span class="sxs-lookup"><span data-stu-id="9457e-119">Microsoft recommends that you use [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] whenever possible for the following reasons.</span></span>  

*   <span data-ttu-id="9457e-120">Melhorar a manutenção do código.</span><span class="sxs-lookup"><span data-stu-id="9457e-120">Improve code maintainability.</span></span>  
*   <span data-ttu-id="9457e-121">Reduza a fragilidade do código.</span><span class="sxs-lookup"><span data-stu-id="9457e-121">Reduce code fragility.</span></span>  
*   <span data-ttu-id="9457e-122">Reduza a quebra de código das alterações na User-Agent cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9457e-122">Reduce code breakage from changes to the User-Agent string.</span></span>  
    
<span data-ttu-id="9457e-123">Quando [a detecção de][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] recursos não for aplicável e você deve usar a detecção de agente de usuário, use o formato a seguir para detectar Microsoft Edge agente de usuário no Windows e Android.</span><span class="sxs-lookup"><span data-stu-id="9457e-123">When [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable and you must use user agent detection, use the following format to detect Microsoft Edge user agent on Windows and Android.</span></span>  

## <a name="user-agent-client-hints"></a><span data-ttu-id="9457e-124">User-Agent dicas de cliente</span><span class="sxs-lookup"><span data-stu-id="9457e-124">User-Agent Client Hints</span></span>  

<span data-ttu-id="9457e-125">A partir Microsoft Edge versão 90, acesse as informações do navegador de forma mais limpa e preservando a privacidade.</span><span class="sxs-lookup"><span data-stu-id="9457e-125">Starting in Microsoft Edge version 90, access browser information in a cleaner, more privacy-preserving way.</span></span>  

### <a name="user-agent-client-hints-https-header"></a><span data-ttu-id="9457e-126">User-Agent cliente dicas de cabeçalho HTTPS</span><span class="sxs-lookup"><span data-stu-id="9457e-126">User-Agent Client Hints HTTPS Header</span></span>  

<span data-ttu-id="9457e-127">Por padrão, Chromium navegadores incluindo Microsoft Edge enviar o header de `Accept-CH-UA` resposta no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="9457e-127">By default, Chromium browsers including Microsoft Edge send the `Accept-CH-UA` response header in the following format.</span></span>  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> <span data-ttu-id="9457e-128">As Dicas de Cliente são enviadas apenas por conexões seguras usando `HTTPS` .</span><span class="sxs-lookup"><span data-stu-id="9457e-128">Client Hints are only sent over secure connections using `HTTPS`.</span></span>  

<span data-ttu-id="9457e-129">As dicas de entropia baixa a seguir são enviadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="9457e-129">The following low entropy hints are sent by default.</span></span>  <span data-ttu-id="9457e-130">Se precisar acessar mais informações, envie um dos seguintes headers de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9457e-130">If you need to access more information, send one of the following request headers.</span></span>  

#### <a name="user-agent-request-and-response-headers"></a><span data-ttu-id="9457e-131">User-Agent de solicitação e resposta</span><span class="sxs-lookup"><span data-stu-id="9457e-131">User-Agent request and response headers</span></span>  

| <span data-ttu-id="9457e-132">Cabeçalho da solicitação</span><span class="sxs-lookup"><span data-stu-id="9457e-132">Request header</span></span> | <span data-ttu-id="9457e-133">Valor de resposta de exemplo</span><span class="sxs-lookup"><span data-stu-id="9457e-133">Example response value</span></span> |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a><span data-ttu-id="9457e-134">User-Agent Api JavaScript de Dicas de Cliente</span><span class="sxs-lookup"><span data-stu-id="9457e-134">User-Agent Client Hints JavaScript API</span></span>  

<span data-ttu-id="9457e-135">O valor de resposta padrão de `navigator.userAgentData` usa o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="9457e-135">The default response value from `navigator.userAgentData` uses the following format.</span></span>  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

<span data-ttu-id="9457e-136">Se você precisar acessar informações mais detalhadas, use o [método getHighEntropyValues().][GithubWicgUaClientHintsGethighentropyvalues]</span><span class="sxs-lookup"><span data-stu-id="9457e-136">If you need to access more detailed information, use the [getHighEntropyValues()][GithubWicgUaClientHintsGethighentropyvalues] method.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9457e-137">O trecho de código a seguir envia uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="9457e-137">The following code snippet sends a request.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9457e-138">Para receber a seguinte resposta.</span><span class="sxs-lookup"><span data-stu-id="9457e-138">To receive the following response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```javascript
         navigator.userAgentData.getHighEntropyValues(
             ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
             .then(ua => { console.log(ua) });
      ```  
   :::column-end:::
   :::column span="":::
      ```javascript
      {architecture: "x86", 
      model: "", 
      platform: "Windows", 
      platformVersion: "10.0", 
      uaFullVersion: "92.0.866.0"}
      ```  
   :::column-end:::
:::row-end:::  

## <a name="recommended-uses-of-user-agent-client-hints"></a><span data-ttu-id="9457e-139">Usos recomendados User-Agent dicas de cliente</span><span class="sxs-lookup"><span data-stu-id="9457e-139">Recommended uses of User-Agent Client Hints</span></span>  

<span data-ttu-id="9457e-140">O conjunto de marcas e a ordem de exibição associada mudam ao longo do tempo, portanto, você nunca deve codificar índices na matriz de marcas retornadas.</span><span class="sxs-lookup"><span data-stu-id="9457e-140">The set of brands and the associated display order change over time, so you should never hard-code indices into the array of returned brands.</span></span>  <span data-ttu-id="9457e-141">Para ajudar a garantir que você localize problemas semelhantes em seu site no início, o navegador inclui um valor de marca que muda ao longo do tempo e é formatado para quebra devido a problemas comuns de análise de `GREASE` cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9457e-141">To help ensure you spot similar issues in your website early, the browser includes a `GREASE` brand value that changes over time and is formatted to break because of common string parsing issues.</span></span>  

<span data-ttu-id="9457e-142">Se você for impedido de usar a detecção de [recursos,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]não use uma lista codificada de navegadores Chromium conhecidos para verificação.</span><span class="sxs-lookup"><span data-stu-id="9457e-142">If you're prevented from using [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection], don't use a hardcoded list of known Chromium-based browsers for verification.</span></span>  <span data-ttu-id="9457e-143">Exemplos de nomes de navegadores de código rígido `Microsoft Edge` incluem e `Google Chrome` .</span><span class="sxs-lookup"><span data-stu-id="9457e-143">Examples of hardcoded browser names include `Microsoft Edge` and `Google Chrome`.</span></span>  <span data-ttu-id="9457e-144">Os motivos pelos [quais a][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] detecção de recursos não é aplicável podem incluir a seguinte situação.</span><span class="sxs-lookup"><span data-stu-id="9457e-144">Reasons why [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable may include the following situation.</span></span>  

*   <span data-ttu-id="9457e-145">Uma correção para Chromium bug em uma versão posterior deve ser evitada e os navegadores afetados são difíceis de detectar fora de uma verificação da marca e da versão.</span><span class="sxs-lookup"><span data-stu-id="9457e-145">A fix for a Chromium bug in a later version must be avoided and the affected browsers are difficult to detect outside of a verification of the brand and version.</span></span>  
    
<span data-ttu-id="9457e-146">Em vez disso, você deve verificar a marca, o que garante que sua detecção se aplique a todos os navegadores Chromium `Chromium` baseados em Chromium afetados.</span><span class="sxs-lookup"><span data-stu-id="9457e-146">Instead, you should verify the `Chromium` brand, which ensures your detection applies to all affected Chromium-based browsers.</span></span>  


```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium") {
            return true;
        }
    }
    return false;
}
```  

## <a name="user-agent-string"></a><span data-ttu-id="9457e-147">Cadeia de caracteres de agente do usuário</span><span class="sxs-lookup"><span data-stu-id="9457e-147">User agent string</span></span>  

<span data-ttu-id="9457e-148">Sempre que possível, a Microsoft recomenda minimizar o uso da Microsoft Edge de detecção do navegador com base na cadeia de caracteres do agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="9457e-148">Wherever possible, Microsoft recommends you minimize your use of Microsoft Edge browser detection logic based on the user agent string.</span></span>  <span data-ttu-id="9457e-149">Se você tiver um bom motivo para detectar o agente do usuário, a equipe Microsoft Edge recomenda que você [use](#user-agent-client-hints) As Dicas de Cliente de Agente de Usuário como a lógica de detecção principal.</span><span class="sxs-lookup"><span data-stu-id="9457e-149">If you have a good reason to detect the user agent, the Microsoft Edge team recommends you use [User-Agent Client Hints](#user-agent-client-hints) as the primary detection logic.</span></span>  <span data-ttu-id="9457e-150">[As Dicas](#user-agent-client-hints) de Cliente do Agente de Usuário também reduzem o número necessário de cadeias de caracteres analisados.</span><span class="sxs-lookup"><span data-stu-id="9457e-150">[User-Agent Client Hints](#user-agent-client-hints) also reduces the required number of parsed strings.</span></span>  <span data-ttu-id="9457e-151">No entanto, para referência herdado, o formato a seguir é usado para User-Agent cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9457e-151">However, for legacy reference, the following format is used for the User-Agent string.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9457e-152">No Windows, o `User-Agent` cabeçalho de solicitação HTTP usa o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="9457e-152">On Windows, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9457e-153">No Android, o `User-Agent` cabeçalho de solicitação HTTP usa o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="9457e-153">On Android, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="9457e-154">O valor de resposta `navigator.userAgent` do método usa o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="9457e-154">The response value from `navigator.userAgent` method uses the following format.</span></span>  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

<span data-ttu-id="9457e-155">Os identificadores de plataforma mudam com base no sistema operacional usado, e os números de versão também são incrementados conforme o tempo passa.</span><span class="sxs-lookup"><span data-stu-id="9457e-155">Platform identifiers change based on the operating system used, and the version numbers also increment as time passes.</span></span>  <span data-ttu-id="9457e-156">O formato é o mesmo que o Chromium do usuário com a adição de um `Edg` novo token no final.</span><span class="sxs-lookup"><span data-stu-id="9457e-156">The format is the same as the Chromium user agent with the addition of a new `Edg` token at the end.</span></span>  <span data-ttu-id="9457e-157">A Microsoft escolheu o token para evitar problemas de compatibilidade causados pela cadeia de caracteres, que foi usada Microsoft Edge `Edg` `Edge` navegador herdado com base no EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="9457e-157">Microsoft chose the `Edg` token to avoid compatibility issues caused by `Edge` string, which was used legacy Microsoft Edge browser based on EdgeHTML.</span></span>  <span data-ttu-id="9457e-158">O `Edg` token também é consistente com [tokens existentes][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] usados no iOS e no Android.</span><span class="sxs-lookup"><span data-stu-id="9457e-158">The `Edg` token is also consistent with [existing tokens][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] used on iOS and Android.</span></span>

## <a name="map-the-user-agent-string-to-browser-name"></a><span data-ttu-id="9457e-159">Mapear a cadeia de caracteres do agente do usuário para o nome do navegador</span><span class="sxs-lookup"><span data-stu-id="9457e-159">Map the user agent string to browser name</span></span>  

<span data-ttu-id="9457e-160">Mapeie os tokens de cadeia de caracteres do agente do usuário para um nome de navegador mais acessível para uso no código.</span><span class="sxs-lookup"><span data-stu-id="9457e-160">Map the user agent string tokens to a more human-readable browser name to use in code.</span></span>  <span data-ttu-id="9457e-161">É um padrão comum na Web hoje.</span><span class="sxs-lookup"><span data-stu-id="9457e-161">It's a common pattern on the web today.</span></span>  <span data-ttu-id="9457e-162">Quando você mapeia o novo token para um nome de navegador, a Microsoft recomenda que você use um nome diferente do usado para o navegador Microsoft Edge herdado para evitar a aplicação acidental de qualquer solução alternativa herdada que não seja aplicável a navegadores baseados em `Edg` Chromium.</span><span class="sxs-lookup"><span data-stu-id="9457e-162">When you map the new `Edg` token to a browser name, Microsoft recommends that you use a different name than the one used for the legacy Microsoft Edge browser to avoid accidentally applying any legacy workarounds that aren't applicable to Chromium-based browsers.</span></span>

## <a name="user-agent-overrides"></a><span data-ttu-id="9457e-163">O Agente de Usuário substitui</span><span class="sxs-lookup"><span data-stu-id="9457e-163">User Agent overrides</span></span>  

<span data-ttu-id="9457e-164">Às vezes, um site não reconhece o novo Microsoft Edge usuário.</span><span class="sxs-lookup"><span data-stu-id="9457e-164">Sometimes, a website doesn't recognize the new Microsoft Edge user agent.</span></span>  <span data-ttu-id="9457e-165">Como resultado, um conjunto de recursos do site pode não funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="9457e-165">As a result, a set of the features of the website may not work correctly.</span></span>  <span data-ttu-id="9457e-166">Quando a Microsoft é notificada sobre os tipos de problemas, a Microsoft o contata \(um proprietário do site\) e informa sobre o agente de usuário atualizado.</span><span class="sxs-lookup"><span data-stu-id="9457e-166">When Microsoft is notified about the types of issues, Microsoft contacts you \(a website owner\) and informs you about the updated user agent.</span></span>  

<span data-ttu-id="9457e-167">Talvez você precise de mais tempo para atualizar e testar a lógica de detecção do agente do usuário para seu site para resolver os problemas relatados pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9457e-167">You may need more time to update and test the user agent detection logic for your website to address the issues reported by Microsoft.</span></span>  <span data-ttu-id="9457e-168">Para maximizar a compatibilidade com seus usuários, os canais Microsoft Edge Beta e Estável usam uma lista de substituições de agente de usuário.</span><span class="sxs-lookup"><span data-stu-id="9457e-168">To maximize compatibility for your users, the Microsoft Edge Beta and Stable channels use a list of user agent overrides.</span></span>  <span data-ttu-id="9457e-169">Use as substituições do agente do usuário enquanto você atualiza seu site.</span><span class="sxs-lookup"><span data-stu-id="9457e-169">Use the user agent overrides while you update your website.</span></span>  <span data-ttu-id="9457e-170">A lista de substituições de agente de usuário fornecidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9457e-170">The list of user agent overrides provided by Microsoft.</span></span>  

<span data-ttu-id="9457e-171">As substituições especificam novos valores de agente de usuário que Microsoft Edge envia em vez do agente de usuário padrão para sites específicos.</span><span class="sxs-lookup"><span data-stu-id="9457e-171">The overrides specify new user agent values that Microsoft Edge sends instead of the default user agent for specific websites.</span></span>  <span data-ttu-id="9457e-172">Para exibir a lista de substituições de agente de usuário aplicadas no momento, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9457e-172">To display the list of user agent overrides that are currently applied, complete the following actions.</span></span>  

1.  <span data-ttu-id="9457e-173">Abra o Microsoft Edge Beta ou canal Estável.</span><span class="sxs-lookup"><span data-stu-id="9457e-173">Open the Microsoft Edge Beta or Stable channel.</span></span>  
1.  <span data-ttu-id="9457e-174">Navegue até `edge://compat/useragent`.</span><span class="sxs-lookup"><span data-stu-id="9457e-174">Navigate to `edge://compat/useragent`.</span></span>  
    
<span data-ttu-id="9457e-175">Os Microsoft Edge canais Canary e Dev não recebem substituições de agente de usuário no momento.</span><span class="sxs-lookup"><span data-stu-id="9457e-175">The Microsoft Edge Canary and Dev channels don't currently receive user agent overrides.</span></span>  <span data-ttu-id="9457e-176">Os Microsoft Edge canais Canary e Dev fornecem ambientes que usam o agente de usuário padrão Microsoft Edge usuário.</span><span class="sxs-lookup"><span data-stu-id="9457e-176">The Microsoft Edge Canary and Dev channels provide environments that use the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="9457e-177">Use os canais Microsoft Edge Canary e Dev para reproduzir facilmente problemas em seu site causados pelo agente de usuário padrão Microsoft Edge usuário.</span><span class="sxs-lookup"><span data-stu-id="9457e-177">Use the Microsoft Edge Canary and Dev channels to easily reproduce issues on your website caused by the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="9457e-178">Para desativar as substituições do agente de usuário nos canais Microsoft Edge Beta ou Estável, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9457e-178">To turn off user agent overrides in the Microsoft Edge Beta or Stable channels, complete the following actions.</span></span>  

1.  <span data-ttu-id="9457e-179">Abra seu aplicativo de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9457e-179">Open your command-line app.</span></span>  
1.  <span data-ttu-id="9457e-180">Copie e colar o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="9457e-180">Copy and paste the following code snippet.</span></span>  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  <span data-ttu-id="9457e-181">Execute o Microsoft Edge usando o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="9457e-181">Run the Microsoft Edge app using the code snippet.</span></span>  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge para iOS e Android: o que os desenvolvedores precisam saber | Blogs Windows Microsoft"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. método getHighEntropyValues - User-Agent Dicas de Cliente | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementando a detecção de recursos | MDN"  
