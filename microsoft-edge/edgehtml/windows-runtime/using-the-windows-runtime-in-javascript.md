---
description: Usando o Tempo de Execução do Windows no JavaScript
title: Usando o Tempo de Execução do Windows no JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4e137526ce147cdeb82749474bd43d1b3697361b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399320"
---
# <a name="using-the-windows-runtime-in-javascript"></a>Usando o Tempo de Execução do Windows no JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Ao escrever um aplicativo da Plataforma Universal do Windows \(UWP\), você pode usar classes, métodos e propriedades do Windows Runtime da mesma maneira que usaria objetos, métodos e propriedades javaScript nativos.  Este tópico fornece informações introdutivas e links para tópicos que explicam os conceitos básicos de uso de APIs do Windows Runtime em JavaScript, incluindo uma explicação sobre como os tipos do Windows Runtime são representados, como usar métodos assíncronos do Windows Runtime e como ouvir e manipular eventos do Windows Runtime.  

Para a documentação geral do idioma, confira a biblioteca de referência [JavaScript][MDNJavascriptReference] do MDN.  

> [!IMPORTANT]
> Os recursos do Windows Runtime não estão disponíveis para aplicativos executados no Internet Explorer.  

## <a name="windows-runtime-reference-documentation"></a>Documentação de referência do Windows Runtime  

Para ver a documentação de referência, consulte [Referência do Tempo de Execução do Windows][UwpApiIndex].  Exemplos de código estão disponíveis em JavaScript e também em C++, C# e Visual Basic.  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a>Escrevendo componentes do Windows Runtime em C++, C# ou Visual Basic  

Para obter instruções e diretrizes para escrever componentes do Windows Runtime que podem ser consumidos no JavaScript, consulte Criando componentes do Tempo de Execução do Windows em [C++][WindowsUwpWinrtCpp] e Criando componentes do Tempo de Execução do [Windows em C#][WindowsUwpWinrtCsharpVb]e Visual Basic .  

## <a name="casing-conventions-with-windows-runtime-features"></a>Convenções de cobertura com recursos do Windows Runtime  

As convenções de invólucro para recursos do Windows Runtime em JavaScript diferem ligeiramente das de outros idiomas:  

*   Namespaces e classes estão no caso Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Membros de classes, incluindo métodos e propriedades e membros de estruturas e enumerações, estão em caso de camel:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Os nomes de eventos estão em menor caso:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a>Veja também  

[Considerações ao usar a API do Windows Runtime][WindowsRuntimeConsiderationsApi]  
[Usando Métodos Assíncronos do Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Lidando com de Eventos do Windows Runtime no JavaScript][WindowsRuntimeEventsJavascript]   
[Representação JavaScript de Tipos de Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Projeção JavaScript do Windows Runtime DateTime e TimeSpan][WindowsRuntimeDatetimeTimespan]  

<!-- links -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Considerações ao usar a API do Tempo de Execução do Windows | Microsoft Docs"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Manipulando eventos do Tempo de Execução do Windows no JavaScript | Microsoft Docs"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representação javascript de tipos de tempo de execução do Windows | Microsoft Docs"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Usando métodos assíncronos do Windows Runtime | Microsoft Docs"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Representações do Windows Runtime DateTime e TimeSpan | Microsoft Docs"  

[UwpApiIndex]: /uwp/api/index "Namespaces UWP do Windows | Microsoft Docs"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do Windows Runtime com C++/CX | Microsoft Docs"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do Windows Runtime com C# e Visual Basic | Microsoft Docs"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Referência javascript | MDN"  
