---
description: Microsoft Edge (Chromium) e Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs, visual studio, depurador
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387271"
---
# <a name="visual-studio"></a>Visual Studio  

O [Microsoft Visual Studio][MicrosoftVisualstudioVs] é um ambiente de desenvolvimento integrado \(IDE\).   Use-o para editar, depurar, criar e publicar seus aplicativos Web.  É um programa rico em recursos que pode ser usado para muitos aspectos do desenvolvimento da Web.  Além do editor padrão e do depurador que a maioria das IDEs fornece, Visual Studio inclui os seguintes recursos para facilitar seu processo de desenvolvimento.  

*   compiladores  
*   ferramentas de conclusão de código  
*   designers gráficos  
*   muitos mais  
    
Se você ainda não estiver usando Visual Studio, navegue até [Baixar][MicrosoftVisualstudioDownloads] Visual Studio para baixá-lo.  

Atualmente, o Visual Studio 2019 oferece suporte à depuração do JavaScript no Microsoft Edge para seus aplicativos ASP.NET Framework e ASP.NET Core.  Conclua as etapas a seguir para usar Visual Studio para depurar Microsoft Edge.  

## <a name="launch-microsoft-edge"></a>Iniciar Microsoft Edge  

Visual Studio o fluxo de trabalho a seguir usando um único botão.  

1.  Cria seu ASP.NET e ASP.NET Core app.  
1.  Inicia seu servidor Web.  
1.  Inicia Microsoft Edge.  
1.  Conecta o Visual Studio depurador.  
    
O fluxo de trabalho simplificado permite depurar JavaScript que é executado Microsoft Edge diretamente do seu IDE.  

### <a name="create-a-new-aspnet-core-web-app"></a>Criar um novo ASP.NET Core web  

Abra Visual Studio 2019 e escolha **Criar um novo projeto.**  Na próxima tela, escolha ASP.NET Core **Web App**  >  **Next**.  

:::image type="complex" source="./media/create-new-project.png" alt-text="Criar um novo ASP.NET Core Web" lightbox="./media/create-new-project.png":::
   Criar um novo ASP.NET Core Web  
:::image-end:::  

Forneça um **Project para** seu novo projeto e escolha **Criar**.  Para os fins do exemplo, ** escolha **React.jscomo o modelo e escolha **Criar**.  O **React.js** especifica como integrar o React.js com um ASP.NET Core aplicativo.  

### <a name="launch-microsoft-edge-from-visual-studio"></a>Iniciar Microsoft Edge de Visual Studio  

Depois de criar seu projeto, abra `ClientApp/src/components/Counter.js` .  Agora, para usar Visual Studio para depurar JavaScript, escolha a lista suspenso ao lado do botão **verde Reproduzir** **e IIS Express**.  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="O menu suspenso ao lado do botão verde Reproduzir e IIS Express" lightbox="./media/vs-dropdown.png":::
   O menu suspenso ao lado do botão **verde Reproduzir** **e IIS Express**  
:::image-end:::  

Escolha **Depuração de Script**  >  **Habilitada**.  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Ativar a depuração de script no Visual Studio" lightbox="./media/enable-script-debugging.png":::
   Ativar a depuração de script no Visual Studio  
:::image-end:::  

No mesmo menu suspenso, escolha Navegador da **Web** > o canal de visualização do Microsoft Edge que você deseja Visual Studio iniciar, como Microsoft Edge Canary, Dev ou Beta.  Se você ainda não estiver usando um dos canais Microsoft Edge de visualização, navegue até Baixar Microsoft Edge [Canais Insider][MicrosoftedgeinsiderDownload] para baixar um.  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Escolha o canal de visualização Microsoft Edge que você deseja Visual Studio iniciar" lightbox="./media/set-web-browser.png":::
   Escolha o canal de visualização Microsoft Edge que você deseja Visual Studio iniciar  
:::image-end:::  

> [!NOTE]
> Se você escolher Microsoft Edge \(EdgeHTML\), Visual Studio o iniciará em vez de Microsoft Edge \(Chromium\).  [Instale][MicrosoftedgeinsiderDownload] um dos canais de visualização do Microsoft Edge ou certifique-se de que a versão do Microsoft Edge instalada em seu computador seja Microsoft Edge \(Chromium\) e não Microsoft Edge \(EdgeHTML\).  

