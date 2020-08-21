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
# <span data-ttu-id="2eeae-102">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="2eeae-102">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="2eeae-103">Ao escrever um aplicativo da plataforma universal do Windows \ (UWP \), você pode usar as classes, métodos e propriedades do Windows Runtime da mesma forma que usaria objetos, métodos e propriedades JavaScript nativos.</span><span class="sxs-lookup"><span data-stu-id="2eeae-103">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="2eeae-104">Este tópico fornece informações introdutórias e links para tópicos que explicam os conceitos básicos do uso de APIs do tempo de execução do Windows em JavaScript, incluindo uma explicação sobre como os tipos do Windows Runtime são representados, como usar métodos assíncronos do Windows Runtime e como ouvir e manipular eventos do tempo de execução do Windows.</span><span class="sxs-lookup"><span data-stu-id="2eeae-104">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="2eeae-105">Para a documentação geral da linguagem, confira a biblioteca de [referência JavaScript][MDNJavascriptReference] do MDN.</span><span class="sxs-lookup"><span data-stu-id="2eeae-105">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="2eeae-106">Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2eeae-106">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="2eeae-107">Documentação de referência do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eeae-107">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="2eeae-108">Para obter documentação de referência, consulte [referência do tempo de execução do Windows][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="2eeae-108">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="2eeae-109">Exemplos de código estão disponíveis em JavaScript e também em C++, C# e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2eeae-109">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="2eeae-110">Gravando componentes do tempo de execução do Windows em C++, C# ou Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2eeae-110">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="2eeae-111">Para obter instruções e diretrizes para escrever componentes do tempo de execução do Windows que podem ser consumidos em JavaScript, consulte [criando componentes do tempo de execução do Windows em C++][WindowsUwpWinrtCpp] e [criando componentes do tempo de execução do Windows em C# e Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="2eeae-111">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="2eeae-112">Convenções de maiúsculas e minúsculas com recursos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eeae-112">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="2eeae-113">As convenções de maiúsculas e minúsculas para recursos do tempo de execução do Windows em JavaScript são ligeiramente diferentes das outras linguagens:</span><span class="sxs-lookup"><span data-stu-id="2eeae-113">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="2eeae-114">Namespaces e classes estão em casos Pascal:</span><span class="sxs-lookup"><span data-stu-id="2eeae-114">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="2eeae-115">Membros de classes, incluindo métodos e propriedades, e membros de estruturas e enumerações, estão em camel case:</span><span class="sxs-lookup"><span data-stu-id="2eeae-115">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="2eeae-116">Os nomes dos eventos são em minúsculas:</span><span class="sxs-lookup"><span data-stu-id="2eeae-116">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="2eeae-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2eeae-117">See also</span></span>  

[<span data-ttu-id="2eeae-118">Considerações ao usar a API do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eeae-118">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="2eeae-119">Usando Métodos Assíncronos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eeae-119">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="2eeae-120">Lidando com de Eventos do Windows Runtime no JavaScript</span><span class="sxs-lookup"><span data-stu-id="2eeae-120">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="2eeae-121">Representação JavaScript de Tipos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eeae-121">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="2eeae-122">Projeção JavaScript de DateTime e TimeSpan do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="2eeae-122">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
