---
description: A ferramenta What's New agora é Bem-vindo, Editor de Fontes Visuais no painel Estilos, ferramentas de depuração do CSS Flexbox e muito mais.
title: Novidades no DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2722da0093b3ba6521b5190e61bb208e02a2041e
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408336"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-89"></a>Novidades no DevTools (Microsoft Edge 89)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="whats-new-is-now-welcome"></a>O que há de novo agora é Bem-vindo  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

A **ferramenta Novidades no** Microsoft Edge DevTools agora tem uma nova aparência e um novo nome: **Bem-vindo.**  A **ferramenta Bem-vindo** ainda exibe as últimas notícias e atualizações do DevTools.  Agora também inclui links para a documentação do Microsoft Edge DevTools, maneiras de enviar comentários e muito mais.  Para exibir a **ferramenta Bem-vindo** após cada atualização para o Microsoft Edge, escolha a caixa de seleção ao lado da guia Abrir após **cada atualização** sob o título.  Para fechar a **ferramenta Bem-vindo,** escolha o **X** no lado direito do título da guia.  Se você preferir a ferramenta **Original Novidades,** navegue até [Configurações Experimentos][DevtoolsCustomizeIndexSettings]e remova a caixa de seleção ao lado da guia  >  **** Habilitar **Boas-vindas.**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="A ferramenta Welcome é realçada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   A **ferramenta Welcome** é realçada  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Editor de Fontes Visuais no painel Estilos  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Quando você trabalha com fontes em CSS, use o novo Editor de [Fontes visual.][DevtoolsInspectStylesEditFonts]  Você pode definir fontes de fallback e usar controles deslizantes para definir o peso, o tamanho, a altura da linha e o espaçamento.  O **Editor de Fontes** ajuda você a concluir as seguintes ações.  

*   Alternar entre unidades para propriedades de fonte diferentes  
*   Alternar entre palavras-chave para propriedades de fonte diferentes  
*   Converter unidades  
*   Gerar código CSS preciso  
    
Para ativar esse experimento, navegue até [Configurações Experimentos][DevtoolsCustomizeIndexSettings]e escolha a caixa de seleção ao lado de Habilitar novas ferramentas do Editor de Fontes  >  **** no **painel Estilos.**  Para obter mais informações, navegue até Editar estilos de fonte CSS e configurações no [painel Estilos em DevTools][DevtoolsInspectStylesEditFonts].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="O editor de Fonte visual é realçado no painel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   O editor **de Fonte visual** é realçado no painel **Estilos**  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>Ferramentas de depuração do CSS Flexbox  

