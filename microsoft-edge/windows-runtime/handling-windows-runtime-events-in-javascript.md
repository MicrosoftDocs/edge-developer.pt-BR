---
title: Lidando com de Eventos do Windows Runtime no JavaScript
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: fe44457206569c1e32c40514b4b186bec50d1e3c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942159"
---
# Manipulando eventos do Windows Runtime em JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Os eventos do tempo de execução do Windows não são representados da mesma maneira em JavaScript como se estivessem em C++ ou no .NET Framework.  Elas não são propriedades de classe, mas, em vez disso, são representadas como identificadores de cadeias de caracteres de classe \ (minúscula \) passados para `addEventListener` `removeEventListener` métodos e métodos.  Por exemplo, você pode adicionar um manipulador de eventos para o evento [geolocator. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] passando a cadeia de caracteres `positionchanged` para o `Geolocator.addEventListener` método:  

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
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.  

## Consulte também  

[Usando o Tempo de Execução do Windows no JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar o tempo de execução do Windows em JavaScript | Documentos da Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe geolocator | Documentos da Microsoft"  
