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
# <a name="content-security-policy-csp"></a>Política de Segurança de Conteúdo \(CSP\)  

Para reduzir uma grande classe de possíveis problemas de script entre sites, o sistema de Extensão do Microsoft Edge incorporou o conceito geral de Política de Segurança de Conteúdo [\(CSP\)][W3CContentSecurityPolicy].  Isso introduz algumas políticas bastante estritas que fazem extensões mais seguras por padrão e fornece a você a capacidade de criar e impor regras que regem os tipos de conteúdo que podem ser carregados e executados por suas Extensões e aplicativos.  

Em geral, o CSP funciona como um mecanismo de bloqueio/lista de recursos carregados ou executados por suas Extensões.  A definição de uma política razoável para o Extension permite que você considere cuidadosamente os recursos necessários para o Extension e peça ao navegador para garantir que esses sejam os únicos recursos aos quais o Extension tem acesso.  As políticas fornecem segurança acima e acima das permissões de host que suas solicitações de Extensão; eles são uma camada adicional de proteção, não uma substituição.  

Na Web, essa política é definida por meio de um cabeçalho HTTP ou `meta` elemento.  Dentro do sistema de Extensão do Microsoft Edge, nenhum deles é um mecanismo apropriado.  Em vez disso, uma política de Extensão é definida usando `manifest.json` o arquivo para o Extension da seguinte forma:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Para obter detalhes completos sobre a sintaxe do CSP, confira a especificação da Política de Segurança de Conteúdo [e][W3CContentSecurityPolicy] o artigo "Introdução à Política de Segurança de [Conteúdo"][HTML5RocksIntroductionContentSecurityPolicy] em HTML5Rocks.  

## <a name="default-policy-restrictions"></a>Restrições de política padrão  

Pacotes que não definem um `manifest_version` não têm uma política de segurança de conteúdo padrão.  Os pacotes que escolherem 2 têm uma política de segurança de `manifest_version` conteúdo padrão a seguir.  

```javascript
script-src 'self'; object-src 'self'
```  

A política adiciona segurança limitando extensões e aplicativos de três maneiras:  

**Funções relacionadas e de avaliação estão desabilitadas**  

Código como o seguinte não funciona:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Avaliar cadeias de caracteres de JavaScript como esta é um vetor de ataque XSS comum.  Em vez disso, você deve escrever código como:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**JavaScript embutido não são executados**  

JavaScript embutido não são executados.  Essa restrição proíbe blocos em linha e manipuladores de eventos em `<script>` linha, como `<button onclick="...">` .

A primeira restrição apaga uma classe enorme de ataques de script entre sites, tornando impossível executar acidentalmente o script fornecido por um terceiro mal-intencionado.  No entanto, ele exige que você escreva seu código com uma separação limpa entre o conteúdo e o comportamento \(o que você deve fazer de qualquer maneira, certo?\).  Um exemplo pode deixar isso mais claro.  Você pode tentar gravar um pop-up de Ação do Navegador como um único `pop-up.html` que contenha:  

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

Três coisas devem mudar para que isso funcione da maneira esperada:  

*   A `clickHandler` definição deve ser movida para um arquivo JavaScript externo \( `popup.js` pode ser um bom destino).  
*   As definições de manipulador de eventos em linha devem ser reescritas em termos de `addEventListener` e extraídas em `popup.js` .  
    Se você estiver iniciando seu programa usando código como , considere substituí-lo por conectar-se ao evento do documento ou ao evento da `<body onload="main();">` `DOMContentLoaded` janela, dependendo de seus `load` requisitos.  Use o primeiro, já que geralmente dispara mais rapidamente.  

*   A `setTimeout` chamada deve ser regravada para evitar converter a cadeia de `"awesome(); totallyAwesome()"` caracteres em JavaScript para execução.  
    Essas alterações podem ter a seguinte aparência:  

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

**Somente os recursos de script e objeto locais são carregados**  

Os recursos de script e objeto só podem ser carregados do pacote extension, e não da Web em geral.  Isso garante que o Extension só executa o código aprovado especificamente, impedindo que um invasor ativo de rede redirecione mal-intencionadamente sua solicitação para um recurso.  

Em vez de escrever um código que dependa do carregamento de jQuery \(ou qualquer outra biblioteca\) de uma CDN externa, considere incluir a versão específica do jQuery em seu pacote de Extensão.  Ou seja, em vez de:  

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

Baixe o arquivo, inclua-o no pacote e escreva:  

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

## <a name="relaxing-the-default-policy"></a>Descontrair a política padrão  

**Script em linha**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Scripts embutida podem ser permitidos especificando o hash codificado com base64 do código-fonte na política.  Esse hash deve ser prefixado pelo algoritmo de hash usado \(sha256, sha384 ou sha512\).  Por exemplo, navegue até [Hash para uso de \<script\> elementos][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].  

**Script Remoto**  

Se você precisar de alguns recursos externos de JavaScript ou de objeto, você poderá descontrair a política em uma extensão limitada, permitindo listar origens seguras das quais os scripts devem ser aceitos.  Verifique se os recursos de tempo de execução carregados com permissões elevadas de um Extension são exatamente os recursos esperados e não são substituídos por um invasor de rede ativo.  Como [os ataques man-in-the-middle][WikiManMiddleAttacks] são triviais e indetectáveis em HTTP, essas origens não são aceitas.  

