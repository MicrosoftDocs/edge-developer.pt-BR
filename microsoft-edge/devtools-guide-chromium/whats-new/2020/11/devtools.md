---
description: Microsoft Edge no Linux, webhints aperfeiçoadas na ferramenta Issues, novos recursos de depuração de trabalho do serviço e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: a63515060d989a84838e4a9ba7f803184a3fc91f
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514372"
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
# <a name="whats-new-in-devtools-microsoft-edge-88"></a>O que há de novo no DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="microsoft-edge-and-microsoft-edge-driver-now-available-on-linux"></a>O Microsoft Edge e o Microsoft Edge Driver agora estão disponíveis no Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

O Microsoft Edge Dev agora é compatível com o Ubuntu, o Debian, o Fedora e as distribuições do openSUSE.  Baixe e instale o pacote `.deb`ou `.rpm` do Microsoft Edge Dev diretamente do site [Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou use as ferramentas de gerenciamento de pacote padrão de sua distribuição Linux.  

Se você estiver usando um ambiente Linux em suas soluções de integração e entrega contínuas (CI/CD\), o Microsoft Edge Driver também está disponível no Linux.  Para começar a automatizar o Microsoft Edge Dev com o Microsoft Edge Driver, navegue até a [página de downloads do Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Para obter ajuda com a automação do Microsoft Edge Dev junto com o Microsoft Edge Driver, navegue até [Usar WebDriver (Chromium) para automação de teste][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools no Microsoft Edge no Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools no Microsoft Edge no Linux  
:::image-end:::  

## <a name="improved-webhint-and-platform-tips-in-the-issues-tool"></a>Dica da web e plataforma aprimoradas na ferramenta Issues  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Uma ferramenta de código-fonte aberto, [webhint][WebhintMain], fornece comentários em tempo real para sites e páginas da Web locais.  A partir do [Microsoft Edge versão 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], reveja comentários de webhint na ferramenta [Issues][DevtoolsIssuesIndex].  Os problemas que aparecem na ferramenta **Issues** agora estão mais fáceis de serem analisados com a adição das categorias a seguir.  

*   [Acessibilidade][WebhintUserGuideHintsAccessibility]  
*   [Compatibilidade][WebhintUserGuideHintsCompatibility]  
*   [Desempenho][WebhintUserGuideHintsPerformance]  
*   [Armadilhas][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Segurança][WebhintUserGuideHintsSecurity]  
    
Agora você pode filtrar problemas de terceiros usando uma nova caixa de seleção.  A funcionalidade de filtro ajuda você a ocultar problemas relacionados ao código de bibliotecas de terceiros ou de outras fontes.  

Para ajudá-lo a revisar os problemas revelados pela [webhint][WebhintMain], a ferramenta **Problemas** agora exibe as informações a seguir.  

*   Trechos de código aprimorados.  
*   Links para outros painéis relevantes.  
*   Links para a documentação para ajudá-lo a corrigir problemas no seu website.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Ferramenta Issues" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Ferramenta **Issues**  
:::image-end:::  

## <a name="composited-layers-are-now-in-3d-view"></a>Camadas Compostas agora estão no modo de exibição 3D  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Agora você pode visualizar o conteúdo das **Camadas** juntamente com os valores de índice z e o Modelo de Objeto do Documento \(DOM\).  Esse recurso ajuda você a depurar sem alternar entre as ferramentas[exibição 3D][Devtools3dViewIndex] e **Camadas** com frequência.  Para uma experiência de depuração visual abrangente, o [Modo de exibição 3D e as camadas compostas agora são combinados][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Painel de **Camadas Compostas**  
:::image-end:::  

## <a name="css-variable-definitions-in-styles-pane"></a>Definições de variáveis CSS no painel Estilos  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

No painel **Estilos**, as [variáveis CSS][MdnUsingCssCustomProperties] agora se vinculam diretamente a cada definição.  Escolha a variável para exibir ou alterar facilmente a definição da variável CSS.  No exemplo, DevTools exibe os atributos CSS do elemento`body`.  Para exibir a definição de variável para a `--theme-body-background` variável CSS, conclua as ações a seguir.  

1.  No painel **Estilos**, escolha `var(--theme-body-background)`.  
1.  O painel **estilos** agora exibe a definição da `--theme-body-background` variável CSS.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variável CSS vinculada ao estilo" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Variável CSS vinculada ao estilo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variável CSS vinculada ao destino do estilo" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Variável CSS vinculada ao destino do estilo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="service-worker-debugging-improvements"></a>Melhorias na depuração do trabalho do serviço  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Os novos recursos a seguir nas ferramentas [Rede](#network-tool), [Aplicativo](#application-tool)e [Fontes](#sources-tool) ajudam você a criar seu [PWA][ProgressiveWebAppsIndex].  Use os recursos a seguir quando tiver dificuldades para depurar o Trabalho de Serviço.  

O roteamento de solicitação exibe os eventos `startup` e os eventos `fetch` com base nas solicitações de rede executadas por meio de Trabalho de Serviço.  As linhas do tempo são acessadas a partir da ferramenta **Aplicativo** ou **Rede**.  Os cronogramas ajudam quando você está tendo problemas com trabalhadores de serviço e deseja exibir se algo está errado com o evento `startup` ou `fetch`.  

### <a name="application-tool"></a>Ferramenta aplicativo  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Exibir todas as informações de roteamento de solicitação de trabalho do serviço com o novo link**Solicitações de rede**.  Para exibir um contexto adicional durante a depuração do trabalho do serviço, conclua as ações a seguir.  

1.  Navegue até **Aplicativo**  >  **Trabalho de Serviço**.  
1.  Escolha **Solicitações de rede**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abra a ferramenta de rede no painel de Trabalho de Serviço" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Abra a ferramenta **Rede** no painel **Trabalho de Serviço**
    :::image-end:::  
    
1.  A ferramenta **Rede** é aberta na **gaveta** e exibe todas as solicitações de rede relacionadas ao Trabalho de Serviço.  As solicitações de rede são filtradas usando `is:service-worker-intercepted`.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Ferramenta Rede na gaveta" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Ferramenta **Rede** na **gaveta**  
    :::image-end:::
    
1. Para retornar à ferramenta **Rede** para o painel superior, feche a **Gaveta**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Feche a gaveta para retornar à ferramenta Rede" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Feche a **gaveta** para retornar à ferramenta **Rede**  
    :::image-end:::  
    
### <a name="network-tool"></a>Ferramenta Rede  

Depure solicitações de rede executadas por meio de trabalho de serviço.  Você também pode abrir solicitações de rede na ferramenta **Aplicativo**.  Para cada solicitação, DevTools exibe as informações a seguir no painel [Tempo][DevtoolsNetworkReferenceViewTimingBreakdownRequest].  

*   O início de uma solicitação e a duração da inicialização.  
*   Alterações no registro de trabalho de serviço.  
*   O tempo de execução de um manipulador de eventos `fetch`.  
*   O tempo de execução de todos os eventos `fetch` para carregar um cliente.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Painel Tempo" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Painel **Tempo**  
:::image-end:::  

### <a name="sources-tool"></a>Ferramenta Fontes  

Em versões anteriores do Microsoft Edge, o nível de profundidade na pilha de chamadas era limitado ao código JavaScript no seu trabalho de serviço.  No Microsoft Edge 88, a pilha de chamadas agora exibe o iniciador de solicitações que são executadas por meio do seu trabalho de serviço.  

Para localizar o iniciador da solicitação, use a pilha de chamadas do seu código JavaScript no trabalho de serviço.  A pilha de chamadas nas figuras a seguir começa com o código JavaScript em seu trabalho de serviço e exibe uma referência à solicitação de página da Web original como `(index):157`.  Na segunda figura, a referência é escolhida e abre o iniciador que fez a solicitação.  O iniciador na segunda figura é a página da Web.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="O arquivo service-worker.js e a pilha de chamadas que destacam o remetente da solicitação" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         O arquivo `service-worker.js` e a pilha de chamadas que destacam o remetente da solicitação  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="A página da Web (índice) é o iniciador da solicitação" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         A página da Web `(index)` é o iniciador da solicitação  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="copy-property-value-of-a-network-request"></a>Copiar o valor da propriedade de uma solicitação de rede  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

Na ferramenta **Rede**, copie o valor da propriedade de uma solicitação de rede usando a opção nova **Valor de cópia**.  O valor da propriedade é copiado como um valor JSON decodificado.  Em versões anteriores do Microsoft Edge, você precisava copiar um valor usando uma das ações a seguir.  

*   Realce o texto inteiro e copie-o.  
*   Armazene o valor como variável global, conforme aplicável, e copie-o do [Console][DevtoolsConsoleIndex]do Devtools.  
    
Para copiar o valor da propriedade para a área de transferência, navegue até [Copiar resposta formatada JSON para a área de transferência][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar valor da propriedade em DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Copiar valor da propriedade em DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Colar o valor da propriedade no Microsoft Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Colar o valor da propriedade no Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="customize-multi-press-keyboard-shortcuts"></a>Personalizar atalhos de teclado com várias prensas  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Desde a versão 87 do Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], você pode personalizar os atalhos de teclado para qualquer ação no DevTools.  No Microsoft Edge versão 88, agora você pode criar atalhos de teclado com várias prensas.  Para definir um atalho para uma ação no DevTools, navegue até [Configurações][DevtoolsCustomizeIndexSettings] > **Experimentos** e escolha a caixa de seleção ao lado de **Habilitar o editor de atalhos de teclado**.  Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Por exemplo, o realce vermelho exibe um atalho de teclado personalizado com várias prensas para a ação **Iniciar gravação de eventos**.  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o [Issue #174309][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Atalhos de teclado de corda" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Atalhos de teclado com várias prensas  
:::image-end:::  

## <a name="devtools-now-match-browser-language"></a>O DevTools agora corresponde ao idioma do navegador  

No Microsoft Edge versão 87, se você ativou a configuração de **idioma do navegador correspondente** nas [configurações do DevTools][DevtoolsCustomizeIndexSettings], o DevTools não correspondia ao idioma do navegador.  No Microsoft Edge versão 88, o DevTools agora corresponde ao idioma do navegador se você ativar a configuração de **Idioma do navegador correspondente**.  Para obter mais informações sobre a configuração **corresponder ao idioma do navegador** do DevTools, navegue até [Alterar as configurações de idioma do DevTools][DevtoolsCustomizeLocalization].  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Corresponder a configuração DevTools ao idioma do navegador em japonês" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   Configuração **Corresponder ao idioma do navegador** em Japonês  
:::image-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-css-angle-visualization-tools"></a>Novas ferramentas de visualização do ângulo CSS  

O DevTools agora tem melhor suporte para depuração de ângulos CSS.  Quando um elemento HTML na sua página tem ângulo CSS aplicado a ele, um ícone de relógio é exibido ao lado do ângulo na ferramenta **Estilos**.  Para alternar a sobreposição do relógio, escolha o ícone do relógio.  Para alterar o ângulo, escolha qualquer lugar no relógio ou arraste a agulha.  Para alterar o valor do ângulo, você também pode usar atalhos de teclado e mouse.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [1126178][CR1126178] e [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

O ângulo CSS a seguir é usado para o exemplo.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ângulo de CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Ângulo de CSS  
:::image-end:::  

### <a name="simulate-storage-quota-size-in-the-storage-pane"></a>Simule o tamanho da cota de armazenamento no painel Armazenamento  

Agora você pode substituir o tamanho da cota de armazenamento no painel **Armazenamento**.  Esse recurso permite simular diferentes dispositivos e testar o comportamento de seu site ou aplicativo em cenários de baixa disponibilidade de disco.  Para simular a cota de armazenamento, conclua as ações a seguir.  

1.  Navegue até o **Aplicativo**  >  **Armazenamento**.  
1.  Ative a caixa de seleção **Simular cota de armazenamento personalizada**.  
1.  Digite um número válido.  
    
Para obter mais informações sobre como emular dispositivos móveis e outros recursos no DevTools, navegue para [Emular dispositivos móveis no DevTools do Microsoft Edge][DevtoolsDeviceModeIndex].  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [945786][CR945786] e [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular o tamanho da cota de armazenamento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simular o tamanho da cota de armazenamento  
:::image-end:::  

### <a name="report-cors-errors-in-the-network-tool"></a>Relatar erros CORS na ferramenta Rede  

Experimente este recurso ao navegar até a [demonstração de erro CORS][GlitchCorsErrors].  Abra a ferramenta de **Rede**, atualize a página e observe a solicitação de rede CORS com falha.  A coluna status exibe o **erro CORS**.  Quando você focaliza o erro, a dica de ferramenta agora exibe o código de erro.  No Microsoft Edge versão 87 e anterior, o DevTools só exibia o status genérico **(com falha)** para erros CORS.  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erros CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Erros CORS  
:::image-end:::  

### <a name="frame-details-view-updates"></a>Atualizações da exibição de detalhes do quadro  

#### <a name="cross-origin-isolation-information-in-the-frame-details-view"></a>Informações de isolamento de origem cruzada na visualização de detalhes do quadro  

O status isolado de origem cruzada agora é exibido na seção **Isolamento e Segurança**.  A nova seção **disponibilidade da API** exibe a disponibilidade de `SharedArrayBuffer`s\ (SAB\) e se os buffers podem ser compartilhados usando `postMessage()`.  Um aviso de substituição será exibido se o SAB e `postMessage()` estiverem disponíveis no momento, mas o contexto não estiver isolado na origem.  Para obter mais informações sobre o isolamento entre origens e por que é necessário para recursos como `SharedArrayBuffers`, navegue até [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informações entre origens" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Informações entre origens  
:::image-end:::  

#### <a name="new-web-workers-information-in-the-frame-details-view"></a>Novas informações de Trabalhos na Web na visualização de detalhes do quadro  

O DevTools agora organiza os Trabalhadores da Web no quadro pai relevante.  Por exemplo, se o `someName`quadro criar `worker.js`, `worker.js` aparecerá abaixo `someName` na lista **Quadros**.  Para exibir os detalhes do trabalho da web, conclua as ações a seguir.  

1.  Abra a ferramenta **Aplicativo**.  
1.  Expanda um quadro que contém trabalhos da web.  
1.  Expanda a árvore **Trabalhos**.  
1.  Escolha um trabalho.  
    
Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [1122507][CR1122507] e [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informações de trabalho da web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Informações de trabalho da web  
:::image-end:::  

#### <a name="display-opener-frame-details-for-opened-windows"></a>Exibir detalhes do quadro aberto para janelas abertas  

O DevTools agora organiza [Janelas][MdnWindowConstructors] abertas sob o [quadro][MdnWindowFrames]pai relevante.  Por exemplo, se o `top`quadro abrir uma`Window` para `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, o botão `Window` aparecerá abaixo `top` na lista **Quadros**.  

Para revelar o quadro responsável pela abertura de outra janela na ferramenta **Elementos**, conclua as ações a seguir.  

1.  Abra a árvore **Quadros**.  
1.  Expanda **Janelas Abertas** e escolha `Window` para o quadro pai que você deseja saber.  
1.  Escolha o link do**Quadro Aberto**.  

Os detalhes são exibidos sobre qual quadro causou a abertura do outro `Window`.  Para revelar o abridor na ferramenta **Elementos**, conclua as ações a seguir.  

1.  Abra a árvore **Quadros**.  
1.  Escolha uma janela aberta para abrir os detalhes `Window`.  
1.  Escolha o link do**Quadro Aberto**.  
    
Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalhes do quadro aberto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Detalhes do quadro aberto  
:::image-end:::  

### <a name="copy-stacktrace-for-network-initiator"></a>Copiar StackTrace para o iniciador de rede  

Para copiar o StackTrace para a área de transferência, conclua as ações a seguir.  

1.  Abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Copiar**  >  **Copiar StackTrace**.  
    
Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Copiar StackTrace  
:::image-end:::  

### <a name="preview-wasm-variable-value-on-mouseover"></a>Visualize o valor da variável Wasm ao passar o mouse  

Use esse recurso para analisar o valor de uma variável Webassembly \(Wasm\) quando o código for pausado.  Para exibir o valor atual de uma variável, passe o mouse sobre uma variável.  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até Issues [1058836][CR1058836] e [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Variável de visualização do Wasm ao passar o mouse" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Variável de visualização do Wasm ao passar o mouse  
:::image-end:::  

### <a name="consistent-units-of-measurement-for-sizes-of-files-and-memory"></a>Unidades de medida consistentes para tamanhos de arquivos e memória  

O DevTools agora usa consistentemente `kB` para exibir tamanhos de arquivos e memória.  Anteriormente, o DevTools mesclava `kB` e `KiB`.

*   `kB` ou quilobyte \(10^3 ou 1000 bytes\)  
*   `KiB` ou kibibyte \(2^10 ou 1024 bytes \)  
    
Por exemplo, a ferramenta **Rede** anteriormente usada `kB` em rótulos, mas agora usada `KiB` em cálculos.  Seus comentários mostraram que essa inconsistência causou confusão.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1035309][CR1035309].  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Modo de exibição 3D | Microsoft Docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Visão geral do console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Alterar configurações de idioma do DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado -Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Ativar camadas compostas no modo de exibição 3D – recursos experimentais | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar resposta formatada JSON para a área de transferência - Referência de análise da rede | Microsoft Docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Exibir a divisão de tempo de uma solicitação - Referência de análise de rede | Microsoft Docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Use o WebDriver (Chromium) para automação de teste | Microsoft Docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Microsoft Docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: ../10/devtools.md#customize-keyboard-shortcuts-in-settings "Personalizar atalhos de teclado em configurações – Novidades do DevTools (Microsoft Edge 87) | Microsoft Docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: ../06/devtools.md#webhint-feedback-in-the-issues-panel "comentários de webhint no painel Issues-novidades do DevTools (Microsoft Edge 85) | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixar o WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Erros de Chromium"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir a substituição de navigator.storage.estimate() | Erros do Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: Reduzir a sobrecarga de desempenho do despacho de mensagens de protocolo no front-end | Erros do Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools deve usar consistentemente MB para significar megabyte, não mebibyte | Erros do Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools | Erros do Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: problemas com o UX na depuração Wasm| Erros do Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ experiência do desenvolvedor básico do WASM | Erros do Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: exibir informações sobre quadros gerados por 'window.open()' na árvore de quadros | Erros do Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o trabalho da superfície no modo de exibição árvore de quadros | Erros do Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: CSS <type> components Erros do Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: testar fallbacks de imagem (emulação) | Erros do Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: não há uma maneira fácil de copiar a carga de solicitação JSON | Erros do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramenta Flexbox | Erros de Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: o componente CSS <angle> deve refletir a aparência de sua propriedade residente no fundo do relógio | Erros do Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: o iniciador de rede deve oferecer a capacidade de copiar o rastreamento de pilha | Erros do Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros do Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: ícones para propriedades CSS do flexbox no painel Estilos | Erros do Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: melhorar o relatório de erros CORS no DevTools | Erros do Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: adicionar adornos de estilo flexível à árvore de elementos | Erros de Chromium"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: o texto limpo ainda é visto na caixa de texto da seção 'Armazenamento' da janela 'Ferramentas de Desenvolvimento' | Erros do Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erros CORS | Falha"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Compartilhamento de recurso entre origens (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propriedades personalizadas CSS (variáveis) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Construtores - Janela | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Acessibilidade | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidade | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Desempenho | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Armadilhas | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Segurança | webhint"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-88) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
