---
title: Referência do evento Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611717"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Referência do evento Timeline   




O modo de eventos de linha do tempo exibe todos os eventos disparados ao criar uma gravação.  Use a referência de evento Timeline para saber mais sobre cada tipo de evento de linha do tempo.  

## Propriedades de eventos comuns da linha do tempo  

Alguns detalhes estão presentes em eventos de todos os tipos, enquanto alguns só se aplicam a determinados tipos de eventos.  Esta seção lista as propriedades comuns a diferentes tipos de eventos.  As propriedades específicas para determinados tipos de eventos são listadas nas referências para os tipos de eventos que se seguem.  

| Propriedade | Quando é exibido |  
|:--- |:--- |  
| Tempo agregado | Para eventos com **eventos aninhados**, o tempo usado por cada categoria de eventos. |  
| Pilha de chamadas | Para eventos com **eventos filho**, o tempo usado por cada categoria de eventos. |  
| Tempo de CPU | Quanto tempo da CPU o evento registrado levou. |  
| Detalhes | Outros detalhes sobre o evento. |  
| Duration \ (no carimbo de data/hora \) | Quanto tempo levava o evento com todos os seus filhos a concluir; carimbo de data/hora é o horário em que o evento ocorreu em relação ao início da gravação. |  
| Tempo de autoatendimento | Por quanto tempo o evento demorou sem qualquer um de seus filhos. |  
| Tamanho de heap usado | A quantidade de memória que está sendo usada pelo aplicativo quando o evento foi gravado, e a alteração de \ (+/-\) do Delta é usada em tamanho de heap usado desde a última amostragem. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## Carregando eventos  

Esta seção lista os eventos que pertencem à categoria de carregamento e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Analisar HTML |  O Microsoft Edge executou o algoritmo de análise HTML. |  
| Concluir o carregamento |  Uma solicitação de rede foi concluída. |  
| Receber dados |  Os dados de uma solicitação foram recebidos.  Há um ou mais eventos de recebimento de dados. |  
| Receber resposta |  A resposta HTTP inicial de uma solicitação. |  
| Enviar solicitação |  Uma solicitação de rede foi enviada. |  

### Carregando Propriedades do evento  

| Propriedade | Descrição |  
|:--- |:--- |  
| Recurso | A URL do recurso solicitado. |  
| Visualização | Visualização do recurso solicitado \ (apenas imagens \). |  
| Método de solicitação | Método HTTP usado para a solicitação \ ( `GET` ou `POST` , por exemplo, \). |  
| Código de status | Código de resposta HTTP. |  
| Tipo MIME | Tipo MIME do recurso solicitado. |  
| Comprimento de dados codificados | Comprimento do recurso solicitado em bytes. |  

## Eventos de script  

Esta seção lista os eventos que pertencem à categoria de script e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Quadro de animação acionado | Um quadro de animação programado foi acionado, e seu manipulador de retorno de chamada foi invocado. |  
| Cancelar quadro de animação |  Um quadro de animação agendado foi cancelado. |  
| Evento GC |  Ocorreu uma coleta de lixo. |  
| DOMContentLoaded |  O [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] foi acionado pelo navegador.  Esse evento é acionado quando todo o conteúdo DOM da página é carregado e analisado. |  
| Avaliar o script | Um script foi avaliado. |  
| Evento | Um evento JavaScript \ (por exemplo, `mousedown` , ou `key` \). |  
| Chamada de função | Uma chamada de função JavaScript de nível superior foi feita \ (só aparece quando o navegador entra no mecanismo JavaScript \). |  
| Temporizador de instalação | Um temporizador foi criado com [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Quadro de animação de solicitação | Uma `requestAnimationFrame()` chamada agendou um novo quadro. |  
| Remover temporizador | Um temporizador criado anteriormente foi limpo. |  
| Hora |  Um script chamado [console. time ()][ConsoleApiTime]. |  
| Término do tempo | Um script chamado [console. timeEnd ()][ConsoleApiTimeEnd]. |  
| Temporizador acionado | Um temporizador foi acionado que foi agendado com `setInterval()` ou `setTimeout()` . |  
| Alteração de estado pronto para XHR | O estado pronto de um XMLHttpRequest alterado. |  
| Carga XHR | `XMLHTTPRequest`Conclusão do carregamento. |  

### Propriedades de evento de script  

| Propriedade | Descrição |  
|:--- |:--- |  
| ID do temporizador | A ID do temporizador. |  
| Tempo limite | O tempo limite especificado pelo temporizador. |  
| Repete | Booliano que especifica se o cronômetro se repete. |  
| Chamada de função | Uma função que foi invocada. |  

## Eventos de renderização  

Esta seção lista os eventos que pertencem à categoria de renderização e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Layout Invalidate | O layout da página foi invalidado por uma alteração DOM. |  
| Layout | Um layout de página foi concluído. |  
| Recalcular estilo | Estilos de elemento recalculados do Microsoft Edge. |  
| Rolagem | O conteúdo do modo de exibição aninhado foi rolado. |  

### Renderizando Propriedades de eventos  

| Propriedade | Descrição |  
|:--- |:--- |  
| Layout invalidado | Para registros de layout, o rastreamento de pilha do código que fez com que o layout fosse invalidado. |  
| Nós que precisam de layout | Para registros de layout, o número de nós que foram marcados como necessidade de layout antes do reinício do layout.  Esses nós normalmente são aqueles que foram invalidados pelo código do desenvolvedor, mais o caminho para a vertical para refazer o layout da raiz. |  
| Tamanho da árvore de layout | Para registros de layout, o número total de nós sob a raiz do relayout \ (o nó que o Microsoft Edge inicia o relayout \). |  
| Escopo de layout | Os valores possíveis são `Partial` \ (o limite de novo layout é uma parte do dom \) ou `Whole document` . |  
| Elementos afetados | Para recalcular registros de estilo, o número de elementos afetados por um recálculo de estilo. |  
| Estilos invalidados | Para recalcular registros de estilo, fornece o rastreamento de pilha do código que causou a invalidação de estilo. |  

## Eventos de pintura  

Esta seção lista os eventos que pertencem à categoria de pintura e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Camadas compostas | As camadas da imagem compostas para o mecanismo de renderização do Microsoft Edge. |  
| Decodificação de imagem | Um recurso de imagem foi decodificado. |  
| Redimensionamento de imagens | Uma imagem foi redimensionada a partir de suas dimensões nativas. |  
| Paint | Camadas compostas foram pintadas para uma região da exibição.  Passar o mouse sobre um registro de pintura realça a região do vídeo que foi atualizado. |  

### Propriedades de evento de pintura  

| Propriedade | Descrição |  
|:--- |:--- |  
| Location | Para eventos de pintura, as coordenadas x e y do retângulo de pintura. |  
| Dimension | Para eventos de pintura, a altura e a largura da região pintada. |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "tempo-referência da API do console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-referência de API do console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Janela: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e o [Flavio][FlavioCopes] se encontra \ (desenvolvedor de pilha completa \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
