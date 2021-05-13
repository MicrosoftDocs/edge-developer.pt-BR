---
description: Use o painel Aplicativo para inspecionar, modificar e depurar manifestos de aplicativo Web, funcionários de serviço e caches de funcionários do serviço.
title: Depurar aplicativos Web progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3a0732327aac210e399c438b8d9c34c75a7c2910
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564725"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="debug-progressive-web-apps"></a>Depurar aplicativos Web progressivos  

Use o **painel Aplicativo** para inspecionar, modificar e depurar manifestos de aplicativo Web, funcionários de serviço e caches de funcionários do serviço.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

Este guia discute apenas os recursos do Progressive Web App do **painel Aplicativo.**  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a>Resumo  

*   Use o **painel Manifesto** para inspecionar o manifesto do aplicativo Web e disparar Adicionar a eventos homescreen.  
*   Use **** o painel Funcionários do Serviço para uma ampla gama de tarefas relacionadas ao serviço de trabalho, como o registro ou atualização de um serviço, a emulação de eventos push, a offline ou a interrupção de um trabalhador de serviço.  
*   Exibir seu cache de trabalho de serviço no **painel Cache Armazenamento.**  
*   Desaconselhe um funcionário de serviço e limpe todos os armazenamentos e caches com um único botão escolha no painel **Limpar armazenamento.**  
    
## <a name="web-app-manifest"></a>Manifesto do aplicativo Web  

Se você quiser que seus usuários sejam capazes de adicionar seu aplicativo às telas de tela inicial móveis, você precisa de um manifesto do aplicativo Web.  O manifesto define como o aplicativo aparece na tela inicial, onde direcionar o usuário ao iniciar a partir da tela inicial e como o aplicativo se parece ao iniciar.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Depois de configurar o manifesto, você pode usar o painel **Manifesto** do painel **Aplicativo** para inspecioná-lo.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="O Painel de Manifesto" lightbox="../media/manifest-pane.msft.png":::
   O **Painel de** Manifesto  
:::image-end:::  

*   Para ver a fonte do manifesto, escolha o link abaixo rótulo **de Manifesto** do Aplicativo \( na `https://airhorner.com/manifest.json` figura anterior\).  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   As **seções Identidade** e **Apresentação** exibem apenas campos da fonte de manifesto em uma exibição mais fácil de usar.  
*   A **seção Ícones** exibe todos os ícones especificados.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a>Profissionais de serviço  

Os funcionários de serviços são uma tecnologia fundamental na plataforma Web futura.  Eles são scripts que o navegador executa em segundo plano, separados de uma página da Web.  Os scripts permitem que você acesse recursos que sem a necessidade de uma página da Web ou interação do usuário, como notificações por push, sincronização em segundo plano e experiências offline.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

O **painel Trabalhadores do** Serviço no painel **Aplicativo** é o principal local no DevTools para inspecionar e depurar os funcionários do serviço.  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="O painel Trabalhadores do Serviço" lightbox="../media/service-workers-pane.msft.png":::
   O **painel Trabalhadores do** Serviço  
:::image-end:::  

