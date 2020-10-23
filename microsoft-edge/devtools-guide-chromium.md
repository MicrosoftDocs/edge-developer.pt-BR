---
description: Conheça as ferramentas de desenvolvedor do Microsoft Edge (Chromium)
title: Ferramentas de desenvolvedor do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 9f035df5bc80aa6a1df0464eb326e4185e2205d2
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133901"
---
# Ferramentas de desenvolvedor do Microsoft Edge (Chromium)  

O Microsoft Edge adotou o projeto de código-fonte aberto Chromium para criar melhor compatibilidade com a Web e menos fragmentação de diferentes plataformas da Web subjacentes.  Essa alteração deve facilitar a criação e teste de seus sites no Microsoft Edge e garantir que cada um funciona como esperado, mesmo quando visto em um navegador diferente baseado em Chromium \ (como Google Chrome, Vivaldi, Opera ou Brave \).  

Como a Web cresceu a utilização em um conjunto de dispositivos cada vez maior dos tipos de dispositivos, a complexidade e a sobrecarga envolvidas nos testes de websites explodiram. Como os desenvolvedores da Web \ (principalmente os de pequenas empresas \) devem testar tantos sistemas diferentes, talvez seja praticamente impossível garantir que os sites funcionem bem em todos os tipos de dispositivo e em todos os navegadores.  Agora que o Microsoft Edge é baseado no Chromium, a equipe do Microsoft Edge simplificou a matriz, alinhando a plataforma da Web do Microsoft Edge com outros navegadores baseados no Chromium e forneceu a melhor experiência de ferramentas de desenvolvimento, tanto dentro do navegador quanto com as outras ferramentas de desenvolvedor que você usa todos os dias \ (por exemplo, o código do Visual Studio \).  

Se você estiver fazendo check-out do Microsoft Edge e se desenvolve principalmente em um navegador baseado no Chromium, você deve se sentir em casa.  As ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) funcionam da mesma maneira que as ferramentas de desenvolvedor que você já conhece e usa.  Para obter mais informações, confira [o que há de novo no Microsoft Edge (Chromium) devtools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Se você está conferindo a próxima versão do Microsoft Edge e já desenvolveu no Microsoft Edge \ (EdgeHTML \), agora tem algumas ferramentas incríveis que devem facilitar e agilizar a criação e teste de seus websites no Microsoft Edge!  

## Abrir o DevTools  

Se você nunca usou o DevTools antes, as ferramentas de desenvolvedor do Microsoft Edge são um conjunto de ferramentas criadas diretamente no navegador Microsoft Edge.  Com esses DevTools, você pode fazer o seguinte.  

*   Inspecionar e fazer alterações no seu site HTML  
*   Editar CSS e ver instantaneamente a visualização de como seu site renderiza  
*   Veja todas as `console.log()` instruções do seu código JavaScript front-end  
*   Depurar o script definindo pontos de interrupção e passando por ele linha por linha  

diretamente no navegador.  Esses são apenas exemplos de alguns dos recursos que o DevTools fornece para facilitar e agilizar a criação e teste de seus websites no Microsoft Edge.  

Para abrir o DevTools  

*   pressionado `F12` 
*   Pressione `Ctrl` + `Shift` + `I` no Windows/Linux \ ( `Command` + `Option` + `I` no MacOS \)  

Se você quiser ver o HTML ou CSS de um elemento em seu site, clique com o botão direito do mouse no elemento e selecione **inspecionar** para saltar para o painel elementos.  Você também pode pressionar `Ctrl` + `Shift` + `C` Windows/Linux \ ( `Command` + `Option` + `C` no MacOS \) para abrir o devtools no **modo inspecionar elemento** , que permite selecionar um elemento no site e ver o HTML e CSS no painel de **elementos** .  

Se você quiser ver os logs do seu código JavaScript front-end ou executar um script rapidamente, pressione `Ctrl` + `Shift` + `J` no Windows/Linux ou `Command` + `Option` + `J` no MacOS para iniciar o painel do console no devtools.  

## Ferramentas principais  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Microsoft Edge (Chromium) DevTools":::
   Ferramentas principais do Microsoft Edge (Chromium) DevTools  
:::image-end::: 

O DevTools Microsoft Edge \ (Chromium \) inclui os painéis a seguir.  

*   Um painel de **Elementos** para editar HTML e CSS, inspecionar propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de mutação do DOM.  
*   Um **Console** para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós do DOM e executar o JavaScript no contexto da janela ou quadro selecionado.  
*   Um painel **fontes** para abrir e abrir o código, definir pontos de interrupção, depurar o código e ver o estado do seu website uma linha de JavaScript de cada vez  
*   Um painel de**Rede**para monitorar e inspecionar solicitações e respostas do cache da rede e do navegador   
*   Um painel de **Desempenho** para criar um perfil de tempo e recursos do sistema necessários para o seu site  
*   Um painel de **Memória** para medir o uso dos recursos de memória e comparar os instantâneos da pilha em diferentes estados de tempo de execução do código  
*   Um painel de **aplicativos** para inspecionar, modificar e depurar manifestos do aplicativo Web, trabalhos de serviço e caches de trabalho do serviço.  Você também pode inspecionar e gerenciar armazenamento, bancos de dados e caches no painel do **aplicativo** .  
*   Um painel de **segurança** para depurar problemas de segurança e garantir que você implementou corretamente HTTPS em seu site.  O HTTPS fornece segurança crítica e integridade de dados para seu site e seus usuários que fornecem informações pessoais em seu site.  
*   Um painel de **auditoria** \ (agora renomeou **Lighthouse**\) para executar uma auditoria de seu site.  Os resultados da auditoria ajudam você a melhorar a qualidade do seu site das seguintes maneiras.  
    *   Capture erros comuns relacionados à disponibilização do seu site, segurança, execução e assim por diante.  
    *   Corrigir cada erro.  
    *   Crie um PWA.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Envie seus [comentários e solicitações de recursos](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Extensões  

Você pode ter usado extensões para o DevTools para ajudá-lo a diagnosticar e depurar problemas ao criar seus sites ou aplicativos.  Você pode adquirir extensões para o Microsoft Edge da página [Complementos do Microsoft Edge][MicrosoftEdgeAddonsExtensions] .  Na página [Complementos do Microsoft Edge][MicrosoftEdgeAddonsExtensions] , você pode navegar pelas extensões devtools da categoria **ferramentas de desenvolvedor** ou pesquisar por uma extensão específica.  

Você também pode adicionar extensões da [loja da Web Chrome][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Microsoft Edge (Chromium) DevTools":::
   Loja da Web do Chrome no Microsoft Edge  
:::image-end:::  

Na parte superior, selecione **permitir extensões de outras lojas** e, em seguida, selecione **permitir** na caixa de diálogo que é exibida.  

> [!NOTE]
> As extensões instaladas de fontes diferentes da Microsoft Store não são verificadas e podem afetar o desempenho do navegador.  

Selecione **Adicionar ao Chrome** para adicionar sua extensão devtools ao Microsoft Edge!  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Microsoft Edge (Chromium) DevTools"  
