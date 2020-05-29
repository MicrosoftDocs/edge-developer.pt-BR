---
title: Depurar aplicativos Web progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: ce389ad10073efd318e5fa4df59d78fd40b7ebeb
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601877"
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





# Depurar aplicativos Web progressivos   



Use o painel do **aplicativo** para inspecionar, modificar e depurar manifestos do aplicativo Web, trabalhos de serviço e caches de trabalho do serviço.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

Este guia apenas descreve os recursos do aplicativo Web progressivo do painel do **aplicativo** .  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### Resumo  

*   Use o painel **manifestar** para inspecionar seu manifesto do aplicativo Web e disparar adicionar a eventos tela inicial.  
*   Use o painel **trabalhadores do serviço** para uma variedade completa de tarefas relacionadas ao trabalhador, como cancelar o registro ou a atualização de um serviço, a emulação de eventos Push, o offline ou a interrupção de um trabalhador de serviço.  
*   Exiba o cache do serviço de trabalho no painel **armazenamento do cache** .  
*   Cancele o registro de um trabalhador de serviço e limpe todos os armazenamentos e caches com um único clique de botão no painel **limpar armazenamento** .  

## Manifesto do aplicativo Web   

Se você quiser que os usuários possam adicionar seu aplicativo à sua homescreens móvel, você precisará de um manifesto do aplicativo Web.  O manifesto define como o aplicativo é exibido no tela inicial, onde direcionar o usuário ao iniciar a partir do tela inicial e como é a aparência do aplicativo durante a inicialização.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Depois de configurar o manifesto, você pode usar o painel **manifesto** do painel do **aplicativo** para inspecioná-lo.  

> ##### Figura 1  
> Painel de **manifesto**  
> ![Painel de manifesto][ImageManifest]  

