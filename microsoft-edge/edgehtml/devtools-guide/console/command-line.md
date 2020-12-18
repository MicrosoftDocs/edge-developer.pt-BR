---
description: Usar a linha de comando do console para interagir com uma página em execução
title: DevTools-console-linha de comando
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, linha de comando do console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d7ea2bef9fa0014e4d61745636a06d508565df91
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231500"
---
# Linha de comando do console

Use a linha de comando do console para exibir e alterar valores em uma página e executar o código de depuração instantaneamente, tudo isso aproveitando a conclusão de código automático do Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) . 

Basta inserir qualquer JavaScript válido no prompt da linha de comando e pressionar `Enter` para executar. Para a entrada de várias linhas, use `Shift+Enter` para adicionar uma quebra de linha. Use as `Up` `Down` teclas de direção para navegar pelos comandos de console anteriores que você inseriu durante a sessão atual do devtools. Além do JavaScript padrão e da [API do console](./console-api.md), o console também oferece suporte aos seguintes comandos para:

 - [Selecionando objetos DOM](#dom-selectors)
 - [Inspecionar as propriedades do objeto](#object-inspection)
 - [Localizando todos os ouvintes de eventos em um determinado objeto](#event-listeners)

O script inserido na linha de comando é executado no [escopo global](/scripting/javascript/advanced/variable-scope-javascript) da janela selecionada no momento, a menos que a página seja pausada em um ponto de interrupção. Os comandos de console inseridos durante a pausa da página serão executados no [escopo local](/scripting/javascript/advanced/variable-scope-javascript) da função atual dentro da pilha de chamadas.

O console tem um menu suspenso de contexto de execução de **destino** logo acima da área de saída do console. A seleção padrão é o documento de nível superior, **_top**. Qualquer iframe no documento ou extensões em execução também aparecerão como opções, permitindo que você execute comandos de forma alternada nesses escopos.

## Seletores DOM
Esses seletores de console fornecem abreviações simples para acessar rapidamente objetos no DOM:

### $ (*Cadeia de caracteres do seletor CSS*)
Retorna o primeiro elemento dentro do documento que corresponde à cadeia de caracteres do [seletor CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  especificado (ou grupo de seletores separados por vírgula). Abreviação de [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).

Exemplo: Abra o console e digite `$('#main')` para retornar o objeto div com `id='main'` nesta página.

![Exemplo de uso do seletor ' $ '](../media/console_cmd_$.png)

### $ $ (*Cadeia de caracteres do seletor CSS*)
Retorna uma matriz de elementos dentro do documento que corresponde à cadeia de caracteres do [seletor CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  especificado (ou grupo de seletores separados por vírgula). Abreviação de [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).

Exemplo: Abra o console e digite `$$('.container')` para retornar todos os objetos div com `class='container'` nesta página.

![Exemplo de uso do seletor ' $ $ '](../media/console_cmd_$$.png)

### $0, $1, $2,...
Retorna os últimos elementos selecionados no painel [**elementos**](../elements.md) , onde `$0` representa o item atualmente selecionado, `$1` foi o item selecionado antes dele e assim por diante.

Exemplo: abrir DevTools na guia **elementos** , pressione `CTRL + B` para ativar a ferramenta **selecionar elemento** e clique em uma área desta página com o mouse. Agora, abra o console e digite `$0` para retornar o elemento que você acabou de clicar.

![Exemplo de uso do seletor ' $0 '](../media/console_cmd_$0.png)

### $x (*expressão XPath*)
Retorna uma matriz de elementos correspondentes à expressão [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) especificada. 

Exemplo: Abra o console e digite `$x('//script[@defer]')` para retornar todos os `<script>` elementos dessa página que contenham um `defer` atributo.

![Exemplo de uso do seletor ' $x '](../media/console_cmd_$x.png)

## Inspeção de objeto

Esses comandos fornecem maneiras rápidas de inspecionar as propriedades de um objeto. O objeto especificado deve ser definido no namespace global ou no escopo atual do depurador.

### Dir (*objeto*)
Retorna uma lista de modos de exibição de árvore de propriedades do objeto especificado.

Exemplo: Abra o console e digite `dir(document)` para ver as propriedades de objeto do objeto de documento que representam esta página.

![Exemplo de uso do método ' dir '](../media/console_cmd_dir.png)

### Keys (*objeto*)
Retorna uma matriz de nomes de propriedade anexada ao objeto especificado.

Exemplo: Abra o console e digite `keys(window)` para retornar todas as propriedades definidas no objeto da janela global.

![Exemplo de uso do método ' Keys '](../media/console_cmd_keys.png)

### valores (*objeto*)
Retorna uma matriz de valores de propriedade anexados ao objeto especificado.

Exemplo: Abra o console e digite `values(window)` para retornar os valores de todas as propriedades (chaves) definidas no objeto da janela global.

![Exemplo de uso do método ' Values '](../media/console_cmd_values.png)

## Ouvintes de eventos

Esse comando permite que você inspecione os ouvintes de eventos registrados para um determinado objeto. O objeto especificado deve ser definido no namespace global ou no escopo atual do depurador.

### getEventListeners (*objeto*)
Retorna um objeto que contém uma chave para cada tipo de evento registrado no objeto especificado. O valor de cada chave é uma matriz de ouvintes de eventos e suas informações relacionadas. 

Exemplo: Abra o console e digite `getEventListeners(document)` para ver todos os ouvintes de eventos registrados no objeto de documento desta página.

![Exemplo de uso do método ' getEventListeners '](../media/console_cmd_getEventListeners.png)
