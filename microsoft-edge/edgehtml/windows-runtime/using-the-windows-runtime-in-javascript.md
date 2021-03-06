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
# <a name="using-the-windows-runtime-in-javascript"></a><span data-ttu-id="b8448-103">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="b8448-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="b8448-104">Ao escrever um aplicativo da Plataforma Universal do Windows \(UWP\), você pode usar classes, métodos e propriedades do Windows Runtime da mesma maneira que usaria objetos, métodos e propriedades javaScript nativos.</span><span class="sxs-lookup"><span data-stu-id="b8448-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="b8448-105">Este tópico fornece informações introdutivas e links para tópicos que explicam os conceitos básicos de uso de APIs do Windows Runtime em JavaScript, incluindo uma explicação sobre como os tipos do Windows Runtime são representados, como usar métodos assíncronos do Windows Runtime e como ouvir e manipular eventos do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="b8448-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="b8448-106">Para a documentação geral do idioma, confira a biblioteca de referência [JavaScript][MDNJavascriptReference] do MDN.</span><span class="sxs-lookup"><span data-stu-id="b8448-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b8448-107">Os recursos do Windows Runtime não estão disponíveis para aplicativos executados no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b8448-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="windows-runtime-reference-documentation"></a><span data-ttu-id="b8448-108">Documentação de referência do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b8448-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="b8448-109">Para ver a documentação de referência, consulte [Referência do Tempo de Execução do Windows][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="b8448-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="b8448-110">Exemplos de código estão disponíveis em JavaScript e também em C++, C# e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b8448-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a><span data-ttu-id="b8448-111">Escrevendo componentes do Windows Runtime em C++, C# ou Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b8448-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="b8448-112">Para obter instruções e diretrizes para escrever componentes do Windows Runtime que podem ser consumidos no JavaScript, consulte Criando componentes do Tempo de Execução do Windows em [C++][WindowsUwpWinrtCpp] e Criando componentes do Tempo de Execução do [Windows em C#][WindowsUwpWinrtCsharpVb]e Visual Basic .</span><span class="sxs-lookup"><span data-stu-id="b8448-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <a name="casing-conventions-with-windows-runtime-features"></a><span data-ttu-id="b8448-113">Convenções de cobertura com recursos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b8448-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="b8448-114">As convenções de invólucro para recursos do Windows Runtime em JavaScript diferem ligeiramente das de outros idiomas:</span><span class="sxs-lookup"><span data-stu-id="b8448-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="b8448-115">Namespaces e classes estão no caso Pascal:</span><span class="sxs-lookup"><span data-stu-id="b8448-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="b8448-116">Membros de classes, incluindo métodos e propriedades e membros de estruturas e enumerações, estão em caso de camel:</span><span class="sxs-lookup"><span data-stu-id="b8448-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="b8448-117">Os nomes de eventos estão em menor caso:</span><span class="sxs-lookup"><span data-stu-id="b8448-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a><span data-ttu-id="b8448-118">Veja também</span><span class="sxs-lookup"><span data-stu-id="b8448-118">See also</span></span>  

[<span data-ttu-id="b8448-119">Considerações ao usar a API do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b8448-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="b8448-120">Usando Métodos Assíncronos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b8448-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="b8448-121">Lidando com de Eventos do Windows Runtime no JavaScript</span><span class="sxs-lookup"><span data-stu-id="b8448-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="b8448-122">Representação JavaScript de Tipos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b8448-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="b8448-123">Projeção JavaScript do Windows Runtime DateTime e TimeSpan</span><span class="sxs-lookup"><span data-stu-id="b8448-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
