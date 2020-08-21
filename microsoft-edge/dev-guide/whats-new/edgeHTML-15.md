---
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no EdgeHTML 15.
title: Novos recursos e APIs no EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: 4febe4be1fce29207de7a57b61d96eae0a5c02ab
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941924"
---
# O que há de novo no EdgeHTML 15  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Aqui estão as alterações fornecidas com a versão atual da plataforma Microsoft Edge, a partir da [atualização do Windows 10 Creators](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) \ (04/2017, Build 15063 \).  Para obter uma visão geral das alterações no navegador geral do Microsoft Edge, confira [novidades do Microsoft Edge na atualização do Windows 10 para criadores](https://blogs.windows.com/msedgedev/2017/04/11).  

Para alterações nas compilações subsequentes do Windows Insider Preview, confira novidades [no EdgeHTML](../whats-new.md).  

Aqui está o link permanente para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_15](./edgehtml-15.md) .  

## Novos recursos  

### Propriedades personalizadas de CSS  

O Microsoft Edge agora oferece suporte a [Propriedades personalizadas CSS](https://drafts.csswg.org/css-variables), a. k. a variáveis CSS.  As variáveis CSS permitem que você crie propriedades CSS personalizadas que podem ser reutilizadas em todas as folhas de estilos para ajudar a reduzir a quantidade de dados duplicados, como repetidas cores.  O uso de variáveis CSS é simples:  

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

EdgeHTML 15 introduz a especificação da [API do observador interseção](https://w3c.github.io/IntersectionObserver) .  A API do observador de interseção permite consultar assincronamente a posição e a visibilidade de elementos DOM em relação a outros elementos ou ao visor global.  Essa API elimina a necessidade de código caro personalizado, criando um método para notificar os elementos com eficiência quando eles estiverem em exibição.  

### JavaScript  

Otimizações de desempenho levam ao estágio Center com o EdgeHTML 15 Rev do mecanismo JavaScript Chakra.  Com a atualização do Windows 10 Creators, o chakra salva a memória referindo novamente as funções e otimizando os argumentos de heap e melhora o desempenho do código minified.  

Além disso, EdgeHTML 15 introduz as seguintes visualizações de recursos:  

#### Recursos de JavaScript experimental  

Habilitado com `about:flags`  

*   [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) \ ([demonstração](https://webassembly.org/demo)\)  
*   [Memória compartilhada e Atomicidades](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

Consulte [melhor desempenho do JavaScript, Webassembly e memória compartilhada no Microsoft Edge](https://blogs.windows.com/msedgedev/2017/04/20) para obter mais detalhes.  

### API da Solicitação de Pagamento  

Agora há suporte para a [API de solicitação de pagamento](https://w3.org/TR/payment-request) , permitindo check-out e pagamentos mais simples na Web em computadores e telefones Windows 10.  Essa API permite que o Microsoft Edge atue como intermediário entre comerciantes, consumidores e métodos de pagamento \ (como cartões de crédito \) que os consumidores armazenaram na nuvem.  Para obter mais informações sobre a API de solicitação de pagamento, confira [pagamentos da Web mais simples: apresentando a API de solicitação de pagamento](https://blogs.windows.com/msedgedev/2016/12/15) e o guia de desenvolvedor da [API de solicitação de pagamento](/microsoft-edge/dev-guide/device/payment-request-api) .  

### TCP Fast Open (TFO)  
O TCP Fast Open é um recurso que reduz o número de viagens de ida e outros necessários para abrir uma conexão TCP, melhorando o desempenho da rede do navegador.  Para obter mais detalhes, consulte [criando uma Web mais rápida e segura com o TCP Fast aberto](https://blogs.windows.com/msedgedev/2016/06/15).  Devido a diferenças de interoperabilidade em várias topologias de rede, esses recursos não são habilitados por padrão no Microsoft Edge.  Para habilitá-lo, digite `about:flags` a barra de endereços e marque a caixa de seleção **habilitar TCP Fast abrir** na seção **rede** .  

### Suporte a codecs de vídeo RTC WebRTC e interoperável  

O EdgeHTML 15 oferece suporte a um subconjunto da API WebRTC 1,0 para interoperabilidade com aplicativos criados com versões anteriores da API W3C WebRTC-PC circa 2015.  Consulte a [referência de API WebRTC](/previous-versions//mt806139(v=vs.85)) para obter detalhes.  

Para aproveitar os nossos recursos mais avançados em comunicações ponto a ponto de áudio e vídeo, recomendamos usar a API de [comunicação em tempo real do objeto](https://ortc.org).  A API ORTC é mais adequada para situações em que você deseja configurar chamadas de áudio e com vídeo em grupo, ou controlar diretamente objetos de transporte, remetente e receptor individuais.  

O Microsoft Edge oferece suporte a H. 264/AVC e VP8 vídeo com ORTC e WebRTC 1,0, e fornece os seguintes recursos para dar suporte aos dois tipos de codec: [ABS-Send-time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time), [GOOG-remb](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03), [indicação de perda de imagem e comentários de Nack genérico](https://tools.ietf.org/html/rfc4585), [retransmissão de RTP](https://tools.ietf.org/html/rfc4588).  

Para obter mais informações, consulte [apresentando o WebRTC 1,0 e comunicações interoperáveis em tempo real no Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31).  

### WebVR  

Agora o Microsoft Edge tem suporte para o [WebVR](https://immersive-web.github.io/webxr), uma API experimental que conecta exibições de cabeçote de realidade mista do Windows e Microsoft Edge.  Essa conexão permite que o conteúdo VR seja experiente dentro de um site, o que significa que as experiências de VR de imersão não estão mais limitadas aos aplicativos da área de trabalho.  

A realidade virtual no Microsoft Edge é da plataforma WebGL, uma API JavaScript para renderização de elementos gráficos 3D e 2D.  Aplicativos WebGL e aplicativos criados com bibliotecas WebGL como o BabylonJS são suportados.  Uma vez conectado, o WebVR envia elementos visuais correspondentes à posição e às informações do sensor em torno do fone de ouvido.  A API WebVR também dá suporte a controladores espaciais graças a uma extensão para a [API do gamepad](../dom/gamepad-api.md).  Essa API está ativada por padrão, portanto, não é necessário ativar um sinalizador.  

Consulte a [referência de API WebVR](/previous-versions//mt806281(v=vs.85)) e a [referência de API do gamepad](https://developer.mozilla.org/docs/Web/API/Gamepad_API) para obter detalhes.  

 > [!NOTE] 
 > Como a especificação do WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar posteriormente na linha.  

## Recursos atualizados  

### Política de segurança de conteúdo (nível 2)  

Os sites que já usam o CSP 1 devem continuar a funcionar com o suporte do Microsoft Edge para o CSP 2, mas é melhor alternar todas as `frame-src` diretivas que carregam scripts de trabalhador para a nova `child-src` política para manter a obsolescência do seu site.  \ (No CSP 3, `frame-src` não será mais aplicável a trabalhadores. \) o CSP 2 também adiciona o seguinte:  

:::row:::
   :::column span="1":::
      Novas diretivas  
   :::column-end:::
   :::column span="2":::
      `base-uri`, `child-src` , `form-action` `frame-ancestors` e `plugin-types` .  Consulte as [diretrizes de CSP com suporte do Microsoft Edge](../security/content-security-policy.md) para obter mais informações.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Suporte a trabalhadores  
   :::column-end:::
   :::column span="2":::
      Os scripts do trabalho em segundo plano são regidos pela própria política, separados da política do documento que os carrega.  Assim como com os documentos do host, você pode definir o CSP para um trabalhador no cabeçalho de resposta.  Além disso, novo no CSP 2 é que  `allow-scripts` e `allow-same-origin` os sinalizadores da `sandbox` diretiva agora afetam a criação de threads de trabalho.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Estilos e scripts embutidos  
   :::column-end:::
   :::column span="2":::
      O CSP 2 permite a execução de scripts embutidos e blocos de estilo ao fornecer nonces e hashes como um mecanismo de lista branca.  Os nonces são valores base aleatórios-64 gerados em cada carga de página que aparece na política de CSP e nas marcas de script na página.  Quando a página é gerada dinamicamente na carga, o servidor gera um valor de nonce, a insere no NonceToken na página e também a declara no cabeçalho HTTP da política de segurança de conteúdo.  Hashes são valores estáticos gerados \ (via SHA256, Sha384 ou algoritmos SHA512 \) a partir do conteúdo de um `<script>` `<style>` elemento or que são especificados \ (via `script-src` ou `style-src` Diretivas \) na política de CSP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Relatório de violação de CSP  
   :::column-end:::
   :::column span="2":::
      Um novo evento, `SecurityPolicyViolationEvent` agora é disparado nas violações do CSP.  O mecanismo anterior para relatórios do CSP, `report-uri` continua a ser compatível.  Vários novos campos foram adicionados aos relatórios de violação comuns a ambos, incluindo `effectiveDirective` \ (a política que foi violada \), `statusCode` \ (o código de resposta http \), `sourceFile` \ (a URL do recurso incorreto \), `lineNumber` e `columnNumber` .  
   :::column-end:::
:::row-end:::  

### Autenticação Web  

O suporte do Microsoft Edge para a [API de autenticação da Web](../device/web-authentication.md) emergente que usa a biometria do [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) foi atualizado com as seguintes alterações:  

*   A implementação inicial da API de autenticação da Web experimental introduzida no [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04) \ (atualização de aniversário do Windows 10, Build 10240, 7/2016 \) foi exposta por meio das APIs prefixadas da MS \ (a interface [MSCredentials](/previous-versions//mt697639(v=vs.85)) \).  Embora essas APIs ainda estejam disponíveis no EdgeHTML 15, elas agora são preteridas em favor das APIs e comportamentos não predefinidos e baseados em padrões definidos em um [instantâneo mais recente](https://w3.org/TR/2016/WD-webauthn-20160928) da especificação e provavelmente continuarão mudando à medida que a especificação for desenvolvida para a padronização.  

*   A última implementação do Microsoft Edge é desativada por padrão e é enviada atrás de um sinalizador \ (digite a `about:flags` barra de endereços para ativar o recurso \).  

*   O Microsoft Edge ainda não dá suporte a credenciais externas, como chaves USB ou dispositivos Bluetooth.  A API atual limita-se a credenciais inseridas armazenadas no TPM.  Um fallback de software será usado se o TPM não estiver disponível no dispositivo.  

*   A conta de usuário do Windows atualmente conectada deve ser configurada para dar suporte a pelo menos um PIN, e preferencialmente diante ou biometria de impressão digital.  Isso é para garantir que o Windows possa autenticar o acesso ao TPM.  

*   Das [extensões predefinidas](https://w3.org/TR/webauthn/#extension-predef) descritas na espec, o Microsoft Edge só oferece suporte ao [Fido AppID](https://w3.org/TR/webauthn/#extension-appid) \ ( `webauthn_txAuthSimple` \) no momento.  

*  A `timeoutSeconds` opção não é avaliada no momento  

### WebDriver  

O EdgeHTML 15 traz algumas atualizações para o WebDriver, incluindo suporte para o sinalizador de linha de comando silencioso e novos pontos de extremidade de comando:  

| Método | Modelo de URI | Comando |  
|:--- |:---  |:--- |    
| POST | ID do/Session/{Session}/Alert/Accept | [Aceitar alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert) |  
| POST | ID do/Session/{Session}/Alert/dismiss | [Ignorar alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert) |  
| GET | ID do/Session/{Session}/Alert/Text | [Obter texto de alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text) |  
| POST | ID do/Session/{Session}/Alert/Text | [Enviar texto de alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text) |  
| POST | ID do/Session/{Session}/execute/Async | [Executar um script assíncrono](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script) |  
| POST | ID do/Session/{Session}/execute/Sync | [Executar script](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script) |  
| GET | ID do/Session/{Session}/Window | [Obter identificador de janela](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle) |  
| GET | ID do/Session/{Session}/Window/Handles | [Obter identificadores de janela](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles) |  

Para obter mais informações e o status de outros recursos do WebDriver, confira o [WebDriver](../../webdriver.md).  

## Novas APIs no EdgeHTML 15  

Aqui está a lista completa de novas APIs no EdgeHTML 15.  Elas são listadas no formato de `[interface name].[api name]` .  

<iframe height='582' scrolling='no' title='Novas APIs EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Veja a caneta <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> New EdgeHTML15 APIs </a> by Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Versões anteriores do EdgeHTML  

[EdgeHTML 12/Build do Windows 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13/Build do Windows 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14/Build do Windows 14393 (8/2016)](./edgehtml-14.md)  
