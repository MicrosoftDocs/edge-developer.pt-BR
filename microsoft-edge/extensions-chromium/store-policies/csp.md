---
description: Política de Segurança de Conteúdo para Extensões de Borda (Chromium).
title: Política de Segurança de Conteúdo (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 8307482e780b4d631edffd976cca7ba724e2ad40
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397514"
---
# <a name="content-security-policy-csp"></a><span data-ttu-id="0a1f8-104">Política de Segurança de Conteúdo \(CSP\)</span><span class="sxs-lookup"><span data-stu-id="0a1f8-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="0a1f8-105">Para reduzir uma grande classe de possíveis problemas de script entre sites, o sistema de Extensão do Microsoft Edge incorporou o conceito geral de Política de Segurança de Conteúdo [\(CSP\)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="0a1f8-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="0a1f8-106">Isso introduz algumas políticas bastante estritas que fazem extensões mais seguras por padrão e fornece a você a capacidade de criar e impor regras que regem os tipos de conteúdo que podem ser carregados e executados por suas Extensões e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="0a1f8-107">Em geral, o CSP funciona como um mecanismo de bloqueio/lista de recursos carregados ou executados por suas Extensões.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="0a1f8-108">A definição de uma política razoável para o Extension permite que você considere cuidadosamente os recursos necessários para o Extension e peça ao navegador para garantir que esses sejam os únicos recursos aos quais o Extension tem acesso.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="0a1f8-109">As políticas fornecem segurança acima e acima das permissões de host que suas solicitações de Extensão; eles são uma camada adicional de proteção, não uma substituição.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-109">The policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="0a1f8-110">Na Web, essa política é definida por meio de um cabeçalho HTTP ou `meta` elemento.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="0a1f8-111">Dentro do sistema de Extensão do Microsoft Edge, nenhum deles é um mecanismo apropriado.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="0a1f8-112">Em vez disso, uma política de Extensão é definida usando `manifest.json` o arquivo para o Extension da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-112">Instead, an Extension policy is defined using the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="0a1f8-113">Para obter detalhes completos sobre a sintaxe do CSP, confira a especificação da Política de Segurança de Conteúdo [e][W3CContentSecurityPolicy] o artigo "Introdução à Política de Segurança de [Conteúdo"][HTML5RocksIntroductionContentSecurityPolicy] em HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <a name="default-policy-restrictions"></a><span data-ttu-id="0a1f8-114">Restrições de política padrão</span><span class="sxs-lookup"><span data-stu-id="0a1f8-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="0a1f8-115">Pacotes que não definem um `manifest_version` não têm uma política de segurança de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="0a1f8-116">Os pacotes que escolherem 2 têm uma política de segurança de `manifest_version` conteúdo padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-116">Packages that choose `manifest_version` 2, have a the follwoing default content security policy.</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="0a1f8-117">A política adiciona segurança limitando extensões e aplicativos de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-117">The policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="0a1f8-118">Funções relacionadas e de avaliação estão desabilitadas</span><span class="sxs-lookup"><span data-stu-id="0a1f8-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="0a1f8-119">Código como o seguinte não funciona:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="0a1f8-120">Avaliar cadeias de caracteres de JavaScript como esta é um vetor de ataque XSS comum.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="0a1f8-121">Em vez disso, você deve escrever código como:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="0a1f8-122">JavaScript embutido não são executados</span><span class="sxs-lookup"><span data-stu-id="0a1f8-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="0a1f8-123">JavaScript embutido não são executados.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="0a1f8-124">Essa restrição proíbe blocos em linha e manipuladores de eventos em `<script>` linha, como `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="0a1f8-125">A primeira restrição apaga uma classe enorme de ataques de script entre sites, tornando impossível executar acidentalmente o script fornecido por um terceiro mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="0a1f8-126">No entanto, ele exige que você escreva seu código com uma separação limpa entre o conteúdo e o comportamento \(o que você deve fazer de qualquer maneira, certo?\).</span><span class="sxs-lookup"><span data-stu-id="0a1f8-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="0a1f8-127">Um exemplo pode deixar isso mais claro.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-127">An example may make this clearer.</span></span>  <span data-ttu-id="0a1f8-128">Você pode tentar gravar um pop-up de Ação do Navegador como um único `pop-up.html` que contenha:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

<span data-ttu-id="0a1f8-129">Três coisas devem mudar para que isso funcione da maneira esperada:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="0a1f8-130">A `clickHandler` definição deve ser movida para um arquivo JavaScript externo \( `popup.js` pode ser um bom destino).</span><span class="sxs-lookup"><span data-stu-id="0a1f8-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="0a1f8-131">As definições de manipulador de eventos em linha devem ser reescritas em termos de `addEventListener` e extraídas em `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="0a1f8-132">Se você estiver iniciando seu programa usando código como , considere substituí-lo por conectar-se ao evento do documento ou ao evento da `<body onload="main();">` `DOMContentLoaded` janela, dependendo de seus `load` requisitos.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="0a1f8-133">Use o primeiro, já que geralmente dispara mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="0a1f8-134">A `setTimeout` chamada deve ser regravada para evitar converter a cadeia de `"awesome(); totallyAwesome()"` caracteres em JavaScript para execução.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="0a1f8-135">Essas alterações podem ter a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-135">Those changes may look something like the following:</span></span>  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**<span data-ttu-id="0a1f8-136">Somente os recursos de script e objeto locais são carregados</span><span class="sxs-lookup"><span data-stu-id="0a1f8-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="0a1f8-137">Os recursos de script e objeto só podem ser carregados do pacote extension, e não da Web em geral.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="0a1f8-138">Isso garante que o Extension só executa o código aprovado especificamente, impedindo que um invasor ativo de rede redirecione mal-intencionadamente sua solicitação para um recurso.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="0a1f8-139">Em vez de escrever um código que dependa do carregamento de jQuery \(ou qualquer outra biblioteca\) de uma CDN externa, considere incluir a versão específica do jQuery em seu pacote de Extensão.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="0a1f8-140">Ou seja, em vez de:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-140">That is, instead of:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

<span data-ttu-id="0a1f8-141">Baixe o arquivo, inclua-o no pacote e escreva:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-141">Download the file, include it in your package, and write:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## <a name="relaxing-the-default-policy"></a><span data-ttu-id="0a1f8-142">Descontrair a política padrão</span><span class="sxs-lookup"><span data-stu-id="0a1f8-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="0a1f8-143">Script em linha</span><span class="sxs-lookup"><span data-stu-id="0a1f8-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="0a1f8-144">Scripts embutida podem ser permitidos especificando o hash codificado com base64 do código-fonte na política.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="0a1f8-145">Esse hash deve ser prefixado pelo algoritmo de hash usado \(sha256, sha384 ou sha512\).</span><span class="sxs-lookup"><span data-stu-id="0a1f8-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="0a1f8-146">Por exemplo, navegue até [Hash para uso de \<script\> elementos][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span><span class="sxs-lookup"><span data-stu-id="0a1f8-146">For an example, navigate to [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span></span>  

**<span data-ttu-id="0a1f8-147">Script Remoto</span><span class="sxs-lookup"><span data-stu-id="0a1f8-147">Remote Script</span></span>**  

<span data-ttu-id="0a1f8-148">Se você precisar de alguns recursos externos de JavaScript ou de objeto, você poderá descontrair a política em uma extensão limitada, permitindo listar origens seguras das quais os scripts devem ser aceitos.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="0a1f8-149">Verifique se os recursos de tempo de execução carregados com permissões elevadas de um Extension são exatamente os recursos esperados e não são substituídos por um invasor de rede ativo.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="0a1f8-150">Como [os ataques man-in-the-middle][WikiManMiddleAttacks] são triviais e indetectáveis em HTTP, essas origens não são aceitas.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="0a1f8-151">Atualmente, os desenvolvedores são capazes de permitir origens de lista com os seguintes esquemas: `blob` `filesystem` , , e `https` `extension` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="0a1f8-152">A parte host da origem deve ser explicitamente especificada para `https` os `extension` esquemas e.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="0a1f8-153">Caracteres curinga genéricos, como https:, e não são permitidos; caracteres curinga `https://*` de `https://*.com` subdomínio, como `https://*.example.com` são permitidos.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="0a1f8-154">Domínios na lista [Sufixo][PublicSuffixList] Público também são exibidos como domínios genéricos de nível superior.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="0a1f8-155">Para carregar um recurso desses domínios, o subdomínio deve ser listado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="0a1f8-156">Por exemplo, `https://*.cloudfront.net` não é válido, `https://XXXX.cloudfront.net` mas é capaz de ser `https://*.XXXX.cloudfront.net` `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be `allowlisted`.</span></span>  

<span data-ttu-id="0a1f8-157">Para facilitar o desenvolvimento, os recursos carregados por HTTP de servidores em sua máquina local podem ser `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be `allowlisted`.</span></span>  <span data-ttu-id="0a1f8-158">Você pode permitir fontes de script e objeto de lista em qualquer porta de `http://127.0.0.1` um ou `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="0a1f8-159">A restrição contra recursos carregados por HTTP se aplica somente aos recursos que são executados diretamente.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="0a1f8-160">Você ainda está livre, por exemplo, para fazer conexões com qualquer origem que você quiser; a política padrão não restringe ou qualquer uma das outras `XMLHTTPRequest` `connect-src` diretivas CSP de qualquer maneira.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-160">You are still free, for example, to make `XMLHTTPRequest` connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="0a1f8-161">Uma definição de política descontraída que permite que os recursos de script sejam carregados por `example.com` meio de HTTPS pode ter a aparência:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-161">A relaxed policy definition which allows script resources to be loaded from `example.com` over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="0a1f8-162">Ambos `script-src` e `object-src` são definidos pela política.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="0a1f8-163">O Microsoft Edge não aceita uma política que não limita cada um desses valores a \(pelo menos\) ' `self` '.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="0a1f8-164">JavaScript avaliado</span><span class="sxs-lookup"><span data-stu-id="0a1f8-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="0a1f8-165">A política contra e funções relacionadas, como , e são capazes de ser descontraídas `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` adicionando `unsafe-eval` à sua política:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="0a1f8-166">No entanto, você deve evitar políticas de descontração.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-166">However, you should avoid relaxing policies.</span></span>  <span data-ttu-id="0a1f8-167">As funções são vetores de ataque XSS notórios.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-167">The functions are notorious XSS attack vectors.</span></span>  

## <a name="tightening-the-default-policy"></a><span data-ttu-id="0a1f8-168">Apertar a política padrão</span><span class="sxs-lookup"><span data-stu-id="0a1f8-168">Tightening the default policy</span></span>  

<span data-ttu-id="0a1f8-169">Você pode, é claro, apertar essa política em qualquer medida que o Extension permita para aumentar a segurança às custas de conveniência.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="0a1f8-170">Para especificar que o Extension só pode carregar recursos de qualquer tipo \(imagens e assim por diante\) do pacote de Extensão associado, por exemplo, uma política de pode ser `default-src 'self'` apropriada.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a><span data-ttu-id="0a1f8-171">Scripts de conteúdo</span><span class="sxs-lookup"><span data-stu-id="0a1f8-171">Content Scripts</span></span>  

<span data-ttu-id="0a1f8-172">A política que está sendo discutida se aplica às páginas em segundo plano e às páginas de eventos do Extension.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="0a1f8-173">A forma como os scripts de conteúdo se aplicam aos scripts de conteúdo do Extension é mais complicada.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="0a1f8-174">Scripts de conteúdo geralmente não estão sujeitos ao CSP da Extensão.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="0a1f8-175">Como os scripts de conteúdo não são HTML, o principal impacto disso é que eles podem usar mesmo que o CSP do Extension não especifique , embora isso não `eval` `unsafe-eval` seja recomendado.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="0a1f8-176">Além disso, o CSP da página não se aplica a scripts de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="0a1f8-177">Mais complicadas são `<script>` as marcas que os scripts de conteúdo criam e colocam no DOM da página em que estão sendo executados.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="0a1f8-178">Eles são referenciados como scripts injetados dom no futuro.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="0a1f8-179">Scripts injetados dom que são executados imediatamente após a injeção na página são executados como você pode esperar.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="0a1f8-180">Imagine um script de conteúdo com o seguinte código como um exemplo simples:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="0a1f8-181">Esse script de conteúdo causa `alert` um imediatamente sobre o `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="0a1f8-182">Observe que isso é executado independentemente da política que uma página pode especificar.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="0a1f8-183">No entanto, o comportamento se torna mais complicado dentro desse script injetado dom e para qualquer script que não seja executado imediatamente após a injeção.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="0a1f8-184">Imagine que o Extension está sendo executado em uma página que fornece um CSP associado que especifica `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="0a1f8-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="0a1f8-185">Agora, imagine que o script de conteúdo executa o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="0a1f8-186">Se um usuário escolher esse botão, `onclick` o script não será executado.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-186">If a user chooses that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="0a1f8-187">Isso ocorre porque o script não foi executado imediatamente e o código não é interpretado até que o evento ocorra não seja considerado parte do script de conteúdo, portanto, o CSP da página \(não do Extension\) restringe o `click` comportamento.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-187">This is because the script did not immediately run and code is not interpreted until the `click` event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="0a1f8-188">E como esse CSP não especifica , o manipulador de eventos em `unsafe-inline` linha é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="0a1f8-189">A maneira correta de implementar o comportamento desejado nesse caso pode ser adicionar o manipulador como uma função do script de `onclick` conteúdo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="0a1f8-190">Outro problema semelhante ocorrerá se o script de conteúdo executa o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="0a1f8-191">Nesse caso, o script é executado e o alerta é exibido.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="0a1f8-192">No entanto, leve este caso:</span><span class="sxs-lookup"><span data-stu-id="0a1f8-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="0a1f8-193">Enquanto o script inicial é executado, a chamada `eval` é bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="0a1f8-194">Ou seja, embora o tempo de execução do script inicial seja permitido, o comportamento dentro do script é regulado pelo CSP da página.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="0a1f8-195">Assim, dependendo de como você escreve scripts injetados dom em sua Extensão, as alterações no CSP da página podem afetar o comportamento de sua Extensão.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="0a1f8-196">Como os scripts de conteúdo não são afetados pelo CSP da página, esse é um ótimo motivo para colocar o máximo de comportamento possível de sua Extensão no script de conteúdo, em vez de scripts injetados dom.</span><span class="sxs-lookup"><span data-stu-id="0a1f8-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Uma introdução à política de segurança de conteúdo | Html5 Rochas"  
[PublicSuffixList]: https://publicsuffix.org/list "EXIBIR A LISTA DE SUFIXOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para \<script\> elementos - Nível de Política de Segurança de Conteúdo 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Nível 3 da Política de Segurança de Conteúdo | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque man-in-the-middle | Wikipédia"  

> [!NOTE]
> <span data-ttu-id="0a1f8-202">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a1f8-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0a1f8-203">A página original é encontrada [aqui](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="0a1f8-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0a1f8-205">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a1f8-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
