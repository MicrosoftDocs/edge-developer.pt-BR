---
description: Trechos de código são scripts pequenos que você pode escrever e executar na ferramenta Sources do Microsoft Edge DevTools.  Você pode acessar e executar recursos de qualquer página da Web.  Quando você executa um trecho, ele é executado a partir do contexto da página da Web aberta no momento.
title: Executar trechos de javascript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439420"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a>Executar trechos de código do JavaScript em qualquer página da Web com o Microsoft Edge DevTools  

Se você estiver executando o mesmo código no [Console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho.  Trechos de código são scripts que você escreveu na [ferramenta Fontes.][DevToolsSourcesTool]  Trechos de código têm acesso ao contexto JavaScript da página da Web e você pode executar trechos em qualquer página da Web.  As configurações de segurança da maioria das páginas da Web bloqueiam o carregamento de outros scripts em Trechos de Código.  Por esse motivo, você deve incluir todo o código em um arquivo.  

Trechos de código são [][WikiBookmarklet] uma alternativa aos indicadores com a diferença de que trechos de código são executados apenas no DevTools e não se limitam ao tamanho permitido de uma URL.  

Usar trechos de código é uma excelente maneira de alterar algumas coisas em uma página da Web de terceiros.  As alterações de código em Trechos de Código são adicionadas à página da Web atual e são executados no mesmo contexto.  Para obter mais informações sobre como alterar o código existente de uma página da Web, navegue até [Substituições][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      Por exemplo, na figura a seguir mostra a homepage DevTools à esquerda e algum código-fonte trecho à direita.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="O antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         A página da Web antes de executar o trecho de código  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      O código-fonte trecho da página da Web antes de executar o trecho.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

Na figura a seguir, a página da Web é exibida após a execução do trecho de código.  A **Gaveta de Console** é exibida para exibir a mensagem que o trecho de código registra e o conteúdo da página da Web muda `Hello, Snippets!` completamente.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="A página da Web após a execução do trecho de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   A página da Web após a execução do trecho de código  
:::image-end:::  

## <a name="open-the-snippets-pane"></a>Abra o painel Trechos de Código  

O **painel Trechos de** Código lista seus trechos.  Quando você deseja editar um trecho, você precisa abri-lo do painel **Trechos** de Código.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="O painel Trechos de Código" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   O **painel Trechos** de Código  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a>Abra o painel Trechos de Código com um mouse  

1.  Escolha a **guia Fontes** para abrir a **ferramenta Fontes.**  O **painel Página** geralmente é aberto por padrão.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="A ferramenta Sources com o painel Página aberta à esquerda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       A **ferramenta Sources** com o painel **Página** aberta à esquerda  
    :::image-end:::  
    
1.  Escolha a **guia Trechos de** Código para abrir o painel **Trechos** de Código.  Talvez seja necessário escolher **Mais Guias** \( Mais ![ Guias ](../media/more-tabs-icon.msft.png) \) para acessar a opção **Trechos** de Código.  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a>Abra o painel Trechos de Código com o Menu de Comando  

1.  Concentre seu cursor em algum lugar no DevTools.  
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.  
1.  Digite `Snippets` , escolha Mostrar **Trechos de**Código e, em seguida, selecione para executar o `Enter` comando.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="O comando Mostrar Trechos de Código" lightbox="../media/javascript-search-show-snippets.msft.png":::
       O **comando Mostrar Trechos de** Código  
    :::image-end:::  
    
## <a name="create-snippets"></a>Criar trechos de código  

### <a name="create-a-snippet-through-the-sources-panel"></a>Criar um trecho por meio do painel Fontes  

1.  [Abra o **painel Trechos de** Código.](#open-the-snippets-pane)  
1.  Escolha **Novo trecho**de código .  
1.  Insira um nome para o trecho de código e selecione `Enter` salvar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nomear um trecho" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nomear um trecho  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a>Criar um trecho de código por meio do Menu de Comando  

1.  Concentre seu cursor em algum lugar no DevTools.  
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.  
1.  Digite `Snippet` , escolha Criar novo trecho de **código**e, em seguida, selecione para executar `Enter` o comando.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="O comando para criar um novo trecho" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       O comando para criar um novo trecho  
    :::image-end:::  
    
Para renomear seu novo trecho de código com um nome personalizado, navegue até [Renomear Trechos de Código](#rename-snippets).  

## <a name="edit-snippets"></a>Editar trechos  

1.  [Abra o **painel Trechos de** Código.](#open-the-snippets-pane)  
1.  No painel **Trechos** de Código, escolha o nome do trecho que você deseja editar.  Ele é aberto no **Editor de Código.**  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="O Editor de Código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       O **Editor de Código**  
    :::image-end:::  
    
1.  Use o **Editor de Código** para adicionar JavaScript ao seu trecho de código.  
1.  Quando um asterisco é exibido ao lado do nome do trecho de código, significa que você tem código não saved.  Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Um asterisco ao lado do nome trecho indica código não saved" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Um asterisco ao lado do nome trecho indica código não saved  
    :::image-end:::  
    
## <a name="run-snippets"></a>Executar trechos de código  

### <a name="run-a-snippet-from-the-sources-panel"></a>Executar um trecho do painel Fontes  

1.  [Abra o **painel Trechos de** Código.](#open-the-snippets-pane)  
1.  Escolha o nome do trecho que você deseja executar.  O trecho é aberto no **Editor de Código.**  
1.  Escolha **Executar Trecho de Código** \( Executar Trecho \) ou selecione ![ ](../media/run-snippet-icon.msft.png) `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\).  
    
### <a name="run-a-snippet-with-the-command-menu"></a>Executar um trecho com o Menu de Comando  

1.  Concentre seu cursor em algum lugar no DevTools.  
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.  
1.  Exclua o caractere e digite o caractere seguido pelo nome do `>` trecho que você deseja `!` executar.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Executando um trecho do Menu de Comando" lightbox="../media/javascript-search-run-command.msft.png":::
       Executando um trecho do **Menu de Comando**  
    :::image-end:::  
    
1.  Selecione `Enter` para executar o trecho.  

## <a name="rename-snippets"></a>Renomear trechos  

1.  [Abra o **painel Trechos de** Código.](#open-the-snippets-pane)  
1.  Passe o mouse no nome do trecho, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Renomear**.  
    
## <a name="delete-snippets"></a>Excluir trechos de código  

1.  [Abra o **painel Trechos de** Código.](#open-the-snippets-pane)  
1.  Passe o mouse no nome do trecho, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Remover**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Substitui | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
