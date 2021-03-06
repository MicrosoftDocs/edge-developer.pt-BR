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
# <a name="considerations-when-using-the-windows-runtime-api"></a>Considerações ao usar a API do Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Você pode usar quase todos os elementos da API do Windows Runtime em JavaScript.  No entanto, há alguns aspectos da representação JavaScript dos elementos do Windows Runtime que você deve ter em mente.  

> [!IMPORTANT]
> Para obter informações sobre como criar componentes do Windows Runtime em C++, C# ou Visual Basic e consumi-los em JavaScript, consulte [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a>Casos especiais na Representação JavaScript de tipos do Windows Runtime  

:::row:::
   :::column span="1":::
      Cadeias de caracteres  
   :::column-end:::
   :::column span="3":::
      Uma cadeia de caracteres não unificada é passada para um método do Windows Runtime como a cadeia de caracteres "indefinida", e um conjunto de cadeias de caracteres é passado como a `null` cadeia de caracteres "null".  \(Isso é verdadeiro sempre que um ou valor é coagido a uma cadeia de caracteres.\) Antes de passar uma cadeia de caracteres para um método do Windows Runtime, você deve inicializa-la como a cadeia de caracteres `null` `undefined` vazia \(""\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Interfaces  
   :::column-end:::
   :::column span="3":::
      Não é possível implementar uma interface do Windows Runtime em JavaScript.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Matrizes  
   :::column-end:::
   :::column span="3":::
      As matrizes do Windows Runtime não são resizáveis, portanto, os métodos que resizem matrizes em JavaScript não funcionam em matrizes do Windows Runtime.  
      *   Matrizes: se você passar um valor de matriz JavaScript para um método do Windows Runtime, a matriz será copiada.  O método Do Windows Runtime não é capaz de modificar a matriz ou seus membros e devolvê-la ao seu aplicativo JavaScript.  No entanto, você pode usar matrizes digitados \(por exemplo, [Objeto Int32Array][MDNInt32array]\), que não são copiadas.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Estruturas  
   :::column-end:::
   :::column span="3":::
      As estruturas do Windows Runtime são objetos em JavaScript.  Se você quiser passar uma estrutura do Windows Runtime para um método do Windows Runtime, não instaurem a estrutura com a `new` palavra-chave.  Em vez disso, crie um objeto e adicione os membros relevantes e seus valores.  Os nomes dos membros devem estar em caso de camel: `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Objetos  
   :::column-end:::
   :::column span="3":::
      Os objetos JavaScript não são iguais aos objetos de código gerenciado \( `System.Object` \).  Não é possível passar um objeto JavaScript para um método do Windows Runtime que exija um `System.Object` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Identidade do objeto  
   :::column-end:::
   :::column span="3":::
      Na maioria dos casos, os objetos passados para frente e para trás entre o Windows Runtime e JavaScript não mudam.  O mecanismo JavaScript mantém um mapa de objetos conhecidos.  Quando um objeto é retornado do Windows Runtime, ele é corresponder ao mapa e, se ele não existir, um novo objeto será criado.  O mesmo procedimento é seguido para objetos que representam interfaces retornadas pelos métodos do Windows Runtime.  Há dois tipos de exceções:  
      
      *   Os objetos retornados de uma chamada do Windows Runtime e, em seguida, têm novas propriedades \(expando\) adicionadas, não retêm suas novas propriedades quando são passadas de volta para o Windows Runtime.  No entanto, quando eles são retornados para o aplicativo JavaScript, porque eles são corresponder ao objeto existente, o objeto retornado tem as propriedades expando.  
      *   Estruturas e representantes no Windows Runtime não podem ser identificados como idênticos a estruturas ou representantes usados anteriormente.  Sempre que uma estrutura ou representante é retornada, ela obtém uma nova referência.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Colisões de nomes  
   :::column-end:::
   :::column span="3":::
      Várias interfaces do Windows Runtime podem ter membros com os mesmos nomes.  Se eles são combinados em um único objeto JavaScript (que pode ser uma representação de uma classe de tempo de execução ou uma interface), os membros serão representados com nomes totalmente qualificados.  Você pode chamar esses membros usando a seguinte sintaxe:  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      No código a seguir, duas interfaces têm um método Draw e uma classe de tempo de execução implementa ambas as interfaces.  
      
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
      
      Veja como você pode chamar o código acima em JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` parameters  
   :::column-end:::
   :::column span="3":::
      Se um método do Windows Runtime tiver vários parâmetros, em JavaScript, o método tem um objeto JavaScript como seu valor de retorno e o objeto tem propriedades que correspondem `out` ao `out` parâmetro.  Por exemplo, considere a seguinte assinatura do Windows Runtime em C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      A versão JavaScript dessa assinatura é:  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      Neste exemplo, `returnValue` é um objeto JavaScript que tem dois campos: e `first` `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Membros estáticos  
   :::column-end:::
   :::column span="3":::
      O Windows Runtime define membros estáticos e membros de instância.  Em JavaScript, membros estáticos são adicionados ao objeto associado à classe ou interface do Windows Runtime.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Para obter mais informações sobre a representação JavaScript de tipos básicos do Windows Runtime, consulte [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representação javascript de tipos de tempo de execução do Windows | Microsoft Docs"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do Windows Runtime com C++/CX | Microsoft Docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do Windows Runtime com C# e Visual Basic | Microsoft Docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
