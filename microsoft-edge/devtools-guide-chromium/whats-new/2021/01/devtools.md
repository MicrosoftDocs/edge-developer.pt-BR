---
description: A ferramenta Novidades agora se chama Bem-Vindo, Editor de Fonte Visual no painel Estilos, ferramentas de depuração do CSS Flexbox e muito mais.
title: Novidades no DevTools (Microsoft Edge 89)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: 6d1952832c84dc159222a8aa16aa0ffe11edff34
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564921"
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

## <a name="whats-new-is-now-welcome"></a>A ferramenta Novidades agora chama-se Bem-vindo  

<!--  Title: What's New is now Welcome  -->  
<!--  Subtitle: The What's New tool now has a new appearance and a new name:  Welcome -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

A ferramenta **Novidades** do Microsoft Edge DevTools agora tem uma nova aparência e um novo nome: **Bem-vindo.**  A ferramenta **Bem-vindo** ainda exibe as últimas notícias e atualizações do DevTools.  Agora também inclui links para a documentação do Microsoft Edge DevTools, maneiras de enviar comentários e muito mais.  Para exibir a ferramenta **Bem-vindo** após cada atualização para o Microsoft Edge, escolha a caixa de seleção ao lado da **guia Abrir após cada atualização** sob o título.  Para fechar a ferramenta **Bem-vindo**, escolha o **X** no lado direito do título da guia.  Se você preferir a ferramenta original **Novidades,** navegue até [Configurações][DevtoolsCustomizeIndexSettings]  > **Experimentos** e remova o X da caixa de seleção ao lado da **guia Habilitar Bem-vindo.**  

:::image type="complex" source="../../media/2021/01/welcome-tool-whats-new-88.msft.png" alt-text="A ferramenta Bem-vindo é realçada" lightbox="../../media/2021/01/welcome-tool-whats-new-88.msft.png":::
   A ferramenta **Bem-vindo** é realçada  
:::image-end:::  

## <a name="visual-font-editor-in-the-styles-pane"></a>Editor de Fonte visual no painel Estilos  

<!--  Title: Visual font editor in the Styles pane  -->  
<!--  Subtitle: Visual font editor in the Styles pane -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Quando você trabalha com fontes em CSS, use o novo [Editor de Fonte][DevtoolsInspectStylesEditFonts] visual.  Você pode definir fontes de fallback e usar controles deslizantes para definir o peso, o tamanho, a altura da linha e o espaçamento.  O **Editor de Fonte** ajuda você a concluir as seguintes ações.  

*   Alternar entre unidades para propriedades de fonte diferentes  
*   Alternar entre palavras-chave para propriedades de fonte diferentes  
*   Converter unidades  
*   Gerar código CSS preciso  
    
Para ativar esse experimento, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos** e escolha a caixa de seleção ao lado de **Habilitar as novas ferramentas de Editor de fonte dentro do painel Estilos**.  Para obter mais informações, navegue até [Editar estilos de fonte CSS e configurações no painel Estilos no DevTools][DevtoolsInspectStylesEditFonts].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1093229][CR1093229].  

:::image type="complex" source="../../media/2021/01/visual-font-editor.msft.png" alt-text="O Editor de fonte visual é realçado no painel Estilos" lightbox="../../media/2021/01/visual-font-editor.msft.png":::
   O **Editor de fonte** visual é realçado no painel **Estilos**  
:::image-end:::  

## <a name="css-flexbox-debugging-tools"></a>Ferramentas de depuração do CSS Flexbox  

Os recursos de depuração do Flexbox estão em desenvolvimento ativo.  Para ativar o experimento para os dois recursos a seguir, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos**e escolha a caixa de seleção ao lado de **Habilitar novos recursos de depuração do CSS Flexbox.**  Para analisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1136394][CR1136394] e [1139949][CR1139949].  

### <a name="new-flexbox-flex-icon-helps-identify-and-display-flex-containers"></a>Novo ícone do Flexbox (flex) ajuda a identificar e exibir contêineres flexíveis  

