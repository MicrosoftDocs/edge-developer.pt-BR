---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no Microsoft Edge.
title: Guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 36c5e6530ff584a97e4b42910757495362a1960d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560581"
---
# O que há de novo no EdgeHTML 16

Aqui está uma lista dos recursos novos e atualizados fornecidos na plataforma da Web [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17/edgehtml-16-fall-creators-update/) , como parte da [atualização do Windows 10 para criadores de outono](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update/) (10/2017, Build 16299). Para alterações em compilações específicas do Windows Insider Preview, consulte o [changelog do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) e [o que há de novo no EdgeHTML](../whats-new.md).

Aqui está o link permanente para a seguinte lista de alterações: [https://aka.ms/devguide_edgehtml_16](https://aka.ms/devguide_edgehtml_16) .

## Recursos novos e atualizados

### Layout de grade CSS

O Microsoft Edge agora suporta a implementação não prefixada do [layout de grade CSS](https://www.w3.org/TR/css-grid-1/). O [layout de grade](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define um sistema de layout baseado em grade bidimensional que permite mais fluidos de layout do que o possível com posicionamento com floats ou scripts. O exemplo a seguir usa o layout de grade CSS para criar a estrutura de uma página da Web básica.


<iframe height='303' scrolling='no' title='Layout de grade CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulte o <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> layout de grade CSS da caneta </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .
</iframe>


### CSS `object-fit` e `object-position`

EdgeHTML 16 introduz suporte para propriedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) e [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Essas propriedades controlam a posição e o tamanho do conteúdo substituído na caixa conteúdo.  

### Ferramentas de Desenvolvedor

Este lançamento, começamos a usar um importante esforço de refatoração do Microsoft Edge DevTools para melhorar a eficiência e o desempenho, além de adicionar um monte de novos recursos que você pode começar a usar hoje mesmo em compilações do [Windows Insider](https://insider.windows.com/) .  Confira o [Guia do Microsoft Edge devtools](../../devtools-guide/whats-new.md) para saber mais sobre o que mudou!

### JavaScript

[EdgeHTML 16 cria](https://blogs.windows.com/msedgedev/2017/10/31/optimizations-webassembly-sharedarraybuffer-atomics-edgehtml-16/#FodxEPHxR4WkbtyA.97) otimizações de desempenho de JavaScript de versões anteriores ao expandir a capacidade do mecanismo chakra de adiar/readiar funções, usar caches embutidos polimórficos e otimizar funções com blocos *try/finally* .

Além disso, os recursos primeiro visualizados no EdgeHTML 15 agora são estáveis e habilitados por padrão:

#### Novos recursos (ativado por padrão)

* [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP ([demonstração](https://webassembly.org/demo/))
* [Memória compartilhada e Atomicidades](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

### API de solicitação de pagamento

A [API de solicitação de pagamento](../windows-integration/payment-request-api.md) é um padrão de navegador cruzado aberto que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento (por exemplo, cartões de crédito) que os consumidores armazenaram na nuvem.  A API no EdgeHTML 16 foi atualizada para corresponder à especificação da [API de solicitação de pagamento](https://w3c.github.io/payment-request/) W3C mais recente. Isso inclui:
* Suporte para o `canMakePayment()` método
* Suporte para a `requestId` Propriedade
* Suporte para a `id` Propriedade
* O valor padrão para o `complete()` parâmetro do método `result` mudou de "" para "desconhecido"

### Trabalhadores do serviço

[Os funcionários de serviço](https://www.w3.org/TR/service-workers-1/) são scripts orientados por eventos que são executados em segundo plano de uma página da Web. Os funcionários de serviço habilitam a funcionalidade anteriormente somente disponível em aplicativos nativos, como interceptação e manipulação de solicitações na rede, gerenciamento e manipulação de sincronização em segundo plano, armazenamento local e notificações por push. O suporte para o serviço de trabalho ainda está em desenvolvimento, mas você pode testar o PWA no Microsoft Edge com o nosso suporte experimental ao trabalho habilitando o recurso de trabalhador do serviço em **about: flags**.

### WebVR
O WebVR para Microsoft Edge incluiu suporte para [controladores de movimento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers). Esses controladores têm uma posição precisa em espaço, permitindo uma interação refinada com objetos digitais em realidade virtual.

![Controladores de animação](../media/MotionControllers.jpg)

O WebVR também foi otimizado para dar suporte a dois tipos diferentes de experiências.

**PCs Windows Mixed Reality** -desktops e laptops com elementos gráficos integrados.  Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 60 quadros por segundo.  
**Windows Mixed Reality ultra PCs** -desktops e laptops com elementos gráficos discretos. Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 90 quadros por segundo.   

Ambas as configurações aceitarão as mesmas experiências de vídeo e de jogos imersivas. 

Para obter mais informações sobre as futuras atualizações da realidade do Windows Mixed, confira a postagem do blog de atualização de férias do [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update/) . 

Para guias e demonstrações, vá para o [Guia do desenvolvedor do WebVR](https://docs.microsoft.com/microsoft-edge/webvr/).

 > [!NOTE] 
 > Como a especificação do WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar posteriormente na linha.

## Novas APIs no EdgeHTML 16

Aqui está a lista completa de novas APIs no EdgeHTML 16. Elas são listadas no formato **[nome da interface]. [ nome da API]**.

> [!NOTE] 
> Embora as seguintes APIs sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento. Consulte o [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para obter a palavra oficial sobre o suporte ao recurso.

<iframe height='559' scrolling='no' title='Novas APIs no EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulte as <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> novas APIs de caneta no EdgeHTML 16 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe></p>

<h2 id="previous-edgehtml-releases">Versões anteriores do EdgeHTML</h2>
<p><a href="https://aka.ms/devguide_edgehtml_12" data-raw-source="[EdgeHTML 12 / Windows build 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)">EdgeHTML 12/Build do Windows 10240 (7/2015)</a>

[EdgeHTML 13/Build do Windows 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Build do Windows 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Build do Windows 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)
