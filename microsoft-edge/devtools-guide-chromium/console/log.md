---
title: Introdução ao registro de mensagens no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c2cf868e6daaf9dd45c7acc90a71c2154261b9c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982590"
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





# Introdução ao registro de mensagens no console   



Este tutorial interativo mostra como registrar e filtrar mensagens no console do [Microsoft Edge devtools][MicrosoftEdgeDevTools] .  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensagens no console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Mensagens no **console**  
:::image-end:::  

Este tutorial deve ser concluído em ordem.  Ele pressupõe que você compreenda os conceitos básicos do desenvolvimento na Web, por exemplo, como usar JavaScript para adicionar interatividade a uma página.  

## Configurar a demonstração e a DevTools   

Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho.  Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.  

1.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de log do console** para abrir em uma nova guia.  
    
    [Exemplos de log do console][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Focalize a demonstração e, em seguida, pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o devtools.  Por padrão, o DevTools é aberto à direita da demonstração.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="O DevTools é aberto à direita da demonstração" lightbox="../media/console-example-devtools-right-console.msft.png":::
             O DevTools é aberto à direita da demonstração  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Encaixe devtools na parte inferior da janela][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools encaixado na parte inferior da demonstração" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools encaixado na parte inferior da demonstração  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Desencaixe o devtools em uma janela separada][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navegador em uma janela separada" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Navegador em uma janela separada  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Desencaixe o devtools em uma janela separada][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desencaixado em uma janela separada" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools desencaixado em uma janela separada  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Exibir mensagens registradas do JavaScript   

A maioria das mensagens que você vê no console vem dos desenvolvedores da Web que escreveram o JavaScript da página.  O objetivo desta seção é apresentar a você os diferentes tipos de mensagem que provavelmente você verá no console e explicar como você pode registrar cada tipo de mensagem a partir de seu JavaScript.  

1.  Clique no botão **informações de log** na demonstração.  `Hello, Console!` é registrado no console.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="O console depois de clicar em informações de log" lightbox="../media/console-log-info.msft.png":::
       O **console** depois de clicar em **informações de log**  
    :::image-end:::  
    
1.  Ao lado da `Hello, Console!` mensagem no console, clique em **log.js:2**.  O painel fontes é aberto e realça a linha de código que fez com que a mensagem seja registrada no console.  A mensagem foi registrada quando o JavaScript da página foi executado `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="O DevTools abre o painel fontes depois que você clica em log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       O DevTools abre o painel **fontes** depois que você clica em `log.js:2`  
    :::image-end:::  
    
1.  Navegue de volta para o **console** usando qualquer um dos fluxos de trabalho a seguir:  
    
    *   Clique na guia **console** .  
    *   Pressione `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) até que o painel do console esteja em foco.  
    *   [Abra o menu de comando][DevToolsCommandMenu], comece `Console` a digitar, selecione o comando **Mostrar painel do console** e pressione `Enter` .  
    
1.  Clique no botão **aviso de log** na demonstração.  `Abandon Hope All Ye Who Enter` é registrado no console.  As mensagens formatadas assim são avisos.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="O console depois de clicar em registrar aviso" lightbox="../media/console-log-warning.msft.png":::
       O **console** depois de clicar em **registrar aviso**  
    :::image-end:::  
    
    > [!TIP]
    > Se você quiser ver o código que causou a conexão de uma mensagem, clique em um script \ (como `log.js:12` \) para exibir o código que causou a formatação da mensagem.  

1.  Clique no ícone **expandir** \ ( ![ expandir ][ImageExpandIcon] \) em frente a `Abandon Hope All Ye Who Enter` .  DevTools mostra o [rastreamento de pilha][WikiStackTrace] que leva para a chamada.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Um rastreamento de pilha" lightbox="../media/console-log-warning-expanded.msft.png":::
       Um rastreamento de pilha  
    :::image-end:::  
    
    O rastreamento de pilha informa que uma função nomeada `logWarning` foi chamada, que, por sua vez, chamou uma função nomeada `quoteDante` .  Em outras palavras, a chamada que aconteceu primeiro está na parte inferior do rastreamento de pilha.  Você pode fazer o log de rastreamentos de pilha a qualquer momento chamando `console.trace()` .  

