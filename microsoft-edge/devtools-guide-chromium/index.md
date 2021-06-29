---
description: Conheça as ferramentas de desenvolvedor Microsoft Edge (Chromium)
title: Microsoft Edge (Chromium) visão geral das Ferramentas de Desenvolvedor
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 78603c51dab5a61f8d6b43e60a3f252eac665d99
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624756"
---
# <a name="microsoft-edge-chromium-developer-tools-overview"></a>Microsoft Edge (Chromium) visão geral das Ferramentas de Desenvolvedor  

Quando você instala Microsoft Edge, você tem um navegador. Além disso, você tem uma maneira poderosa de inspecionar, depurar e até mesmo criar projetos web.  As Ferramentas de Desenvolvedor enviadas com o navegador são baseadas nas ferramentas no projeto Chromium de código aberto, portanto, você já pode estar familiarizado com as ferramentas.  Para manter as descrições mais curtas neste artigo, as `Microsoft Edge Developer Tools` agora são conhecidas como `DevTools` .  

Use o DevTools para revisar e saber mais sobre as seguintes tarefas de desenvolvimento.  

*   [Inspecione e altere a página da Web atual][DevtoolsGuideDomIndex] ao vivo no navegador.  
*   [Emular como seu produto se comporta em diferentes dispositivos e][DevtoolsGuideDeviceModeIndex] simular um ambiente móvel completo com diferentes condições de rede.  
*   [Inspecionar, ajustar e alterar os estilos de elementos][DevtoolsGuideInspectStylesEditFonts] na página da Web usando ferramentas ao vivo com uma interface visual.  
*   [Depurar seu JavaScript][DevtoolsGuideJavascriptIndex] usando a depuração de ponto de interrupção e com o [console ao vivo][DevtoolsGuideConsoleIndex].  
*   Encontre [problemas de acessibilidade, desempenho, compatibilidade][DevtoolsGuideIssuesIndex] e segurança em seus produtos e saiba como usar o DevTools para corrigir cada um deles.  
*   [Inspecione o tráfego de][DevtoolsGuideNetworkIndex] rede e examine o local dos problemas.  
*   [Inspecione onde o navegador armazenou o conteúdo][DevtoolsGuideStorageSessionstorage] em vários formatos.  
*   [Avalie o desempenho][DevtoolsGuideEvaluatePerformanceIndex] do produto para encontrar problemas [de memória][DevtoolsGuideMemoryProblemsIndex] e problemas [de renderização.][DevtoolsGuideRenderingToolsIndex]  
*   [Use um ambiente de desenvolvimento][DevtoolsGuideSourcesIndex] para [sincronizar alterações no DevTools com o][DevtoolsGuideWorkspacesIndex] sistema de arquivos e substituir [arquivos][DevtoolsGuideJavascriptOverrides] da Web.  
    
<!-- Is the link meant to be local or session storage for "inspect where the browser stored content"? -->  

E muito mais.  Tudo começa quando você abre o DevTools e personaliza cada ferramenta de acordo com suas necessidades.  

## <a name="open-the-devtools"></a>Abra o DevTools  

Para abrir e explorar o DevTools, use uma das seguintes ações.  

*   Passe o mouse em qualquer elemento na página da Web, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  Essa ação abre a **ferramenta Elements.**  
*   Selecione `F12` .  
*   Selecione `Ctrl` + `Shift` + `I` em Windows/Linux ou `Command` + `Option` + `I` no macOS.  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect.msft.png" alt-text="Escolha Inspecionar no menu contextual em qualquer elemento" lightbox="./media/devtools-intro-inspect.msft.png":::  
         Escolha **Inspecionar** no menu contextual em qualquer elemento  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect-devtools-open.png" alt-text="O DevTools é aberto com o elemento escolhido realçado" lightbox="./media/devtools-intro-inspect-devtools-open.png":::  
         O DevTools é aberto com o elemento escolhido realçado  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

Há duas maneiras principais de interagir com o DevTools.
*   Usar o mouse  
*   [Atalhos de teclado][DevtoolsGuideShortcutsIndex].  Atalhos de teclado fornecem uma maneira rápida de acessar a funcionalidade e são necessários para acessibilidade.  A Microsoft Edge equipe do DevTools trabalha duro para disponibilizar todas as ferramentas usando o teclado e tecnologias assistivas, como leitores de tela.  Para obter mais informações sobre como abrir os diferentes recursos no DevTools, navegue até Microsoft Edge [atalhos de teclado do DevTools.][DevtoolsGuideOpenIndex]  

