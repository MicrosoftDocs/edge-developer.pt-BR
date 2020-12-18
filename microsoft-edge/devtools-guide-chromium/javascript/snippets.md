---
description: Os trechos de código são pequenos scripts que você pode criar e executar dentro da ferramenta fontes do Microsoft Edge DevTools.  Você pode acessar e executar recursos de qualquer página da Web.  Quando você executa um trecho, ele é executado do contexto da página da Web aberta no momento.
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230954"
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

# Executar trechos de JavaScript em qualquer página da Web com o Microsoft Edge DevTools  

Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho em vez disso.  Trechos de código são scripts que você cria na ferramenta [fontes][DevToolsSourcesTool] .  Os snippets têm acesso ao contexto JavaScript da página da Web, e você pode executar Snippets em qualquer página da Web.  As configurações de segurança da maioria das páginas da Web bloqueiam o carregamento de outros scripts em Snippets.  Por esse motivo, você deve incluir todo o código em um arquivo.  

Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet] com a diferença que os trechos de código são executados apenas em devtools e não se limitam ao comprimento permitido de uma URL.  

Usar Snippets é uma maneira excelente de alterar algumas coisas em uma página da Web de terceiros.  As alterações de código em Snippets são adicionadas à página da Web atual e são executadas no mesmo contexto.  Para obter mais informações sobre como alterar o código existente de uma página da Web, navegue até [substituições][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      Por exemplo, na figura a seguir mostra a home page do DevTools à esquerda e algum código de origem do trecho à direita.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="O antes de executar o trecho de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         A página da Web antes de executar o trecho de código  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      O código-fonte do trecho da página da Web antes de executar o trecho de código.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

Na figura a seguir, a página da Web é exibida após a execução do trecho de código.  A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="A página da Web após a execução do snippet" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   A página da Web após a execução do snippet  
:::image-end:::  

## Abrir o painel Snippets  

O painel **Snippets** lista seus trechos de código.  Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="O painel Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   O painel **Snippets**  
:::image-end:::  

### Abrir o painel Snippets com um mouse  

1.  Escolha a guia **fontes** para abrir a ferramenta **fontes** .  O painel de **página** geralmente abre por padrão.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="A ferramenta fontes com o painel da página aberto à esquerda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       A ferramenta **fontes** com o painel da **página** aberto à esquerda  
    :::image-end:::  
    
1.  Escolha a guia **Snippets** para abrir o painel **Snippets** .  Talvez seja necessário escolher **mais guias** \ ( ![ mais guias ][ImageMoreTabsIcon] \) para acessar a opção **Snippets** .  
    
### Abrir o painel Snippets com o menu de comandos  

1.  Focalize o cursor em algum lugar no DevTools.  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.  
1.  Tipo `Snippets` , escolha **Mostrar Snippets**e, em seguida, selecione `Enter` para executar o comando.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="O comando Mostrar Snippets" lightbox="../media/javascript-search-show-snippets.msft.png":::
       O comando **Mostrar Snippets**  
    :::image-end:::  
    
## Criar Snippets  

### Criar um snippet por meio do painel fontes  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Escolha **novo snippet**.  
1.  Digite um nome para o seu snippet e, em seguida, selecione `Enter` salvar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nomear um snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nomear um snippet  
    :::image-end:::  
    
### Criar um snippet por meio do menu de comando  

1.  Focalize o cursor em algum lugar no DevTools.  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.  
1.  Digite `Snippet` , escolha **criar novo snippet**e, em seguida, selecione `Enter` para executar o comando.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="O comando para criar um novo snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       O comando para criar um novo snippet  
    :::image-end:::  
    
Para renomear o novo snippet com um nome personalizado, navegue até [renomear trechos](#rename-snippets).  

## Editar trechos  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  No painel **Snippets** , escolha o nome do trecho que você deseja editar.  Ele abre no **Editor de código**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       **Editor de código**  
    :::image-end:::  
    
1.  Use o **Editor de código** para adicionar JavaScript ao seu snippet.  
1.  Quando um asterisco é exibido ao lado do nome do seu snippet, isso significa que você tem código não salvo.  Selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) para salvar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Um asterisco ao lado do nome do trecho indica o código não salvo" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Um asterisco ao lado do nome do trecho indica o código não salvo  
    :::image-end:::  
    
## Executar Snippets  

### Executar um snippet do painel fontes  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Escolha o nome do trecho que você deseja executar.  O trecho é aberto no **Editor de código**.  
1.  Escolha **executar snippet** \ ( ![ executar snippet ][ImageRunSnippetIcon] \) ou selecionar `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \).  
    
### Executar um snippet com o menu de comando  

1.  Focalize o cursor em algum lugar no DevTools.  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.  
1.  Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Executar um snippet no menu de comando" lightbox="../media/javascript-search-run-command.msft.png":::
       Executar um snippet no **menu de comando**  
    :::image-end:::  
    
1.  Selecione `Enter` para executar o trecho de código.  

## Renomear trechos  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Passe o cursor do mouse sobre o nome do snippet, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **renomear**.  
    
## Excluir Snippets  

1.  [Abrir o painel **Snippets** ](#open-the-snippets-pane).  
1.  Passe o cursor do mouse sobre o nome do snippet, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **remover**.  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta fontes | Documentos da Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Substituições | Documentos da Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloco de rascunho | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
