---
description: Conheça as ferramentas de desenvolvedor do Microsoft Edge (Chromium)
title: Ferramentas de desenvolvedor do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2019
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 178f72fbc47f712882de6f9564478953f4834890
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645305"
---
# Ferramentas de desenvolvedor do Microsoft Edge (Chromium)  

O Microsoft Edge adotou o projeto de código-fonte aberto Chromium para criar melhor compatibilidade com a Web e menos fragmentação de diferentes plataformas da Web subjacentes.  Essa alteração deve facilitar a criação e teste de seus sites no Microsoft Edge e garantir que cada um funciona como esperado, mesmo quando visto em um navegador diferente baseado em Chromium \ (como Google Chrome, Vivaldi, Opera ou Brave \).  

Como a Web cresceu a utilização em um conjunto de dispositivos cada vez maior dos tipos de dispositivos, a complexidade e a sobrecarga envolvidas nos testes de websites explodiram. Como os desenvolvedores da Web \ (principalmente os de pequenas empresas \) devem testar tantos sistemas diferentes, talvez seja praticamente impossível garantir que os sites funcionem bem em todos os tipos de dispositivo e em todos os navegadores.  Agora que o Microsoft Edge é baseado no Chromium, a equipe do Microsoft Edge simplificou a matriz, alinhando a plataforma da Web do Microsoft Edge com outros navegadores baseados no Chromium e forneceu a melhor experiência de ferramentas de desenvolvimento, tanto dentro do navegador quanto com as outras ferramentas de desenvolvedor que você usa todos os dias \ (por exemplo, o código do Visual Studio \).  