## <a name="dock-the-devtools-in-your-browser"></a>Acoplar o DevTools no navegador  

Quando você abre o DevTools, ele encaixa à esquerda do navegador.  Para alterar o local encaixado do DevTools, conclua as seguintes ações.  

1.  Escolha o **botão Personalizar e Controlar DevTools** \( `...` \)  
1.  À direita de **Posicionamento do DevTools** em relação à página \(**Lado**do encaixe \), escolha uma opção do **lado do** encaixe.  
    
Para obter mais informações, navegue até [Change Microsoft Edge DevTools placement (Undock, Dock to Bottom, Dock To Left)][DevtoolsGuideCustomizePlacement].  

:::image type="complex" source="./media/devtools-intro-docking-menu.msft.png" alt-text="Captura de tela do menu do lado do dock no DevTools" lightbox="./media/devtools-intro-docking-menu.msft.png":::  
   Captura de tela do menu do lado do dock no DevTools  
:::image-end:::  

No **lado do encaixe,** escolha qualquer uma das opções de layout a seguir.  

*   **Desfazer em janela separada**.   Ajuda você a trabalhar com vários monitores ou se precisar trabalhar em um aplicativo de tela inteira.  
*   **Encaixe para a esquerda** ou **Encaixe para a direita**.  Ajuda você a manter o DevTools lado a lado com seu produto Web e é excelente quando você emular dispositivos móveis.  As **opções Doca para a esquerda** e **Doca** para a direita funcionam melhor com exibições de alta resolução.  Para obter mais informações sobre dispositivos de emulação, navegue até [Emular dispositivos móveis Microsoft Edge DevTools][DevtoolsGuideDeviceModeIndex].  
*   **Encaixe na parte inferior**.  Ajuda quando você não tem espaço de exibição horizontal suficiente ou deseja depurar texto longo no DOM ou **console.**  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-docking-left.msft.png" alt-text="Escolha Encaixar para a Esquerda" lightbox="./media/devtools-intro-docking-left.msft.png":::  
         Escolha **Encaixar para a Esquerda**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-bottom.msft.png" alt-text="Escolha Dock to Bottom" lightbox="media/devtools-intro-docking-bottom.msft.png":::  
         Escolha **Dock to Bottom**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  
:::row:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-right.msft.png" alt-text="Escolha Encaixe para a Direita" lightbox="media/devtools-intro-docking-right.msft.png":::  
         Escolha **Encaixe para a Direita**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-own-window.msft.png" alt-text="Escolha Desfazer em janela separada" lightbox="media/devtools-intro-docking-own-window.msft.png":::  
         Escolha **Desfazer em janela separada**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="learn-about-the-core-tools"></a>Saiba mais sobre as principais ferramentas  

O DevTools lhe dá uma quantidade incrível de energia para inspecionar, depurar e alterar o produto Web exibido no momento no navegador.  A maioria das ferramentas exibe as alterações ao vivo.  As atualizações ao vivo fazem as ferramentas extremamente úteis para refinar a aparência e a navegação ou a funcionalidade de um projeto da Web sem a necessidade de atualizá-lo ou criar.  O DevTools também permite que você altere produtos de terceiros baseados na Web em seu computador.  

O DevTools cresceu durante um período de vários anos.  Você pode supor que o DevTools é difícil de aprender quando você abre pela primeira vez qualquer uma das ferramentas.  O texto a seguir apresenta rapidamente as diferentes partes.  A barra de ferramentas principal oferece algumas seções e as seções são ordenadas da esquerda para a direita.  

:::image type="complex" source="./media/devtools-intro-menu-bar.msft.png" alt-text="Captura de tela da barra de menus do DevTools com rótulos que explicam as diferentes seções.  Em ordem: Inspecionar ferramenta, ferramenta de emulação de dispositivo, grupo de guias Ferramentas, erros javascript, problemas, Configurações, feedback, personalizar e fechar." lightbox="./media/devtools-intro-menu-bar.msft.png":::  
   Captura de tela da barra de menus do DevTools com rótulos que explicam as diferentes seções.  Em ordem: Inspecionar ferramenta, ferramenta de emulação de dispositivo, grupo de guias Ferramentas, Erros do JavaScript, Problemas, Configurações, Feedback, Personalizar e Fechar.  
