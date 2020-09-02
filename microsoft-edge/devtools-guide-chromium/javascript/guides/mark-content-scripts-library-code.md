---
title: Marcar Scripts de Conteúdo como Código de Biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a5101cb8561a49ce6c271398f4c1a828984da9e3
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991159"
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
   limitations under the License.  -->

# <span data-ttu-id="5143b-103">Marcar scripts de conteúdo como código de biblioteca</span><span class="sxs-lookup"><span data-stu-id="5143b-103">Mark content scripts as Library code</span></span>  

<span data-ttu-id="5143b-104">Ao usar o painel **fontes** do Microsoft Edge devtools para percorrer o [código][DevToolsJavascriptStepThroughCode], às vezes, você pode pausar o código que não reconhece.</span><span class="sxs-lookup"><span data-stu-id="5143b-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="5143b-105">Você provavelmente pausou no código de uma das extensões do Microsoft Edge instaladas.</span><span class="sxs-lookup"><span data-stu-id="5143b-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="5143b-106">Conclua as etapas a seguir para não pausar no código de extensão.</span><span class="sxs-lookup"><span data-stu-id="5143b-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="5143b-107">Abra o DevTools, selecione **Personalizar e controle devtools** \ ( `...` \) e escolha **configurações**.</span><span class="sxs-lookup"><span data-stu-id="5143b-107">Open DevTools, select **Customize and control DevTools** \(`...`\) and choose **Settings**.</span></span>  <span data-ttu-id="5143b-108">Você também pode abrir **as configurações** selecionando `F1` .</span><span class="sxs-lookup"><span data-stu-id="5143b-108">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="5143b-109">Selecione a guia **código de biblioteca** que abre a seção de código da biblioteca de **estrutura** de **configurações**.</span><span class="sxs-lookup"><span data-stu-id="5143b-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="5143b-110">Habilite a caixa de seleção **Marcar scripts de conteúdo como código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="5143b-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Habilitar a caixa de seleção Marcar scripts de conteúdo como código de biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="5143b-112">Habilitar a caixa de seleção **Marcar scripts de conteúdo como código de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="5143b-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5143b-113">Entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5143b-113">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Etapa 4: percorrer o código-introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="5143b-115">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5143b-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5143b-116">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5143b-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5143b-118">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5143b-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
