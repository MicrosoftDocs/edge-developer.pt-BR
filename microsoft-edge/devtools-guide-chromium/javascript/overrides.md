---
description: O recurso Substituições é um recurso dentro da ferramenta Sources do Microsoft Edge DevTools que permite copiar recursos de página da Web para seu disco rígido.  Quando você atualize a página da Web, o DevTools não carrega o recurso, mas o substitui pela cópia local.
title: Substituir recursos de página da Web com cópias locais usando o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: 2ddfd98d1e871be9c61380a8ca57da398d38bd54
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11230961"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a><span data-ttu-id="2a7a1-105">Substituir recursos de página da Web com cópias locais usando o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2a7a1-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="2a7a1-106">Às vezes, você precisa corrigir um problema em uma página da Web que você não tem acesso ou correções envolvem um processo de com build lento e complexo.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="2a7a1-107">Você pode depurar e corrigir todos os tipos de problemas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="2a7a1-108">Mas o problema é que as alterações não persistem.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="2a7a1-109">Depois de atualizar o arquivo, todo o seu trabalho se foi.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="2a7a1-110">O recurso Substituições na ferramenta [Fontes][DevToolsSourcesTool] ajuda você a resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="2a7a1-111">Agora você pode pegar um recurso da página da Web atual e armazená-la localmente.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="2a7a1-112">Quando você atualize a página da Web, o navegador não carrega o recurso do servidor.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="2a7a1-113">Em vez disso, o navegador substitui-o pela cópia local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <a name="setting-up-your-local-folder-to-store-overrides"></a><span data-ttu-id="2a7a1-114">Configurando sua pasta local para armazenar Substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="2a7a1-115">Na ferramenta **Fontes,** encontre várias seções no lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="2a7a1-116">Se a **opção Substituições** não for exibida, escolha o</span><span class="sxs-lookup"><span data-stu-id="2a7a1-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="2a7a1-117">ícone para chegar lá.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Ferramenta Sources com espaço não suficiente para mostrar a opção substituições" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="2a7a1-119">**Ferramenta Sources** com espaço não suficiente para mostrar a opção substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Escolha a opção substituições" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="2a7a1-121">Escolha a opção substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="2a7a1-122">Depois de escolher a **opção Substituições,** você deve escolher uma pasta em seu computador local para armazenar os arquivos de recursos que deseja substituir.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="2a7a1-123">Escolha **a pasta + Selecionar para substituições** para pesquisar uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Escolha uma pasta a ser usada para substituições" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="2a7a1-125">Escolha uma pasta a ser usada para substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2a7a1-126">O DevTools avisa que deve ter acesso total à pasta e que você não deve revelar informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="2a7a1-127">Na barra de avisos, escolha **Permitir** para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acesso ao DevTools à pasta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="2a7a1-129">Conceder acesso ao DevTools à pasta</span><span class="sxs-lookup"><span data-stu-id="2a7a1-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2a7a1-130">No painel **Substituições,** uma caixa de seleção deve ser exibida ao lado e `Enable Local Overrides` sua pasta substitui.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="2a7a1-131">Um ícone é exibido ao lado dele que permite excluir as configurações de substituições locais.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="2a7a1-132">Você terminou de configurar sua pasta e pronto para substituir os recursos ao vivo por locais.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuração bem-sucedida de uma pasta de substituições" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="2a7a1-134">Configuração bem-sucedida de uma pasta de substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a><span data-ttu-id="2a7a1-135">Adicionar arquivos à pasta Substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="2a7a1-136">Para adicionar arquivos à pasta substituições, abra a **ferramenta Elements** e inspecione a página da Web.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="2a7a1-137">Para editar, escolha o nome do arquivo CSS no **Inspetor de Estilos.**</span><span class="sxs-lookup"><span data-stu-id="2a7a1-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Escolha um arquivo no Inspetor de Estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="2a7a1-139">Escolha um arquivo no **Inspetor de Estilos**</span><span class="sxs-lookup"><span data-stu-id="2a7a1-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="2a7a1-140">No editor **Fontes,** passe o mouse no nome do arquivo escolhido, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar para substituições**.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="No editor Fontes, adicione o nome do arquivo às substituições" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="2a7a1-142">No editor **Fontes,** adicione o nome do arquivo às substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="No menu de contexto, escolha Salvar para substituições" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="2a7a1-144">No menu de contexto, escolha **Salvar para substituições**</span><span class="sxs-lookup"><span data-stu-id="2a7a1-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="2a7a1-145">O arquivo é armazenado em sua pasta de substituições.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="2a7a1-146">Verifique se o DevTools cria uma pasta nomeada usando a URL do arquivo com a estrutura de diretório correta.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="2a7a1-147">O arquivo é armazenado dentro.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-147">The file is stored inside.</span></span>  <span data-ttu-id="2a7a1-148">O nome do arquivo no editor agora também mostra um ponto roxo que indica que o arquivo é local e não um ao vivo.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Armazenou com êxito o arquivo em sua pasta de substituições" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="2a7a1-150">Armazenou com êxito o arquivo em sua pasta de substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="2a7a1-151">No exemplo a seguir, agora você pode alterar os estilos da página da Web.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="2a7a1-152">Para adicionar uma borda vermelha ao redor do arquivo, no editor **estilos,** copie o estilo a seguir e adicione-o ao elemento body.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2a7a1-153">O arquivo é salvo automaticamente no computador.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="2a7a1-154">Se você atualizar o arquivo, a borda será exibida e nenhum de seu trabalho será perdido.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Alterar estilos de página da Web persistentemente editando um arquivo em sua pasta substitui" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="2a7a1-156">Alterar estilos de página da Web persistentemente editando um arquivo em sua pasta substitui</span><span class="sxs-lookup"><span data-stu-id="2a7a1-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="2a7a1-157">Na ferramenta **Fontes,** na seção **Página,** passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e adicione-o às substituições.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="2a7a1-158">Novamente, os arquivos que já estão na pasta substituições têm um ponto roxo no ícone.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Escolha um arquivo na ferramenta Fontes para substituições" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="2a7a1-160">Escolha um arquivo na ferramenta **Fontes** para substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2a7a1-161">Como alternativa, na ferramenta **Rede,** passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e adicione-o a substituições.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="2a7a1-162">Quando as substituições estão em vigor, os arquivos que estão localizados no computador e não na página da Web ao vivo.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="2a7a1-163">Quando as substituições estão em vigor, na ferramenta **Rede,** localize um ícone de aviso ao lado do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Escolha um arquivo na ferramenta Rede para substituições" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="2a7a1-165">Escolha um arquivo na ferramenta **Rede** para substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a><span data-ttu-id="2a7a1-166">Interação de duas vias de substituições</span><span class="sxs-lookup"><span data-stu-id="2a7a1-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="2a7a1-167">Use o editor fornecido com a **ferramenta Sources** do DevTools ou qualquer editor que você deseja alterar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="2a7a1-168">As alterações são sincronizadas em todos os produtos que acessam os arquivos na pasta substituições.</span><span class="sxs-lookup"><span data-stu-id="2a7a1-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2a7a1-169">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2a7a1-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
