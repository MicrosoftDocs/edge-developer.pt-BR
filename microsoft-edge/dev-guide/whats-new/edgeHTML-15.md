---
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no EdgeHTML 15.
title: O que há de novo no EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: e750a9272bb8bcdb51662839a31cc303c4064ef9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560584"
---
# O que há de novo no EdgeHTML 15
Aqui estão as alterações fornecidas com a versão atual da plataforma Microsoft Edge, a partir da [atualização do Windows 10 para criadores](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (04/2017, Build 15063). Para obter uma visão geral das alterações no navegador geral do Microsoft Edge, confira [novidades no Microsoft Edge na atualização do Windows 10 para criadores](https://blogs.windows.com/msedgedev/2017/04/11/introducing-edgehtml-15/#DrVEvmPU6TPq3tMK.97)

Para alterações nas compilações subsequentes do Windows Insider Preview, confira novidades [no EdgeHTML](../whats-new.md).

Aqui está o link permanente para a seguinte lista de alterações: **[https://aka.ms/devguide_edgehtml_15](https://aka.ms/devguide_edgehtml_15)** .

## Novos recursos

### Propriedades personalizadas de CSS
O Microsoft Edge agora oferece suporte a [Propriedades personalizadas CSS](https://drafts.csswg.org/css-variables/), a. k. a variáveis CSS. As variáveis CSS permitem que você crie propriedades CSS personalizadas que podem ser reutilizadas em todas as folhas de estilos para ajudar a reduzir a quantidade de dados duplicados, como repetidas cores. O uso de variáveis CSS é simples:

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Observador de interseção
EdgeHTML 15 introduz a especificação da [API do observador interseção](https://w3c.github.io/IntersectionObserver/) . A API do observador de interseção permite consultar assincronamente a posição e a visibilidade de elementos DOM em relação a outros elementos ou ao visor global. Essa API elimina a necessidade de código caro personalizado, criando um método para notificar os elementos com eficiência quando eles estiverem em exibição.

### JavaScript

Otimizações de desempenho levam ao estágio Center com o EdgeHTML 15 Rev do mecanismo JavaScript Chakra. Com a atualização do Windows 10 Creators, o chakra salva a memória referindo novamente as funções e otimizando os argumentos de heap e melhora o desempenho do código minified.

Além disso, EdgeHTML 15 introduz as seguintes visualizações de recursos:

#### Recursos experimentais do JavaScript (habilitado com *about: flags*)

* [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) ([demonstração](https://webassembly.org/demo/))
* [Memória compartilhada e Atomicidades](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

Consulte [*melhor desempenho do JavaScript, Webassembly e memória compartilhada no Microsoft Edge*](https://blogs.windows.com/msedgedev/2017/04/20/improved-javascript-performance-webassembly-shared-memory/#t4gwUKjjtdmstMbs.97) para obter mais detalhes.

### API de solicitação de pagamento
Agora há suporte para a [API de solicitação de pagamento](https://w3.org/TR/payment-request/) , permitindo check-out e pagamentos mais simples na Web em computadores e telefones Windows 10. Essa API permite que o Microsoft Edge atue como intermediário entre comerciantes, consumidores e métodos de pagamento (por exemplo, cartões de crédito) que os consumidores armazenaram na nuvem. Para obter mais informações sobre a API de solicitação de pagamento, confira [pagamentos da Web mais simples: apresentando a API de solicitação de pagamento](https://blogs.windows.com/msedgedev/2016/12/15/payment-request-api-edge/) e o guia de desenvolvedor da [API de solicitação de pagamento](/microsoft-edge/dev-guide/device/payment-request-api) .

### TCP Fast Open (TFO)
O TCP Fast Open é um recurso que reduz o número de viagens de ida e outros necessários para abrir uma conexão TCP, melhorando o desempenho da rede do navegador. Para obter mais detalhes, consulte [criando uma Web mais rápida e segura com o TCP Fast aberto](https://blogs.windows.com/msedgedev/2016/06/15/building-a-faster-and-more-secure-web-with-tcp-fast-open-tls-false-start-and-tls-1-3/#eQMauReErmIRXYqh.97). Devido a diferenças de interoperabilidade em várias topologias de rede, esses recursos não são habilitados por padrão no Microsoft Edge. Para habilitá-lo, digite `about:flags` a barra de endereços e marque a caixa de seleção **habilitar TCP Fast abrir** na seção *rede* . 

### Suporte a codecs de vídeo RTC WebRTC e interoperável

O EdgeHTML 15 oferece suporte a um subconjunto da API WebRTC 1,0 para interoperabilidade com aplicativos criados com versões anteriores da API W3C WebRTC-PC circa 2015. Consulte a [referência de API WebRTC](https://msdn.microsoft.com/library/mt806139(v=vs.85).aspx) para obter detalhes.

Para aproveitar os nossos recursos mais avançados em comunicações ponto a ponto de áudio e vídeo, recomendamos usar a API de [comunicação em tempo real do objeto](../realtime-communication/object-rtc-api.md). A API ORTC é mais adequada para situações em que você deseja configurar chamadas de áudio e com vídeo em grupo, ou controlar diretamente objetos de transporte, remetente e receptor individuais.

O Microsoft Edge oferece suporte a H. 264/AVC e VP8 vídeo com ORTC e WebRTC 1,0, e fornece os seguintes recursos para dar suporte aos dois tipos de codec: [ABS-Send-time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time/), [GOOG-remb](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03), [indicação de perda de imagem e comentários de Nack genérico](https://tools.ietf.org/html/rfc4585), [retransmissão de RTP](https://tools.ietf.org/html/rfc4588).

Para obter mais informações, consulte [apresentando o WebRTC 1,0 e comunicações interoperáveis em tempo real no Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31/introducing-webrtc-microsoft-edge/#k8XMeWKyZDQDPYR4.97).

### WebVR

Agora o Microsoft Edge tem suporte para o [WebVR](https://immersive-web.github.io/webxr/), uma API experimental que conecta exibições de cabeçote de realidade mista do Windows e Microsoft Edge. Essa conexão permite que o conteúdo VR seja experiente dentro de um site, o que significa que as experiências de VR de imersão não estão mais limitadas aos aplicativos da área de trabalho.  

A realidade virtual no Microsoft Edge é da plataforma WebGL, uma API JavaScript para renderização de elementos gráficos 3D e 2D. Aplicativos WebGL e aplicativos criados com bibliotecas WebGL como o BabylonJS são suportados. Uma vez conectado, o WebVR envia elementos visuais correspondentes à posição e às informações do sensor em torno do fone de ouvido. A API WebVR também dá suporte a controladores espaciais graças a uma extensão para a [API do gamepad](../dom/gamepad-api.md). Essa API está ativada por padrão, portanto, não é necessário ativar um sinalizador.

Consulte a [referência de API WebVR](https://msdn.microsoft.com/library/mt806281(v=vs.85).aspx) e a [referência de API do gamepad](https://msdn.microsoft.com/library/dn743630(v=vs.85).aspx) para obter detalhes.

 > [!NOTE] 
 > Como a especificação do WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar posteriormente na linha.



## Recursos atualizados

### Política de segurança de conteúdo (nível 2)
Os sites que já usam o CSP 1 devem continuar a funcionar com o suporte do Microsoft Edge para o CSP 2, mas é melhor alternar todas as `frame-src` diretivas que carregam scripts de trabalhador para a nova `child-src` política para manter a obsolescência do seu site. (No CSP 3, `frame-src` não será mais aplicável a trabalhadores.) O CSP 2 também adiciona o seguinte:

1. Novas diretivas: `base-uri` , `child-src` , `form-action` `frame-ancestors` e `plugin-types` . Consulte as [diretrizes de CSP com suporte do Microsoft Edge](../security/content-security-policy.md) para obter mais informações.

2. Suporte a trabalhadores: os scripts de trabalhador em segundo plano são regidos por sua própria política, separados da política do documento que os carrega. Assim como com os documentos do host, você pode definir o CSP para um trabalhador no cabeçalho de resposta. Além disso, novo no CSP 2 é que `allow-scripts` e `allow-same-origin` os sinalizadores da `sandbox` diretiva agora afetam a criação de threads de trabalho.

3. Scripts e estilos embutidos: o CSP 2 permite a execução de blocos de estilo e scripts embutidos fornecendo nonces e hashes como um mecanismo de lista branca. Os nonces são valores base aleatórios-64 gerados em cada carga de página que aparece na política de CSP e nas marcas de script na página. Quando a página é gerada dinamicamente na carga, o servidor gera um valor de nonce, a insere no NonceToken na página e também a declara no cabeçalho HTTP da política de segurança de conteúdo. Hashes são valores estáticos gerados (por meio de algoritmos *SHA256*, *Sha384* ou *SHA512* ) do conteúdo de um `<script>` `<style>` elemento or que são especificados (por meio de `script-src` ou `style-src` diretivas) na política de CSP.

4. Relatório de violação de CSP: um novo evento, o SecurityPolicyViolationEvent agora é disparado nas violações do CSP. O mecanismo anterior para relatórios do CSP, `report-uri` continua a ser compatível. Vários novos campos foram adicionados aos relatórios de violação comuns a ambos, incluindo `effectiveDirective` (a política que foi violada), `statusCode` (o código de resposta http) `sourceFile` (a URL do recurso incorreto), `lineNumber` e `columnNumber` .

### Autenticação da Web
O suporte do Microsoft Edge para a [API de autenticação da Web](../device/web-authentication.md) emergente que usa a biometria do [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) foi atualizado com as seguintes alterações:
- A implementação inicial da API de autenticação da Web experimental introduzida no [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14/#TVSCzKDkG4jCI5mt.97) (atualização de aniversário do Windows 10, compilação 10240, 7/2016) foi exposta por meio de APIs prefixadas da MS (a interface [MSCredentials](https://msdn.microsoft.com/library/mt697639) ). Embora essas APIs ainda estejam disponíveis no EdgeHTML 15, elas agora são preteridas em favor das APIs e comportamentos não predefinidos e baseados em padrões definidos em um [instantâneo mais recente](https://w3.org/TR/2016/WD-webauthn-20160928) da especificação e provavelmente continuarão mudando à medida que a especificação for desenvolvida para a padronização.

- A última implementação do Microsoft Edge é desativada por padrão e é enviada atrás de um sinalizador (tipo `about:flags` na barra de endereços para ativar o recurso).

- O Microsoft Edge ainda não dá suporte a credenciais externas, como chaves USB ou dispositivos Bluetooth. A API atual limita-se a credenciais inseridas armazenadas no TPM. Um fallback de software será usado se o TPM não estiver disponível no dispositivo.

- A conta de usuário do Windows atualmente conectada deve ser configurada para dar suporte a pelo menos um PIN, e preferencialmente diante ou biometria de impressão digital. Isso é para garantir que o Windows possa autenticar o acesso ao TPM.

- Das [extensões predefinidas](https://w3.org/TR/webauthn/#extension-predef) descritas na espec, o Microsoft Edge só oferece suporte ao [Fido AppID](https://w3.org/TR/webauthn/#extension-appid) ( `webauthn_txAuthSimple` ) no momento.

- A `timeoutSeconds` opção não é avaliada no momento

### WebDriver

O EdgeHTML 15 traz algumas atualizações para o WebDriver, incluindo suporte para o sinalizador de linha de comando silencioso e novos pontos de extremidade de comando:

Método | Modelo de URI | Comando
:----- | :----------  | :--------
POST | ID do/Session/{Session}/Alert/Accept | [Aceitar alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert)
POST | ID do/Session/{Session}/Alert/dismiss | [Ignorar alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert)
GET | ID do/Session/{Session}/Alert/Text | [Obter texto de alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text)
POST | ID do/Session/{Session}/Alert/Text | [Enviar texto de alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text)
POST | ID do/Session/{Session}/execute/Async | [Executar um script assíncrono](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script)
POST | ID do/Session/{Session}/execute/Sync | [Executar script](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script)
GET | ID do/Session/{Session}/Window | [Obter identificador de janela](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle)
GET | ID do/Session/{Session}/Window/Handles | [Obter identificadores de janela](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles)

Para obter mais informações e o status de outros recursos do WebDriver, confira o [WebDriver](../../webdriver.md).

## Novas APIs no EdgeHTML 15

Aqui está a lista completa de novas APIs no EdgeHTML 15. Elas são listadas no formato **[nome da interface]. [ nome da API]**.

<iframe height='582' scrolling='no' title='Novas APIs EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Veja a caneta <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> New EdgeHTML15 APIs </a> by Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Versões anteriores do EdgeHTML
[EdgeHTML 12/Build do Windows 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)

[EdgeHTML 13/Build do Windows 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Build do Windows 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)
