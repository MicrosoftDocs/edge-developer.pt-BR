---
title: Usando o Tempo de Execução do Windows no JavaScript
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: 444008598a2f7a2f5257544304bed87fbfaa203a
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942174"
---
# Usando o Tempo de Execução do Windows no JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

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
[Usando Métodos Assíncronos do Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Lidando com de Eventos do Windows Runtime no JavaScript][WindowsRuntimeEventsJavascript]   
[Representação JavaScript de Tipos de Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Projeção JavaScript de DateTime e TimeSpan do Windows Runtime][WindowsRuntimeDatetimeTimespan]  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Considerações ao usar a API do tempo de execução do Windows | Documentos da Microsoft"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Manipulando eventos do tempo de execução do Windows em JavaScript | Documentos da Microsoft"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representação JavaScript de tipos do Windows Runtime | Documentos da Microsoft"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Usando métodos assíncronos do tempo de execução do Windows | Documentos da Microsoft"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Representações de DateTime e TimeSpan do Windows Runtime | Documentos da Microsoft"  

[UwpApiIndex]: /uwp/api/index "Namespaces UWP do Windows | Documentos da Microsoft"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do tempo de execução do Windows com C++/CX | Documentos da Microsoft"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do tempo de execução do Windows com C# e Visual Basic | Documentos da Microsoft"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Referência de JavaScript | MDN"  
