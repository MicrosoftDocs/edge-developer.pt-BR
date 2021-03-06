---
description: O modo de eventos de linha do tempo exibe todos os eventos disparados durante a gravação.  Use a referência de evento da linha do tempo para saber mais sobre cada tipo de evento de linha do tempo.
title: Referência do evento Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2a166c9eebc980682fa872e5ee8d213f2058b384
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398662"
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

# <a name="timeline-event-reference"></a>Referência do evento Timeline  

O modo de eventos de linha do tempo exibe todos os eventos disparados durante a gravação.  Use a referência de evento da linha do tempo para saber mais sobre cada tipo de evento de linha do tempo.  

## <a name="common-timeline-event-properties"></a>Propriedades comuns de eventos de linha do tempo  

Certos detalhes estão presentes em eventos de todos os tipos, enquanto alguns se aplicam apenas a determinados tipos de evento.  Esta seção lista propriedades comuns a tipos de eventos diferentes.  Propriedades específicas de determinados tipos de evento são listadas nas referências para os tipos de evento a seguir.  

| Propriedade | Quando é mostrado |  
|:--- |:--- |  
| Tempo agregado | Para eventos com **eventos aninhados**, o tempo de cada categoria de eventos. |  
| Pilha de chamada | Para eventos com **eventos filho**, o tempo de cada categoria de eventos. |  
| Hora da CPU | Quanto tempo de CPU o evento gravado levou. |  
| Detalhes | Outros detalhes sobre o evento. |  
| Duração \(at time-stamp\) | Quanto tempo levou para concluir o evento com todos os seus filhos; timestamp é o momento em que o evento ocorreu, em relação ao início da gravação. |  
| Auto-tempo | Quanto tempo o evento demorou sem nenhum de seus filhos. |  
| Tamanho da pilha usado | Quantidade de memória sendo usada pelo aplicativo quando o evento foi gravado e a alteração delta \(+/-\) no tamanho de pilha usado desde a última amostragem. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a>Carregando eventos  

Esta seção lista eventos que pertencem à categoria Loading e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| HTML de análise |  O Microsoft Edge correu o algoritmo de análise HTML. |  
| Concluir o carregamento |  Uma solicitação de rede concluída. |  
| Receber Dados |  Os dados de uma solicitação foram recebidos.  Há um ou mais eventos De recebimento de dados. |  
| Receber Resposta |  A resposta HTTP inicial de uma solicitação. |  
| Enviar Solicitação |  Uma solicitação de rede foi enviada. |  

### <a name="loading-event-properties"></a>Carregando propriedades de evento  

| Propriedade | Descrição |  
|:--- |:--- |  
| Recurso | A URL do recurso solicitado. |  
| Visualização | Visualização do recurso solicitado \(somente imagens\). |  
| Método Request | Método HTTP usado para a solicitação \( `GET` ou `POST` , por exemplo\). |  
| Código de Status | Código de resposta HTTP. |  
| Tipo MIME | Tipo MIME do recurso solicitado. |  
| Comprimento de dados codificados | Comprimento do recurso solicitado em bytes. |  

## <a name="scripting-events"></a>Eventos de script  

Esta seção lista eventos que pertencem à categoria Scripting e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Quadro de animação disparado | Um quadro de animação agendado disparado e seu manipulador de retorno de chamada invocado. |  
| Cancelar Quadro de Animação |  Um quadro de animação agendado foi cancelado. |  
| Evento GC |  Coleta de lixo ocorreu. |  
| DOMContentLoaded |  O [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] foi disparado pelo navegador.  Esse evento é acionado quando todo o conteúdo DOM da página é carregado e analisado. |  
| Avaliar Script | Um script foi avaliado. |  
| Evento | Um evento JavaScript \(por exemplo, `mousedown` , ou `key` \). |  
| Chamada de função | Uma chamada de função JavaScript de nível superior foi feita \(somente aparece quando o navegador entra no mecanismo JavaScript\). |  
| Instalar Timer | Um timer foi criado com [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Quadro de animação de solicitação | Uma `requestAnimationFrame()` chamada agendou um novo quadro. |  
| Remover Timer | Um temporizador criado anteriormente foi limpo. |  
| Hora |  Um script chamado [console.time()][ConsoleApiTime]. |  
| Fim do Tempo | Um script chamado [console.timeEnd()][ConsoleApiTimeEnd]. |  
| Timer acionado | Um timer disparado que foi agendado `setInterval()` com ou `setTimeout()` . |  
| Alteração de estado pronto XHR | O estado pronto de um XMLHTTPRequest foi alterado. |  
| Carga XHR | Um `XMLHTTPRequest` carregamento concluído. |  

### <a name="scripting-event-properties"></a>Propriedades do evento Scripting  

| Propriedade | Descrição |  
|:--- |:--- |  
| Timer ID | A ID do timer. |  
| Tempo limite | O tempo de tempo especificado pelo temporizador. |  
| Repetições | Boolean que especifica se o temporizador se repete. |  
| Chamada de função | Uma função que foi invocada. |  

## <a name="rendering-events"></a>Eventos de renderização  

Esta seção lista eventos que pertencem à categoria Rendering e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Layout inválido | O layout da página foi invalidado por uma alteração dom. |  
| Layout | Um layout de página foi concluído. |  
| Estilo recalcular | Estilos de elemento recalculados do Microsoft Edge. |  
| Rolagem | O conteúdo do exibição aninhado foi rolado. |  

### <a name="rendering-event-properties"></a>Propriedades de evento de renderização  

| Propriedade | Descrição |  
|:--- |:--- |  
| Layout invalidado | Para registros de Layout, o rastreamento de pilha do código que fez com que o layout fosse invalidado. |  
| Nós que precisam de layout | Para registros de Layout, o número de nós que foram marcados como layout necessário antes do retransmissão ser iniciado.  Esses são normalmente os nós que foram invalidados pelo código do desenvolvedor, além de um caminho para cima para raiz de retransmissão. |  
| Tamanho da árvore de layout | Para registros de Layout, o número total de nós sob a raiz de retransmissão \(o nó que o Microsoft Edge inicia o retransmissão\). |  
| Escopo de layout | Os valores `Partial` possíveis são \(o limite de layout de novo é uma parte do DOM\) ou `Whole document` . |  
| Elementos afetados | Para registros de estilo recalculado, o número de elementos afetados por um recálculo de estilo. |  
| Estilos invalidados | Para registros de estilo recalculado, fornece o rastreamento de pilha do código que causou a invalidação do estilo. |  

## <a name="painting-events"></a>Eventos de pintura  

Esta seção lista eventos que pertencem à categoria Painting e suas propriedades.  

| Evento | Descrição |  
|:--- |:--- |  
| Camadas compostas | As camadas de imagem compostas para o mecanismo de renderização do Microsoft Edge. |  
| Decodificar imagem | Um recurso de imagem foi decodificado. |  
| Resize de imagem | Uma imagem foi resized de suas dimensões nativas. |  
| Paint | Camadas compostas foram pintadas para uma região da exibição.  Passar o mouse sobre um registro Paint realça a região da exibição que foi atualizada. |  

### <a name="painting-event-properties"></a>Propriedades do evento Painting  

| Propriedade | Descrição |  
|:--- |:--- |  
| Location | Para eventos Paint, as coordenadas x e y do retângulo de tinta. |  
| Dimensões | Para eventos Paint, a altura e a largura da região pintada. |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time - Referência da API de Console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd - Referência da API de Console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Janela: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Flávio Copes][FlavioCopes] \(Desenvolvedor de Pilha Completa\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