<!--  Title: Display Flexbox containers with Flexbox (flex) icon  -->  
<!--  Subtitle: New Flexbox (flex) icon in the Elements tool help you identify Flexbox containers in your code.  When toggled, the adorner displays and hides outlines of the flex container to help you debug the layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Na ferramenta **Elementos,** o novo ícone flexbox (flex) ajuda a identificar contêineres do Flexbox em seu código.  Escolha o ícone Flexbox \(flex\) para ativar ou desativar o efeito de sobreposição que descreve um contêiner do Flexbox.  Você pode personalizar a cor da sobreposição no painel **Layout,** que está localizado ao lado de **Estilos** e **Calculado**.  

:::row:::
   :::column span="":::
      Para ativar e desativar o efeito de sobreposição que descreve o contêiner Flexbox, escolha o ícone Flexbox \( `flex` \).  
   :::column-end:::
   :::column span="":::
      Você pode personalizar a cor da sobreposição no painel **Layout** ao lado de **Estilos** e **Calculado**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container.msft.png" alt-text="O ícone e a página da Web do Flexbox (flex) realçados" lightbox="../../media/2021/01/elements-flex-container.msft.png":::
         O ícone e a página da Web do **Flexbox** `flex` \( \) realçados :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-layout-flex-container.msft.png" alt-text="As sobreposições do Flexbox realçadas no painel Layout" lightbox="../../media/2021/01/elements-layout-flex-container.msft.png":::
         As **sobreposições do Flexbox** realçadas no painel **Layout**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-alignment-icons-and-visual-guides-when-flexbox-layouts-change-using-css-properties"></a>Exibir ícones de alinhamento e guias visuais quando os layouts do Flexbox mudam usando propriedades CSS  

<!--  Title: Display alignment icons and visual guides for changes to Flexbox layouts from CSS properties  -->  
<!--  Subtitle:  CSS autocomplete in the Styles tool now displays icons next to Flexbox properties to help you review the effect a property has on your Flexbox layout -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Quando você edita o CSS para o layout do Flexbox, o preenchimento automático do CSS no painel **Estilos** agora exibe ícones úteis ao lado de propriedades relevantes do Flexbox.  Para experimentar esse novo recurso, abra a ferramenta **Elementos** e selecione um contêiner flexível.  Em seguida, adicione ou altere uma propriedade nesse contêiner no painel **Estilos**.  

:::row:::
   :::column span="":::
      O menu de preenchimento automático agora exibe ícones que indicam o efeito das propriedades de alinhamento, como `align-content` e `align-items`.  
   :::column-end:::
   :::column span="":::
      Além disso, o DevTools agora exibe uma linha de orientação para ajudá-lo a revisar melhor a propriedade CSS `align-items`.  A propriedade CSS `gap` também tem suporte.  Na figura a seguir, a propriedade CSS `gap` é definida como `gap: 12px;` e o padrão de eclosão para cada intervalo é exibido.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align.msft.png" alt-text="Menu de preenchimento automático realçado para propriedades CSS que começam com alinhamento-" lightbox="../../media/2021/01/elements-flex-container-align.msft.png":::
         Menu de preenchimento automático realçado para propriedades CSS que começam com `align-`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png" alt-text="Lacuna do Flexbox em propriedades CSS e página da Web realçadas" lightbox="../../media/2021/01/elements-flex-container-align-items-center-gap-12px.msft.png":::
         Flexbox `gap` em propriedades CSS e página da Web realçadas  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="add-tools-quickly-with-new-more-tools-button"></a>Adicionar ferramentas rapidamente com o novo botão Mais Ferramentas  

<!--  Title: Add tools quickly with new More Tools button  -->  
<!--  Subtitle: A convenient way to open new tools in Microsoft Edge DevTools -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Agora você tem uma nova maneira de abrir mais ferramentas no Microsoft Edge DevTools.  Depois de ativar esse experimento, o ícone **Mais Ferramentas** será exibido como um sinal de mais (`+`) à direita do painel principal.  Para exibir uma lista de outras ferramentas para adicionar ao painel principal, escolha o ícone **Mais Ferramentas** \( `+` \).  Para ativar esse experimento, navegue até [Configurações][DevtoolsCustomizeIndexSettings]  > **Experimentos** e, em seguida, escolha a caixa de seleção ao lado de **Habilitar + menus de guia para abrir mais ferramentas**.  