Atualmente, os desenvolvedores são capazes de permitir origens de lista com os seguintes esquemas: `blob` `filesystem` , , e `https` `extension` .  A parte host da origem deve ser explicitamente especificada para `https` os `extension` esquemas e.  Caracteres curinga genéricos, como https:, e não são permitidos; caracteres curinga `https://*` de `https://*.com` subdomínio, como `https://*.example.com` são permitidos.  Domínios na lista [Sufixo][PublicSuffixList] Público também são exibidos como domínios genéricos de nível superior.  Para carregar um recurso desses domínios, o subdomínio deve ser listado explicitamente.  Por exemplo, `https://*.cloudfront.net` não é válido, `https://XXXX.cloudfront.net` mas é capaz de ser `https://*.XXXX.cloudfront.net` `allowlisted` .  

Para facilitar o desenvolvimento, os recursos carregados por HTTP de servidores em sua máquina local podem ser `allowlisted` .  Você pode permitir fontes de script e objeto de lista em qualquer porta de `http://127.0.0.1` um ou `http://localhost` .  

> [!NOTE]
> A restrição contra recursos carregados por HTTP se aplica somente aos recursos que são executados diretamente.  Você ainda está livre, por exemplo, para fazer conexões com qualquer origem que você quiser; a política padrão não restringe ou qualquer uma das outras `XMLHTTPRequest` `connect-src` diretivas CSP de qualquer maneira.  

Uma definição de política descontraída que permite que os recursos de script sejam carregados por `example.com` meio de HTTPS pode ter a aparência:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Ambos `script-src` e `object-src` são definidos pela política.  O Microsoft Edge não aceita uma política que não limita cada um desses valores a \(pelo menos\) ' `self` '.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript avaliado**  

A política contra e funções relacionadas, como , e são capazes de ser descontraídas `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` adicionando `unsafe-eval` à sua política:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

No entanto, você deve evitar políticas de descontração.  As funções são vetores de ataque XSS notórios.  

## <a name="tightening-the-default-policy"></a>Apertar a política padrão  

Você pode, é claro, apertar essa política em qualquer medida que o Extension permita para aumentar a segurança às custas de conveniência.  Para especificar que o Extension só pode carregar recursos de qualquer tipo \(imagens e assim por diante\) do pacote de Extensão associado, por exemplo, uma política de pode ser `default-src 'self'` apropriada.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a>Scripts de conteúdo  

A política que está sendo discutida se aplica às páginas em segundo plano e às páginas de eventos do Extension.  A forma como os scripts de conteúdo se aplicam aos scripts de conteúdo do Extension é mais complicada.  

Scripts de conteúdo geralmente não estão sujeitos ao CSP da Extensão.  Como os scripts de conteúdo não são HTML, o principal impacto disso é que eles podem usar mesmo que o CSP do Extension não especifique , embora isso não `eval` `unsafe-eval` seja recomendado.  Além disso, o CSP da página não se aplica a scripts de conteúdo.  Mais complicadas são `<script>` as marcas que os scripts de conteúdo criam e colocam no DOM da página em que estão sendo executados.  Eles são referenciados como scripts injetados dom no futuro.  

Scripts injetados dom que são executados imediatamente após a injeção na página são executados como você pode esperar.  Imagine um script de conteúdo com o seguinte código como um exemplo simples:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Esse script de conteúdo causa `alert` um imediatamente sobre o `document.write()` .  Observe que isso é executado independentemente da política que uma página pode especificar.
No entanto, o comportamento se torna mais complicado dentro desse script injetado dom e para qualquer script que não seja executado imediatamente após a injeção.  Imagine que o Extension está sendo executado em uma página que fornece um CSP associado que especifica `script-src 'self'` .  Agora, imagine que o script de conteúdo executa o seguinte código:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Se um usuário escolher esse botão, `onclick` o script não será executado.  Isso ocorre porque o script não foi executado imediatamente e o código não é interpretado até que o evento ocorra não seja considerado parte do script de conteúdo, portanto, o CSP da página \(não do Extension\) restringe o `click` comportamento.  E como esse CSP não especifica , o manipulador de eventos em `unsafe-inline` linha é bloqueado.  
A maneira correta de implementar o comportamento desejado nesse caso pode ser adicionar o manipulador como uma função do script de `onclick` conteúdo da seguinte maneira:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Outro problema semelhante ocorrerá se o script de conteúdo executa o seguinte:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

Nesse caso, o script é executado e o alerta é exibido.  No entanto, leve este caso:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Enquanto o script inicial é executado, a chamada `eval` é bloqueada.  Ou seja, embora o tempo de execução do script inicial seja permitido, o comportamento dentro do script é regulado pelo CSP da página.  
Assim, dependendo de como você escreve scripts injetados dom em sua Extensão, as alterações no CSP da página podem afetar o comportamento de sua Extensão.  Como os scripts de conteúdo não são afetados pelo CSP da página, esse é um ótimo motivo para colocar o máximo de comportamento possível de sua Extensão no script de conteúdo, em vez de scripts injetados dom.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Uma introdução à política de segurança de conteúdo | Html5 Rochas"  
[PublicSuffixList]: https://publicsuffix.org/list "EXIBIR A LISTA DE SUFIXOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para \<script\> elementos - Nível de Política de Segurança de Conteúdo 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Nível 3 da Política de Segurança de Conteúdo | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque man-in-the-middle | Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