*   Se um trabalhador de serviço estiver instalado na página aberta no momento, ele será listado neste painel.  Por exemplo, na figura anterior, há um trabalhador de serviço instalado para o escopo de `https://weather-pwa-sample.firebaseapp.com` .  
*   A **caixa de** seleção Offline coloca o DevTools no modo offline.  Isso equivale ao modo offline disponível na ferramenta **Rede** ou à opção `Go offline` no Menu De [comando][DevtoolsCommandMenuIndex].  
*   A **caixa de seleção** Atualizar ao recarregar força o trabalhador do serviço a atualizar em cada carga de página.  
*   A **caixa de seleção Ignorar** para rede ignora o funcionário do serviço e força o navegador a ir para a rede para recursos solicitados.  
*   O **botão** Atualizar executa uma atualização única do trabalhador de serviço especificado.  
*   O **botão Push** emula uma notificação por push sem uma carga \(também conhecida como uma **coceira**\).  
*   O **botão Sincronizar** emula um evento de sincronização em segundo plano.  
*   O **botão Não registro** no registro do funcionário de serviço especificado.  Confira [Limpar o armazenamento para](#clear-storage) saber como desoperdá-lo e apagar o armazenamento e os caches com um único botão escolha.  
*   A **linha Source** informa quando o funcionário do serviço em execução foi instalado.  O link é o nome do arquivo de origem do trabalhador do serviço.  A escolha no link o envia para a origem do trabalhador do serviço.  
*   A **linha Status** informa o status do trabalhador do serviço.  O número de ID ao lado do indicador de status verde \( na figura anterior\) é para o Trabalhador `#36` de Serviço ativo no momento.  Ao lado do status, **um** botão iniciar \(se o **** trabalhador do serviço for interrompido\) ou um botão de parada \(se o trabalhador do serviço estiver em execução\) é exibido.  Os funcionários do serviço são projetados para serem interrompidos e iniciados pelo navegador a qualquer momento.  Interromper explicitamente o trabalho de serviço usando o **botão parar** pode simular isso.  Parar o seu funcionário de serviço é uma ótima maneira de testar como seu código se comporta quando o trabalhador do serviço começa a fazer o back-up novamente.  Ele frequentemente revela bugs devido a suposições incorretas sobre o estado global persistente.  
*   A **linha Clientes** informa a origem para a que o trabalhador do serviço tem escopo.  O **botão** de foco é mais útil quando você habilita a caixa de **seleção mostrar tudo.**  Quando essa caixa de seleção está habilitada, todos os funcionários de serviço registrados são listados.  Se você escolher o botão **de foco** ao lado de um trabalhador de serviço que está executando em uma guia diferente, Microsoft Edge se concentrará nessa guia.  
    
Se o trabalhador do serviço causar erros, um novo rótulo chamado **Errors** será a aparecer.  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a>Caches de funcionários de serviço  

O **painel Armazenamento** cache fornece uma lista somente leitura de recursos que foram armazenados em cache usando a API de Cache \(service worker\) [Cache][MDNWebCacheAPI].  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="O Painel de Armazenamento cache" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   O **Painel de Armazenamento** Cache  
:::image-end:::  

> [!NOTE]
> Na primeira vez que você abrir um cache e adicionar um recurso a ele, o DevTools pode não detectar a alteração.  Atualize a página e para exibir o cache.  

Se você tiver dois ou mais caches abertos, os caches serão exibidos na lista **Armazenamento** cache a seguir.  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="O menu suspenso Armazenamento cache" lightbox="../media/cache-pane-cache-storage.msft.png":::
   O **menu suspenso Armazenamento** cache  
:::image-end:::  

## <a name="quota-usage"></a>Uso de cota  

Algumas respostas no **painel Cache Armazenamento** podem ser sinalizadas como "opacas".  Isso se refere a uma resposta recuperada de **** uma origem diferente, como de uma api CDN ou remota, quando [o CORS][FetchHttpCorsProtocol] não está habilitado.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Para evitar vazamento de informações entre domínios, preenchimento significativo é adicionado ao tamanho de uma resposta opaca usada para calcular os limites de cota de armazenamento \(por exemplo, se uma exceção é lançada\) e relatada pela `QuotaExceeded` `navigator.storage` API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Os detalhes desse preenchimento variam de navegador para navegador, mas para **** Microsoft Edge, isso significa que o tamanho mínimo que qualquer resposta opaca em cache único contribui para o uso geral do armazenamento é de aproximadamente [7 megabytes][ChromiumIssues796060#c17].  Lembre-se do preenchimento ao determinar quantas respostas opacas você deseja armazenar em cache, já que você pode exceder facilmente as limitações de cota de armazenamento muito antes do esperado com base no tamanho real dos recursos opacos.  

Guias relacionados:  

*   [Stack Overflow: Quais limitações se aplicam às respostas opacas?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a>Limpar o armazenamento  

O **painel Limpar Armazenamento** é um recurso muito útil ao desenvolver aplicativos Web progressivos.  Esse painel permite que você desaconselhe os funcionários do serviço e desimpe todos os caches e armazenamento com um único botão escolha.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Problema 796060: o valor Armazenamento cache aumenta em cada atualização quando o código do Analytics está no html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache - APIs da Web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow: Quais limitações se aplicam às respostas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