:::image-end:::  

*   A ferramenta Inspecionar permite que você escolha um elemento na página da Web atual.  Depois de ativá-lo, você pode mover o mouse sobre diferentes partes da página da Web para obter informações detalhadas sobre o elemento e uma sobreposição de cores para exibir dimensões, preenchimento e margem.  
    
    :::image type="complex" source="./media/devtools-intro-inspect-tool.msft.png" alt-text="A ferramenta Inspecionar com o primeiro título deste artigo escolhido" lightbox="./media/devtools-intro-inspect-tool.msft.png":::  
       A ferramenta Inspecionar com o primeiro título deste artigo escolhido  
    :::image-end:::  
    
*   A [ferramenta Emulação de Dispositivo][DevtoolsGuideDeviceModeIndex] exibe o produto Web atual em um modo de dispositivo emulado.  A **ferramenta Emulação de** Dispositivo permite que você execute e teste como seu produto reage quando você resize o navegador.  Ele também fornece uma estimativa do layout e do comportamento em um dispositivo móvel.  
    
    :::image type="complex" source="./media/devtools-intro-device-emulation.msft.png" alt-text="Captura de tela da exibição DevTools deste artigo em um telefone celular emulado" lightbox="./media/devtools-intro-device-emulation.msft.png":::  
       Captura de tela da exibição DevTools deste artigo em um telefone celular emulado  
    :::image-end:::  
    
*   O grupo de guias Ferramentas é um grupo de guias que representam diferentes ferramentas usadas em cenários diferentes.  Você pode personalizar cada uma das ferramentas e cada ferramenta pode mudar com base no contexto.  Para abrir um menu suspenso de mais ferramentas, escolha o botão **Mais guias** \( `>>` \)  Cada uma das ferramentas é introduzida posteriormente na seção a seguir.  
*   Ao lado do grupo de guias Ferramentas, há erros opcionais e atalhos de problemas.  Os atalhos são exibidos quando ocorrem erros ou problemas do JavaScript na página da Web atual.  O botão Abrir Console para exibir **# erros, # avisos** \(**JavaScript Errors**\) exibe um círculo vermelho com um seguido pelo número de `X` erros JavaScript.  Para abrir o [Console][DevtoolsGuideConsoleIndex] e saber mais sobre o erro, escolha o **botão Erros do JavaScript.**  O **botão Abrir Problemas para exibir # problemas** \(**Problemas**\) é um ícone de mensagem azul seguido pelo número de problemas.  Para abrir a ferramenta [Problemas,][DevtoolsGuideIssuesIndex] escolha **Botão Problemas.**  
*   O **botão Configurações** exibe um ícone de engrenagem.  Para abrir a página da Web do DevTools **Configurações,** escolha o **botão Configurações.**  A **Configurações** da Web exibe um menu para alterar **Preferências,** ativar **Experimentos**e muito mais.  
*   O **botão Enviar Feedback** exibe o tronco com uma bolha de chat ao lado dele.  Para abrir a caixa de diálogo Enviar **Comentários,** escolha o **botão Enviar Comentários.**  A **caixa de diálogo** Enviar Comentários permite que você insira informações para descrever o que aconteceu e inclui automaticamente uma captura de tela.  Use-o para se conectar à equipe do DevTools para relatar problemas, problemas ou sugerir ideias.  
*   O **botão Personalizar e controlar Devtools** \( `...` \) abre um menu suspenso.  Ele permite definir onde encaixar o DevTools, pesquisar, abrir ferramentas diferentes e muito mais.  
    
No grupo de guias Ferramentas, você pode abrir as diferentes ferramentas disponíveis no DevTools.  A lista a seguir descreve as ferramentas mais usadas no DevTools.  

