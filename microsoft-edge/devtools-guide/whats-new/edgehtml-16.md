---
description: Recursos adicionados ao Microsoft Edge DevTools na atualização do Windows 10 para criadores de outono (EdgeHTML 16)
title: DevTools no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, edgehtml 16
ms.custom: seodec18
ms.openlocfilehash: 78ede81e022cc8f0f623ecd33fd2303314ec9cb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561371"
---
# DevTools na atualização do Windows 10 para criadores de outono (EdgeHTML 16)

Com este lançamento, começamos um grande esforço de refatoração de DevTools para melhorar a robustez e o desempenho, além de adicionar um monte de novos recursos que você pode começar a usar hoje mesmo! 

Estes são os recursos do Microsoft Edge DevTools fornecidos com a [atualização do Windows 10 para criadores de outono](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).

## Ouvintes de eventos ancestrais 

O painel **eventos** agora adiciona a opção para exibir ouvintes de eventos registrados em qualquer ancestral do elemento atualmente selecionado (no painel **elementos** ), além daqueles do elemento em si. Além disso, você agora pode agrupar a exibição ouvinte de eventos por *evento* ou *elemento*. 

![Painel de inspeção do ouvinte de eventos](../media/elements_ancestor_events.png)

## Pontos de interrupção de mutação DOM

Agora você pode definir pontos de interrupção de mutação DOM para invadir o depurador sempre que um nó de elemento selecionado é alterado. No painel **elementos** , clique com o botão RT em qualquer elemento na exibição de árvore DOM e selecione um ou mais dos seguintes itens:

 - Quebra no nó removida
 - Quebra na subárvore modificada
 - Quebra no atributo modificado

Você pode gerenciar seus pontos de interrupção de mutação do painel **pontos de interrupção do dom** nos painéis **elementos** ou **depurador** .

![Painel pontos de interrupção DOM](../media/elements_dom_breakpoints.png)

## Suporte a CSS at-Rule

As regras CSS "at" (@) agora são representadas entre outras declarações de regra CSS no painel **estilos** , incluindo regras de animação `@keyframes` (atualmente limitadas a somente leitura), `@supports` consultas de recursos e `@media` consultas.

![Inspeção em regras CSS no painel estilo DevTools](../media/elements_at_rules.png)

## Painel fontes CSS

`@font-face`Agora, as regras CSS têm o próprio painel **fontes** dedicadas que exibe onde a fonte é carregada (*local* ou *rede*) e quantos caracteres estão usando. Se uma fonte for carregada da rede, o DevTools exibirá a regra que a importada juntamente com o seu alias e tipo de fonte.

![Informações de fonte CSS](../media/elements_fonts.png)

## Suporte a polielemento CSS

Agora, o painel **estilos** agrupa os pseudoelementos em seus próprios títulos e não exibe mais o conteúdo deles como riscado.

**Antes:**
<br>
![O conteúdo gerado foi anteriormente riscado](../media/gc_before.png)

**Depois:**
<br>
![O conteúdo gerado não é mais exibido com um tachado](../media/gc_after.png)

## Melhorias no console

O painel de **console** tem uma revisão de UX para melhor usabilidade e uma experiência de IntelliSense mais rápida e mais rica.

**Antes:** 
![ Console anterior](../media/console_old.png)

**Após:** 
![ Novo console](../media/console_new.png)

