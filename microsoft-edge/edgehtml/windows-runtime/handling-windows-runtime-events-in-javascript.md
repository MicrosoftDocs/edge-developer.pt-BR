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
# <a name="handling-windows-runtime-events-in-javascript"></a><span data-ttu-id="c8ac8-103">Manipulação de eventos do Windows Runtime no JavaScript</span><span class="sxs-lookup"><span data-stu-id="c8ac8-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="c8ac8-104">Os eventos do Windows Runtime não são representados da mesma maneira no JavaScript, como no C++ ou no .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="c8ac8-105">Elas não são propriedades de classe, mas são representadas como identificadores de cadeia de caracteres \(minúsculas\) que são passados para os métodos e da `addEventListener` `removeEventListener` classe.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="c8ac8-106">Por exemplo, você pode adicionar um manipulador de eventos para o [evento Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] passando a cadeia de caracteres `positionchanged` para o `Geolocator.addEventListener` método:</span><span class="sxs-lookup"><span data-stu-id="c8ac8-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="c8ac8-107">Você também pode definir a `locator.onpositionchanged` propriedade:</span><span class="sxs-lookup"><span data-stu-id="c8ac8-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="c8ac8-108">Outra diferença entre .NET/C++ e JavaScript é o número de parâmetros tomados por um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="c8ac8-109">Em .NET/C++, um manipulador leva dois: o remetente do evento e os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="c8ac8-110">Em JavaScript, os dois são agrupados como um único `Event` objeto.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="c8ac8-111">No exemplo a seguir, o parâmetro contém o remetente do evento \(a propriedade\) e as propriedades de dados do evento `ev` `target` \(aqui, apenas `position` \).</span><span class="sxs-lookup"><span data-stu-id="c8ac8-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="c8ac8-112">As propriedades de dados do evento são as que estão documentadas para cada evento.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="c8ac8-113">Os recursos do Windows Runtime não estão disponíveis para aplicativos executados no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c8ac8-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c8ac8-114">Veja também</span><span class="sxs-lookup"><span data-stu-id="c8ac8-114">See also</span></span>  

[<span data-ttu-id="c8ac8-115">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="c8ac8-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usando o Tempo de Execução do Windows no JavaScript | Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe Geolocator | Microsoft Docs"  
