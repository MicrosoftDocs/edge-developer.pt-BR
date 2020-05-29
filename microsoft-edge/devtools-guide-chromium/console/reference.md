---
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601780"
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





# Referência do console   



Esta página é uma referência de recursos relacionados ao console DevTools do Microsoft Edge.  Ele pressupõe que você já esteja familiarizado com o uso do console para exibir mensagens registradas e executar JavaScript.  Se não estiver, consulte Introdução [à execução de JavaScript no console][DevToolsConsoleJavascript] e [introdução ao registro de mensagens no console][DevToolsConsoleLog].  

Se você estiver procurando a referência de API em funções como `console.log()` consulte [referência de API do console][DevToolsConsoleApi].  Para a referência em funções como `monitorEvents()` consulte [referência da API de utilitários de console][DevToolsConsoleUtilities].  

## Abrir o console   

Você pode abrir o console como um [painel](#open-the-console-panel) ou uma [guia na gaveta](#open-the-console-tab-in-the-drawer).  

### Abrir o painel de console   

Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  

> ##### Figura 1  
> Painel do console  
> ![Painel do console][ImageConsolePanel]  

Para abrir o painel do console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e execute o comando **show console** que tenha o selo do **painel** ao lado dele.  

> ##### Figura 2  
> O comando para mostrar o painel do console  
> ![O comando para mostrar o painel do console][ImageCommandShowConsole]  

### Abrir a guia Console na gaveta   

Pressione `Escape` ou clique em **Personalizar e controle devtools** `...` e selecione **Mostrar gaveta do console**.  

> ##### Figura 3  
> Mostrar gaveta do console  
> ![Mostrar gaveta do console][ImageShowConsoleDrawer]  

A gaveta é exibida na parte inferior da janela do DevTools, com a guia **console** aberta.  

> ##### Figura 4  
> A guia Console na gaveta  
> ![A guia Console na gaveta][ImageDrawerConsole]  

Para abrir a guia Console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e, em seguida, execute o comando **show console** que tenha o selo de **gaveta** ao lado dele.  

> ##### Figura 5  
> O comando para mostrar a guia Console na gaveta  
> ![O comando para mostrar a guia Console na gaveta][ImageShowDrawerCommand]  

### Abrir as configurações do console   

Clique em configurações do console configurações **do console** ![ ][ImageSettingsButtonIcon] .  

> ##### Figura 6  
> Configurações do console  
> ![Configurações do console][ImageConsoleSettings]  

Os links a seguir explicam cada configuração:  

*   [**Ocultar rede**](#hide-network-messages)  
*   [**Preservar log**](#persist-messages-across-page-loads)  
*   [**Somente contexto selecionado**](#filter-out-messages-from-different-contexts)  
*   [**Grupo semelhante**](#disable-message-grouping)  
*   [**Registros XMLHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Avaliação rápida**](#disable-eager-evaluation)  
*   [**Preenchimento automático do histórico**](#disable-autocomplete-from-history)  

### Abrir a barra lateral do console   

Clique em **Mostrar barra lateral do console** ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] do console para mostrar a barra lateral, que é útil para filtragem.  

> ##### Figura 7  
> Barra lateral do console  
> ![Barra lateral do console][ImageConsoleSidebar]  

## Exibir mensagens   

Esta seção contém recursos que alteram o modo como as mensagens são apresentadas no console.  Consulte [Exibir mensagens][DevToolsConsoleViewMessages] para obter uma explicação prática.  

### Desabilitar o agrupamento de mensagens   

[Abra as configurações do console](#open-console-settings) e desabilite o grupo de forma **semelhante** para desabilitar o comportamento padrão de agrupamento de mensagens do console.  Consulte [log XHR e recuperar solicitações](#log-xhr-and-fetch-requests) para obter um exemplo.  

### Registrar solicitações de XHR e busca   

[Abra as configurações do console](#open-console-settings) e habilite **XMLHttpRequests de log** para registrar todas as `XMLHttpRequest` `Fetch` solicitações e solicitações ao console à medida que elas acontecem.  

> ##### Figura 8  
> Registro `XMLHttpRequest` em log e `Fetch` solicitações  
> ![Registrando solicitações XMLHttpRequest e busca][ImageXhrGrouped]  

A mensagem superior na [Figura 8](#figure-8) mostra o comportamento padrão de agrupamento do console.  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### Persistir mensagens em todas as cargas de página   

Por padrão, o console é limpo sempre que você carrega uma nova página.  Para persistir mensagens em cargas de página, [abra as configurações do console](#open-console-settings) e, em seguida, habilite a caixa de seleção **preservar registro** .  

### Ocultar mensagens de rede   

Por padrão, o navegador registra as mensagens da rede no **console**.  Por exemplo, a mensagem selecionada na [Figura 9](#figure-9) representa um código de status de `429` .  

> ##### Figura 9  
> Uma mensagem do 429 no console  
> ! [Uma mensagem do 429 no console] [Image429Message]  

Para ocultar as mensagens de rede:  

1.  [Abra as configurações do console](#open-console-settings).  
1.  Habilitar a caixa de seleção **ocultar rede** .  

## Filtrar mensagens   

Há muitas maneiras de filtrar mensagens no console.  

### Filtrar mensagens do navegador   

[Abra a barra lateral do console](#open-the-console-sidebar) e clique em **mensagens de usuário** para mostrar apenas as mensagens que vieram do JavaScript da página.  

> ##### Figura 10  
> Exibindo mensagens de usuário  
> ! [Exibindo mensagens de usuário] [ImageUserMessages]  

### Filtrar por nível de log   

O DevTools atribui `console.*` um nível de severidade a cada método.  Há 4 níveis: `Verbose` ,, `Info` `Warning` e `Error` .  Por exemplo, `console.log()` é o `Info` grupo, enquanto `console.error()` está no `Error` grupo.  A [referência de API do console][DevToolsConsoleApi] descreve o nível de severidade de cada método aplicável.  Cada mensagem que o navegador registra no console também tem um nível de gravidade.  Você pode ocultar qualquer nível de mensagens em que não está interessado.  Por exemplo, se você estiver interessado apenas em `Error` mensagens, poderá ocultar os outros 3 grupos.  

Clique na lista suspensa **níveis de log** para habilitar ou desabilitar `Verbose` , `Info` `Warning` ou `Error` mensagens.  

> ##### Figura 11  
> Lista suspensa **níveis de log**  
> ! [A lista suspensa níveis de log] [ImageLogLevels]  

Você também pode filtrar por nível de log [abrindo a barra lateral do console](#open-the-console-sidebar) e clicando em **erros**, **avisos**, **informações**ou **detalhados**.  

> ##### Figura 12  
> Usar a barra lateral para exibir avisos  
> ! [Usando a barra lateral para exibir avisos] [ImageSidebarWarnings]  

### Filtrar mensagens por URL   

Tipo `url:` seguido por uma URL para exibir apenas as mensagens que vieram dessa URL.  Depois que você digitar `url:` devtools, todas as URLs relevantes são exibidas.  Os domínios também funcionam.  Por exemplo, se `https://example.com/a.js` e `https://example.com/b.js` estiver registrando mensagens, o `url:https://example.com` permite que você se concentre nas mensagens desses 2 scripts.  

> ##### Figura 13  
> Um filtro de URL  
> ! [Um filtro de URL] [ImageUrlFilter]  

Digite `-url:` para ocultar as mensagens dessa URL.  Isso é chamado de filtro de URL negativo.  

> ##### Figura 14  
> Um filtro de URL negativo que oculta todas as mensagens que correspondem à URL `https://b.wal.co`  
> ! [Um filtro de URL negativo que oculta todas as mensagens correspondentes à URL https://b.wal.co ] [ImageNegativeUrlFilter1]  

Você também pode mostrar mensagens de uma única URL [abrindo a barra lateral do console](#open-the-console-sidebar), expandindo a seção **mensagens do usuário** e, em seguida, clicando na URL do script que contém as mensagens nas quais você deseja se concentrar.  

> ##### Figura 15  
> Exibindo as mensagens provenientes de `wp-ad.min.js`  
> ! [Exibindo as mensagens que vieram do WP-AD. min. js] [ImageNegativeUrlFilter2]  

### Filtrar mensagens de diferentes contextos   

Suponha que você tenha um anúncio \ (AD \) na sua página.  O anúncio está incorporado em um `<iframe>` e está gerando muitas mensagens no console.  Como o anúncio está em execução em um [contexto JavaScript](#select-javascript-context)diferente, uma maneira de ocultar as mensagens é [abrir as configurações do console](#open-console-settings) e habilitar a caixa de seleção **contexto selecionado somente** .  

### Filtrar mensagens que não correspondem a um padrão de expressão normal   

Digite uma expressão regular como `/[gm][ta][mi]/` na caixa de texto **Filtrar** para filtrar todas as mensagens que não correspondam a esse padrão.  O DevTools verifica se o padrão é encontrado no texto da mensagem ou no script que fez com que a mensagem seja registrada.  

> ##### Figura 16  
> Filtragem de mensagens que não correspondem `/[gm][ta][mi]/`  
> ! [Filtrar todas as mensagens que não correspondam à expressão Regex] [ImageRegExFilter]  

## Executar JavaScript   

Esta seção contém recursos relacionados à execução de JavaScript no console.  Confira [executar o JavaScript][DevToolsConsoleOverviewJavascript] para um passo a passo prático.  

### Executar novamente as expressões do histórico   

Pressione a `Up Arrow` tecla para percorrer o histórico de expressões JavaScript que você executou anteriormente no console.  Pressione `Enter` para executar essa expressão novamente.  

### Assista ao valor de uma expressão em tempo real com expressões dinâmicas   

Se você estiver digitando a mesma expressão JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.  Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.  O valor da expressão é atualizado em tempo real quase em tempo real.  Consulte [observar valores de expressão JavaScript em tempo real com expressões dinâmicas][DevToolsConsoleLiveExpressions].  

### Desabilitar a avaliação rápida   

À medida que você digita expressões JavaScript no console, a **avaliação adiantada** mostra uma visualização do valor de retorno dessa expressão.  [Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **avaliação adiantada** para desativar as visualizações de valor de retorno.  

### Desabilitar o preenchimento automático do histórico   

À medida que você digita uma expressão, a janela pop-up de preenchimento automático do console mostra as expressões que você executou anteriormente.  Essas expressões são precedidas com o `>` caractere.  [Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **AutoCompletar do histórico** para parar de mostrar as expressões do seu histórico.  

> [!NOTE]
> Na [Figura 17](#figure-17), `document.querySelector('a')` e `document.querySelector('img')` são expressões que foram avaliadas anteriormente.  

> ##### Figura 17  
> O pop-up de preenchimento automático mostrando expressões do histórico  
> ! [O pop-up AutoCompletar mostrando expressões do histórico] [ImageHistoryAutocomplete]  

### Selecionar contexto JavaScript   

Por padrão, a lista suspensa de **contexto JavaScript** é definida como **Top**, que representa o [contexto de navegação][MDNBrowsingContext] do documento principal.  

> ##### Figura 18  
> A lista suspensa de **contexto JavaScript**  
> ! [A lista suspensa contexto JavaScript] [ImageJavascriptContext]  

Suponha que você tenha um anúncio na sua página incorporado em um `<iframe>` .  Você deseja executar o JavaScript para ajustar o DOM do anúncio.  Primeiro, você deve selecionar o contexto de navegação do anúncio na lista suspensa de **contexto JavaScript** .  

> ##### Figura 19  
> Selecionando um contexto JavaScript diferente  
> ! [Selecionando um contexto JavaScript diferente] [ImageSelectContext]  

## Limpar o console   

Você pode usar qualquer um dos fluxos de trabalho a seguir para limpar o console:  

*   Clique em **limpar** console ![ limpar console ][ImageClearConsoleIcon] .  
*   Clique com o botão direito do mouse em uma mensagem e selecione **limpar console**.  
*   Digite `clear()` o console e pressione `Enter` .  
*   Ligue `console.clear()` do JavaScript para a sua página da Web.  
*   Pressione `Control` + `L` enquanto o console estiver em foco.  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Figura 1: painel do console"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figura 2: o comando para mostrar o painel do console"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Figura 3: mostrar a gaveta do console"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Figura 4: guia Console na gaveta"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figura 5: o comando para mostrar a guia Console na gaveta"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Figura 6: configurações do console"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Figura 7: barra lateral do console"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Figura 8: registro em log de solicitações XMLHttpRequest e FETCH"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Show-Network.msft.png "Figura 9: uma mensagem do 429 no console"  
[ImageUserMessages]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-Drawer-User-messages.msft.png "Figura 10: exibindo mensagens de usuário"  
[ImageLogLevels]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Level-default-Levels.msft.png "Figura 11: a lista suspensa de níveis de log"  
[ImageSidebarWarnings]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-Warnings.msft.png "Figura 12: usar a barra lateral para exibir avisos"  
[ImageUrlFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Text.msft.png "Figura 13: um filtro de URL"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Negative-Filter-Text.msft.png "Figura 14: um filtro de URL negativo que oculta todas as mensagens correspondentes à URL https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Text-specified.msft.png "Figura 15: exibindo as mensagens provenientes de wp-AD. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Regex.msft.png "Figura 16: filtrar todas as mensagens que não correspondam à expressão Regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Text-AutoFilter-History.msft.png "figura 17: pop-up de preenchimento automático mostrando expressões do histórico"  
[ImageJavascriptContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-dom-Level-Top.msft.png "Figura 18: a lista suspensa de contexto JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-dom-Level-Multiple.msft.png "Figura 19: selecionando um contexto JavaScript diferente"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Exibir mensagens registradas – visão geral do console"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Visão geral do console em JavaScript"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Começar a executar o JavaScript no console"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência de API de utilitários de console"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
