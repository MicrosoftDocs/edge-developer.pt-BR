---
description: A ferramenta Novidades agora é Bem-vindo, Editor de Fonte Visual no painel Estilos, ferramentas de depuração do CSS Flexbox e muito mais.
title: Novidades no DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: cfaee927d2d914cf0d816505ea2cf6b36a225d64
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313092"
---
# Novidades no DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## O que há de novo agora é bem-vindo  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

A **ferramenta Novidades no** Microsoft Edge DevTools agora tem uma nova aparência e um novo nome: **Bem-vindo.**  A **ferramenta de** boas-vindas ainda exibe as últimas notícias e atualizações do DevTools.  Agora também inclui links para a documentação do Microsoft Edge DevTools, maneiras de enviar comentários e muito mais.  Para exibir a **ferramenta de** boas-vindas após cada atualização do Microsoft Edge, escolha a caixa de seleção ao lado da guia Abrir após **cada atualização** no título.  Para fechar a **ferramenta de** boas-vindas, escolha **o X** no lado direito do título da guia.  Se você preferir a ferramenta **Novidades** original, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e remova a caixa de seleção ao lado da guia  >  **** **Habilitar Boas-vindas.**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="A ferramenta de boas-vindas está realçada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   A **ferramenta de** boas-vindas está realçada  
:::image-end:::  

## Editor de Fonte Visual no painel Estilos  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

When you work with fonts in CSS, use the new visual [Font Editor][DevtoolsInspectStylesEditFonts].  Você pode definir fontes de fallback e usar controles deslizantes para definir o peso, o tamanho, a altura da linha e o espaçamento da fonte.  O **Editor de Fontes** ajuda você a concluir as seguintes ações.  

*   Alternar entre unidades para propriedades de fonte diferentes  
*   Alternar entre palavras-chave para propriedades de fonte diferentes  
*   Converter unidades  
*   Gerar código CSS preciso  
    
Para ativar esse experimento, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e escolha a caixa de seleção ao lado de Habilitar novas ferramentas do Editor de Fontes no  >  **** **painel Estilos.**  Para obter mais informações, navegue até Editar estilos de fonte CSS e configurações no painel [Estilos no DevTools][DevtoolsInspectStylesEditFonts].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="O editor de fonte visual é realçado no painel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   O **editor de fonte visual** está realçado no **painel** Estilos  
:::image-end:::  

## Ferramentas de depuração do CSS Flexbox  

Os recursos de depuração do Flexbox estão em desenvolvimento ativo.  Para ativar o experimento para os dois recursos a seguir, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e escolha a caixa de seleção ao lado de Habilitar novos recursos  >  **** de depuração do **CSS Flexbox.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1136394][CR1136394] e [1139949][CR1139949].  

### O ícone novo flexbox (flexível) ajuda a identificar e exibir contêineres flexíveis  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Na ferramenta **Elementos,** o novo ícone Flexbox (flex) ajuda você a identificar contêineres do Flexbox em seu código.  Escolha o ícone Flexbox \(flex\) para ativar ou desativar o efeito de sobreposição que descreve um contêiner flexbox.  Você pode personalizar a cor da sobreposição no painel **Layout,** que está localizado ao lado de **Estilos** e **Calculados.**  

:::row:::
   :::column span="":::
      Para ativar e desativar o efeito de sobreposição que descreve o contêiner Flexbox, escolha o ícone Flexbox \( `flex` \).  
   :::column-end:::
   :::column span="":::
      Você pode personalizar a cor da sobreposição no painel **Layout** ao lado de **Estilos** e **Calculados.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="O ícone e a página da Web flexbox (flexível) realçadas" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         O ícone e a página da Web **do Flexbox** \( `flex` \) realçadas :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="As sobreposições do Flexbox realçadas no painel Layout" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         As **sobreposições do Flexbox** realçadas no **painel Layout**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Exibir ícones de alinhamento e linhas de grade quando layouts do Flexbox mudam usando propriedades CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Quando você edita CSS para o layout do **** Flexbox, os preenchimentos automáticos de CSS no painel Estilos agora exibem ícones úteis ao lado das propriedades relevantes do Flexbox.  Para experimentar esse novo recurso, abra a ferramenta **Elementos** e selecione um contêiner flexível.  Em seguida, adicione ou altere uma propriedade nesse contêiner no **painel** Estilos.  

