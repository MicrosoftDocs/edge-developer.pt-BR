---
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no EdgeHTML 16.
title: Novos recursos e APIs no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399194"
---
# <a name="whats-new-in-edgehtml-16"></a>Novidades no EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Aqui está uma lista dos recursos novos e atualizados fornecidos na plataforma Web [EdgeHTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) como parte da Atualização de Criadores de Fall do [Windows 10](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).  Para alterações em builds específicos do Windows Insider Preview, consulte o [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) e [Novidades no EdgeHTML](../whats-new.md).  

Aqui está o permalink para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .  

## <a name="new-and-updated-features"></a>Recursos novos e atualizados  

### <a name="css-grid-layout"></a>Layout da Grade CSS  

O Microsoft Edge agora dá suporte à implementação não prefixada de [Layout de Grade CSS.](https://www.w3.org/TR/css-grid-1)  [Layout de Grade](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define um sistema de layout baseado em grade bidimensional que permite mais fluidez de layout do que possível com o posicionamento usando floats ou scripts.  O exemplo a seguir usa Layout de Grade CSS para criar a estrutura de uma página da Web básica.  

<iframe height='303' scrolling='no' title='Layout da Grade CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulte o Layout da Grade CSS da Caneta <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) em </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

### <a name="css-object-fit-and-object-position"></a>Css object-fit and object-position  

EdgeHTML 16 apresenta suporte para propriedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) e [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Essas propriedades controlam a posição e o tamanho do conteúdo substituído dentro da caixa de conteúdo.  

### <a name="developer-tools"></a>Ferramentas de Desenvolvedor  

Esta versão iniciamos um grande esforço de novafação do Microsoft Edge DevTools para melhorar a robustez e o desempenho e também adicionamos um monte de novos recursos que você pode começar a usar hoje em builds [do Windows Insider.](https://insider.windows.com)  Confira o [guia Microsoft Edge DevTools](../whats-new.md) para saber mais sobre o que mudou!  

### <a name="javascript"></a>JavaScript  

[O EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) se cria em otimizações de desempenho javascript de versões anteriores expandindo a capacidade do mecanismo de Chakra de adiar/adiar funções, usar caches embutidos polimórficos e otimizar funções com `try` / `finally` blocos.  

Além disso, os recursos visualizados pela primeira vez no EdgeHTML 15 agora estão estáveis e habilitados por padrão:  

#### <a name="new-features"></a>Novos recursos  

Ativado por padrão  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)  
*   [Memória Compartilhada e Atomics](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a>API da Solicitação de Pagamento  

A [API](../windows-integration/payment-request-api.md) de Solicitação de Pagamento é um padrão aberto entre navegadores que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \(como cartões de crédito\) que os consumidores armazenaram na nuvem.  A API no EdgeHTML 16 foi atualizada para corresponder à especificação mais recente da [API](https://w3c.github.io/payment-request) de Solicitação de Pagamento W3C.  Isso inclui:  

*   Suporte para o `canMakePayment()` método  
*   Suporte para a `requestId` propriedade  
*   Suporte para a `id` propriedade  
*   O valor padrão do parâmetro do método foi `complete()` alterado de " " para `result` "desconhecido"  

### <a name="service-workers"></a>Profissionais de Serviço  

[Os Trabalhadores do](https://www.w3.org/TR/service-workers-1) Serviço são scripts orientados por eventos que são executados em segundo plano de uma página da Web.  Os funcionários de serviço habilitam a funcionalidade anteriormente disponível apenas com aplicativos nativos, como interceptação e manipulação de solicitações da rede, gerenciamento e tratamento de sincronização em segundo plano, armazenamento local e notificações por push.  O suporte para o trabalhador do serviço ainda está em desenvolvimento, mas você pode testar seu PWA no Microsoft Edge com nosso suporte de funcionário de serviço experimental habilitando o recurso de trabalho do serviço em `about:flags` .  

### <a name="webvr"></a>WebVR  

WebVR para Microsoft Edge adicionou suporte para [controladores de movimento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).  Esses controladores têm uma posição precisa no espaço, permitindo uma interação fina com objetos digitais na realidade virtual.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de movimento" lightbox="../media/MotionControllers.jpg":::
   Controladores de movimento  
:::image-end:::  

A WebVR também foi otimizada para dar suporte a dois tipos diferentes de experiências.  

**Computadores de realidade mista do Windows** - Desktops e laptops com elementos gráficos integrados.  Quando conectados a esses dispositivos, nossos fones de ouvido imersivos serão executados a 60 quadros por segundo.  
**Windows Mixed Reality Ultra PCs** - Desktops e laptops com gráficos discretos.  Quando conectados a esses dispositivos, nossos fones de ouvido imersivos serão executados a 90 quadros por segundo.  

Ambas as configurações darão suporte às mesmas experiências imersivas de vídeo e jogos.  

Para obter mais informações sobre as próximas atualizações de Realidade Mista do Windows, confira a postagem do blog de atualização de feriados da Realidade Mista do [Windows.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)  

Para guias e demonstrações, vá para o [Guia do Desenvolvedor webvr.](/microsoft-edge/webvr)  

 > [!NOTE] 
 > Como a especificação WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar mais tarde.  

## <a name="new-apis-in-edgehtml-16"></a>Novas APIs no EdgeHTML 16  

Aqui está a lista completa de novas APIs no EdgeHTML 16.  Eles estão listados no formato de `[interface name].[api name]` .

> [!NOTE] 
> Embora as APIs a seguir sejam expostas no DOM, o comportamento de ponta a ponta de algumas ainda pode estar em desenvolvimento.  Consulte o [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para o suporte oficial do word on feature.  

---  

<iframe height='559' scrolling='no' title='Novas APIs no EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulte as <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> APIs Caneta Novas no EdgeHTML 16 </a> by MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) em </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

---  

## <a name="previous-edgehtml-releases"></a>Versões anteriores do EdgeHTML  

[EdgeHTML 12 / build do Windows 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / build do Windows 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Build do Windows 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15 / build do Windows 15063 (4/2017)](./edgehtml-15.md)  
