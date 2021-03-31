---
description: O recurso substituições é um recurso dentro da ferramenta fontes do Microsoft Edge DevTools que permite copiar recursos de página da Web para seu disco rígido.  Quando você atualiza a página da Web, o DevTools não carrega o recurso, mas o substitui pela cópia local em vez disso.
title: Substituir recursos de páginas da Web por cópias locais usando o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230961"
---
# Substituir recursos de páginas da Web por cópias locais usando o Microsoft Edge DevTools  

Às vezes, você precisa corrigir um problema em uma página da Web à qual você não tem acesso ou correções envolve um processo de compilação lento e complexo.  Você pode depurar e corrigir todos os tipos de problemas do DevTools. Mas o problema é que as alterações não persistem.  Após atualizar o arquivo, todo o seu trabalho não existe mais.  

O recurso substituições na ferramenta [fontes][DevToolsSourcesTool] ajuda você a resolver esse problema.  

Agora você pode pegar um recurso da página da Web atual e armazená-lo localmente.  Quando você atualiza a página da Web, o navegador não carrega o recurso do servidor.  Em vez disso, o navegador substitui-o pela sua cópia local do recurso.  

## Configurando sua pasta local para armazenar substituições  

1.  Na ferramenta **fontes** , encontre várias seções no lado esquerdo.  Se a opção **substituições** não for exibida, escolha o botão <code>&#x0226B;</code><!--`≫`--> ícone para chegar lá.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Ferramenta fontes com espaço insuficiente para mostrar a opção substituições" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             Ferramenta **fontes** com espaço insuficiente para mostrar a opção substituições  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Escolher a opção substituições" lightbox="../media/javascript-overrides-menu.msft.png":::
             Escolher a opção substituições  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Depois de escolher a opção **substituições** , você deve escolher uma pasta no seu computador local para armazenar os arquivos de recursos que deseja substituir.  Escolha a **pasta + selecionar para substituições** para pesquisar uma pasta.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Escolher uma pasta para usar para substituições" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Escolher uma pasta para usar para substituições  
    :::image-end:::  
    
1.  O DevTools avisa que deve ter acesso total à pasta e que você não deve revelar informações confidenciais.  Na barra de aviso, escolha **permitir** para conceder acesso.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acesso DevTools à pasta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Conceder acesso DevTools à pasta  
    :::image-end:::  
    
1.  No painel **substituições** , uma caixa de seleção deve ser exibida ao lado de `Enable Local Overrides` e sua pasta substitui.  Um ícone é exibido ao lado dele que permite excluir suas configurações locais de substituição.  Agora, você concluiu a configuração de sua pasta e está pronto para substituir recursos ao vivo por locais.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Êxito na configuração de uma pasta de substituições" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Êxito na configuração de uma pasta de substituições  
    :::image-end:::  
    
## Adicionando arquivos à sua pasta substituições  
  
Para adicionar arquivos à sua pasta substituis, abra a ferramenta **elementos** e inspecione a página da Web.  Para editar, escolha o nome do arquivo CSS no Inspetor de **estilos** .  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Escolher um arquivo no Inspetor de estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Escolher um arquivo no Inspetor de **estilos**  
:::image-end:::  

No editor de **códigos-fonte** , passe o mouse no nome do arquivo escolhido, abra o menu contextual \(clique com o botão direito do mouse \) e escolha **salvar para substituições**.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="No editor de códigos-fonte, adicione o nome do arquivo para substituir" lightbox="../media/javascript-overrides-file-name.msft.png":::
   No editor de **códigos-fonte** , adicione o nome do arquivo para substituir  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="No menu de contexto, escolha salvar para substituições" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   No menu de contexto, escolha **salvar para substituições**  
:::image-end:::  

O arquivo é armazenado na sua pasta substituis.  Verifique se DevTools criar uma pasta chamada usando a URL do arquivo com a estrutura de diretório correta.  O arquivo está armazenado dentro.  O nome do arquivo no Editor agora também mostra um ponto roxo que indica que o arquivo é local e não um ao vivo.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="O arquivo foi armazenado com êxito na pasta substituições" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   O arquivo foi armazenado com êxito na pasta substituições  
:::image-end:::  

:::row:::
   :::column span="":::
      No exemplo a seguir, agora você pode alterar os estilos da página da Web.  Para adicionar uma borda vermelha ao seu lado do arquivo, no editor de **estilos** , copie o seguinte estilo e adicione-o ao elemento body.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      O arquivo é salvo automaticamente no seu computador.  Se você atualizar o arquivo, a borda será exibida e nenhum trabalho será perdido.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Alterar estilos de página da Web de maneira persistente editando um arquivo na sua pasta substituis" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Alterar estilos de página da Web de maneira persistente editando um arquivo na sua pasta substituis  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      Na ferramenta **fontes** , na seção **página** , passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse \) e adicione-o a substituições.  Novamente, os arquivos que já estão na sua pasta substitui têm um ponto roxo no ícone.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Escolher um arquivo da ferramenta fontes para substituições" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Escolher um arquivo da ferramenta **fontes** para substituições  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Ou, se preferir, na ferramenta **rede** , passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse \) e adicione-o a substituições.  Quando as substituições estão em vigor, arquivos que estão em seu computador e não na página da Web ao vivo são armazenados.  Quando as substituições estiverem em vigor, na ferramenta **rede** , localize um ícone de aviso ao lado do nome do arquivo.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Escolha um arquivo da ferramenta de rede para substituições" lightbox="../media/javascript-overrides-network.msft.png":::
         Escolha um arquivo da ferramenta de **rede** para substituições  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Interação bidirecional de substituições  

Use o editor fornecido com a ferramenta **fontes** do devtools ou qualquer editor para o qual você deseja alterar os arquivos.  As alterações são sincronizadas em todos os produtos que acessam os arquivos na pasta substituições.  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta fontes | Documentos da Microsoft"  
