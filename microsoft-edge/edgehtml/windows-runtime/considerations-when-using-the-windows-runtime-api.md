---
description: Considerações ao usar a API do Windows Runtime
title: Considerações ao usar a API do Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 170374fd109802bff0aa0fc93cea6c8d50c9d7c7
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399341"
---
# <a name="considerations-when-using-the-windows-runtime-api"></a><span data-ttu-id="dcb3a-103">Considerações ao usar a API do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="dcb3a-103">Considerations when using the Windows Runtime API</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="dcb3a-104">Você pode usar quase todos os elementos da API do Windows Runtime em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-104">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="dcb3a-105">No entanto, há alguns aspectos da representação JavaScript dos elementos do Windows Runtime que você deve ter em mente.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-105">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="dcb3a-106">Para obter informações sobre como criar componentes do Windows Runtime em C++, C# ou Visual Basic e consumi-los em JavaScript, consulte [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="dcb3a-106">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a><span data-ttu-id="dcb3a-107">Casos especiais na Representação JavaScript de tipos do Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="dcb3a-107">Special cases in the JavaScript Representation of Windows Runtime types</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-108">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="dcb3a-108">Strings</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-109">Uma cadeia de caracteres não unificada é passada para um método do Windows Runtime como a cadeia de caracteres "indefinida", e um conjunto de cadeias de caracteres é passado como a `null` cadeia de caracteres "null".</span><span class="sxs-lookup"><span data-stu-id="dcb3a-109">An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="dcb3a-110">\(Isso é verdadeiro sempre que um ou valor é coagido a uma cadeia de caracteres.\) Antes de passar uma cadeia de caracteres para um método do Windows Runtime, você deve inicializa-la como a cadeia de caracteres `null` `undefined` vazia \(""\).</span><span class="sxs-lookup"><span data-stu-id="dcb3a-110">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="dcb3a-111">Interfaces</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-112">Não é possível implementar uma interface do Windows Runtime em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-112">You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-113">Matrizes</span><span class="sxs-lookup"><span data-stu-id="dcb3a-113">Arrays</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-114">As matrizes do Windows Runtime não são resizáveis, portanto, os métodos que resizem matrizes em JavaScript não funcionam em matrizes do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-114">Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
      *   <span data-ttu-id="dcb3a-115">Matrizes: se você passar um valor de matriz JavaScript para um método do Windows Runtime, a matriz será copiada.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-115">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="dcb3a-116">O método Do Windows Runtime não é capaz de modificar a matriz ou seus membros e devolvê-la ao seu aplicativo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-116">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="dcb3a-117">No entanto, você pode usar matrizes digitados \(por exemplo, [Objeto Int32Array][MDNInt32array]\), que não são copiadas.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-117">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-118">Estruturas</span><span class="sxs-lookup"><span data-stu-id="dcb3a-118">Structures</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-119">As estruturas do Windows Runtime são objetos em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-119">Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="dcb3a-120">Se você quiser passar uma estrutura do Windows Runtime para um método do Windows Runtime, não instaurem a estrutura com a `new` palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-120">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="dcb3a-121">Em vez disso, crie um objeto e adicione os membros relevantes e seus valores.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-121">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="dcb3a-122">Os nomes dos membros devem estar em caso de camel: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="dcb3a-122">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-123">Objetos</span><span class="sxs-lookup"><span data-stu-id="dcb3a-123">Objects</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-124">Os objetos JavaScript não são iguais aos objetos de código gerenciado \( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="dcb3a-124">JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="dcb3a-125">Não é possível passar um objeto JavaScript para um método do Windows Runtime que exija um `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="dcb3a-125">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-126">Identidade do objeto</span><span class="sxs-lookup"><span data-stu-id="dcb3a-126">Object identity</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-127">Na maioria dos casos, os objetos passados para frente e para trás entre o Windows Runtime e JavaScript não mudam.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-127">In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="dcb3a-128">O mecanismo JavaScript mantém um mapa de objetos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-128">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="dcb3a-129">Quando um objeto é retornado do Windows Runtime, ele é corresponder ao mapa e, se ele não existir, um novo objeto será criado.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-129">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="dcb3a-130">O mesmo procedimento é seguido para objetos que representam interfaces retornadas pelos métodos do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-130">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="dcb3a-131">Há dois tipos de exceções:</span><span class="sxs-lookup"><span data-stu-id="dcb3a-131">There are two kinds of exceptions:</span></span>  
      
      *   <span data-ttu-id="dcb3a-132">Os objetos retornados de uma chamada do Windows Runtime e, em seguida, têm novas propriedades \(expando\) adicionadas, não retêm suas novas propriedades quando são passadas de volta para o Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-132">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="dcb3a-133">No entanto, quando eles são retornados para o aplicativo JavaScript, porque eles são corresponder ao objeto existente, o objeto retornado tem as propriedades expando.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-133">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
      *   <span data-ttu-id="dcb3a-134">Estruturas e representantes no Windows Runtime não podem ser identificados como idênticos a estruturas ou representantes usados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-134">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="dcb3a-135">Sempre que uma estrutura ou representante é retornada, ela obtém uma nova referência.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-135">Every time a structure or delegate is returned, it gets a new reference.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-136">Colisões de nomes</span><span class="sxs-lookup"><span data-stu-id="dcb3a-136">Name collisions</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-137">Várias interfaces do Windows Runtime podem ter membros com os mesmos nomes.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-137">Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="dcb3a-138">Se eles são combinados em um único objeto JavaScript (que pode ser uma representação de uma classe de tempo de execução ou uma interface), os membros serão representados com nomes totalmente qualificados.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-138">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="dcb3a-139">Você pode chamar esses membros usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="dcb3a-139">You can call these members by using the following syntax:</span></span>  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      <span data-ttu-id="dcb3a-140">No código a seguir, duas interfaces têm um método Draw e uma classe de tempo de execução implementa ambas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-140">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
      
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
      
      <span data-ttu-id="dcb3a-141">Veja como você pode chamar o código acima em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-141">Here is how you can call the above code in JavaScript.</span></span>  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` <span data-ttu-id="dcb3a-142">parameters</span><span class="sxs-lookup"><span data-stu-id="dcb3a-142">parameters</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-143">Se um método do Windows Runtime tiver vários parâmetros, em JavaScript, o método tem um objeto JavaScript como seu valor de retorno e o objeto tem propriedades que correspondem `out` ao `out` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-143">If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="dcb3a-144">Por exemplo, considere a seguinte assinatura do Windows Runtime em C++.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-144">For example, consider the following Windows Runtime signature in C++.</span></span>  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      <span data-ttu-id="dcb3a-145">A versão JavaScript dessa assinatura é:</span><span class="sxs-lookup"><span data-stu-id="dcb3a-145">The JavaScript version of this signature is:</span></span>  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      <span data-ttu-id="dcb3a-146">Neste exemplo, `returnValue` é um objeto JavaScript que tem dois campos: e `first` `second` .</span><span class="sxs-lookup"><span data-stu-id="dcb3a-146">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="dcb3a-147">Membros estáticos</span><span class="sxs-lookup"><span data-stu-id="dcb3a-147">Static members</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="dcb3a-148">O Windows Runtime define membros estáticos e membros de instância.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-148">The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="dcb3a-149">Em JavaScript, membros estáticos são adicionados ao objeto associado à classe ou interface do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="dcb3a-149">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
<span data-ttu-id="dcb3a-150">Para obter mais informações sobre a representação JavaScript de tipos básicos do Windows Runtime, consulte [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="dcb3a-150">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representação javascript de tipos de tempo de execução do Windows | Microsoft Docs"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do Windows Runtime com C++/CX | Microsoft Docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do Windows Runtime com C# e Visual Basic | Microsoft Docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
