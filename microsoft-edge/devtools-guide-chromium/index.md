---
description: Conheça as Ferramentas de Desenvolvedor do Microsoft Edge (Chromium)
title: Ferramentas de desenvolvedor do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 05b757b7cb399815d072b9d6038873cfd118a59d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327488"
---
# Visão geral das Ferramentas de Desenvolvedor do Microsoft Edge (Chromium)  

O Microsoft Edge adotou o projeto de código aberto Chromium.  O novo navegador Microsoft Edge cria melhor compatibilidade com a Web e reduz a fragmentação de diferentes plataformas web.  A alteração deve tornar mais fácil para você criar e testar suas páginas da Web no Microsoft Edge.  O novo Microsoft Edge deve ajudar suas páginas da Web a funcionar conforme o esperado quando abertas em outros navegadores baseados no Chromium.  Os navegadores baseados no Chromium incluem o Google Chrome, Vivaldi, Opera, Olei e o novo Microsoft Edge.  

A Web cresceu em uso em uma matriz cada vez maior de tipos de dispositivos.  A complexidade e a sobrecarga envolvidas no teste de páginas da Web cresceram rapidamente.  Os desenvolvedores da Web como você precisam testar em vários sistemas diferentes.  Para garantir que suas páginas da Web funcionem bem em todos os tipos de dispositivos e navegadores, você pode achar quase impossível, especialmente se você trabalha em uma pequena empresa.  O novo Microsoft Edge agora é baseado no Chromium.  A equipe do Microsoft Edge simplificou a matriz alinhando a plataforma Web do Microsoft Edge com outros navegadores baseados no Chromium.  O novo Microsoft Edge oferece uma experiência de desenvolvimento da melhor classe.  A experiência é realizada dentro do navegador e junto com as outras ferramentas de desenvolvedor que você usa diariamente, como o Visual Studio Code.  

