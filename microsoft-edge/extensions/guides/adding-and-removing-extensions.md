---
description: Saiba como adicionar e remover extensões, bem como mover um botão de extensão ao lado da barra de endereços.
title: Adicionando e removendo extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, extensão
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561230"
---
# Adicionar, mover e remover extensões do Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

O suporte do Microsoft Edge para extensões foi apresentado na **atualização de aniversário do Windows 10**. Se você estiver desenvolvendo uma extensão do Microsoft Edge e quiser carregá-la, ou se já tiver e agora deseja removê-la, Confira as etapas abaixo.
Também estão incluídos detalhes sobre como alterar o local do ícone de extensão no navegador.

## Adicionando uma extensão

1. Abra o Microsoft Edge e digite ' about: flags ' na barra de endereços.

2. Marque a caixa de seleção **habilitar recursos de desenvolvedor de extensão** .

   ![sobre: indicadores ative os recursos de desenvolvedor](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Se você não tiver a atualização de aniversário do Windows 10 ou posterior, essa opção não estará disponível.

3. Selecione **mais (...)** para abrir o menu.

   ![botão mais](./../media/morebutton.png)  

4. Selecione **extensões** no menu.

5. Selecione o botão **carregar extensão** .

   ![selecionando a extensão de carga](./../media/sideload-load-extension.png)

6. Navegue até a pasta da extensão e selecione o botão **Selecionar pasta** .
   ![selecionando a pasta de extensão para carregar](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Se você encontrar uma mensagem de erro ao carregar a extensão, consulte a página de [solução de problemas](./../troubleshooting.md) para obter orientação.


**Tudo pronto! Agora você deve ver a extensão listada no painel extensão da Microsoft Edge.**

![extensão no painel de extensão](./../media/sideload-extension-installed.png)

> [!NOTE]
> As extensões não assinadas são desativadas automaticamente em inicializações subsequentes do Microsoft Edge. Quando o navegador entra em um estado ocioso (após cerca de 10 segundos de inatividade), você verá a seguinte notificação na parte inferior da janela. ![notificação arriscada ](./../media/riskynotification.png) para ativar as extensões não assinadas, clique em "ativar de qualquer maneira".



## Movendo o botão extensão
Dependendo das configurações da extensão, ela pode aparecer no menu **mais (...)** .

   ![menu ações](./../media/browseraction.png)  


Se você quiser mover o botão para o menu para facilitar o acesso:

1. Clique com o botão direito do mouse no botão extensão.

2. Selecione o **botão Mostrar ao lado da barra de endereços**.

   ![menu ações](./../media/browseraction_contextmenu.png)  

Você também pode fazer isso na página de detalhes de extensões:

1. Clique no botão extensão.
2. Botão de alternância de **mostrar ao lado da barra de endereços** para ativado.

   ![botão de alternância Mostrar ativado](./../media/show-button-toggle.png)

> [!NOTE]
> Você sempre pode mover o botão de volta para o menu **mais (...)** clicando com o botão direito do mouse nele e desmarcando **mostrar ao lado da barra de endereços** ou acessando a página detalhes da extensão e alternando **Mostrar botão ao lado de barra de endereços** para desativar.


## Removendo uma extensão

1. Abra o Microsoft Edge.

2. Selecione **mais (...)** para abrir o menu.

3. Selecione **extensões** no menu.

4. Clique com o botão direito do mouse na extensão que você deseja remover e selecione **remover**ou selecione a extensão e clique no botão **remover** .

   ![menu ações](./../media/remove.png)  

**A extensão deve desaparecer da lista no Microsoft Edge.**
