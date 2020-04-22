---
description: Conheça as ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)
title: Ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 1abc01af5c1b058687d9ba1402911d4367b6e2b3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561452"
---
# Ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

Os DevTools Microsoft Edge \ (EdgeHTML \) são criados com [TypeScript][|::ref1::|Index], habilitados por [fonte aberta][GithubMicrosoftChakracore], otimizados para fluxos de trabalho de front-end modernos e agora disponíveis como um [aplicativo autônomo do Windows 10][MicrosoftStoreEdgeDevtoolsPreview] na Microsoft Store!  

Para saber mais sobre os recursos mais recentes, confira [devtools na atualização mais recente do Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Ferramentas principais  

![Microsoft Edge \ (EdgeHTML \) DevTools][ImageDevtoolsEdgehtml]  

O DevTools Microsoft Edge \ (EdgeHTML \) inclui:  

*   Um painel de [elementos][DevtoolsGuideEdgehtml|::ref2::|] para editar HTML e CSS, inspecionar Propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de MUTAção dom  
*   Um [console][DevtoolsGuideEdgehtml|::ref3::|] para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós dom e executar JavaScript no contexto da janela ou do quadro selecionado  
*   Um [depurador][DevtoolsGuideEdgehtml|::ref4::|] para depurar o código, definir inspeções e pontos de interrupção, editar seu código e inspecionar o armazenamento da Web e os caches de cookies  
*   Um painel de [rede][DevtoolsGuideEdgehtml|::ref5::|] para monitorar e inspecionar solicitações e respostas da rede e do cache do navegador  
*   Um painel de [desempenho][DevtoolsGuideEdgehtml|::ref6::|] para criar o perfil do tempo e dos recursos do sistema necessários para seu site  
*   Um painel de [memória][DevtoolsGuideEdgehtml|::ref7::|] para medir o uso dos recursos de memória e comparar os instantâneos de heap em diferentes Estados do tempo de execução do código  
*   Um painel de [armazenamento][DevtoolsGuideEdgehtml|::ref8::|] para inspecionar e gerenciar seu armazenamento da Web, IndexedDB, cookies e dados de cache  
*   Um painel [funcionários de serviço][DevtoolsGuideEdgehtmlServiceworkers] para gerenciar e depurar seus trabalhadores de serviço  
*   Um painel de [emulação][DevtoolsGuideEdgehtml|::ref9::|] para testar seu site com diferentes perfis de navegador, resoluções de tela e coordenadas de localização de GPS  

Continue enviando seus [comentários e solicitações de recursos](#feedback)!  

> [!TIP]
> [Teste no Microsoft Edge \ (EdgeHTML \) grátis de qualquer navegador][BrowserstackEdgehtml]:  
> Fizemos a parceria com a [BrowserStack][BrowserstackEdgehtml] para oferecer testes automatizados e ativos no Microsoft Edge \ (EdgeHTML \).  

## Aplicativo da Microsoft Store  

O **devtools Microsoft Edge \ (EdgeHTML \)** [agora está disponível][DevtoolsGuideEdgehtmlWhatsnew] como um [aplicativo autônomo do Windows 10 da Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], além da experiência de ferramenta no navegador \ (`F12`\).  Com a versão da loja vem um painel do **seletor** para anexar a abertura de destinos de página locais e remotos e um layout com guias para facilitar a alternância entre instâncias de devtools.  

### Depuração local  

Para depurar uma página localmente, basta iniciar o aplicativo Microsoft Edge DevTools.  O painel **local** do seletor exibirá todos os processos de conteúdo ativos do EdgeHTML, incluindo guias do navegador Edge aberto, executando [PWAs][PwasEdgehtmlIndex] \`WWAHost.exe` (processos \) e controles [WebView][HostingWebview] .  Clique no destino desejado para anexar e abrir uma nova instância de guia do DevTools.  

![Painel local do aplicativo DevTools][ImageDevtoolsGuideEdgehtmlChooselocal]  

### Depuração remota  

O aplicativo Microsoft Edge DevTools introduz suporte básico para depurar páginas em um computador remoto por meio do [protocolo devtools][DevtoolsProtocolEdgehtmlIndex]recém-lançado.  Com a versão mais recente vem o acesso remoto à funcionalidade central no [depurador][DevtoolsGuideEdgehtml|::ref10::|], [elementos][DevtoolsGuideEdgehtml|::ref11::|] \ (para operações somente leitura \) e painéis do [console][DevtoolsGuideEdgehtml|::ref12::|] .  A depuração remota está limitada ao Microsoft Edge \ (EdgeHTML \) que executa hosts de área de trabalho, com suporte para outros hosts EdgeHTML e dispositivos Windows 10 chegando em versões futuras.  

Para começar, confira a seção [*devtools do Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] dos documentos de [protocolo do devtools][DevtoolsProtocolEdgehtmlIndex] .  

![Painel remoto do aplicativo DevTools][DevtoolsGuideEdgehtmlRemote]  

## Privacidade Jurídica  

Envie-nos seus comentários para que possamos continuar aprimorando o Microsoft Edge \ (EdgeHTML \) DevTools para você!  Basta abrir as ferramentas (`F12`) e clicar no botão [enviar comentários](#microsoft-edge-edgehtml-developer-tools) .  

Torne-se um [Windows Insider][WindowsInsiderProgram] para visualizar os [recursos mais recentes que chegam ao devtools][DevtoolsGuideEdgehtmlWhatsnew].  Use o aplicativo Hub de feedback do Windows para postar, fazer uma votação, acompanhar e obter suporte para sugestões gerais do Windows e problemas.  

## Atalhos gerais  

Esses atalhos controlam a janela principal do DevTools e devem funcionar em todas as ferramentas.  

| Ação | Atalho |  
|:--- |:--- |  
| Mostrar/ocultar DevTools \ (abre para o último painel exibido \) | `F12`, `Ctrl`+`Shift`+`I` |  
| Alternar encaixe \ (desencaixar/abaixo/direita \) | `Ctrl`+`Shift`+`D` |  
| Abrir arquivo | `Ctrl`+`P`, `Ctrl`+`O` |  
| Mostrar código-fonte HTML não editável no depurador | `Ctrl`+`U` |  
| Mostrar/ocultar console na parte inferior de qualquer outra ferramenta  | `Ctrl`+`` ` `` |  
| Alternar para elementos \ (explorador do DOM \) | `Ctrl`+`1` |  
| Alternar para o console |  `Ctrl`+`2` |  
| Alternar para o depurador | `Ctrl`+`3` |  
| Alternar para a rede | `Ctrl`+`4` |  
| Alternar para o desempenho | `Ctrl`+`5` |  
| Alternar para memória | `Ctrl`+`6` |  
| Alternar para emulação | `Ctrl`+`7` |  
| Documento de ajuda | `F1` |  
| Próxima ferramenta | `Ctrl`+`F6` |  
| Ferramenta anterior | `Ctrl`+`Shift`+`F6` |  
| Ferramenta anterior \ (do histórico \) | `Ctrl`+`Shift`+`[` |  
| Próxima ferramenta \ (do histórico \) | `Ctrl`+`Shift`+`]` |  
| Subquadro seguinte | `F6` |  
| Subquadro anterior | `Shift`+`F6` |  
| Próxima correspondência na caixa de pesquisa | `F3` |  
| Correspondência anterior na caixa de pesquisa | `Shift`+`F3` |  
| Localizar na caixa de pesquisa | `Ctrl`+`F` |  
| Coloque o foco no console na parte inferior | `Alt`+`Shift`+`I` |  
| Iniciar o DevTools para o console | `Ctrl`+`Shift`+`J` |  
| Atualizar a página | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> Se você estiver Depurando e pausado em um ponto de interrupção, a ação **atualizar a página** retomará o tempo de execução primeiro.

<!-- image links  -->  

[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  
[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "Painel local do aplicativo DevTools"  
[DevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "Painel remoto do aplicativo DevTools"  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Consola"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Depurador"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Elementos"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Emulação"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Rowset"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Network"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Execução"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Trabalhadores do serviço"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "SPS"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Protocolo de DevTools Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clientes do protocolo DevTools preview do Microsoft Edge-DevTools"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) para aplicativos do Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Aplicativos Web progressivos (EdgeHTML) no Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools Preview"  

[WindowsInsiderProgram]: https://insider.windows.com "Programa Windows Insider"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste do navegador Microsoft Edge gratuito | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
