---
description: Fornece orientações sobre como personalizar a exibição do botão de revelação de senha
title: Personalize o botão de mostrar senha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web, revelação de senha, ícone do olho
ms.openlocfilehash: 93f618d28e5fa2f16dda87b4122a097ef40618c9
ms.sourcegitcommit: 1f0b2534b51417bb19d05945fea54ddad977e88f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526155"
---
# <a name="customize-the-password-reveal-button"></a>Personalize o botão de mostrar senha  

O `password` tipo de entrada no Microsoft Edge inclui um controle de **revelação de** senha.  Um usuário pode escolher o botão **de entrada de** senha para revelar o campo **senha.**  O campo **senha revelada** ajuda o usuário a verificar se a senha está corretamente.  Depois que um usuário **** tiver inserido texto no **** campo senha, um usuário poderá escolher o botão de revelação de senha ou selecionar para alternar a `Alt` + `F8` visibilidade da entrada.  

:::row:::
   :::column span="":::
      Um **campo** de senha com pontos ocultando os caracteres inseridos por um usuário.  O **botão de** revelação de senha aparece à direita do campo de **senha.**
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Alterne o **botão de** revelação de senha para alterar o ícone do olho para um ícone de olho com uma barra através dele e para revelar o texto da senha original.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="O ícone em forma de olho tem uma barra nele e o texto de senha original é exibido" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         O ícone em forma de olho tem uma barra nele e o texto de senha original é exibido :::image-end:::  
   :::column-end:::
:::row-end:::  

Por padrão, o **botão de** revelação de senha insere no DOM sombra de todos os elementos HTML com o conjunto `input` como `type` `"password"` .  A partir Microsoft Edge versão 87, os usuários ou [empresas][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] podem desabilitar esse recurso globalmente.  Você, web designers e desenvolvedores, deve esperar que a maioria Microsoft Edge usuários tenham a experiência padrão.  

## <a name="remove-the-password-reveal-control"></a>Remover o controle de revelação de senha  

Você pode remover completamente o **botão de revelação** de senha direcionando o `::-ms-reveal` pseudo elemento.  

```css
::-ms-reveal {
    display: none;
}
```  

No entanto, você deve considerar tirar proveito do botão de **revelação de** senha.  O botão **de revelação de** senha nativa tem medidas [de segurança importantes internas](#visibility-of-the-control) no comportamento.  

## <a name="customize-the-control-style"></a>Personalizar o estilo de controle  

Em vez de remover totalmente o controle, você pode, em vez disso, modificar o estilo do botão de revelação de senha para melhor corresponder à linguagem visual do site. ****  O trecho a seguir fornece um exemplo desse estilo.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Lembre-se das seguintes coisas ao estilo do botão **de revelação de** senha.  

*   O ícone do olho é implementado como uma imagem de plano de fundo.  Para adicionar uma cor **** de plano de fundo ao botão de revelação de senha, use a propriedade CSS `background-color` em vez da propriedade `background` shorthand.  
*   Você pode ajustar o tamanho e a escala do botão **revelar senha.**  
    
    > [!NOTE]
    >O navegador oculta qualquer estouro fora dos limites do controle de entrada de senha.  
    
*   Atualmente, nenhum seletor de estado está disponível para estilizou o estado alternado do botão de **revelação de** senha.  
    
## <a name="visibility-of-the-control"></a>Visibilidade do controle  

O **botão de revelação** de senha não estará disponível até que o usuário insira texto no **campo senha.**  Para ajudar a manter a entrada de senha do usuário segura, o navegador suprime o botão nos cenários a seguir.

*   Se o foco se afastar do campo **senha,** o navegador removerá o botão **de revelação de** senha.  
*   Se os scripts modificarem o campo **de** senha, o navegador removerá o botão **de revelação de** senha.  

Se o **botão de revelação** de senha for **** removido, **** o usuário deverá excluir o conteúdo do campo de senha antes que o botão de revelação de senha seja exibido novamente. Esse comportamento impede que alguém faz um pequeno ajuste para exibir a senha, caso o usuário se afaste de um dispositivo desbloqueado.
    
O **botão de revelação** de senha não estará disponível se **o** campo de senha for automaticamente contabilizados usando o gerenciador de senhas.  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Políticas | Microsoft Docs"  