1.  Clique em **log Error**.  A seguinte mensagem de erro é registrada: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Uma mensagem de erro" lightbox="../media/console-log-error.msft.png":::
       Uma mensagem de erro  
    :::image-end:::  
    
1.  Clique em **tabela de log**.  Uma tabela sobre artistas famosos é registrada no console.  
    
    > [!NOTE]
    > A `birthday` coluna é apenas preenchida para uma linha.  Revise o código para determinar por que se trata.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Uma tabela no console" lightbox="../media/console-log-table.msft.png":::
       Uma tabela no **console**  
    :::image-end:::  
    
1.  Clique em **grupo de log**.  Os nomes das 4 tartarugas famosas são agrupados sob a `Adolescent Irradiated Espionage Tortoises` etiqueta.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Um grupo de mensagens no console" lightbox="../media/console-log-group.msft.png":::
       Um grupo de mensagens no **console**  
    :::image-end:::  
    
1.  Clique em **log personalizado**.  Uma mensagem com uma borda vermelha e plano de fundo azul é registrada no console.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Uma mensagem com formatação personalizada no console" lightbox="../media/console-log-custom.msft.png":::
       Uma mensagem com formatação personalizada no **console**  
    :::image-end:::  
    
A idéia principal aqui é que, quando você quiser registrar mensagens no console a partir de seu JavaScript, use um dos `console` métodos.  Cada método formata mensagens de maneira diferente.  

Há ainda mais métodos do que o que foi demonstrado nesta seção.  Este tutorial mostra como explorar o restante dos métodos.  

## Exibir mensagens registradas pelo navegador   

O navegador também registra mensagens no console.  Isso geralmente acontece quando há um problema com a página.  

1.  Clique em **causa 404**.  O navegador registra um código de status HTTP do `404` erro de rede porque o JavaScript da página tentou buscar um arquivo que não existe.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Um erro do 404 no console" lightbox="../media/console-cause-404.msft.png":::
       Um `404` erro no **console**  
    :::image-end:::  
    
1.  Clique em **causa erro**.  O navegador registra uma não capturada `TypeError` porque o JavaScript está tentando atualizar um nó DOM que não existe.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Um TypeError no console" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` no **console**  
    :::image-end:::  
    
1.  Clique na lista suspensa **níveis de log** e habilite a opção **detalhado** se estiver desabilitada.  Saiba mais sobre a filtragem na próxima seção.  Você precisa fazer isso para certificar-se de que a próxima mensagem que você registrar está visível.  
    
    > [!NOTE]
    > Se o menu suspenso níveis padrão estiver desabilitado, talvez seja necessário fechar a barra lateral do **console** .  Filtre por fonte de mensagem abaixo para obter mais informações sobre a barra lateral do **console** .
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitando o nível de log detalhado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Habilitando o nível de log detalhado  
    :::image-end:::  
    
1.  Clique em **causa violação**.  A página deixa de responder por alguns segundos e, em seguida, o navegador registra a mensagem no `[Violation] 'click' handler took 3000ms` console.  A duração exata pode variar.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Uma violação no console" lightbox="../media/console-cause-violation.msft.png":::
       Uma violação no **console**  
    :::image-end:::  
    
## Filtrar mensagens   

Em algumas páginas, o console fica inundado com mensagens.  O DevTools oferece várias maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.  

### Filtrar por nível de log   

Cada `console` método é atribuído a um nível de gravidade: `Verbose` ,, `Info` `Warning` ou `Error` .  Por exemplo, `console.log()` é uma `Info` mensagem de nível um, enquanto `console.error()` é uma `Error` mensagem de nível um.  