Os recursos de depuração do Flexbox estão em desenvolvimento ativo.  Para ativar o experimento para os dois recursos a seguir, navegue até [Settings Experiments][DevtoolsCustomizeIndexSettings]e escolha a caixa de seleção ao lado de Habilitar novos recursos  >  **** **de depuração do CSS Flexbox.**  Para analisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1136394][CR1136394] e [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>Novo ícone do Flexbox (flex) ajuda a identificar e exibir contêineres flexíveis  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Na ferramenta **Elementos,** o novo ícone flexbox (flex) ajuda a identificar contêineres do Flexbox em seu código.  Escolha o ícone Flexbox \(flex\) para ativar ou desativar o efeito de sobreposição que descreve um contêiner do Flexbox.  Você pode personalizar a cor da sobreposição no painel **Layout,** que está localizado ao lado de **Styles** e **Computed**.  

:::row:::
   :::column span="":::
      Para ativar e desativar o efeito de sobreposição que descreve o contêiner Flexbox, escolha o ícone Flexbox \( `flex` \)  
   :::column-end:::
   :::column span="":::
      Você pode personalizar a cor da sobreposição no painel **Layout** ao lado de **Styles** e **Computed**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="O ícone e a página da Web do Flexbox (flex) realçados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         O ícone e a página da Web do **Flexbox** `flex` \( \) realçadas :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="As sobreposições do Flexbox realçadas no painel Layout" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         As **sobreposições do Flexbox** realçadas no **painel Layout**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-gridlines-when-flexbox-layouts-change-using-css-properties"></a>Exibir ícones de alinhamento e linhas de grade quando layouts do Flexbox mudam usando propriedades CSS  

<!--  Title: Display alignment icons and gridlines for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Quando você edita CSS para o layout do Flexbox, os preenchimentos automáticos CSS no painel **Estilos** agora exibem ícones úteis ao lado de propriedades relevantes do Flexbox.  Para experimentar esse novo recurso, abra a **ferramenta Elements** e selecione um contêiner flexível.  Em seguida, adicione ou altere uma propriedade nesse contêiner no painel **Estilos.**  

:::row:::
   :::column span="":::
      O menu de preenchimento automático agora exibe ícones que indicam o efeito das propriedades de alinhamento, como `align-content` e `align-items` .  
   :::column-end:::
   :::column span="":::
      Além disso, o DevTools agora exibe uma linha de orientação para ajudá-lo a revisar melhor a `align-items` propriedade CSS.  A `gap` propriedade CSS também tem suporte.  Na figura a seguir, a propriedade CSS é definida como e o padrão de eclosão `gap` para cada intervalo é `gap: 12px;` exibido.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de preenchimento automático realçado para propriedades CSS que começam com alinhamento-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menu de preenchimento automático realçado para propriedades CSS que começam com `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Lacuna do Flexbox em propriedades CSS e página da Web realçada" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` em propriedades CSS e página da Web realçada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Adicionar ferramentas rapidamente com o novo botão Mais Ferramentas  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Agora você tem uma nova maneira de abrir mais ferramentas no Microsoft Edge DevTools.  Depois de ativar esse experimento, o ícone **Mais Ferramentas** será exibido como um sinal de a mais ( ) à direita do `+` painel principal.  Para exibir uma lista de outras ferramentas para adicionar ao painel principal, escolha o ícone **Mais Ferramentas** \( `+` \)  Para ativar esse experimento, navegue até [Configurações Experimentos][DevtoolsCustomizeIndexSettings]e, em seguida, escolha a caixa de seleção ao lado de  >  **** Habilitar **+ menus**de guia de botão para abrir mais ferramentas .  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Mais Ferramentas realçadas no DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Mais Ferramentas** realçadas no DevTools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Tecnologias assistivas agora anunciam posição e contagem de sugestões CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Quando você edita CSS, você tem um menu suspenso de recursos.  Esse recurso não estava disponível para usuários de tecnologias assistivas, já que ele é anunciado no Microsoft Edge versão 89.  Um usuário de tecnologias assistivas agora pode navegar por sugestões CSS no painel **Estilos.**  No Microsoft Edge versão 88 e anterior, a tecnologia assistiva anunciada como um usuário navegava pela lista de sugestões ao editar CSS no `Suggestion` painel **Estilos.**  No Microsoft Edge versão 89, um usuário de tecnologia assistida agora ouve a posição e a contagem da sugestão atual.  Cada sugestão é anunciada à medida que o usuário navega pela lista de sugestões, como a Sugestão 3 de 5.  Para saber mais sobre como escrever CSS no DevTools, navegue até [Alterar CSS][DevtoolsCssReferenceChangeCss].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1157329][CR1157329].  

