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
# Política de segurança de conteúdo \ (CSP \)  

Para reduzir uma grande classe de problemas potenciais de script entre sites, o sistema de extensão do Microsoft Edge incorporou o conceito geral da política de [segurança de conteúdo \ (CSP \)][W3CContentSecurityPolicy].  Isso introduz algumas políticas bastante rigorosas que tornam as extensões mais seguras por padrão e oferece a capacidade de criar e impor regras que regem os tipos de conteúdo que podem ser carregados e executados por suas extensões e aplicativos.  

Em geral, o CSP funciona como um mecanismo de blocos/allowlisting para recursos carregados ou executados por suas extensões.  Definir uma política razoável para sua extensão permite que você considere cuidadosamente os recursos que sua extensão requer e para solicitar que o navegador Verifique se esses são os únicos recursos aos quais sua extensão tem acesso.  Essas políticas fornecem segurança e, acima das permissões de host, suas solicitações de extensão; Eles são uma camada adicional de proteção, e não um substituto.  

Na Web, essa política é definida por meio de um cabeçalho ou `meta` elemento http.  Dentro do sistema de extensão do Microsoft Edge, nenhum deles é um mecanismo apropriado.  Em vez disso, uma política de extensão é definida pelo `manifest.json` arquivo para a extensão da seguinte maneira:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Para obter detalhes completos sobre a sintaxe do CSP, confira a [especificação da política de segurança de conteúdo][W3CContentSecurityPolicy] e o artigo ["introdução à política de segurança de conteúdo"][HTML5RocksIntroductionContentSecurityPolicy] em HTML5Rocks.  

## Restrições de política padrão  

Os pacotes que não definem a não `manifest_version` têm uma política de segurança de conteúdo padrão.  Aqueles que selecionarem `manifest_version` 2 têm uma política de segurança de conteúdo padrão de:  

```javascript
script-src 'self'; object-src 'self'
```  

Essa política adiciona segurança limitando extensões e aplicativos de três maneiras:  

**As funções evals e relacionadas estão desabilitadas**  

Um código como o seguinte não funciona:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Avaliar cadeias de caracteres de JavaScript como esse é um vetor de ataque XSS comum.  Em vez disso, você deve escrever um código como:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**JavaScript embutido não são executados**  

JavaScript embutido não são executados.  Essa restrição Bans os blocos embutidos `<script>` e manipuladores de eventos embutidos, como `<button onclick="...">` .

A primeira restrição apaga uma enorme classe de ataques de script entre sites impossibilitando que você execute acidentalmente o script fornecido por um terceiro mal-intencionado.  No entanto, ele exige que você escreva o código com uma separação de limpeza entre conteúdo e comportamento \ (o que você deve fazer é, certo? \).  Um exemplo pode deixar isso mais claro.  Você pode tentar escrever um pop-up de ação do navegador como um único `pop-up.html` contendo:  

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

Três itens devem mudar para que isso funcione da maneira esperada:  

*   A `clickHandler` definição deve ser movida para um arquivo JavaScript externo \ ( `popup.js` pode ser um bom alvo).  
*   As definições do manipulador de eventos embutidas devem ser regravadas em termos de `addEventListener` e extraídos para `popup.js` .  
    Se, no momento, você iniciar o programa usando um código como `<body onload="main();">` , considere substituí-lo ao se conectar ao `DOMContentLoaded` evento do documento ou ao `load` evento da janela, dependendo dos seus requisitos.  Use o primeiro, uma vez que ele geralmente é acionado mais rapidamente.  

*   A `setTimeout` chamada deve ser reescrita para evitar converter a cadeia de caracteres `"awesome(); totallyAwesome()"` em JavaScript para execução.  
    Essas alterações podem ter uma aparência semelhante à seguinte:  

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

**Somente recursos locais de script e de objeto são carregados**  

Recursos de script e de objeto só podem ser carregados do pacote de extensão, e não da Web, em grande parte.  Isso garante que sua extensão execute apenas o código que você aprovou especificamente, evitando que um invasor de rede ativo redirecione sua solicitação para um recurso de maneira maliciosa.  

Em vez de escrever código que dependa do jQuery \ (ou de qualquer outra biblioteca \) carregando de uma CDN externa, considere a inclusão da versão específica do jQuery em seu pacote de extensão.  Ou seja, em vez de:  

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

## Relaxar a política padrão  

**Script embutido**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Scripts embutidos podem ser permitidos especificando o hash codificado em base64 do código-fonte na política.  Esse hash deve ser prefixado pelo algoritmo de hash usado \ (SHA256, Sha384 ou SHA512 \).  Consulte o [uso de hash para os elementos \ <script \ >][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] para obter um exemplo.  

**Script remoto**  

Se você precisar de alguns recursos externos de JavaScript ou de objetos, pode relaxar a política para uma extensão limitada allowlisting proteger as origens de quais scripts devem ser aceitos.  Verifique se os recursos de tempo de execução carregados com permissões elevadas de uma extensão são exatamente os recursos que você espera e não são substituídos por um invasor de rede ativo.  Como [ataques man-in-the-Middle][WikiManMiddleAttacks] são triviais e não detectáveis por http, essas origens não são aceitas.  

