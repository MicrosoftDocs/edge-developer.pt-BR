---
description: Para ver rapidamente a ordem de tabulação das seções de uma página, use o Visualizador de Ordem de Origem na ferramenta Acessibilidade, à direita da guia Estilos.
title: Teste o suporte ao teclado usando o Visualizador de Ordem de Origem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597168"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a>Teste o suporte ao teclado usando o Visualizador de Ordem de Origem

A ordem de origem de um documento é importante para a tecnologia assistida e pode ser diferente da ordem na qual os elementos aparecem na página renderizada.  Usando CSS, você pode re-ordenar elementos de página de forma visual, mas isso não significa que a tecnologia auxiliar, como leitores de tela, representaria elementos de página na mesma ordem.  

Para garantir que o documento tenha uma **** ordem lógica, você pode usar o Visualizador de Ordem de Origem para rotular diferentes elementos de página com números que especificam a ordem no código-fonte do documento.  O **Visualizador de Ordem de** Origem está na guia **Acessibilidade** (perto da **guia Estilos).**


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a>Analisando a ordem de acesso ao teclado por meio de seções da página

A [página da Web][DevToolsA11yErrorsDemopage] de demonstração de teste de acessibilidade tem uma ordem de tabulação contraintuitiva, onde os usuários de teclado acessam o menu de navegação da barra lateral somente depois de fazer a tabulação de todos os links **Mais.**  O menu de navegação da barra lateral deve ser um atalho para alcançar profundamente o conteúdo da página.  Porém, como você precisa passar por toda a página antes de chegar ao menu de navegação da barra lateral, esse menu de navegação é ineficaz para usuários de teclado.

A `Tab` ordem de chave na página de demonstração é:
1. O **campo** Pesquisa e, em seguida, **o botão ir** para o **campo** Pesquisa.
1. O **botão Mais** na seção **Gatos,** para navegar até uma página da Web "Gatos".  Em seguida, os **outros botões Mais,** para Cachorros, Cavalos, Cavalos e, em seguida, Alpacas.
1. Os links azuis do menu de navegação da **** barra lateral: **Gatos**, **Cachorros,** **Cavalos,** Cavalos e **Alpacas**.
1. A caixa de texto de doação no formulário de doação.
1. Os botões na barra de navegação superior: **Home**, **Adopt a pet**, **Doar**, **Trabalhos**e, em seguida, **Sobre Nós**.
1. A interface top-of-window do navegador.

O motivo da ordem de chave confusa é que a ordem experimentada ao usar um teclado é determinada pela `Tab` ordem de origem do documento.  A ordem experimentado usando um teclado pode ser modificada usando o atributo em elementos, o que tira esse elemento `tabindex` da ordem de origem.

No código-fonte do documento, o menu de navegação da barra lateral é exibido após o conteúdo principal da página da Web.  CSS foi usado para posicionar o menu de navegação da barra lateral acima da maioria do conteúdo principal da página da Web. 

Você pode testar a ordem dos elementos de página usando o Visualizador de Ordem **de Origem** na guia **Acessibilidade.**  O **Visualizador de Ordem de Origem** é um recurso experimental. Para obter mais informações, navegue até [Source Order Viewer](../experimental-features/index.md#source-order-viewer).


Para ativar o Visualizador de Ordem de Origem:

1.  No DevTools, no canto superior direito, selecione o botão **Configurações** \( Configurações ![ botão ](../media/settings-button-icon.msft.png) \).  

1.  Abaixo **Configurações**, selecione **Experimentos**.  

1.  Selecione a **caixa de seleção Visualizador de Ordem** de Origem.

1.  No canto superior direito da **página** Configurações, selecione **X** para fechar a página Configurações.  Na parte superior do DevTools, a mensagem Uma ou mais configurações foram **alteradas,** o que exige que uma recarga entre em vigor. é exibido.  Selecione o **botão Recarregar DevTools.**



Para ativar e usar o Visualizador de Ordem de Origem, com a página de demonstração:

1.  Abra a [página da Web de demonstração de teste de acessibilidade][DevToolsA11yErrorsDemopage] em uma nova guia.  Em seguida, **selecione F12** para abrir o DevTools.

1.  Na ferramenta **Elementos,** à direita da guia **Estilos,** selecione **a guia** Acessibilidade.

1.  Na seção **Visualizador de Ordem de** Origem, selecione a caixa de seleção **Mostrar ordem de** origem.  Na página da Web renderizada, os números aparecem, indicando a ordem como controlada pela ordem de linhas de `Tab` código no arquivo de origem.

1.  Na árvore DOM na ferramenta **Elementos,** selecione um elemento de layout principal, como o `header` elemento.  As sobreposições numéricas agora são exibidas em seções da página renderizada, que indicam a ordem de origem dos diferentes elementos. 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Ativar o Visualizador de Ordem de Origem mostra a ordem dos elementos na origem como sobreposições na página" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        Ativar o **Visualizador de Ordem** de Origem mostra a ordem dos elementos na origem como sobreposições na página
    :::image-end:::
    
1.  Role a página para ver todas as sobreposições numéricas, incluindo na seção rodapé da página.


## <a name="see-also"></a>Consulte também

*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
