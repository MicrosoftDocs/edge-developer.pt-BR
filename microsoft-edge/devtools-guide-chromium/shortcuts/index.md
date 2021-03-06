---
description: A documentação canônica para atalhos de teclado do Microsoft Edge DevTools.
title: Atalhos de teclado do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c6d51d27ce41ed8192a867cf33555b3880dd3ef9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398347"
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

# <a name="microsoft-edge-devtools-keyboard-shortcuts"></a>Atalhos de teclado do Microsoft Edge DevTools  

Este artigo é uma referência de atalhos de teclado no Microsoft Edge DevTools.

Você também pode encontrar atalhos em dicas de ferramentas.  Passe o mouse em um elemento de interface do usuário do DevTools para exibir a dica de ferramenta.  Se o elemento tiver um atalho, a dica de ferramenta o incluirá.

## <a name="keyboard-shortcuts-for-opening-devtools"></a>Atalhos de teclado para abrir o DevTools  

Para abrir o DevTools, selecione os seguintes atalhos de teclado enquanto o cursor está focado no visualizador do navegador.

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Abra qualquer painel usado pela última vez | `F12` ou `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Abra a **ferramenta Console** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Abra a **ferramenta Elements** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` ou `Command`+`Option`+`C` |  

## <a name="global-keyboard-shortcuts"></a>Atalhos globais de teclado  

