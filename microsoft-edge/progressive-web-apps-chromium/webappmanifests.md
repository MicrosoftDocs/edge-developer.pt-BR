---
title: Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao Sistema Operacional
description: Saiba como usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao sistema operacional.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Borda, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399096"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a><span data-ttu-id="79a48-104">Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="79a48-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="79a48-105">Um Manifesto do Aplicativo Web de um site rege a aparência e o comportamento do seu Aplicativo Web Progressivo \(PWA\) quando instalado em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79a48-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="79a48-106">No nível mais básico, o Manifesto fornece detalhes sobre o nome do seu aplicativo, ícones a ser usado para representar seu aplicativo nos menus do sistema e as cores de tema que o sistema operacional \(OS\) usa na barra de título.</span><span class="sxs-lookup"><span data-stu-id="79a48-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="79a48-107">O Manifesto também permite desbloquear recursos poderosos que permitem que seu aplicativo se comporte como outros aplicativos nativos no sistema.</span><span class="sxs-lookup"><span data-stu-id="79a48-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a><span data-ttu-id="79a48-108">Usar atalhos para fornecer acesso rápido aos recursos</span><span class="sxs-lookup"><span data-stu-id="79a48-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="79a48-109">A maioria dos sistemas operacionais fornece acesso rápido aos principais recursos do aplicativo usando atalhos no menu de contexto conectado ao ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79a48-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="79a48-110">Para usar atalhos no PWA, inclua a `shortcuts` propriedade no Manifesto do Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="79a48-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="79a48-111">O trecho de código a seguir exibe como definir um atalho no manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="79a48-111">The following code snippet displays how to define a shortcut in your web app manifest.</span></span>  

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

<span data-ttu-id="79a48-112">Quando adicionado a um Manifesto completo do Aplicativo Web, a adição do trecho de código anterior habilita dois atalhos no menu de contexto no ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79a48-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="79a48-113">O primeiro é nomeado `Play Later` e tem um ícone personalizado.</span><span class="sxs-lookup"><span data-stu-id="79a48-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="79a48-114">O segundo é nomeado `Subscriptions` e não tem um ícone porque a propriedade é `icons` opcional.</span><span class="sxs-lookup"><span data-stu-id="79a48-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="79a48-115">A `description` propriedade também é opcional e pode ser usada para fornecer informações adicionais para fins de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="79a48-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <a name="identify-your-app-as-a-share-target"></a><span data-ttu-id="79a48-116">Identificar seu aplicativo como um Destino de Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="79a48-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="79a48-117">Muitos sistemas operacionais permitem que os usuários compartilhem rapidamente links e arquivos com aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="79a48-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="79a48-118">Os Aplicativos Web Progressivos também podem participar desse recurso, usando o `share_target` membro do Manifesto do Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="79a48-118">Progressive Web Apps can participate in this feature as well, using the `share_target` member of the Web App Manifest.</span></span>  <span data-ttu-id="79a48-119">Usando `share_target` , você define a página `"action"` \(semelhante a um formulário\) e os parâmetros que você espera que sejam passados para ela.</span><span class="sxs-lookup"><span data-stu-id="79a48-119">Using `share_target`, you define the `"action"` page \(similar to a form\) and the parameters you expect to be passed into it.</span></span>  <span data-ttu-id="79a48-120">O trecho de código a seguir exibe um exemplo de como usar `share_target` .</span><span class="sxs-lookup"><span data-stu-id="79a48-120">The following code snippet displays an example of how to use `share_target`.</span></span>

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

<span data-ttu-id="79a48-121">Quando adicionado ao Manifesto do Aplicativo Web, isso se estabelece `"/share.html"` como a página de ação de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="79a48-121">When added to the Web App Manifest, this establishes `"/share.html"` as the action page for a share.</span></span> <span data-ttu-id="79a48-122">Além disso, define três parâmetros que seriam passados para essa página de ação: `"title"` , `"text"` e `"url"` .</span><span class="sxs-lookup"><span data-stu-id="79a48-122">Additionally, it defines three parameters that would be passed to that action page:`"title"`, `"text"`, and `"url"`.</span></span>  <span data-ttu-id="79a48-123">Esses parâmetros serão armazenados nas `"name"` propriedades , e do objeto `"description"` `"link"` [ShareData.][GitHubWicgWebShareDomSharedata]</span><span class="sxs-lookup"><span data-stu-id="79a48-123">These parameters will be stored in the `"name"`, `"description"`, and `"link"` properties of the [ShareData][GitHubWicgWebShareDomSharedata] object.</span></span>  <span data-ttu-id="79a48-124">Por padrão, a página de ação recebe os parâmetros como parte de uma solicitação GET, mas você pode especificar a solicitação e codificação \(como \), assim como faria em um `method` `enctype` formulário da Web.</span><span class="sxs-lookup"><span data-stu-id="79a48-124">By default, the action page receives the parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <a name="see-also"></a><span data-ttu-id="79a48-125">Veja também</span><span class="sxs-lookup"><span data-stu-id="79a48-125">See also</span></span>  

<span data-ttu-id="79a48-126">Para saber mais sobre Manifestos de Aplicativo Web, navegue até a lista a seguir de tópicos relacionados.</span><span class="sxs-lookup"><span data-stu-id="79a48-126">To learn more about Web App Manifests, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="79a48-127">Manifestos do Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="79a48-127">Web App Manifests</span></span>][MDNWebAppManifests]  
*   [<span data-ttu-id="79a48-128">Destino do Compartilhamento web</span><span class="sxs-lookup"><span data-stu-id="79a48-128">Web Share Target</span></span>][GitHubWicgWebShareTarget]
*   [<span data-ttu-id="79a48-129">Web Share</span><span class="sxs-lookup"><span data-stu-id="79a48-129">Web Share</span></span>][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestos do aplicativo Web | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Web Share Target API | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Dicionário ShareData - API do Web Share | WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Api do Web Share | WICG"
