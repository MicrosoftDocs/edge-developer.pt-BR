---
description: A documentação canônica para os atalhos de teclado do Microsoft Edge DevTools.
title: Atalhos de teclado do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 417e2235e4ea63d0258c158035ea201cd5657099
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231268"
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

# Atalhos de teclado do Microsoft Edge DevTools  

Este artigo é uma referência de atalhos de teclado no Microsoft Edge DevTools.

Você também pode encontrar atalhos nas dicas de ferramentas.  Passe o mouse sobre um elemento de interface do usuário do DevTools para exibir a dica de ferramenta.  Se o elemento tiver um atalho, a dica de ferramenta o incluirá.

## Atalhos de teclado para abrir o DevTools  

Para abrir o DevTools, selecione os seguintes atalhos de teclado enquanto o cursor está focalizado no visor do navegador.

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Abrir o painel usado por último | `F12` or `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Abrir o painel de **console** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Abrir o painel **elementos** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` or `Command`+`Option`+`C` |  

## Atalhos de teclado global  

Os atalhos de teclado a seguir estão disponíveis nos painéis mais, se não todos, DevTools.

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Mostrar **configurações** | `?` ou `F1` | `?` or `Function`+`F1` |  
| Focalizar o próximo painel | `Control`+`]` | `Command`+`]` |  
| Concentrar o painel anterior | `Control`+`[` | `Command`+`[` |  
| Volte para qualquer [posição de encaixe][DevtoolsCustomizeIndexPlacement] usada por último.  Se DevTools estiver na posição padrão para toda a sessão, esse atalho desencaixa o DevTools em uma janela separada | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Alternar [emulação de dispositivo][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar o **modo de inspeção do elemento** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Abrir o [menu de comandos][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Alternar a [gaveta][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Recarregamento normal | `F5` or `Control`+`R` | `Command`+`R` |  
| Recarregamento fixo | `Control`+`F5` or `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Pesquisar texto dentro do painel atual.  Não é compatível com os painéis **auditorias**, **aplicativo**e **segurança** | `Control`+`F` | `Command`+`F` |  
| Abre a guia **Pesquisar** na [gaveta][DevtoolsCustomizeIndexDrawer], que permite Pesquisar texto em todos os recursos carregados | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir um arquivo no painel **fontes** | `Control`+`O` or `Control`+`P` | `Command`+`O` or `Command`+`P` |  
| Ampliar | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Reduzir | `Control`+`-` | `Command`+`-` |  
| Restaurar o nível de zoom padrão | `Control`+`0` | `Command`+`0` |  
| Executar trecho | Selecione `Control` + `O` para abrir o [menu de comando][DevtoolsCommandMenuIndex], digite `!` seguido do nome do script e, em seguida, selecione `Enter` | Selecione `Command` + `O` para abrir o [menu de comando][DevtoolsCommandMenuIndex], digite `!` seguido do nome do script e, em seguida, selecione `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Atalhos de teclado do painel elementos  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Desfazer alterar | `Control`+`Z` | `Command`+`Z` |  
| Refazer alterar | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Selecionar o elemento acima/abaixo do elemento atualmente selecionado | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Expanda o nó selecionado no momento.  Se o nó já estiver expandido, esse atalho selecionará o elemento abaixo dele | `Right Arrow` | `Right Arrow` |  
| Recolher o nó selecionado no momento.  Se o nó já estiver recolhido, esse atalho selecionará o elemento acima dele | `Left Arrow` | `Left Arrow` |  
| Expandir ou recolher o nó selecionado no momento e todos os filhos | Segure `Control` + `Alt` e escolha o ícone **de seta** ao lado do nome do elemento | Segure `Option` e escolha o ícone de **seta** ao lado do nome do elemento |  
| Alternar o modo de **edição de atributos** no elemento atualmente selecionado | `Enter` | `Enter` |  
| Selecionar o próximo atributo/anterior após inserir o modo de **edição de atributos** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ocultar o elemento atualmente selecionado | `H` | `H` |  
| Alternar o modo **de edição como HTML** no elemento atualmente selecionado | `Function`+`F2` | `F2` |  

### Atalhos de teclado do painel estilos  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Ir para a linha na qual um valor de propriedade é declarado | Segure `Control` e selecione o valor da propriedade | Segure `Command` e selecione o valor da propriedade |  
| Percorrer as representações RBGA, HSLA e HexA de um valor de cor | Segure `Shift` e escolha a caixa **visualização de cor** ao lado do valor | Segure `Shift` e escolha a caixa **visualização de cor** ao lado do valor |  
| Selecionar o valor ou a propriedade próximo/anterior | Escolha um nome ou valor de propriedade e, em seguida, selecione `Tab` / `Shift`+`Tab` | Escolha um nome ou valor de propriedade e, em seguida, selecione `Tab` / `Shift`+`Tab` |  
| Incrementar/decrementar um valor de propriedade por 0,1 | Escolha um valor e, em seguida, selecione `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Escolha um valor e selecione `Option` + `Up Arrow` /Option + seta para baixo |  
| Incrementar/decrementar um valor de propriedade em 1 | Escolha um valor e, em seguida, selecione `Up Arrow` / `Down Arrow` | Escolha um valor e, em seguida, selecione `Up Arrow` / `Down Arrow` |  
| Incrementar/decrementar um valor de propriedade em 10 | Escolha um valor e, em seguida, selecione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Escolha um valor e, em seguida, selecione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Incrementar/decrementar um valor de propriedade por 100 | Escolha um valor e, em seguida, selecione `Control`+`Up Arrow` / `Control`+`Down Arrow` | Escolha um valor e, em seguida, selecione `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Atalhos de teclado do painel fontes  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Pausar o tempo de execução do script \ (se estiver em execução \) ou continuar \ (se estiver em pausa \) | `F8` or `Control`+`\` | `F8` or `Command`+`\` |  
| Etapa da próxima chamada de função | `F10` or `Control`+`'` | `F10` or `Command`+`'` |  
| Passar para a próxima chamada de função | `F11` or `Control`+`;` | `F11` or `Command`+`;` |  
| Etapa sair da função atual | `Shift`+`F11` or `Control`+`Shift`+`;` | `Shift`+`F11` or `Command`+`Shift`+`;` |  
| Continuar em uma [linha específica de código enquanto estiver em pausa][DevtoolsJavascriptBreakpointsLOC] | Segure `Control` e escolha a linha de código | Segure `Command` e escolha a linha de código |  
| Selecionar o quadro de chamada abaixo/acima do quadro selecionado no momento | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Salvar alterações em modificações locais | `Control`+`S` | `Command`+`S` |  
| Salvar todas as alterações | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Ir para linha | `Control`+`G` | `Control`+`G` |  
| Ir para um número de linha do arquivo aberto no momento | Selecione `Control` + `O` para abrir o [menu de comando][DevtoolsCommandMenuIndex], digite `:` seguido do número da linha e, em seguida, selecione `Enter` | Selecione `Command` + `O` para abrir o [menu de comando][DevtoolsCommandMenuIndex], digite `:` seguido do número da linha e, em seguida, selecione `Enter` |  
| Ir para uma coluna do arquivo aberto no momento \ (por exemplo, linha 5, coluna 9 \) | Selecione `Control` + `O` para abrir o [menu de comando][DevtoolsCommandMenuIndex], digite `:` , o número da linha, depois `:` o número da coluna e, em seguida, selecione `Enter` | Selecione `Command` + `O` para abrir o [menu de comando][DevtoolsCommandMenuIndex], digite `:` , o número da linha, depois `:` o número da coluna e, em seguida, selecione `Enter` |  
| Vá para uma declaração de função, se o arquivo atual for HTML ou um script.  <br />  Vá para um conjunto de regras, se o arquivo atual for uma folha de estilo.  | Selecione `Control` + `Shift` + `O` , digite o nome da declaração/conjunto de regras ou selecione-o na lista de opções | Selecione `Command` + `Shift` + `O` , digite o nome da declaração/conjunto de regras ou selecione-o na lista de opções |  
| Fechar a guia ativa | `Alt`+`W` | `Option`+`W` |  

### Atalhos de teclado do editor de código  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Excluir todos os caracteres na última palavra, até o cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Adicionar ou remover um [ponto de interrupção de linha de código][DevtoolsJavascriptBreakpointsLOC] | Focalize o cursor na linha e selecione `Control`+`B` | Focalize o cursor na linha e selecione `Command`+`B` |  
| Ir para o colchete correspondente | `Control`+`M` | `Control`+`M` |  
| Alternar o comentário em linha única.  Se várias linhas estiverem selecionadas, DevTools adicionar um comentário ao início de cada linha | `Control`+`/` | `Command`+`/` |  
| Selecionar/desmarcar a próxima ocorrência de qualquer palavra que o cursor esteja ativada.  Cada ocorrência é realçada simultaneamente | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Atalhos de teclado do painel de desempenho  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar/parar gravação | `Control`+`E` | `Command`+`E` |  
| Salvar gravação | `Control`+`S` | `Command`+`S` |  
| Carregar gravação | `Control`+`O` | `Command`+`O` |  

## Atalhos de teclado do painel memória  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar/parar gravação | `Control`+`E` | `Command`+`E` |  

## Atalhos de teclado do painel do console  

| Ação | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Aceitar sugestão de preenchimento automático | `Right Arrow` ou `Tab` | `Right Arrow` ou `Tab` |  
| Rejeitar sugestão de preenchimento automático | `Escape` | `Escape` |  
| Instrução Get Previous | `Up Arrow` | `Up Arrow` |  
| Obter próxima instrução | `Down Arrow` | `Down Arrow` |  
| Concentrar o **console** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Limpar o **console** | `Control`+`L` | `Command`+`K` or `Option`+`L` |  
| Force uma entrada de várias linhas.  Esse atalho é praticamente desnecessário, porque o DevTools deve detectar cenários de várias linhas por padrão | `Shift`+`Enter` | `Command`+`Return` |  
| Executar | `Enter` | `Return` |  
| Expandir todas as subpropriedades de um objeto que são registrados no console | Segure `Alt` e escolha **expandir** \ ( ![ expandir ][ImageExpandIcon] \) | Segure `Alt` e escolha **expandir** \ ( ![ expandir ][ImageExpandIcon] \) |  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "Alterar o posicionamento do DevTools-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Pontos de interrupção de linha de código-como pausar um código com pontos de interrupção no Microsoft Edge DevTools | Documentos da Microsoft"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/shortcuts) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  