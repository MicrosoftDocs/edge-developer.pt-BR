---
title: Introdução aos emuladores Remote Debugging Surface Duo
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, depuração remota, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621499"
---
# <span data-ttu-id="0b553-103">Introdução aos emuladores Remote Debugging Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0b553-103">Get Started with Remote Debugging Surface Duo emulators</span></span>

<span data-ttu-id="0b553-104">Neste artigo, você percorre o processo de depuração remota do conteúdo da Web no [aplicativo Microsoft Edge][AndroidEdge] em um emulador [Surface Duo][SurfaceDuo] de uma instância da área de trabalho do [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="0b553-104">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][AndroidEdge] on a [Surface Duo][SurfaceDuo] emulator from a desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="0b553-105">Para obter informações sobre a depuração em um dispositivo Surface Duo, siga nosso guia para [dispositivos Android de depuração remota][RemoteDebuggingAndroid].</span><span class="sxs-lookup"><span data-stu-id="0b553-105">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][RemoteDebuggingAndroid].</span></span>

## <span data-ttu-id="0b553-106">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="0b553-106">Before you Begin</span></span>

<span data-ttu-id="0b553-107">Instale o [SDK do Surface Duo][DuoSdk] antes de executar o [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="0b553-107">Install the [Surface Duo SDK][DuoSdk] before running the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="0b553-108">Para obter mais informações, consulte [obter o SDK Surface Duo][DuoSdkdocs].</span><span class="sxs-lookup"><span data-stu-id="0b553-108">For more information, see [Get the Surface Duo SDK][DuoSdkdocs].</span></span>

## <span data-ttu-id="0b553-109">Etapa 1: Navegue até edge://inspect</span><span class="sxs-lookup"><span data-stu-id="0b553-109">Step 1: Navigate to edge://inspect</span></span>

<span data-ttu-id="0b553-110">Abra uma instância da área de trabalho do [Microsoft Edge][DesktopEdge]e navegue até `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="0b553-110">Open a desktop instance of [Microsoft Edge][DesktopEdge], and navigate to `edge://inspect`.</span></span>

> ##### <span data-ttu-id="0b553-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="0b553-111">Figure 1</span></span>  
> <span data-ttu-id="0b553-112">A `edge://inspect` página no Microsoft Edge na área ![ de trabalho a página Edge://inspect no Microsoft Edge na área de trabalho][ImageEdgeInspect]</span><span class="sxs-lookup"><span data-stu-id="0b553-112">The `edge://inspect` page in Microsoft Edge on the desktop ![The edge://inspect page in Microsoft Edge on the desktop][ImageEdgeInspect]</span></span>

> [!NOTE]
> <span data-ttu-id="0b553-113">Se a `edge://inspect` página não reconhecer o [emulador Surface Duo][DuoEmulator], reinicie o emulador.</span><span class="sxs-lookup"><span data-stu-id="0b553-113">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DuoEmulator], restart the emulator.</span></span>

## <span data-ttu-id="0b553-114">Etapa 2: iniciar o emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0b553-114">Step 2: Launch the Surface Duo emulator</span></span>

<span data-ttu-id="0b553-115">Inicie o [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="0b553-115">Launch the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="0b553-116">Observe que o emulador exibe duas telas diferentes em execução no emulador.</span><span class="sxs-lookup"><span data-stu-id="0b553-116">Notice that the emulator displays 2 different screens running on the emulator.</span></span>

> ##### <span data-ttu-id="0b553-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="0b553-117">Figure 2</span></span>
> <span data-ttu-id="0b553-118">Emulador Surface Duo ![ o emulador Surface Duo][ImageDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="0b553-118">The Surface Duo emulator ![The Surface Duo emulator][ImageDuoEmulator]</span></span>  

## <span data-ttu-id="0b553-119">Etapa 3: carregar o conteúdo da Web no Microsoft Edge no emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0b553-119">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>

<span data-ttu-id="0b553-120">Em qualquer uma das telas, passe o dedo sobre a bandeja de favoritos do [emulador Surface Duo][DuoEmulator] para exibir a gaveta de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0b553-120">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DuoEmulator] to display the Apps Drawer.</span></span> <span data-ttu-id="0b553-121">Escolha **borda** para iniciar o [aplicativo Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="0b553-121">Choose **Edge** to launch the [Microsoft Edge app][AndroidEdge].</span></span>

> ##### <span data-ttu-id="0b553-122">Figura 3</span><span class="sxs-lookup"><span data-stu-id="0b553-122">Figure 3</span></span>
> <span data-ttu-id="0b553-123">O aplicativo Microsoft Edge no emulador Surface Duo ![ do aplicativo Microsoft Edge no emulador Surface Duo][ImageDuoEmulatorEdge]</span><span class="sxs-lookup"><span data-stu-id="0b553-123">The Microsoft Edge app on the Surface Duo emulator ![The Microsoft Edge app on the Surface Duo emulator][ImageDuoEmulatorEdge]</span></span>  

<span data-ttu-id="0b553-124">Navegue até o site ou o aplicativo que você deseja depurar no [aplicativo Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="0b553-124">Navigate to the website or app that you want to debug in the [Microsoft Edge app][AndroidEdge].</span></span>

## <span data-ttu-id="0b553-125">Etapa 4: depurar o conteúdo da Web pelo emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="0b553-125">Step 4: Debug your web content from the Surface Duo emulator</span></span> 

<span data-ttu-id="0b553-126">Volte para a instância da área de trabalho do [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="0b553-126">Switch back to the desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="0b553-127">A `edge://inspect` página agora mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][PwaDocs] que estão em execução no [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="0b553-127">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaDocs] that are running on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="0b553-128">Figura 4</span><span class="sxs-lookup"><span data-stu-id="0b553-128">Figure 4</span></span>
> <span data-ttu-id="0b553-129">A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador ![ a página Edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador][ImageEdgeInspectTargets]</span><span class="sxs-lookup"><span data-stu-id="0b553-129">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator ![The edge://inspect page displays a list of the open tabs in the Microsoft Edge app running on the emulator][ImageEdgeInspectTargets]</span></span>  

> [!NOTE]
> <span data-ttu-id="0b553-130">Se você não vir **SurfaceDuoEmulator** na `edge://inspect` página, tente abrir ou fechar as guias no [aplicativo Microsoft Edge][AndroidEdge] no [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="0b553-130">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][AndroidEdge] on the [Surface Duo Emulator][DuoEmulator].</span></span> <span data-ttu-id="0b553-131">Para obter etapas adicionais de solução de problemas, consulte a [seção solução de problemas para dispositivos Android][TroubleshootingAndroid].</span><span class="sxs-lookup"><span data-stu-id="0b553-131">For additional troubleshooting steps, see the [troubleshooting section for Android devices][TroubleshootingAndroid].</span></span>

<span data-ttu-id="0b553-132">Na lista de guias abertas em execução no emulador, escolha **inspecionar** na guia em que o conteúdo da Web deve ser depurado.</span><span class="sxs-lookup"><span data-stu-id="0b553-132">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span> <span data-ttu-id="0b553-133">O [Microsoft Edge devtools][DevToolsDocs] será aberto em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="0b553-133">The [Microsoft Edge DevTools][DevToolsDocs] will open in a new window.</span></span> <span data-ttu-id="0b553-134">Escolha **alternar screencast** ![ alternar screencast ][ImageToggleScreencastIcon] para ver o conteúdo da Web do seu [emulador Surface Duo][DuoEmulator] na janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="0b553-134">Choose **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the web content from your [Surface Duo emulator][DuoEmulator] in the DevTools window.</span></span> <span data-ttu-id="0b553-135">Agora você pode usar o Microsoft Edge DevTools para depurar o conteúdo da Web no [emulador Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="0b553-135">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="0b553-136">Figura 5</span><span class="sxs-lookup"><span data-stu-id="0b553-136">Figure 5</span></span>
> <span data-ttu-id="0b553-137">Usando o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo ![ usando o Microsoft Edge devtools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo][ImageDevTools]</span><span class="sxs-lookup"><span data-stu-id="0b553-137">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator ![Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator][ImageDevTools]</span></span>  

> [!NOTE]
> <span data-ttu-id="0b553-138">Se você ocupar o [aplicativo Microsoft Edge][AndroidEdge] entre as duas telas no emulador, o screencast refletirá o novo tamanho do aplicativo, mas não a dobradiça.</span><span class="sxs-lookup"><span data-stu-id="0b553-138">If you span the [Microsoft Edge app][AndroidEdge] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span> <span data-ttu-id="0b553-139">Para entender como a dobradiça impacta o layout do seu conteúdo da Web, use o [emulador Surface Duo][DuoEmulator] em vez do screencast.</span><span class="sxs-lookup"><span data-stu-id="0b553-139">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DuoEmulator] instead of the screencast.</span></span>

## <span data-ttu-id="0b553-140">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="0b553-140">Additional Resources</span></span>

<span data-ttu-id="0b553-141">A Web é uma ótima plataforma para a nova classe de dobrável e dispositivos de tela dupla porque você pode escrever seu HTML, CSS e JavaScript uma vez e ter uma ótima aparência em dispositivos com tela única, tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="0b553-141">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span> <span data-ttu-id="0b553-142">Para obter mais informações, consulte estes recursos adicionais para começar a criar conteúdo da Web para esses novos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0b553-142">For more information, see these additional resources to get started building web content for these new devices.</span></span>

- [<span data-ttu-id="0b553-143">Documentação para criar aplicativos em dispositivos de tela dupla</span><span class="sxs-lookup"><span data-stu-id="0b553-143">Documentation for creating apps on dual-screen devices</span></span>][DualScreenDocs]
- [<span data-ttu-id="0b553-144">O explicativo da plataforma Web Microsoft Edge para novas APIs para criar experiências na Web no dobrável e em dispositivos de tela dupla</span><span class="sxs-lookup"><span data-stu-id="0b553-144">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][WebPlatformExplainer]
- [<span data-ttu-id="0b553-145">Gravação da sessão de dia do desenvolvedor do Microsoft 365: como criar experiências de tela dupla para sites e aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="0b553-145">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Figura 1: a página edge://inspect no Microsoft Edge na área de trabalho"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Figura 2: emulador Surface Duo"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Figura 3: o aplicativo Microsoft Edge no emulador Surface Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Figura 4: a página edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador"
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Figura 5: usar o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introdução à depuração remota de dispositivos Android"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Solução de problemas: o DevTools não está detectando o dispositivo Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicativo Android do Microsoft Edge"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Apresentando o Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Apresentando o novo Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Usar o emulador Surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Lançamento do SDK Surface Duo Preview"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Obter o SDK do Surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Criar aplicativos para dispositivos com tela dupla"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma Web para experiências otimizadas em dispositivos dobrável"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Como criar experiências de tela dupla para o site e os aplicativos Web"
