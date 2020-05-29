---
description: Política de segurança de conteúdo para extensões de Edge (Chromium).
title: Política de segurança de conteúdo (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 52d6d0afb38401250183788726013d521a269f06
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561272"
---
# <span data-ttu-id="ffbdd-104">Política de segurança de conteúdo \ (CSP \)</span><span class="sxs-lookup"><span data-stu-id="ffbdd-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="ffbdd-105">Para reduzir uma grande classe de problemas potenciais de script entre sites, o sistema de extensão do Microsoft Edge incorporou o conceito geral da política de [segurança de conteúdo \ (CSP \)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="ffbdd-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="ffbdd-106">Isso introduz algumas políticas bastante rigorosas que tornam as extensões mais seguras por padrão e oferece a capacidade de criar e impor regras que regem os tipos de conteúdo que podem ser carregados e executados por suas extensões e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="ffbdd-107">Em geral, o CSP funciona como um mecanismo de blocos/allowlisting para recursos carregados ou executados por suas extensões.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="ffbdd-108">Definir uma política razoável para sua extensão permite que você considere cuidadosamente os recursos que sua extensão requer e para solicitar que o navegador Verifique se esses são os únicos recursos aos quais sua extensão tem acesso.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="ffbdd-109">Essas políticas fornecem segurança e, acima das permissões de host, suas solicitações de extensão; Eles são uma camada adicional de proteção, e não um substituto.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-109">These policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="ffbdd-110">Na Web, essa política é definida por meio de um cabeçalho ou `meta` elemento http.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="ffbdd-111">Dentro do sistema de extensão do Microsoft Edge, nenhum deles é um mecanismo apropriado.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="ffbdd-112">Em vez disso, uma política de extensão é definida pelo `manifest.json` arquivo para a extensão da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-112">Instead, an Extension policy is defined via the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="ffbdd-113">Para obter detalhes completos sobre a sintaxe do CSP, confira a [especificação da política de segurança de conteúdo][W3CContentSecurityPolicy] e o artigo ["introdução à política de segurança de conteúdo"][HTML5RocksIntroductionContentSecurityPolicy] em HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <span data-ttu-id="ffbdd-114">Restrições de política padrão</span><span class="sxs-lookup"><span data-stu-id="ffbdd-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="ffbdd-115">Os pacotes que não definem a não `manifest_version` têm uma política de segurança de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="ffbdd-116">Aqueles que selecionarem `manifest_version` 2 têm uma política de segurança de conteúdo padrão de:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-116">Those that select `manifest_version` 2, have a default content security policy of:</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="ffbdd-117">Essa política adiciona segurança limitando extensões e aplicativos de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-117">This policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="ffbdd-118">As funções evals e relacionadas estão desabilitadas</span><span class="sxs-lookup"><span data-stu-id="ffbdd-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="ffbdd-119">Um código como o seguinte não funciona:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="ffbdd-120">Avaliar cadeias de caracteres de JavaScript como esse é um vetor de ataque XSS comum.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="ffbdd-121">Em vez disso, você deve escrever um código como:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="ffbdd-122">JavaScript embutido não são executados</span><span class="sxs-lookup"><span data-stu-id="ffbdd-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="ffbdd-123">JavaScript embutido não são executados.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="ffbdd-124">Essa restrição Bans os blocos embutidos `<script>` e manipuladores de eventos embutidos, como `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="ffbdd-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="ffbdd-125">A primeira restrição apaga uma enorme classe de ataques de script entre sites impossibilitando que você execute acidentalmente o script fornecido por um terceiro mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="ffbdd-126">No entanto, ele exige que você escreva o código com uma separação de limpeza entre conteúdo e comportamento \ (o que você deve fazer é, certo? \).</span><span class="sxs-lookup"><span data-stu-id="ffbdd-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="ffbdd-127">Um exemplo pode deixar isso mais claro.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-127">An example may make this clearer.</span></span>  <span data-ttu-id="ffbdd-128">Você pode tentar escrever um pop-up de ação do navegador como um único `pop-up.html` contendo:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="ffbdd-129">Três itens devem mudar para que isso funcione da maneira esperada:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="ffbdd-130">A `clickHandler` definição deve ser movida para um arquivo JavaScript externo \ ( `popup.js` pode ser um bom alvo).</span><span class="sxs-lookup"><span data-stu-id="ffbdd-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="ffbdd-131">As definições do manipulador de eventos embutidas devem ser regravadas em termos de `addEventListener` e extraídos para `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="ffbdd-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="ffbdd-132">Se, no momento, você iniciar o programa usando um código como `<body onload="main();">` , considere substituí-lo ao se conectar ao `DOMContentLoaded` evento do documento ou ao `load` evento da janela, dependendo dos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="ffbdd-133">Use o primeiro, uma vez que ele geralmente é acionado mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="ffbdd-134">A `setTimeout` chamada deve ser reescrita para evitar converter a cadeia de caracteres `"awesome(); totallyAwesome()"` em JavaScript para execução.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="ffbdd-135">Essas alterações podem ter uma aparência semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="ffbdd-136">Somente recursos locais de script e de objeto são carregados</span><span class="sxs-lookup"><span data-stu-id="ffbdd-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="ffbdd-137">Recursos de script e de objeto só podem ser carregados do pacote de extensão, e não da Web, em grande parte.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="ffbdd-138">Isso garante que sua extensão execute apenas o código que você aprovou especificamente, evitando que um invasor de rede ativo redirecione sua solicitação para um recurso de maneira maliciosa.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="ffbdd-139">Em vez de escrever código que dependa do jQuery \ (ou de qualquer outra biblioteca \) carregando de uma CDN externa, considere a inclusão da versão específica do jQuery em seu pacote de extensão.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="ffbdd-140">Ou seja, em vez de:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-140">That is, instead of:</span></span>  

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

<span data-ttu-id="ffbdd-141">Baixe o arquivo, inclua-o no pacote e escreva:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-141">Download the file, include it in your package, and write:</span></span>  

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

## <span data-ttu-id="ffbdd-142">Relaxar a política padrão</span><span class="sxs-lookup"><span data-stu-id="ffbdd-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="ffbdd-143">Script embutido</span><span class="sxs-lookup"><span data-stu-id="ffbdd-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="ffbdd-144">Scripts embutidos podem ser permitidos especificando o hash codificado em base64 do código-fonte na política.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="ffbdd-145">Esse hash deve ser prefixado pelo algoritmo de hash usado \ (SHA256, Sha384 ou SHA512 \).</span><span class="sxs-lookup"><span data-stu-id="ffbdd-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="ffbdd-146">Consulte o [uso de hash para os elementos \ <script \ >][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] para obter um exemplo.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-146">See [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] for an example.</span></span>  

**<span data-ttu-id="ffbdd-147">Script remoto</span><span class="sxs-lookup"><span data-stu-id="ffbdd-147">Remote Script</span></span>**  

<span data-ttu-id="ffbdd-148">Se você precisar de alguns recursos externos de JavaScript ou de objetos, pode relaxar a política para uma extensão limitada allowlisting proteger as origens de quais scripts devem ser aceitos.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="ffbdd-149">Verifique se os recursos de tempo de execução carregados com permissões elevadas de uma extensão são exatamente os recursos que você espera e não são substituídos por um invasor de rede ativo.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="ffbdd-150">Como [ataques man-in-the-Middle][WikiManMiddleAttacks] são triviais e não detectáveis por http, essas origens não são aceitas.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="ffbdd-151">Atualmente, os desenvolvedores podem permitir origens da lista com os seguintes esquemas: `blob` , `filesystem` , `https` e `extension` .</span><span class="sxs-lookup"><span data-stu-id="ffbdd-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="ffbdd-152">A parte do host da origem deve ser especificada explicitamente para os `https` `extension` esquemas e.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="ffbdd-153">Caracteres curinga genéricos como https: `https://*` e `https://*.com` não são permitidos; os curingas de subdomínio como `https://*.example.com` são permitidos.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="ffbdd-154">Os domínios na [lista de sufixos públicos][PublicSuffixList] também são exibidos como domínios genéricos de nível superior.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="ffbdd-155">Para carregar um recurso desses domínios, o subdomínio deve estar explicitamente listado.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="ffbdd-156">Por exemplo, `https://*.cloudfront.net` não é válido, mas `https://XXXX.cloudfront.net` é `https://*.XXXX.cloudfront.net` possível ser allowlisted.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be allowlisted.</span></span>  

<span data-ttu-id="ffbdd-157">Para facilitar o desenvolvimento, os recursos carregados pelo HTTP de servidores em seu computador local podem ser allowlisted.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be allowlisted.</span></span>  <span data-ttu-id="ffbdd-158">Você pode permitir o script deList e fontes de objeto em qualquer porta de `http://127.0.0.1` ou `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="ffbdd-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="ffbdd-159">A restrição de recursos carregados via HTTP aplica-se somente a esses recursos que são executados diretamente.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="ffbdd-160">Você ainda é gratuito, por exemplo, para fazer conexões XMLHttpRequest a qualquer origem que desejar; a política padrão não restringe `connect-src` nem qualquer outra política de CSP de maneira alguma.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-160">You are still free, for example, to make XMLHTTPRequest connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="ffbdd-161">Uma definição de política relaxada que permite que os recursos de script sejam carregados de example.com em HTTPS pode parecer com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-161">A relaxed policy definition which allows script resources to be loaded from example.com over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="ffbdd-162">Ambas `script-src` e `object-src` são definidas pela política.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="ffbdd-163">O Microsoft Edge não aceita uma política que não limite cada um desses valores para \ (pelo menos \) ' `self` '.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="ffbdd-164">JavaScript avaliado</span><span class="sxs-lookup"><span data-stu-id="ffbdd-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="ffbdd-165">A política contra `eval()` funções e funções relacionadas `setTimeout(String)` , como, `setInterval(String)` e `new Function(String)` pode ser relaxada adicionando- `unsafe-eval` se à sua política:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="ffbdd-166">No entanto, é altamente recomendável fazer isso.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-166">However, we strongly recommend against doing this.</span></span>  <span data-ttu-id="ffbdd-167">Essas funções são vetores de ataque XSS notories.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-167">These functions are notorious XSS attack vectors.</span></span>  

## <span data-ttu-id="ffbdd-168">Estreitando a política padrão</span><span class="sxs-lookup"><span data-stu-id="ffbdd-168">Tightening the default policy</span></span>  

<span data-ttu-id="ffbdd-169">É claro que você pode diminuir essa política para qualquer ponto que sua extensão permita para aumentar a segurança às custas da conveniência.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="ffbdd-170">Para especificar que sua extensão só poderá carregar recursos de qualquer tipo \ (imagens e assim por diante \) a partir do pacote de extensão associado, por exemplo, uma política de `default-src 'self'` pode ser apropriada.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <span data-ttu-id="ffbdd-171">Scripts de conteúdo</span><span class="sxs-lookup"><span data-stu-id="ffbdd-171">Content Scripts</span></span>  

<span data-ttu-id="ffbdd-172">A política que está sendo abordada se aplica às páginas de plano de fundo e páginas de evento da extensão.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="ffbdd-173">Como os scripts de conteúdo se aplicam aos scripts de conteúdo da extensão são mais complicados.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="ffbdd-174">Os scripts de conteúdo geralmente não estão sujeitos ao CSP da extensão.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="ffbdd-175">Como os scripts de conteúdo não são HTML, o principal impacto disso é que eles podem ser usados `eval` mesmo que o CSP da extensão não `unsafe-eval` seja especificado, embora isso não seja recomendado.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="ffbdd-176">Além disso, o CSP da página não se aplica a scripts de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="ffbdd-177">Mais complicado são `<script>` marcas que os scripts de conteúdo criam e colocam no dom da página em que estão sendo executados.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="ffbdd-178">Elas são referenciadas como scripts injetados DOM em andamento.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="ffbdd-179">Os scripts injetados DOM que são executados imediatamente após a injeção na página são executados como você pode esperar.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="ffbdd-180">Imagine um script de conteúdo com o código a seguir como exemplo simples:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="ffbdd-181">Este script de conteúdo causa um `alert` logo após o `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="ffbdd-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="ffbdd-182">Observe que isso é executado independentemente da política que uma página pode especificar.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="ffbdd-183">No entanto, o comportamento se torna mais complicado tanto dentro daquele DOM injetado do script e para qualquer script que não seja executado imediatamente após a injeção.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="ffbdd-184">Imagine que sua extensão esteja em execução em uma página que fornece um CSP associado que especifica `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="ffbdd-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="ffbdd-185">Agora, imagine que o script de conteúdo execute o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="ffbdd-186">Se um usuário clicar nesse botão, o `onclick` script não será executado.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-186">If a user clicks on that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="ffbdd-187">Isso ocorre porque o script não executou imediatamente e o código não é interpretado até que o evento Click ocorra não seja considerado parte do script de conteúdo, portanto, o CSP da página \ (não da extensão \) restringe o comportamento.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-187">This is because the script did not immediately run and code is not interpreted until the click event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="ffbdd-188">E como esse CSP não especifica `unsafe-inline` , o manipulador de eventos embutido está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="ffbdd-189">A maneira correta de implementar o comportamento desejado nesse caso pode ser adicionar o `onclick` manipulador como uma função do script de conteúdo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="ffbdd-190">Outra questão semelhante ocorrerá se o script de conteúdo executar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="ffbdd-191">Nesse caso, o script é executado e o alerta é exibido.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="ffbdd-192">No entanto, faça este caso:</span><span class="sxs-lookup"><span data-stu-id="ffbdd-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="ffbdd-193">Durante a execução do script inicial, a chamada `eval` será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="ffbdd-194">Ou seja, enquanto o tempo de execução do script inicial é permitido, o comportamento no script é regulamentado pelo CSP da página.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="ffbdd-195">Portanto, dependendo de como você escreve scripts injetados DOM em sua extensão, as alterações no CSP da página podem afetar o comportamento da extensão.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="ffbdd-196">Como os scripts de conteúdo não são afetados pelo CSP da página, isso é um ótimo motivo para colocar o melhor comportamento possível de sua extensão no script de conteúdo, em vez de scripts injetados DOM.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Uma introdução à política de segurança de conteúdo-HTML5 tem"  
[PublicSuffixList]: https://publicsuffix.org/list "EXIBIR A LISTA DE SUFIXOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para \ <script \ > elementos-política de segurança de conteúdo nível 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Política de segurança de conteúdo nível 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque man-in-Middle-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="ffbdd-202">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ffbdd-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ffbdd-203">A página original foi encontrada [aqui](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="ffbdd-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ffbdd-205">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ffbdd-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
