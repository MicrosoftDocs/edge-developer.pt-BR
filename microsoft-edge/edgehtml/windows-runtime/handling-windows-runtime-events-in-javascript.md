---
description: Lidando com de Eventos do Windows Runtime no JavaScript
title: Lidando com de Eventos do Windows Runtime no JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 08562f7ebff0c02b96bfc8229238a62463b95451
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397521"
---
# <a name="handling-windows-runtime-events-in-javascript"></a>Manipulação de eventos do Windows Runtime no JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Os eventos do Windows Runtime não são representados da mesma maneira no JavaScript, como no C++ ou no .NET Framework.  Elas não são propriedades de classe, mas são representadas como identificadores de cadeia de caracteres \(minúsculas\) que são passados para os métodos e da `addEventListener` `removeEventListener` classe.  Por exemplo, você pode adicionar um manipulador de eventos para o [evento Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] passando a cadeia de caracteres `positionchanged` para o `Geolocator.addEventListener` método:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Você também pode definir a `locator.onpositionchanged` propriedade:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Outra diferença entre .NET/C++ e JavaScript é o número de parâmetros tomados por um manipulador de eventos.  Em .NET/C++, um manipulador leva dois: o remetente do evento e os dados do evento.  Em JavaScript, os dois são agrupados como um único `Event` objeto.  No exemplo a seguir, o parâmetro contém o remetente do evento \(a propriedade\) e as propriedades de dados do evento `ev` `target` \(aqui, apenas `position` \).  As propriedades de dados do evento são as que estão documentadas para cada evento.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Os recursos do Windows Runtime não estão disponíveis para aplicativos executados no Internet Explorer.  

## <a name="see-also"></a>Veja também  

[Usando o Tempo de Execução do Windows no JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usando o Tempo de Execução do Windows no JavaScript | Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe Geolocator | Microsoft Docs"  
