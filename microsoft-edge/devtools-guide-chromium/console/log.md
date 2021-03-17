---
description: Saiba como registrar mensagens no Console.
title: Começar a registrar mensagens no Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: fb428154b00959db1627096819c565dd5dc11346
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439286"
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

# <a name="get-started-with-logging-messages-in-the-console"></a>Começar a registrar mensagens no Console  

Este tutorial interativo mostra como registrar e filtrar mensagens no [console do Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensagens no Console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Mensagens no **Console**  
:::image-end:::  

Este tutorial destina-se a ser concluído em ordem.  Ele supõe que você entenda os fundamentos do desenvolvimento da Web, como como usar JavaScript para adicionar interatividade a uma página.  

## <a name="set-up-the-demo-and-devtools"></a>Configurar a demonstração e o DevTools  

Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho por conta própria.  Quando você acompanha fisicamente, é mais provável que você se lembre mais tarde dos fluxos de trabalho.  

1.  Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Exemplos** de Log de Console para abrir em uma nova guia.  
    
    [Exemplos de log de console][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Concentre a demonstração e selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\) para abrir o DevTools.  Por padrão, o DevTools é aberto à direita da demonstração.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools abre à direita da demonstração" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools abre à direita da demonstração  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Dock DevTools na parte inferior da janela][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools encaixado na parte inferior da demonstração" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools encaixado na parte inferior da demonstração  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Desfazer DevTools em uma janela separada.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navegador em uma janela separada" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Navegador em uma janela separada  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Desfazer DevTools em uma janela separada.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desfazida em uma janela separada" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools desfazida em uma janela separada  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a>Exibir mensagens registradas no JavaScript  

A maioria das mensagens exibidas no **Console vem** dos desenvolvedores da Web que escreveram o JavaScript da página.  O objetivo desta seção é apresentar os diferentes tipos de mensagem que você provavelmente revisará no **Console**e explicar como você pode registrar cada tipo de mensagem por conta própria do seu próprio JavaScript.  

1.  Escolha o **botão Informações de** Log na demonstração.  `Hello, Console!` é registrado no Console.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="O Console depois de escolher Informações de Log" lightbox="../media/console-log-info.msft.png":::
       O **Console depois** de escolher Informações de **Log**  
    :::image-end:::  
    
1.  Ao lado da `Hello, Console!` mensagem no Console, escolha **log.js:2**.  O painel Fontes abre e realça a linha de código que fez com que a mensagem seja registrada no Console.  A mensagem foi registrada quando o JavaScript da página foi executar `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="O DevTools abre a ferramenta Sources depois que você log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       O DevTools abre a **ferramenta Sources** depois de escolher `log.js:2`  
    :::image-end:::  
    
1.  Navegue até **o Console** usando qualquer um dos seguintes fluxos de trabalho:  
    
    *   Escolha a **ferramenta Console.**  
    *   Selecione `Control` + `[` \(Windows, Linux\) ou `Command` + `[` \(macOS\) até que a **ferramenta Console** está em foco.  
    *   [Abra o Menu de Comando][DevToolsCommandMenu], digite , escolha o comando Mostrar Painel de `Console` **Console** e selecione `Enter` .  
    
1.  Escolha o **botão Aviso de** Log na demonstração.  `Abandon Hope All Ye Who Enter` é registrado no **Console**.  Mensagens formatadas assim são avisos.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="O Console depois de escolher Aviso de Log" lightbox="../media/console-log-warning.msft.png":::
       O **Console depois** de escolher Aviso de **Log**  
    :::image-end:::  
    
    > [!TIP]
    > Se você quiser exibir o código que fez com que uma mensagem fosse registrada de uma determinada maneira, escolha em um script \(como \) para exibir o código que fez com que a mensagem fosse `log.js:12` formatada.  

1.  Escolha o **ícone Expandir** \( ![ Expand ](../media/expand-icon.msft.png) \) na frente de `Abandon Hope All Ye Who Enter` .  DevTools mostra o [rastreamento de][WikiStackTrace] pilha que antecede a chamada.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Um rastreamento de pilha" lightbox="../media/console-log-warning-expanded.msft.png":::
       Um rastreamento de pilha  
    :::image-end:::  
    
    O rastreamento de pilha está dizendo que uma função chamada é executado, que, por sua `logWarning` vez, executa uma função chamada `quoteDante` .  Em outras palavras, a solicitação que aconteceu primeiro está na parte inferior do rastreamento de pilha.  Você pode registrar rastreamentos de pilha a qualquer momento executando `console.trace()` .  

1.  Escolha **Erro de Log**.  A seguinte mensagem de erro é registrada: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Uma mensagem de erro" lightbox="../media/console-log-error.msft.png":::
       Uma mensagem de erro  
    :::image-end:::  
    
1.  Escolha **Tabela de Log**.  Uma tabela sobre os artistas famoso é registrada no **Console**.  
    
    > [!NOTE]
    > A `birthday` coluna só é preenchida por uma linha.  Revise o código para determinar por que isso é.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Uma tabela no Console" lightbox="../media/console-log-table.msft.png":::
       Uma tabela no **Console**  
    :::image-end:::  
    
1.  Escolha **Grupo de Log**.  Os nomes de 4 tartarugas que combatem crimes são agrupados sob o `Adolescent Irradiated Espionage Tortoises` rótulo.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Um grupo de mensagens no Console" lightbox="../media/console-log-group.msft.png":::
       Um grupo de mensagens no **Console**  
    :::image-end:::  
    
1.  Escolha **Log Personalizado**.  Uma mensagem com borda vermelha e plano de fundo azul é registrada no Console.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Uma mensagem com formatação personalizada no Console" lightbox="../media/console-log-custom.msft.png":::
       Uma mensagem com formatação personalizada no **Console**  
    :::image-end:::  
    
A ideia principal aqui é que, quando você deseja registrar mensagens no Console do JavaScript, use um dos `console` métodos.  Cada método formatará mensagens de forma diferente.  

Há ainda mais métodos do que o que foi demonstrado nesta seção.  Este tutorial mostra como explorar o restante dos métodos.  

## <a name="view-messages-logged-by-the-browser"></a>Exibir mensagens registradas pelo navegador  

O navegador registra mensagens no Console também.  Isso geralmente acontece quando há um problema com a página.  

1.  Escolha **Causa 404**.  O navegador registra um código de status HTTP de erro de rede porque o JavaScript da página tentou buscar um `404` arquivo que não existe.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Um erro 404 no Console" lightbox="../media/console-cause-404.msft.png":::
       Um `404` erro no **Console**  
    :::image-end:::  
    
1.  Escolha **Causar Erro**.  O navegador registra um arquivo não detectado porque o JavaScript está tentando atualizar um nó `TypeError` DOM que não existe.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Um TypeError no Console" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` no **Console**  
    :::image-end:::  
    
1.  Escolha o **menu suspenso Níveis de** Log e habilita a opção **Verbose** se estiver desabilitada.  Saiba mais sobre filtragem na próxima seção.  Você precisa fazer isso para garantir que a próxima mensagem que você registrar está visível.  
    
    > [!NOTE]
    > Se a lista de menus padrão Níveis estiver desabilitada, talvez seja necessário fechar **a** Barra Lateral do Console.  Filtrar por Fonte de Mensagem abaixo para obter mais informações sobre a Barra Lateral **do** Console.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitando o nível de log Detalhado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Habilitando o nível de log Detalhado  
    :::image-end:::  
    
1.  Escolha **Violação de Causa**.  A página fica sem resposta por alguns segundos e, em seguida, o navegador registra a mensagem `[Violation] 'click' handler took 3000ms` no Console.  A duração exata pode variar.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Uma violação no Console" lightbox="../media/console-cause-violation.msft.png":::
       Uma violação no **Console**  
    :::image-end:::  
    
## <a name="filter-messages"></a>Filtrar mensagens  

Em algumas páginas da Web, você revisa **o Console** e é inundado de mensagens.  O DevTools fornece muitas maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.  

### <a name="filter-by-log-level"></a>Filtrar por nível de log  

Cada `console` método recebe um nível de severidade: , , ou `Verbose` `Info` `Warning` `Error` .  Por exemplo, `console.log()` é uma mensagem de `Info` nível, enquanto é uma mensagem `console.error()` de `Error` nível.  

1.  Escolha o **menu suspenso Níveis de** Log e desabilite **Erros**.  Um nível é desabilitado quando não há mais uma marca de seleção ao lado dele.  As `Error` mensagens de nível desaparecem.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Desabilitar mensagens de nível de erro no Console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Desabilitar mensagens de nível de erro no **Console**  
    :::image-end:::  
    
1.  Escolha o **menu suspenso Níveis de** Log novamente e reabilitar **Erros**.  As `Error` mensagens de nível reaparecem.  

### <a name="filter-by-text"></a>Filtrar por texto  

Quando você deseja exibir apenas mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na **caixa de texto Filtrar.**  

1.  Digite `Dave` na caixa de **texto** Filtrar.  Todas as mensagens que não incluem a cadeia de `Dave` caracteres estão ocultas.  Você também pode revisar o `Adolescent Irradiated Espionage Tortoises` rótulo.  Isso é um bug.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrar qualquer mensagem que não inclua Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Filtrar qualquer mensagem que não inclua `Dave`  
    :::image-end:::  
    
1.  Excluir `Dave` da caixa de **texto** Filtro.  Todas as mensagens reaparecem.  

### <a name="filter-by-regular-expression"></a>Filtrar por expressão regular  

Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].  

1.  Digite `/^[AH]/` na caixa de **texto** Filtrar.  Digite o padrão em [RegExr][|::ref1::|Main] para uma explicação do que ele está fazendo.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrando qualquer mensagem que não corresponder a um padrão" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Filtrando qualquer mensagem que não corresponder ao padrão `/^[AH]/`  
    :::image-end:::  
    
1.  Excluir `/^[AH]/` da caixa de **texto** Filtro.  Todas as mensagens estão visíveis novamente.  

### <a name="filter-by-message-source"></a>Filtrar por fonte de mensagem  

Quando você quiser exibir apenas as mensagens que vieram de uma determinada URL, use a **barra lateral**.  

1.  Escolha **Mostrar Barra Lateral do Console** \( Mostrar Barra Lateral do Console ![ ](../media/show-console-sidebar-icon.msft.png) \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="A barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       A barra lateral  
    :::image-end:::  
    
1.  Escolha o **ícone Expandir** \( ![ Expand ](../media/expand-icon.msft.png) \) ao lado do número de mensagens.  Na figura a seguir, o número de mensagens é indicado como **13 Mensagens**.  A **barra lateral** mostra uma lista de URLs que causaram o registro de mensagens.  Por exemplo, `log.js` causou 11 mensagens.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Exibindo a origem das mensagens na barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Exibindo a origem das mensagens na barra lateral  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a>Filtrar por mensagens de usuário  

Anteriormente, quando você escolhe **Informações de Log**, um script chamado para registrar a mensagem no `console.log('Hello, Console!')` Console.  As mensagens registradas no JavaScript como esta são chamadas **de mensagens de usuário**.  Por outro lado, quando você escolhe **Causa 404**, o navegador registra uma mensagem de nível informando que o recurso `Error` solicitado não foi encontrado.  Mensagens como essa são consideradas **mensagens do navegador**.  Use a **Barra lateral para** filtrar as mensagens do navegador e mostrar apenas mensagens do usuário.  

1.  Escolha **9 Mensagens de Usuário**.  As mensagens do navegador estão ocultas.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrando mensagens do navegador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Filtrando mensagens do navegador  
    :::image-end:::  
    
1.  Escolha **13 Mensagens para** mostrar todas as mensagens novamente.  

## <a name="use-the-console-alongside-any-other-tools"></a>Use o Console juntamente com qualquer outra ferramenta  

Se você estiver editando estilos, mas precisar verificar rapidamente o log do Console para algo, Use a Gaveta.  

1.  Escolha a **ferramenta Elementos.**  
1.  Selecione `Escape` .  A **ferramenta Console** na **Gaveta** é aberta.  Ele tem todos os recursos do painel console que você tem usado durante este tutorial.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="A ferramenta Console na Gaveta" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         A **ferramenta Console** na **Gaveta**  
    :::image-end:::  
    
## <a name="see-also"></a>Ver também  

*   Para explorar mais recursos e fluxos de trabalho relacionados à interface do usuário do **Console,** navegue até [Referência do Console][DevToolsConsoleApi].  
*   Para saber mais sobre todos os métodos demonstrados em Exibir mensagens registradas no JavaScript e explorar os outros métodos não abordados neste artigo, navegue até Referência da `console` API de [](#view-messages-logged-from-javascript) `console` [Console.][DevToolsConsoleReference]  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge \(Chromium\) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md "Console reference | Microsoft Docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Começar a registrar mensagens em log | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha - Wikipédia"  
> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/log) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
