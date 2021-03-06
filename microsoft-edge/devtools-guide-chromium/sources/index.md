---
description: Exibir e editar arquivos, criar trechos de código, depurar JavaScript e configurar Espaços de Trabalho no painel Fontes do Microsoft Edge DevTools.
title: Visão geral do painel fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4677bf82d3506a4b8d6336ded7ab557b794fd3df
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397759"
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

# <a name="sources-panel-overview"></a>Visão geral do painel fontes  

Use o painel Fontes **** do Microsoft Edge DevTools para executar as seguintes ações.  

*   [Exibir arquivos](#display-files).  
*   [Edite CSS e JavaScript](#edit-css-and-javascript).  
*   [Crie e salve **trechos de** JavaScript](#create-save-and-run-snippets), que você pode executar em qualquer página da Web.  **Trechos de código** são semelhantes aos indicadores.  
*   [Depurar JavaScript](#debug-javascript).  
*   [Configurar um Espaço de Trabalho](#set-up-a-workspace), para que as alterações feitas no DevTools são salvas no código em seu sistema de arquivos.  
    
## <a name="display-files"></a>Exibir arquivos  

Use o **painel Página;** para exibir todos os recursos que a página carregou.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="O painel Página" lightbox="../media/sources-page-pane.msft.png":::
   O **painel Página**  
:::image-end:::  

Como o **painel** Página é organizado:  
*   O nível superior, como `top` na figura anterior, representa um [quadro HTML][W3CHtml4Frames].  Encontre `top` em todas as páginas que você visitar.  `top` representa o quadro principal do documento.  
*   O segundo nível, como `docs.microsoft.com` na figura anterior, representa uma [origem][HtmlstandardOrigin].  
*   O terceiro nível, quarto nível e assim por diante, representam diretórios e recursos carregados a partir dessa origem.  Por exemplo, na figura anterior, o caminho completo para o `devtools-guide-chromium` recurso é `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Escolha um arquivo no painel **Página** para exibir o conteúdo no **painel Editor.**  Você pode exibir qualquer tipo de arquivo.  Para imagens, uma visualização da imagem é exibida.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Exibir o conteúdo de a4d10f71.index-docs.js no painel Editor" lightbox="../media/sources-editor-pane.msft.png":::
   Exibir o conteúdo `a4d10f71.index-docs.js` do painel **Editor**  
:::image-end:::  

## <a name="edit-css-and-javascript"></a>Editar CSS e JavaScript  

Use o **painel Editor** para editar CSS e JavaScript.  O DevTools atualiza a página para executar seu novo código.  Por exemplo, se você editar um arquivo CSS adicionando a regra de estilo abaixo:

```css
.metadata.page-metadata {
    color: red;
}
```

Essa alteração deve ter efeito imediato.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS no painel Editor para alterar a cor do texto do subtítulo para vermelho" lightbox="../media/edit-css.msft.png":::
   Editar CSS no **painel Editor** para alterar a cor do texto do subtítulo para vermelho  
:::image-end:::  

As alterações css têm efeito imediato, sem a necessidade de salvar.  Para que as alterações do JavaScript entre em vigor, selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\).  DevTools não executará um script de novo, portanto, as únicas alterações javaScript que entrarão em vigor são aquelas que você faz dentro das funções.  Por exemplo, na figura a seguir, observe como `console.log('A')` não é executado, enquanto `console.log('B')` o faz.  Se o DevTools re-executa todo o script depois de fazer a alteração, o texto é `A` registrado no **Console**.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Editando JavaScript no painel Editor" lightbox="../media/edit-js.msft.png":::
   Editando JavaScript no **painel Editor**  
:::image-end:::  

O DevTools apaga as alterações CSS e JavaScript quando você atualize a página.  Navegue [até Configurar um Espaço de Trabalho](#set-up-a-workspace) para saber como salvar as alterações no sistema de arquivos.  

## <a name="create-save-and-run-snippets"></a>Criar, salvar e executar trechos de código  

Trechos de código são scripts que você pode executar em qualquer página.  Imagine que você digite repetidamente o código a seguir no **Console**, para inserir a biblioteca jQuery em uma página, para que você possa executar comandos jQuery do **Console**.  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Em vez disso, você pode salvar esse código em **um trecho** de código e execute-o com alguns cliques de botão, sempre que precisar dele.  O DevTools salva **o trecho em** seu sistema de arquivos.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página" lightbox="../media/snippet.msft.png":::
   Um **trecho que** insere a biblioteca jQuery em uma página  
:::image-end:::  

Para executar um **trecho de código:**

*   Abra o arquivo usando o painel **Trechos** de Código e escolha **Executar** \( ![ O botão Executar ][ImageRunIcon] \).  
*   Abra o [Menu de Comando,][DevtoolsGuideChromiumCommandMenuIndex]exclua o caractere, digite , digite o nome do trecho de código e `>` `!` selecione **** `Enter` .  
    
Navegue [até Executar trechos de código de qualquer página][DevtoolsGuideChromiumJavascriptSnippets] para saber mais.

## <a name="debug-javascript"></a>Depurar JavaScript  

Em vez de usar para inferir onde o JavaScript está indo mal, considere usar as ferramentas `console.log()` de depuração do Microsoft Edge DevTools, em vez disso.  A ideia geral é definir um ponto de interrupção, que é um local de interrupção intencional em seu código e, em seguida, passar pelo tempo de execução do código, uma linha por vez.  Conforme você passa pelo código, você pode exibir e alterar os valores de todas as propriedades e variáveis definidas no momento, executar JavaScript no **Console**e muito mais.

Navegue [até Começar a Depurar JavaScript][DevtoolsGuideChromiumJavascriptIndex] para aprender os conceitos básicos de depuração no DevTools.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="../media/debugging.msft.png":::
   Depurar JavaScript  
:::image-end:::  

## <a name="set-up-a-workspace"></a>Configurar um Espaço de Trabalho  

Por padrão, quando você edita um arquivo na ferramenta **Fontes,** essas alterações são perdidas quando você atualize a página.  **Os espaços de** trabalho permitem que você salve as alterações feitas no DevTools em seu sistema de arquivos.  Essencialmente, o DevTools é capaz de ser usado como seu editor de código.

Navegue [até Editar Arquivos com Espaços de Trabalho][DevtoolsGuideChromiumWorkspacesIndex] para começar.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar arquivos com espaços de trabalho | Microsoft Docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem | HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/sources) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