Para exibir um vídeo que exibe e lê em voz alta várias sugestões com esse experimento ativado, navegue até Voiceover anunciando opções [de devtools](https://youtu.be/9TcUpleEwwA) no YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="A sugestão realçada no painel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   A `suggestion` lista realçada no painel **Estilos**  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emular o Surface Duo e o Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Teste a aparência do seu site ou aplicativo nos seguintes dispositivos no Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Ative os **recursos da Plataforma Web Experimental** para acessar o novo recurso de abrangência de tela de mídia [CSS][DualScreenWebCssMediaSpanning] e obter a [API JavaScript doWindowSegments.][DualScreenWebJavascriptGetwindowsegments]  Navegue `edge://flags` até e alterne o sinalizador ao lado dos recursos **da Plataforma Web Experimental.**  Para ajudar a aprimorar seu site ou aplicativo para dispositivos de tela dupla e dobráveis, use os seguintes recursos ao [emular o dispositivo][DevtoolsDeviceModeIndex].  

*   [Abrangendo][DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices], que é quando seu site \(ou app\) aparece em ambas as telas.  
*   [Renderização da emenda][DualScreenIntroductionHowToWorkWithSeam], que é o espaço entre as duas telas.  
    
Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular tela dupla" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emular tela dupla  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>Microsoft Edge Developer Tools for Visual Studio Code versão 1.1.2  

O [Microsoft Edge Developer Tools for Visual Studio Code versão][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] 1.1.2 do Microsoft Visual Studio Code tem as seguintes alterações desde a versão anterior.  O Microsoft Visual Studio Code atualiza as extensões automaticamente.  Para atualizar manualmente para a versão 1.1.2, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Adicionado um **botão Fechar instância** a cada item na lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Versão do [Microsoft Edge DevTools][DevtoolsMain] com 84.0.522.63 para [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   [Depurador incluído para o Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como uma dependência \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Opção de configurações implementadas para alterar temas de extensão \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub do vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Captura de tela do nó de captura além do viewport  

No Microsoft Edge versão 89, as capturas de tela do nó são mais precisas, capturando o nó completo, mesmo que o conteúdo do nó não seja visível no viewport.  Na ferramenta **Elementos,** passe o mouse em um elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Captura de **tela do nó captura de tela**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de tela do nó de captura realçada no menu de contexto na ferramenta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Captura de tela do nó de** captura realçada no menu de contexto na ferramenta **Elementos**  
:::image-end:::  

### <a name="elements-tool-updates"></a>Atualizações da ferramenta Elements  

#### <a name="support-forcing-the-target-css-state"></a>Suporte forçando o estado :target CSS  

Agora você pode usar o DevTools para forçar a [pseudo-classe :target][MdnDocsWebCssTarget] CSS.  A pseudo-classe é disparada quando um elemento exclusivo \(o elemento de destino\) tem um que corresponde `:target` a um fragmento da `id` URL.  Por exemplo, a `http://www.example.com/index.html#section1` URL dispara a `:target` pseudo-classe em um elemento HTML com `id="section1"` .  Para experimentar uma demonstração com a seção 1 realçada, navegue até [CSS :target demo][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="A página da Web realçada sem CSS forçado" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Página da Web realçada sem CSS forçado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text=":css de destino forçado e página da Web realçada" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forçado e página da Web realçada  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Usar elementos Duplicados para copiar elementos  

Use o novo **atalho de elemento Duplicate** para clonar um elemento.  Na ferramenta **Elementos,** passe o mouse em um elemento, abra o menu contextual \(clique com o botão direito do mouse\), escolha **Duplicar elemento**.  Um novo elemento é criado sob o elemento selecionado.  Para duplicar o elemento com um atalho de teclado, selecione `Shift` + `Alt` + `Down Arrow` \(Windows/Linux\) ou `Shift` + `Option` + `Down Arrow` \(macOS\).  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="O elemento Duplicate é realçado no menu de contexto em um elemento na ferramenta Elements" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   O **elemento Duplicate** é realçado no menu de contexto em um elemento na ferramenta **Elements**  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Seletores de cores para propriedades CSS personalizadas  

O **painel Estilos** agora exibe seletores de cores para propriedades CSS personalizadas.  Para passar pelos formatos RGBA, HSLA e Hex do valor de cor, segure e `Shift` escolha o selador de cores.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1147016][CR1147016].  

:::image type="complex" source="../../media/2021/01/elements-styles-change-color-format.msft.png" alt-text="Seletores de cores para propriedades CSS personalizadas" lightbox="../../media/2021/01/elements-styles-change-color-format.msft.png":::
   Seletores de cores para propriedades CSS personalizadas  
:::image-end:::  

#### <a name="copy-css-classes-and-properties"></a>Copiar classes e propriedades CSS  

Agora você pode copiar as propriedades CSS mais rapidamente com algumas novas opções no menu contextual.  Na ferramenta **Elementos,** escolha um elemento.  Para copiar o valor, no painel **Estilos,** passe o mouse em uma classe CSS ou em uma propriedade CSS, abra um menu contextual \(clique com o botão direito do mouse\) e escolha a opção de cópia.  

:::row:::
   :::column span="":::
      Opções de cópia para uma classe CSS.  
      
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
      | **Valor de cópia** | Copie o valor da linha atual. |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-class.msft.png" alt-text="Opções de cópia para uma classe CSS no menu contextual" lightbox="../../media/2021/01/copy-css-class.msft.png":::
         Opções de cópia para uma classe CSS no menu contextual  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/copy-css-property-cropped.msft.png" alt-text="Opções de cópia de uma propriedade CSS no menu contextual" lightbox="../../media/2021/01/copy-css-property.msft.png":::
         Opções de cópia de uma propriedade CSS no menu contextual  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1152391][CR1152391].  

### <a name="cookies-updates"></a>Atualizações de cookies  

#### <a name="new-option-to-display-url-decoded-cookies"></a>Nova opção para exibir cookies decodificados por URL  

Agora, você pode optar por exibir o valor de cookies decodificados por URL no **painel Cookies.**  Para exibir o cookie decodificado, navegue até o painel **** Cookies de Aplicativo, escolha qualquer cookie na lista e escolha a caixa de seleção ao lado de Mostrar URL  >  **** **decodificada**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opção para exibir cookies decodificados por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Opção para exibir cookies decodificados de URL  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtrar e limpar cookies visíveis  

No Microsoft Edge versão 88 ou anterior, a ferramenta **Application** só forneceu uma maneira de limpar todos os cookies com o botão **Limpar todos os cookies.**  No Microsoft Edge versão 89, agora você pode escolher **Limpar cookies filtrados** para excluir apenas os cookies filtrados.  Para filtrar cookies, navegue até Cookies **de**  >  **Aplicativo**e digite na **caixa de texto Filtro.**  Para excluir os cookies exibidos, escolha o botão **Limpar cookies filtrados.**  Para exibir todos os outros cookies, limpe o texto do filtro.  Para analisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Limpar somente cookies visíveis" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Limpar somente cookies visíveis  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Nova opção para limpar cookies de terceiros no painel Armazenamento  

O DevTools agora limpa apenas cookies de primeira parte por padrão.  Para limpar apenas os dados do site e cookies de primeira parte, navegue até **Armazenamento**de  >  **Aplicativos**e escolha **Limpar dados do site.**  

Para limpar os dados do site e todos os cookies, navegue até **Armazenamento de**  >  **Aplicativos.**  Escolha a caixa de seleção ao lado **de incluir cookies de**terceiros e, em seguida, escolha Limpar dados do **site**.  

Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opção para limpar cookies de terceiros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Opção para limpar cookies de terceiros  
:::image-end:::  

### <a name="network-tool-updates"></a>Atualizações da ferramenta de rede  

#### <a name="persist-record-network-log-setting"></a>Persist Record network log setting  

No Microsoft Edge versão 88 ou anterior, o DevTools redefine a configuração registro de **log** de rede quando uma página da Web é atualizada.  No Microsoft Edge versão 89, o DevTools agora persiste na **configuração registro de log de rede.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registrar log de rede" lightbox="../../media/2021/01/network-log.msft.png":::
   Registrar log de rede  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>A opção Online agora é Nenhuma opção de throttling  

A opção de emulação de rede **Online** agora é renomeada para **Nenhuma Throttling**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Nenhuma opção de throttling" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   **Nenhuma opção de throttling**  
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Novas opções de cópia no painel Console, Ferramenta Fontes e Estilos

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Copiar objeto na ferramenta Console e Fontes  

Agora você pode copiar valores de objeto nas **ferramentas Console** **e Sources.**  A capacidade de copiar valores de objeto é útil ao trabalhar com objetos grandes.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1148353][CR1148353] e [1149859][CR1149859].  

:::row:::
   :::column span="":::
      Na ferramenta **Console,** passe o mouse em um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar objeto**.  
   :::column-end:::
   :::column span="":::
      Na ferramenta **Fontes,** em um ponto de interrupção, passe o mouse em um objeto, na janela **pop-up** Objeto, realça um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar **objeto**.  
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

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Copiar nome de arquivo no painel Fontes e Estilos  

Agora você pode copiar um nome de arquivo usando o menu contextual.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1155120][CR1155120].  