*   **Bem-vindo**.  Inclui informações sobre os novos recursos do DevTools, como entrar em contato com a equipe e fornece informações sobre determinados recursos.  
*   **Elementos**.  Permite editar ou inspecionar HTML e CSS.  Você pode editar ambos na ferramenta e exibir as alterações ao vivo no navegador.  
*   [Console][DevtoolsGuideConsoleIndex].  Permite exibir e filtrar mensagens de log.  As mensagens de log são logs automatizados do navegador, como solicitações de rede e logs gerados pelo desenvolvedor.  Você também pode executar JavaScript diretamente no **Console** no contexto da janela ou quadro atual.  
*   [Fontes][DevtoolsGuideSourcesIndex].  Um editor de código e um depurador JavaScript.  Você pode editar projetos, manter trechos e depurar seu projeto atual.  
*   [Rede][DevtoolsGuideNetworkIndex].  Permite monitorar e inspecionar solicitações ou respostas da rede e do cache do navegador.  Você pode filtrar solicitações e respostas para se ajustar às suas necessidades e simular diferentes condições de rede.  Outras ferramentas especializadas também estão disponíveis, como **Desempenho,** **Memória,** **Aplicativo,** **Segurança**e **Auditorias.**  

## <a name="power-tip-use-the-command-menu"></a>Dica de energia: Use o menu de comando  

O DevTools fornece muitos recursos e funcionalidades para usar com seu produto Web.  Acesse as diferentes partes do DevTools de várias maneiras, mas a maneira mais rápida de acessar os recursos necessários é usar o menu de comando.  Para obter mais informações, navegue até [Executar comandos com o menu Microsoft Edge DevTools Command][DevtoolsGuideCommandMenuIndex].  Para abrir o menu de comando, conclua uma das seguintes ações.  

*   Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).  
*   Escolha **Personalizar e controlar DevTools** \( `...` \) e escolha Executar **Comando**.  

:::image type="complex" source="./media/devtools-intro-command-menu.msft.png" alt-text="Captura de tela do menu de comando no DevTools" lightbox="./media/devtools-intro-command-menu.msft.png":::  
Captura de tela do menu de comando no DevTools  
:::image-end:::  

O menu de comando permite que você digite comandos para exibir, ocultar ou executar recursos no DevTools.  Com o menu de comando aberto, insira a palavra **alterações**e escolha **Drawer Show Changes**.  A **ferramenta Changes** é aberta, o que é útil ao editar CSS, mas é difícil de encontrar na interface do usuário do DevTools.  

:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-command-menu-show-changes.msft.png" alt-text="O menu De comando exibe as opções depois de digitar alterações" lightbox="./media/devtools-intro-command-menu-show-changes.msft.png":::  
         O menu De comando exibe as opções depois de digitar `changes`  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-showing-changes.msft.png" alt-text="DevTools com a ferramenta Changes aberta" lightbox="./media/devtools-intro-showing-changes.msft.png":::  
         DevTools com a **ferramenta Changes** aberta  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="customize-the-devtools"></a>Personalizar o DevTools  

DevTools são personalizáveis para atender às suas necessidades ou à maneira como você trabalha.  Para alterar as configurações, conclua uma das seguintes ações.  

*   Escolha **Configurações** \(o ícone de engrenagem na parte superior direita\)  
*   Selecione `F1` ou `?` .  
    
Na seção **Preferências,** você pode alterar várias partes do DevTools.  Por exemplo, você pode usar a configuração **Corresponder** ao idioma do navegador para usar o mesmo idioma no DevTools que é usado no navegador.  Para outro exemplo, use a **configuração Tema** para alterar o tema do DevTools.  

:::image type="complex" source="media/devtools-intro-all-settings.msft.png" alt-text="Captura de tela de todas as configurações no DevTools" lightbox="./media/devtools-intro-all-settings.msft.png":::  
   Captura de tela de todas as configurações no DevTools  
:::image-end:::  

Você também pode alterar as configurações de recursos avançados, incluindo os seguintes recursos.    

*   [Espaços de trabalho][DevtoolsGuideWorkspacesIndex].  
*   Filtrar o código da biblioteca com a **lista Ignorar**.  
*   Defina **os dispositivos** que você deseja incluir no modo de teste e simulação de dispositivo.  Para obter mais informações, navegue até [Emular dispositivos móveis Microsoft Edge DevTools][DevtoolsGuideDeviceModeIndex].  
*   Escolha um perfil **de throttling de** rede.  
*   Definir locais **simulados**.  
*   Personalizar atalhos de teclado.  Para usar os mesmos atalhos no DevTools que Visual Studio Code, conclua as seguintes ações.  
    1.  Escolha **Corresponder atalhos da predefinição**.  
    1.  Escolha **Visual Studio Code**.  
        
    :::image type="complex" source="./media/devtools-intro-match-keys.msft.png" alt-text="Captura de tela de todos os atalhos de teclado e o menu para corresponder cada um aos atalhos no Visual Studio Code" lightbox="./media/devtools-intro-match-keys.msft.png":::  
       Captura de tela de todos os atalhos de teclado e o menu para corresponder cada um aos atalhos no Visual Studio Code  
    :::image-end:::  
    
