---
description: Começar a usar WebViews de Depuração Remota em seus aplicativos Android nativos usando Microsoft Edge Ferramentas de Desenvolvedor.
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 75d948465c62c63c9ccbe0fcd46616819a04e79d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565075"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="get-started-with-remote-debugging-android-webviews"></a><span data-ttu-id="185ed-104">Introdução à depuração remota de dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="185ed-104">Get started with remote debugging Android WebViews</span></span>  

<span data-ttu-id="185ed-105">Depurar o Android WebViews em seus aplicativos Android nativos usando Microsoft Edge Ferramentas de Desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="185ed-105">Debug Android WebViews in your native Android apps using Microsoft Edge Developer Tools.</span></span>  

<span data-ttu-id="185ed-106">No Android 4.4 \(KitKat\) ou posterior, use DevTools para depurar o conteúdo webView em aplicativos Android nativos.</span><span class="sxs-lookup"><span data-stu-id="185ed-106">On Android 4.4 \(KitKat\) or later, use DevTools to debug WebView content in native Android apps.</span></span>  

### <a name="summary"></a><span data-ttu-id="185ed-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="185ed-107">Summary</span></span>  

*   <span data-ttu-id="185ed-108">Ativar a depuração do Android WebView em seu aplicativo Android nativo; depurar o Android WebViews Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="185ed-108">Turn on Android WebView debugging in your native Android app; debug Android WebViews in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="185ed-109">Para exibir a lista dos WebViews do Android com a depuração ativas, navegue até `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="185ed-109">To display the list of the Android WebViews with debugging turned on, navigate to `edge://inspect`.</span></span>  
*   <span data-ttu-id="185ed-110">Depurar o Android WebViews da mesma maneira que você depura uma página da Web por meio [da depuração remota.][RemoteDebuggingGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="185ed-110">Debug Android WebViews in the same way you debug a webpage through [remote debugging][RemoteDebuggingGettingStarted].</span></span>  

## <a name="configure-android-webviews-to-debug"></a><span data-ttu-id="185ed-111">Configurar WebViews do Android para depurar</span><span class="sxs-lookup"><span data-stu-id="185ed-111">Configure Android WebViews to debug</span></span>  

<span data-ttu-id="185ed-112">A depuração do Android WebView deve estar 100% ativas no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185ed-112">Android WebView debugging must be turned on within your app.</span></span>  <span data-ttu-id="185ed-113">Para ativar a depuração do Android WebView, execute o [método estático setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] na `WebView` classe.</span><span class="sxs-lookup"><span data-stu-id="185ed-113">To turn on Android WebView debugging, run the [setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] static method on the `WebView` class.</span></span>  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

<span data-ttu-id="185ed-114">A configuração se aplica a todos os WebViews do Android do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185ed-114">The setting applies to all of the Android WebViews of the app.</span></span>  

> [!TIP]
> <span data-ttu-id="185ed-115">A depuração do Android WebView não é afetada pelo estado `debuggable` do sinalizador no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185ed-115">Android WebView debugging is not affected by the state of the `debuggable` flag in the manifest of the app.</span></span>  <span data-ttu-id="185ed-116">Se você quiser ativar a depuração do Android WebView somente quando o sinalizador estiver , teste o `debuggable` sinalizador no tempo de `true` execução.</span><span class="sxs-lookup"><span data-stu-id="185ed-116">If you want to turn on Android WebView debugging only when the `debuggable` flag is `true`, test the flag at runtime.</span></span>  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a><span data-ttu-id="185ed-117">Abrir um WebView do Android no DevTools</span><span class="sxs-lookup"><span data-stu-id="185ed-117">Open an Android WebView in DevTools</span></span>  

<span data-ttu-id="185ed-118">Para exibir uma lista dos WebViews do Android com a depuração ativas que são executados em seu dispositivo, navegue até `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="185ed-118">To display a list of the Android WebViews with debugging turned on that run on your device, navigate to `edge://inspect`.</span></span>  

<span data-ttu-id="185ed-119">Para iniciar a depuração, no WebView do Android que você deseja depurar, escolha **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="185ed-119">To start debugging, under the Android WebView you want to debug, choose **inspect**.</span></span>  <span data-ttu-id="185ed-120">Use DevTools da mesma maneira que você faz uma guia de navegador remoto.</span><span class="sxs-lookup"><span data-stu-id="185ed-120">Use DevTools in the same way that you do a remote browser tab.</span></span>  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a><span data-ttu-id="185ed-121">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="185ed-121">Troubleshoot</span></span>  

<span data-ttu-id="185ed-122">Seus WebViews do Android não são exibidos na `edge://inspect` página?</span><span class="sxs-lookup"><span data-stu-id="185ed-122">Your Android WebViews aren't displayed on the `edge://inspect` page?</span></span>  

*   <span data-ttu-id="185ed-123">Verifique se a depuração do Android WebView está ativas para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="185ed-123">Verify that Android WebView debugging is turned on for your app.</span></span>  
*   <span data-ttu-id="185ed-124">Em seu dispositivo, abra o aplicativo com o Android WebView que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="185ed-124">On your device, open the app with the Android WebView you want to debug.</span></span>  <span data-ttu-id="185ed-125">Em seguida, atualize `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="185ed-125">Then, refresh `edge://inspect`.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="185ed-126">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="185ed-126">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introdução com dispositivos Android de depuração remota | Microsoft Docs"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled - WebView | Desenvolvedores Android"  

> [!NOTE]
> <span data-ttu-id="185ed-129">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="185ed-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="185ed-130">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="185ed-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="185ed-132">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="185ed-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
