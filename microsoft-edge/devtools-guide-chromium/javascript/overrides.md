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
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a><span data-ttu-id="f9608-105">Substituir recursos de página da Web com cópias locais usando o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f9608-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="f9608-106">Às vezes, você precisa experimentar algumas correções possíveis para uma página da Web, mas você não tem acesso aos arquivos de origem ou alterar a página requer um processo de com build lento e complexo.</span><span class="sxs-lookup"><span data-stu-id="f9608-106">Sometimes you need to try out some possible fixes for a webpage, but you don't have access to the source files, or changing the page requires a slow and complex build process.</span></span>  <span data-ttu-id="f9608-107">Você pode depurar e corrigir todos os tipos de problemas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="f9608-107">You may debug and fix all kind of problems in DevTools.</span></span>  <span data-ttu-id="f9608-108">Mas as alterações não persistem; depois de atualizar o arquivo local, todo o seu trabalho se foi.</span><span class="sxs-lookup"><span data-stu-id="f9608-108">But the changes do not persist; after you refresh the local file, all your work is gone.</span></span>  <span data-ttu-id="f9608-109">O recurso Substituições na ferramenta [Fontes][DevToolsSourcesTool] ajuda você a resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="f9608-109">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="f9608-110">Agora você pode pegar um recurso da página da Web atual e armazená-la localmente.</span><span class="sxs-lookup"><span data-stu-id="f9608-110">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="f9608-111">Quando você atualize a página da Web, o navegador não carrega o recurso do servidor.</span><span class="sxs-lookup"><span data-stu-id="f9608-111">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="f9608-112">Em vez disso, o navegador substitui-o pela cópia local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f9608-112">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <a name="setting-up-your-local-folder-to-store-overrides"></a><span data-ttu-id="f9608-113">Configurando sua pasta local para armazenar Substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-113">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="f9608-114">Navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="f9608-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="f9608-115">No painel **Navegador** (à esquerda), escolha a guia **Substituições.**  Se a **guia Substituições** não for exibida, escolha o</span><span class="sxs-lookup"><span data-stu-id="f9608-115">In the **Navigator** pane (on the left), choose the **Overrides** tab.  If the **Overrides** tab is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="f9608-116">.</span><span class="sxs-lookup"><span data-stu-id="f9608-116">icon.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Ferramenta Sources com espaço não suficiente para mostrar a opção substituições" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="f9608-118">**Ferramenta Sources** com espaço não suficiente para mostrar a opção substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-118">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Escolha a opção substituições" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="f9608-120">Escolha a opção substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-120">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="f9608-121">Escolha uma pasta no computador local para armazenar os arquivos de recursos que você deseja substituir.</span><span class="sxs-lookup"><span data-stu-id="f9608-121">Choose a folder on your local computer to store the resource files that you want to replace.</span></span>  
     *   <span data-ttu-id="f9608-122">Para pesquisar uma pasta, escolha **+ Selecionar pasta para substituições**.</span><span class="sxs-lookup"><span data-stu-id="f9608-122">To search for a folder, choose **+ Select folder for overrides**.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Escolha uma pasta a ser usada para substituições" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="f9608-124">Escolha uma pasta a ser usada para substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-124">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f9608-125">O DevTools avisa que deve ter acesso total à pasta e que você não deve revelar informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="f9608-125">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="f9608-126">Na barra de avisos, escolha **Permitir** para conceder acesso.</span><span class="sxs-lookup"><span data-stu-id="f9608-126">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acesso ao DevTools à pasta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="f9608-128">Conceder acesso ao DevTools à pasta</span><span class="sxs-lookup"><span data-stu-id="f9608-128">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f9608-129">Na guia **Substituições,** uma caixa de seleção é mostrada ao lado de **Habilitar Substituições Locais.**</span><span class="sxs-lookup"><span data-stu-id="f9608-129">In the **Overrides** tab, a checkbox is shown next to **Enable Local Overrides**.</span></span>  <span data-ttu-id="f9608-130">À direita de **Habilitar Substituições** Locais está **um** ícone de configuração Clear que permite excluir as configurações de substituições locais.</span><span class="sxs-lookup"><span data-stu-id="f9608-130">To the right of **Enable Local Overrides** is a **Clear configuration** icon that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="f9608-131">Você terminou de configurar sua pasta e está pronto para substituir os recursos ao vivo por locais.</span><span class="sxs-lookup"><span data-stu-id="f9608-131">You are now done setting up your folder and are ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuração bem-sucedida de uma pasta de substituições" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="f9608-133">Configuração bem-sucedida de uma pasta de substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-133">Successful setup of an overrides folder</span></span>  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a><span data-ttu-id="f9608-134">Adicionar arquivos à pasta Substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-134">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="f9608-135">Para adicionar arquivos à pasta substituições, abra a **ferramenta Elements** e inspecione a página da Web.</span><span class="sxs-lookup"><span data-stu-id="f9608-135">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="f9608-136">Para editar, escolha o nome do arquivo CSS no **Inspetor de Estilos.**</span><span class="sxs-lookup"><span data-stu-id="f9608-136">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Escolha um arquivo no Inspetor de Estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="f9608-138">Escolha um arquivo no **Inspetor de Estilos**</span><span class="sxs-lookup"><span data-stu-id="f9608-138">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="f9608-139">No editor **Fontes,** passe o mouse no nome do arquivo escolhido, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Salvar para substituições**.</span><span class="sxs-lookup"><span data-stu-id="f9608-139">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="No editor Fontes, adicione o nome do arquivo às substituições" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="f9608-141">No editor **Fontes,** adicione o nome do arquivo às substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-141">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="No menu de contexto, escolha Salvar para substituições" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="f9608-143">No menu de contexto, escolha **Salvar para substituições**</span><span class="sxs-lookup"><span data-stu-id="f9608-143">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="f9608-144">O arquivo é armazenado em sua pasta de substituições.</span><span class="sxs-lookup"><span data-stu-id="f9608-144">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="f9608-145">Verifique se o DevTools cria uma pasta nomeada usando a URL do arquivo com a estrutura de diretório correta.</span><span class="sxs-lookup"><span data-stu-id="f9608-145">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="f9608-146">O arquivo é armazenado dentro.</span><span class="sxs-lookup"><span data-stu-id="f9608-146">The file is stored inside.</span></span>  <span data-ttu-id="f9608-147">O nome do arquivo no editor agora também mostra um ponto roxo que indica que o arquivo é local e não um ao vivo.</span><span class="sxs-lookup"><span data-stu-id="f9608-147">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Armazenou com êxito o arquivo em sua pasta de substituições" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="f9608-149">Armazenou com êxito o arquivo em sua pasta de substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-149">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="f9608-150">No exemplo a seguir, agora você pode alterar os estilos da página da Web.</span><span class="sxs-lookup"><span data-stu-id="f9608-150">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="f9608-151">Para adicionar uma borda vermelha ao redor do arquivo, no editor **estilos,** copie o estilo a seguir e adicione-o ao elemento body.</span><span class="sxs-lookup"><span data-stu-id="f9608-151">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f9608-152">O arquivo é salvo automaticamente no computador.</span><span class="sxs-lookup"><span data-stu-id="f9608-152">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="f9608-153">Se você atualizar o arquivo, a borda será exibida e nenhum de seu trabalho será perdido.</span><span class="sxs-lookup"><span data-stu-id="f9608-153">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Alterar estilos de página da Web persistentemente editando um arquivo em sua pasta substitui" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="f9608-155">Alterar estilos de página da Web persistentemente editando um arquivo em sua pasta substitui</span><span class="sxs-lookup"><span data-stu-id="f9608-155">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="f9608-156">Na ferramenta **Fontes,** na seção **Página,** passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e adicione-o às substituições.</span><span class="sxs-lookup"><span data-stu-id="f9608-156">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="f9608-157">Novamente, os arquivos que já estão na pasta substituições têm um ponto roxo no ícone.</span><span class="sxs-lookup"><span data-stu-id="f9608-157">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Escolha um arquivo na ferramenta Fontes para substituições" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="f9608-159">Escolha um arquivo na ferramenta **Fontes** para substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-159">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f9608-160">Como alternativa, na ferramenta **Rede,** passe o mouse em qualquer arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e adicione-o a substituições.</span><span class="sxs-lookup"><span data-stu-id="f9608-160">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="f9608-161">Quando as substituições estão em vigor, os arquivos que estão localizados no computador e não na página da Web ao vivo.</span><span class="sxs-lookup"><span data-stu-id="f9608-161">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="f9608-162">Quando as substituições estão em vigor, na ferramenta **Rede,** localize um ícone de aviso ao lado do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f9608-162">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Escolha um arquivo na ferramenta Rede para substituições" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="f9608-164">Escolha um arquivo na ferramenta **Rede** para substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-164">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a><span data-ttu-id="f9608-165">Interação de duas vias de substituições</span><span class="sxs-lookup"><span data-stu-id="f9608-165">Two-way interaction of overrides</span></span>  

<span data-ttu-id="f9608-166">Use o editor fornecido com a **ferramenta Sources** do DevTools ou qualquer editor que você deseja alterar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="f9608-166">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="f9608-167">As alterações são sincronizadas em todos os produtos que acessam os arquivos na pasta substituições.</span><span class="sxs-lookup"><span data-stu-id="f9608-167">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f9608-168">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f9608-168">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
