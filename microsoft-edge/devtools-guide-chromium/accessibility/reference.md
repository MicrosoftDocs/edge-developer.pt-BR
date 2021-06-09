---
description: Uma lista dos recursos de teste de acessibilidade no Microsoft Edge DevTools.
title: Recursos de teste de acessibilidade no DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a906d60bb74d927fd86c21af1535a8f62eb93cad
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597040"
---
# <a name="accessibility-testing-features-in-devtools"></a>Recursos de teste de acessibilidade no DevTools

Para testar suas páginas da Web para acessibilidade, primeiro faça uma lista de verificação dos aspectos de acessibilidade a testar e, em seguida, use os recursos relevantes do DevTools para verificar cada aspecto.

| Aspecto de acessibilidade a ser verificar | Recurso do DevTools | Artigo ou subcapação |
|---|---|---|
| Verificar se as imagens têm texto alt | **Problemas** da ferramenta > **seção Acessibilidade** do relatório | [Verificar se as imagens têm texto alt](test-issues-tool.md#verify-that-images-have-alt-text) |
| Verificar o suporte ao teclado | **Inspecionar** a seção > **Acessibilidade** da sobreposição | [Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web](test-inspect-tool.md) |
| Verificar o suporte ao teclado | `Tab`, `Shift+Tab` e `Enter` teclas | [Verifique o suporte ao teclado usando as teclas Tab e Enter](test-tab-enter-keys.md) |
| Verificar o suporte ao teclado: verifique se o foco está indicado | **Ferramenta Inspecionar,** **Guia Estilos** e **Ferramenta Fontes** | [Analise a falta de indicação do foco do teclado em um menu de barra lateral](test-analyze-no-focus-indicator.md) |
| Verificar o suporte ao teclado: verifique se os botões de formulário podem ser usados com o teclado | **Ferramenta Inspecionar,** **árvore DOM** na ferramenta **Elementos** e guia **Ouvintes de** Eventos | [Analise a falta de suporte ao teclado em um formulário](test-analyze-no-keyboard-support.md) |
| Verificar o suporte ao teclado: verificar `Tab` a ordem da chave | **Ferramenta Elements** > **guia Acessibilidade >** **Visualizador de Ordem de Origem** | [Teste o suporte ao teclado usando o Visualizador de Ordem de Origem](test-tab-key-source-order-viewer.md) |
| Verifique se o texto tem contraste suficiente (automaticamente, para a página inteira) | **Problemas** da ferramenta > **seção Acessibilidade** do relatório | [Verificar se as cores de texto têm contraste suficiente](test-issues-tool.md#verify-that-text-colors-have-enough-contrast) |
| Verificar se o texto tem contraste suficiente | **Ferramenta Elements** > **guia Estilos** > **Selador de Cores** | [Teste o contraste da cor do texto usando o Seletor de Cor](color-picker.md) |
| Verificar se o texto tem contraste suficiente | **Inspecionar** a seção > **Acessibilidade da** linha > **Contraste** | [Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web](test-inspect-tool.md) |
| Verifique se o texto tem contraste suficiente: no estado de foco | **Ferramenta Elements** > **Estilos >** Estado **do Elemento Toggle** | [Verifique a acessibilidade de todos os estados dos elementos](test-inspect-states.md) |
| Verifique se o texto tem contraste suficiente: com tema escuro (modo escuro) e tema claro | **Ferramenta** de renderização > recurso de **mídia CSS emular prefere esquema de cores** | [Verifique se há problemas de contraste com o tema escuro e o tema claro](test-dark-mode.md) |
| Verificar o suporte ao leitor de tela: Verifique se os campos de entrada têm rótulos | **Problemas** da ferramenta > **seção Acessibilidade** do relatório | [Verificar se os campos de entrada têm rótulos](test-issues-tool.md#verify-that-input-fields-have-labels) |
| Verificar o suporte ao leitor de tela | **Inspecionar** a seção > **Acessibilidade da** sobreposição > **Nome** e **Função** | [Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web](test-inspect-tool.md) |
| Verificar o suporte ao leitor de tela | **Ferramenta Elements** > **guia Acessibilidade** > **Árvore de Acessibilidade** | [Verifique a Árvore de Acessibilidade para suporte a teclado](test-accessibility-tree.md)e leitor de tela e Teste acessibilidade usando a guia [Acessibilidade](accessibility-tab.md) |
| Verifique se a página da Web pode ser usável por pessoas com falta de cor | **Ferramenta** de renderização > lista de listas de lista lista suspenso de **deficiências de visão** emular | [Verifique se a página pode ser usada por pessoas com daltonismo](test-color-blindness.md) |
| Verifique se a página da Web é usável com visão desfocado | **Ferramenta** de renderização > lista de listas de lista lista suspenso de **deficiências de visão** emular | [Verifique se a página pode ser usada com visão turva](test-blurred-vision.md) |
| Verifique se a página da Web pode ser usável com a animação da interface do usuário desligada (movimento reduzido) | **Ferramenta** de renderização > **recurso de mídia CSS emular prefere-reduced-motion** | [Verifique se a página pode ser usada com a animação da interface do usuário desligada](test-reduced-ui-motion.md) |
| Verifique se o layout da página da Web é acessível quando estreito | **Ferramenta de Emulação de** Dispositivo | [Verifique se o layout da página da Web é acessível](accessibility-testing-in-devtools.md#verify-that-the-webpage-layout-is-usable-when-narrow)quando estreito e emular dispositivos móveis [Microsoft Edge DevTools](../device-mode/index.md) |


## <a name="see-also"></a>Consulte também

*   [Visão geral dos testes de acessibilidade usando o DevTools][DevtoolsAccessibilityAccessibilitytestingindevtools]
*   [Navegue Microsoft Edge DevTools com tecnologia assistida][DevtoolsAccessibilityNavigation]
*   [Testes de acessibilidade][DevtoolsAccessibilityTest]
*   [Princípios de acessibilidade e práticas recomendadas][MDNAccessibility]
*   [Leitor de tela][MDNScreenReader]


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
[DevtoolsAccessibilityTest]: ../../accessibility/test.md "Teste de acessibilidade | Microsoft Docs"
[DevtoolsAccessibilityAccessibilitytestingindevtools]: accessibility-testing-in-devtools.md "Visão geral dos testes de acessibilidade usando o DevTools | Microsoft Docs"
[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegue Microsoft Edge DevTools com tecnologia | Microsoft Docs"  
<!-- external -->
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Acessibilidade | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Leitor de tela | MDN"  
