---
description: Habilita "Marcar scripts de conteúdo como código biblioteca" a partir de Configurações > Código da Biblioteca da Estrutura.
title: Marcar scripts de conteúdo como código biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ffc27cdd04ce28df888507fb2e1dc460d5bb4f21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398949"
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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="8d54e-104">Marcar scripts de conteúdo como código biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d54e-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="8d54e-105">Ao usar o **painel Fontes** do Microsoft Edge DevTools para passar o [código,][DevToolsJavascriptStepThroughCode]às vezes você pausa no código que não reconhece.</span><span class="sxs-lookup"><span data-stu-id="8d54e-105">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="8d54e-106">Você provavelmente fez uma pausa no código para uma das Extensões do Microsoft Edge instaladas.</span><span class="sxs-lookup"><span data-stu-id="8d54e-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="8d54e-107">Conclua as etapas a seguir para não pausar no código de extensão.</span><span class="sxs-lookup"><span data-stu-id="8d54e-107">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="8d54e-108">Abra DevTools, escolha **Personalizar e controlar o DevTools** \( `...` \) > **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="8d54e-108">Open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="8d54e-109">Você também pode abrir **Configurações** selecionando `F1` .</span><span class="sxs-lookup"><span data-stu-id="8d54e-109">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="8d54e-110">Escolha o **painel de código** biblioteca que abre a seção Código da **Biblioteca** da Estrutura **de Configurações**.</span><span class="sxs-lookup"><span data-stu-id="8d54e-110">Choose the **Library code** panel which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="8d54e-111">A turn on the **Mark content scripts as Library code checkbox.**</span><span class="sxs-lookup"><span data-stu-id="8d54e-111">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Habilitar a caixa de seleção Marcar scripts de conteúdo como código da biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="8d54e-113">Habilitar a caixa de seleção **Marcar scripts de** conteúdo como código da biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d54e-113">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8d54e-114">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8d54e-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Etapa 4: passo a passo pelo código - Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="8d54e-116">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d54e-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8d54e-117">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8d54e-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8d54e-119">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d54e-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
