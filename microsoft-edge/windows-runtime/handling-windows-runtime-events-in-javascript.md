---
title: Manipulando eventos do Windows Runtime em JavaScript
ms.custom: ''
ms.date: 04/01/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3db0116a3d464c75fe754e73e41ff1d154f928e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562522"
---
# Manipulando eventos do Windows Runtime em JavaScript  

Os eventos do tempo de execução do Windows não são representados da mesma maneira em JavaScript como se estivessem em C++ ou no .NET Framework.  Elas não são propriedades de classe, mas, em vez disso, são representadas como identificadores de cadeias de caracteres de classe \ (minúscula \) passados para `addEventListener` `removeEventListener` métodos e métodos.  Por exemplo, você pode adicionar um manipulador de eventos para o evento [geolocator. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] passando a cadeia de caracteres "PositionChanged" para o `Geolocator.addEventListener` método:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Você também pode definir a `locator.onpositionchanged` Propriedade:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Outra diferença entre .NET/C++ e JavaScript é o número de parâmetros utilizados por um manipulador de eventos.  Em .NET/C++, um manipulador leva dois: o remetente do evento e os dados do evento.  Em JavaScript, os dois são agrupados como um único `Event` objeto.  No exemplo a seguir, o `ev` parâmetro contém o remetente do evento \ (a `target` Propriedade \) e as propriedades de dados do evento \ (aqui, apenas `position` \).  As propriedades de dados de evento são aquelas documentadas para cada evento.  

```javascript
function (ev) {
    console.log("Sender:  " + ev.target);
    console.log("Position:  " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.  

## Consulte também  

[Usar o tempo de execução do Windows em JavaScript][WindowsRuntimeJavascript]  

 <!-- image links -->  

 <!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar o tempo de execução do Windows em JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe geolocator"  
