---
title: Abrir o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601884"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# <span data-ttu-id="1b832-103">Abrir o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1b832-103">Open Microsoft Edge DevTools</span></span>   



<span data-ttu-id="1b832-104">Há muitas maneiras de abrir o Microsoft Edge DevTools, pois diferentes usuários querem acesso rápido a diferentes partes da interface do usuário do DevTools.</span><span class="sxs-lookup"><span data-stu-id="1b832-104">There are many ways to open Microsoft Edge DevTools, because different users want fast access to different parts of the DevTools UI.</span></span>  

## <span data-ttu-id="1b832-105">Abrir o painel de elementos para inspecionar o DOM ou CSS</span><span class="sxs-lookup"><span data-stu-id="1b832-105">Open the Elements panel to inspect the DOM or CSS</span></span>   

<span data-ttu-id="1b832-106">Quando você quiser inspecionar os estilos ou atributos de um nó DOM, clique com o botão direito do mouse no elemento e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1b832-106">When you want to inspect the styles or attributes of a DOM node, right-click the element and select **Inspect**.</span></span>  

> ##### <span data-ttu-id="1b832-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="1b832-107">Figure 1</span></span>  
> <span data-ttu-id="1b832-108">A opção **inspecionar**</span><span class="sxs-lookup"><span data-stu-id="1b832-108">The **Inspect** option</span></span>  
> ![A opção inspecionar][ImageInspectOption]  

<span data-ttu-id="1b832-110">Ou pressione `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Option` + `C` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="1b832-110">Or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Option`+`C` \(macOS\).</span></span>  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <span data-ttu-id="1b832-111">Abrir o painel de console para ver as mensagens registradas ou executar JavaScript</span><span class="sxs-lookup"><span data-stu-id="1b832-111">Open the Console panel to view logged messages or run JavaScript</span></span>   

<span data-ttu-id="1b832-112">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para saltar diretamente para o painel do **console** .</span><span class="sxs-lookup"><span data-stu-id="1b832-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to jump straight into the **Console** panel.</span></span>  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## <span data-ttu-id="1b832-113">Abrir o último painel que você abriu</span><span class="sxs-lookup"><span data-stu-id="1b832-113">Open the last panel you had open</span></span>   

<span data-ttu-id="1b832-114">Pressione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="1b832-114">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  

## <span data-ttu-id="1b832-115">Abrir o DevTools a partir do menu principal do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b832-115">Open DevTools from the Microsoft Edge main menu</span></span>  

<span data-ttu-id="1b832-116">Clique em **configurações e mais \ (Alt + F \)** `...` e selecione **mais**ferramentas de  >  **desenvolvedor**ferramentas.</span><span class="sxs-lookup"><span data-stu-id="1b832-116">Click **Settings and more \(Alt+F\)** `...` and then select **More Tools** > **Developer Tools**.</span></span>  

> ##### <span data-ttu-id="1b832-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="1b832-117">Figure 2</span></span>  
> <span data-ttu-id="1b832-118">Abrindo o DevTools a partir do menu principal do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b832-118">Opening DevTools from the Microsoft Edge main menu</span></span>  
> ![Abrindo o DevTools a partir do menu principal do Microsoft Edge][ImageOpenFromMain]  

## <span data-ttu-id="1b832-120">Abrir automaticamente o DevTools em cada nova guia</span><span class="sxs-lookup"><span data-stu-id="1b832-120">Auto-open DevTools on every new tab</span></span>   

<span data-ttu-id="1b832-121">Abra o Microsoft Edge na linha de comando e passe o `--auto-open-devtools-for-tabs` sinalizador.</span><span class="sxs-lookup"><span data-stu-id="1b832-121">Open Microsoft Edge from the command line and pass the `--auto-open-devtools-for-tabs` flag.</span></span>  

<span data-ttu-id="1b832-122">Windows \ (CMD \):</span><span class="sxs-lookup"><span data-stu-id="1b832-122">Windows \(CMD\):</span></span>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

<span data-ttu-id="1b832-123">Windows \ (PowerShell \):</span><span class="sxs-lookup"><span data-stu-id="1b832-123">Windows \(PowerShell\):</span></span>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

<span data-ttu-id="1b832-124">MacOS</span><span class="sxs-lookup"><span data-stu-id="1b832-124">macOS:</span></span>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Figura 1: a opção inspecionar"  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Figura 2: abrindo o DevTools a partir do menu principal do Microsoft Edge"  

<!-- links -->  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> <span data-ttu-id="1b832-127">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1b832-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1b832-128">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/open) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1b832-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/open) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1b832-130">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1b832-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
