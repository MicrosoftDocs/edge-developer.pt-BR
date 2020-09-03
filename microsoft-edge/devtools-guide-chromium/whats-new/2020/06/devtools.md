---
description: Recursos de depuração de grade CSS, solicitações de edição e reprodução com o console de rede e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 96ad9a4f21c36135013033fa4de31281fe6c4e83
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993608"
---
# O que há de novo no DevTools (Microsoft Edge 85)  

## Anúncios da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.  Veja os comunicados para experimentar novos recursos no DevTools, extensões de código VS e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga a equipe do Microsoft Edge devtools no Twitter][EdgeDevToolsTwitterAccount].  

### Recursos de depuração de grade CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

A equipe do Microsoft Edge DevTools está colaborando com o Chrome DevTools Team e na Comunidade Chromium para adicionar novos recursos de depuração de grade CSS ao DevTools.  Agora você pode exibir números de linha de grade, lacunas de grade e linhas de grade estendidas como uma sobreposição na página.  Além disso, mais melhorias nas ferramentas de grade serão disponibilizadas em breve.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Recursos de depuração de grade CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Recursos de depuração de grade CSS
:::image-end:::  

> [!NOTE]
> Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar novos recursos de depuração de grade CSS**.  
> 
> Para experimentar o experimento com um exemplo, consulte [exemplo de planejador de grade CSS][CodepenRachelweilYzwBzKM].  

