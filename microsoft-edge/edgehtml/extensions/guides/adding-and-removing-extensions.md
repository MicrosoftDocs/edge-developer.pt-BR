---
description: Saiba como adicionar e remover extensões, bem como mover o botão da extensão ao lado da barra de endereços.
title: Adicionando e removendo extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento para a web, html, css, javascript, desenvolvedor, extensão
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3473108918ec3cb3945e0999b27873ddea40aa5c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231898"
---
# Adicionar, mover e remover extensões para o Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

O suporte ao Microsoft Edge para extensões foi introduzido na **Atualização de Aniversário do Windows 10**. Se você estiver desenvolvendo uma extensão do Microsoft Edge e deseja carregá-la, ou se você já a tiver e agora quiser removê-la, confira as etapas abaixo.
Também estão incluídos detalhes sobre como alterar o local do ícone de extensão no navegador.

## Adicionar uma extensão

1. Abra o Microsoft Edge e digite 'about:flags' na barra de endereço.

2. Marque a caixa de seleção **Habilitar recursos da extensão do desenvolvedor**.

   ![about:flags ativa os recursos do desenvolvedor](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Se você não tiver a Atualização de Aniversário do Windows 10 ou posterior, essa opção não estará disponível.

3. Selecione **Mais (...)** para abrir o menu.

   ![botão mais](./../media/morebutton.png)  

4. Selecione **Extensões** no menu.

5. Selecione o botão **Extensão de carregamento**.

   ![selecionar a extensão de carregamento](./../media/sideload-load-extension.png)

6. Navegue até a pasta da extensão e selecione o botão **Selecionar pasta**.
   ![selecionar a pasta de extensão a ser carregada](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Se você encontrar uma mensagem de erro ao carregar a extensão, confira a página [solução de problemas](./../troubleshooting.md) para obter ajuda.


**Pronto! Agora você deverá ver a extensão listada no painel extensão do Microsoft Edge.**

![extensão no painel extensão](./../media/sideload-extension-installed.png)

> [!NOTE]
> As extensões não assinadas são desativadas automaticamente nas inicializações subsequentes do Microsoft Edge. Quando o navegador entra em um estado ocioso (após aproximadamente 10 segundos de inatividade), você verá a seguinte notificação na parte inferior da janela. ![notificação de risco](./../media/riskynotification.png) para ativar as extensões não assinadas, clique em "ativar mesmo assim".



## Mover o botão extensão
Dependendo das configurações da extensão, ela pode aparecer no menu **Mais (...)**.

   ![menu Ações-navegador](./../media/browseraction.png)  


Se você quiser mover o botão para fora desse menu para facilitar o acesso:

1. Clicar com o botão direito do mouse no botão extensão.

2. Selecione **Mostrar botão ao lado da barra de endereços**.

   ![menu Ações-menu contextual do navegador](./../media/browseraction_contextmenu.png)  

Como alternativa, você pode fazer isso na página de detalhes das extensões:

1. Clique no botão extensão.
2. Alterne **Mostrar botão ao lado da barra de endereços** para ativado.

   ![Mostrar botão de alternância ativado](./../media/show-button-toggle.png)

> [!NOTE]
> Você sempre poderá mover o botão de volta para o menu**Mais (...)** clicando com o botão direito do mouse nele e desmarcando **Mostrar ao lado da barra de endereços** ou acessando a página detalhes da extensão e alternando **Mostrar botão ao lado da barra de endereços** para desativado.


## Remover uma extensão

1. Abra o Microsoft Edge.

2. Selecione **Mais (...)** para abrir o menu.

3. Selecione **Extensões** no menu.

4. Clique com o botão direito do mouse na extensão que você deseja remover e selecione **Remover**ou selecione a extensão e clique no botão **Remover**.

   ![menu Ações-remover](./../media/remove.png)  

**A extensão deve desaparecer da lista no Microsoft Edge.**
