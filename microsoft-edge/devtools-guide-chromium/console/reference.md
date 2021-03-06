---
description: Uma referência abrangente sobre todos os recursos e comportamentos relacionados à interface do usuário do Console no Microsoft Edge DevTools.
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399159"
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

# <a name="console-reference"></a>Referência do console  

Esta página é uma referência de recursos relacionados ao Console do Microsoft Edge DevTools.  Ele supõe que você já está familiarizado com o uso do Console para exibir mensagens registradas e executar JavaScript.  Caso não seja, navegue até [Começar a executar JavaScript][DevToolsConsoleJavascript] no console e começar a registrar [mensagens no console.][DevToolsConsoleLog]  

Se você estiver procurando a referência da API em funções como `console.log()` , navegue até [Referência da API do Console][DevToolsConsoleApi].  Para fazer referência a funções como `monitorEvents()` , navegue até [Console Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Abrir o Console  

Você pode abrir **o Console** como uma ferramenta [no painel](#open-the-console-tool) superior ou como uma ferramenta [na Gaveta](#open-the-console-tool-in-the-drawer).  

### <a name="open-the-console-tool"></a>Abra a ferramenta Console  

Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="A ferramenta Console" lightbox="../media/console-hello-console.msft.png":::
   A **ferramenta Console**  
:::image-end:::  

Para abrir a **ferramenta Console** no Menu [de Comando,][DevToolsCommandMenu]comece a digitar e execute o comando Mostrar Console que tem o selo `Console` **Painel** ao lado dele. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="O comando para mostrar o painel console" lightbox="../media/console-command-menu-show-console.msft.png":::
   O comando para mostrar a **ferramenta Console**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Abra a ferramenta Console na Gaveta  

Selecione `Escape` ou escolha Personalizar e Controlar **DevTools** \( \) e escolha `...` Mostrar gaveta do **console**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar gaveta de console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Mostrar gaveta de console**  
:::image-end:::  

A Gaveta aparece na parte inferior da janela DevTools, com a **ferramenta Console** aberta.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="A ferramenta Console na Gaveta" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   A **ferramenta Console** na **Gaveta**  
:::image-end:::  

Para abrir a **ferramenta Console** no Menu [de Comando,][DevToolsCommandMenu]comece a digitar e execute o comando Mostrar Console que tem o selo `Console` **Drawer** ao lado dele. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="O comando para mostrar a ferramenta **Console** na Gaveta" lightbox="../media/console-command-menu-show-console.msft.png":::
   O comando para mostrar a **ferramenta Console** na **Gaveta**  
:::image-end:::  

### <a name="open-console-settings"></a>Configurações do Console Aberto  

Escolha **Configurações do** Console \( ![ Ícone de Configurações de Console ][ImageSettingsButtonIcon] \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configurações do Console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Configurações do Console**  
:::image-end:::  

Os links abaixo explicam cada configuração:  

*   [**Ocultar Rede**](#hide-network-messages)  
*   [**Preservar Log**](#persist-messages-across-page-loads)  
*   [**Somente contexto selecionado**](#filter-out-messages-from-different-contexts)  
*   [**Grupo Semelhante**](#disable-message-grouping)  
*   [**Xml de logHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Avaliação avida**](#disable-eager-evaluation)  
*   [**Preenchimento automático do histórico**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a>Abra a barra lateral do console  

Escolha **Mostrar Barra Lateral do Console** \( Mostrar Barra Lateral do Console \) para mostrar a Barra ![ ][ImageShowConsoleSidebarIcon] lateral, que é útil para filtragem.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra Lateral do Console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Console** Barra lateral  
:::image-end:::  

## <a name="view-messages"></a>Exibir mensagens  

Esta seção contém recursos que alteram a forma como as mensagens são apresentadas no Console.  Para um passo a passo hands-on, navegue até [Exibir mensagens][DevToolsConsoleViewMessages].  

### <a name="disable-message-grouping"></a>Desabilitar o agrupamento de mensagens  

[Abra Configurações do Console e](#open-console-settings) **desabilite Grupo semelhante** para desabilitar o comportamento padrão de agrupação de mensagens do Console.  Para obter um exemplo, navegue até [Log XHR e Buscar solicitações](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Solicitações XHR e Fetch de log  

[Abra Configurações do Console e](#open-console-settings) habilita **o Log XMLHttpRequests** para registrar todas as solicitações e no `XMLHttpRequest` Console conforme elas `Fetch` ocorrem.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Solicitações de Log XMLHttpRequest e Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   Log `XMLHttpRequest` e `Fetch` solicitações  
:::image-end:::  
A mensagem superior na figura anterior exibe o comportamento de agrupação padrão do **Console**.  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Persistir mensagens entre cargas de página  

Por padrão, o Console é limpo sempre que você carrega uma nova página.  Para persistir mensagens entre cargas de página, [Abra Configurações do Console](#open-console-settings) e habilita a caixa de seleção Preservar **Log.**  

### <a name="hide-network-messages"></a>Ocultar mensagens de rede  

Por padrão, o navegador registra mensagens de rede no **Console**.  Na figura a seguir, a mensagem selecionada representa um código de status HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Uma mensagem 429 no Console" lightbox="../media/console-show-network.msft.png":::
   Uma `429` mensagem no **Console**  
:::image-end:::  
Para ocultar mensagens de rede:  

1.  [Abra Configurações do Console](#open-console-settings).  
1.  Habilita **a caixa de seleção Ocultar Rede.**  
    
## <a name="filter-messages"></a>Filtrar mensagens  

Há muitas maneiras de filtrar mensagens no Console.  

### <a name="filter-out-browser-messages"></a>Filtrar mensagens do navegador  

[Abra a Barra Lateral do Console](#open-the-console-sidebar) e escolha Mensagens **de** Usuário para mostrar apenas mensagens que vieram do JavaScript da página.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Exibir mensagens de usuário" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Exibir mensagens de usuário  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtrar por nível de log  

O DevTools atribui a cada `console.*` método um nível de severidade.  Há 4 níveis: `Verbose` , `Info` , e `Warning` `Error` .  Por exemplo, `console.log()` está no `Info` grupo, enquanto que está no `console.error()` `Error` grupo.  A [Referência da API de Console][DevToolsConsoleApi] descreve o nível de gravidade de cada método aplicável.  Cada mensagem que o navegador registra no Console também tem um nível de severidade.  Você pode ocultar qualquer nível de mensagens que não esteja interessado.  Por exemplo, se você estiver interessado apenas em `Error` mensagens, poderá ocultar os outros 3 grupos.  

Escolha o **menu suspenso Níveis de** Log para habilitar ou `Verbose` desabilitar , ou `Info` `Warning` `Error` mensagens.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="O menu suspenso Níveis de Log" lightbox="../media/console-log-level-default-levels.msft.png":::
   O **menu suspenso Níveis de** Log  
:::image-end:::  

Você também pode filtrar por nível de log abrindo a Barra lateral do [Console](#open-the-console-sidebar) e, em seguida, recoosing **Errors**, **Warnings**, **Info**ou **Verbose**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar a barra lateral para exibir avisos" lightbox="../media/console-sidebar-warnings.msft.png":::
   Usar a barra lateral para exibir avisos  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtrar mensagens por URL  

Digite `url:` seguido de uma URL para exibir apenas mensagens que vieram dessa URL.  Depois de digitar `url:` DevTools, mostra todas as URLs relevantes.  Domínios também funcionam.  Por exemplo, se e estão registrando mensagens, permite que você se concentre nas mensagens `https://example.com/a.js` `https://example.com/b.js` desses dois `url:https://example.com` scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Um filtro DE URL" lightbox="../media/console-filter-text.msft.png":::
   Um filtro DE URL  
:::image-end:::  

Digite `-url:` para ocultar mensagens dessa URL.  Isso é chamado de filtro de URL negativo.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Um filtro de URL negativo que oculta todas as mensagens que corresponderem à https://b.wal.co URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Um filtro de URL negativo que oculta todas as mensagens que corresponderem à `https://b.wal.co` URL
:::image-end:::  

Você também pode mostrar mensagens de uma única URL **** abrindo a Barra Lateral do [Console,](#open-the-console-sidebar)expandindo a seção Mensagens do Usuário e, em seguida, ingando a URL do script que contém as mensagens nas quais você deseja se concentrar.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Exibir as mensagens que vieram de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Exibir as mensagens que vieram `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtrar mensagens de diferentes contextos  

Suponha que você tenha um anúncio \(ad\) em sua página.  O ad é incorporado em um `<iframe>` e está gerando muitas mensagens em seu Console.  Como o ad está sendo executado em um contexto [JavaScript](#select-javascript-context)diferente, uma maneira de ocultar as mensagens é abrir Configurações do [Console](#open-console-settings) e ativar a caixa de seleção **Somente** contexto selecionado.  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a>Filtrar mensagens que não corresponderem a um padrão de expressão regular  

Digite uma expressão regular, como na caixa de texto Filtro, para filtrar todas as mensagens `/[gm][ta][mi]/` que não corresponderem a esse padrão. ****  O DevTools verifica se o padrão foi encontrado no texto da mensagem ou no script que fez com que a mensagem fosse registrada.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar todas as mensagens que não corresponderem à expressão regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrar todas as mensagens que não corresponderem à `/[gm][ta][mi]/` expressão regex  
:::image-end:::  

## <a name="run-javascript"></a>Executar JavaScript  

Esta seção contém recursos relacionados à execução do JavaScript no Console.  Para um passo a passo hands-on, navegue até [Executar JavaScript][DevToolsConsoleOverviewJavascript].  

### <a name="re-run-expressions-from-history"></a>Re-executar expressões do histórico  

Selecione a `Up Arrow` chave para passar pelo histórico de expressões JavaScript que você fez anteriormente no Console.  Selecione `Enter` para executar essa expressão novamente.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Assista ao valor de uma expressão em tempo real com expressões ao vivo  

Se você estiver digitando a mesma expressão JavaScript no Console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo.**  Com **expressões ao vivo,** você digita uma expressão uma vez e, em seguida, fixá-la na parte superior do console.  O valor da expressão é atualizado quase em tempo real.  Navegue [até Ver valores de expressão javascript em Real-Time com expressões ao vivo][DevToolsConsoleLiveExpressions].  

### <a name="disable-eager-evaluation"></a>Desabilitar a avaliação avida  

Ao digitar expressões JavaScript no Console, a **Avaliação** Ávida mostra uma visualização do valor de retorno dessa expressão.  [Abra Configurações do Console e](#open-console-settings) desabilite a caixa de seleção **Avaliação** Ávida para desativar as visualizações de valor de retorno.  

### <a name="disable-autocomplete-from-history"></a>Desabilitar o preenchimento automático do histórico  

À medida que você digita uma expressão, a janela pop-up de preenchimento automático do Console mostra expressões que você fez anteriormente.  Essas expressões são pré-anexadas ao `>` caractere.  [Abra Configurações do Console](#open-console-settings) e **desabilite** a caixa de seleção Preenchimento Automático do Histórico para parar de mostrar expressões do seu histórico.  

> [!NOTE]
> Na figura a seguir, `document.querySelector('a')` e `document.querySelector('img')` são expressões avaliadas anteriormente.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="O pop-up de preenchimento automático exibe expressões do histórico" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   O pop-up de preenchimento automático exibe expressões do histórico  
:::image-end:::  

### <a name="select-javascript-context"></a>Selecionar contexto JavaScript  

Por padrão, o menu suspenso **Contexto JavaScript** é definido como **superior**, o que representa o contexto [de][MDNBrowsingContext] navegação do documento principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="O menu suspenso Contexto JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   O **menu suspenso Contexto JavaScript**  
:::image-end:::  

Suponha que você tenha um ad em sua página inserida em `<iframe>` um .  Você deseja executar JavaScript para ajustar o DOM do ad.  Você deve primeiro selecionar o contexto de navegação do ad no menu suspenso **Contexto JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Escolha um contexto JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   Escolha um contexto JavaScript diferente  
:::image-end:::  

## <a name="clear-the-console"></a>Limpar o Console  

Você pode usar qualquer um dos seguintes fluxos de trabalho para limpar o Console:  

*   Escolha **Limpar Console** \( Limpar Console ![ ][ImageClearConsoleIcon] \).  
*   Passe o mouse em uma mensagem, abra o menu contextual \(righ-click\) e escolha **Limpar Console**.  
*   Insira `clear()` no Console **e** selecione `Enter` .  
*   Execute `console.clear()` a partir do JavaScript para sua página da Web.  
*   Selecione `Control` + `L` enquanto **o Console** está em foco.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Exibindo mensagens registradas - Visão geral do console | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Executando o JavaScript - Visão geral do console | Microsoft Docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Começar a executar JavaScript no console | Microsoft Docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Assista aos valores de expressão javascript em tempo real com expressões ao | Microsoft Docs"  
[DevToolsConsoleLog]: ./log.md "Começar a registrar mensagens no console | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
