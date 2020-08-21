---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no Microsoft Edge.
title: Novos recursos e APIs no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: a15888bc8c1314d61d436759e5d63be942174ea4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941935"
---
# O que há de novo no EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Aqui está uma lista dos recursos novos e atualizados fornecidos na plataforma da Web [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) , como parte da [atualização do Windows 10 para criadores de outono](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \ (10/2017, Build 16299 \).  Para alterações em compilações específicas do Windows Insider Preview, consulte o [changelog do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) e [o que há de novo no EdgeHTML](../whats-new.md).  

Aqui está o link permanente para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .  

## Recursos novos e atualizados  

### Layout de grade CSS  

O Microsoft Edge agora oferece suporte à implementação prefixada do [layout de grade CSS](https://www.w3.org/TR/css-grid-1).  O [layout de grade](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define um sistema de layout baseado em grade bidimensional que permite mais fluidos de layout do que o possível com posicionamento com floats ou scripts.  O exemplo a seguir usa o layout de grade CSS para criar a estrutura de uma página da Web básica.  

<iframe height='303' scrolling='no' title='Layout de grade CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulte o <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> layout de grade CSS da caneta </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>  

### Objeto CSS-ajustar e posição do objeto  

EdgeHTML 16 introduz suporte para propriedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) e [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Essas propriedades controlam a posição e o tamanho do conteúdo substituído na caixa conteúdo.  

### Ferramentas de Desenvolvedor  

Este lançamento, começamos a usar um importante esforço de refatoração do Microsoft Edge DevTools para melhorar a eficiência e o desempenho, além de adicionar um monte de novos recursos que você pode começar a usar hoje mesmo em compilações do [Windows Insider](https://insider.windows.com) .  Confira o [Guia do Microsoft Edge devtools](../whats-new.md) para saber mais sobre o que mudou!  

### JavaScript  

[EdgeHTML 16 cria](https://blogs.windows.com/msedgedev/2017/10/31) otimizações de desempenho de JavaScript de versões anteriores ao expandir a capacidade do mecanismo chakra de adiar/readiar funções, usar caches embutidos polimórficos e otimizar funções com `try` / `finally` blocos.  

Além disso, os recursos primeiro visualizados no EdgeHTML 15 agora são estáveis e habilitados por padrão:  

#### Novos recursos  

Ativado por padrão  

*   [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \ ([demonstração](https://webassembly.org/demo)\)  
*   [Memória compartilhada e Atomicidades](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### API da Solicitação de Pagamento  

A [API de solicitação de pagamento](../windows-integration/payment-request-api.md) é um padrão de navegador cruzado aberto que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \ (como cartões de crédito \) que os consumidores armazenaram na nuvem.  A API no EdgeHTML 16 foi atualizada para corresponder à especificação da [API de solicitação de pagamento](https://w3c.github.io/payment-request) W3C mais recente.  Isso inclui:  

*   Suporte para o `canMakePayment()` método  
*   Suporte para a `requestId` Propriedade  
*   Suporte para a `id` Propriedade  
*   O valor padrão para o `complete()` parâmetro do método `result` mudou de "" para "desconhecido"  

### Profissionais de Serviço  

[Os funcionários de serviço](https://www.w3.org/TR/service-workers-1) são scripts orientados por eventos que são executados em segundo plano de uma página da Web.  Os funcionários de serviço habilitam a funcionalidade anteriormente somente disponível em aplicativos nativos, como interceptação e manipulação de solicitações na rede, gerenciamento e manipulação de sincronização em segundo plano, armazenamento local e notificações por push.  O suporte para o serviço de trabalho ainda está em desenvolvimento, mas você pode testar o PWA no Microsoft Edge com o nosso serviço de trabalho experimental ao habilitar o recurso de trabalho do serviço `about:flags` .  

### WebVR  

O WebVR para Microsoft Edge incluiu suporte para [controladores de movimento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).  Esses controladores têm uma posição precisa em espaço, permitindo uma interação refinada com objetos digitais em realidade virtual.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de animação" lightbox="../media/MotionControllers.jpg":::
   Controladores de animação  
:::image-end:::  

O WebVR também foi otimizado para dar suporte a dois tipos diferentes de experiências.  

**PCs Windows Mixed Reality** -desktops e laptops com elementos gráficos integrados.  Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 60 quadros por segundo.  
**Windows Mixed Reality ultra PCs** -desktops e laptops com elementos gráficos discretos.  Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 90 quadros por segundo.  

Ambas as configurações aceitarão as mesmas experiências de vídeo e de jogos imersivas.  

Para obter mais informações sobre as futuras atualizações da realidade do Windows Mixed, confira a postagem do blog de atualização de férias do [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) .  

Para guias e demonstrações, vá para o [Guia do desenvolvedor do WebVR](/microsoft-edge/webvr).  

 > [!NOTE] 
 > Como a especificação do WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar posteriormente na linha.  

## Novas APIs no EdgeHTML 16  

Aqui está a lista completa de novas APIs no EdgeHTML 16.  Elas são listadas no formato de `[interface name].[api name]` .

> [!NOTE] 
> Embora as seguintes APIs sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento.  Consulte o  [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para obter a palavra oficial sobre o suporte ao recurso.  

---  

<iframe height='559' scrolling='no' title='Novas APIs no EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulte as <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> novas APIs de caneta no EdgeHTML 16 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>  

---  

## Versões anteriores do EdgeHTML  

[EdgeHTML 12/Build do Windows 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13/Build do Windows 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14/Build do Windows 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15/Build do Windows 15063 (4/2017)](./edgehtml-15.md)  