:::image type="complex" source="../../media/2021/01/more-tools.msft.png" alt-text="Mais Ferramentas realçado no DevTools" lightbox="../../media/2021/01/more-tools.msft.png":::
   **Mais Ferramentas** realçado no DevTools  
:::image-end:::  

## <a name="assistive-technologies-now-announce-position-and-count-of-css-suggestions"></a>Tecnologias assistivas agora anunciam posição e contagem de sugestões CSS  

<!--  Title: Assistive technologies now announce position and count of CSS suggestions  -->  
<!--  Subtitle: CSS suggestions are now easier to navigate using screen readers -->  

Quando você edita CSS, você tem um menu suspenso de recursos.  Esse recurso não estava disponível para usuários de tecnologias assistivas, já que ele está anunciado no Microsoft Edge versão 89.  Um usuário de tecnologias assistivas agora pode navegar por sugestões CSS no painel **Estilos**.  No Microsoft Edge versão 88 e anterior, a tecnologia assistiva apresentava `Suggestion` à medida que um usuário navegava pela lista de sugestões ao editar CSS no painel **Estilos**.  No Microsoft Edge versão 89, um usuário de tecnologia assistida agora ouve a posição e a contagem da sugestão atual.  Cada sugestão é anunciada à medida que o usuário navega pela lista de sugestões, como a Sugestão 3 de 5.  Para saber mais sobre como escrever CSS no DevTools, navegue até [Alterar CSS][DevtoolsCssReferenceChangeCss].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1157329][CR1157329].  