Agora que Visual Studio está configurado corretamente, escolha o botão **verde Reproduzir.**  Visual Studio criar seu aplicativo, iniciar o servidor Web, iniciar Microsoft Edge e navegar até ou qualquer `https://localhost:44362/` porta especificada em `launchSettings.json` .  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge inicia a partir Visual Studio" lightbox="./media/edge-launch.png":::
   Microsoft Edge inicia a partir Visual Studio  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a>Depurar JavaScript em execução Microsoft Edge  

Alternar de volta para Visual Studio.  Em `Counter.js` , para definir um ponto de interrupção na Linha 13, escolha a canalização ao lado da linha.  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Escolha a canalização ao lado da Linha 13 Counter.js definir um ponto de interrupção no Visual Studio" lightbox="./media/set-breakpoint.png":::
   Escolha a canalização ao lado da Linha 13 para definir um ponto de interrupção `Counter.js` no Visual Studio  
:::image-end:::  

Agora alternar de volta para a instância de Microsoft Edge que Visual Studio foi lançada.  Escolha no **Contador** no NavMenu à esquerda da página da Web.  Agora escolha **Increment**.  

:::image type="complex" source="./media/edge-counter.png" alt-text="A página Contador em nosso ASP.NET Core Web" lightbox="./media/edge-counter.png":::
   A página Contador em nosso ASP.NET Core Web  
:::image-end:::  

O depurador JavaScript no Visual Studio atinge o ponto de interrupção definido em `Counter.js` .  Visual Studio agora pausa o tempo de execução do JavaScript em execução no Microsoft Edge e você pode passar pelo script linha por linha.  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio o JavaScript em execução no Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   Visual Studio o JavaScript em execução no Microsoft Edge  
:::image-end:::  

O exemplo foi apenas uma pequena demonstração da funcionalidade disponível no Visual Studio.  Para obter mais informações sobre a funcionalidade no Visual Studio 2019, navegue [até Visual Studio documentação][VisualStudioWindowsIndex].  

## <a name="attach-to-microsoft-edge"></a>Anexar a Microsoft Edge  

Anteriormente, você precisava iniciar Microsoft Edge de Visual Studio.  Agora, você pode anexar o Visual Studio depurador a uma instância de Microsoft Edge.  

Primeiro, verifique se não há instâncias em execução de Microsoft Edge.  Agora, na linha de comando, execute o seguinte comando.  

```console
start msedge –remote-debugging-port=9222
```  

No Visual Studio, abra o menu **Depurar** e escolha **Anexar ao Processo** ou selecione `Ctrl` + `Alt` + `P` .  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Escolha Anexar ao processo no Visual Studio" lightbox="./media/attach-to-process.png":::
   Escolha **Anexar ao processo** no Visual Studio  
:::image-end:::  

Na caixa **de diálogo Anexar ao Processo,** de definir **Tipo** de conexão como Websocket de protocolo do **Chrome devtools (sem autenticação)**.  Na caixa **de texto Conectar destino,** digite `http://localhost:9222/` e selecione `Enter` .  Revise a lista de guias abertas que você Microsoft Edge listada na caixa **de diálogo Anexar ao Processo.**  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configure a caixa de diálogo Anexar ao Processo Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   Configure a **caixa de diálogo Anexar ao Processo** Visual Studio  
:::image-end:::  

Escolha **Selecionar...** > caixa de seleção ao lado de **JavaScript (Microsoft Edge – Chromium)**.  Para adicionar guias, navegue até novas guias e feche guias **** e exibe as alterações refletidas na caixa de diálogo Anexar ao Processo, escolha o **botão Atualizar.**  Escolha a guia que você deseja depurar e escolha **Anexar**.  

O Visual Studio depurador agora está anexado ao Microsoft Edge.  Você pode pausar a execução do JavaScript, definir pontos de interrupção e revisar instruções diretamente na janela `console.log()` Depurar Saída em Visual Studio.  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a>Entrar em contato com a Microsoft Visual Studio equipe  

As equipes Microsoft Visual Studio e Microsoft Edge querem saber mais sobre como você trabalha com JavaScript no Visual Studio.  Para enviar seus comentários, escolha o **ícone Enviar Comentários** no Visual Studio ou tweet @VisualStudio e [@EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].  

:::image type="complex" source="./media/feedback-icon.png" alt-text="O ícone Enviar Comentários no Visual Studio" lightbox="./media/feedback-icon.png":::
   O **ícone Enviar Comentários** no Visual Studio  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentação | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Baixar Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet para @VisualStudio e @EdgeDevTools | Twitter"  
