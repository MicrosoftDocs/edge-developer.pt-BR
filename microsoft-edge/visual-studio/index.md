---
description: Microsoft Edge (Chromium) e Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, vs, Visual Studio, depurador
ms.openlocfilehash: 3fc2e2c3dc21689d8c378ccbe33e4dff813ea12f
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986189"
---
# Visual Studio

O Microsoft [Visual Studio](https://visualstudio.microsoft.com/vs/) é um IDE (ambiente de desenvolvimento integrado) que você pode usar para editar, depurar, criar e publicar seus aplicativos Web. É um programa rico em recursos que pode ser usado para muitos aspectos do seu desenvolvimento na Web. Acima do editor e do depurador padrão que a maioria dos IDEs fornece, o Visual Studio inclui compiladores, ferramentas de auto-completar de código, designers gráficos e muitos outros recursos para facilitar o processo de desenvolvimento. Vá até [esta página](https://visualstudio.microsoft.com/downloads/) para baixar o Visual Studio se você ainda não o estiver usando.

Atualmente, o Visual Studio 2019 é compatível com a depuração de JavaScript no Microsoft Edge para a estrutura do ASP\.NET e aplicativos principais do ASP\.NET. Siga as etapas abaixo para depurar o Microsoft Edge do Visual Studio.

## Iniciar o Microsoft Edge
O Visual Studio cria o aplicativo de núcleo do ASP\.NET e do ASP\.NET, inicia o servidor Web, inicia o Microsoft Edge e conecta o depurador do Visual Studio, tudo com o clique de um botão único. Isso permite que você depure a execução de JavaScript no Microsoft Edge diretamente do IDE!

### Criar um novo aplicativo Web do ASP.NET Core

Abra o Visual Studio 2019 e selecione **criar um novo projeto**. Na tela seguinte, selecione **ASP\.NET Core Web aplicativo** e clique em **Avançar**.

> ##### Figura 1  
> Criar um novo aplicativo Web ASP.NET Core ![ criar um novo aplicativo Web de núcleo do ASP.net](./media/create-new-project.png)  

Forneça um **nome de projeto** para seu novo projeto e clique em **criar**. Para os fins deste exemplo, selecione **React.js** como o modelo que mostra como integrar React.js com um aplicativo ASP.NET Core e clique em **criar**.

### Iniciar o Microsoft Edge do Visual Studio

Após a criação do projeto, abra **ClientApp/src/Components/Counter.js**. Agora, indique ao Visual Studio para Depurar JavaScript selecionando o menu suspenso ao lado do botão verde **Play** e o **IIS Express**. 

> ##### Figura 2  
> O menu suspenso ao lado do botão verde **reproduzir** e o **IIS expressou** 
> ![ o menu suspenso ao lado do botão verde reproduzir e do IIS Express](./media/vs-dropdown.png)  

Selecione **depuração de script** e clique em **habilitado**.

> ##### Figura 3  
> Habilitar a depuração de script no Visual Studio ![ habilitar a depuração de script no Visual Studio](./media/enable-script-debugging.png)  

Na mesma lista suspensa, selecione **navegador da Web** e clique no canal de visualização do Microsoft Edge que você deseja que o Visual Studio inicie: Microsoft Edge Canárias, dev ou beta. Se ainda não fez [isso, acesse esta página](https://www.microsoftedgeinsider.com/download) para instalar os canais de visualização do Microsoft Edge.

> ##### Figura 4  
> Selecione o canal de visualização do Microsoft Edge que você deseja que o Visual Studio inicie ![ Selecione o canal de visualização do Microsoft Edge que você deseja que o Visual Studio inicie](./media/set-web-browser.png)  

> [!NOTE]
> Se você selecionar o Microsoft Edge (EdgeHTML), o Visual Studio iniciará isso em vez do Microsoft Edge (Chromium). [Instale os canais de visualização do Microsoft Edge](https://www.microsoftedgeinsider.com/download) e selecione-os ou certifique-se de que a versão do Microsoft Edge instalada em seu computador seja o Microsoft Edge (Chromium) e não o Microsoft Edge (EdgeHTML).

Agora que o Visual Studio está configurado corretamente, clique no botão de **reprodução** verde. O Visual Studio criará seu aplicativo, iniciará o servidor Web, iniciará o Microsoft Edge e navegará até a `https://localhost:44362/` porta ou qualquer porta especificada em **launchSettings.js**.

> ##### Figura 5  
> Microsoft Edge iniciado do Visual Studio ![ Microsoft Edge iniciado a partir do Visual Studio](./media/edge-launch.png)  

### Depurar JavaScript em execução no Microsoft Edge

Retorne ao Visual Studio. Em **Counter.js**, defina um ponto de interrupção na linha 13 clicando na medianiz ao lado da linha.

> ##### Figura 6
> Configurando um ponto de interrupção no Visual Studio clicando na medianiz ao lado da linha 13 em **Counter.js** 
> ![ definindo um ponto de interrupção no Visual Studio clicando na medianiz ao lado da linha 13 em Counter.js](./media/set-breakpoint.png)  

Agora, alterne de volta para a instância do Microsoft Edge iniciada pelo Visual Studio. Clique em **Counter (contador** ) na NavMenu à esquerda da página. Agora, clique em **Increment**.

> ##### Figura 7
> A página de contador em nosso aplicativo Web ![ de núcleo do ASP.net a página do contador em nosso aplicativo Web principal do ASP.net](./media/edge-counter.png)  

O depurador de JavaScript no Visual Studio vai chegar ao ponto de interrupção que definimos em **Counter.js**. O Visual Studio agora pausou a execução do JavaScript em execução no Microsoft Edge e você pode percorrer o script linha por linha.

> ##### Figura 8
> Visual Studio pausar JavaScript executando no Microsoft Edge ![ Visual Studio pausar o JavaScript em execução no Microsoft Edge](./media/hit-breakpoint.png)  

Este exemplo era apenas uma demonstração mínima da funcionalidade disponível no Visual Studio. Saiba mais sobre todas as coisas que você pode fazer no Visual Studio 2019 lendo [a documentação dela](https://docs.microsoft.com/visualstudio/windows/?view=vs-2019).

## Anexar ao Microsoft Edge
No fluxo de trabalho anterior, o Visual Studio inicia o Microsoft Edge. Com esse fluxo de trabalho, você poderá anexar o depurador do Visual Studio a uma instância já em execução do Microsoft Edge. 

Primeiro, verifique se não há instâncias em execução do Microsoft Edge. Agora, no seu terminal, execute o seguinte comando:

```console
start msedge –remote-debugging-port=9222
```

No Visual Studio, abra o menu **depurar** e selecione **anexar ao processo** ou pressione `Ctrl`  +  `Alt`  +  `P` .

> ##### Figura 9
> Selecionando **anexar ao processo** no Visual Studio ![ selecionando * * anexar ao processo * * no Visual Studio](./media/attach-to-process.png)  

Na caixa de diálogo **anexar ao processo** , defina o **tipo de conexão** como **WebSocket do protocolo Chrome devtools (sem autenticação)**. Na caixa de texto **conexão de destino** , digite `http://localhost:9222/` e pressione `Enter` . Você deve ver a lista de guias abertas que você tem no Microsoft Edge listada na caixa de diálogo **anexar ao processo** .

> ##### Figura 10
> Configurando a caixa de diálogo **anexar ao processo** no Visual Studio ![ Configurando a caixa de diálogo anexar para processar no Visual Studio](./media/attach-to-process-dialog.png)  

Clique em **selecionar..** . e marque **JavaScript (Microsoft Edge – Chromium)**. Você pode adicionar guias, navegar para novas guias e fechar guias e ver essas alterações refletidas na caixa de diálogo **anexar ao processo** clicando no botão **Atualizar** . Selecione a guia que você deseja depurar e clique em **anexar**.

O depurador do Visual Studio agora está anexado ao Microsoft Edge! Você pode pausar a execução do JavaScript, definir pontos de interrupção e ver `console.log()` instruções diretamente na janela de saída de depuração do Visual Studio.

## Entrar em contato com a equipe do Microsoft Visual Studio  

Estamos ansiosos para saber mais sobre como trabalhar com JavaScript no Visual Studio!  Envie-nos comentários clicando no ícone de **comentários** do Visual Studio ou em tweeting [ @VisualStudio and @EdgeDevTools](https://twitter.com/intent/tweet?text= @VisualStudio + @EdgeDevTools).  

> ##### Figura 11
> O ícone de **comentários** no Visual Studio ![ o ícone de comentários no Visual Studio](./media/feedback-icon.png)  
