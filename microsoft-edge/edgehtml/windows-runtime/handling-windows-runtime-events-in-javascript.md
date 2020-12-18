---
description: Manipular eventos do tempo de execução do Windows em JavaScript.
title: Lidando com de Eventos do Windows Runtime no JavaScript
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
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e0a3e35c908c766c0308903381b271f5ccdb27a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231788"
---
# <span data-ttu-id="75e93-103">Manipulação de eventos do Windows Runtime no JavaScript</span><span class="sxs-lookup"><span data-stu-id="75e93-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="75e93-104">Os eventos do tempo de execução do Windows não são representados da mesma maneira em JavaScript como se estivessem em C++ ou no .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="75e93-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="75e93-105">Elas não são propriedades de classe, mas, em vez disso, são representadas como identificadores de cadeias de caracteres de classe \ (minúscula \) passados para `addEventListener` `removeEventListener` métodos e métodos.</span><span class="sxs-lookup"><span data-stu-id="75e93-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="75e93-106">Por exemplo, você pode adicionar um manipulador de eventos para o evento [geolocator. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] passando a cadeia de caracteres `positionchanged` para o `Geolocator.addEventListener` método:</span><span class="sxs-lookup"><span data-stu-id="75e93-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="75e93-107">Você também pode definir a `locator.onpositionchanged` Propriedade:</span><span class="sxs-lookup"><span data-stu-id="75e93-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="75e93-108">Outra diferença entre .NET/C++ e JavaScript é o número de parâmetros utilizados por um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="75e93-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="75e93-109">Em .NET/C++, um manipulador leva dois: o remetente do evento e os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="75e93-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="75e93-110">Em JavaScript, os dois são agrupados como um único `Event` objeto.</span><span class="sxs-lookup"><span data-stu-id="75e93-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="75e93-111">No exemplo a seguir, o `ev` parâmetro contém o remetente do evento \ (a `target` Propriedade \) e as propriedades de dados do evento \ (aqui, apenas `position` \).</span><span class="sxs-lookup"><span data-stu-id="75e93-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="75e93-112">As propriedades de dados de evento são aquelas documentadas para cada evento.</span><span class="sxs-lookup"><span data-stu-id="75e93-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="75e93-113">Os recursos do tempo de execução do Windows não estão disponíveis para aplicativos que são executados no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="75e93-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="75e93-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="75e93-114">See also</span></span>  

[<span data-ttu-id="75e93-115">Usando o Tempo de Execução do Windows no JavaScript</span><span class="sxs-lookup"><span data-stu-id="75e93-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar o tempo de execução do Windows em JavaScript | Documentos da Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe geolocator | Documentos da Microsoft"  
