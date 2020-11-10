---
description: Conheça o título das Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)
title: O autor do Título das ferramentas para desenvolvedores do Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, f12 tools, devtools
experimental: true
experiment_id: "51fe4b97-3e55-41"
ms.localizationpriority: high
---

# Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)  

[!INCLUIR[new-devtools-version-note](includes/new-devtools-version-note.md)]  

O Microsoft Edge (EdgeHTML) DevTools é compilado com [TypeScript][TypeScriptIndex], da plataforma [abrir fonte][GithubMicrosoftChakracore], otimizado para os fluxos de trabalho de front-end modernos e agora está disponível como um [aplicativo autônomo do Windows 10][MicrosoftStoreEdgeDevtoolsPreview] na Microsoft Store!  

Para saber mais sobre os recursos mais recentes, confira [DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Ferramentas principais  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft Edge (EdgeHTML) DevTools":::
  Microsoft Edge (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

O Microsoft Edge (EdgeHTML) DevTools inclui:  

*   Um painel de [Elementos][DevtoolsGuideEdgehtmlElements] para editar HTML e CSS, inspecionar propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de mutação DOM  
*   Um [Console][DevtoolsGuideEdgehtmlConsole] para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós DOM e executar JavaScript no contexto da janela ou quadro selecionado  
*   Um [Depurador][DevtoolsGuideEdgehtmlDebugger] para percorrer o código, definir inspeções e pontos de interrupção, editar seu código ao vivo e inspecionar o armazenamento da Web e os caches de cookies  
*   Um painel de [Rede][DevtoolsGuideEdgehtmlNetwork] para monitorar e inspecionar solicitações e respostas do cache da rede e do navegador  
*   Um painel de [Desempenho][DevtoolsGuideEdgehtmlPerformance] para criar um perfil de tempo e recursos do sistema necessários para o seu site  
*   Um painel de [Memória][DevtoolsGuideEdgehtmlMemory] para medir o uso dos recursos de memória e comparar os instantâneos da memória em diferentes estados de tempo de execução de código  
*   Um painel de [Armazenamento][DevtoolsGuideEdgehtmlStorage] para inspecionar e gerenciar seu armazenamento da Web, IndexedDB, cookies e dados de cache  
*   Um painel de [Trabalhos de Serviço][DevtoolsGuideEdgehtmlServiceworkers] para gerenciar e depurar seus profissionais de serviço  
*   Um painel de [Emulação][DevtoolsGuideEdgehtmlEmulation] para testar o seu site com diferentes perfis de navegador, resoluções de tela e coordenadas de local GPS  

Continue enviando seus [comentários e solicitações de recursos](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [! DICA]
> [Testar no Microsoft Edge (EdgeHTML) sem qualquer navegador][BrowserstackEdgehtml].  
> A equipe do Microsoft Edge é parceira com [BrowserStack][BrowserstackEdgehtml] para fornecer testes gratuitos e automatizados no Microsoft Edge (EdgeHTML).  

## Aplicativo da Microsoft Store  

O **Microsoft Edge (EdgeHTML) DevTools** agora está [disponível][DevtoolsGuideEdgehtmlWhatsnew] como um [Aplicativo autônomo Windows 10 da Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], além da experiência de ferramentas do navegador (`F12`). Com a versão do armazenamento, há um painel **seletor** para anexar a abrir destinos de página locais e remotos e um layout com guias para alternar entre instâncias DevTools.  

### Depuração local  

Para depurar uma página localmente, basta iniciar o aplicativo Microsoft Edge DevTools. O painel **Local** do seletor exibirá todos os processos de conteúdo ativos do EdgeHTML, incluindo as guias abrir navegador do Microsoft Edge, executando os processos [PWAs][PwasEdgehtmlIndex] (`WWAHost.exe`) e [os controles do modo de exibição da Web][HostingWebview]. Selecione seu destino desejado para anexar e abra uma nova instância da guia do DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="DevTools app Local panel":::
  Painel Local do aplicativo DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Depuração remota  

O aplicativo Microsoft Edge DevTools introduz o suporte básico para depurar páginas em um computador remoto por meio de nosso novo [Protocolo de DevTools][DevtoolsProtocolEdgehtmlIndex]. Com a versão mais recente vem o acesso remoto à funcionalidade central no [Depurador][DevtoolsGuideEdgehtmlDebugger], [Elementos][DevtoolsGuideEdgehtmlElements] (para operações somente leitura) e painéis do [Console][DevtoolsGuideEdgehtmlConsole]. O depurador remoto está limitado ao Microsoft Edge (EdgeHTML) que executa hosts da área de trabalho, com suporte para outros hosts EdgeHTML e dispositivos com Windows 10 chegando nas versões futuras.  

Para começar, confira a seção [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] de documentos [DevTools][DevtoolsProtocolEdgehtmlIndex].  

:::image type="complex" source="./devtools-guide/media/chooser\_remote.png" alt-text="DevTools app Remote panel":::
  Painel remoto do aplicativo DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Atalhos Gerais  

> [! IMPORTANTE]
> Todos os atalhos foram verificados na versão mais recente do Windows.  
> Se não for possível usar um atalho, atualize sua cópia do Windows.  

Esses atalhos controlam a janela principal do DevTools e devem funcionar em todas as ferramentas.  

| Ação | Atalho |  
|:--- |:--- |  
| Mostrar/Ocultar DevTools (abre para o último painel exibido) | `F12`, `Ctrl`+`Shift`+`I` |  
| Alternar encaixe (Desencaixar/Abaixo/Direita) | `Ctrl`+`Shift`+`D` |  
| Abrir arquivo | `Ctrl`+`P`, `Ctrl`+`O` |  
| Mostrar código-fonte HTML não editável no Depurador | `Ctrl`+`U` |  
| Mostrar/ocultar Console na parte inferior de qualquer outra ferramenta | `Ctrl`+`` ' `` |  
| Alternar para Elementos (Explorador do DOM) | `Ctrl`+`1` |  
| Alternar para o Console | `Ctrl`+`2` |  
| Alternar para o Depurador | `Ctrl`+`3` |  
| Alternar para a Rede | `Ctrl`+`4` |  
| Alternar para o Desempenho | `Ctrl`+`5` |  
| Alternar para Memória | `Ctrl`+`6` |  
| Alternar para Emulação | `Ctrl`+`7` |  
| Documento de ajuda | `F1` |  
| Próxima ferramenta | `Ctrl`+`F6` |  
| Ferramenta anterior | `Ctrl`+`Shift`+`F6` |  
| Ferramenta anterior (do histórico) | `Ctrl`+`Shift`+`[` |  
| Próxima ferramenta (do histórico) | `Ctrl`+`Shift`+`]` |  
| Subquadro Seguinte | `F6` |  
| Subquadro Anterior | `Turno`+`F6` |  
| Próxima correspondência na caixa de Pesquisa | `F3` |  
| Correspondência anterior na caixa de Pesquisa | `Shift`+`F3` |  
| Procurar na caixa de pesquisa | `Ctrl`+`F` |  
| Focalizar o console na parte inferior | `Alt`+`Shift`+`I` |  
| Iniciar o DevTools para Console | `Ctrl`+`Shift`+`J` |  
| Atualizar a página | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [! OBSERVAÇÃO]
> se você estiver depurando e pausado em um ponto de interrupção, a ação **Atualizar a página** retoma o tempo de execução primeiro.  

## Entre em contato com a equipe do Microsoft Edge DevTools  

Envie seus comentários para ajudar a melhorar o Microsoft Edge (EdgeHTML) DevTools para você! Basta abrir as ferramentas (`F12`) e selecionar o botão [Enviar comentários](#microsoft-edge-edgehtml-developer-tools).  

Torne-se um [Participante do Programa Windows Insider][WindowsInsiderProgram] para visualizar os [recursos mais recentes que estão chegando no DevTools][DevtoolsGuideEdgehtmlWhatsnew]. Use o aplicativo Hub do Windows Feedback para publicar, votar, acompanhar e obter suporte para sugestões gerais e problemas do Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Console"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulação"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Memória"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Rede"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Desempenho"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Profissionais de Serviço"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Armazenamento"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo do Microsoft Edge (EdgeHTML) DevTools "  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Visualização do Microsoft Edge DevTools - Clientes do Protocolo DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicativos do Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicativos Web Progressivos (EdgeHTML) no Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Visualização do Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider".  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste Gratuito do Navegador Microsoft Edge | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
