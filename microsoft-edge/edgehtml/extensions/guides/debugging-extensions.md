---
description: Com as Ferramentas de Desenvolvedor F12, saiba como depurar o script em segundo plano, scripts de conteúdo e páginas de extensão de uma extensão.
title: Depuração | Extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, javascript, desenvolvedor, depuração, depuração
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399362"
---
# <a name="debugging-extensions"></a>Depurar extensões  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Você pode depurar suas extensões no Microsoft Edge usando as Ferramentas de Desenvolvedor F12.  

O vídeo a seguir passa por uma extensão de bugs do Microsoft Edge, acompanhando cada cenário de depuração e corrigindo-o ao longo do caminho.  Confira as instruções passo a passo abaixo para obter mais informações.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> Para aproveitar a depuração de extensão com F12, primeiro você deve ativar os recursos do desenvolvedor em about:flags.  Consulte [Adicionando e removendo extensões](./adding-and-removing-extensions.md) para obter detalhes sobre como fazer isso.  

## <a name="background-script-debugging"></a>Depuração de script em segundo plano  

Para começar a depurar o script em segundo plano da extensão:  

1.  Clique em **Mais (...)** seguido de **Extensões** para entrar no painel de extensão.  
    
    ![botão mais](../media/morebutton.png)  
    
1.  Clique na extensão que você deseja depurar.  
1.  Clique no link **Página em segundo** plano para trazer o F12 para o processo em segundo plano.  
    
    ![exibição de extensão selecionada de opções com link de inspeção](../media/debug-inspect.png)  
    
1.  Selecione a **guia Depurador** no F12.  
1.  Navegue até e selecione o script em segundo plano da extensão.  
1.  Coloque pontos de interrupção para depuração clicando à esquerda do número da linha de código-fonte.  
    
    ![console f12 mostrando script em segundo plano com pontos de quebra](../media/debug-f12-background.png)  
    
1.  Selecione a **guia Console** e execute o `location.reload()` comando.  Isso executará o script em segundo plano, permitindo que você execute o código.  
    
    ![console com location.reload inserido](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a>Depuração de script de conteúdo  

Para começar a depurar o script de conteúdo da extensão:  

1.  Iniciar F12 navegando até o botão **Mais (...)** e selecionando Ferramentas de Desenvolvedor **F12** ou pressionando `F12` o teclado.  
1.  Navegue até e selecione o script de conteúdo da extensão.  Scripts de conteúdo para extensões em execução serão representados por uma pasta diferente para cada extensão.  
    
    > [!NOTE]
    > Somente os scripts de conteúdo em execução serão exibidos.  
    
1.  Coloque pontos de interrupção para depuração clicando à esquerda do número da linha de código-fonte.  
    
    ![f12 com script de conteúdo sendo depurado](../media/debug-content-f12.png)  
    
1.  Atualize a guia do navegador para começar a fazer a revisão do código.  
    
## <a name="extension-page-debugging"></a>Depuração de página de extensão  

Há dois métodos que podem ser usados para acessar o código-fonte da página de extensão para depuração.  Um método se aplica a uma variedade de páginas enquanto o outro só funciona para páginas pop-up.  

### <a name="debugging-any-extension-page"></a>Depurando qualquer página de extensão  

O método a seguir funciona para todas as páginas de extensão, como a página de opções e pop-ups:  

1.  Clique com o botão direito do mouse no plano de fundo da página.  
1.  Selecione **Exibir fonte**.  
    
    ![Abrir depuração pop-up com f12](../media/debug-popup-select.png)  
    
1.  Quando f12 é aberto, coloque pontos de interrupção no arquivo que você deseja depurar.  
    
    ![depuração pop-up com f12](../media/debug-popup-f12.png)  
    
1.  Selecione a **guia Console** e execute o comando `location.reload()` .  Isso executará o script de página de novo, permitindo que você execute seu código.  
    
    ![console com location.reload inserido](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a>Depurando uma página de extensão pop-up  

Embora o método de depuração de páginas de extensão também se aplique a páginas de extensão pop-up, as etapas a seguir definem outra maneira de depurar seu pop-up:  

1.  Clique com o botão direito do mouse no ícone da extensão.  
1.  Selecione **Inspecionar pop-up**.  
    
    ![inspeção de depuração pop-up](../media/debug-popup-inspect.png)  
    
1.  Siga as etapas 3 e 4 acima para colocar pontos de interrupção e recarregar o pop-up.  
    