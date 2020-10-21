---
description: Os trechos de código são pequenos scripts que você pode criar e executar no painel fontes do Microsoft Edge DevTools.  Você pode acessá-los e executá-los em qualquer página.  Quando você executa um trecho, ele é executado do contexto da página atualmente aberta.
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124737"
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

Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho de código em vez disso.  Trechos de código são scripts que você cria no painel [fontes][DevToolsSourcesPanel] .  Eles têm acesso ao contexto JavaScript da página, e você pode executá-los em qualquer página.  Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet].  
O Firefox DevTools tem um recurso semelhante a Snippets chamado [bloco de rascunho][MDNScratchpad].  

Por exemplo, na figura a seguir mostra a home page do DevTools à esquerda e algum código de origem do trecho à direita.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   Qual a aparência da página antes de executar o trecho  
:::image-end:::  

O código-fonte do trecho da figura anterior.  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

Na figura a seguir, a página aparece depois de executar o trecho de código.  A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Qual a aparência da página depois de executar o trecho  
:::image-end:::  

## Abrir o painel Snippets  

O painel **Snippets** lista seus trechos de código.  Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   O painel **Snippets**  
:::image-end:::  

### Abrir o painel Snippets com um mouse  

1.  Clique na guia **fontes** para abrir o painel **fontes** .  O painel de **página** geralmente abre por padrão.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-page-pane.msft.png":::
       O painel **fontes** com o painel da **página** aberto à esquerda  
    :::image-end:::  
    
1.  Clique na guia **Snippets** para abrir o painel **Snippets** .  Talvez seja necessário escolher **mais guias** \ ( ![ mais guias ][ImageMoreTabsIcon] \) para acessar a opção **Snippets** .  
    
### Abrir o painel Snippets com o menu de comandos  

1.  Focalize o cursor em algum lugar dentro da DevTools.  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.  
1.  Comece a digitar `Snippets` , escolha **Mostrar Snippets**e, em seguida, selecione `Enter` para executar o comando.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-search-show-snippets.msft.png":::
       O comando **Mostrar Snippets**  
    :::image-end:::  
    
## Criar Snippets  

### Criar um snippet por meio do painel fontes  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Escolha **novo snippet**.  
1.  Digite um nome para o seu snippet e, em seguida, selecione `Enter` salvar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nomear um snippet  
    :::image-end:::  
    
### Criar um snippet por meio do menu de comando  

1.  Focalize o cursor em algum lugar dentro da DevTools.  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.  
1.  Comece a digitar `Snippet` , escolha **criar novo snippet**e, em seguida, selecione `Enter` para executar o comando.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       O comando para criar um novo snippet  
    :::image-end:::  
    
Consulte [renomear trechos](#rename-snippets) se quiser dar um nome personalizado ao novo Snippet.  

## Editar trechos  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  No painel **Snippets** , clique no nome do trecho que você deseja editar para abri-lo no **Editor de código**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       **Editor de código**  
    :::image-end:::  
    
1.  Use o **Editor de código** para adicionar JavaScript ao seu snippet.  
1.  Quando um asterisco aparece ao lado do nome de seu snippet, significa que você tem código não salvo. Selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) para salvar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Um asterisco ao lado do nome do snippet, que indica o código não salvo  
    :::image-end:::  
    
## Executar Snippets  

### Executar um snippet do painel fontes  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique no nome do trecho que você deseja executar.  O trecho é aberto no **Editor de código**.  
1.  Escolha **executar snippet** \ ( ![ executar snippet ][ImageRunSnippetIcon] \) ou selecionar `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \).  
    
### Executar um snippet com o menu de comando  

1.  Focalize o cursor em algum lugar dentro da DevTools.  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.  
1.  Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-search-run-command.msft.png":::
       Executar um snippet no **menu de comando**  
    :::image-end:::  
    
1.  Selecione `Enter` para executar o trecho de código.  

## Renomear trechos  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique com o botão direito do mouse no nome do snippet e escolha **renomear**.  
    
## Excluir Snippets  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Clique com o botão direito do mouse no nome do snippet e escolha **remover**.  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Visão geral do painel fontes | Documentos da Microsoft"  

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