:::row:::
   :::column span="":::
      Na ferramenta **Fontes,** passe o mouse em um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome de arquivo**.  
   :::column-end:::
   :::column span="":::
      No painel **Ferramentas de elementos** > **Estilos,** passe o mouse em um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome de arquivo**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar nome de arquivo em Fontes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copiar nome de arquivo em **Fontes**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar nome de arquivo no painel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copiar nome de arquivo no painel **Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Atualizações para detalhes do Quadro  

#### <a name="service-workers-information-in-frame-details"></a>Informações de Funcionários do Serviço em Detalhes do Quadro  

O DevTools lista agora um funcionário de serviço dedicado sob o quadro pai.  Na figura a seguir, os detalhes do trabalhador do serviço são exibidos.  Para exibir os detalhes do serviço de trabalho, navegue até **Application**  >  **Frames**  >  `top`  >  **Service Workers** e escolha um trabalhador de serviço.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informações dos Trabalhadores do Serviço nos detalhes quadros" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   **Informações dos Trabalhadores** do Serviço nos **detalhes quadros**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Medir informações de memória nos detalhes do quadro  

O `performance.measureMemory()` status da API agora é exibido na seção disponibilidade da **API.**  A nova `performance.measureMemory()` API estima o uso de memória de toda a página da Web.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir Memória" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Medir Memória  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Quadros descartados na ferramenta Desempenho  

