---
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581814"
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





# Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools   



Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho de código em vez disso.  Trechos de código são scripts que você cria no [painel **fontes** ][DevToolsSourcesPanel].  Eles têm acesso ao contexto JavaScript da página, e você pode executá-los em qualquer página.  Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet].  
O Firefox DevTools tem um recurso semelhante a Snippets chamado [bloco de rascunho][MDNScratchpad].  

Por exemplo, a [**Figura 1**](#figure-1) mostra a home page do devtools à esquerda e parte do código-fonte do trecho à direita.  

> ##### Figura 1  
> Qual a aparência da página antes de executar o trecho  
> ![Qual a aparência da página antes de executar o trecho][ImageSnippetSplitScreen]  

O código-fonte do trecho da [**Figura 1**](#figure-1):  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

A [**Figura 2**](#figure-2) mostra como a página é exibida após a execução do trecho de código.  A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.  

> ##### Figura 2  
> Qual a aparência da página depois de executar o trecho  
> ![Qual a aparência da página depois de executar o trecho][ImageSnippetSplitScreenAfter]  

## Abrir o painel Snippets   

O painel **Snippets** lista seus trechos de código.  Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .  

> ##### Figura 3  
> O painel **Snippets**  
> ![O painel Snippets][ImageSnippetsPane]  

### Abrir o painel Snippets com um mouse   

1.  Clique na guia **fontes** para abrir o painel **fontes** .  O painel de **página** geralmente abre por padrão.  

    > ##### Figura 4  
    > O painel **fontes** com o painel da **página** aberto à esquerda  
    > ![O painel fontes com o painel da página aberto à esquerda][ImageSourcesPageEmpty]  

1.  Clique na guia **Snippets** para abrir o painel **Snippets** .  Talvez seja necessário clicar em **mais** guias ![ ][ImageMoreTabsIcon] para acessar a opção **Snippets** .  

### Abrir o painel Snippets com o menu de comandos   

1.  Focalize o cursor em algum lugar dentro da DevTools.  
1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.  
1.  Comece a digitar `Snippets` , selecione **Mostrar Snippets**e pressione `Enter` para executar o comando.  

    > ##### Figura 5  
    > O comando **Mostrar Snippets**  
    > ![O comando Mostrar Snippets][ImageShowSnippetsSearch]  

## Criar Snippets   

### Criar um snippet por meio do painel fontes   

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique em **novo snippet**.  
1.  Digite um nome para o seu snippet e pressione `Enter` para salvar.  

    > ##### Figura 6  
    > Nomear um snippet  
    > ![Nomear um snippet][ImageSnippetName]  

### Criar um snippet por meio do menu de comando   

1.  Focalize o cursor em algum lugar dentro da DevTools.  
1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.  
1.  Comece a digitar `Snippet` , selecione **criar novo snippet**e pressione `Enter` para executar o comando.  

    > ##### Figura 7  
    > O comando para criar um novo snippet  
    > ![O comando para criar um novo snippet][ImageCreateSnippetSearch]  

Consulte [renomear trechos](#rename-snippets) se quiser dar um nome personalizado ao novo Snippet.  

## Editar trechos   

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  No painel **Snippets** , clique no nome do trecho que você deseja editar para abri-lo no **Editor de código**.  

    > ##### Figura 8  
    > Editor de código  
    > ![Editor de código][ImageSnippetEditor]  

1.  Use o **Editor de código** para adicionar JavaScript ao seu snippet.  
1.  Quando um asterisco aparece ao lado do nome de seu snippet, significa que você tem código não salvo. Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar.  

    > ##### Figura 9  
    > Um asterisco ao lado do nome do snippet, que indica o código não salvo  
    > ![Um asterisco ao lado do nome do snippet, que indica o código não salvo][ImageUnsavedSnippet]  

## Executar Snippets   

### Executar um snippet do painel fontes   

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique no nome do trecho que você deseja executar.  O trecho é aberto no **Editor de código**.  
1.  Clique em **executar** ![ trecho ][ImageRunSnippetIcon] de código de execução, ou pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).  

### Executar um snippet com o menu de comando   

1.  Focalize o cursor em algum lugar dentro da DevTools.  
1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.  
1.  Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.  

    > ##### Figura 10  
    > Executar um snippet no menu de comando  
    > ![Executar um snippet no menu de comando][ImageRunSnippetCommand]  

1.  Pressione `Enter` para executar o trecho de código.  

## Renomear trechos   

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique com o botão direito do mouse no nome do snippet e selecione **renomear**.  

## Excluir Snippets   

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique com o botão direito do mouse no nome do snippet e selecione **remover**.  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Figura 1: qual a aparência da página antes de executar o trecho"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Figura 2: como a página é exibida após a execução do snippet"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Figura 3: o painel Snippets"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Figura 4: painel fontes com o painel da página aberto à esquerda"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Figura 5: o comando Mostrar Snippets"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Figura 6: nomeando um trecho"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Figura 7: o comando para criar um novo snippet"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Figura 8: editor de código"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Figura 9: um asterisco ao lado do nome do snippet, que indica o código não salvo"  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Figura 10: executando um snippet no menu de comando"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console"  
[DevToolsSourcesPanel]: ../sources.md "Visão geral do painel fontes"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloco de rascunho | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