Os atalhos de teclado a seguir estão disponíveis na maioria, se não todos, painéis DevTools.

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Mostrar **configurações** | `?` or `F1` | `?` ou `Function`+`F1` |  
| Focalizar o próximo painel | `Control`+`]` | `Command`+`]` |  
| Focalizar o painel anterior | `Control`+`[` | `Command`+`[` |  
| Alternar de volta para qualquer posição [de encaixe][DevtoolsCustomizeIndexPlacement] usada pela última vez.  Se DevTools tiver estado na posição padrão para toda a sessão, esse atalho desfaz o DevTools em uma janela separada | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Emulação [de dispositivo de alternância][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar **Modo de Elemento Inspect** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Abra o [Menu de Comando][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Alternar a [gaveta][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Atualização normal | `F5` ou `Control`+`R` | `Command`+`R` |  
| Atualização difícil | `Control`+`F5` ou `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Pesquise texto no painel atual.  Não há suporte nas ferramentas **Auditorias,** **Aplicativos** **e Segurança** | `Control`+`F` | `Command`+`F` |  
| Abre a **guia Pesquisa** na [Gaveta][DevtoolsCustomizeIndexDrawer], que permite que você pesquise texto em todos os recursos carregados | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir um arquivo no painel **Fontes** | `Control`+`O` ou `Control`+`P` | `Command`+`O` ou `Command`+`P` |  
| Zoom in | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Reduzir | `Control`+`-` | `Command`+`-` |  
| Restaurar o nível de zoom padrão | `Control`+`0` | `Command`+`0` |  
| Executar trecho de código | Selecione `Control` + `O` para abrir o [Menu de Comando][DevtoolsCommandMenuIndex], digite seguido `!` pelo nome do script e selecione `Enter` | Selecione `Command` + `O` para abrir o [Menu de Comando][DevtoolsCommandMenuIndex], digite seguido `!` pelo nome do script e selecione `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## <a name="elements-tool-keyboard-shortcuts"></a>Atalhos de teclado da ferramenta Elements  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Desfazer alterações | `Control`+`Z` | `Command`+`Z` |  
| Refazer a alteração | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Selecione o elemento acima/abaixo do elemento selecionado no momento | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Expanda o nó selecionado no momento.  Se o nó já estiver expandido, esse atalho selecionará o elemento abaixo dele | `Right Arrow` | `Right Arrow` |  
| Colapse o nó selecionado no momento.  Se o nó já estiver recolhido, esse atalho selecionará o elemento acima dele | `Left Arrow` | `Left Arrow` |  
| Expandir ou fechar o nó selecionado no momento e todos os filhos | Mantenha `Control` + `Alt` , escolha o ícone **de seta** ao lado do nome do elemento | Mantenha `Option` , escolha o ícone de **seta** ao lado do nome do elemento |  
| Alternar **o modo Editar** Atributos no elemento selecionado no momento | `Enter` | `Enter` |  
| Selecione o próximo/ atributo anterior depois de inserir **o modo Editar Atributos** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ocultar o elemento selecionado no momento | `H` | `H` |  
| Alternar **Editar como modo HTML** no elemento selecionado no momento | `Function`+`F2` | `F2` |  

### <a name="styles-panel-keyboard-shortcuts"></a>Estilos de atalhos de teclado do painel  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Navegue até a linha onde um valor de propriedade é declarado | Hold `Control` , em seguida, selecione o valor da propriedade | Hold `Command` , em seguida, selecione o valor da propriedade |  
| Passar pelas representações RBGA, HSLA e Hex de um valor de cor | Mantenha `Shift` , escolha a caixa **Visualização** de Cores ao lado do valor | Mantenha `Shift` , escolha a caixa **Visualização** de Cores ao lado do valor |  
| Selecione a próxima / anterior propriedade ou valor | Escolha um nome de propriedade ou valor e selecione `Tab` / `Shift`+`Tab` | Escolha um nome de propriedade ou valor e selecione `Tab` / `Shift`+`Tab` |  
| Increment /decrement um valor de propriedade em 0,1 | Escolha um valor e selecione `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Escolha um valor e selecione `Option` + `Up Arrow` / Opção+Seta para Baixo |  
| Increment /decrement um valor de propriedade por 1 | Escolha um valor e selecione `Up Arrow` / `Down Arrow` | Escolha um valor e selecione `Up Arrow` / `Down Arrow` |  
| Increment /decrement um valor de propriedade em 10 | Escolha um valor e selecione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Escolha um valor e selecione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Increment /decrement um valor de propriedade em 100 | Escolha um valor e selecione `Control`+`Up Arrow` / `Control`+`Down Arrow` | Escolha um valor e selecione `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## <a name="sources-tool-keyboard-shortcuts"></a>Atalhos de teclado da ferramenta Sources  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Pausar o tempo de execução do script \(se estiver em execução\) ou retomar \(se estiver pausado\) | `F8` ou `Control`+`\` | `F8` ou `Command`+`\` |  
| Passo a passo na próxima chamada de função | `F10` ou `Control`+`'` | `F10` ou `Command`+`'` |  
| Entrar na próxima chamada de função | `F11` ou `Control`+`;` | `F11` ou `Command`+`;` |  
| Sair da função atual | `Shift`+`F11` ou `Control`+`Shift`+`;` | `Shift`+`F11` ou `Command`+`Shift`+`;` |  
| Continuar para uma [linha de código específica enquanto pausada][DevtoolsJavascriptBreakpointsLOC] | Hold `Control` , em seguida, escolha a linha de código | Hold `Command` , em seguida, escolha a linha de código |  
| Selecione o quadro de chamada abaixo /acima do quadro selecionado no momento | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Salvar alterações em modificações locais | `Control`+`S` | `Command`+`S` |  
| Salvar todas as alterações | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Navegue até a linha | `Control`+`G` | `Control`+`G` |  
| Pule para um número de linha do arquivo aberto no momento | Selecione `Control` + `O` para abrir o [Menu de Comando][DevtoolsCommandMenuIndex], digite seguido pelo número de linha e `:` selecione `Enter` | Selecione `Command` + `O` para abrir o [Menu de Comando][DevtoolsCommandMenuIndex], digite seguido pelo número de linha e `:` selecione `Enter` |  
| Pule para uma coluna do arquivo atualmente aberto \(por exemplo, linha 5, coluna 9\) | Selecione para abrir o Menu de Comando , digite , em seguida, o número da `Control` + `O` [][DevtoolsCommandMenuIndex] `:` linha, em seguida, outro `:` , o número da coluna e selecione `Enter` | Selecione para abrir o Menu de Comando , digite , em seguida, o número da `Command` + `O` [][DevtoolsCommandMenuIndex] `:` linha, em seguida, outro `:` , o número da coluna e selecione `Enter` |  
| Navegue até uma declaração de função, se o arquivo atual for HTML ou um script.  <br />  Navegue até um conjunto de regras, se o arquivo atual for uma folha de estilos.  | Selecione , digite o nome do conjunto `Control` + `Shift` + `O` de declaração/regra ou selecione-o na lista de opções | Selecione , digite o nome do conjunto `Command` + `Shift` + `O` de declaração/regra ou selecione-o na lista de opções |  
| Fechar a guia ativa | `Alt`+`W` | `Option`+`W` |  

### <a name="code-editor-keyboard-shortcuts"></a>Atalhos de teclado do Editor de Código  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Excluir todos os caracteres na última palavra, até o cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Adicionar ou remover um [ponto de interrupção][DevtoolsJavascriptBreakpointsLOC] de linha de código | Concentre o cursor na linha e selecione `Control`+`B` | Concentre o cursor na linha e selecione `Command`+`B` |  
| Navegue até o colchete correspondente | `Control`+`M` | `Control`+`M` |  
| Alternar comentário de linha única.  Se várias linhas forem selecionadas, o DevTools adicionará um comentário ao início de cada linha | `Control`+`/` | `Command`+`/` |  
| Ativar ou desativar a próxima ocorrência de qualquer palavra em que o cursor está.  Cada ocorrência é realçada simultaneamente | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## <a name="performance-tool-keyboard-shortcuts"></a>Atalhos de teclado da ferramenta de desempenho  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar/parar a gravação | `Control`+`E` | `Command`+`E` |  
| Salvar gravação | `Control`+`S` | `Command`+`S` |  
| Gravação de carga | `Control`+`O` | `Command`+`O` |  

## <a name="memory-tool-keyboard-shortcuts"></a>Atalhos de teclado da ferramenta de memória  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar/parar a gravação | `Control`+`E` | `Command`+`E` |  

## <a name="console-tool-keyboard-shortcuts"></a>Atalhos de teclado da ferramenta de console  

| Ação | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Aceitar sugestão de preenchimento automático | `Right Arrow` or `Tab` | `Right Arrow` or `Tab` |  
| Rejeitar sugestão de preenchimento automático | `Escape` | `Escape` |  
| Obter instrução anterior | `Up Arrow` | `Up Arrow` |  
| Obter a próxima instrução | `Down Arrow` | `Down Arrow` |  
| Focalizar o **Console** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Limpar o **Console** | `Control`+`L` | `Command`+`K` ou `Option`+`L` |  
| Force uma entrada de várias linhas.  Esse atalho é basicamente desnecessário, porque o DevTools deve detectar cenários de várias linhas por padrão | `Shift`+`Enter` | `Command`+`Return` |  
| Executar | `Enter` | `Return` |  
| Expanda todas as subpropropriedades de um objeto conectado ao Console | Segure `Alt` e escolha **Expandir** \( ![ Expand ][ImageExpandIcon] \) | Segure `Alt` e escolha **Expandir** \( ![ Expand ][ImageExpandIcon] \) |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Gaveta - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "Alterar o posicionamento do DevTools - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Pontos de interrupção de linha de código - Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/shortcuts) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  