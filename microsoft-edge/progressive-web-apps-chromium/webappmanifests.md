---
title: Usar o manifesto do aplicativo Web para integrar seu aplicativo Web progressivo ao sistema operacional
description: Saiba como usar o manifesto do aplicativo Web para integrar seu aplicativo Web progressivo ao sistema operacional.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659290"
---
# <span data-ttu-id="d0e94-104">Usar o manifesto do aplicativo Web para integrar seu aplicativo Web progressivo ao sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d0e94-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="d0e94-105">Um manifesto de aplicativo Web de um site rege a aparência do seu aplicativo Web progressivo \ (PWA \) e se comporta quando instalado em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0e94-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="d0e94-106">No nível mais básico, o manifesto fornece detalhes sobre o nome do seu aplicativo, ícones a serem usados para representar seu aplicativo em menus do sistema e as cores do tema que o sistema operacional \ (OS \) usa na barra de título.</span><span class="sxs-lookup"><span data-stu-id="d0e94-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="d0e94-107">O manifesto também permite desbloquear recursos avançados que permitem que seu aplicativo se comporte como outros aplicativos nativos no sistema.</span><span class="sxs-lookup"><span data-stu-id="d0e94-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <span data-ttu-id="d0e94-108">Usar atalhos para fornecer acesso rápido aos recursos</span><span class="sxs-lookup"><span data-stu-id="d0e94-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="d0e94-109">A maioria dos sistemas operacionais fornece acesso rápido aos principais recursos do aplicativo usando atalhos no menu de contexto conectado ao ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0e94-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="d0e94-110">Para usar atalhos no PWA, inclua a `shortcuts` propriedade no manifesto do seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d0e94-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="d0e94-111">O trecho de código a seguir mostra como definir um atalho em seu manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d0e94-111">The following code snippet shows how to define a shortcut in your web app manifest.</span></span>  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

<span data-ttu-id="d0e94-112">Quando adicionado a um manifesto completo do aplicativo Web, adicionar o trecho de código anterior habilita dois atalhos no menu de contexto no ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0e94-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="d0e94-113">O primeiro é nomeado `Play Later` e tem um ícone personalizado.</span><span class="sxs-lookup"><span data-stu-id="d0e94-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="d0e94-114">O segundo é nomeado `Subscriptions` e não tem um ícone porque a `icons` propriedade é opcional.</span><span class="sxs-lookup"><span data-stu-id="d0e94-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="d0e94-115">A `description` propriedade também é opcional e pode ser usada para fornecer informações adicionais para fins de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="d0e94-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <span data-ttu-id="d0e94-116">Identifique o aplicativo como um destino de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d0e94-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="d0e94-117">Muitos sistemas operacionais permitem que os usuários compartilhem rapidamente links e arquivos com aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="d0e94-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="d0e94-118">Aplicativos Web progressivos também podem participar desse recurso, por meio do `share_target` membro do manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d0e94-118">Progressive Web Apps can participate in this feature as well, via the `share_target` member of the Web App Manifest.</span></span> <span data-ttu-id="d0e94-119">Usando share_target, você define a página "ação" (semelhante a um formulário) e os parâmetros que espera que sejam passados para ele.</span><span class="sxs-lookup"><span data-stu-id="d0e94-119">Using share_target, you define the "action" page (similar to a form) and the parameters you expect to be passed into it.</span></span> <span data-ttu-id="d0e94-120">O trecho de código a seguir mostra um exemplo de como usar `share_target` .</span><span class="sxs-lookup"><span data-stu-id="d0e94-120">The following code snippet shows an example of how to use `share_target`.</span></span>

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

<span data-ttu-id="d0e94-121">Quando adicionado ao manifesto do aplicativo Web, isso estabelece "/share.html" como a página de ação para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d0e94-121">When added to the Web App Manifest, this establishes "/share.html" as the action page for a share.</span></span> <span data-ttu-id="d0e94-122">Além disso, ele define três parâmetros que seriam passados para essa página de ação: "título", "texto" e "URL".</span><span class="sxs-lookup"><span data-stu-id="d0e94-122">Additionally, it defines three parameters that would be passed to that action page: "title", "text", and "url".</span></span> <span data-ttu-id="d0e94-123">Esses parâmetros serão armazenados nas propriedades "nome", "Descrição" e "link" do objeto [ShareData](https://wicg.github.io/web-share#dom-sharedata) .</span><span class="sxs-lookup"><span data-stu-id="d0e94-123">These parameters will be stored in the [ShareData](https://wicg.github.io/web-share#dom-sharedata) object’s "name", "description", and "link" properties.</span></span> <span data-ttu-id="d0e94-124">Por padrão, a página de ação recebe esses parâmetros como parte de uma solicitação GET, mas você pode especificar a solicitação `method` e a codificação \ (as `enctype` \), da mesma forma que faria em um formulário da Web.</span><span class="sxs-lookup"><span data-stu-id="d0e94-124">By default, the action page receives these parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <span data-ttu-id="d0e94-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0e94-125">See also</span></span>  

<span data-ttu-id="d0e94-126">Para saber mais sobre manifestos do aplicativo Web, consulte a lista de tópicos relacionados a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0e94-126">To learn more about Web App Manifests, see the following list of related topics.</span></span>  

* [<span data-ttu-id="d0e94-127">Manifestos do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d0e94-127">Web App Manifests</span></span>][MDNWebAppManifests]  
* [<span data-ttu-id="d0e94-128">Destino do compartilhamento da Web</span><span class="sxs-lookup"><span data-stu-id="d0e94-128">Web Share Target</span></span>][WICGShareTarget]
* [<span data-ttu-id="d0e94-129">Compartilhamento na Web</span><span class="sxs-lookup"><span data-stu-id="d0e94-129">Web Share</span></span>][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestos do aplicativo Web | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "API de destino do compartilhamento da Web | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API de compartilhamento na Web | WICG"
