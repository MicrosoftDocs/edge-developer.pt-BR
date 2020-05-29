---
title: Introdução ao registro de mensagens no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601730"
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

> ##### Figura 1  
> Mensagens no console  
> ![Mensagens no console][ImageLogExample]  

Este tutorial deve ser concluído em ordem.  Ele pressupõe que você compreenda os conceitos básicos do desenvolvimento na Web, por exemplo, como usar JavaScript para adicionar interatividade a uma página.  

## Configurar a demonstração e a DevTools   

Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho.  Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.  

1.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de log do console** para abrir em uma nova guia.  
    
    [Exemplos de log do console][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  Focalize a demonstração e, em seguida, pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o devtools.  Por padrão, o DevTools é aberto à direita da demonstração.  
    
    > ##### Figura 2  
    > O DevTools é aberto à direita da demonstração  
    > ! [O DevTools abre à direita da demonstração] [ImageDevToolsRight]  
    
    > [!TIP]
    > [Encaixe devtools na parte inferior da janela ou desencaixe-a em uma janela separada][DevToolsCustomizePlacement].  
    
    > ##### Figura 3  
    > DevTools encaixado na parte inferior da demonstração  
    > ! [DevTools encaixado na parte inferior da demonstração] [ImageDevToolsBottom]  
    
    > ##### Figura 4  
    > Navegador em uma janela separada  
    > ! [Navegador em uma janela separada] [ImageDevToolsSeparateBrowse]  
    
    > ##### Figura 5  
    > DevTools desencaixado em uma janela separada  
    > ! [DevTools desencaixado em uma janela separada] [ImageDevToolsSeparateDevTools]  
    
## Exibir mensagens registradas do JavaScript   

A maioria das mensagens que você vê no console vem dos desenvolvedores da Web que escreveram o JavaScript da página.  O objetivo desta seção é apresentar a você os diferentes tipos de mensagem que provavelmente você verá no console e explicar como você pode registrar cada tipo de mensagem a partir de seu JavaScript.  

1.  Clique no botão **informações de log** na demonstração.  `Hello, Console!` é registrado no console.
    
    > ##### Figura 6  
    > O console depois de clicar em **informações de log**  
    > ! [O console após clicar em informações do log] [ImageLogInfo]  
    
1.  Ao lado da `Hello, Console!` mensagem no console, clique em **log. js: 2**.  O painel fontes é aberto e realça a linha de código que fez com que a mensagem seja registrada no console.  A mensagem foi registrada quando o JavaScript da página foi executado `console.log('Hello, Console!')` .
    
    > ##### Figura 7  
    > O DevTools abre o painel fontes depois que você clica em **log. js: 2**  
    > ! [DevTools abre o painel fontes depois que você clica em log. js: 2] [ImageSourceLog]  
    
1.  Navegue de volta para o console usando qualquer um dos fluxos de trabalho a seguir:  
    
    *   Clique na guia **console** .  
    *   Pressione `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) até que o painel do console esteja em foco.  
    *   [Abra o menu de comando][DevToolsCommandMenu], comece `Console` a digitar, selecione o comando **Mostrar painel do console** e pressione `Enter` .  
    
1.  Clique no botão **aviso de log** na demonstração.  `Abandon Hope All Ye Who Enter` é registrado no console.  As mensagens formatadas assim são avisos.  
    
    > ##### Figura 8  
    > O console após clicar em **aviso de log**  
    > ! [O console após clicar em aviso de log] [ImageConsoleLogWarning]  
    
    > [!TIP]
    > Se você quiser ver o código que causou a conexão de uma mensagem, clique em um script \ (como `log.js:12` \) para exibir o código que causou a formatação da mensagem.  

1.  Clique no ícone **expandir** ![ expansão ][ImageExpandIcon] na frente da `Abandon Hope All Ye Who Enter` .  DevTools mostra o [rastreamento de pilha][WikiStackTrace] que leva para a chamada.  
    
    > ##### Figura 9  
    > Um rastreamento de pilha  
    > ! [Um rastreamento de pilha] [ImageStackTrace]  
    
    O rastreamento de pilha informa que uma função nomeada `logWarning` foi chamada, que, por sua vez, chamou uma função nomeada `quoteDante` .  Em outras palavras, a chamada que aconteceu primeiro está na parte inferior do rastreamento de pilha.  Você pode fazer o log de rastreamentos de pilha a qualquer momento chamando `console.trace()` .  

1.  Clique em **log Error**.  A seguinte mensagem de erro é registrada: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### Figura 10  
    > Uma mensagem de erro  
    > ! [Uma mensagem de erro] [ImageLogError]  
    
1.  Clique em **tabela de log**.  Uma tabela sobre artistas famosos é registrada no console.  
    
    > [!NOTE]
    > A `birthday` coluna é apenas preenchida para uma linha.  Verifique o código para descobrir o motivo.
    
    > ##### Figura 11  
    > Uma tabela no console  
    > ! [Uma tabela no console] [ImageConsoleTable]  
    
1.  Clique em **grupo de log**.  Os nomes das 4 tartarugas famosas são agrupados sob a `Adolescent Irradiated Espionage Tortoises` etiqueta.  
    
    > ##### Figura 12  
    > Um grupo de mensagens no console  
    > ! [Um grupo de mensagens no console] [ImageConsoleLogGroup]  
    
1.  Clique em **log personalizado**.  Uma mensagem com uma borda vermelha e plano de fundo azul é registrada no console.  
    
    > ##### Figura 13  
    > Uma mensagem com formatação personalizada no console  
    > ! [Uma mensagem com formatação personalizada no console] [ImageConsoleLogCustomFormatting]  
    
A idéia principal aqui é que, quando você quiser registrar mensagens no console a partir de seu JavaScript, use um dos `console` métodos.  Cada método formata mensagens de maneira diferente.  

Há ainda mais métodos do que o que foi demonstrado nesta seção.  Este tutorial mostra como explorar o restante dos métodos.  

## Exibir mensagens registradas pelo navegador   

O navegador também registra mensagens no console.  Isso geralmente acontece quando há um problema com a página.  

1.  Clique em **causa 404**.  O navegador registra um `404` erro de rede porque o JavaScript da página tentou buscar um arquivo que não existe.  
    
    > ##### Figura 14  
    > Um erro do 404 no console  
    > ! [Um erro 404 no console] [ImageConsoleLogError]  
    
1.  Clique em **causa erro**.  O navegador registra uma não capturada `TypeError` porque o JavaScript está tentando atualizar um nó DOM que não existe.  
    
    > ##### Figura 15  
    > Um TypeError no console  
    > ! [Um TypeError no console] [ImageConsoleLogTypeError]  
    
1.  Clique na lista suspensa **níveis de log** e habilite a opção **detalhado** se estiver desabilitada.  Saiba mais sobre a filtragem na próxima seção.  Você precisa fazer isso para certificar-se de que a próxima mensagem que você registrar está visível.  
    
    > ##### Figura 16  
    > Habilitando o nível de log **detalhado**  
    > ! [Habilitando o nível de log detalhado] [ImageVerboseLogLevel]  
    
1.  Clique em **causa violação**.  A página deixa de responder por alguns segundos e, em seguida, o navegador registra a mensagem no `[Violation] 'click' handler took 3000ms` console.  A duração exata pode variar.  
    
    > ##### Figura 17  
    > Uma violação no console  
    > ! [Uma violação no console] [ImageConsoleLogViolation]  
    
## Filtrar mensagens   

Em algumas páginas, o console fica inundado com mensagens.  O DevTools oferece várias maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.  

### Filtrar por nível de log   

Cada `console` método é atribuído a um nível de gravidade: `Verbose` ,, `Info` `Warning` ou `Error` .  Por exemplo, `console.log()` é uma `Info` mensagem de nível um, enquanto `console.error()` é uma `Error` mensagem de nível um.  

1.  Clique na lista suspensa **níveis de log** e desabilite os **erros**.  Um nível fica desabilitado quando não há mais uma marca de opção ao lado dele.  As `Error` mensagens de nível desaparecerão.  
    
    > ##### Figura 18  
    > Desativando `Error` mensagens de nível no console  
    > ! [Desativando mensagens de nível de erro no console] [ImageConsoleDisablingLogError]  
    
1.  Clique novamente na lista suspensa **níveis de log** e ative novamente os **erros**.  As `Error` mensagens de nível reexibida.  

### Filtrar por texto   

Quando quiser exibir apenas as mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na caixa de texto **filtro** .  

1.  Digite `Dave` na caixa de texto **filtro** .  Todas as mensagens que não incluem a cadeia de caracteres `Dave` estão ocultas.  Você também pode ver o `Adolescent Irradiated Espionage Tortoises` rótulo.  Isso é um bug.  
    
    > ##### Figura 19  
    > Filtragem de qualquer mensagem que não inclua `Dave`  
    > ! [Filtragem de qualquer mensagem que não inclua Dave] [ImageLogTextFiltering]  
    
1.  Excluir `Dave` na caixa de texto **Filtrar** .  Todas as mensagens reaparecem.  

### Filtrar por expressão regular   

Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].  

1.  Digite `/^[AH]/` na caixa de texto **filtro** .  Digite esse padrão no [regexr][|::ref1::|Main] para obter uma explicação do que ele está fazendo.  
    
    > ##### Figura 20  
    > Filtragem de qualquer mensagem que não corresponda ao padrão `/^[AH]/`  
    > ! [Filtrar qualquer mensagem que não corresponda a um padrão] [ImageLogRegExFiltering]  
    
1.  Excluir `/^[AH]/` na caixa de texto **Filtrar** .  Todas as mensagens ficarão visíveis novamente.  

### Filtrar por fonte de mensagem   

Quando quiser exibir apenas as mensagens que vieram de determinada URL, use a **barra lateral**.  

1.  Clique em **Mostrar barra lateral do console** ![ Mostrar barra lateral do console ][ImageShowConsoleSidebarIcon] .  
    
    > ##### Figura 21  
    > A barra lateral  
    > ! [A barra lateral] [ImageConsoleSidebar]  
    
1.  Clique no ícone **expandir** ![ expansão ][ImageExpandIcon] ao lado do número de mensagens.  Na [Figura 21](#figure-21), o número de mensagens é indicado como **13 mensagens**.  A **barra lateral** mostra uma lista de URLs que fizeram o registro das mensagens.  Por exemplo, `log.js` causou 11 mensagens.  
    
    > ##### Figura 22  
    > Exibindo a fonte de mensagens na barra lateral  
    > ! [Exibindo a fonte de mensagens na barra lateral] [ImageConsoleSidebarLogSource]  
    
### Filtrar por mensagens de usuário   

Antes, quando você clicou em **registrar informações**, um script chamado para `console.log('Hello, Console!')` registrar a mensagem no console.  As mensagens registradas do JavaScript como essa são chamadas de **mensagens de usuário**.  Por outro lado, quando você clicou em **causa 404**, o navegador registrou uma `Error` mensagem de nível informando que o recurso solicitado não foi encontrado.  Mensagens como essa são consideradas **mensagens do navegador**.  Use a **barra lateral** para filtrar mensagens do navegador e mostrar apenas mensagens de usuário.  

1.  Clique em **9 mensagens de usuário**.  As mensagens do navegador estão ocultas.  
    
    > ##### Figura 23  
    > Filtrando mensagens do navegador  
    > ! [Filtrando mensagens do navegador] [ImageConsoleLogBrowserFiltering]  
    
1.  Clique em **13 mensagens** para mostrar todas as mensagens novamente.  

## Usar o console juntamente com qualquer outro painel   

E se você estiver editando estilos, mas precisar verificar rapidamente o log do console para algo? Use a gaveta.  

1.  Clique na guia **elementos** .  
1.  Pressione `Escape` .  A guia Console da **gaveta** será aberta.  Ele tem todos os recursos do painel do console que você estava usando em todo este tutorial.  
    
    > ##### Figura 24  
    > A guia Console na gaveta  
    > ! [A guia Console na gaveta] [ImageDrawerConsole]  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Figura 1: mensagens no console"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-Right-console.msft.png "Figura 2: DevTools abre à direita da demonstração"  
[ImageDevToolsBottom]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-Bottom-console.msft.png "Figura 3: DevTools encaixado na parte inferior da demonstração"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-separate-console-Browse.msft.png "Figura 4: navegador em uma janela separada"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-separate-console-devtools.msft.png "Figura 5: DevTools desencaixado em uma janela separada"  
[ImageLogInfo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-info.msft.png "Figura 6: o console após clicar em informações do log"  
[ImageSourceLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-sources-logjs.msft.png "Figura 7: DevTools abre o painel fontes depois que você clica em log. js: 2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Warning.msft.png "Figura 8: o console após clicar em aviso do log"  
[ImageStackTrace]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Warning-Expanded.msft.png "Figura 9: um rastreamento de pilha"  
[ImageLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Error.msft.png "Figura 10: uma mensagem de erro"  
[ImageConsoleTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Table.msft.png "Figura 11: uma tabela no console"  
[ImageConsoleLogGroup]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Group.msft.png "Figura 12: um grupo de mensagens no console"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Custom.msft.png "Figura 13: uma mensagem com formatação personalizada no console"  
[ImageConsoleLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-404.msft.png "Figura 14: um erro 404 no console"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-Error.msft.png "Figura 15: uma TypeError no console"  
[ImageVerboseLogLevel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-error-log-Levels.msft.png "Figura 16: Habilitando o nível de log detalhado"  
[ImageConsoleLogViolation]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-Violation.msft.png "figura 17: uma violação no console"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-Violation-log-Levels.msft.png "Figura 18: Desativando mensagens de nível de erro no console"  
[ImageLogTextFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-All-Messages-Text-Filter.msft.png "Figura 19: filtrando qualquer mensagem que não inclua Dave"  
[ImageLogRegExFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-All-Messages-Regex-Filter.msft.png "Figura 20: filtrando qualquer mensagem que não corresponda a um padrão"  
[ImageConsoleSidebar]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-All-Messages.msft.png "figura 21: a barra lateral"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-Expanded-All-Messages.msft.png "Figura 22: exibindo a fonte de mensagens na barra lateral"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-User-messages.msft.png "Figura 23: filtrando mensagens do navegador"  
[ImageDrawerConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Elements-Drawer-console-Sidebar-All-Messages.msft.png "Figura 24: a guia Console na gaveta"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Referência do console"  

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
