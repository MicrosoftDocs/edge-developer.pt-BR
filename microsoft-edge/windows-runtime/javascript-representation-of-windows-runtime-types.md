---
title: Representação JavaScript de tipos do Windows Runtime
ms.custom: ''
ms.date: 04/01/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Windows Runtime types [JavaScript]
- JavaScript, Windows Runtime types
ms.assetid: f4851802-8b40-4afa-ba6c-8a162a9a43cc
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b76c28d3448b8be6fbef1fd7e23b07b2eff8d087
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562521"
---
# Representação JavaScript de tipos do Windows Runtime  

A tabela a seguir descreve a maneira como o JavaScript representa tipos do Windows Runtime.  

> [!IMPORTANT]
> Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.  

## Tipos de tempo de execução do Windows em JavaScript  

| Tipo de tempo de execução do Windows | Representação JavaScript | Descrição |  
|:--- |:--- |:--- |  
| `UInt8` | `Number` | Um tempo de execução do Windows `Uint8` é um inteiro de 8 bits não assinado, representado como um número JavaScript.  Um valor de JavaScript é primeiramente convertido em um número de JavaScript e, em seguida, o `ToUint32` processo é seguido.  Se o valor de número JavaScript estiver fora do intervalo de um Uint8, o resultado terá o módulo 2 ^ 8 aplicado. |  
| `Int32` | `Number` | Um tempo de execução do Windows `Int32` é um inteiro de 32 assinado assinado, representado como um número JavaScript.  Um valor de JavaScript é primeiramente convertido em um número de JavaScript e, em seguida, o `ToInt32` processo é seguido.  Se o valor de número de JavaScript estiver fora do intervalo de um `Int32` , o resultado terá o módulo 2 ^ 16 aplicado. |  
| `Int64` | `Number` | Um tempo de execução `Int64` do Windows é um inteiro de 64 assinado, representado como um número padrão quando ele está dentro do intervalo \ [-2 ^ 53, 2 ^ 53 \].  Se ficar fora desse intervalo, ele será representado como um valor numérico que tem um repositório de backup personalizado que mantém os bits de 64 completos de dados inteiros.  Todas as operações matemáticas nesses valores numéricos de Int64 personalizados fazem com que o valor seja convertido em um número padrão no intervalo \ [-2 ^ 53, 2 ^ 53 \].  Se o valor estiver fora desse intervalo, um erro de tipo será gerado.  As exceções a esse processo de conversão são `==` as `===` `SameValue` operações, e e `RelationalComparison` que comparam os argumentos com base nos bits 64 completos quando passaram dois valores de 64 bits representados.  Se o argumento for um número padrão do JavaScript, essas operações também converterão o argumento em um número JavaScript antes da comparação.  Um valor JavaScript será diretamente atribuído se for um valor Int64 em si; caso contrário, o resultado da aplicação da `ToInteger` conversão no valor será passado para o tempo de execução do Windows.  Se a coerção de tipo falhar, uma exceção será retornada. |  
| `Uint64` | `Number` | Um tempo de execução `Uint64` do Windows é um inteiro de 64 bits sem sinal, representado como um número padrão quando ele está dentro do intervalo \ [0, 2 ^ 53 \].  Se ficar fora desse intervalo, ele será representado como um número que tem um repositório de backup personalizado que mantém os bits 64 completos de dados inteiros sem sinal.  Todas as operações matemáticas nesses valores de UInt64 personalizados fazem com que o valor seja convertido em um número padrão no intervalo \ [0, 2 ^ 53 \].  Se o valor estiver fora desse intervalo, um erro de tipo será gerado.  As exceções a esse processo de conversão são `==` as `===` `SameValue` operações, e e `RelationalComparison` que comparam os argumentos com base nos bits 64 completos quando passados valores de 2 64 bits.  Se o argumento for um número padrão do JavaScript, essas operações também converterão o argumento em um número JavaScript antes da comparação.  Um valor de JavaScript será diretamente atribuído se for um valor UInt64 em si; caso contrário, o resultado da aplicação da `ToInteger` conversão no valor, seguido da criação do módulo 2 ^ 52, será passado para Windows Runtime.  Se a conversão do tipo falhar, uma exceção será retornada. |  
| `Single` | `Number` | Um tempo de execução do Windows `Single` é um número de ponto flutuante de 32 bits, representado como um número de JavaScript, selecionando o valor de precisão dupla mais próximo para o valor de precisão única.  Um valor JavaScript é convertido em um número JavaScript e, em seguida, o intervalo é verificado para garantir que o valor possa ser representado em um número de ponto flutuante de ponto flutuante de 32 754 bits de precisão simples.  Se a conversão ou verificação de intervalo falhar, um erro de marshaling será retornado. |  
| `Double` | `Number` | Um tempo de execução do Windows `Double` é um número de ponto flutuante de 64 bits.  `ToNumber` é usado para converter um tempo de execução do Windows `Double` em um número JavaScript.  Se a conversão falhar, um erro de marshaling será retornado. |  
| `Boolean` | `Boolean` | Um tempo de execução do Windows `Boolean` é um valor de 8 bits em que zero é `false` e qualquer valor diferente de zero é `true` representado como um JavaScript `Boolean` .  Um valor de JavaScript é primeiramente convertido em JavaScript `Boolean` por `ToBoolean` .  Isso significa que uma função do tempo de execução do Windows declarada como `void func(BOOL);` pode ser gravada em JavaScript como `obj.func("test");` .  A função do tempo de execução do Windows é chamada com o `BOOL` parâmetro passado como `TRUE` .  Se a conversão falhar, um erro de marshaling será retornado. |  
| `Char16` | `String` | Um tempo de execução do Windows `Char16` é um caractere Unicode de 16 bits, representado como uma cadeia de caracteres JavaScript que contém um único caractere.  Um valor JavaScript é convertido em uma cadeia de caracteres JavaScript por `ToString` e, em seguida, verificado para garantir que a cadeia de caracteres seja apenas um único caractere de longa duração.  O caractere único é passado como o `Char16` valor.  Se a verificação de conversão ou de comprimento falhar, um erro de marshaling será retornado. |  
| `String` | `String` | Um tempo de execução `String` do Windows é uma sequência imutável de `Char16` objetos.  As cadeias de caracteres são representadas como `String` objetos JavaScript.  As cadeias de caracteres do Windows Runtime não têm valores diferentes para `null` e uma cadeia de caracteres vazia \ ("" \).  `null` e valores de cadeia de caracteres vazias são convertidos na cadeia de caracteres vazia de JavaScript.  Observação: quando JavaScript `null` é passado para um parâmetro do tempo de execução do Windows que espera uma cadeia de caracteres, ele produz o valor de cadeia de caracteres "NULL", não `null` ou a cadeia de caracteres vazia \ ("" \).  Cadeias de caracteres passadas para o tempo de execução do Windows sempre devem ser instanciadas para a cadeia de caracteres vazia. |  
| `Enumeration` | `Object` | Um tempo de execução do Windows `Enumeration` é um inteiro de 32 bits \ (assinado ou não assinado \) que tem um conjunto associado de constantes nomeadas.  Em JavaScript, uma enumeração é representada como um objeto que contém um campo somente leitura para cada valor nomeado.  Os valores de enumeração são convertidos em números JavaScript, conforme definido anteriormente para `Int32` and `UInt32` .  Quando um valor JavaScript é convertido em uma enumeração do tempo de execução do Windows, ele é convertido, truncado e o intervalo é verificado conforme descrito anteriormente.  No entanto, o valor resultante não é verificado em relação aos valores nomeados definidos que são especificados na enumeração. |  
| `Structure` | `Object` | Um tempo de execução `Structure` do Windows é uma coleção heterogênea de campos de dados nomeados.  Em JavaScript, uma estrutura é representada como um objeto JavaScript que contém uma propriedade nomeada para cada campo da estrutura.  Se a conversão de qualquer valor de estrutura falhar, um erro de marshaling será retornado.  Os campos no objeto JavaScript que não têm equivalentes na estrutura do tempo de execução do Windows são ignorados.  Observação: uma estrutura do tempo de execução do Windows não pode ser instanciada em JavaScript com a `new` palavra-chave. |  
| `Array` | `Array` | Um tempo de execução do Windows `Array` é convertido em uma matriz de JavaScript.  No entanto, as matrizes do Windows Runtime não são redimensionáveis, portanto, algumas operações de matriz de JavaScript não são possíveis.  A `[[Class]]` Propriedade Internal de uma matriz convertida não está definida como "array" porque isso não é permitido pela especificação ECMAScript 5.  Isso significa que `Array.isArray(v)` retorna `false` .  Um valor JavaScript é convertido em uma matriz do Windows Runtime da seguinte maneira: se o valor for `null` ou `undefined` , ele será convertido em Native `null` .  Se a `[[Class]]` propriedade interna for "array", ela será copiada para uma matriz nativa e uma referência a essa matriz será passada.  Se for uma matriz convertida, conforme descrito anteriormente, a matriz nativa subjacente será transmitida.  Observação: passar um valor de matriz JavaScript para um método do tempo de execução do Windows causa uma cópia completa da matriz. |  
| Delegate \ (retorno de chamada de função \) | `Function` | Um representante do tempo de execução do Windows é uma referência a um único método.  Um representante do tempo de execução do Windows é representado em JavaScript como JavaScript `Function` , que tem a garantia de ser chamado no thread adequado.  Quando `Function` invocado, os argumentos são convertidos nos tipos de parâmetro equivalentes do tempo de execução do Windows.  Se houver menos argumentos JavaScript do que `in` os parâmetros representante, a chamada de representante falhará.  Se houver mais argumentos JavaScript do que os `in` parâmetros no representante, os argumentos adicionais JavaScript serão ignorados.  Após o representante ser invocado, os `out` parâmetros são convertidos em tipos JavaScript e retornados.  Se um objeto de função JavaScript nativo for convertido em um representante do Windows Runtime, ele será encapsulado em um representante do tempo de execução do Windows do tipo correspondente.  Quando o representante é invocado, os `in` parâmetros são convertidos em tipos JavaScript.  Após o representante ser invocado, o valor de retorno é convertido nos `out` parâmetros do representante. |  
| Interface | `Object` | Interfaces e grupos de interface não são representados diretamente em JavaScript como objetos.  No entanto, as interfaces são representadas como parâmetro e tipos de retorno dos métodos do tempo de execução do Windows.  Uma instância de interface do tempo de execução do Windows é convertida da seguinte maneira:<br /> <br /> 1. se houver uma classe de tempo de execução válida, represente o objeto como uma instância dessa classe.<br /> 2. se não houver uma classe de tempo de execução válida, represente o objeto como uma instância de uma classe de tempo de execução sem nome que implementa exatamente a interface que a instância é conhecida a implementar, além das interfaces necessárias.<br /> <br /> Um valor JavaScript é testado para determinar se ele é uma instância de uma classe de tempo de execução ou uma interface.  Se for, e o valor do Windows Runtime original implementar a interface, o objeto será passado para o tempo de execução do Windows. |  
| Classes de tempo de execução | `Object` | Os objetos no Windows Runtime podem ser instâncias de classes de tempo de execução que implementam uma ou mais interfaces.  Os objetos do Windows Runtime são representados em JavaScript como objetos.  A União de métodos, propriedades e eventos definidos em todas as interfaces implementadas da classe representam as propriedades nomeadas no protótipo do objeto JavaScript.  Os consumidores de JavaScript podem acessar qualquer membro da classe diretamente.  Os objetos do Windows Runtime têm um protótipo que contém todos os membros de todas as interfaces implementadas da classe de tempo de execução. |  
  
## Consulte também  

[Usar o tempo de execução do Windows em JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar o tempo de execução do Windows em JavaScript"  