*   Para ver a origem do manifesto, clique no link abaixo do rótulo do **manifesto do aplicativo** \ ( `https://airhorner.com/manifest.json` na [**Figura 1**](#figure-1)] \).  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   As seções de **identidade** e **apresentação** só exibem os campos da fonte de manifesto em uma tela mais fácil de usar.  
*   A seção **ícones** exibe todos os ícones que você especificou.  

<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--![add to desktop shelf][ImageDesktopShelf]  -->

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## Trabalhadores do serviço   

Os funcionários de serviço são uma tecnologia fundamental na próxima plataforma Web.  Eles são scripts que o navegador executa em segundo plano, separado de uma página da Web.  Esses scripts permitem que você acesse recursos que não precisam de uma página da Web ou interação do usuário, como notificações por push, sincronização em segundo plano e experiências offline.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  

<!--TODO:  Link to sections when available. -->  

O painel de **trabalhadores de serviço** no painel de **aplicativos** é o local principal no devtools para inspecionar e depurar trabalhadores de serviço.  

> ##### Figura 2  
> O painel **funcionários do serviço**  
> ! [O painel funcionários do serviço] [ImageServiceWorkersPane]  

*   Se um trabalhador do serviço estiver instalado na página atualmente aberta, você verá-o listado nesse painel.  Por exemplo, na [**Figura 2**](#figure-2) , há um trabalho de serviço instalado para o escopo de `https://weather-pwa-sample.firebaseapp.com` .  
*   A caixa de seleção **offline** coloca devtools no modo offline.  Isso equivale ao modo offline disponível no painel **rede** ou na `Go offline` opção no [menu de comando][DevtoolsCommandMenuIndex].  
*   A caixa de seleção **Atualizar na recarga** força o trabalhador do serviço a atualizar em cada carregamento de página.  
*   A caixa **de seleção Ignorar para rede** ignora o trabalhador do serviço e força o navegador a ir para a rede para obter os recursos solicitados.  
*   O botão **Atualizar** executa uma atualização única do trabalho de serviço especificado.  
*   O botão de **ação** emula uma notificação por push sem uma carga \ (também conhecida como **Tickle**\).  
*   O botão **sincronizar** emula um evento de sincronização em segundo plano.  
*   O botão **Cancelar registro** cancela o registro do trabalho de serviço especificado.  Confira o [armazenamento claro](#clear-storage) para obter uma maneira de cancelar o registro de um trabalhador de serviço e revelar armazenamento e caches com um único clique de botão.  
*   A linha de **origem** informa quando o trabalho de serviço atualmente em execução foi instalado.  O link é o nome do arquivo de origem do trabalhador do serviço.  Clicar no link envia você para a fonte do trabalhador do serviço.  
*   A linha **status** informa o status do trabalhador do serviço.  O número de identificação ao lado do indicador de status verde \ ( `#36` na [**Figura 2**](#figure-2)\) é para o trabalhador de serviço ativo no momento.  Ao lado do status, você verá um botão **Iniciar** \ (se o trabalhador do serviço estiver parado \) ou um botão **parar** \ (se o trabalhador do serviço estiver em execução \).  Os funcionários de serviço são projetados para serem interrompidos e iniciados pelo navegador a qualquer momento.  Parar explicitamente seu trabalho de serviço usando o botão **parar** pode simular isso.  Parar seu trabalho de serviço é uma ótima maneira de testar como o seu código se comporta quando o trabalho do serviço começa a fazer backup novamente.  Freqüentemente, ele revela bugs devido a suposições defeituosas sobre o estado global persistente.  
*   A linha **clientes** informa a origem para a qual o trabalhador do serviço tem escopo.  O botão **foco** é principalmente útil quando você habilita a caixa de seleção **Mostrar tudo** .  Quando essa caixa de seleção estiver habilitada, todos os trabalhos de serviço registrados serão listados.  Se você clicar no botão **foco** ao lado de um trabalhador de serviço que está sendo executado em uma guia diferente, o Microsoft Edge será focalizado nessa guia.  

Se o trabalhador do serviço causar algum erro, um novo rótulo chamado **erros** aparecerá.  

<!--![service worker with errors][ImageServiceWorkerErrors]  -->

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## Caches de funcionários do serviço 

O painel **armazenamento de cache** fornece uma lista somente leitura de recursos que foram armazenados em cache usando a API de [cache][MDNWebCacheAPI]\ (serviço de trabalho \).  

> ##### Figura 3  
> Painel **armazenamento do cache**  
> ! [O painel armazenamento do cache] [ImageServiceWorkersCachePane]  

> [!NOTE]
> Na primeira vez que você abre um cache e adiciona um recurso a ele, a DevTools pode não detectar a alteração.  Recarregue a página e você deve ver o cache.  

Se houver dois ou mais caches abertos, você os verá listados abaixo do menu suspenso **armazenamento em cache** .  

> ##### Figura 4  
> O menu suspenso **armazenamento do cache**  
> ! [O menu suspenso armazenamento do cache] [ImageMultipleCaches]  

## Uso da cota 

Algumas respostas dentro do painel armazenamento do cache podem ser sinalizadas como "**opaco**".  Isso se refere a uma resposta recuperada de uma origem diferente, como de uma **CDN** ou API remota, quando o [CORS][FetchHttpCorsProtocol] não está habilitado.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Para evitar o vazamento de informações entre domínios, há um preenchimento significativo adicionado ao tamanho de uma resposta opaca usada para calcular limites de cotas de armazenamento \ (por exemplo, se uma `QuotaExceeded` exceção é acionada \) e reportada pela **`navigator.storage`** API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Os detalhes desse preenchimento variam do navegador para o navegador, mas para o Microsoft Edge, isso significa que o **tamanho mínimo** que qualquer resposta opaca em cache única contribui para o uso geral do armazenamento é de [aproximadamente 7 megabytes][ChromiumIssues796060#c17].  Você deve ter isso em mente ao determinar quantas respostas opacas você deseja armazenar em cache, pois você pode ter facilmente excedido as limitações de cotas de armazenamento muito antes do que você esperaria com base no tamanho real dos recursos opacos.  

Guias relacionados:  

*   [Estouro de pilha: quais limitações se aplicam às respostas opacas?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->

<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## Limpar armazenamento 

O painel **limpar armazenamento** é um recurso muito útil ao desenvolver aplicativos Web progressivos.  Esse painel permite cancelar o registro de trabalhadores do serviço e limpar todos os caches e armazenamento com um único clique de botão.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->

<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->

<!--TODO  -->

 



<!-- image links -->  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/manifest-pane.msft.png "Figura 1: o painel manifestar"  
<!--[ImageDesktopShelf]: /microsoft-edge/devtools-guide-chromium/media/io.msft.png "Add to desktop shelf"  -->
[ImageServiceWorkersPane]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Service-Workers-pane.msft.png "Figura 2: o painel de trabalho do serviço"  
<!--[ImageServiceWorkerErrors]: /microsoft-edge/devtools-guide-chromium/media/sw-error.msft.png "Service worker with errors"  -->
[ImageServiceWorkersCachePane]:/Microsoft-Edge/devtools-Guide-Chromium/Media/cache-pane-cache-Storage-Resources.msft.png "Figura 3: painel armazenamento do cache"  
[ImageMultipleCaches]:/Microsoft-Edge/devtools-Guide-Chromium/Media/cache-pane-cache-Storage.msft.png "Figura 4: a lista suspensa **armazenamento em cache** "  

<!-- links -->  

[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "796060 problema de Chromium: o valor de armazenamento em cache aumenta em cada atualização quando o código analítico está em HTML"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "APIs da Web em cache | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Estouro de pilha: quais limitações se aplicam às respostas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