Como desenvolvedor de navegador baseado no Chromium, você deve se sentir confortável com o novo navegador Microsoft Edge.  O Microsoft Edge \(Chromium\) DevTools funciona exatamente como as ferramentas de desenvolvedor que você já conhece e usa.  As Ferramentas de Desenvolvedor do Microsoft Edge \(Chromium\) geralmente são chamadas de Microsoft Edge \(Chromium\) DevTools ou DevTools.  Para obter mais informações, navegue até [Novidades no Microsoft Edge (Chromium) DevTools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Se você já desenvolveu para o Microsoft Edge \(EdgeHTML\) e está avaliando o novo Microsoft Edge, ele agora fornece novas ferramentas excelentes para você criar e testar suas páginas da Web de forma mais fácil e rápida.  

## Abra o DevTools  

O Microsoft Edge DevTools é um conjunto de ferramentas criadas diretamente no navegador Microsoft Edge.  O DevTools permite que você faça as seguintes tarefas diretamente no navegador.  

*   Inspecionar e fazer alterações em sua página da Web HTML  
*   Editar CSS e ver instantaneamente a visualização de como sua página da Web é renderiza  
*   Revise todas as instruções `console.log()` do seu código JavaScript front-end  
*   Depurar seu script, definir pontos de interrupção e passar pela linha por linha do código  
    
Mais exemplos dos recursos que o DevTools fornece para tornar mais fácil e rápido criar e testar sua página da Web no Microsoft Edge.  

Para abrir o DevTools  

*   Selecionar `F12` 
*   Selecione `Ctrl` + `Shift` + `I` \(Windows/Linux\) ou `Command` + `Option` + `I` \(macOS\)  
    
Se você quiser ver o HTML ou CSS de um elemento em seu site, clique com o botão direito do mouse no elemento e escolha **Inspecionar** para ir para a **ferramenta Elementos.**  Para abrir o DevTools no modo **inspecionar elemento,** selecione `Ctrl` + `Shift` + `C` \(Windows/Linux\) ou `Command` + `Option` + `C` \(macOS\). o **modo de elemento** inspect permite que você escolha um elemento na página da Web e exibir o HTML e CSS na ferramenta **Elementos.**  

Se você quiser revisar os logs do código JavaScript front-end ou executar rapidamente algum script, abra o **Console.**   Para iniciar a **ferramenta Console** no DevTools, selecione `Ctrl` + `Shift` + `J` \(Windows/Linux\) ou `Command` + `Option` + `J` \(macOS\).  

## Ferramentas principais  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Principais ferramentas do Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools-core-tools.png":::
   Principais ferramentas do Microsoft Edge (Chromium) DevTools  
:::image-end::: 

O Microsoft Edge \(Chromium\) DevTools inclui as ferramentas a seguir.  

*   Uma **ferramenta elements** para editar HTML e CSS, inspecionar propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de mutação dom  
*   Um **Console para** revisar e filtrar mensagens de log, inspecionar objetos JavaScript e nós DOM e executar JavaScript no contexto da janela ou quadro selecionado  
*   Uma **ferramenta Sources** para abrir e editar seu código, definir pontos de interrupção, passar pelo código e exibir o estado da sua página da Web
*   Uma **ferramenta de** rede para monitorar e inspecionar solicitações e respostas do cache da rede e do navegador   
*   Uma **ferramenta de** desempenho para perfilar o tempo e os recursos do sistema exigidos pelo seu site  
*   Uma **ferramenta de** memória para medir o uso de recursos de memória e comparar instantâneos de heap em diferentes estados de tempo de execução do código  
*   Uma **ferramenta de** aplicativo para inspecionar, modificar e depurar manifestos de aplicativos Web, trabalhadores de serviço e caches de serviço.  Você também pode inspecionar e gerenciar armazenamento, bancos de dados e caches da **ferramenta Aplicativo.**  
*   Uma **ferramenta de** segurança para depurar problemas de segurança e garantir que você implementou corretamente HTTPS em sua página da Web.  O HTTPS fornece segurança crítica e integridade de dados para o seu site e para os usuários que fornecem informações pessoais no seu site.  
*   Uma **ferramenta de Auditorias** \(agora renomeada **comoNamed**\) para executar uma auditoria de sua página da Web.  Os resultados da auditoria ajudam a melhorar a qualidade do seu site das seguintes maneiras.  
    *   Catch common errors related to making your webpage accessible, secure, performant, and so on.  
    *   Corrige cada erro.  
    *   Crie um PWA.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Envie seus [comentários e solicitações de recursos.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Extensões  

Você pode ter acessado o DevTools usando extensões ao diagnosticar e depurar problemas enquanto criou suas páginas da Web \(ou aplicativos\). As extensões do Microsoft Edge são adquiridas [dos Complementos do Microsoft Edge.][MicrosoftEdgeAddonsExtensions]  Em [Complementos do Microsoft Edge,][MicrosoftEdgeAddonsExtensions]procure extensões do DevTools na categoria **Ferramentas** de desenvolvedor ou procure uma extensão específica.  

Você também pode adicionar extensões da [Chrome Web Store.][GoogleChromeWebstoreExtensions]  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store no Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store no Microsoft Edge  
:::image-end:::  

Na parte superior, escolha **Permitir extensões de outros armazenamentos** e, em seguida, escolha **Permitir** na caixa de diálogo exibida.  

> [!NOTE]
> As extensões instaladas de fontes diferentes da Microsoft Store não são verificadas e podem afetar o desempenho do navegador.  

Escolha **Adicionar ao Chrome** para adicionar sua extensão DevTools ao Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Adicionar extensão da Chrome Web Store ao Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Adicionar extensão da Chrome Web Store ao Microsoft Edge  
:::image-end:::  

## Atalhos  

Os atalhos a seguir controlam a janela principal do DevTools, funcionam em todas as ferramentas ou ambos.  

| Ação | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Mostrar/Ocultar DevTools \(abre para a última ferramenta exibida\) | `F12` ou `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Mostrar o Console | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Mostrar o DevTools no modo **inspecionar elemento** que permite escolher um elemento e exibir o HTML e CSS na ferramenta **Elementos** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Mostrar Configurações | `?` ou `Fn`+`F1` | `?` ou `Fn`+`F1` |  
| Mostrar o próximo painel | `Ctrl`+`]` | `Command`+`]` |  
| Mostrar o painel anterior | `Ctrl`+`[` | `Command`+`[` |  
| Encaixa o DevTools na última posição usada.  Se o DevTools permanecer na posição padrão de toda a sessão, o atalho desfaz o DevTools em uma janela separada | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Alternar o **modo de dispositivo** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar **o modo de** elemento inspect que permite que você escolha um elemento e exibir o HTML e CSS na ferramenta **Elementos** | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Mostrar o Menu de Comando | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Mostrar/ocultar a gaveta | `Esc` | `Esc` |  
| Atualizar.  Atualiza a página da Web usando o cache.  | `F5` ou `Ctrl`+`R` | `Command`+`R` |  
| Hard Refresh.  Força o Microsoft Edge a baixar recursos novamente e recarregar.  Os recursos usados podem vir de uma versão armazenada em cache | `Ctrl`+`F5` ou `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Procure texto dentro do painel atual.  Sem suporte nas ferramentas auditorias, aplicativo e segurança | `Ctrl`+`F` | `Command`+`F` |  
| Mostrar a ferramenta pesquisa na gaveta, que permite pesquisar texto em todos os recursos carregados | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir um arquivo no painel Fontes | `Ctrl`+`O` ou `Ctrl`+`P` | `Command`+`O` ou `Command`+`P` |  
| Ampliar | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Reduzir | `Ctrl`+`-` | `Command`+`-` |  
| Restaurar o nível de zoom padrão | `Ctrl`+`0` | `Command`+`0` |  
| Executar trecho de código | `Ctrl`+`O`ou `Ctrl` + `P` , tipo `!` seguido pelo nome do script e pressione `Enter` | Pressione `Command` + `O` ou `Command` + `P` , digite seguido pelo nome `!` do script e pressione `Enter` |  
| Mostrar código-fonte HTML não editável em uma nova guia | `Ctrl`+`U` | N/D |  

> [!NOTE]
> Se você estiver depurando e pausando **** em um ponto de interrupção, o atalho Atualizar retomará o tempo de execução primeiro.  

## Confira também  

*   [DevTools para iniciantes: Começar a trabalhar com HTML e o DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Protocolo DevTools do Microsoft Edge (Chromium)][DevtoolsProtocolChromiumIndex]  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Se você quiser visualizar os recursos mais recentes que vêm para [o DevTools][DevtoolsGuideChromiumWhatsNewIndex], baixe [o Microsoft Edge Canary][MicrosoftedgeinsiderDownload], que é construído à noite.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools para iniciantes: começar a trabalhar com HTML e o DOM | Microsoft Docs"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Novidades no microsoft edge (Chromium) DevTools | Microsoft Docs"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Protocolo DevTools do Microsoft Edge (Chromium) | Microsoft Docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Complementos do Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Chrome Web Store"  