Atualmente, os desenvolvedores podem permitir origens da lista com os seguintes esquemas: `blob` , `filesystem` , `https` e `extension` .  A parte do host da origem deve ser especificada explicitamente para os `https` `extension` esquemas e.  Caracteres curinga genéricos como https: `https://*` e `https://*.com` não são permitidos; os curingas de subdomínio como `https://*.example.com` são permitidos.  Os domínios na [lista de sufixos públicos][PublicSuffixList] também são exibidos como domínios genéricos de nível superior.  Para carregar um recurso desses domínios, o subdomínio deve estar explicitamente listado.  Por exemplo, `https://*.cloudfront.net` não é válido, mas `https://XXXX.cloudfront.net` é `https://*.XXXX.cloudfront.net` possível ser allowlisted.  

Para facilitar o desenvolvimento, os recursos carregados pelo HTTP de servidores em seu computador local podem ser allowlisted.  Você pode permitir o script deList e fontes de objeto em qualquer porta de `http://127.0.0.1` ou `http://localhost` .  

> [!NOTE]
> A restrição de recursos carregados via HTTP aplica-se somente a esses recursos que são executados diretamente.  Você ainda é gratuito, por exemplo, para fazer conexões XMLHttpRequest a qualquer origem que desejar; a política padrão não restringe `connect-src` nem qualquer outra política de CSP de maneira alguma.  

Uma definição de política relaxada que permite que os recursos de script sejam carregados de example.com em HTTPS pode parecer com o seguinte:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Ambas `script-src` e `object-src` são definidas pela política.  O Microsoft Edge não aceita uma política que não limite cada um desses valores para \ (pelo menos \) ' `self` '.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript avaliado**  

A política contra `eval()` funções e funções relacionadas `setTimeout(String)` , como, `setInterval(String)` e `new Function(String)` pode ser relaxada adicionando- `unsafe-eval` se à sua política:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

No entanto, é altamente recomendável fazer isso.  Essas funções são vetores de ataque XSS notories.  

## Estreitando a política padrão  

É claro que você pode diminuir essa política para qualquer ponto que sua extensão permita para aumentar a segurança às custas da conveniência.  Para especificar que sua extensão só poderá carregar recursos de qualquer tipo \ (imagens e assim por diante \) a partir do pacote de extensão associado, por exemplo, uma política de `default-src 'self'` pode ser apropriada.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## Scripts de conteúdo  

A política que está sendo abordada se aplica às páginas de plano de fundo e páginas de evento da extensão.  Como os scripts de conteúdo se aplicam aos scripts de conteúdo da extensão são mais complicados.  

Os scripts de conteúdo geralmente não estão sujeitos ao CSP da extensão.  Como os scripts de conteúdo não são HTML, o principal impacto disso é que eles podem ser usados `eval` mesmo que o CSP da extensão não `unsafe-eval` seja especificado, embora isso não seja recomendado.  Além disso, o CSP da página não se aplica a scripts de conteúdo.  Mais complicado são `<script>` marcas que os scripts de conteúdo criam e colocam no dom da página em que estão sendo executados.  Elas são referenciadas como scripts injetados DOM em andamento.  

Os scripts injetados DOM que são executados imediatamente após a injeção na página são executados como você pode esperar.  Imagine um script de conteúdo com o código a seguir como exemplo simples:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Este script de conteúdo causa um `alert` logo após o `document.write()` .  Observe que isso é executado independentemente da política que uma página pode especificar.
No entanto, o comportamento se torna mais complicado tanto dentro daquele DOM injetado do script e para qualquer script que não seja executado imediatamente após a injeção.  Imagine que sua extensão esteja em execução em uma página que fornece um CSP associado que especifica `script-src 'self'` .  Agora, imagine que o script de conteúdo execute o seguinte código:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Se um usuário clicar nesse botão, o `onclick` script não será executado.  Isso ocorre porque o script não executou imediatamente e o código não é interpretado até que o evento Click ocorra não seja considerado parte do script de conteúdo, portanto, o CSP da página \ (não da extensão \) restringe o comportamento.  E como esse CSP não especifica `unsafe-inline` , o manipulador de eventos embutido está bloqueado.  
A maneira correta de implementar o comportamento desejado nesse caso pode ser adicionar o `onclick` manipulador como uma função do script de conteúdo da seguinte maneira:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Outra questão semelhante ocorrerá se o script de conteúdo executar o seguinte:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

Nesse caso, o script é executado e o alerta é exibido.  No entanto, faça este caso:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Durante a execução do script inicial, a chamada `eval` será bloqueada.  Ou seja, enquanto o tempo de execução do script inicial é permitido, o comportamento no script é regulamentado pelo CSP da página.  
Portanto, dependendo de como você escreve scripts injetados DOM em sua extensão, as alterações no CSP da página podem afetar o comportamento da extensão.  Como os scripts de conteúdo não são afetados pelo CSP da página, isso é um ótimo motivo para colocar o melhor comportamento possível de sua extensão no script de conteúdo, em vez de scripts injetados DOM.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Uma introdução à política de segurança de conteúdo-HTML5 tem"  
[PublicSuffixList]: https://publicsuffix.org/list "EXIBIR A LISTA DE SUFIXOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para \ <script \ > elementos-política de segurança de conteúdo nível 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Política de segurança de conteúdo nível 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque man-in-Middle-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
