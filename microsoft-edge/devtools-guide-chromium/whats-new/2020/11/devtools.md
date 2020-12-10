---
description: Microsoft Edge no Linux, dicas da WebDicas aperfeiçoadas na ferramenta problemas, novos recursos de depuração de trabalho do serviço e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205240"
---
# O que há de novo no DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## O Microsoft Edge e o Microsoft Edge driver agora estão disponíveis no Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

O Microsoft Edge dev agora é compatível com o Ubuntu, o Debian, o Fedora e as distribuições do openSUSE.  Baixe e instale o `.deb` pacote ou o encapsulamento do Microsoft Edge `.rpm` diretamente do [site do Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] ou use as ferramentas de gerenciamento de pacotes padrão da sua distribuição Linux.  

Se você estiver usando um ambiente Linux em suas soluções de integração contínua e distribuição \ (CI/CD \), o driver do Microsoft Edge também estará disponível no Linux.  Para começar a automatizar o Microsoft Edge dev com o Microsoft Edge Driver, acesse a [página de downloads do driver Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Para obter ajuda com a automação de desenvolvimento do Microsoft Edge juntamente com o Microsoft Edge Driver, navegue para [usar o WebDriver (Chromium) para automação de teste][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools no Microsoft Edge no Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools no Microsoft Edge no Linux  
:::image-end:::  

## Dicas da webdica e plataforma aprimoradas na ferramenta problemas  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Uma ferramenta de código-fonte aberto, [webhint][WebhintMain], fornece comentários em tempo real para sites e páginas da Web locais.  Começando com o [Microsoft Edge versão 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], reveja comentários do webhint na ferramenta [problemas][DevtoolsIssuesIndex] .  Os problemas que aparecem na ferramenta **problemas** agora são mais fáceis de serem analisados com a adição das categorias a seguir.  

*   [Acessibilidade][WebhintUserGuideHintsAccessibility]  
*   [Compatibilidade][WebhintUserGuideHintsCompatibility]  
*   [Desempenho][WebhintUserGuideHintsPerformance]  
*   [Armadilhas][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Segurança][WebhintUserGuideHintsSecurity]  
    
Agora você pode filtrar problemas de terceiros usando uma nova caixa de seleção.  A funcionalidade de filtro ajuda você a ocultar problemas relacionados ao código de bibliotecas de terceiros ou de outras fontes.  

Para ajudá-lo a revisar os problemas revelados pela [webhint][WebhintMain], a ferramenta **problemas** agora exibe as informações a seguir.  

*   Trechos de código aprimorados.  
*   Links para outros painéis relevantes.  
*   Links para a documentação para ajudá-lo a corrigir problemas no seu website.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Ferramenta de problemas" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Ferramenta de **problemas**  
:::image-end:::  

## Camadas compostas agora estão no modo de exibição 3D  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

Agora você pode visualizar o conteúdo das **camadas** juntamente com os valores de índice z e o modelo de objeto do documento \ (dom \).  Esse recurso ajuda você a depurar sem alternar entre as ferramentas de [exibição 3D][Devtools3dViewIndex] e **camadas** com frequência.  Para uma experiência de depuração Visual abrangente, o [modo de exibição 3D e as camadas compostas agora são combinados][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Painel de camadas compostas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Painel de **camadas compostas**  
:::image-end:::  

## Definições de variáveis CSS no painel estilos  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

No painel **estilos** , as [variáveis CSS][MdnUsingCssCustomProperties] agora se vinculam diretamente a cada definição.  Escolha a variável para exibir ou alterar facilmente a definição da variável CSS.  No exemplo, DevTools exibe os atributos CSS do `body` elemento.  Para exibir a definição de variável para a `--theme-body-background` variável CSS, conclua as ações a seguir.  

1.  No painel **estilos** , escolha `var(--theme-body-background)` .  
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

## Melhorias na depuração do trabalho do serviço  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Os novos recursos a seguir nas ferramentas de [rede](#network-tool), [aplicativo](#application-tool)e [fontes](#sources-tool) ajudam você a criar seu [PWA][ProgressiveWebAppsChromiumIndex].  Use os recursos a seguir quando tiver dificuldades para depurar o trabalhador do serviço.  

O roteamento de solicitação exibe os `startup` eventos e os `fetch` eventos com base nas solicitações de rede executadas por meio de trabalhadores do serviço.  As linhas do tempo são acessadas a partir da ferramenta **aplicativo** ou **rede** .  Os cronogramas ajudam quando você está tendo problemas com trabalhadores de serviço e deseja ver se algo está errado com o `startup` evento ou `fetch` .  

### Ferramenta do aplicativo  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Exibir todas as informações de roteamento de solicitação de trabalho do serviço com o novo link de **solicitações de rede** .  Para exibir um contexto adicional durante a depuração do trabalho do serviço, conclua as ações a seguir.  

1.  Navegue até ****  >  **trabalhadores do serviço**de aplicativo.  
1.  Escolha **solicitações de rede**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abrir a ferramenta de rede no painel de trabalhadores do serviço" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Abrir a ferramenta de **rede** no painel de **trabalhadores do serviço**
    :::image-end:::  
    
1.  A ferramenta **rede** é aberta na **gaveta** e exibe todas as solicitações de rede relacionadas ao trabalhador do serviço.  As solicitações de rede são filtradas usando `is:service-worker-intercepted` .  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Ferramenta de rede na gaveta" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Ferramenta de **rede** na **gaveta**  
    :::image-end:::
    
1. Para retornar a ferramenta de **rede** para o painel superior, feche a **gaveta**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Fechar a ferramenta gaveta para retornar a rede" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Fechar a ferramenta **gaveta** para retornar a **rede**  
    :::image-end:::  
    
### Ferramenta de rede  

Depurar solicitações de rede executadas por meio de trabalhadores de serviço.  Você também pode abrir solicitações de rede na ferramenta do **aplicativo** .  Para cada solicitação, DevTools exibir as informações a seguir no painel [intervalo][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .  

*   O início de uma solicitação e duração da inicialização.  
*   Alterações no registro de trabalho do serviço.  
*   O tempo de execução de um `fetch` manipulador de eventos.  
*   O tempo de execução de todos os `fetch` eventos para carregar um cliente.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Painel de intervalo" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Painel de **intervalo**  
:::image-end:::  

### Ferramenta fontes  

Em versões anteriores do Microsoft Edge, o nível de profundidade na pilha de chamadas era limitado ao código JavaScript no seu trabalhador do serviço.  No Microsoft Edge 88, a pilha de chamadas agora exibe o iniciador de solicitações que são executadas por meio do trabalho do serviço.  

Para localizar o iniciador da solicitação, use a pilha de chamadas do seu código JavaScript no trabalhador do serviço.  A pilha de chamadas nas figuras a seguir começa com o código JavaScript em seu trabalhador do serviço e exibe uma referência à solicitação de página da Web original como `(index):157` .  Na segunda figura, a referência é escolhida e o iniciador que fez a solicitação foi aberto.  O iniciador na segunda figura é a página da Web.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="O arquivo service-worker.js e a pilha de chamadas que destacam o remetente da solicitação" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         O `service-worker.js` remetente da solicitação de realce de arquivo e chamada  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="A página da Web (índice) é o iniciador da solicitação" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         A `(index)` página da Web é o iniciador da solicitação  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Copiar o valor da propriedade de uma solicitação de rede  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

Na ferramenta **rede** , copie o valor da propriedade de uma solicitação de rede usando a opção novo **valor de cópia** .  O valor da propriedade é copiado como um valor JSON decodificado.  Em versões anteriores do Microsoft Edge, você precisava copiar um valor usando uma das ações a seguir.  

*   Realce o texto inteiro e copie-o.  
*   Armazene o valor como variável global, conforme aplicável, e copie-o do [console][DevtoolsConsoleIndex]do devtools.  
    
Para copiar o valor da propriedade para a área de transferência, navegue até [copiar resposta formatada JSON para a área de transferência][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar valor da propriedade em DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Copiar valor da propriedade em DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Colar valor da propriedade no código do Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Colar valor da propriedade no código do Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Personalizar atalhos de teclado com várias prensas  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Desde a versão 87 do Microsoft Edge][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], você pode personalizar os atalhos de teclado para qualquer ação no devtools.  No Microsoft Edge versão 88, agora você pode criar atalhos de teclado com várias prensas.  Para definir um atalho para uma ação no devtools, navegue até experiências de [configurações][DevtoolsCustomizeIndexSettings]  >  **** e escolha a caixa de seleção ao lado de **habilitar o editor de atalhos de teclado**.  Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Por exemplo, o realce vermelho exibe um atalho de teclado com várias prensas personalizado para a ação **Iniciar gravação de eventos** .  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o [Issue #174309][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Atalhos de teclado de corda" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Atalhos de teclado com várias prensas  
:::image-end:::  

## Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Novas ferramentas de visualização do ângulo CSS  

O DevTools agora tem melhor suporte para depuração de ângulo CSS.  Quando um elemento HTML na sua página tem ângulo CSS aplicado a ele, um ícone de relógio é exibido ao lado do ângulo na ferramenta **estilos** .  Para alternar a sobreposição do relógio, escolha o ícone do relógio.  Para alterar o ângulo, escolha qualquer lugar no relógio ou arraste a agulha.  Para alterar o valor do ângulo, você também pode usar atalhos de teclado e mouse.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [1126178][CR1126178] e [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

O ângulo CSS a seguir é usado para o exemplo.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ângulo de CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Ângulo de CSS  
:::image-end:::  

### Simular o tamanho da cota de armazenamento no painel armazenamento  

Agora você pode substituir o tamanho da cota de armazenamento no painel **armazenamento** .  Esse recurso permite simular diferentes dispositivos e testar o comportamento de seu site ou aplicativo em cenários de baixa disponibilidade de disco.  Para simular a cota de armazenamento, conclua as ações a seguir.  

1.  Navegue até ****  >  **armazenamento**do aplicativo.  
1.  Ative a caixa de seleção **simular cota de armazenamento personalizada** .  
1.  Digite um número válido.  
    
Para obter mais informações sobre como emular dispositivos móveis e outros recursos no DevTools, navegue para [emular dispositivos móveis no Microsoft Edge devtools ][DevtoolsDeviceModeIndex].  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [945786][CR945786] e [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular o tamanho da cota de armazenamento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simular o tamanho da cota de armazenamento  
:::image-end:::  

### Relatar erros CORS na ferramenta rede  

Experimente este recurso ao navegar até a [demonstração de erro CORS][GlitchCorsErrors].  Abra a ferramenta de **rede** , atualize a página e observe a solicitação de rede CORS com falha.  A coluna status exibe o **erro CORS**.  Quando você focaliza o erro, a dica de ferramenta agora exibe o código de erro.  No Microsoft Edge versão 87 e anterior, DevTools só exibiu status genérico **(com falha)** para erros CORS.  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Erros CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Erros CORS  
:::image-end:::  

### Atualizações da exibição de detalhes do quadro  

#### Informações de isolamento entre origens na exibição de detalhes do quadro  

O status isolado de origem cruzada agora é exibido na seção **isolamento de segurança &** .  A nova seção **disponibilidade da API** exibe a disponibilidade de `SharedArrayBuffer` s \ (sab \) e se os buffers podem ser compartilhados usando `postMessage()` .  Um aviso de substituição será exibido se o SAB e `postMessage()` estiver disponível no momento, mas o contexto não estiver isolado na origem.  Para obter mais informações sobre o isolamento entre origens e por que é necessário para recursos como `SharedArrayBuffers` , navegue até [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Informações entre origens" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Informações entre origens  
:::image-end:::  

#### Novas informações de funcionários da Web na exibição detalhes do quadro  

O DevTools agora organiza os funcionários da Web no quadro pai relevante.  Por exemplo, se o `someName` quadro criar `worker.js` , `worker.js` aparecerá abaixo `someName` na lista de **quadros** .  Para exibir os detalhes do Web Worker, conclua as ações a seguir.  

1.  Ferramenta abrir **aplicativo** .  
1.  Expanda um quadro que contém funcionários da Web.  
1.  Expanda a árvore **funcionários** .  
1.  Escolha um trabalhador.  
    
Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [1122507][CR1122507] e [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Informações de funcionários da Web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Informações de funcionários da Web  
:::image-end:::  

#### Exibir detalhes do quadro aberto para janelas abertas  

O DevTools agora organiza [janelas][MdnWindowConstructors] abertas sob o [quadro][MdnWindowFrames]pai relevante.  Por exemplo, se o `top` quadro abrir uma `Window` a para `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , o botão `Window` aparecerá abaixo `top` na lista de **quadros** .  

Para revelar o quadro responsável pela abertura de outra janela na ferramenta **elementos** , conclua as ações a seguir.  

1.  Abra a árvore de **quadros** .  
1.  Expanda **janelas abertas** e escolha o `Window` para o quadro pai que você deseja saber.  
1.  Escolha o link de **quadro aberto** .  

Os detalhes são exibidos sobre qual quadro causou a abertura de outro `Window` .  Para revelar o abredor na ferramenta **elementos** , conclua as ações a seguir.  

1.  Abra a árvore de **quadros** .  
1.  Escolha uma janela aberta para abrir os `Window` detalhes.  
1.  Escolha o link de **quadro aberto** .  
    
Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalhes do quadro aberto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Detalhes do quadro aberto  
:::image-end:::  

### Copiar StackTrace para o iniciador de rede  

Para copiar o StackTrace para a área de transferência, conclua as ações a seguir.  

1.  Abra o menu contextual \ (clique com o botão direito do mouse \).  
1.  Escolha **copiar**  >  **StackTrace de cópia**.  
    
Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Copiar StackTrace  
:::image-end:::  

### Visualizar o valor da variável WASM ao mouseover  

Use esse recurso para analisar o valor de uma variável Webassembly \ (WASM \) quando o código for pausado.  Para exibir o valor atual de uma variável, passe o mouse sobre uma variável.  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até problemas [1058836][CR1058836] e [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Visualização de WASM variável ao mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Visualização de WASM variável ao mouseover  
:::image-end:::  

### Unidades de medida consistentes para tamanhos de arquivos e memória  

O DevTools agora usa consistentemente `kB` para exibir tamanhos de arquivos e memória.  DevTools anteriormente `kB` em combinação e `KiB` .

*   `kB` ou quilobyte \ (10 ^ 3 ou 1000 bytes \)  
*   `KiB` ou Kibibyte \ (2 ^ 10 ou 1024 bytes \)  
    
Por exemplo, a ferramenta de **rede** anteriormente usada `kB` em rótulos, mas usada `KiB` em cálculos.  Seus comentários mostraram que essa inconsistência causou confusão.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Issue [1035309][CR1035309].  

## Baixar os canais de visualização do Microsoft Edge  

Se estiver no Windows, Linux ou macOS, considere o uso do [Microsoft Edge Preview Channels] [MicrosoftEdgePreviewChannels] como navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Modo de exibição 3D | Documentos da Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Visão geral do console | Documentos da Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Ativar camadas compostas no modo de exibição 3D – recursos experimentais | Documentos da Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar resposta formatada JSON para a área de transferência-referência de análise da rede | Documentos da Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Exibir a divisão de tempo de uma solicitação-referência de análise de rede | Documentos da Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Use o WebDriver (Chromium) para automação de teste | Documentos da Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Documentos da Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personalizar atalhos de teclado em configurações – novidades do DevTools (Microsoft Edge 87) | Documentos da Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "webhint feedback no painel problemas-novidades do DevTools (Microsoft Edge 85) | Documentos da Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Baixar o WebDriver | Desenvolvedor da Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Baixar canais do Microsoft Edge Insider"  

[VisualStudioCode]: https://code.visualstudio.com "Código do Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Erros de Chromium"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir a substituição de Navigator. Storage. Estimate () | Erros de Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: Reduza a sobrecarga de desempenho do despacho de mensagens de protocolo no front-end | Erros de Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools deve usar consistentemente MB para significar megabyte, não mebibyte | Erros de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools | Erros de Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: problemas com o UX ao WASM a depuração | Erros de Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ experiência do desenvolvedor básico do WASM | Erros de Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: exibir informações sobre quadros gerados por ' Window. Open () ' na árvore de quadros | Erros de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: informações sobre o trabalhador da superfície no modo de exibição árvore de quadros | Erros de Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: CSS <tipo> componentes Erros de Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: testar fallbacks de imagem (emulação) | Erros de Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: não há uma maneira fácil de copiar a carga de solicitação JSON | Erros de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: ferramenta de flexbox | Erros de Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: o ângulo de <de CSS> componente deve refletir a aparência da propriedade contida na tela de fundo do relógio | Erros de Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: o iniciador de rede deve oferecer a capacidade de copiar o rastreamento de pilha | Erros de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: relatar a disponibilidade da API restringida na exibição de detalhes do quadro | Erros de Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: ícones para propriedades de CSS do flexbox no painel estilos | Erros de Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: melhorar o relatório de erros CORS no DevTools | Erros de Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: Adicione estilos Flex decoradores à árvore de elementos | Erros de Chromium"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: o texto limpo ainda está sendo visto na caixa de texto da seção "armazenamento" da janela "ferramentas de desenvolvimento" Erros de Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Erros CORS | Problema"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Compartilhamento de recursos entre origens (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propriedades personalizadas CSS (variáveis) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Construtores-janela | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Acessibilidade | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidade | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Desempenho | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Armadilhas | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Segurança | webhint"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/11/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
