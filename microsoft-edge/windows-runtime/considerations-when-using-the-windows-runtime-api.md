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
# Considerações ao usar a API do Windows Runtime  

Você pode usar praticamente todos os elementos da API do tempo de execução do Windows em JavaScript.  No entanto, há alguns aspectos da representação JavaScript dos elementos do tempo de execução do Windows que você deve ter em mente.  

> [!IMPORTANT]
> Para obter informações sobre como criar componentes do tempo de execução do Windows em C++, C# ou Visual Basic e consumindo-os em JavaScript, consulte [criando componentes do tempo de execução do Windows em c++][WindowsUwpComponentsCreatingCpp] e [criando componentes do tempo de execução do Windows em C# e Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## Casos especiais na representação JavaScript de tipos do Windows Runtime  

*   Cadeias de caracteres: uma cadeia de caracteres não inicializada é passada para um método do Windows Runtime como a cadeia de caracteres "undefined", e uma cadeia de caracteres `null` é passada como a cadeia de caracteres "NULL".  \ (Isso é verdade sempre que `null` um `undefined` valor ou for forçado para uma cadeia de caracteres. \) antes de passar uma cadeia de caracteres para um método do tempo de execução do Windows, você deve inicializá-la como uma cadeia de caracteres vazia \ ("" \).  
*   Interfaces: não é possível implementar uma interface do tempo de execução do Windows em JavaScript.  
*   Matrizes: as matrizes do tempo de execução do Windows não são redimensionáveis, portanto métodos que redimensionam matrizes em JavaScript não funcionam em matrizes do Windows Runtime.  
*   Matrizes: se você passar um valor de matriz JavaScript para um método do tempo de execução do Windows, a matriz será copiada.  O método do tempo de execução do Windows não pode modificar a matriz nem seus membros e devolvê-los ao seu aplicativo JavaScript.  No entanto, você pode usar matrizes tipadas \ (por exemplo, [Int32Array objeto][MDNInt32array]\), que não são copiadas.  
*   Estruturas: estruturas do tempo de execução do Windows são objetos em JavaScript.  Se você quiser passar uma estrutura do tempo de execução do Windows para um método do tempo de execução do Windows, não instancie a estrutura com a `new` palavra-chave.  Em vez disso, crie um objeto e adicione os membros relevantes e seus valores.  Os nomes dos membros devem estar no camel case: `SomeStruct.firstMember` .  
*   Objetos: objetos JavaScript não são iguais a objetos de código gerenciados \ ( `System.Object` \).  Você não pode passar um objeto JavaScript para um método do tempo de execução do Windows que exija um `System.Object` .  
*   Identidade do objeto: na maioria dos casos, os objetos passados de volta e para trás entre o Windows Runtime e o JavaScript não são alterados.  O mecanismo JavaScript mantém um mapa de objetos conhecidos.  Quando um objeto é retornado do tempo de execução do Windows, ele corresponde ao mapa e, se ele não existir, um novo objeto será criado.  O mesmo procedimento é seguido para objetos que representam interfaces que são retornadas por métodos do tempo de execução do Windows.  Há dois tipos de exceções:  

    *   Os objetos retornados de uma chamada do tempo de execução do Windows e, em seguida, têm novas propriedades \ (expando \) adicionadas, não mantêm suas novas propriedades quando são passados para o tempo de execução do Windows.  No entanto, quando eles são retornados ao aplicativo JavaScript, porque eles são correspondentes ao objeto existente, o objeto retornado tem as propriedades expando.  
    *   Estruturas e representantes no Windows Runtime não podem ser identificados como idênticos a estruturas ou representantes usados anteriormente.  Toda vez que uma estrutura ou representante é retornado, ele recebe uma nova referência.  

*   Colisões de nomes: várias interfaces do tempo de execução do Windows podem ter membros com os mesmos nomes.  Se eles forem combinados em um único objeto JavaScript (que pode ser uma representação de uma classe de tempo de execução ou uma interface), os membros serão representados com nomes totalmente qualificados.  Você pode chamar esses membros usando a seguinte sintaxe:  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    No código a seguir, duas interfaces têm um método Draw, e uma classe de tempo de execução implementa ambas as interfaces.  
    
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
    
*   `Out` parâmetros: se um método do tempo de execução do Windows tem vários `out` parâmetros, em JavaScript, o método tem um objeto JavaScript como valor de retorno, e o objeto tem propriedades que correspondem ao `out` parâmetro.  Por exemplo, considere a seguinte assinatura do Windows Runtime em C++.  
    
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
    
    Neste exemplo, `returnValue` é um objeto JavaScript que tem dois campos: `first` e `second` .  
    
*   Membros estáticos: o tempo de execução do Windows define membros estáticos e membros de instância.  Em JavaScript, os membros estáticos são adicionados ao objeto associado à classe ou interface do Windows Runtime.  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
Para obter mais informações sobre a representação JavaScript dos tipos básicos do Windows Runtime, consulte [representação JavaScript de tipos do tempo de execução do Windows][WindowsRuntimeJavascriptTypes].  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Representação JavaScript de tipos do Windows Runtime"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes do tempo de execução do Windows com C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes do tempo de execução do Windows com C# e Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  