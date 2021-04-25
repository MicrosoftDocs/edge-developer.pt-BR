---
description: Habilita "Marcar scripts de conteúdo como código biblioteca" a partir de Configurações > Código da Biblioteca da Estrutura.
title: Marcar scripts de conteúdo como código biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c1571ab909aac09e4593413e96f7d4b7723c7759
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519342"
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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="6bc1f-104">Marcar scripts de conteúdo como código biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bc1f-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="6bc1f-105">Quando você usa a **ferramenta Sources** para passar [pelo código][DevToolsJavascriptStepThroughCode], às vezes você pausa no código que não reconhece.</span><span class="sxs-lookup"><span data-stu-id="6bc1f-105">When you use the **Sources** tool to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you don't recognize.</span></span>  <span data-ttu-id="6bc1f-106">Você provavelmente fez uma pausa no código para uma das Extensões do Microsoft Edge instaladas.</span><span class="sxs-lookup"><span data-stu-id="6bc1f-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="6bc1f-107">Para não pausar no código de extensão, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="6bc1f-107">To not pause on extension code, complete the following actions.</span></span>  

1.  <span data-ttu-id="6bc1f-108">No DevTools, no canto superior direito, escolha o ícone de engrenagem (**Configurações**).</span><span class="sxs-lookup"><span data-stu-id="6bc1f-108">In DevTools, in the upper right, choose the gear icon (**Settings**).</span></span>  <span data-ttu-id="6bc1f-109">A página **Configurações** é exibida.</span><span class="sxs-lookup"><span data-stu-id="6bc1f-109">The **Settings** page appears.</span></span>  
1.  <span data-ttu-id="6bc1f-110">Abaixo **Configurações,** escolha **Ignorar Lista**.</span><span class="sxs-lookup"><span data-stu-id="6bc1f-110">Below **Settings**, choose **Ignore List**.</span></span>  <span data-ttu-id="6bc1f-111">A **seção Código da Biblioteca** da Estrutura de **Configurações** é exibida.</span><span class="sxs-lookup"><span data-stu-id="6bc1f-111">The **Framework Library Code** section of **Settings** appears.</span></span>  
1.  <span data-ttu-id="6bc1f-112">A turn on the **Mark content scripts as Library code checkbox.**</span><span class="sxs-lookup"><span data-stu-id="6bc1f-112">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Habilitar a caixa de seleção Marcar scripts de conteúdo como código da biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="6bc1f-114">Habilitar a caixa de seleção **Marcar scripts de** conteúdo como código da biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bc1f-114">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6bc1f-115">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6bc1f-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Etapa 4: passo a passo pelo código - Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="6bc1f-117">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6bc1f-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6bc1f-118">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6bc1f-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6bc1f-120">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6bc1f-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
