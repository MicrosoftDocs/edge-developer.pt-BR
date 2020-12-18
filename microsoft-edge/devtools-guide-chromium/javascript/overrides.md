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
# <span data-ttu-id="c3f5d-105">Substituir recursos de páginas da Web por cópias locais usando o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c3f5d-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c3f5d-106">Às vezes, você precisa corrigir um problema em uma página da Web à qual você não tem acesso ou correções envolve um processo de compilação lento e complexo.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="c3f5d-107">Você pode depurar e corrigir todos os tipos de problemas do DevTools.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="c3f5d-108">Mas o problema é que as alterações não persistem.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="c3f5d-109">Após atualizar o arquivo, todo o seu trabalho não existe mais.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="c3f5d-110">O recurso substituições na ferramenta [fontes][DevToolsSourcesTool] ajuda você a resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="c3f5d-111">Agora você pode pegar um recurso da página da Web atual e armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="c3f5d-112">Quando você atualiza a página da Web, o navegador não carrega o recurso do servidor.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="c3f5d-113">Em vez disso, o navegador substitui-o pela sua cópia local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <span data-ttu-id="c3f5d-114">Configurando sua pasta local para armazenar substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="c3f5d-115">Na ferramenta **fontes** , encontre várias seções no lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="c3f5d-116">Se a opção **substituições** não for exibida, escolha o botão</span><span class="sxs-lookup"><span data-stu-id="c3f5d-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="c3f5d-117">ícone para chegar lá.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Ferramenta fontes com espaço insuficiente para mostrar a opção substituições" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="c3f5d-119">Ferramenta **fontes** com espaço insuficiente para mostrar a opção substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Escolher a opção substituições" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="c3f5d-121">Escolher a opção substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="c3f5d-122">Depois de escolher a opção **substituições** , você deve escolher uma pasta no seu computador local para armazenar os arquivos de recursos que deseja substituir.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="c3f5d-123">Escolha a **pasta + selecionar para substituições** para pesquisar uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Escolher uma pasta para usar para substituições" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="c3f5d-125">Escolher uma pasta para usar para substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3f5d-126">O DevTools avisa que deve ter acesso total à pasta e que você não deve revelar informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="c3f5d-127">Na barra de aviso, escolha **permitir** para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acesso DevTools à pasta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="c3f5d-129">Conceder acesso DevTools à pasta</span><span class="sxs-lookup"><span data-stu-id="c3f5d-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3f5d-130">No painel **substituições** , uma caixa de seleção deve ser exibida ao lado de `Enable Local Overrides` e sua pasta substitui.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="c3f5d-131">Um ícone é exibido ao lado dele que permite excluir suas configurações locais de substituição.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="c3f5d-132">Agora, você concluiu a configuração de sua pasta e está pronto para substituir recursos ao vivo por locais.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Êxito na configuração de uma pasta de substituições" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="c3f5d-134">Êxito na configuração de uma pasta de substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c3f5d-135">Adicionando arquivos à sua pasta substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="c3f5d-136">Para adicionar arquivos à sua pasta substituis, abra a ferramenta **elementos** e inspecione a página da Web.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="c3f5d-137">Para editar, escolha o nome do arquivo CSS no Inspetor de **estilos** .</span><span class="sxs-lookup"><span data-stu-id="c3f5d-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Escolher um arquivo no Inspetor de estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="c3f5d-139">Escolher um arquivo no Inspetor de **estilos**</span><span class="sxs-lookup"><span data-stu-id="c3f5d-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="c3f5d-140">No editor de **códigos-fonte** , passe o mouse no nome do arquivo escolhido, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **salvar para substituições**.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="No editor de códigos-fonte, adicione o nome do arquivo para substituir" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="c3f5d-142">No editor de **códigos-fonte** , adicione o nome do arquivo para substituir</span><span class="sxs-lookup"><span data-stu-id="c3f5d-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="No menu de contexto, escolha salvar para substituições" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="c3f5d-144">No menu de contexto, escolha **salvar para substituições**</span><span class="sxs-lookup"><span data-stu-id="c3f5d-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="c3f5d-145">O arquivo é armazenado na sua pasta substituis.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="c3f5d-146">Verifique se DevTools criar uma pasta chamada usando a URL do arquivo com a estrutura de diretório correta.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="c3f5d-147">O arquivo está armazenado dentro.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-147">The file is stored inside.</span></span>  <span data-ttu-id="c3f5d-148">O nome do arquivo no Editor agora também mostra um ponto roxo que indica que o arquivo é local e não um ao vivo.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="O arquivo foi armazenado com êxito na pasta substituições" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="c3f5d-150">O arquivo foi armazenado com êxito na pasta substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="c3f5d-151">No exemplo a seguir, agora você pode alterar os estilos da página da Web.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="c3f5d-152">Para adicionar uma borda vermelha ao seu lado do arquivo, no editor de **estilos** , copie o seguinte estilo e adicione-o ao elemento body.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c3f5d-153">O arquivo é salvo automaticamente no seu computador.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="c3f5d-154">Se você atualizar o arquivo, a borda será exibida e nenhum trabalho será perdido.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Alterar estilos de página da Web de maneira persistente editando um arquivo na sua pasta substituis" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="c3f5d-156">Alterar estilos de página da Web de maneira persistente editando um arquivo na sua pasta substituis</span><span class="sxs-lookup"><span data-stu-id="c3f5d-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="c3f5d-157">Na ferramenta **fontes** , na seção **página** , passe o mouse em qualquer arquivo, abra o menu contextual \ (clique com o botão direito do mouse \) e adicione-o a substituições.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="c3f5d-158">Novamente, os arquivos que já estão na sua pasta substitui têm um ponto roxo no ícone.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Escolher um arquivo da ferramenta fontes para substituições" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="c3f5d-160">Escolher um arquivo da ferramenta **fontes** para substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c3f5d-161">Ou, se preferir, na ferramenta **rede** , passe o mouse em qualquer arquivo, abra o menu contextual \ (clique com o botão direito do mouse \) e adicione-o a substituições.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="c3f5d-162">Quando as substituições estão em vigor, arquivos que estão em seu computador e não na página da Web ao vivo são armazenados.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="c3f5d-163">Quando as substituições estiverem em vigor, na ferramenta **rede** , localize um ícone de aviso ao lado do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Escolha um arquivo da ferramenta de rede para substituições" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="c3f5d-165">Escolha um arquivo da ferramenta de **rede** para substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="c3f5d-166">Interação bidirecional de substituições</span><span class="sxs-lookup"><span data-stu-id="c3f5d-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="c3f5d-167">Use o editor fornecido com a ferramenta **fontes** do devtools ou qualquer editor para o qual você deseja alterar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="c3f5d-168">As alterações são sincronizadas em todos os produtos que acessam os arquivos na pasta substituições.</span><span class="sxs-lookup"><span data-stu-id="c3f5d-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <span data-ttu-id="c3f5d-169">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c3f5d-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta fontes | Documentos da Microsoft"  