1.  Clique na lista suspensa **níveis de log** e desabilite os **erros**.  Um nível fica desabilitado quando não há mais uma marca de opção ao lado dele.  As `Error` mensagens de nível desaparecerão.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Desativando mensagens do nível de erro no console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Desativando mensagens do nível de erro no **console**  
    :::image-end:::  
    
1.  Clique novamente na lista suspensa **níveis de log** e ative novamente os **erros**.  As `Error` mensagens de nível reexibida.  

### Filtrar por texto   

Quando quiser exibir apenas as mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na caixa de texto **filtro** .  

1.  Digite `Dave` na caixa de texto **filtro** .  Todas as mensagens que não incluem a cadeia de caracteres `Dave` estão ocultas.  Você também pode ver o `Adolescent Irradiated Espionage Tortoises` rótulo.  Isso é um bug.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtragem de qualquer mensagem que não inclua Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtragem de qualquer mensagem que não inclua `Dave`  
    :::image-end:::  
    
1.  Excluir `Dave` na caixa de texto **Filtrar** .  Todas as mensagens reaparecem.  

### Filtrar por expressão regular   

Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].  

1.  Digite `/^[AH]/` na caixa de texto **filtro** .  Digite esse padrão no [regexr][|::ref1::|Main] para obter uma explicação do que ele está fazendo.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtragem de qualquer mensagem que não corresponda a um padrão" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtragem de qualquer mensagem que não corresponda ao padrão `/^[AH]/`  
    :::image-end:::  
    
1.  Excluir `/^[AH]/` na caixa de texto **Filtrar** .  Todas as mensagens ficarão visíveis novamente.  

### Filtrar por fonte de mensagem   

Quando quiser exibir apenas as mensagens que vieram de determinada URL, use a **barra lateral**.  

1.  Clique em **Mostrar barra lateral do console** \ ( ![ Mostrar barra lateral do console ][ImageShowConsoleSidebarIcon] \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="A barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       A barra lateral  
    :::image-end:::  
    
1.  Clique no ícone **expandir** \ ( ![ expandir ][ImageExpandIcon] \) ao lado do número de mensagens.  Na figura a seguir, o número de mensagens é indicado como **13 mensagens**.  A **barra lateral** mostra uma lista de URLs que fizeram o registro das mensagens.  Por exemplo, `log.js` causou 11 mensagens.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Exibindo a fonte de mensagens na barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Exibindo a fonte de mensagens na barra lateral  
    :::image-end:::  
    
### Filtrar por mensagens de usuário   

Antes, quando você clicou em **registrar informações**, um script chamado para `console.log('Hello, Console!')` registrar a mensagem no console.  As mensagens registradas do JavaScript como essa são chamadas de **mensagens de usuário**.  Por outro lado, quando você clicou em **causa 404**, o navegador registrou uma `Error` mensagem de nível informando que o recurso solicitado não foi encontrado.  Mensagens como essa são consideradas **mensagens do navegador**.  Use a **barra lateral** para filtrar mensagens do navegador e mostrar apenas mensagens de usuário.  

1.  Clique em **9 mensagens de usuário**.  As mensagens do navegador estão ocultas.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrando mensagens do navegador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtrando mensagens do navegador  
    :::image-end:::  
    
1.  Clique em **13 mensagens** para mostrar todas as mensagens novamente.  

## Usar o console juntamente com qualquer outro painel   

E se você estiver editando estilos, mas precisar verificar rapidamente o log do console para algo? Use a gaveta.  

1.  Clique na guia **elementos** .  
1.  Pressione `Escape` .  A guia Console da **gaveta** será aberta.  Ele tem todos os recursos do painel do console que você estava usando em todo este tutorial.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="A guia Console na gaveta" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         A guia **console** na **gaveta**  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

<!--
 


-->  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) | Documentos da Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsConsoleApi]: ./api.md "Referência de API de console | Documentos da Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Referência do console | Documentos da Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introdução ao registro de mensagens | Problema"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha-Wikipédia"  


> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/log) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