## <a name="try-experimental-features"></a>Experimente recursos experimentais  

A equipe de DevTools fornece novos recursos como experimentos no DevTools.  Para obter a lista completa de experimentos, navegue até o devTools **Configurações**e escolha **Experimentos**.  Você pode ativar ou desativar cada um dos experimentos.  Ajude a decidir qual dos experimentos é valioso para você.  Para obter mais informações sobre os experimentos, navegue até [Recursos Experimentais][DevtoolsGuideExperimentalFeaturesIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Se você quiser visualizar os recursos mais recentes que vêm para [o DevTools,][DevtoolsGuideWhatsNew202102Devtools]baixe [Microsoft Edge Canary][MicrosoftedgeinsiderDownload], que é construído à noite.  

## <a name="see-also"></a>Consulte também  

*   [DevtoolsGuide para Iniciantes: Introdução com HTML e DOM][DevtoolsGuideBeginnersHtml]  
*   [Microsoft Edge (Chromium) Protocolo DevTools][DevtoolsProtocolIndex]  
    
<!-- links -->  

[DevtoolsGuideBeginnersHtml]: ./beginners/html.md "DevTools para iniciantes: começar com HTML e o dom | Microsoft Docs"  
[DevtoolsGuideCommandMenuIndex]: ./command-menu/index.md "Execute comandos com o menu Microsoft Edge DevTools Command | Microsoft Docs"  
[DevtoolsGuideConsoleIndex]: ./console/index.md "Visão geral do console | Microsoft Docs"  
[DevtoolsGuideCustomizePlacement]: ./customize/placement.md "Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Encaixar para Baixo, Encaixar para a Esquerda) | Microsoft Docs"  
[DevtoolsGuideDeviceModeIndex]: ./device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideDomIndex]: ./dom/index.md "Começar a exibir e alterar o dom | Microsoft Docs"  
[DevtoolsGuideEvaluatePerformanceIndex]: ./evaluate-performance/index.md "Começar a analisar o desempenho do tempo de execução | Microsoft Docs"  
[DevtoolsGuideExperimentalFeaturesIndex]: ./experimental-features/index.md "Recursos experimentais | Microsoft Docs"  
[DevtoolsGuideMemoryProblemsIndex]: ./memory-problems/index.md "Corrigir problemas de memória | Microsoft Docs"  
[DevtoolsGuideInspectStylesEditFonts]: ./inspect-styles/edit-fonts.md "Editar estilos de fonte CSS e configurações no painel Estilos | Microsoft Docs"  
[DevtoolsGuideIssuesIndex]: ./issues/index.md "Encontre e corrige problemas usando a ferramenta Problemas | Microsoft Docs"  
[DevtoolsGuideJavascriptIndex]: ./javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideJavascriptOverrides]: ./javascript/overrides.md "Substituir recursos de página da Web por cópias locais usando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideNetworkIndex]: ./network/index.md "Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideOpenIndex]: ./open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideRenderingToolsIndex]: ./rendering-tools/index.md "Analisar o desempenho do tempo de execução | Microsoft Docs"  
[DevtoolsGuideShortcutsIndex]: ./shortcuts/index.md "Microsoft Edge Atalhos de teclado do DevTools | Microsoft Docs"  
[DevtoolsGuideSourcesIndex]: ./sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
[DevtoolsGuideStorageSessionstorage]: ./storage/sessionstorage.md "Exibir e editar o armazenamento de sessão com Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideWhatsNew202102Devtools]: ./whats-new/2021/02/devtools.md "Novidades no DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsGuideWorkspacesIndex]: ./workspaces/index.md "Editar arquivos com espaços de trabalho | Microsoft Docs"  
[DevtoolsProtocolIndex]: ../devtools-protocol-chromium/index.md "Visão geral do Protocolo DevTools do Microsoft Edge (Chromium) | Microsoft Docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Microsoft Edge Complementos"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Chrome Web Store"  
