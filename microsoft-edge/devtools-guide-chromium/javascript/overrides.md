---
description: O recurso Substituições é um recurso dentro da ferramenta Sources do Microsoft Edge DevTools que permite copiar recursos de página da Web para seu disco rígido.  Quando você atualize a página da Web, o DevTools não carrega o recurso, mas o substitui pela cópia local.
title: Substituir recursos de página da Web com cópias locais usando o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 66c0686c166163f1640384d096288af0b530f135
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519433"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a>Substituir recursos de página da Web com cópias locais usando o Microsoft Edge DevTools  

Às vezes, você precisa experimentar algumas correções possíveis para uma página da Web, mas você não tem acesso aos arquivos de origem ou alterar a página requer um processo de com build lento e complexo.  Você pode depurar e corrigir todos os tipos de problemas no DevTools.  Mas as alterações não persistem; depois de atualizar o arquivo local, todo o seu trabalho se foi.  O recurso Substituições na ferramenta [Fontes][DevToolsSourcesTool] ajuda você a resolver esse problema.  

Agora você pode pegar um recurso da página da Web atual e armazená-la localmente.  Quando você atualize a página da Web, o navegador não carrega o recurso do servidor.  Em vez disso, o navegador substitui-o pela cópia local do recurso.  

## <a name="setting-up-your-local-folder-to-store-overrides"></a>Configurando sua pasta local para armazenar Substituições  

1.  Navegue até a **ferramenta Sources.**  
1.  No painel **Navegador** (à esquerda), escolha a guia **Substituições.**  Se a **guia Substituições** não for exibida, escolha o <code>&#x0226B;</code><!--`≫`--> .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Ferramenta Sources com espaço não suficiente para mostrar a opção substituições" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             **Ferramenta Sources** com espaço não suficiente para mostrar a opção substituições  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Escolha a opção substituições" lightbox="../media/javascript-overrides-menu.msft.png":::
             Escolha a opção substituições  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Escolha uma pasta no computador local para armazenar os arquivos de recursos que você deseja substituir.  
     *   Para pesquisar uma pasta, escolha **+ Selecionar pasta para substituições**.  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Escolha uma pasta a ser usada para substituições" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       Escolha uma pasta a ser usada para substituições  
    :::image-end:::  
    
1.  O DevTools avisa que deve ter acesso total à pasta e que você não deve revelar informações confidenciais.  Na barra de avisos, escolha **Permitir** para conceder acesso.  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acesso ao DevTools à pasta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       Conceder acesso ao DevTools à pasta  
    :::image-end:::  
    
1.  Na guia **Substituições,** uma caixa de seleção é mostrada ao lado de **Habilitar Substituições Locais.**  À direita de **Habilitar Substituições** Locais está **um** ícone de configuração Clear que permite excluir as configurações de substituições locais.  Você terminou de configurar sua pasta e está pronto para substituir os recursos ao vivo por locais.
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuração bem-sucedida de uma pasta de substituições" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       Configuração bem-sucedida de uma pasta de substituições  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a>Adicionar arquivos à pasta Substituições  
  
Para adicionar arquivos à pasta substituições, abra a **ferramenta Elements** e inspecione a página da Web.  Para editar, escolha o nome do arquivo CSS no **Inspetor de Estilos.**  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Escolha um arquivo no Inspetor de Estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   Escolha um arquivo no **Inspetor de Estilos**  
:::image-end:::  

No editor **Fontes,** passe o mouse no nome do arquivo escolhido, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar para substituições**.  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="No editor Fontes, adicione o nome do arquivo às substituições" lightbox="../media/javascript-overrides-file-name.msft.png":::
   No editor **Fontes,** adicione o nome do arquivo às substituições  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="No menu de contexto, escolha Salvar para substituições" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   No menu de contexto, escolha **Salvar para substituições**  
:::image-end:::  

O arquivo é armazenado em sua pasta de substituições.  Verifique se o DevTools cria uma pasta nomeada usando a URL do arquivo com a estrutura de diretório correta.  O arquivo é armazenado dentro.  O nome do arquivo no editor agora também mostra um ponto roxo que indica que o arquivo é local e não um ao vivo.  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Armazenou com êxito o arquivo em sua pasta de substituições" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   Armazenou com êxito o arquivo em sua pasta de substituições  
:::image-end:::  

:::row:::
   :::column span="":::
      No exemplo a seguir, agora você pode alterar os estilos da página da Web.  Para adicionar uma borda vermelha ao redor do arquivo, no editor **estilos,** copie o estilo a seguir e adicione-o ao elemento body.  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      O arquivo é salvo automaticamente no computador.  Se você atualizar o arquivo, a borda será exibida e nenhum de seu trabalho será perdido.  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Alterar estilos de página da Web persistentemente editando um arquivo em sua pasta substitui" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         Alterar estilos de página da Web persistentemente editando um arquivo em sua pasta substitui  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      Na ferramenta **Fontes,** na seção **Página,** passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e adicione-o às substituições.  Novamente, os arquivos que já estão na pasta substituições têm um ponto roxo no ícone.  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Escolha um arquivo na ferramenta Fontes para substituições" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         Escolha um arquivo na ferramenta **Fontes** para substituições  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Como alternativa, na ferramenta **Rede,** passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e adicione-o a substituições.  Quando as substituições estão em vigor, os arquivos que estão localizados no computador e não na página da Web ao vivo.  Quando as substituições estão em vigor, na ferramenta **Rede,** localize um ícone de aviso ao lado do nome do arquivo.  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Escolha um arquivo na ferramenta Rede para substituições" lightbox="../media/javascript-overrides-network.msft.png":::
         Escolha um arquivo na ferramenta **Rede** para substituições  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a>Interação de duas vias de substituições  

Use o editor fornecido com a **ferramenta Sources** do DevTools ou qualquer editor que você deseja alterar os arquivos.  As alterações são sincronizadas em todos os produtos que acessam os arquivos na pasta substituições.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