:::row:::
   :::column span="":::
      O menu de preenchimento automático agora exibe ícones que indicam o efeito das propriedades de alinhamento, como `align-content` e `align-items` .  
   :::column-end:::
   :::column span="":::
      Além disso, o DevTools agora exibe uma linha de orientação para ajudá-lo a analisar melhor a `align-items` propriedade CSS.  A `gap` propriedade CSS também é compatível.  Na figura a seguir, a `gap` propriedade CSS é definida como e o padrão de `gap: 12px;` desassocie para cada lacuna é exibido.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de preenchimento automático realçada para propriedades CSS que começam com alinhar-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menu de preenchimento automático realçada para propriedades CSS que começam com `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Espaço flexível em propriedades CSS e página da Web realçada" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` in CSS properties and webpage highlighted  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Adicionar ferramentas rapidamente com o novo botão Mais Ferramentas  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Agora você tem uma nova maneira de abrir mais ferramentas no Microsoft Edge DevTools.  Depois que você ativar esse experimento, o ícone **Mais** Ferramentas será exibido como um sinal de a mais ( `+` ) à direita do painel principal.  Para exibir uma lista de outras ferramentas para adicionar ao painel principal, escolha o ícone Mais **Ferramentas** \( `+` \).  Para ativar esse experimento, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e, em seguida, escolha a caixa de seleção ao lado dos menus da guia Habilitar + botão para  >  **** abrir **mais ferramentas.**  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Mais ferramentas realçadas no DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Mais ferramentas** realçadas no DevTools  
:::image-end:::  

## Tecnologias adaptativas agora anunciam a posição e a contagem de sugestões css  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Ao editar CSS, você pode obter um menu suspenso de recursos.  Esse recurso não estava disponível para os usuários de tecnologias adaptativas, pois foi anunciado no Microsoft Edge versão 89.  Um usuário de tecnologias adaptativas agora pode navegar por sugestões CSS no **painel** Estilos.  No Microsoft Edge versão 88 e versões anteriores, a tecnologia adaptativa anunciada como um usuário navegava pela lista de sugestões ao editar CSS no `Suggestion` painel Estilos. ****  No Microsoft Edge versão 89, um usuário de tecnologia adaptativa agora ouve a posição e a contagem da sugestão atual.  Cada sugestão é anunciada conforme o usuário navega pela lista de sugestões, como Sugestão 3 de 5.  Para saber mais sobre como escrever CSS no DevTools, navegue até [Alterar CSS][DevtoolsCssReferenceChangeCss].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1157329][CR1157329].  

