---
description: Usar o painel funcionários do serviço para gerenciar e depurar seus trabalhadores de serviço
title: DevTools-depurador-funcionários do serviço
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, depurador, depuração, PWA, trabalho do serviço, API do cache
ms.custom: seodec18
ms.openlocfilehash: 8e1fa62358657a47ce40d0742f95a76f2586d0c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561391"
---
# Trabalhadores do serviço

O painel **funcionários do serviço** tem ferramentas para gerenciar e depurar os trabalhadores do serviço para o seu site, para ajudá-lo a:

 - Obter uma visão geral de todos os funcionários de serviço associados ao seu site e detalhes de seu escopo e status
 - **Atualizar** e gerenciar (**Cancelar registro**) o registro de trabalho do serviço para o escopo especificado
 - **Enviar** uma notificação de teste
 - **Parar** / **Inicie** trabalhadores de serviço individuais e
 - **Inspecionar** o trabalhador de serviço selecionado em uma janela separada do depurador

![Painel Visão geral do trabalhador do serviço](./media/service_worker.png)

Observe o seguinte sobre a depuração de trabalhador de serviço no Edge DevTools:

 - A depuração de um trabalhador de serviço iniciará uma nova instância do DevTools separada das ferramentas da página, pois os trabalhadores do serviço podem ser compartilhados entre várias guias.
 - Os painéis de [**elementos**](./elements.md) e [**emulação**](./emulation.md) estão ausentes do depurador de trabalho do serviço, pois os trabalhadores do serviço são executados em segundo plano e não controlam diretamente o front-end do seu aplicativo.
 - Atualmente, o tráfego de rede para um trabalhador de serviço é reportado apenas da instância de depuração DevTools para esse trabalhador, e não da instância do depurador para a própria página.
 - Para simular um **Push** da devtools, você precisará adicionar um ouvinte de evento *Push* ao seu trabalhador do serviço para observar o efeito. O exemplo a seguir imprimirá "testar mensagem de envio de DevTools" no **console**do serviço de trabalho.

   ```JavaScript
   self.addEventListener('push', function(event){
       console.log(event.data.text());
   });
   ```

Aqui estão algumas coisas gerais a serem lembradas ao usar trabalhadores de serviço:

- **Somente HTTPS.** Os funcionários do serviço não funcionarão em HTTP; será preciso usar HTTPS. No entanto, você pode registrar trabalhadores `localhost` de serviço para fins de teste.

- **Não é permitido acesso DOM.** Assim como em funcionários da Web, você não obtém acesso ao modelo de objeto da página. Isso significa que, se você precisar alterar algo sobre a página, será necessário usar [`postMessage`](https://developer.mozilla.org/docs/Web/API/Worker/postMessage) o trabalhador do serviço para a página para que você possa manipular alterações de dom da página.

- **Executa a partir de uma página separada.** Como esses scripts não estão ligados ao tempo de vida de uma página, é importante entender que eles não compartilham o mesmo contexto que a página. Além de não ter acesso ao DOM (conforme declarado anteriormente), ele não terá acesso às mesmas variáveis disponíveis na página.

- **Substitui o *cache do aplicativo*.** O cache do aplicativo será ignorado quando os funcionários do serviço estiverem em uso. A API de trabalho do serviço destina-se a supplant completamente o cache do aplicativo fornecendo controle mais granular ao desenvolvedor da Web.

  - **O script não pode estar em CDN.** O arquivo JavaScript para o trabalho de serviço não pode ser hospedado em uma CDN (rede de distribuição de conteúdo), ele deve estar no mesmo domínio da página. No entanto, se quiser, você pode importar scripts da CDN.

- **Pode ser encerrado a qualquer momento.** Os funcionários de serviço devem ser de curta duração, e o tempo de vida deles está vinculado a eventos. Em particular, os funcionários de serviço têm um limite de tempo no qual eles devem concluir a execução dos manipuladores de eventos. Em outros casos, o navegador ou o sistema operacional podem optar por encerrar um trabalhador de serviço que afete a bateria, a CPU ou o consumo de memória. Em ambos os casos, evite confiar nas variáveis globais no script de trabalho do serviço, caso uma instância diferente do trabalho do serviço seja usada em um evento subsequente que está sendo manipulado.

- **Somente solicitações assíncronas permitidas.** O XHR síncrono não é permitido aqui! Nada é localStorage, portanto, é melhor usar o IndexedDB e a nova API de caches descrita anteriormente.

- **O trabalhador do serviço para o escopo é 1:1.** Você só poderá ter um trabalho de serviço por escopo. Isso significa que se você tentar registrar um trabalho de serviço diferente para um escopo que já tenha um trabalhador de serviço, esse trabalho de serviço será atualizado.