Também adicionamos estes aprimoramentos:

 -  Use `Shift + Enter` para adicionar uma linha adicional a um comando antes de executá-lo `Enter` . (Antigamente, houve uma *mudança para o botão de alternância de várias linhas/modo de linha única* .)

 - Há suporte para as seguintes novas APIs:
    - método [**console. Table (***objeto***)**](../console/console-api.md#organizing-log-output)
    - comando [**getEventListeners (***objeto***)**](../console/command-line.md#event-listeners)
    - comando [**Keys (***objeto***)**](../console/command-line.md#object-inspection)
    - comando [**valores (***objeto***)**](../console/command-line.md#object-inspection)
    - seletor [**de $x (***expressão XPath***)**](../console/command-line.md#dom-selectors)

 - Agora há suporte para o parâmetro de formatação [**% c ()**](../console/console-api.md#logging-custom-messages)

## Aprimoramentos de depuração

Além de um conjunto de novos recursos para a depuração dos [funcionários e do cache do serviço PWA](#progressive-web-app-debugging), o depurador adicionou estes recursos:

### Depuração consolidada para recursos compartilhados

Mesmo quando um recurso, como um arquivo carregado da CDN, é referenciado várias vezes em todo o seu código, o DevTools agora fornecerá uma única instância de depuração para esse arquivo em que você pode, em seguida, definir pontos de interrupção comuns que serão atingidos independentemente de onde o arquivo for referenciado. (Anteriormente, cada referência de script foi considerada um recurso exclusivo que seria mapeado para um conjunto separado de pontos de interrupção.)

### Editar em tempo real JavaScript com o *Editing-on-Idle*

Agora você pode editar o JavaScript ao vivo durante uma sessão de depuração. Este recurso estava experimentomente disponível (atrás de um sinalizador) na versão [anterior](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) e agora é um recurso permanente. Basta selecionar qualquer arquivo de script no painel **depurador** , editar e, em seguida, clicar em **salvar** (ou `Ctrl+S` ) para testar suas alterações na próxima vez que a seção de código for executada. 

![O depurador permite editar script ao vivo e comparar as alterações](../media/debugger_edit_buttons.png) 

Clique no botão **comparar documento com o original** para exibir a comparação do que você alterou.

![Modo de exibição diff do código editado no depurador](../media/debugger_edit_code.png) 

Lembre-se das seguintes restrições:

- A edição de script funciona apenas em arquivos *. js* externos (e não inseridos `<script>` em *. html*)
- As edições são salvas na memória e liberadas quando o documento é recarregado, portanto, você não poderá executar edições dentro de um `DOMContentLoaded` manipulador, por exemplo
- No momento, não há nenhuma maneira (como a opção **salvar como** ) para salvar suas edições em disco a partir do devtools

## Teclado

Agora você pode iniciar o DevTools no último painel exibido ( `Ctrl+Shift+I` ) ou diretamente ao console ( `Ctrl+Shift+J` ) da mesma forma que faria em outros principais navegadores.

## Depuração de aplicativo Web progressivo

Teste o suporte experimental para aplicativos Web progressivos (PWAs) no Microsoft Edge e no DevTools selecionando a opção **habilitar trabalhos de serviço** a partir de `about:flags` (e reiniciar o Microsoft Edge). Se um site usa funcionários de **serviço** e/ou a API de **cache** , as entradas no painel do **depurador** serão preenchidas para cada origem, de forma semelhante à forma como o armazenamento da Web e a inspeção de cookies funcionam.

Clicar em uma entrada de trabalho específica do serviço abrirá a **visão geral do trabalho do serviço**, onde você pode gerenciar o registro de trabalho do serviço para o escopo fornecido e forçar uma notificação por push de teste. Você também pode **parar** / de**Iniciar** trabalhadores individuais do serviço e **inspecioná** -los em uma janela separada do depurador:

![Painel Visão geral do trabalhador do serviço](../media/debugger_sw_overview.png)

Observe o seguinte sobre a depuração de trabalho do serviço:

 - A depuração de um trabalhador de serviço iniciará uma nova instância do DevTools separada das ferramentas da página, pois os trabalhadores do serviço podem ser compartilhados entre várias guias. 
 - Os painéis de [elementos](../elements.md) e [emulação](../emulation.md) estão ausentes do depurador de trabalho do serviço, pois os trabalhadores do serviço são executados em segundo plano e não controlam diretamente o front-end do seu aplicativo.
 - Atualmente, o tráfego de rede para um trabalhador de serviço é reportado apenas da instância de depuração DevTools para esse trabalhador, e não da instância central da própria página.

Clicar em uma entrada de cache específica abrirá o Gerenciador de **cache** , onde você pode inspecionar e, opcionalmente, excluir entradas de cache (pares de*solicitação* e *resposta* de chave/valor).