<!--To view a video that displays and reads aloud several suggestions with this experiment turned on, navigate to [Voiceover announcing devtools options](https://youtu.be/9TcUpleEwwA) on YouTube.  -->  

O link de vídeo a seguir exibe e lê em voz alta várias sugestões com esse experimento ligado.  

> [!VIDEO https://youtu.be/9TcUpleEwwA]  

## Emular Surface Duo e Samsung Top  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Teste a aparência do seu site ou aplicativo nos seguintes dispositivos no Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Ative os recursos da Plataforma **Web Experimental** para acessar o novo recurso de tela de mídia [CSS][DualScreenWebCssMediaSpanning] e obter a API [JavaScript doWindowSegments.][DualScreenWebJavascriptGetwindowsegments]  Navegue `edge://flags` até e alterne o sinalizador ao lado dos **recursos da Plataforma Web Experimental.**  Para ajudar a aprimorar seu site ou aplicativo para os dispositivos de tela dupla e dobrável, use os seguintes recursos ao [emular o dispositivo.][DevtoolsDeviceModeIndex]  

*   [Abrangendo][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], que é quando seu site \(ou aplicativo\) aparece nas duas telas.  
*   [Renderização da seam][DualScreenIntroductionHowToWorkWithSeam], que é o espaço entre as duas telas.  
    
Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular tela dupla" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emular tela dupla  
:::image-end:::  

## Microsoft Edge Developer Tools para Visual Studio Code versão 1.1.2  

As Ferramentas de Desenvolvedor do Microsoft Edge para [Visual Studio Code versão][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] 1.1.2 do Microsoft Visual Studio Code têm as seguintes alterações desde a versão anterior.  O Microsoft Visual Studio Code atualiza as extensões automaticamente.  Para atualizar manualmente para a versão 1.1.2, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Adicionado um **botão Fechar instância** a cada item na lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Versão do [Microsoft Edge DevTools][DevtoolsMain] de 84.0.522.63 para [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   [Depurador incluído para o Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como uma dependência \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Opção de configurações implementadas para alterar os temas de extensão \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Você pode registrar problemas e contribuir com a extensão no [repositório do GitHub vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

## Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Captura de tela do nó de captura além do viewport  

No Microsoft Edge versão 89, as capturas de tela do nó são mais precisas, capturando o nó completo, mesmo se o conteúdo do nó não estiver visível no viewport.  Na ferramenta **Elementos,** passe o mouse sobre um elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Captura de tela **do nó captura de tela.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de tela do nó de captura realçada no menu de contexto na ferramenta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Captura de tela do nó de** captura realçada no menu de contexto na ferramenta **Elementos**  
:::image-end:::  

### Atualizações da ferramenta Elementos  

#### Suporte forçando o estado de CSS :target  

Agora você pode usar o DevTools para forçar a pseudo-classe CSS [:target.][MdnDocsWebCssTarget]  A pseudo-classe é disparada quando um elemento exclusivo \(o elemento de destino\) tem um que corresponde a um `:target` `id` fragmento da URL.  Por exemplo, a `http://www.example.com/index.html#section1` URL dispara a `:target` pseudo-classe em um elemento HTML com `id="section1"` .  Para testar uma demonstração com a seção 1 realçada, navegue [até CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="A página da Web realçada sem CSS forçado" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Página da Web realçada sem CSS forçado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":target CSS forced and webpage highlighted" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forçado e página da Web realçada  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Usar elementos Duplicate para copiar elementos  

Use o novo **atalho de elemento Duplicado** para clonar um elemento.  Na ferramenta **Elementos,** passe o mouse sobre um elemento, abra o menu contextual \(clique com o botão direito do mouse\), escolha **o elemento Duplicate**.  Um novo elemento é criado sob o elemento selecionado.  Para duplicar o elemento com um atalho de teclado, selecione `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) ou `Shift` + `Option` + `Down Arrow` \(macOS\).  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="O elemento Duplicate é realçado no menu de contexto em um elemento da ferramenta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   O **elemento Duplicate** é realçado no menu de contexto em um elemento da ferramenta **Elementos**  
:::image-end:::  

#### Seletores de cores para propriedades CSS personalizadas  

O **painel Estilos** agora exibe seletores de cores para propriedades CSS personalizadas.  Para passar pelos formatos RGBA, HSLA e Hex do valor de cor, segure e `Shift` escolha o selador de cores.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Seletores de cores para propriedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Seletores de cores para propriedades CSS personalizadas  
:::image-end:::  

#### Copiar classes e propriedades CSS  

Agora você pode copiar as propriedades CSS mais rapidamente com algumas novas opções no menu contextual.  Na ferramenta **Elementos,** escolha um elemento.  Para copiar o valor, no painel **Estilos,** passe o mouse sobre uma classe CSS ou uma propriedade CSS, abra um menu contextual \(clique com o botão direito do mouse\) e escolha a opção de cópia.  

:::row:::
   :::column span="":::
      Copiar opções para uma classe CSS.  
      
      | Opção | Detalhes |  
      |:--- |:--- |  
      | **Seletor de cópia** | Copie o nome do seletor atual. |  
      | **Regra de cópia** | Copie a regra do seletor atual. |  
      | **Copiar todas as declarações** | Copie todas as declarações sob a regra atual, incluindo propriedades não válidas e prefixadas. |  
   :::column-end:::
   :::column span="":::
      Copiar opções para uma propriedade CSS.  
      
      | Opção | Detalhes |      
      |:--- |:--- |  
      | **Declaração de cópia** | Copie a declaração da linha atual. |  
      | **Propriedade Copy** | Copie a propriedade da linha atual. |  
      | **Valor da cópia** | Copie o valor da linha atual. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Copiar opções para uma classe CSS no menu contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Copiar opções para uma classe CSS no menu contextual  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Copiar opções para uma propriedade CSS no menu contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Copiar opções para uma propriedade CSS no menu contextual  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1152391][CR1152391].  

### Atualizações de cookies  

#### Nova opção para exibir cookies decodificados por URL  

Agora você pode optar por exibir o valor de cookies decodificados de URL no **painel Cookies.**  Para exibir o cookie decodificado, navegue até o painel **** Cookies do Aplicativo, escolha qualquer cookie na lista e marque a caixa de seleção ao lado de Mostrar URL  >  **** **decodificada.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opção para exibir cookies decodificados por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Opção para exibir cookies de URL decodificados  
:::image-end:::  

#### Filtrar e limpar cookies visíveis  

No Microsoft Edge versão 88 ou anterior, a ferramenta **Aplicativo** só forneceu uma maneira de limpar todos os cookies com o botão Limpar **todos os cookies.**  No Microsoft Edge versão 89, agora você pode escolher Limpar **cookies** filtrados para excluir apenas os cookies filtrados.  Para filtrar cookies, navegue **até**Cookies de  >  **** Aplicativo e digite a caixa **de** texto Filtro.  Para excluir os cookies exibidos, escolha o botão Limpar **cookies filtrados.**  Para exibir todos os outros cookies, limpe o texto do filtro.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Limpar somente cookies visíveis" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Limpar somente cookies visíveis  
:::image-end:::  

#### Nova opção para limpar cookies de terceiros no painel armazenamento  

O DevTools agora limpa somente cookies de terceiros por padrão.  Para limpar somente os dados do site **** e os cookies de terceiros, navegue até o Armazenamento de Aplicativos e escolha Limpar  >  **** dados **do site.**  

Para limpar os dados do site e todos os cookies, navegue até **o Armazenamento de**  >  **Aplicativos.**  Escolha a caixa de seleção ao lado **da inclusão de cookies de**terceiros e, em seguida, selecione Limpar dados do **site.**  

Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opção para limpar cookies de terceiros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Opção para limpar cookies de terceiros  
:::image-end:::  

### Atualizações da ferramenta de rede  

#### Persist Record network log setting  

No Microsoft Edge versão 88 ou anterior, o DevTools redefine a configuração de **log** de rede Registro quando uma página da Web é atualizada.  No Microsoft Edge versão 89, o DevTools agora mantém a **configuração de log de rede Gravar.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registrar log de rede" lightbox="../../media/2021/01/network-log.msft.png":::
   Registrar log de rede  
:::image-end:::  

#### A opção online agora é Nenhuma opção de reação  

A opção de emulação de rede **Online** agora é renomeada como **Sem Throttling**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Nenhuma opção de throttling" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Nenhuma opção de throttling**  
:::image-end:::  

### Novas opções de cópia na ferramenta Console, ferramenta Fontes e painel Estilos

#### Copiar objeto na ferramenta Console e Fontes  

Agora você pode copiar valores de objeto nas **ferramentas Console** **e** Fontes.  A capacidade de copiar valores de objeto é útil ao trabalhar com objetos grandes.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1148353][CR1148353] e [1149859][CR1149859].  

:::row:::
   :::column span="":::
      Na ferramenta **Console,** passe o mouse sobre um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar objeto**.  
   :::column-end:::
   :::column span="":::
      Na ferramenta **Fontes,** em um ponto de interrupção, passe o mouse sobre um objeto, na janela **pop-up** Objeto, realça um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar objeto **.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/console-copy-object.msft.png" alt-text="Copiar objeto no Console" lightbox="../../media/2021/01/console-copy-object.msft.png":::
         Copiar objeto no **Console**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png" alt-text="Copiar objeto em Fontes" lightbox="../../media/2021/01/sources-breakpoint-object-copy-object.msft.png":::
         Copiar objeto em **Fontes**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Copiar o nome do arquivo na ferramenta Sources e no painel Estilos  

Agora você pode copiar um nome de arquivo usando o menu contextual.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1155120][CR1155120].  

:::row:::
   :::column span="":::
      Na ferramenta **Fontes,** passe o mouse sobre um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome de arquivo.**  
   :::column-end:::
   :::column span="":::
      Na ferramenta **Elementos** > **de** Estilos, passe o mouse sobre um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar nome **de arquivo.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar o nome do arquivo em Fontes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copiar o nome do arquivo em **Fontes**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar o nome do arquivo no painel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copiar o nome do arquivo **no painel** Estilos  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Atualizações nos detalhes do Quadro  

#### Informações dos funcionários do serviço nos detalhes do quadro  

O DevTools agora lista um serviço dedicado sob o quadro pai.  Na figura a seguir, os detalhes do serviço são exibidos.  Para exibir os detalhes do serviço de trabalho, navegue até **Os**Funcionários do Serviço de Quadros de Aplicativo e  >  ****  >  `top`  >  **** escolha um trabalhador de serviço.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informações dos trabalhadores do serviço nos detalhes de Quadros" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Informações dos trabalhadores** do serviço nos **detalhes de** Quadros  
:::image-end:::  

#### Medir informações de memória nos detalhes do quadro  

O `performance.measureMemory()` status da API agora é exibido na seção disponibilidade da **API.**  A nova `performance.measureMemory()` API estima o uso de memória de toda a página da Web.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memória" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Medir memória  
:::image-end:::  

### Quadros descartados na ferramenta desempenho  

Quando você [analisa o desempenho da carga na ferramenta Desempenho,][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]a seção **Quadros** agora marca quadros descartados como vermelho.  Para exibir a taxa de quadros, passe o mouse sobre um quadro descartado.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Quadros descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Quadros descartados  
:::image-end:::  

#### Novo cálculo de contraste de cor - Algoritmo de Contraste Perceptual Avançado (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

O [APCA (Advanced Perceptual Contrast Algorithm)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] substitui a taxa de contraste das diretrizes do [][W3cWaiWcag21QuickrefContrastMinimum] / [AA AAA][W3cWaiWcag21QuickrefContrastEnhanced] no Selador [de Cores.][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]  APCA é uma nova maneira de calcular o contraste.  Ele é baseado em pesquisas modernas sobre percepção de cores.  Em comparação com as diretrizes AA/AAA, a APCA depende mais do contexto.  O contraste é calculado com base nas seguintes propriedades espaciais do texto, cor e contexto.  

*   Propriedades espaciais do texto que incluem peso e tamanho da fonte.  
*   Propriedades espaciais de cor que incluem o contraste percebido entre o texto e o plano de fundo.  
*   Propriedades espaciais de contexto que incluem luz ambiente, arredores e finalidade pretendido.  
    
Para ativar esse experimento, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e escolha a caixa de seleção ao lado de Habilitar novo ApCA (Advanced Perceptual Contrast Algorithm) substituindo a taxa de contraste anterior e as diretrizes  >  **** **AA/AAA.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA no Selador de Cores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA no Selador de Cores  
:::image-end:::  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows, Linux ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novidades no devTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Exibir a taxa de contraste de um elemento de texto no selador de cores - referência de acessibilidade | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Alterar CSS - referência css | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Teste em dispositivos de tela dupla e dobráveis - Emular dispositivos de tela dupla e dobrável no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um viewport móvel - Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Desempenho da carga do registro - referência da análise de | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Editar estilos e configurações de fonte CSS no painel Estilos no DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Visão geral das Ferramentas de Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a sam - Introdução a dispositivos de tela dupla | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Recurso de abrangeção de tela de mídia CSS para detecção de tela dupla | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Seção 1 - Demonstração css :target para o que há de novo no DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementando o menu suspenso em configurações para alterar os temas | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Incluindo o Depurador do Microsoft Edge como uma conta de | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Atualizando a versão do Edge DevTools para 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Adicionar botões de fechamento único ao painel de instâncias | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Selecione características de fonte e cores de plano de fundo para fornecer contraste suficiente para a capacidade de | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos confiáveis | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Novo Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Extensões do Marketplace | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador do Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

<!--[CR174309]: https://crbug.com/174309 "Issue 174309: DevTools: Allow to customize keyboard shortcuts/key bindings | Chromium bugs"  -->  
<!--[CR772558]: https://crbug.com/772558 "Issue 772558: DevTools: Update to latest version of Lighthouse | Chromium bugs"  -->  
[CR978059]: "Problema 978059: Excluir cookies ao filtre-los, exclua todos os cookies não apenas os https://crbug.com/978059 filtrados | Bugs do Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Novo recurso | Precisa de uma opção para ver o valor de url decodificado em cookies | Bugs do Chromium"  
[CR1003629]: "Problema 1003629: o nó de captura não captura de tela do nó abaixo https://crbug.com/1003629 da dobra mais. | Bugs do Chromium"  
[CR1012337]: "Problema 1012337: Limpar Dados do Site destrói a sessão do Google em sites que não são do https://crbug.com/1012337 Google | Bugs do Chromium"  
[CR1028078]: "Problema 1028078: Colocar Online e Offline um ao lado do outro na lista https://crbug.com/1028078 | Bugs do Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitação de Recurso: o DevTools deve emular dispositivos de tela dupla e dobrável | Bugs do Chromium"  
<!--[CR1073909]: https://crbug.com/1073909 "Issue 1073909: BLOCKED | Chromium bugs"  -->  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: Mostrar quadros descartados na linha do tempo do devtools | Bugs do Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: oferecer uma interface do usuário do editor de face de tipos especializada | Bugs do Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: lógica de cálculo de contraste de atualização por nova especificação | Bugs do Chromium"  
[CR1122507]: "Problema 1122507: Informações de trabalho do Surface no quadro de exibição de árvore https://crbug.com/1122507 | Bugs do Chromium"  
[CR1122580]: "Problema 1122580: Impossível desabilitar a gravação de rede ao https://crbug.com/1122580 recarregar | Bugs do Chromium"  
<!--[CR1126824]: https://crbug.com/1126824 "Issue 1126824: ☂ Support Trust Token debugging in DevTools | Chromium bugs"  -->  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramentas do Flexbox | Bugs do Chromium"  
<!--[CR1137837]: https://crbug.com/1137837 "Issue 1137837: ☂ Improve Trusted Types support in DevTools | Chromium bugs"  -->  
[CR1139899]: "Problema 1139899: Disponibilidade de API com entrada de relatório na exibição de detalhes https://crbug.com/1139899 do quadro | Bugs do Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: sobreposição de | Bugs do Chromium"  
<!--[CR1142804]: https://crbug.com/1142804 "Issue 1142804: Implement break-on-trusted-type-violation | Chromium bugs"  -->  
<!--[CR1144127]: https://crbug.com/1144127 "Issue 1144127: BLOCKED | Chromium bugs"  -->  
[CR1147016]: "Problema 1147016: O selador de cores não é exibido na https://crbug.com/1147016 função var(). | Bugs do Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: Solicitação de Recurso: Copiar Objeto do console de ferramentas de | Bugs do Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitação de recurso][Console] adicione o objeto copy ao item da área de transferência ao menu contextual | Bugs do Chromium"  
[CR1150797]: "Problema 1150797: Adicionar menu de contexto de elemento duplicado no painel https://crbug.com/1150797 elemento | Bugs do Chromium"  
<!--[CR1150883]: https://crbug.com/1150883 "Issue 1150883: Remove TT messages from the console but keep underlining in the sources tab | Chromium bugs"  -->  
<!--[CR1152290]: https://crbug.com/1152290 "Issue 1152290: Devtools support for QuicTransport | Chromium bugs"  -->  
[CR1152391]: "Problema 1152391: Suporte para copiar o menu de contexto CSS no painel de https://crbug.com/1152391 estilos | Bugs do Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Suporte para nome de arquivo de cópia e número de linha | Bugs do Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: adicionar suporte para :target no recurso de estado do elemento de força | Bugs do Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Acessibilidade - Narrador: O Narrador não está anunciando a contagem e a posição das sugestões disponíveis para o código na guia Estilos | Bugs do Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "| Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (aprimorado) - Como atender às WCAG (Referência Rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo) - Como atender às WCAG (Referência Rápida) | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2021/01/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Espaços reservados em espaços reservados"  
