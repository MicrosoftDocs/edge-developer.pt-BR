---
description: Fornece orientações sobre como personalizar a exibição do botão revelar senha
title: Personalizar o botão revelar senha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma web, revelação de senha, ícone de olho
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327705"
---
# Personalizar o botão revelar senha  

O `password` tipo de entrada no Microsoft Edge inclui um controle de **revelação de** senha.  Um usuário pode escolher o botão **de entrada de** senha para revelar o campo **de** senha.  O campo **de senha** revelado ajuda o usuário a verificar se a senha está corretamente.  Depois que um usuário inserir texto no **campo** **** de senha, um usuário poderá escolher o botão de revelar a senha ou optar por alternar a `Alt` + `F8` visibilidade da entrada.  

:::row:::
   :::column span="":::
      Um **campo** de senha com pontos ocultando os caracteres inseridos por um usuário.  O **botão revelar** senha aparece à direita do campo **de** senha.
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Alterne o **botão de** revelação de senha para alterar o ícone de olho para um ícone de olho com uma barra através dele e para revelar o texto original da senha.  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="O ícone em forma de olho tem uma barra nele e o texto original da senha é exibido" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         O ícone em forma de olho tem uma barra nele e o texto original da senha é exibido :::image-end:::  
   :::column-end:::
:::row-end:::  

Por padrão, o **botão de revelar** senha insere no SHADOW DOM de todos os elementos HTML com o conjunto como `input` `type` `"password"` .  A partir da versão 87 do Microsoft Edge, os usuários ou empresas [podem][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] desabilitar esse recurso globalmente.  Você, web designers e desenvolvedores devem esperar que a maioria dos usuários do Microsoft Edge tenha a experiência padrão.  

## Remover o controle de revelação de senha  

Você pode remover completamente o **botão de revelar** senha direcionando o pseudo `::-ms-reveal` elemento.  

```css
::-ms-reveal {
    display: none;
}
```  

No entanto, você deve considerar tirar proveito do botão **de revelar senha.**  O botão **de revelar senha** nativa tem medidas de segurança importantes [internas](#visibility-of-the-control) ao comportamento.  

## Personalizar o estilo de controle  

Em vez de remover totalmente o controle, você pode **** modificar o estilo do botão de revelar senha para melhor corresponder à linguagem visual do site.  O trecho a seguir fornece um exemplo desse estilo.  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

Lembre-se do seguinte ao estilcar o botão **de revelar a** senha.  

*   O ícone de olho é implementado como uma imagem de plano de fundo.  Para adicionar uma cor de plano de fundo **ao** botão de revelar senha, use a propriedade CSS em vez da `background-color` propriedade `background` shorthand.  
*   Você pode ajustar o tamanho e a escala do botão revelar **senha.**  
    
    > [!NOTE]
    >O navegador oculta qualquer estouro fora dos limites do controle de entrada de senha.  
    
*   Atualmente, nenhum seletor de estado está disponível para estilgrafar o estado de alternância do botão de revelação **de** senha.  
    
## Visibilidade do controle  

O **botão de revelar** senha não estará disponível até que o usuário insira texto no campo **de** senha.  Para ajudar a manter a entrada de senha do usuário segura, o navegador suprime o botão nos cenários a seguir.

*   Se o foco se mover para fora do campo **de** senha, o navegador removerá o **botão de revelar senha.**  
*   Se os scripts modificarem **o campo de** senha, o navegador removerá o botão revelar **a** senha.  
*   Se um usuário remover o botão revelar senha, ele **** deverá excluir **** o conteúdo do campo de senha antes que o botão de revelar senha seja exibido novamente. ****  
    
    > [!NOTE]
    > Esse recurso impede que alguém faz um ajuste secundário para exibir a senha, caso o usuário saia de um dispositivo desbloqueado.
    
O **botão de revelar** senha não estará disponível se o campo de senha for automaticamente preenchimento usando o gerenciador de senhas. ****  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Políticas | Microsoft Docs"  
