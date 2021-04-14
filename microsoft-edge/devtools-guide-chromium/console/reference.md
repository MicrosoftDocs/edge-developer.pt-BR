---
description: Uma referência abrangente para todos os recursos e comportamentos da interface do usuário do Console no Microsoft Edge DevTools.
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: adc3f6c33d6e1a2f6c7db8336c5ab803e76c3307
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483260"
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

Este artigo é uma referência de recursos relacionados ao Console do Microsoft Edge DevTools.  Ele supõe que você já esteja familiarizado com o uso do Console para exibir mensagens registradas e executar JavaScript.  Caso não seja, navegue até Começar a executar [JavaScript][DevtoolsConsoleConsoleJavascript] no Console e Começar a registrar [mensagens no Console][DevtoolsConsoleConsoleLog].  

Se você estiver procurando a referência da API em funções como `console.log()` , navegue até [Console API Reference][DevToolsConsoleApi].  Para fazer referência a funções como `monitorEvents()` , navegue até [Console Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Abrir o Console  

Você pode abrir **o Console** como uma ferramenta [no painel](#open-the-console-tool) superior ou como uma ferramenta [na Gaveta](#open-the-console-tool-in-the-drawer).  

### <a name="open-the-console-tool"></a>Abra a ferramenta Console  

Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="A ferramenta Console" lightbox="../media/console-hello-console.msft.png":::
   A **ferramenta Console**  
:::image-end:::  

Para abrir a **ferramenta Console** no Menu [de Comando][DevtoolsCommandMenuIndex], digite e execute o comando Mostrar Console que tem o selo `Console` **Painel** ao lado dele. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Execute o comando para exibir a ferramenta Console" lightbox="../media/console-command-menu-show-console.msft.png":::
   Execute o comando para exibir a **ferramenta Console**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Abra a ferramenta Console na Gaveta  

Selecione `Esc` ou escolha Personalizar e controlar o **DevTools** \( \) e escolha `...` Mostrar a gaveta do **console.**  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar gaveta de console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Mostrar gaveta de console**  
:::image-end:::  

A Gaveta aparece na parte inferior da janela DevTools, com a **ferramenta Console** aberta.  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="A ferramenta Console na Gaveta" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   A **ferramenta Console** na **Gaveta**  
:::image-end:::  

Para abrir a **ferramenta Console** no Menu [de Comando][DevtoolsCommandMenuIndex], digite e execute o comando Mostrar Console que tem o selo `Console` **Drawer** ao lado dele. ****  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Execute o comando para exibir a ferramenta **Console** na Gaveta" lightbox="../media/console-command-menu-show-console.msft.png":::
   Execute o comando para exibir a **ferramenta Console** na **Gaveta**  
:::image-end:::  

### <a name="open-console-settings"></a>Configurações do Console Aberto  

Escolha o **botão Configurações do** Console \( ![ Ícone de Configurações do Console ](../media/settings-button-icon.msft.png) \)  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configurações do Console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Configurações do Console**  
:::image-end:::  

Os links a seguir explicam cada configuração.  

*   [Ocultar rede](#hide-network-messages)  
*   [Preservar log](#persist-messages-across-page-loads)  
*   [Somente contexto selecionado](#filter-out-messages-from-different-contexts)  
*   [Grupo semelhante](#turn-off-message-grouping)  
*   [Log XMLHttpRequests](#log-xhr-and-fetch-requests)  
*   [Avaliação ávida](#turn-off-eager-evaluation)  
*   [Preenchimento automático do histórico](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a>Abra a barra lateral do console  

Para exibir a **barra lateral,** escolha **Mostrar barra lateral do console** \( Mostrar barra lateral do console ![ ](../media/show-console-sidebar-icon.msft.png) \).  A **barra lateral** ajuda você a filtrar.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra Lateral do Console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Barra Lateral do Console**  
:::image-end:::  

## <a name="view-messages"></a>Exibir mensagens  

Esta seção contém recursos que alteram a forma como as mensagens são apresentadas no Console.  Para um passo a passo hands-on, navegue até [Exibir mensagens][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].  

### <a name="turn-off-message-grouping"></a>Desativar o agrupamento de mensagens  

Para desativar o comportamento padrão de agrupação de mensagens do **Console**, abra Configurações do [Console](#open-console-settings) e escolha a caixa de seleção ao lado de **Group similar**.  Para obter um exemplo, navegue até [Log XHR e Buscar solicitações](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Solicitações XHR e Fetch de log  

Para registrar todas as solicitações no Console conforme cada uma acontece, abra Configurações do Console e escolha a caixa de seleção ao lado de `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. **** [](#open-console-settings)  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Solicitações de Log XMLHttpRequest e Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   Log `XMLHttpRequest` e `Fetch` solicitações  
:::image-end:::  

A mensagem superior na figura anterior exibe o comportamento de agrupação padrão do **Console**.  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Persistir mensagens entre cargas de página  

Quando você carrega uma nova página da Web, a ação padrão limpa o **Console**.  Para persistir mensagens entre cargas de página, [abra Configurações](#open-console-settings) do Console e escolha a caixa de seleção ao lado de **Preservar Log**.  

### <a name="hide-network-messages"></a>Ocultar mensagens de rede  

A ação padrão do Microsoft Edge é fazer logs de mensagens de rede no **Console**.  Na figura a seguir, a mensagem escolhida representa um código de status HTTP de `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Uma mensagem 429 no Console" lightbox="../media/console-show-network.msft.png":::
   Uma `429` mensagem no **Console**  
:::image-end:::  

Para ocultar mensagens de rede, conclua as seguintes ações.  

1.  [Abra Configurações do Console](#open-console-settings).  
1.  Escolha a caixa de seleção ao lado de **Ocultar Rede**.  
    
## <a name="filter-messages"></a>Filtrar mensagens  

Existem muitas maneiras de filtrar mensagens no **Console**.  

### <a name="filter-out-browser-messages"></a>Filtrar mensagens do navegador  

[Abra a Barra Lateral do Console e](#open-the-console-sidebar) escolha # mensagens de **usuário** para exibir apenas mensagens que vieram do JavaScript da página da Web.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Exibir mensagens de usuário" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Exibir mensagens de usuário  
:::image-end:::  

### <a name="filter-by-log-level"></a>Filtrar por nível de log  

O DevTools atribui a cada `console.*` método um dos quatro níveis de gravidade.  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
Por exemplo, `console.log()` está no `Info` grupo, mas está no `console.error()` `Error` grupo.  A [Referência da API de Console][DevToolsConsoleApi] descreve o nível de gravidade de cada método aplicável.  Cada mensagem que o navegador registra no Console também tem um nível de severidade.  Você pode ocultar qualquer nível de mensagens que não esteja interessado.  Por exemplo, se você só estiver interessado em `Error` mensagens, poderá ocultar os outros três grupos.  

Para filtrar as mensagens, escolha o menu suspenso Níveis de **Log** e `Verbose` escolha , , ou `Info` `Warning` `Error` .  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="O menu suspenso Níveis de Log" lightbox="../media/console-log-level-default-levels.msft.png":::
   O **menu suspenso Níveis de** Log  
:::image-end:::  

Para usar o nível de log para filtrar, [abra](#open-the-console-sidebar) a Barra lateral do Console e escolha **Erros,** **Avisos,** **Informações**ou **Verbose**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar a barra lateral para exibir avisos" lightbox="../media/console-sidebar-warnings.msft.png":::
   Usar a barra lateral para exibir avisos  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Filtrar mensagens por URL  

Digite `url:` seguido de uma URL para exibir apenas mensagens que vieram dessa URL.  Depois de digitar `url:` , o DevTools exibe todas as URLs relevantes.  Domínios também funcionam.  Por exemplo, se e estão registrando mensagens, permite que você se concentre nas mensagens `https://example.com/a.js` `https://example.com/b.js` desses dois `url:https://example.com` scripts.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Um filtro DE URL" lightbox="../media/console-filter-text.msft.png":::
   Um filtro DE URL  
:::image-end:::  

Para ocultar mensagens de uma URL, digite `-url:` .  É um filtro de URL negativo.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Um filtro de URL negativo que oculta todas as mensagens que corresponderem à https://b.wal.co URL" lightbox="../media/console-negative-filter-text.msft.png":::
   Um filtro de URL negativo que oculta todas as mensagens que corresponderem à `https://b.wal.co` URL
:::image-end:::  

Para exibir mensagens de uma única URL, conclua as seguintes ações.  

1.  [Abra a barra lateral do console](#open-the-console-sidebar).  
1.  Expanda **a seção # mensagens do usuário.**  
1.  Escolha a URL do script que contém as mensagens nas quais você deseja se concentrar.  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Exibir as mensagens que vieram de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Exibir as mensagens que vieram `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Filtrar mensagens de diferentes contextos  

Suponha que você tenha um anúncio \(ad\) em sua página da Web.  O ad é incorporado em um `<iframe>` e gera muitas mensagens em seu **Console**.  Como o ad está sendo executado em um contexto [JavaScript](#choose-javascript-context)diferente, uma maneira de ocultar as mensagens é abrir Configurações do [Console](#open-console-settings) e escolher a caixa de seleção ao lado de **Somente Contexto Selecionado.**  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a>Filtrar mensagens que não corresponderem a um padrão de expressão regular  

Digite uma expressão regular, como na caixa de texto Filtro, para filtrar todas as mensagens que não `/[gm][ta][mi]/` corresponderem a esse padrão. ****  O DevTools verifica se o padrão foi encontrado no texto da mensagem ou no script que fez com que a mensagem fosse registrada.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar todas as mensagens que não corresponderem à expressão regex" lightbox="../media/console-filter-regex.msft.png":::
   Filtrar todas as mensagens que não corresponderem à `/[gm][ta][mi]/` expressão regex  
:::image-end:::  

## <a name="run-javascript"></a>Executar JavaScript  

Esta seção contém recursos relacionados à execução de JavaScript no **Console**.  Para um passo a passo hands-on, navegue até [Executar JavaScript][DevtoolsConsoleConsoleJavascript].  

### <a name="rerun-expressions-from-history"></a>Reprisar expressões do histórico  

Selecione `Up Arrow` para passar pelo histórico de expressões JavaScript que você executara anteriormente no **Console**.  Selecione `Enter` para executar essa expressão novamente.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Assista ao valor de uma expressão em tempo real com expressões ao vivo  

Se você estiver digitando a mesma expressão JavaScript no **Console** repetidamente, talvez seja mais fácil criar uma **expressão ao vivo.**  Com **Expressões Ao Vivo,** digite uma expressão uma vez e, em seguida, fixe-a na parte superior do **console.**  O valor da expressão é atualizado quase em tempo real.  Navegue [até Ver valores de expressão javascript em Real-Time com expressões ao vivo][DevToolsConsoleLiveExpressions].  

### <a name="turn-off-eager-evaluation"></a>Desativar a Avaliação Ávida  

**A Avaliação** Avida exibe uma visualização do valor de retorno à medida que você digita expressões JavaScript no **Console**.  Para desativar as visualizações de valor de retorno, conclua as seguintes ações.  

1.  [Abra Configurações do Console](#open-console-settings).  
1.  Remova a caixa de seleção ao lado de **Avaliação Ávida**.  
    
### <a name="turn-off-autocomplete-from-history"></a>Desativar o preenchimento automático do histórico  

À medida que você digita uma expressão, a janela pop-up de preenchimento automático do **Console** exibe expressões que você fez anteriormente.  As expressões são pré-canetadas com o `>` caractere.  Para parar de exibir expressões do seu histórico, [abra Configurações](#open-console-settings) do Console e remova a caixa de seleção ao lado de **Caixa** de seleção Preenchimento Automático do Histórico.  

> [!NOTE]
> Na figura a seguir, `document.querySelector('a')` e `document.querySelector('img')` são expressões avaliadas anteriormente.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="O menu pop-up de preenchimento automático exibe expressões do histórico" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   O menu pop-up de preenchimento automático exibe expressões do histórico  
:::image-end:::  

### <a name="choose-javascript-context"></a>Escolha contexto JavaScript  

A opção padrão para o menu suspenso Contexto **JavaScript** é **superior**, que representa o contexto [de][MdnDocsGlossaryBrowsingContext] navegação da página da Web principal.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="O menu suspenso Contexto JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   O **menu suspenso Contexto JavaScript**  
:::image-end:::  

Suponha que você tenha um ad em sua página da Web incorporado em `<iframe>` um .  Você deseja executar JavaScript para ajustar o DOM do ad.  Primeiro, escolha o contexto de navegação do ad no menu suspenso **Contexto JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Escolha um contexto JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   Escolha um contexto JavaScript diferente  
:::image-end:::  

## <a name="clear-the-console"></a>Limpar o Console  

Para limpar **o Console**, conclua qualquer um dos seguintes fluxos de trabalho.  

*   Escolha o **botão Limpar Console** \( Limpar Console ![ ](../media/clear-console-button-icon.msft.png) \).  
*   Passe o mouse em uma mensagem, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Limpar Console**.  
*   Insira `clear()` no Console **e** selecione `Enter` .  
*   Execute `console.clear()` a partir do JavaScript para sua página da Web.  
*   Selecione `Control` + `L` enquanto **o Console** está em foco.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensagens na ferramenta Console | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console como um ambiente JavaScript | Microsoft Docs"  
[DevtoolsConsoleIndex]: .index.md "Use o console | Microsoft Docs"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Inspecionar e filtrar informações na página da Web atual | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Monitorar alterações no JavaScript usando expressões ao vivo | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
