---
title: Considerações ao usar a API do Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 95b082e27c4f247b841a9540e13bd49bd4c8bd67
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562526"
---
# <span data-ttu-id="9e04e-102">Considerações ao usar a API do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="9e04e-102">Considerations when Using the Windows Runtime API</span></span>  

<span data-ttu-id="9e04e-103">Você pode usar praticamente todos os elementos da API do tempo de execução do Windows em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e04e-103">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="9e04e-104">No entanto, há alguns aspectos da representação JavaScript dos elementos do tempo de execução do Windows que você deve ter em mente.</span><span class="sxs-lookup"><span data-stu-id="9e04e-104">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9e04e-105">Para obter informações sobre como criar componentes do tempo de execução do Windows em C++, C# ou Visual Basic e consumindo-os em JavaScript, consulte [criando componentes do tempo de execução do Windows em c++][WindowsUwpComponentsCreatingCpp] e [criando componentes do tempo de execução do Windows em C# e Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="9e04e-105">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="9e04e-106">Casos especiais na representação JavaScript de tipos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="9e04e-106">Special Cases in the JavaScript Representation of Windows Runtime Types</span></span>  

*   <span data-ttu-id="9e04e-107">Cadeias de caracteres: uma cadeia de caracteres não inicializada é passada para um método do Windows Runtime como a cadeia de caracteres "undefined", e uma cadeia de caracteres `null` é passada como a cadeia de caracteres "NULL".</span><span class="sxs-lookup"><span data-stu-id="9e04e-107">Strings: An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="9e04e-108">\ (Isso é verdade sempre que `null` um `undefined` valor ou for forçado para uma cadeia de caracteres. \) antes de passar uma cadeia de caracteres para um método do tempo de execução do Windows, você deve inicializá-la como uma cadeia de caracteres vazia \ ("" \).</span><span class="sxs-lookup"><span data-stu-id="9e04e-108">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
*   <span data-ttu-id="9e04e-109">Interfaces: não é possível implementar uma interface do tempo de execução do Windows em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e04e-109">Interfaces: You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
*   <span data-ttu-id="9e04e-110">Matrizes: as matrizes do tempo de execução do Windows não são redimensionáveis, portanto métodos que redimensionam matrizes em JavaScript não funcionam em matrizes do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="9e04e-110">Arrays: Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
*   <span data-ttu-id="9e04e-111">Matrizes: se você passar um valor de matriz JavaScript para um método do tempo de execução do Windows, a matriz será copiada.</span><span class="sxs-lookup"><span data-stu-id="9e04e-111">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="9e04e-112">O método do tempo de execução do Windows não pode modificar a matriz nem seus membros e devolvê-los ao seu aplicativo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e04e-112">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="9e04e-113">No entanto, você pode usar matrizes tipadas \ (por exemplo, [Int32Array objeto][MDNInt32array]\), que não são copiadas.</span><span class="sxs-lookup"><span data-stu-id="9e04e-113">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
*   <span data-ttu-id="9e04e-114">Estruturas: estruturas do tempo de execução do Windows são objetos em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e04e-114">Structures: Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="9e04e-115">Se você quiser passar uma estrutura do tempo de execução do Windows para um método do tempo de execução do Windows, não instancie a estrutura com a `new` palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="9e04e-115">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="9e04e-116">Em vez disso, crie um objeto e adicione os membros relevantes e seus valores.</span><span class="sxs-lookup"><span data-stu-id="9e04e-116">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="9e04e-117">Os nomes dos membros devem estar no camel case: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="9e04e-117">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
*   <span data-ttu-id="9e04e-118">Objetos: objetos JavaScript não são iguais a objetos de código gerenciados \ ( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="9e04e-118">Objects: JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="9e04e-119">Você não pode passar um objeto JavaScript para um método do tempo de execução do Windows que exija um `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="9e04e-119">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
*   <span data-ttu-id="9e04e-120">Identidade do objeto: na maioria dos casos, os objetos passados de volta e para trás entre o Windows Runtime e o JavaScript não são alterados.</span><span class="sxs-lookup"><span data-stu-id="9e04e-120">Object identity: In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="9e04e-121">O mecanismo JavaScript mantém um mapa de objetos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="9e04e-121">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="9e04e-122">Quando um objeto é retornado do tempo de execução do Windows, ele corresponde ao mapa e, se ele não existir, um novo objeto será criado.</span><span class="sxs-lookup"><span data-stu-id="9e04e-122">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="9e04e-123">O mesmo procedimento é seguido para objetos que representam interfaces que são retornadas por métodos do tempo de execução do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e04e-123">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="9e04e-124">Há dois tipos de exceções:</span><span class="sxs-lookup"><span data-stu-id="9e04e-124">There are two kinds of exceptions:</span></span>  

    *   <span data-ttu-id="9e04e-125">Os objetos retornados de uma chamada do tempo de execução do Windows e, em seguida, têm novas propriedades \ (expando \) adicionadas, não mantêm suas novas propriedades quando são passados para o tempo de execução do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e04e-125">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="9e04e-126">No entanto, quando eles são retornados ao aplicativo JavaScript, porque eles são correspondentes ao objeto existente, o objeto retornado tem as propriedades expando.</span><span class="sxs-lookup"><span data-stu-id="9e04e-126">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
    *   <span data-ttu-id="9e04e-127">Estruturas e representantes no Windows Runtime não podem ser identificados como idênticos a estruturas ou representantes usados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9e04e-127">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="9e04e-128">Toda vez que uma estrutura ou representante é retornado, ele recebe uma nova referência.</span><span class="sxs-lookup"><span data-stu-id="9e04e-128">Every time a structure or delegate is returned, it gets a new reference.</span></span>  

*   <span data-ttu-id="9e04e-129">Colisões de nomes: várias interfaces do tempo de execução do Windows podem ter membros com os mesmos nomes.</span><span class="sxs-lookup"><span data-stu-id="9e04e-129">Name collisions: Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="9e04e-130">Se eles forem combinados em um único objeto JavaScript (que pode ser uma representação de uma classe de tempo de execução ou uma interface), os membros serão representados com nomes totalmente qualificados.</span><span class="sxs-lookup"><span data-stu-id="9e04e-130">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="9e04e-131">Você pode chamar esses membros usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="9e04e-131">You can call these members by using the following syntax:</span></span>  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    <span data-ttu-id="9e04e-132">No código a seguir, duas interfaces têm um método Draw, e uma classe de tempo de execução implementa ambas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="9e04e-132">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
    
    ```cpp
    namespace CollisionExample {
        interface InterfaceA
        {
            HRESULT Draw([in] Int32 a);
        }
        interface InterfaceB
        {
            HRESULT Draw([in] HString a);
        }
        runtimeclass ExampleObject {
          interface InterfaceA
          interface InterfaceB
        }
    }
    ```  
    
    <span data-ttu-id="9e04e-133">Veja como você pode chamar o código acima em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e04e-133">Here is how you can call the above code in JavaScript.</span></span>  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` <span data-ttu-id="9e04e-134">parâmetros: se um método do tempo de execução do Windows tem vários `out` parâmetros, em JavaScript, o método tem um objeto JavaScript como valor de retorno, e o objeto tem propriedades que correspondem ao `out` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e04e-134">parameters: If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="9e04e-135">Por exemplo, considere a seguinte assinatura do Windows Runtime em C++.</span><span class="sxs-lookup"><span data-stu-id="9e04e-135">For example, consider the following Windows Runtime signature in C++.</span></span>  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    <span data-ttu-id="9e04e-136">A versão JavaScript dessa assinatura é:</span><span class="sxs-lookup"><span data-stu-id="9e04e-136">The JavaScript version of this signature is:</span></span>  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    <span data-ttu-id="9e04e-137">Neste exemplo, `returnValue` é um objeto JavaScript que tem dois campos: `first` e `second` .</span><span class="sxs-lookup"><span data-stu-id="9e04e-137">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
    
*   <span data-ttu-id="9e04e-138">Membros estáticos: o tempo de execução do Windows define membros estáticos e membros de instância.</span><span class="sxs-lookup"><span data-stu-id="9e04e-138">Static members: The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="9e04e-139">Em JavaScript, os membros estáticos são adicionados ao objeto associado à classe ou interface do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="9e04e-139">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
<span data-ttu-id="9e04e-140">Para obter mais informações sobre a representação JavaScript dos tipos básicos do Windows Runtime, consulte [representação JavaScript de tipos do tempo de execução do Windows][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="9e04e-140">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Representação JavaScript de tipos do Windows Runtime"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do tempo de execução do Windows com C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do tempo de execução do Windows com C# e Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  