Chromium problema [#1047356][CR1047356]  

### Editar e reproduzir solicitações com o console de rede  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Agora você pode usar **Editar e reproduzir** em solicitações no [log de rede][DevtoolsNetworkIndexLogActivity] usando o **console de rede**.  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar e reproduzir uma solicitação no NetworkLog com o console de rede" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Editar e reproduzir uma solicitação no [NetworkLog][DevtoolsNetworkIndexLogActivity] com o console de **rede**  
:::image-end:::  

Um novo painel, o **console de rede** abre na [gaveta devtools][DevtoolsCustomizeIndexDrawer] e preenche automaticamente com as informações da solicitação HTTP.  Para ver a resposta retornada do servidor, edite a solicitação \ (se necessário \) e selecione **Enviar**.  

Você também pode usar o **console de rede** para criar e enviar solicitações HTTP diretamente do devtools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Painel do console de rede" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Painel do **console de rede**  
:::image-end:::  

> [!TIP]
> Para ver o **console de rede** no painel main \ (superior \) em vez da [gaveta devtools][DevtoolsCustomizeIndexDrawer], consulte [movendo ferramentas entre painéis](#move-tools-between-panels).  

> [!NOTE]
> Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar console de rede**.  
> 
> Abra o [log de rede][DevtoolsNetworkIndexLogActivity], abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **Editar e reproduzir**.  

Chromium problema [#1093687][CR1093687]  

### Eventos do trabalho do respondWith eventos na guia intervalo  

A guia **intervalo** do painel **rede** agora inclui `respondWith` eventos de trabalho do serviço.  O `respondWith` evento de trabalho do serviço mostra a duração do tempo imediatamente antes de o manipulador de eventos do trabalho do serviço `fetch` começar a ser executado até o momento em que a `respondWith` promessa do `fetch` manipulador é liquidada.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="O evento de trabalho do serviço respondWith na guia intervalo do painel de rede" lightbox="../../media/2020/06/timing-tab.msft.png":::
   O `respondWith` evento de trabalho do serviço na guia **intervalo** do painel de **rede**  
:::image-end:::  

Expanda a **resposta recebida** para ver informações adicionais da `fetch` resposta como `CacheStorageCacheName` , `serviceWorkerResponseSource` e `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expandir a resposta recebida para ver informações adicionais da resposta de busca" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Expandir a **resposta recebida** para ver informações adicionais da `fetch` resposta  
:::image-end:::  

Chromium problema [#1066579][CR1066579]  

### Comentários da webhint no painel problemas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real sobre a acessibilidade, a compatibilidade entre navegadores, a segurança, o desempenho, a PWAs e outras questões de desenvolvimento da Web comuns dos sites.  Agora você pode ver comentários da webhint no painel [problemas][DevtoolsIssues] .  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Comentários da webhint no painel problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   Comentários da webhint no painel problemas  
:::image-end:::  

> [!NOTE]
> Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar webhint**.  
> 
> Abra o painel [problemas][DevtoolsIssues] para ver os comentários da webhint.  

Chromium problema [#1070378][CR1070378]  

### Ferramentas de movimentação entre painéis  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Normalmente, ferramentas como **elementos** e **rede** só podem ser abertas no painel main \ (Top \) do devtools.  Da mesma forma, ferramentas como **modo de exibição 3D** e **problemas** só podem ser abertos no painel gaveta \ (inferior \) do devtools.  Agora você pode personalizar o layout do DevTools movendo ferramentas entre os painéis superior e inferior.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover guias entre painéis" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Mover guias entre painéis  
:::image-end:::  

> [!NOTE]
> Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar o suporte para mover as guias entre painéis**.  

Chromium problema [#897944][CR897944]  

### Dica de ferramenta do iniciador aprimorada no painel rede  

No Microsoft Edge 83 e no 84, as dicas de ferramenta para a coluna do iniciador, que mostra a causa da solicitação do recurso, no [log de rede][DevtoolsNetworkIndexLogActivity] exibido com uma barra de rolagem horizontal.  Você só pôde ver a pilha de chamadas que iniciou a solicitação rolando horizontalmente na dica de ferramenta.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="A dica de ferramenta do iniciador no Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   A dica de ferramenta do iniciador no Microsoft Edge 84  
:::image-end:::  

Começando com o Microsoft Edge 85, agora você pode ver a pilha de chamadas do iniciador na dica de ferramenta sem rolar horizontalmente.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="A dica de ferramenta do iniciador no Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   A dica de ferramenta do iniciador no Microsoft Edge 85
:::image-end:::  

Chromium problema [#1069404][CR1069404]  

## Anúncios do projeto Chromium  

As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 85 que contribuíram para o projeto de código-fonte aberto Chromium.  

### Edição de estilo para estruturas CSS-in-JS  

Agora, o painel **estilos** tem melhor suporte para edição de estilos que foram criados com as APIs do [modelo de objeto CSS (CSSOM)][CsswgDraftsCssom] .  Muitas estruturas e bibliotecas CSS-in-JS usam as APIs CSSOM nos bastidores para construir estilos.  

Agora você pode editar estilos adicionados em JavaScript usando folhas de [estilo construíveis][WicgConstructStylesheet].  As folhas de estilo construíveis são uma nova maneira de criar e distribuir estilos reutilizáveis ao usar o [dom de sombra][MdnShadowDom].  

Por exemplo, os `h1` estilos adicionados com `CSSStyleSheet` \ (APIs CSSOM \) não eram editáveis anteriormente.  Os estilos são editáveis agora no painel **estilos** .  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Alterar a propriedade Background dos estilos H1 adicionados com CSSStyleSheet de rosa a LightBlue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Alterar a `background` propriedade dos `h1` estilos adicionados com `CSSStyleSheet` from `pink` to `lightblue` .
:::image-end:::  

Dê a esse recurso uma tentativa com um [exemplo que usa CSS-in-js][CodepenZoherghadyaliAbdgrpz].

Chromium problema [#946975][CR946975]  

### Lighthouse 6 no painel Lighthouse  

O painel **Lighthouse** agora está em execução Lighthouse 6.  Para obter uma lista completa de todas as alterações, consulte [notas de versão do v 6.0.0][GithubGoogleChromeLighthouse600].  

O Lighthouse 6,0 introduz três novas métricas para o relatório: maior pintura de conteúdo \ (LCP \), deslocamento de layout cumulativo \ (CLS \) e tempo de bloqueio total \ (TBT \).  

A fórmula de Pontuação de desempenho também foi reponderada para refletir melhor a experiência de carregamento do usuário.  

Chromium problema [#772558][CR772558]  

#### Primeira substituição de pintura significativa  

O primeiro pintura FMP \ (\) está obsoleto no Lighthouse 6,0.  O FMP também foi removido do painel **desempenho** .  **Maior pintura com conteúdo** é o substituto recomendado para FMP.  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Chromium problema [#1096008][CR1096008]  

### Suporte para novos recursos de JavaScript  

O DevTools agora tem melhor suporte para alguns dos recursos de linguagem JavaScript mais recentes.  

:::row:::
   :::column span="1":::
      Conclusão automática da sintaxe de [encadeamento opcional][V8DevOptionalChaining]  
   :::column-end:::
   :::column span="2":::
      A conclusão automática de propriedades no **console** agora oferece suporte à sintaxe de encadeamento opcional, por exemplo,  `name?.` agora funciona além de `name.` e `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Realce de sintaxe para [campos particulares][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      os campos de classe particular agora têm a sintaxe corretamente realçada e bem impressas no painel **fontes** .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Realce de sintaxe para [operadora de União NULL][V8DevNullishCoalescing] esficado
   :::column-end:::
   :::column span="2":::
      Agora, o DevTools agora realmente imprime o operador de União NULL esficado no painel **fontes** .  
   :::column-end:::
:::row-end:::  

Problemas com o Chromium [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]  

### Novos avisos de atalho do aplicativo no painel manifesto  

Os **atalhos do aplicativo** ajudam os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.  

<!--todo: add App shortcuts when section is live  -->  

O painel **manifestar** agora mostra avisos para as seguintes condições.  

* Os ícones de atalho do aplicativo são menores do que 96x96 pixels  
* Os ícones de atalho e os ícones de manifesto do aplicativo não são quadrados \ (já que os ícones são ignorados \)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avisos de atalho do aplicativo" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Avisos de atalho do aplicativo  
:::image-end:::  

Chromium problema [#955497][CR955497]  

### Exibição consistente do painel calculado  

O painel **calculado** no painel de **elementos** agora é exibido consistentemente em um painel em todos os tamanhos do visor.  Anteriormente, o painel **calculado** foi mesclado dentro do painel **estilos** quando a largura do visor devtools era estreita.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="O painel calculado é exibido consistentemente como um painel separado, mesmo quando o DevTools é estreito" lightbox="../../media/2020/06/computed-pane.msft.png":::
   O painel **calculado** é exibido consistentemente como um painel separado, mesmo quando os devtools são estreitos.
:::image-end:::  

Chromium problema [#1073899][CR1073899]  

### Deslocamentos de código de bytes para arquivos Webassembly  

O DevTools agora usa deslocamentos de código de bytes para exibir números de linha de desmontagem de WASM.  
Os números de linha tornam mais claro que você está olhando para dados binários e é mais consistente com a maneira como o tempo de execução do WASM faz referência a locais.  

Chromium problema [#1071432][CR1071432]  

### Painel copiar e recortar linhas em fontes  

Ao fazer a cópia ou recortar sem seleção no [Editor de painel fontes][DevtoolsSourcesEditCssJavascript], o devtools copia ou recorta a linha atual do conteúdo.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Com o cursor no final da linha 5, copiar a linha inteira de pen.js no DevTools e colar em um código VS" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Com o cursor no final da linha 5, copiar a linha inteira de **pen.js** no devtools e colar no [vs Code][VSCode].
:::image-end:::  

Chromium problema [#800028][CR800028]

### Atualizações de configurações do console  

#### Desagrupar as mesmas mensagens do console  

A opção de alternância **semelhante em grupo** nas configurações do console agora se aplica a mensagens duplicadas.  Anteriormente, ele era aplicado apenas a mensagens semelhantes.  

Por exemplo, anteriormente, o DevTools não desagrupau as `hello` mensagens, apesar de o **grupo semelhante** não estar desmarcado.  Agora, as `hello` mensagens são desagrupadas.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Quando o grupo semelhante está desmarcado, as mensagens de saudação são desagrupadas" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Quando o **grupo semelhante** está desmarcado, as `hello` mensagens são desagrupadas.
:::image-end:::  

Dê esse recurso uma tentativa com um [exemplo que envia mensagens duplicadas ao console][CodepenZoherghadyaliZyrjgdJ].  

Chromium problema [#1082963][CR1082963]  

### Mantendo somente as configurações de contexto selecionado  

As configurações de **contexto selecionado somente** em configurações do console agora são mantidas.  Anteriormente, as configurações foram redefinidas toda vez que você fechou e reabriu o DevTools.  A alteração torna o comportamento de configuração consistente com outras opções de configurações do console.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuração somente contexto selecionada" lightbox="../../media/2020/06/selected-context.msft.png":::
   Configuração **somente contexto selecionada**  
:::image-end:::  

Chromium problema [#1055875][CR1055875]  

### Atualizações do painel de desempenho  

#### Informações de cache de compilação JavaScript no painel desempenho  

[As informações do cache de compilação do JavaScript][V8DevCodeCaching] agora são sempre exibidas na guia Resumo do painel desempenho.  Anteriormente, o DevTools não mostraria nada relacionado ao cache de código se o cache de código não existisse.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informações do cache de compilação JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Informações do cache de compilação JavaScript  
:::image-end:::  

Chromium problema [#912581][CR912581]  

#### Alinhamento do tempo de navegação no painel desempenho  

O painel de **desempenho** usado para mostrar horas nas réguas com base na hora de início da gravação.  O intervalo foi alterado para gravações nas quais o usuário navega, onde DevTools agora mostra as horas da régua em relação à navegação em vez disso.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinhar o intervalo de navegação no painel de desempenho" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Alinhar o intervalo de navegação no painel de **desempenho**  
:::image-end:::  

As horas para `DOMContentLoaded` , primeiro pintura, primeira pintura com conteúdo e maiores eventos de pintura com conteúdo são atualizadas para serem relativas ao início da navegação, o que significa que o intervalo corresponde aos intervalos relatados por `PerformanceObserver` .  

Chromium problema [#974550][CR974550]  

### Novos ícones para pontos de interrupção, pontos de interrupção condicionais e logpoints  

O painel **fontes** tem novos designs para pontos de interrupção, pontos de interrupção condicionais e logpoints.  Os pontos de interrupção são representados por um círculo vermelho, da mesma forma que o [código vs][VSCode] e o [Visual Studio][VS].  Ícones são adicionados para diferenciar pontos de interrupção condicionais e logpoints.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Pontos de interrupção" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Pontos de interrupção  
:::image-end:::  

Chromium problema [#1041830][CR1041830]  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Visão geral do painel Editar CSS e JavaScript-fontes | Documentos da Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edição de estilo para estruturas CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensagens duplicadas para o console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemplo de Planner de grade CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: Atualize para a versão mais recente do Lighthouse | Erros de Chromium"  
[CR800028]: https://crbug.com/800028 "O atalho de linha duplicada no editor de ferramentas de desenvolvedor não está funcionando após a atualização do Chrome | Erros de Chromium"  
[CR912581]: https://crbug.com/912581 "Expor quais scripts foram armazenados em cache por V8 no DevTools/about: Tracing | Erros de Chromium"  
[CR946975]: https://crbug.com/946975 "A barra lateral estilos DevTools não funciona com folhas de estilos construídas | Erros de Chromium"  
[CR955497]: https://crbug.com/955497 "Menu de atalho do ícone do aplicativo para PWAs | Erros de Chromium"  
[CR974550]: https://crbug.com/974550 "Diferença de métrica entre o painel perf e performanceObserver | Erros de Chromium"  
[CR1041830]: https://crbug.com/1041830 "Melhorar as cores dos pontos de interrupção | Erros de Chromium"  
[CR1055875]: https://crbug.com/1055875 "O valor da configuração do console somente contexto selecionado não persiste após fechar e reabrir as ferramentas de desenvolvedor | Erros de Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: show inworkrs busca a linha do tempo por solicitação no painel de rede | Erros de Chromium"  
[CR1071432]: https://crbug.com/1071432 "WASM experiência básica para desenvolvedores | Erros de Chromium"  
[CR1073899]: https://crbug.com/1073899 "Guia estilo calculado desaparece no modo responsivo | Erros de Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: o realce de sintaxe não funciona com campos particulares | Erros de Chromium"  
[CR1082963]: https://crbug.com/1082963 "Não é possível desativar o comportamento de mensagens semelhantes em grupo do console | Erros de Chromium"  
[CR1083214]: https://crbug.com/1083214 "o Acorn não dá suporte a encadeamento opcional | Erros de Chromium"  
[CR1083797]: https://crbug.com/1083797 "Impressão bonita interrompida para União nula esficarada | Erros de Chromium"  
[CR1096008]: https://crbug.com/1096008 "Remover FMP | Erros de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Ferramentas de grade/flexbox/tabela CSS | Erros de Chromium"  
[CR1093687]: https://crbug.com/1093687 "Crie uma ferramenta para criar e reproduzir solicitações de rede sintéticas | Erros de Chromium"  
[CR1070378]: https://crbug.com/1070378 "Integrar dica WebA DevTools | Erros de Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Ferramentas de desenvolvimento] os pop-ups do widget são muito estreitas | Erros de Chromium"  
[CR897944]: https://crbug.com/897944 "Painéis devtool arrastáveis | Erros de Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema-MicrosoftDocs/Edge-Developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Usando o DOM de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canais de visualização do Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Código do Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objeto CSS (CSSOM) | Rascunhos do editor de grupo de trabalho W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de classe particular-campos de classe pública e particular | V8. Dispositivos"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Cache de código para desenvolvedores de JavaScript | V8. Dispositivos"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "União esnulada nula | V8. Dispositivos"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Encadeamento opcional | V8. Dispositivos"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de folha de estilos construíveis | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "A Web que queremos"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/06/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
