---
description: Uma referência abrangente sobre cada recurso e comportamento relacionados à interface do usuário do console no Microsoft Edge DevTools.
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 27d521a4af528e95d06f58ac240f620a9c745044
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125255"
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

Esta página é uma referência de recursos relacionados ao console DevTools do Microsoft Edge.  Ele pressupõe que você já esteja familiarizado com o uso do console para exibir mensagens registradas e executar JavaScript.  Caso contrário, navegue até [introdução à execução do JavaScript no console][DevToolsConsoleJavascript] e comece a usar [o log de mensagens no console][DevToolsConsoleLog].  

Se você estiver procurando a referência de API em funções como `console.log()` consulte [referência de API do console][DevToolsConsoleApi].  Para obter a referência sobre funções como `monitorEvents()` , navegue até [referência da API de utilitários do console][DevToolsConsoleUtilities].  

## Abrir o console  

Você pode abrir o console como um [painel](#open-the-console-panel) ou uma [guia na gaveta](#open-the-console-tab-in-the-drawer).  

### Abrir o painel de console  

Selecione `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Painel do console" lightbox="../media/console-hello-console.msft.png":::
   Painel do **console**  
:::image-end:::  

Para abrir o painel do console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e execute o comando **show console** que tenha o selo do **painel** ao lado dele.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Painel do console" lightbox="../media/console-command-menu-show-console.msft.png":::
   O comando para mostrar o painel do **console**  
:::image-end:::  

### Abrir a guia Console na gaveta  

Selecione `Escape` ou escolha **Personalizar e controle devtools** \ ( `...` \) e, em seguida, escolha **Mostrar gaveta do console**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Painel do console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Mostrar gaveta do console**  
:::image-end:::  

A gaveta é exibida na parte inferior da janela do DevTools, com a guia **console** aberta.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Painel do console" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   A guia **console** na **gaveta**  
:::image-end:::  

Para abrir a guia Console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e, em seguida, execute o comando **show console** que tenha o selo de **gaveta** ao lado dele.  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Painel do console" lightbox="../media/console-command-menu-show-console.msft.png":::
   O comando para mostrar a guia **console** na **gaveta**  
:::image-end:::  

### Abrir as configurações do console  

Escolha **configurações do console** \ ( ![ ícone de configurações do console ][ImageSettingsButtonIcon] \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Painel do console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Configurações do console**  
:::image-end:::  

Os links a seguir explicam cada configuração:  

*   [**Ocultar rede**](#hide-network-messages)  
*   [**Preservar log**](#persist-messages-across-page-loads)  
*   [**Somente contexto selecionado**](#filter-out-messages-from-different-contexts)  
*   [**Grupo semelhante**](#disable-message-grouping)  
*   [**Registros XMLHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Avaliação rápida**](#disable-eager-evaluation)  
*   [**Preenchimento automático do histórico**](#disable-autocomplete-from-history)  
    
### Abrir a barra lateral do console  

Escolha **Mostrar barra lateral do console** \ ( ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] do console \) para mostrar a barra lateral, que é útil para filtragem.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Painel do console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console** do Nota  
:::image-end:::  

## Exibir mensagens  

Esta seção contém recursos que alteram o modo como as mensagens são apresentadas no console.  Consulte [Exibir mensagens][DevToolsConsoleViewMessages] para obter uma explicação prática.  

### Desabilitar o agrupamento de mensagens  

[Abra as configurações do console](#open-console-settings) e desabilite o grupo de forma **semelhante** para desabilitar o comportamento padrão de agrupamento de mensagens do console.  Consulte [log XHR e recuperar solicitações](#log-xhr-and-fetch-requests) para obter um exemplo.  

### Registrar solicitações de XHR e busca  

[Abra as configurações do console](#open-console-settings) e habilite **XMLHttpRequests de log** para registrar todas as `XMLHttpRequest` `Fetch` solicitações e solicitações ao console à medida que elas acontecem.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Painel do console" lightbox="../media/console-xhr-fetch.msft.png":::
   Log `XMLHttpRequest` e `Fetch` solicitações  
:::image-end:::  
A mensagem superior na figura anterior exibe o comportamento padrão de agrupamento do **console**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="Painel do console" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### Persistir mensagens em todas as cargas de página  

Por padrão, o console é limpo sempre que você carrega uma nova página.  Para persistir mensagens em cargas de página, [abra as configurações do console](#open-console-settings) e, em seguida, habilite a caixa de seleção **preservar registro** .  

### Ocultar mensagens de rede  

Por padrão, o navegador registra as mensagens da rede no **console**.  Na figura a seguir, a mensagem selecionada representa um código de status HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Painel do console" lightbox="../media/console-show-network.msft.png":::
   Uma `429` mensagem no **console**  
:::image-end:::  
Para ocultar as mensagens de rede:  

1.  [Abra as configurações do console](#open-console-settings).  
1.  Habilitar a caixa de seleção **ocultar rede** .  
    
## Filtrar mensagens  

Há muitas maneiras de filtrar mensagens no console.  

### Filtrar mensagens do navegador  

[Abra a barra lateral do console](#open-the-console-sidebar) e escolha **mensagens de usuário** para mostrar apenas as mensagens que vieram do JavaScript da página.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Painel do console" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Exibir mensagens de usuário  
:::image-end:::  

### Filtrar por nível de log  

O DevTools atribui `console.*` um nível de severidade a cada método.  Há 4 níveis: `Verbose` ,, `Info` `Warning` e `Error` .  Por exemplo, `console.log()` é o `Info` grupo, enquanto `console.error()` está no `Error` grupo.  A [referência de API do console][DevToolsConsoleApi] descreve o nível de severidade de cada método aplicável.  Cada mensagem que o navegador registra no console também tem um nível de gravidade.  Você pode ocultar qualquer nível de mensagens em que não está interessado.  Por exemplo, se você estiver interessado apenas em `Error` mensagens, poderá ocultar os outros 3 grupos.  

Clique na lista suspensa **níveis de log** para habilitar ou desabilitar `Verbose` , `Info` `Warning` ou `Error` mensagens.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Painel do console" lightbox="../media/console-log-level-default-levels.msft.png":::
   Lista suspensa **níveis de log**  
:::image-end:::  

Você também pode filtrar por nível de log [abrindo a barra lateral do console](#open-the-console-sidebar) e clicando em **erros**, **avisos**, **informações**ou **detalhados**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Painel do console" lightbox="../media/console-sidebar-warnings.msft.png":::
   Usar a barra lateral para exibir avisos  
:::image-end:::  

### Filtrar mensagens por URL  

Tipo `url:` seguido por uma URL para exibir apenas as mensagens que vieram dessa URL.  Depois que você digitar `url:` devtools, todas as URLs relevantes são exibidas.  Os domínios também funcionam.  Por exemplo, se `https://example.com/a.js` e `https://example.com/b.js` estiver registrando mensagens, o `url:https://example.com` permite que você se concentre nas mensagens desses 2 scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Painel do console" lightbox="../media/console-filter-text.msft.png":::
   Um filtro de URL  
:::image-end:::  

Digite `-url:` para ocultar as mensagens dessa URL.  Isso é chamado de filtro de URL negativo.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Painel do console" lightbox="../media/console-negative-filter-text.msft.png":::
   Um filtro de URL negativo que oculta todas as mensagens correspondentes à `https://b.wal.co` URL
:::image-end:::  

Você também pode mostrar mensagens de uma única URL [abrindo a barra lateral do console](#open-the-console-sidebar), expandindo a seção **mensagens do usuário** e, em seguida, clicando na URL do script que contém as mensagens nas quais você deseja se concentrar.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Painel do console" lightbox="../media/console-filter-text-specified.msft.png":::
   Exibir as mensagens provenientes de `wp-ad.min.js`  
:::image-end:::  

### Filtrar mensagens de diferentes contextos  

Suponha que você tenha um anúncio \ (AD \) na sua página.  O anúncio está incorporado em um `<iframe>` e está gerando muitas mensagens no console.  Como o anúncio está em execução em um [contexto JavaScript](#select-javascript-context)diferente, uma maneira de ocultar as mensagens é [abrir as configurações do console](#open-console-settings) e habilitar a caixa de seleção **contexto selecionado somente** .  

### Filtrar mensagens que não correspondem a um padrão de expressão normal  

Digite uma expressão regular como `/[gm][ta][mi]/` na caixa de texto **Filtrar** para filtrar todas as mensagens que não correspondam a esse padrão.  O DevTools verifica se o padrão é encontrado no texto da mensagem ou no script que fez com que a mensagem seja registrada.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Painel do console" lightbox="../media/console-filter-regex.msft.png":::
   Filtrar todas as mensagens que não correspondam à `/[gm][ta][mi]/` expressão Regex  
:::image-end:::  

## Executar JavaScript  

Esta seção contém recursos relacionados à execução de JavaScript no console.  Confira [executar o JavaScript][DevToolsConsoleOverviewJavascript] para um passo a passo prático.  

### Executar novamente as expressões do histórico  

Pressione a `Up Arrow` tecla para percorrer o histórico de expressões JavaScript que você executou anteriormente no console.  Selecione `Enter` para executar essa expressão novamente.  

### Assista ao valor de uma expressão em tempo real com expressões dinâmicas  

Se você estiver digitando a mesma expressão JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.  Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.  O valor da expressão é atualizado em tempo real quase em tempo real.  Consulte [observar valores de expressão JavaScript em Real-Time com expressões ao vivo][DevToolsConsoleLiveExpressions].  

### Desabilitar a avaliação rápida  

À medida que você digita expressões JavaScript no console, a **avaliação adiantada** mostra uma visualização do valor de retorno dessa expressão.  [Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **avaliação adiantada** para desativar as visualizações de valor de retorno.  

### Desabilitar o preenchimento automático do histórico  

À medida que você digita uma expressão, a janela pop-up de preenchimento automático do console mostra as expressões que você executou anteriormente.  Essas expressões são precedidas com o `>` caractere.  [Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **AutoCompletar do histórico** para parar de mostrar as expressões do seu histórico.  

> [!NOTE]
> Na figura a seguir, `document.querySelector('a')` e `document.querySelector('img')` são expressões que foram avaliadas anteriormente.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Painel do console" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   O pop-up AutoCompletar exibe expressões do histórico  
:::image-end:::  

### Selecionar contexto JavaScript  

Por padrão, a lista suspensa de **contexto JavaScript** é definida como **Top**, que representa o [contexto de navegação][MDNBrowsingContext] do documento principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Painel do console" lightbox="../media/console-dom-level-top.msft.png":::
   A lista suspensa de **contexto JavaScript**  
:::image-end:::  

Suponha que você tenha um anúncio na sua página incorporado em um `<iframe>` .  Você deseja executar o JavaScript para ajustar o DOM do anúncio.  Primeiro, você deve selecionar o contexto de navegação do anúncio na lista suspensa de **contexto JavaScript** .  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Painel do console" lightbox="../media/console-dom-level-multiple.msft.png":::
   Selecionar um contexto JavaScript diferente  
:::image-end:::  

## Limpar o console  

Você pode usar qualquer um dos fluxos de trabalho a seguir para limpar o console:  

*   Escolha **limpar console** \ ( ![ limpar console ][ImageClearConsoleIcon] \).  
*   Clique com o botão direito do mouse em uma mensagem e escolha **limpar console**.  
*   Insira `clear()` no console e selecione `Enter` .  
*   Executar `console.clear()` a partir do JavaScript para sua página da Web.  
*   Selecione `Control` + `L` enquanto o console está em foco.  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Exibir mensagens registradas – visão geral do console | Documentos da Microsoft"  
[DevToolsConsoleApi]: ./api.md "Referência de API de console | Documentos da Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Como executar JavaScript – visão geral do console | Documentos da Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Comece a executar o JavaScript no console | Documentos da Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas | Documentos da Microsoft"  
[DevToolsConsoleLog]: ./log.md "Introdução ao registro de mensagens no console | Documentos da Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência de API de utilitários de console | Documentos da Microsoft"  

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
