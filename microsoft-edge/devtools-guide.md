---
description: Conhecer as Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)
title: Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
ms.localizationpriority: high
ms.openlocfilehash: 0c01b761d1aa1fb645b15b0be5d5d6e4265e646e
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10985965"
---
# Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

As Ferramentas para Desenvolvedores do Microsoft Edge \(EdgeHTML\) são criadas com o TypeScript, da plataforma[software livre][GithubMicrosoftChakracore], otimizadas para fluxos de trabalho front-end modernos, e agora disponíveis como um[aplicativo autônomo Windows 10][MicrosoftStoreEdgeDevtoolsPreview] na Microsoft Store!  

Para saber mais sobre os recursos mais recentes, confira [DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Ferramentas principais  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)":::
   Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML)
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

As Ferramentas para Desenvolvedores do Microsoft Edge (EdgeHTML) incluem:  

*   Um painel de [Elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML e CSS, inspecionar propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de mutação do DOM.  
*   Um [Console][DevtoolsGuideEdgehtml|::ref3::|] para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós do DOM e executar o JavaScript no contexto da janela ou quadro selecionado.  
*   Um [Depurador][DevtoolsGuideEdgehtml|::ref4::|] para percorrer o código, definir inspeções e pontos de interrupção, editar seu código ao vivo e inspecionar o armazenamento da Web e os caches de cookies  
*   Um painel de[Rede][DevtoolsGuideEdgehtml|::ref5::|]para monitorar e inspecionar solicitações e respostas do cache da rede e do navegador  
*   Um painel de [Desempenho][DevtoolsGuideEdgehtml|::ref6::|] para criar um perfil de tempo e recursos do sistema necessários para o seu site  
*   Um painel de [Memória][DevtoolsGuideEdgehtml|::ref7::|] para medir o uso dos recursos de memória e comparar os instantâneos da pilha em diferentes estados de tempo de execução do código  
*   Um painel de[Armazenamento][DevtoolsGuideEdgehtml|::ref8::|] para inspecionar e gerenciar seu armazenamento na Web, IndexedDB, cookies e dados de cache  
*   Um painel de [Profissionais de Serviço][DevtoolsGuideEdgehtmlServiceworkers] para gerenciar e depurar seus profissionais de serviço.  
*   Um painel de [Emulação][DevtoolsGuideEdgehtml|::ref9::|] para testar o seu site com diferentes perfis de navegador, resoluções de tela e coordenadas de localização do GPS  

Continue enviando seus [comentários e solicitações de recursos](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

> [!TIP]
> [Teste no Microsoft Edge \(EdgeHTML\) gratuitamente em qualquer navegador][BrowserstackEdgehtml].  
> A equipe do Microsoft Edge criou uma parceria com o [BrowserStack][BrowserstackEdgehtml] para fornecer testes gratuitos e automatizados no Microsoft Edge.  

## Aplicativo da Microsoft Store  

As **Ferramentas para Desenvolvedores do Microsoft Edge \(EdgeHTML\)** estão [disponíveis agora][DevtoolsGuideEdgehtmlWhatsnew] como um aplicativo autônomo [Windows 10 da Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], além da experiência de ferramentas do navegador \(`F12`\).  Com a versão da loja, há um painel de **seletor** para anexar a abrir destinos de página locais e remotos e um layout com guias para alternar entre instâncias das DevTools.  

### Depuração local  

Para depurar uma página localmente, basta iniciar o aplicativo Microsoft Edge DevTools.  O painel **Local** do seletor exibirá todos os processos de conteúdo ativos do EdgeHTML, incluindo as guias de navegação abertas do Edge, [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processos\) em funcionamento e [controles][HostingWebview] do WebView.  Selecione seu destino desejado para anexar e abrir uma nova instância da guia do DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Painel local do aplicativo DevTools":::
   Painel local do aplicativo DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Depuração remota  

O aplicativo Microsoft Edge DevTools introduz o suporte básico para depurar páginas em um computador remoto por meio do nosso novo [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex].  A versão mais recente vem com o acesso remoto à funcionalidade central no [Depurador][DevtoolsGuideEdgehtml|::ref10::|], nos[Elementos][DevtoolsGuideEdgehtml|::ref11::|] \(para operações somente leitura\) e nos painéis do[Console][DevtoolsGuideEdgehtml|::ref12::|].  O depurador remoto está limitado ao Microsoft Edge \(EdgeHTML\) executando hosts da área de trabalho, com suporte para outros hosts EdgeHTML e dispositivos com Windows 10 chegando nas versões futuras.  

Para começar, confira a seção de documentos [Protocolo DevTools][DevtoolsProtocolEdgehtmlIndex]do[*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview].  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Painel remoto do aplicativo DevTools":::
   Painel remoto do aplicativo DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Atalhos gerais  

> [!IMPORTANT]
> Todos os atalhos foram verificados na versão mais recente do Windows.  
> Se não for possível usar um atalho, atualize sua cópia do Windows.  

Esses atalhos controlam a janela principal do DevTools e devem funcionar em todas as ferramentas.  

| Ação | Atalho |  
|:--- |:--- |  
| Mostrar/Ocultar DevTools \(abre para o último painel exibido\) | `F12`, `Ctrl`+`Shift`+`I` |  
| Alternar encaixe \(Desencaixar/Abaixo/Direita\) | `Ctrl`+`Shift`+`D` |  
| Abrir arquivo | `Ctrl`+`P`, `Ctrl`+`O` |  
| Mostrar código-fonte HTML não editável no depurador | `Ctrl`+`U` |  
| Mostrar/ocultar Console na parte inferior de qualquer outra ferramenta  | `Ctrl`+`` ` `` |  
| Alternar para Elementos \(explorador do DOM\) | `Ctrl`+`1` |  
| Alternar para Console |  `Ctrl`+`2` |  
| Alternar para Depurador | `Ctrl`+`3` |  
| Alternar para Rede | `Ctrl`+`4` |  
| Alternar para Desempenho | `Ctrl`+`5` |  
| Alternar para Memória | `Ctrl`+`6` |  
| Alternar para Emulação | `Ctrl`+`7` |  
| Documento de Ajuda | `F1` |  
| Próxima ferramenta | `Ctrl`+`F6` |  
| Guia anterior | `Ctrl`+`Shift`+`F6` |  
| Ferramenta anterior \(do histórico\) | `Ctrl`+`Shift`+`[` |  
| Próxima ferramenta \(do histórico\) | `Ctrl`+`Shift`+`]` |  
| Próximo subquadro | `F6` |  
| Subquadro anterior | `Shift`+`F6` |  
| Próxima correspondência na caixa de pesquisa | `F3` |  
| Correspondência anterior na caixa de pesquisa | `Shift`+`F3` |  
| Procurar na caixa de pesquisa | `Ctrl`+`F` |  
| Focalizar o console na parte inferior | `Alt`+`Shift`+`I` |  
| Iniciar o DevTools para o Console | `Ctrl`+`Shift`+`J` |  
| Atualizar a página | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Se você estiver depurando e pausar em um ponto de interrupção, a ação **Atualizar a página** retoma o tempo de execução primeiro.  

## Entrar em contato com a equipe Microsoft Edge DevTools  

Envie seus comentários para ajudar a melhorar o Microsoft Edge \ (EdgeHTML\) DevTools para você!  Basta abrir as ferramentas \(`F12`\) e selecionar o botão [Enviar comentários](#microsoft-edge-edgehtml-developer-tools).  

Torne-se um Participante do Programa Windows Insider para visualizar os [recursos mais recentes que estão chegando à DevTools][DevtoolsGuideEdgehtmlWhatsnew].  Use o aplicativo Hub do Windows Feedback para publicar, votar, acompanhar e obter suporte para sugestões gerais e problemas do Windows.  

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
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo de DevTools Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Visualização do Microsoft Edge DevTools - Clientes do Protocolo DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicativos do Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicativos de web progressivos (EdgeHTML) no Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Visualização do Microsoft Edge DevTools"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste gratuito do navegador Microsoft Edge | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
