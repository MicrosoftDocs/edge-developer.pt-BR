---
description: Recursos adicionados ao Microsoft Edge (Chromium) DevTools em março de 2019
title: O que há de novo no Microsoft Edge (Chromium) DevTools em março de 2019
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/23/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0b592eddbd68b3bbd8ff0a9edf9a1253bd79677e
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182509"
---
# <span data-ttu-id="62094-104">O que há de novo no Microsoft Edge (Chromium) DevTools</span><span class="sxs-lookup"><span data-stu-id="62094-104">What's new in the Microsoft Edge (Chromium) DevTools</span></span>

<span data-ttu-id="62094-105">Muito obrigado por experimentar uma visualização do novo Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="62094-105">Thank you so much for trying out a preview of the new Microsoft Edge!</span></span> <span data-ttu-id="62094-106">Com esta versão, desenvolvemos uma grande mudança na plataforma da Web subjacente do Microsoft Edge, adotando o projeto de fonte aberta Chromium.</span><span class="sxs-lookup"><span data-stu-id="62094-106">With this release, we've undertaken a major shift in the underlying web platform of Microsoft Edge by adopting the Chromium open source project.</span></span> <span data-ttu-id="62094-107">Com essa alteração, será mais fácil para você criar e testar seus sites no Microsoft Edge e garantir que eles ainda funcionarão como esperado, mesmo se seus usuários estiverem procurando em um navegador diferente baseado no Chromium, como Google Chrome, Vivaldi, Opera ou Brave.</span><span class="sxs-lookup"><span data-stu-id="62094-107">With this change, it will be easier for you to build and test your web sites in Microsoft Edge and ensure they will still work as expected even if your users are browsing in a different Chromium-based browser, like Google Chrome, Vivaldi, Opera, or Brave.</span></span>

## <span data-ttu-id="62094-108">O novo Microsoft Edge (Chromium) DevTools</span><span class="sxs-lookup"><span data-stu-id="62094-108">The new Microsoft Edge (Chromium) DevTools</span></span>

<span data-ttu-id="62094-109">Se você estiver fazendo check-out do Microsoft Edge e se desenvolve principalmente em um navegador baseado no Chromium, você deve se sentir em casa.</span><span class="sxs-lookup"><span data-stu-id="62094-109">If you are checking out Microsoft Edge and you mainly develop in a Chromium-based browser, you should feel right at home.</span></span> <span data-ttu-id="62094-110">As ferramentas de desenvolvedor do Microsoft Edge (Chromium) são exatamente como as ferramentas de desenvolvedor que você já conhece e usa!</span><span class="sxs-lookup"><span data-stu-id="62094-110">The Microsoft Edge (Chromium) Developer Tools are exactly like the developer tools you already know and use!</span></span>

![Microsoft Edge (Chromium) DevTools](./media/devtools.png)

<span data-ttu-id="62094-112">Se você estiver fazendo o check-out do novo Microsoft Edge e tiver desenvolvido principalmente no Microsoft Edge (EdgeHTML), temos algumas ferramentas incríveis incríveis que esperamos facilitar e agilizar a criação e teste de seus sites da Web no Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="62094-112">If you are checking out the new Microsoft Edge and you mainly developed in Microsoft Edge (EdgeHTML), we have got some great new tools that we hope will make it easier and faster for you to build and test your web sites in Microsoft Edge!</span></span> <span data-ttu-id="62094-113">Para saber mais sobre essas novas ferramentas, confira [o guia do devtools Microsoft Edge (Chromium)](../devtools-guide-chromium.md).</span><span class="sxs-lookup"><span data-stu-id="62094-113">To learn more about these new tools, check out [The Microsoft Edge (Chromium) DevTools Guide](../devtools-guide-chromium.md).</span></span>

## <span data-ttu-id="62094-114">Novos temas escuros e leves para o DevTools</span><span class="sxs-lookup"><span data-stu-id="62094-114">New dark and light themes for the DevTools</span></span>

