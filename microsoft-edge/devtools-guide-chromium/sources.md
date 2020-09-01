---
title: Visão geral do Painel Fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 469e4c3d8707379f5f41f072d31e2f7a5669651d
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984335"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->







# Visão geral do painel fontes 



Use o painel **fontes** devtools do Microsoft Edge para executar as ações de folowing.  

*   [Exibir arquivos](#view-files).  
*   [Editar CSS e JavaScript](#edit-css-and-javascript).  
*   [Crie e salve **trechos de código** JavaScript](#create-save-and-run-snippets), que você pode executar em qualquer página.  Os **trechos de código** são semelhantes a bookmarklets.  
*   [Depurar JavaScript](#debug-javascript).  
*   [Configure um espaço de trabalho](#set-up-a-workspace)para que as alterações feitas no devtools sejam salvas no código do seu sistema de arquivos.  
    
## Exibir arquivos 

Use o painel de **página** para exibir todos os recursos que a página carregou.

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Painel de página" lightbox="./media/sources-page-pane.msft.png":::
   Painel de **página**  
:::image-end:::  

Como o painel da **página** está organizado:  
*   O nível superior, como `top` na figura anterior, representa um [quadro HTML][W3CHtml4Frames].  Localizar `top` em cada página que você visita.  `top` representa o quadro do documento principal.  
*   O segundo nível, como `docs.microsoft.com` na figura anterior, representa uma [origem][HtmlstandardOrigin].  
*   O terceiro nível, o quarto nível e assim por diante, representam diretórios e recursos que foram carregados dessa origem.  Por exemplo, na figura anterior, o caminho completo do recurso `devtools-guide-chromium` é `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Clique em um arquivo no painel da **página** para exibir o conteúdo no painel do **Editor** .  Você pode ver qualquer tipo de arquivo.  Para imagens, você vê uma visualização da imagem.  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Exibir o conteúdo de a4d10f71.index-docs.js no painel do editor" lightbox="./media/sources-editor-pane.msft.png":::
   Exibir o conteúdo do `a4d10f71.index-docs.js` painel do **Editor**  
:::image-end:::  

## Editar CSS e JavaScript 

Use o painel **Editor** para editar CSS e JavaScript.  O DevTools atualiza a página para executar seu novo código.  Por exemplo, se você editar um arquivo CSS, adicione a regra de estilo abaixo:

```css
.metadata.page-metadata {
    color: red;
}
```

Você verá que a alteração entrará em vigor imediatamente.

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Editar CSS no painel do editor para alterar a cor do texto do subtítulo para vermelho" lightbox="./media/edit-css.msft.png":::
   Editar CSS no painel do **Editor** para alterar a cor do texto do subtítulo para vermelho  
:::image-end:::  

As alterações de CSS entram em vigor imediatamente, não é necessário salvar.  Para que as alterações de JavaScript sejam efetivadas, pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \).  O DevTools não executa novamente um script, portanto, as únicas alterações de JavaScript que entram em vigor são aquelas que você faz dentro de funções.  Por exemplo, na figura a seguir, observe como não `console.log('A')` é executado, enquanto `console.log('B')` o faz.  Se o DevTools reexecutar o script inteiro depois de fazer a alteração, o texto `A` teria sido registrado no **console**.  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Edição de JavaScript no painel do editor" lightbox="./media/edit-js.msft.png":::
   Edição de JavaScript no painel do **Editor**  
:::image-end:::  

DevTools apagará as alterações de CSS e JavaScript quando você recarregar a página.  Consulte [configurar um espaço de trabalho](#set-up-a-workspace) para saber como salvar as alterações no seu sistema de arquivos.  

## Criar, salvar e executar Snippets 

Trechos de código são scripts que você pode executar em qualquer página.  Imagine que você digite repetidamente o código a seguir no **console**para inserir a biblioteca jQuery em uma página, para que você possa executar comandos do jQuery a partir do **console**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Em vez disso, você pode salvar esse código em um **snippet** e executá-lo com alguns cliques de botão, sempre que precisar.  DevTools salva o **trecho** em seu sistema de arquivos.  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página" lightbox="./media/snippet.msft.png":::
   Um **trecho** que insere a biblioteca jQuery em uma página  
:::image-end:::  

Para executar um **snippet**:

*   Abra o arquivo usando o painel **Snippets** e clique em **executar** \ ( ![ o botão Executar \ ][ImageRunIcon] ).  
*   Abra o **[menu de comando][DevtoolsGuideChromiumCommandMenuIndex]**, exclua o `>` caractere, digite `!` , digite o nome do seu **snippet**e pressione `Enter` .  
    
Consulte [executar trechos de código em qualquer página][DevtoolsGuideChromiumJavascriptSnippets] para saber mais.

## Depurar JavaScript 

Em vez de usar `console.log()` para inferir onde o JavaScript está errado, considere usar as ferramentas de depuração do Microsoft Edge devtools, em vez disso.  A ideia geral é definir um ponto de interrupção, que é uma interrupção intencional em seu código e, em seguida, percorrer o tempo de execução do seu código, uma linha por vez.  Ao percorrer o código, você pode visualizar e alterar os valores de todas as propriedades e variáveis definidas atualmente, executar JavaScript no **console**e muito mais.

Consulte [introdução à depuração de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para aprender as noções básicas de depuração no devtools.

:::image type="complex" source="./media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="./media/debugging.msft.png":::
   Depurar JavaScript  
:::image-end:::  

## Configurar um espaço de trabalho 

Por padrão, quando você edita um arquivo no painel **fontes** , essas alterações são perdidas quando você recarrega a página.  Os **espaços de trabalho** permitem salvar as alterações feitas no devtools em seu sistema de arquivos.  Basicamente, DevTools pode ser usado como editor de código.

Veja [Editar arquivos com espaços de trabalho][DevtoolsGuideChromiumWorkspacesIndex] para começar.

<!--  
 


-->  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Editar arquivos com espaços de trabalho"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem-padrão HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/sources) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
