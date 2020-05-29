---
title: Usar o tempo de execução do Windows em JavaScript
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bffde93aa973f492189aedcfcaa9c3694d9e61bc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562511"
---
# Usar o tempo de execução do Windows em JavaScript  

Ao escrever um aplicativo da plataforma universal do Windows \ (UWP \), você pode usar as classes, métodos e propriedades do Windows Runtime da mesma forma que usaria objetos, métodos e propriedades JavaScript nativos.  Este tópico fornece informações introdutórias e links para tópicos que explicam os conceitos básicos do uso de APIs do tempo de execução do Windows em JavaScript, incluindo uma explicação sobre como os tipos do Windows Runtime são representados, como usar métodos assíncronos do Windows Runtime e como ouvir e manipular eventos do tempo de execução do Windows.  

Para a documentação geral da linguagem, confira a biblioteca de [referência JavaScript][MDNJavascriptReference] do MDN.  

> [!IMPORTANT]
> Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.  

## Documentação de referência do Windows Runtime  

Para obter documentação de referência, consulte [referência do tempo de execução do Windows][UwpApiIndex].  Exemplos de código estão disponíveis em JavaScript e também em C++, C# e Visual Basic.  

## Gravando componentes do tempo de execução do Windows em C++, C# ou Visual Basic  

Para obter instruções e diretrizes para escrever componentes do tempo de execução do Windows que podem ser consumidos em JavaScript, consulte [criando componentes do tempo de execução do Windows em C++][WindowsUwpWinrtCpp] e [criando componentes do tempo de execução do Windows em C# e Visual Basic][WindowsUwpWinrtCsharpVb].  

## Convenções de maiúsculas e minúsculas com recursos do Windows Runtime  

As convenções de maiúsculas e minúsculas para recursos do tempo de execução do Windows em JavaScript são ligeiramente diferentes das outras linguagens:  

*   Namespaces e classes estão em casos Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Membros de classes, incluindo métodos e propriedades, e membros de estruturas e enumerações, estão em camel case:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Os nomes dos eventos são em minúsculas:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## Consulte também  

[Considerações ao usar a API do Windows Runtime][WindowsRuntimeConsiderationsApi]  
[Usando métodos assíncronos do tempo de execução do Windows][WindowsRuntimeAsynchronousMethods]   
[Manipulando eventos do Windows Runtime em JavaScript][WindowsRuntimeEventsJavascript]   
[Representação JavaScript de tipos do Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Projeção JavaScript de DateTime e TimeSpan do Windows Runtime][WindowsRuntimeDatetimeTimespan]  
 
<!-- image links -->  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: /microsoft-edge/windows-runtime/considerations-when-using-the-windows-runtime-api "Considerações ao usar a API do Windows Runtime"  
[WindowsRuntimeEventsJavascript]: /microsoft-edge/windows-runtime/handling-windows-runtime-events-in-javascript "Manipulando eventos do Windows Runtime em JavaScript"  
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Representação JavaScript de tipos do Windows Runtime"  
[WindowsRuntimeAsynchronousMethods]: /microsoft-edge/windows-runtime/using-windows-runtime-asynchronous-methods "Usando métodos assíncronos do tempo de execução do Windows"  
[WindowsRuntimeDatetimeTimespan]: /microsoft-edge/windows-runtime/windows-runtime-datetime-and-timespan-representations "Representações de DateTime e TimeSpan do Windows Runtime"  

[UwpApiIndex]: /uwp/api/index "Namespaces UWP do Windows"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do tempo de execução do Windows com C++/CX"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do tempo de execução do Windows com C# e Visual Basic"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Referência de JavaScript | MDN"  