<span data-ttu-id="62094-115">Projetamos alguns novos temas escuros e leves para a DevTools que achamos que você vai adorar!</span><span class="sxs-lookup"><span data-stu-id="62094-115">We've designed some new dark and light themes for the DevTools that we think you'll love!</span></span> <span data-ttu-id="62094-116">Por padrão, o DevTools Microsoft Edge (Chromium) vai usar o tema escuro.</span><span class="sxs-lookup"><span data-stu-id="62094-116">By default, the Microsoft Edge (Chromium) DevTools will use the Dark theme.</span></span> <span data-ttu-id="62094-117">Para alterar o tema do devtools, pressione `Fn`  +  `F1` no Windows ou Mac ou navegue até configurações usando o `...` botão no canto superior direito do devtools.</span><span class="sxs-lookup"><span data-stu-id="62094-117">To change the theme of the DevTools, press `Fn` + `F1` on Windows or Mac or navigate to Settings using the `...` button in the top right corner of the DevTools.</span></span>

![Menu principal do Microsoft Edge (Chromium) DevTools](./media/devtools-main-menu.png)

<span data-ttu-id="62094-119">Em configurações, você pode alterar o tema da DevTools.</span><span class="sxs-lookup"><span data-stu-id="62094-119">From Settings, you can change the theme of the DevTools.</span></span> <span data-ttu-id="62094-120">Se você gostou da maneira como o DevTools procurou em seu navegador baseado no Chromium, você pode fazer com que o Microsoft Edge (Chromium) DevTools tenha exatamente o seguinte selecionando os temas **escuro (Chromium)** ou **leve (Chromium)** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="62094-120">If you liked the way the DevTools looked in your Chromium-based browser, you can make the Microsoft Edge (Chromium) DevTools look exactly like them by selecting the **Dark (Chromium)** or **Light (Chromium)** themes respectively.</span></span> 

## <span data-ttu-id="62094-121">Depurar o Microsoft Edge (Chromium) a partir de código VS</span><span class="sxs-lookup"><span data-stu-id="62094-121">Debug Microsoft Edge (Chromium) from VS Code</span></span>