Se você estiver fazendo check-out do Microsoft Edge e se desenvolve principalmente em um navegador baseado no Chromium, você deve se sentir em casa.  As ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) funcionam da mesma maneira que as ferramentas de desenvolvedor que você já conhece e usa.  Para obter mais informações, confira [o que há de novo no Microsoft Edge (Chromium) devtools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools":::
   Microsoft Edge (Chromium) DevTools
:::image-end:::

<!--![Microsoft Edge (Chromium) DevTools](./devtools-guide-chromium/media/devtools.png)  -->  

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
*   Pressione `Ctrl` + `Shift` + `I` no Windows \ ( `Command` + `Option` + `I` no MacOS \)  

Se você quiser ver o HTML ou CSS de um elemento em seu site, clique com o botão direito do mouse no elemento e selecione **inspecionar** para saltar para o painel elementos.  Você também pode pressionar `Ctrl` + `Shift` + `C` o Windows \ ( `Command` + `Option` + `C` no MacOS \) para abrir o devtools no **modo inspecionar elemento** , que permite selecionar um elemento no site e ver o HTML e CSS no painel de **elementos** .  

Se você quiser ver os logs do seu código JavaScript front-end ou executar um script rapidamente, pressione `Ctrl` + `Shift` + `J` em Windows \ ( `Command` + `Option` + `J` no MacOS \) para iniciar o painel do console no devtools.  

## Ferramentas principais  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Ferramentas principais do Microsoft Edge (Chromium) DevTools":::
   Ferramentas principais do Microsoft Edge (Chromium) DevTools
:::image-end:::

<!--![Microsoft Edge \(Chromium\) DevTools core tools](./devtools-guide-chromium/media/devtools-core-tools.png)  -->  

O DevTools Microsoft Edge \ (Chromium \) inclui os painéis a seguir.  
*   Um painel de **elementos** para editar HTML e CSS, inspecionar Propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de MUTAção dom  
*   Um **console** para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós dom e executar JavaScript no contexto da janela ou do quadro selecionado  
*   Um painel **fontes** para abrir e abrir o código, definir pontos de interrupção, depurar o código e ver o estado do seu website uma linha de JavaScript de cada vez  
*   Um painel de **rede** para monitorar e inspecionar solicitações e respostas da rede e do cache do navegador   
*   Um painel de **desempenho** para criar o perfil do tempo e dos recursos do sistema necessários para seu site  
*   Um painel de **memória** para medir o uso dos recursos de memória e comparar os instantâneos de heap em diferentes Estados do tempo de execução do código  
*   Um painel de **aplicativos** para inspecionar, modificar e depurar manifestos do aplicativo Web, trabalhos de serviço e caches de trabalho do serviço.  Você também pode inspecionar e gerenciar armazenamento, bancos de dados e caches no painel do **aplicativo** .  
*   Um painel de **segurança** para depurar problemas de segurança e garantir que você implementou corretamente HTTPS em seu site.  O HTTPS fornece segurança crítica e integridade de dados para seu site e seus usuários que fornecem informações pessoais em seu site.  
*   Um painel de **auditoria** \ (agora renomeou **Lighthouse**\) para executar uma auditoria de seu site.  Os resultados da auditoria ajudam você a melhorar a qualidade do seu site das seguintes maneiras.  
    *   Capture erros comuns relacionados à disponibilização do seu site, segurança, execução e assim por diante.  
    *   Corrigir cada erro.  
    *   Crie um PWA.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Envie seus [comentários e solicitações de recursos](#getting-in-touch-with-the-microsoft-edge-devtools-team)!  

## Extensões  

Você pode ter usado extensões para o DevTools para ajudá-lo a diagnosticar e depurar problemas ao criar seus sites ou aplicativos.  Você pode adquirir extensões para o Microsoft Edge da página [Complementos do Microsoft Edge][MicrosoftEdgeAddonsExtensions] .  Na página [Complementos do Microsoft Edge][MicrosoftEdgeAddonsExtensions] , você pode navegar pelas extensões devtools da categoria **ferramentas de desenvolvedor** ou pesquisar por uma extensão específica.  

Você também pode adicionar extensões da [loja da Web Chrome][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Loja da Web do Chrome no Microsoft Edge":::
   Loja da Web do Chrome no Microsoft Edge
:::image-end:::

<!--![Chrome Web Store in Microsoft Edge](./devtools-guide-chromium/media/allow-extensions-from-stores.png)  -->

Na parte superior, selecione **permitir extensões de outras lojas** e, em seguida, selecione **permitir** na caixa de diálogo que é exibida.  

> [!NOTE]
> As extensões instaladas de fontes diferentes da Microsoft Store não são verificadas e podem afetar o desempenho do navegador.  

Selecione **Adicionar ao Chrome** para adicionar sua extensão devtools ao Microsoft Edge!  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Adicionando extensão do Chrome Web Store ao Microsoft Edge":::
   Adicionando extensão do Chrome Web Store ao Microsoft Edge
:::image-end:::

<!--![Adding extension from Chrome Web Store to Microsoft Edge](./devtools-guide-chromium/media/install-extension-from-chrome-store.png)  -->  

## Teclado  

Esses atalhos controlam a janela principal do DevTools, funcionam em todas as ferramentas ou em ambos.  

| Ação | Windows | macOS |  
|:--- |:--- | :--- |  
| Mostrar/ocultar DevTools \ (abre para o último painel exibido \) | `F12` or`Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Mostrar o painel de console | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Mostrar o DevTools no **modo inspecionar elemento** que permite que você selecione um elemento no site e veja HTML e CSS no painel **elementos** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Mostrar configurações | `?` or`Fn`+`F1` | `?` or`Fn`+`F1` |  
| Mostrar o próximo painel | `Ctrl`+`]` | `Command`+`]` |  
| Mostrar o painel anterior | `Ctrl`+`[` | `Command`+`[` |  
| Encaixe o DevTools na última posição usada.  Se o DevTools permanecer na posição padrão para toda a sessão, esse atalho desencaixará o DevTools em uma janela separada | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Alternar o **modo de dispositivo** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar o **modo inspecionar elemento** , que permite selecionar um elemento no site e ver o HTML e CSS no painel **elementos** | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Mostrar o menu de comandos | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Mostrar/ocultar a gaveta | `Esc` | `Esc` |  
| Atualize.  Isso atualiza a página usando o cache.  | `F5` or`Ctrl`+`R` | `Command`+`R` |  
| Atualização de hardware.  Isso obriga o Microsoft Edge a baixar recursos novamente e recarregar.  É possível que os recursos usados sejam provenientes de uma versão em cache | `Ctrl`+`F5`or`Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Pesquisar texto dentro do painel atual.  Não é compatível com os painéis auditorias, aplicativo e segurança | `Ctrl`+`F` | `Command`+`F` |  
| Mostrar o painel de pesquisa na gaveta, o que permite Pesquisar texto em todos os recursos carregados | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir um arquivo no painel fontes | `Ctrl`+`O`or`Ctrl`+`P` | `Command`+`O`or`Command`+`P` |  
| Ampliar | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Reduzir | `Ctrl`+`-` | `Command`+`-` |  
| Restaurar o nível de zoom padrão | `Ctrl`+`0` | `Command`+`0` |  
| Executar trecho | `Ctrl`+`O`ou `Ctrl` + `P` , digite `!` seguido do nome do script e pressione `Enter` | Pressione `Command` + `O` ou `Command` + `P` , digite `!` seguido do nome do script e pressione `Enter` |  
| Mostrar código-fonte HTML não editável em uma nova guia | `Ctrl`+`U` | N/A |  

> [!NOTE]
> Se você estiver Depurando e pausado em um ponto de interrupção, o atalho de **atualização**retomará o tempo de execução primeiro.  

## Consulte também  

*   [DevTools para iniciantes: introdução ao HTML e ao DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Protocolo de DevTools Microsoft Edge (Chromium)][DevtoolsProtocolChromiumIndex]  

## Entrar em contato com a equipe do Microsoft Edge DevTools  

Envie seus comentários para que a equipe do Microsoft Edge Continue melhorando o Microsoft Edge DevTools para você.  Basta selecionar o ícone de **comentários** no devtools ou pressionar o `Alt` + `Shift` + `I` Windows \ ( `Option` + `Shift` + `I` no MacOS \) e digitar qualquer comentário ou solicitação de recurso que você tenha para o devtools.  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Enviar comentários sobre o Microsoft Edge":::
   Enviar comentários sobre o Microsoft Edge
:::image-end:::

<!--![Give feedback on Microsoft Edge](./devtools-guide-chromium/media/devtools-feedback.png)  -->  

Se você quiser visualizar os [recursos mais recentes que chegam ao devtools][DevtoolsGuideChromiumWhatsNewIndex], baixe o [Microsoft Edge Canárias][MicrosoftedgeinsiderDownload], que é criado à noite.  

<!-- image links -->  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools para iniciantes: introdução ao HTML e ao DOM | Documentos da Microsoft"  
[DevtoolsGuideChromiumWhatsNewIndex]: ./devtools-guide-chromium/whats-new.md "O que há de novo no Microsoft Edge (Chromium) DevTools | Documentos da Microsoft"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Protocolo de DevTools Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Complementos do Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Loja da Web Chrome"  