Para exibir um vídeo que exibe e lê em voz alta várias sugestões com esse experimento ativado, navegue até [Voiceover anunciando opções de devtools](https://youtu.be/9TcUpleEwwA) no YouTube.  

:::image type="complex" source="../../media/2021/01/announce-css-suggestion.msft.png" alt-text="A sugestão realçada no painel Estilos" lightbox="../../media/2021/01/announce-css-suggestion.msft.png":::
   A lista `suggestion` realçada no painel **Estilos**  
:::image-end:::  

## <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emular o Surface Duo e o Samsung Galaxy Fold  

<!--  Title: Emulate new dual-screen and foldable devices  -->  
<!--  Subtitle: Test the appearance and feel of your website or app with Surface Duo and Samsung Galaxy Fold emulators -->  

Teste a aparência do seu site ou aplicativo nos seguintes dispositivos no Microsoft Edge.  

*   [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo]  
*   [Samsung Galaxy Fold][SamsungUsMobileGalaxyFold]  
    
Ative os **recursos da Plataforma Web Experimental** para acessar o novo [recurso de abrangência de tela de mídia CSS][DualScreenWebCssMediaSpanning] e [a API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  Navegue até `edge://flags` e alterne o sinalizador ao lado dos recursos para **recursos da Plataforma Web Experimental**.  Para ajudar a aprimorar seu site ou aplicativo para dispositivos de tela dupla e dobráveis, use os seguintes recursos ao [emular o dispositivo][DevtoolsDeviceModeIndex].  

*   [Abrangência][DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices], que é quando seu site \(ou app\) aparece em ambas as telas.  
*   [Renderização da junção][DualScreenIntroductionHowToWorkWithSeam], que é o espaço entre as duas telas.  
    
Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1054281][CR1054281].  

:::image type="complex" source="../../media/2021/01/emulate-surface-device-surface-duo.msft.png" alt-text="Emular tela dupla" lightbox="../../media/2021/01/emulate-surface-device-surface-duo.msft.png":::
   Emular tela dupla  
:::image-end:::  

## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-112"></a>O Microsoft Edge Developer Tools para o Visual Studio Code versão 1.1.2  

O [Microsoft Edge Developer Tools para o Visual Studio Code ][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extensão versão 1.1.2 para Microsoft Visual Studio Code tem as seguintes alterações desde a versão anterior.  O Microsoft Visual Studio Code atualiza as extensões automaticamente.  Para atualizar manualmente para a versão 1.1.2, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

*   Adicionado um botão **Fechar instância** a cada item na lista de destino \([#248][GithubMicrosoftVscodeEdgeDevtoolsPull248]\)  
*   Modificada versão [Microsoft Edge DevTools][DevtoolsIndex] de 84.0.522.63 para [85.0.564.40][DevtoolsWhatsNew85] \([#235][GithubMicrosoftVscodeEdgeDevtoolsPull235]\)  
*   Incluído [Depurador para o Microsoft Edge][VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge] como uma dependência \([#233][GithubMicrosoftVscodeEdgeDevtoolsPull233]\)  
*   Opção de configurações implementadas para alterar temas de extensão \([#229][GithubMicrosoftVscodeEdgeDevtoolsPull229]\)  
    
Você pode registrar problemas e contribuir para a extensão no [repositório do GitHub vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="capture-node-screenshot-beyond-viewport"></a>Captura de tela do nó de captura além do visor  

No Microsoft Edge versão 89, as capturas de tela do nó são mais precisas, capturando o nó completo, mesmo que o conteúdo do nó não seja visível no visor.  Na ferramenta **Elementos,** passe o mouse em um elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Captura de tela do nó**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1003629][CR1003629].  

:::image type="complex" source="../../media/2021/01/capture-node-screenshot.msft.png" alt-text="Captura de tela do nó realçada no menu de contexto na ferramenta Elementos" lightbox="../../media/2021/01/capture-node-screenshot.msft.png":::
   **Captura de tela do nó** realçada no menu de contexto na ferramenta **Elementos**  
:::image-end:::  

### <a name="elements-tool-updates"></a>Atualizações da ferramenta Elementos  

#### <a name="support-forcing-the-target-css-state"></a>Suporte forçando o estado CSS :target  

Você pode agora usar o DevTools para forçar a pseudo-classe CSS [:target][MdnDocsWebCssTarget].  A pseudo-classe `:target` é disparada quando um elemento exclusivo \(o elemento alvo\) tem um `id` que corresponde a um fragmento da URL.  Por exemplo, a URL `http://www.example.com/index.html#section1` dispara a pseudo-classe `:target` em um elemento HTML com `id="section1"`.  Para experimentar uma demonstração com a seção 1 realçada, navegue até [demonstração do CSS :target][GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1156628][CR1156628].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-none-forced.msft.png" alt-text="A página da Web realçada sem CSS forçado" lightbox="../../media/2021/01/elements-styles-none-forced.msft.png":::
         Página da Web realçada sem CSS forçado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-target-forced.msft.png" alt-text="CSS :target forçado e página da Web realçada" lightbox="../../media/2021/01/elements-styles-target-forced.msft.png":::
         `:target` CSS forçado e página da Web realçada  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <a name="use-duplicate-elements-to-copy-elements"></a>Usar Duplicar elemenos para copiar elementos  

Use o novo atalho **Duplicar elemento** para clonar um elemento.  Na ferramenta **Elementos**, passe o mouse em um elemento, abra o menu contextual \(clique com o botão direito do mouse\), escolha **Duplicar elemento**.   Um novo elemento é criado sob o elemento selecionado.  Para duplicar o elemento com um atalho de teclado, selecione `Shift` +`Alt`+`Down Arrow` \(Windows/Linux\) ou `Shift`+`Option`+`Down Arrow` \(macOS\).  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1150797][CR1150797].  

:::image type="complex" source="../../media/2021/01/elements-duplicate-element.msft.png" alt-text="A opção Duplicar elemento é realçada no menu de contexto em um elemento na ferramenta Elementos" lightbox="../../media/2021/01/elements-duplicate-element.msft.png":::
   A opção **Duplicar elemento** é realçada no menu de contexto em um elemento na ferramenta **Elements**  
:::image-end:::  

#### <a name="color-pickers-for-custom-css-properties"></a>Seletores de cores para propriedades CSS personalizadas  

O painel **Estilos** agora exibe seletores de cores para propriedades CSS personalizadas.  Para passar pelos formatos RGBA, HSLA e Hex do valor de cor, segure `Shift` e escolha o seletor de cor.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1147016][CR1147016].  

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
      | **Copiar seletor** | Copiar o nome do seletor atual. |  
      | **Copiar regra** | Copie a regra do seletor atual. |  
      | **Copiar todas as declarações** | Copiar todas as declarações sob a regra atual, incluindo propriedades não válidas e prefixadas. |  
   :::column-end:::
   :::column span="":::
      Opções de cópia para uma propriedade CSS.  
      
      | Opção | Detalhes |      
      |:--- |:--- |  
      | **Copiar declaração** | Copiar a declaração da linha atual. |  
      | **Copiar propriedade** | Copiar a propriedade da linha atual. |  
      | **Copiar valor** | Copiar o valor da linha atual. |  
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

Agora, você pode optar por exibir o valor de cookies decodificados por URL no painel **Cookies.**  Para exibir o cookie decodificado, navegue até **Aplicativo** >  painel **Cookies**, escolha qualquer cookie na lista e marque a caixa de seleção ao lado de **Mostrar URL decodificada**.   Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [997625][CR997625].  

:::image type="complex" source="../../media/2021/01/application-cookies-show-url-decoded.msft.png" alt-text="Opção para exibir cookies decodificados por URL" lightbox="../../media/2021/01/application-cookies-show-url-decoded.msft.png":::
   Opção para exibir cookies decodificados de URL  
:::image-end:::  

#### <a name="filter-and-clear-visible-cookies"></a>Filtrar e limpar cookies visíveis  

Na versão 88 ou anterior do Microsoft Edge, a ferramenta **Application** fornecia apenas uma maneira de limpar todos os cookies com o botão **Limpar todos os cookies**.  Na versão 89 do Microsoft Edge, agora você pode escolher **Limpar cookies filtrados** para excluir somente os cookies filtrados.  Para filtrar cookies, navegue até **Aplicativo** > **Cookies** e digite na caixa de texto **Filtrar**.  Para excluir os cookies exibidos, escolha o botão **Limpar cookies filtrados**.  Para exibir todos os outros cookies, limpe o texto do filtro.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [978059][CR978059].  

:::image type="complex" source="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png" alt-text="Limpar somente os cookies visíveis" lightbox="../../media/2021/01/application-cookies-clear-filtered-cookies.msft.png":::
   Limpar somente os cookies visíveis  
:::image-end:::  

#### <a name="new-option-to-clear-third-party-cookies-in-the-storage-pane"></a>Nova opção para limpar cookies de terceiros no painel Armazenamento  

Agora, o DevTools limpa apenas cookies de terceiros por padrão.  Para limpar somente os dados do site e os cookies de terceiros, navegue até **Aplicativo** > **Armazenamento**e escolha **Limpar dados do site**.  

Para limpar os dados do site e todos os cookies, navegue até **Aplicativo** > **Armazenamento**.  Marque a caixa de seleção ao lado de **incluir cookies de terceiros**e escolha **Limpar dados do site**.  

Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1012337][CR1012337].  

:::image type="complex" source="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png" alt-text="Opção para limpar cookies de terceiros" lightbox="../../media/2021/01/application-storage-clear-site-data-including-third-party-cookies.msft.png":::
   Opção para limpar cookies de terceiros  
:::image-end:::  

### <a name="network-tool-updates"></a>Atualizações da ferramenta de rede  

#### <a name="persist-record-network-log-setting"></a>Mantida a Configuração de Registro de log de rede   

Na versão 88 ou anterior do Microsoft Edge, o DevTools redefinia a configuração **Registro de log de rede** quando uma página da Web era atualizada.  Na versão 89 do Microsoft Edge, o DevTools agora mantem a configuração **Registro de log de rede**.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1122580][CR1122580].  

:::image type="complex" source="../../media/2021/01/network-log.msft.png" alt-text="Registrar log de rede" lightbox="../../media/2021/01/network-log.msft.png":::
   Registrar log de rede  
:::image-end:::  

#### <a name="online-option-is-now-no-throttling-option"></a>A opção Online agora chama-se Sem Limitação (No throttling)  

A opção de emulação de rede **Online** foi renomeada para **Sem Limitação**.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1028078][CR1028078].  

:::image type="complex" source="../../media/2021/01/network-no-throttling.msft.png" alt-text="Opção Sem limitação" lightbox="../../media/2021/01/network-no-throttling.msft.png":::
   Opção **Sem limitação**   
:::image-end:::  

### <a name="new-copy-options-in-the-console-tool-sources-tool-and-styles-pane"></a>Novas opções de cópia na ferramenta Console, ferramenta Fontes e no painel Estilos

#### <a name="copy-object-in-the-console-and-sources-tool"></a>Copiar objeto nas ferramentas Console e Fontes  

Agora você pode copiar valores de objeto nas ferramentas **Console** e **Fontes**.  A capacidade de copiar valores de objetos é útil ao trabalhar com objetos grandes.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [1148353][CR1148353]e [1149859][CR1149859].  

:::row:::
   :::column span="":::
      Na ferramenta **Console**, passe o mouse sobre um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar objeto**.  
   :::column-end:::
   :::column span="":::
      Na ferramenta**Fontes**, em um ponto de interrupção, passe o mouse sobre um objeto, na janela pop-up **Objeto**, realce um objeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar objeto**.  
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

#### <a name="copy-file-name-in-the-sources-tool-and-styles-pane"></a>Copiar o nome do arquivo na ferramenta Fontes e no painel Estilos  

Agora você pode copiar um nome de arquivo usando o menu contextual.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1155120][CR1155120].  

:::row:::
   :::column span="":::
      Na ferramenta **Fontes**, passe o mouse sobre um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome do arquivo**.  
   :::column-end:::
   :::column span="":::
      Na ferramenta **Elementos** > painel **Estilos**, passe o mouse sobre um nome de arquivo, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar nome do arquivo**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/sources-copy-file-name.msft.png" alt-text="Copiar nome do arquivo em Fontes" lightbox="../../media/2021/01/sources-copy-file-name.msft.png":::
         Copiar nome do arquivo em **Fontes**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/01/elements-styles-copy-file-name.msft.png" alt-text="Copiar nome do arquivo no painel Estilos" lightbox="../../media/2021/01/elements-styles-copy-file-name.msft.png":::
         Copiar nome do arquivo no painel **Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="updates-to-frame-details"></a>Atualizações nos detalhes de Quadro  

#### <a name="service-workers-information-in-frame-details"></a>Informações dos Trabalhos de Serviço nos detalhes de Quadro  

O DevTools agora lista um trabalho de serviço dedicado sob o quadro pai.  Na figura a seguir, são exibidos os detalhes do trabalho de serviço.  Para exibir os detalhes do trabalho de serviço navegue até **Aplicativo** > **Quadros** > `top` > **Trabalhos de serviços** e escolha um trabalho de serviço.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1122507][CR1122507].  

:::image type="complex" source="../../media/2021/01/application-frames-service-workers-details.msft.png" alt-text="Informações dos Trabalhos de serviço nos detalhes de Quadros" lightbox="../../media/2021/01/application-frames-service-workers-details.msft.png":::
   Informações dos **Trabalhos de Serviço** nos detalhes de **Quadros**  
:::image-end:::  

#### <a name="measure-memory-information-in-frame-details"></a>Medir informações de memória nos detalhes de Quadro  

O status `performance.measureMemory()` da API agora é exibido na seção **disponibilidade de API**.  A nova `performance.measureMemory()` da API estima o uso da memória de toda a página da Web.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema[1139899][CR1139899].  

:::image type="complex" source="../../media/2021/01/application-frames-measure-memory.msft.png" alt-text="Medir memória" lightbox="../../media/2021/01/application-frames-measure-memory.msft.png":::
   Medir memória  
:::image-end:::  

### <a name="dropped-frames-in-the-performance-tool"></a>Quadros descartados na ferramenta Desempenho  

Quando você [analisa o desempenho da carga na ferramenta Desempenho][DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance], a seção **Quadros** agora marca quadros descartados como vermelhos.  Para exibir a taxa de quadros, passe o mouse sobre um quadro descartado.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até Problema[1075865][CR1075865].  

:::image type="complex" source="../../media/2021/01/performance-frames-dropped-frames-red.msft.png" alt-text="Quadros descartados" lightbox="../../media/2021/01/performance-frames-dropped-frames-red.msft.png":::
   Quadros descartados  
:::image-end:::  

#### <a name="new-color-contrast-calculation---advanced-perceptual-contrast-algorithm-apca"></a>Novo cálculo de contraste de cor - Algoritmo Avançado de Percepção de Contraste (APCA)  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

O [Algoritmo Avançado de Percepção de Contraste (APCA)][GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml] substitui as diretrizes [AA][W3cWaiWcag21QuickrefContrastMinimum]/[AAA][W3cWaiWcag21QuickrefContrastEnhanced] de índice de contraste no [Seletor de Cor][DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker].  O APCA é uma nova maneira de calcular o contraste.  Ele se baseia na pesquisa moderna sobre a percepção de cores.  Comparada com as diretrizes de AA/AAA, a APCA depende mais do contexto.  O contraste é calculado com base nas seguintes propriedades do texto, cor e contexto.  

*   Propriedades da fonte do texto que incluem a peso e o tamanho da fonte.  
*   Propriedades da cor que incluem o contraste percebido entre o texto e o plano de fundo.  
*   Propriedades do contexto que incluem luz ambiente, arredores e objetivo pretendido.  
    
Para ativar esse experimento, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos** e marque a caixa de seleção ao lado de **Habilitar o novo APCA (Algoritmo Avançado de Percepção  Contraste), substituindo a taxa de contraste anterior e as diretrizes de AA/AAA**.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1121900][CR1121900].  

:::image type="complex" source="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png" alt-text="APCA no Seletor de Cor" lightbox="../../media/2021/01/advanced-perceptual-contrast-algorithm.msft.png":::
   APCA no Seletor de Cor  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsWhatsNew85]: ../../2020/06/devtools.md "Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsAccessibilityReferenceViewContrastRatioTextElementColorPicker]: ../../../accessibility/reference.md#view-the-contrast-ratio-of-a-text-element-in-the-color-picker "Exibir a taxa de contraste de um elemento de texto no Seletor de Cor - Referência de acessibilidade |Microsoft Docs"  
[DevtoolsCssReferenceChangeCss]: ../../../css/reference.md#change-css "Alterar CSS - Referência de CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalizar atalhos de teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenFoldablesTestFoldableDualScreenDevices]: ../../../device-mode/dual-screen-and-foldables.md#test-on-foldable-and-dual-screen-devices "Teste em dispositivos dobáveis e de tela dupla : emular dispositivos de duas telas e dobáveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular visor móvel – Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceRecordLoadPerformance]: ../../../evaluate-performance/reference.md#record-load-performance "Registrar desempenho de carga - Referência de análise de desempenho | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Visão geral das Ferramentas para Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsInspectStylesEditFonts]: ../../../inspect-styles/edit-fonts.md "Editar configurações e estilos de fonte CSS no painel Estilos no DevTools | Microsoft Docs"  

[DualScreenIntroductionHowToWorkWithSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a junção – Introdução aos dispositivos de duas telas | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Recurso de abrangência de tela de mídia CSS para detecção de dualidade de tela | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de duas telas | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesWhatsNew89TargetCssDemoHtmlSection1]: https://microsoftedge.github.io/DevToolsSamples/whats-new/89/target-css-demo.html#section-1 "Seção 1 - demonstração do CSS :target para Novidades do DevTools (Microsoft Edge 89) | GitHub"  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull229]: https://github.com/microsoft/vscode-edge-devtools/pull/229 "Pull 229: implementando o menu suspenso em configurações para alterar os temas | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull233]: https://github.com/microsoft/vscode-edge-devtools/pull/233 "Pull 233: incluindo o Depurador do Microsoft Edge como uma dependência| GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull235]: https://github.com/microsoft/vscode-edge-devtools/pull/235 "Pull 235: atualizando a versão do Microsoft Edge DevTools para 85.0.564.40 | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsPull248]: https://github.com/microsoft/vscode-edge-devtools/pull/248 "Pull 248: Adicionar botões de fechamento único ao painel de instâncias | GitHub"  
[GithubW3cSilverGuidelinesMethodsMethodFontCharacteristicContrastHtml]: https://w3c.github.io/silver/guidelines/methods/Method-font-characteristic-contrast.html "Selecione as características da fonte e as cores de plano de fundo para fornecer contraste suficiente para facilitar a leitura | W3C"  
[GithubW3cWebappsecTrustedTypesDistSpec]: https://w3c.github.io/webappsec-trusted-types/dist/spec  "Tipos Confiáveis | W3C"  

[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Novo Surface Duo | Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace de Extensões | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  
[VisualstudioMarketplaceMsjsdiagDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador do Microsoft Edge | Visual Studio Marketplace"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR978059]: https://crbug.com/978059 "Problema 978059: excluindo cookies durante a filtragem deles, excluir todos os cookies e não apenas os filtrados | Bugs do Chromium"  
[CR997625]: https://crbug.com/997625 "Problema 997625: solicitação de novo recurso | é necessária uma opção para ver o valor de URL decodificado nos cookies | Bugs do Chromium"  
[CR1003629]: https://crbug.com/1003629 "Problema 1003629: recurso Capturar Nó não faz mais a captura de tela do nó abaixo da dobra. | Bugs do Chromium"  
[CR1012337]: https://crbug.com/1012337 "Problema 1012337: recurso Limpar os dados do site destruirá a sessão do Google em sites que não são do Google | Bugs do Chromium"  
[CR1028078]: https://crbug.com/1028078 "Problema 1028078: colocar Online e Offline próximos um do outro na lista | Bugs do Chromium"  
[CR1054281]: https://crbug.com/1054281 "Problema 1054281: solicitação de recurso: o DevTools deve emular dispositivos dobráveis e de duas telas | Bugs do Chromium"  
[CR1075865]: https://crbug.com/1075865 "Problema 1075865: mostrar quadros descartados na linha do tempo do Devtools | Bugs do Chromium"  
[CR1093229]: https://crbug.com/1093229 "Problema 1093229: DevTools: oferecer uma interface de usuário de editor de face de tipos especializada | Bugs do Chromium"  
[CR1121900]: https://crbug.com/1121900 "Problema 1121900: DevTools: atualizar lógica de cálculo de contraste por nova especificação | Bugs do Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o worker do Surface no modo de exibição árvore de quadros | Bugs do Chromium"  
[CR1122580]: https://crbug.com/1122580 "Problema 1122580: é impossível desabilitar a gravação de rede ao recarregar | Bugs do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramentas Flexbox | Bugs de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros do Chromium"  
[CR1139949]: https://crbug.com/1139949 "Problema 1139949: sobreposição de Flexbox | Bugs do Chromium"  
[CR1147016]: https://crbug.com/1147016 "Problema 1147016: o seletor de cor não é exibido na função var(). | Bugs do Chromium"  
[CR1148353]: https://crbug.com/1148353 "Problema 1148353: solicitação de recurso: copiar objeto do console do Devtools | Bugs do Chromium"  
[CR1149859]: https://crbug.com/1149859 "Problema 1149859: [solicitação de recurso][Console] adicionar copiar objeto ao item da área de transferência no menu contextual | Bugs do Chromium"  
[CR1150797]: https://crbug.com/1150797 "Problema 1150797: adicionar Duplicar elemento ao menu contextual no painel Elemento | Bugs do Chromium"  
[CR1152391]: https://crbug.com/1152391 "Problema 1152391: suporte para copiar o menu de contexto CSS no painel estilos | Bugs do Chromium"  
[CR1155120]: https://crbug.com/1155120 "Problema 1155120: [FR]Suporte para copiar nome do arquivo e número de linha | Bugs do Chromium"  
[CR1156628]: https://crbug.com/1156628 "Problema 1156628: DevTools: adicionar suporte ao elemento :target no recurso forçar estado do elemento | Bugs do Chromium"  
[CR1157329]: https://crbug.com/1157329 "Problema 1157329: Acessibilidade – Narrador: o Narrador não está anunciando a contagem e a posição para sugestões de código disponíveis na guia Estilos | Bugs do Chromium"  

[MdnDocsWebCssTarget]: https://developer.mozilla.org/docs/web/css/:target ":target | MDN"  

[SamsungUsMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[W3cWaiWcag21QuickrefContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref#contrast-enhanced "Contraste (aprimorado) - Como atender a WCAG (Referência Rápida) | W3c"  
[W3cWaiWcag21QuickrefContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref#contrast-minimum "Contraste (mínimo) - Como atender a WCAG (Referência Rápida) | W3c"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-89) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen

[SpanningPlaceholder]: link-t-b-d "Espaços reservados de abrangência"  