Quando você [analisa o desempenho da carga na ferramenta Desempenho][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], a seção **Quadros** agora marca quadros descartados como vermelho.  Para exibir a taxa de quadros, passe o mouse em um quadro descartado.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Quadros descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Quadros descartados  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Novo cálculo de contraste de cor - Algoritmo de Contraste Perceptual Avançado (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

O [Algoritmo de Contraste Perceptual Avançado (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] substitui a taxa de contraste de diretrizes do [AAAA][W3cWaiWcag21QuickrefContrastMinimum]no / [][W3cWaiWcag21QuickrefContrastEnhanced] [Selador de Cores][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  APCA é uma nova maneira de calcular contraste.  Baseia-se em pesquisas modernas sobre percepção de cores.  Em comparação com as diretrizes do AA/AAA, a APCA é mais dependente de contexto.  O contraste é calculado com base nas seguintes propriedades espaciais do texto, cor e contexto.  

*   Propriedades espaciais do texto que incluem o peso e o tamanho da fonte.  
*   Propriedades espaciais de cor que incluem contraste percebido entre texto e plano de fundo.  
*   Propriedades espaciais do contexto que incluem luz ambiente, ambientes e finalidade pretendido.  
    
Para ativar esse experimento, navegue até Configurações [Experimentos][DevtoolsCustomizeIndexSettings]e escolha a caixa de seleção ao lado de Habilitar novo Algoritmo de Contraste Perceptual Avançado (APCA) substituindo a taxa de contraste anterior e as diretrizes  >  **** **AA/AAA**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA no Se picker de cores" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA no Se picker de cores  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows, Linux ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Exibir a taxa de contraste de um elemento de texto no Selador de Cores - Referência de acessibilidade | Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: /microsoft-edge/devtools-guide-chromium/css/reference#change-css "Alterar CSS - referência CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestingFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/device-mode/dual-screen-and-foldables#testing-on-foldable-and-dual-screen-devices "Teste em dispositivos dobráveis e de tela dupla - Emular dispositivos de tela dupla e dobráveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Simular um viewport móvel - emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-load-performance "Desempenho da carga do registro - referência de análise de desempenho | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: /microsoft-edge/devtools-guide-chromium/inspect-styles/edit-fonts "Editar estilos de fonte CSS e configurações no painel Estilos no DevTools | Microsoft Docs"  
[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium/index "Visão geral das Ferramentas de Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a emenda - Introdução a dispositivos de tela dupla | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Recurso de abrangeção de tela de mídia CSS para detecção de tela | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Seção 1 - demonstração css :target para What's New in DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: Implementing dropdown in settings to change themes | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: Including Debugger for Microsoft Edge as a dependency | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: Atualização da versão Edge DevTools para 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Adicionar botões de fechamento único ao painel de instâncias | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Selecione características de fonte e cores de plano de fundo para fornecer contraste suficiente para | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos confiáveis | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Novo Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Extensão do Marketplace | Visual Studio Código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para o Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: Excluindo cookies ao filtre-los, exclua todos os cookies não apenas os filtrados | Bugs do Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: Novo recurso req | Opção de necessidade para ver o valor de decodificado por url em cookies | Bugs do Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: o Nó de Captura não captura mais a captura de tela do nó abaixo da dobra. | Bugs do Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: Limpar Dados do Site destrói a sessão do Google em sites que não são do Google | Bugs do Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: Colocar Online e Offline um ao lado do outro na lista | Bugs do Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: Solicitação de Recurso: DevTools deve emular dispositivos dobráveis e de tela dupla | Bugs do Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: Mostrar quadros descartados na linha do tempo do devtools | Bugs do Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: oferecer uma interface do usuário do editor de tipo especializado | Bugs do Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: lógica de cálculo de contraste de atualização por nova especificação | Bugs do Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o trabalho da superfície no modo de exibição árvore de quadros | Erros do Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: Impossível desabilitar a gravação de rede no recarregar | Bugs do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramenta Flexbox | Erros de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros do Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: sobreposição do flexbox | Bugs do Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: o selador de cores não é exibido na função var(). | Bugs do Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: Solicitação de Recurso: Copiar Objeto do console de devtools | Bugs do Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitação de recurso][Console] adicionar objeto copy ao item da área de transferência ao menu contextual | Bugs do Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: Adicionar menu de contexto de elemento duplicado no painel elemento | Bugs do Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: Suporte para copiar menu de contexto CSS no painel estilos | Bugs do Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Support copy file name and line number | Bugs do Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: adicione suporte ao recurso :target in force element state | Bugs do Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Acessibilidade - Narrador: o Narrador não está anunciando a contagem e a posição para sugestões disponíveis para código na guia Estilos | Bugs do Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Dobra de | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (aprimorado) - Como atender ao WCAG (Referência Rápida) | W3C"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (Mínimo) - Como atender ao WCAG (Referência Rápida) | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2021/01/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen

[SpanningPlaceholder]: link-t-b-d "Espaço reservado de abrangção"  