<span data-ttu-id="62094-122">Com o [depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, agora você pode depurar o Microsoft Edge (EdgeHTML) e o Microsoft Edge (Chromium) diretamente do código vs!</span><span class="sxs-lookup"><span data-stu-id="62094-122">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can now debug both Microsoft Edge (EdgeHTML) and Microsoft Edge (Chromium) directly from VS Code!</span></span>

![Depurador para borda VS extensão de código](./media/vscode-debugger.png)

<span data-ttu-id="62094-124">Para iniciar o Microsoft Edge (Chromium) em vez do Microsoft Edge (EdgeHTML) a partir do código VS, você precisa adicionar um `version` atributo ao seu **launch.jsexistente na** configuração com a versão do Microsoft Edge (Chromium) que deseja iniciar ( `dev` , `beta` ou ou `canary` ).</span><span class="sxs-lookup"><span data-stu-id="62094-124">To launch Microsoft Edge (Chromium) instead of Microsoft Edge (EdgeHTML) from VS Code, you need to add a `version` attribute to your existing **launch.json** configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="62094-125">Aqui está um exemplo **launch.jsna** configuração que iniciará a versão Canárias do Microsoft Edge (Chromium) para o [Bing.com](https://www.bing.com/):</span><span class="sxs-lookup"><span data-stu-id="62094-125">Here's a sample **launch.json** configuration that will launch the Canary version of Microsoft Edge (Chromium) to [bing.com](https://www.bing.com/):</span></span>

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

<span data-ttu-id="62094-126">Para obter mais informações, confira [como depurar o Microsoft Edge (Chromium) a partir de código vs](../visual-studio-code/debugger-for-edge.md).</span><span class="sxs-lookup"><span data-stu-id="62094-126">For more information, check out [how to debug Microsoft Edge (Chromium) from VS Code](../visual-studio-code/debugger-for-edge.md).</span></span>

## <span data-ttu-id="62094-127">Atualização do protocolo DevTools Edge</span><span class="sxs-lookup"><span data-stu-id="62094-127">Edge DevTools Protocol update</span></span>

<span data-ttu-id="62094-128">Com o turno na plataforma da Web subjacente do Microsoft Edge, o protocolo Edge DevTools não receberá mais nenhuma atualização.</span><span class="sxs-lookup"><span data-stu-id="62094-128">With the shift in the underlying web platform of Microsoft Edge, the Edge DevTools Protocol will not be receiving any further updates.</span></span> <span data-ttu-id="62094-129">O DevTools Microsoft Edge (Chromium) usará o protocolo de DevTools do Chrome ou a CDP.</span><span class="sxs-lookup"><span data-stu-id="62094-129">The Microsoft Edge (Chromium) DevTools will use the Chrome DevTools Protocol or CDP.</span></span> <span data-ttu-id="62094-130">Para fazer referência à documentação dos domínios e métodos no CDP, consulte [o Visualizador de CDP](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).</span><span class="sxs-lookup"><span data-stu-id="62094-130">To reference documentation on the domains and methods in CDP, please refer to [the CDP viewer](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).</span></span>

<span data-ttu-id="62094-131">No novo Microsoft Edge, qualquer método com o prefixo `ms` não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="62094-131">In the new Microsoft Edge, any methods that are prefixed with `ms` will not be supported.</span></span> <span data-ttu-id="62094-132">Para saber mais sobre como usar o CDP no Microsoft Edge (Chromium), consulte [devtools Protocol (Chromium)](../devtools-protocol-chromium.md).</span><span class="sxs-lookup"><span data-stu-id="62094-132">To learn more about how to use CDP in Microsoft Edge (Chromium), please refer to [DevTools Protocol (Chromium)](../devtools-protocol-chromium.md).</span></span>

## <span data-ttu-id="62094-133">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="62094-133">Known issues</span></span>

<span data-ttu-id="62094-134">Muitos links do DevTools Microsoft Edge (Chromium) para conteúdo hospedado em sites de terceiros foram removidos temporariamente.</span><span class="sxs-lookup"><span data-stu-id="62094-134">Many links from the Microsoft Edge (Chromium) DevTools to content hosted on third-party sites have been removed temporarily.</span></span> <span data-ttu-id="62094-135">Assim que pudermos substituir esses links, vamos adicioná-los de volta ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="62094-135">As soon as we can replace these links, we will add them back to the DevTools.</span></span>


<span data-ttu-id="62094-136">Ao depurar o conteúdo da Web em um dispositivo Android do Microsoft Edge (Chromium), a versão do DevTools que é iniciada quando você clica no botão **inspecionar** da ferramenta **dispositivos remotos** pode não corresponder à versão do navegador em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="62094-136">When debugging web content on an Android device from Microsoft Edge (Chromium), the version of the DevTools that launches when you click the **Inspect** button from the **Remote devices** tool may not match the version of the browser on your Android device.</span></span> <span data-ttu-id="62094-137">Como resultado, você poderá ver os novos recursos do DevTools que não funcionarão com o navegador em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="62094-137">As a result, you may see new features in the DevTools that will not work against the browser on your Android device.</span></span> <span data-ttu-id="62094-138">Se isso for algo que você encontrar, adoraríamos saber isso para fazer comentários sobre o [arquivo](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="62094-138">If this is something you encounter, we'd love to hear about it so please [file feedback](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>

<span data-ttu-id="62094-139">Por fim, o Visual Studio no Windows e no Mac ainda não é compatível com o Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="62094-139">Finally, Visual Studio on Windows and Mac does not yet support Microsoft Edge (Chromium).</span></span> <span data-ttu-id="62094-140">Inscreva-se [aqui](https://visualstudio.microsoft.com/vs/preview/) para ser o primeiro a saber quando temos uma versão de visualização do Visual Studio que ofereça suporte à depuração do JavaScript dentro do Microsoft Edge (Chromium) para projetos do ASP.net.</span><span class="sxs-lookup"><span data-stu-id="62094-140">Sign up [here](https://visualstudio.microsoft.com/vs/preview/) to be the first to know when we have a preview version of Visual Studio that supports JavaScript debugging inside Microsoft Edge (Chromium) for ASP.NET projects!</span></span>  
