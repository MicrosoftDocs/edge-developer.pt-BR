---
title: Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607423"
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





# <span data-ttu-id="c2ce0-103">Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c2ce0-103">Simulate Mobile Devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="c2ce0-104">Use o modo de dispositivo para aproximar a aparência e a execução de sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="c2ce0-105">O modo de dispositivo é o nome para a coleção flexível de recursos no Microsoft Edge DevTools que ajudam você a simular dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="c2ce0-106">Esses recursos incluem:</span><span class="sxs-lookup"><span data-stu-id="c2ce0-106">These features include:</span></span>  

*   [<span data-ttu-id="c2ce0-107">Simulando um visor móvel</span><span class="sxs-lookup"><span data-stu-id="c2ce0-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="c2ce0-108">Otimizando a rede</span><span class="sxs-lookup"><span data-stu-id="c2ce0-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="c2ce0-109">Otimizando a CPU</span><span class="sxs-lookup"><span data-stu-id="c2ce0-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="c2ce0-110">Simulação de localização geográfica</span><span class="sxs-lookup"><span data-stu-id="c2ce0-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="c2ce0-111">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="c2ce0-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="c2ce0-112">Limitações</span><span class="sxs-lookup"><span data-stu-id="c2ce0-112">Limitations</span></span>   

<span data-ttu-id="c2ce0-113">Pense no modo de dispositivo como uma [aproximação de primeira ordem][WikiApproximation] de como a sua página se parece e se sente em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="c2ce0-114">Com o modo de dispositivo, você não executa o código em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="c2ce0-115">Você simula a experiência do usuário móvel do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="c2ce0-116">Há alguns aspectos dos dispositivos móveis que o DevTools nunca poderá simular.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="c2ce0-117">Por exemplo, a arquitetura de CPUs móveis é muito diferente da arquitetura de CPUs para laptop ou desktop.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="c2ce0-118">Quando estiver em dúvida, a melhor opção é realmente executar sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="c2ce0-119">Use [depuração remota] [DevToolsRemoteDebugging] para exibir, alterar, depurar e criar o perfil do código de uma página do laptop ou da área de trabalho, enquanto ela é executada em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="c2ce0-120">Simular um visor móvel</span><span class="sxs-lookup"><span data-stu-id="c2ce0-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="c2ce0-121">Clique na **barra de ferramentas Alternar** dispositivo ![ alternar barra ][ImageDeviceToolbarIcon] de ferramentas para abrir a interface do usuário que permite simular um visor móvel.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-121">Click **Toggle Device Toolbar** ![Toggle Device Toolbar][ImageDeviceToolbarIcon] to open the UI that enables you to simulate a mobile viewport.</span></span>  

> ##### <span data-ttu-id="c2ce0-122">Figura 1</span><span class="sxs-lookup"><span data-stu-id="c2ce0-122">Figure 1</span></span>  
> <span data-ttu-id="c2ce0-123">A barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-123">The Device Toolbar</span></span>  
> ![A barra de ferramentas do dispositivo][ImageDeviceToolbar]  

<span data-ttu-id="c2ce0-125">Por padrão, a barra de ferramentas do dispositivo é aberta no modo de visor responsivo.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-125">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="c2ce0-126">Modo de visor responsivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-126">Responsive Viewport Mode</span></span>   

<span data-ttu-id="c2ce0-127">Arraste as alças para redimensionar o visor para qualquer dimensão necessária.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-127">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="c2ce0-128">Ou insira valores específicos nas caixas largura e altura.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-128">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="c2ce0-129">Na [Figura 2](#figure-2), a largura é definida como `626` e a altura é definida como `516` .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-129">In [Figure 2](#figure-2), the width is set to `626` and the height is set to `516`.</span></span>  

> ##### <span data-ttu-id="c2ce0-130">Figura 2</span><span class="sxs-lookup"><span data-stu-id="c2ce0-130">Figure 2</span></span>  
> <span data-ttu-id="c2ce0-131">As alças para alterar as dimensões do visor quando no modo de visor responsivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-131">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
> ![As alças para alterar as dimensões do visor quando no modo de visor responsivo][ImageResponsiveHandles]  

#### <span data-ttu-id="c2ce0-133">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="c2ce0-133">Show media queries</span></span>   

<span data-ttu-id="c2ce0-134">Para mostrar pontos de interrupção de consulta de mídia acima do visor, clique em **mais opções** e selecione **Mostrar consultas de mídia**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-134">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

> ##### <span data-ttu-id="c2ce0-135">Figura 3</span><span class="sxs-lookup"><span data-stu-id="c2ce0-135">Figure 3</span></span>  
> <span data-ttu-id="c2ce0-136">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="c2ce0-136">Show media queries</span></span>  
> ![Mostrar consultas de mídia][ImageShowMediaQueries]  

<span data-ttu-id="c2ce0-138">Clique em um ponto de interrupção para alterar a largura do visor para que o ponto de interrupção seja disparado.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-138">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

> ##### <span data-ttu-id="c2ce0-139">Figura 4</span><span class="sxs-lookup"><span data-stu-id="c2ce0-139">Figure 4</span></span>  
> <span data-ttu-id="c2ce0-140">Clique em um ponto de interrupção para alterar a largura do visor</span><span class="sxs-lookup"><span data-stu-id="c2ce0-140">Click a breakpoint to change the width of the viewport</span></span>  
> ![Clique em um ponto de interrupção para alterar a largura do visor][ImageBreakpoint]  

#### <span data-ttu-id="c2ce0-142">Definir o tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-142">Set the device type</span></span>   

<span data-ttu-id="c2ce0-143">Use a lista **tipo de dispositivo** para simular um dispositivo móvel ou um dispositivo de desktop.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-143">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

> ##### <span data-ttu-id="c2ce0-144">Figura 5</span><span class="sxs-lookup"><span data-stu-id="c2ce0-144">Figure 5</span></span>  
> <span data-ttu-id="c2ce0-145">A lista **tipo de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="c2ce0-145">The **Device Type** list</span></span>  
> ![A lista tipo de dispositivo][ImageDeviceType]  

<span data-ttu-id="c2ce0-147">A tabela a seguir descreve as diferenças entre as opções.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-147">The table below describes the differences between the options.</span></span>  <span data-ttu-id="c2ce0-148">**Método de renderização** refere-se ao Microsoft Edge renderiza a página como um visor móvel ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-148">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="c2ce0-149">**Ícone do cursor** refere-se ao tipo de cursor que você vê quando passa o mouse sobre a página.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-149">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="c2ce0-150">Os **eventos acionados** referem-se à página `touch` ou `click` eventos quando você interage com a página.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-150">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="c2ce0-151">Opção</span><span class="sxs-lookup"><span data-stu-id="c2ce0-151">Option</span></span> | <span data-ttu-id="c2ce0-152">Método de renderização</span><span class="sxs-lookup"><span data-stu-id="c2ce0-152">Rendering method</span></span> | <span data-ttu-id="c2ce0-153">Ícone de cursor</span><span class="sxs-lookup"><span data-stu-id="c2ce0-153">Cursor icon</span></span> | <span data-ttu-id="c2ce0-154">Eventos acionados</span><span class="sxs-lookup"><span data-stu-id="c2ce0-154">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="c2ce0-155">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="c2ce0-155">Mobile</span></span> | <span data-ttu-id="c2ce0-156">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="c2ce0-156">Mobile</span></span> | <span data-ttu-id="c2ce0-157">Circle</span><span class="sxs-lookup"><span data-stu-id="c2ce0-157">Circle</span></span> | <span data-ttu-id="c2ce0-158">touch</span><span class="sxs-lookup"><span data-stu-id="c2ce0-158">touch</span></span> |  
| <span data-ttu-id="c2ce0-159">Celular \ (sem toque \)</span><span class="sxs-lookup"><span data-stu-id="c2ce0-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="c2ce0-160">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="c2ce0-160">Mobile</span></span> | <span data-ttu-id="c2ce0-161">Normal</span><span class="sxs-lookup"><span data-stu-id="c2ce0-161">Normal</span></span> | <span data-ttu-id="c2ce0-162"> clique em </span><span class="sxs-lookup"><span data-stu-id="c2ce0-162">click</span></span> |  
| <span data-ttu-id="c2ce0-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="c2ce0-163">Desktop</span></span> | <span data-ttu-id="c2ce0-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="c2ce0-164">Desktop</span></span> | <span data-ttu-id="c2ce0-165">Normal</span><span class="sxs-lookup"><span data-stu-id="c2ce0-165">Normal</span></span> | <span data-ttu-id="c2ce0-166"> clique em </span><span class="sxs-lookup"><span data-stu-id="c2ce0-166">click</span></span> |  
| <span data-ttu-id="c2ce0-167">Área de trabalho \ (Touch \)</span><span class="sxs-lookup"><span data-stu-id="c2ce0-167">Desktop \(touch\)</span></span> | <span data-ttu-id="c2ce0-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="c2ce0-168">Desktop</span></span> | <span data-ttu-id="c2ce0-169">Circle</span><span class="sxs-lookup"><span data-stu-id="c2ce0-169">Circle</span></span> | <span data-ttu-id="c2ce0-170">touch</span><span class="sxs-lookup"><span data-stu-id="c2ce0-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="c2ce0-171">Se você não vir a lista **tipo de dispositivo** , clique em **mais opções** e selecione **Adicionar tipo de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-171">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="c2ce0-172">Modo visor do dispositivo móvel</span><span class="sxs-lookup"><span data-stu-id="c2ce0-172">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="c2ce0-173">Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

> ##### <span data-ttu-id="c2ce0-174">Figura 6</span><span class="sxs-lookup"><span data-stu-id="c2ce0-174">Figure 6</span></span>  
> <span data-ttu-id="c2ce0-175">Lista de dispositivos</span><span class="sxs-lookup"><span data-stu-id="c2ce0-175">The Device list</span></span>  
> ![Lista de dispositivos][ImageDeviceList]  

#### <span data-ttu-id="c2ce0-177">Girar o visor para a orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="c2ce0-177">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="c2ce0-178">Clique em **girar** ![ rotação ][ImageRotateIcon] para girar o visor para a orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-178">Click **Rotate** ![Rotate][ImageRotateIcon] to rotate the viewport to landscape orientation.</span></span>  

> ##### <span data-ttu-id="c2ce0-179">Figura 7</span><span class="sxs-lookup"><span data-stu-id="c2ce0-179">Figure 7</span></span>  
> <span data-ttu-id="c2ce0-180">Orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="c2ce0-180">Landscape orientation</span></span>  
> ![Orientação paisagem][ImageLandscape]  

> [!NOTE]
> <span data-ttu-id="c2ce0-182">O botão **girar** desaparecerá se a **barra de ferramentas** do seu dispositivo for estreita.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-182">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="c2ce0-183">Figura 8</span><span class="sxs-lookup"><span data-stu-id="c2ce0-183">Figure 8</span></span>  
> <span data-ttu-id="c2ce0-184">A barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-184">The Device Toolbar</span></span>  
> ![A barra de ferramentas do dispositivo][ImageDeviceToolbar2]  

<span data-ttu-id="c2ce0-186">Consulte também [definir orientação](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="c2ce0-186">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="c2ce0-187">Mostrar quadro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-187">Show device frame</span></span>   

<span data-ttu-id="c2ce0-188">Ao simular as dimensões de um dispositivo móvel específico, como um iPhone 6, abra **mais opções** e selecione **Mostrar quadro de dispositivo** para mostrar a estrutura do dispositivo físico em torno do visor.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-188">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="c2ce0-189">Se você não vir um quadro de dispositivo para um dispositivo específico, provavelmente significa que o DevTools não tem arte para essa opção específica.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-189">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

> ##### <span data-ttu-id="c2ce0-190">Figura 9</span><span class="sxs-lookup"><span data-stu-id="c2ce0-190">Figure 9</span></span>  
> <span data-ttu-id="c2ce0-191">Mostrar quadro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-191">Show device frame</span></span>  
> ![Mostrar quadro de dispositivo][ImageShowDeviceFrame]  

> ##### <span data-ttu-id="c2ce0-193">Figura 10</span><span class="sxs-lookup"><span data-stu-id="c2ce0-193">Figure 10</span></span>  
> <span data-ttu-id="c2ce0-194">O quadro do dispositivo para o iPhone 6</span><span class="sxs-lookup"><span data-stu-id="c2ce0-194">The device frame for the iPhone 6</span></span>  
> ![O quadro do dispositivo para o iPhone 6][ImageIphoneFrame]  

#### <span data-ttu-id="c2ce0-196">Adicionar um dispositivo móvel personalizado</span><span class="sxs-lookup"><span data-stu-id="c2ce0-196">Add a custom mobile device</span></span>   

<span data-ttu-id="c2ce0-197">Para adicionar um dispositivo personalizado:</span><span class="sxs-lookup"><span data-stu-id="c2ce0-197">To add a custom device:</span></span>  

1.  <span data-ttu-id="c2ce0-198">Clique na lista de **dispositivos** e, em seguida, selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-198">Click the **Device** list and then select **Edit**.</span></span>  

> ##### <span data-ttu-id="c2ce0-199">Figura 11</span><span class="sxs-lookup"><span data-stu-id="c2ce0-199">Figure 11</span></span>  
> <span data-ttu-id="c2ce0-200">Selecionar **Editar** 
> ![ selecionando editar][ImageEdit]</span><span class="sxs-lookup"><span data-stu-id="c2ce0-200">Selecting **Edit**
![Selecting Edit][ImageEdit]</span></span>  

1.  <span data-ttu-id="c2ce0-201">Clique em **Adicionar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-201">Click **Add custom device**.</span></span>  

1.  <span data-ttu-id="c2ce0-202">Insira um nome, uma largura e uma altura para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-202">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="c2ce0-203">A [taxa de pixels de dispositivo][MDNWindowDevicePixelRatio], a [cadeia de caracteres do agente do usuário][MDNUserAgent]e os campos do tipo de [dispositivo](#set-the-device-type) são opcionais.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-203">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="c2ce0-204">O campo tipo de dispositivo é a lista definida como **celular** por padrão.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-204">The device type field is the list that is set to **Mobile** by default.</span></span>  

> ##### <span data-ttu-id="c2ce0-205">Figura 12</span><span class="sxs-lookup"><span data-stu-id="c2ce0-205">Figure 12</span></span>  
> <span data-ttu-id="c2ce0-206">Criando um dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="c2ce0-206">Creating a custom device</span></span>  
> ![Criando um dispositivo personalizado][ImageAddCustomDevice]  

### <span data-ttu-id="c2ce0-208">Mostrar réguas</span><span class="sxs-lookup"><span data-stu-id="c2ce0-208">Show rulers</span></span>   

<span data-ttu-id="c2ce0-209">Clique em **mais opções** e selecione **Mostrar réguas** para ver as réguas acima e à esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-209">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="c2ce0-210">A unidade de dimensionamento das réguas é pixels.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-210">The sizing unit of the rulers is pixels.</span></span>  

> ##### <span data-ttu-id="c2ce0-211">Figura 13</span><span class="sxs-lookup"><span data-stu-id="c2ce0-211">Figure 13</span></span>  
> <span data-ttu-id="c2ce0-212">Mostrar réguas</span><span class="sxs-lookup"><span data-stu-id="c2ce0-212">Show rulers</span></span>  
> ![Mostrar réguas][ImageShowRulers]  

> ##### <span data-ttu-id="c2ce0-214">Figura 14</span><span class="sxs-lookup"><span data-stu-id="c2ce0-214">Figure 14</span></span>  
> <span data-ttu-id="c2ce0-215">Réguas acima e à esquerda da viewport</span><span class="sxs-lookup"><span data-stu-id="c2ce0-215">Rulers above and to the left of the viewport</span></span>  
> ![Réguas acima e à esquerda da viewport][ImageRulers]  

### <span data-ttu-id="c2ce0-217">Aplicar zoom ao visor</span><span class="sxs-lookup"><span data-stu-id="c2ce0-217">Zoom the viewport</span></span>   

<span data-ttu-id="c2ce0-218">Use a lista **zoom** para ampliar ou reduzir.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-218">Use the **Zoom** list to zoom in or out.</span></span>  

> ##### <span data-ttu-id="c2ce0-219">Figura 15</span><span class="sxs-lookup"><span data-stu-id="c2ce0-219">Figure 15</span></span>  
> <span data-ttu-id="c2ce0-220">Zoom</span><span class="sxs-lookup"><span data-stu-id="c2ce0-220">Zoom</span></span>  
> ![Zoom][ImageZoomViewport]  

## <span data-ttu-id="c2ce0-222">Acelerar a rede e a CPU</span><span class="sxs-lookup"><span data-stu-id="c2ce0-222">Throttle the network and CPU</span></span>   

<span data-ttu-id="c2ce0-223">Para acelerar a rede e a CPU, selecione celular de **nível intermediário** ou **móvel de baixo** nível na lista **acelerador** .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-223">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="c2ce0-224">Figura 16</span><span class="sxs-lookup"><span data-stu-id="c2ce0-224">Figure 16</span></span>  
> <span data-ttu-id="c2ce0-225">Lista de aceleração</span><span class="sxs-lookup"><span data-stu-id="c2ce0-225">The Throttle list</span></span>  
> ![Lista de aceleração][ImageThrottling]  

<span data-ttu-id="c2ce0-227">O **Mobile de nível intermediário** simula a rede 3G rápida e acelera a CPU para que seja 4 vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-227">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="c2ce0-228">O **celular low-end** simula a 3G lenta e acelera a CPU 6 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-228">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="c2ce0-229">Lembre-se de que a limitação é relativa à funcionalidade normal do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-229">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="c2ce0-230">A lista de **aceleração** ficará oculta se a **barra de ferramentas** do seu dispositivo for estreita.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-230">The **Throttle** list will be hidden if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="c2ce0-231">Figura 17</span><span class="sxs-lookup"><span data-stu-id="c2ce0-231">Figure 17</span></span>  
> <span data-ttu-id="c2ce0-232">A barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2ce0-232">The Device Toolbar</span></span>  
> ![A barra de ferramentas do dispositivo][ImageDeviceToolbar3]  

### <span data-ttu-id="c2ce0-234">Acelerar apenas a CPU</span><span class="sxs-lookup"><span data-stu-id="c2ce0-234">Throttle the CPU only</span></span>   

<span data-ttu-id="c2ce0-235">Para controlar apenas a CPU e não a rede, vá para o **painel desempenho** , clique em capturar configurações de captura de **configurações** e ![ ][ImageCaptureIcon] selecione **4x** lentidão ou **lentidão 6x** na lista **CPU** .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-235">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** ![Capture Settings][ImageCaptureIcon], and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

> ##### <span data-ttu-id="c2ce0-236">Figura 18</span><span class="sxs-lookup"><span data-stu-id="c2ce0-236">Figure 18</span></span>  
> <span data-ttu-id="c2ce0-237">Lista da CPU</span><span class="sxs-lookup"><span data-stu-id="c2ce0-237">The CPU list</span></span>  
> ![Lista da CPU][ImageCPU]  

### <span data-ttu-id="c2ce0-239">Acelerar somente a rede</span><span class="sxs-lookup"><span data-stu-id="c2ce0-239">Throttle the network only</span></span>   

<span data-ttu-id="c2ce0-240">Para limitar apenas a rede e não a CPU, vá até **Network** o painel de rede **e selecione 3G** ou a **3G lento** na lista **aceleração** .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-240">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="c2ce0-241">Figura 19</span><span class="sxs-lookup"><span data-stu-id="c2ce0-241">Figure 19</span></span>  
> <span data-ttu-id="c2ce0-242">Lista de aceleração</span><span class="sxs-lookup"><span data-stu-id="c2ce0-242">The Throttle list</span></span>  
> ![Lista de aceleração][ImageNetwork]  

<span data-ttu-id="c2ce0-244">Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `3G` e selecione Habilitar a aceleração **3G rápida** ou **habilitar a limitação 3G lenta**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-244">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

> ##### <span data-ttu-id="c2ce0-245">Figura 20</span><span class="sxs-lookup"><span data-stu-id="c2ce0-245">Figure 20</span></span>  
> <span data-ttu-id="c2ce0-246">O menu de comando</span><span class="sxs-lookup"><span data-stu-id="c2ce0-246">The Command Menu</span></span>  
> ![O menu de comando][ImageCommandMenu]  

<span data-ttu-id="c2ce0-248">Você também pode definir a limitação de rede no painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-248">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="c2ce0-249">Clique em **capturar** ![ configurações de captura ][ImageCaptureIcon] e, em seguida, selecione 3G **rápido** ou **3G lento** na lista **rede** .</span><span class="sxs-lookup"><span data-stu-id="c2ce0-249">Click **Capture Settings** ![Capture Settings][ImageCaptureIcon] and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

> ##### <span data-ttu-id="c2ce0-250">Figura 21</span><span class="sxs-lookup"><span data-stu-id="c2ce0-250">Figure 21</span></span>  
> <span data-ttu-id="c2ce0-251">Definindo a limitação de rede no painel desempenho</span><span class="sxs-lookup"><span data-stu-id="c2ce0-251">Setting network throttling from the Performance panel</span></span>  
> ![Definindo a limitação de rede no painel desempenho][ImageNetwork2]  

## <span data-ttu-id="c2ce0-253">Substituir geolocalização</span><span class="sxs-lookup"><span data-stu-id="c2ce0-253">Override geolocation</span></span>   

<span data-ttu-id="c2ce0-254">Para abrir a interface do usuário que substitui a localização geográfica, clique em **Personalizar e controle devtools** `...` e selecione **mais**  >  **sensores**de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-254">To open the geolocation overriding UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="c2ce0-255">Figura 22</span><span class="sxs-lookup"><span data-stu-id="c2ce0-255">Figure 22</span></span>  
> <span data-ttu-id="c2ce0-256">Sensores</span><span class="sxs-lookup"><span data-stu-id="c2ce0-256">Sensors</span></span>  
> ![Sensores][ImageSensors]  

<span data-ttu-id="c2ce0-258">Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-258">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="c2ce0-259">Figura 23</span><span class="sxs-lookup"><span data-stu-id="c2ce0-259">Figure 23</span></span>  
> <span data-ttu-id="c2ce0-260">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="c2ce0-260">Show Sensors</span></span>  
> ![Mostrar sensores][ImageShowSensors]  

<span data-ttu-id="c2ce0-262">Selecione uma das predefinições **na lista geolocalização** ou selecione **local personalizado** para inserir suas próprias coordenadas ou selecione **localização indisponível** para testar como a sua página se comporta quando a localização geográfica está em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-262">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

> ##### <span data-ttu-id="c2ce0-263">Figura 24</span><span class="sxs-lookup"><span data-stu-id="c2ce0-263">Figure 24</span></span>  
> <span data-ttu-id="c2ce0-264">Geolocalização</span><span class="sxs-lookup"><span data-stu-id="c2ce0-264">Geolocation</span></span>  
> ![Geolocalização][ImageGeolocation]  

## <span data-ttu-id="c2ce0-266">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="c2ce0-266">Set orientation</span></span>   

<span data-ttu-id="c2ce0-267">Para abrir a interface do usuário de orientação, clique em **Personalizar e controle devtools** `...` e selecione **mais**  >  **sensores**de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-267">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="c2ce0-268">Figura 25</span><span class="sxs-lookup"><span data-stu-id="c2ce0-268">Figure 25</span></span>  
> <span data-ttu-id="c2ce0-269">Sensores</span><span class="sxs-lookup"><span data-stu-id="c2ce0-269">Sensors</span></span>  
> ![Sensores][ImageSensors2]  

<span data-ttu-id="c2ce0-271">Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-271">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="c2ce0-272">Figura 26</span><span class="sxs-lookup"><span data-stu-id="c2ce0-272">Figure 26</span></span>  
> <span data-ttu-id="c2ce0-273">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="c2ce0-273">Show Sensors</span></span>  
> ![Mostrar sensores][ImageShowSensors2]  

<span data-ttu-id="c2ce0-275">Selecione uma das predefinições na lista **orientação** ou selecione **orientação personalizada** para definir seus próprios valores Alfa, beta e gama.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-275">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

> ##### <span data-ttu-id="c2ce0-276">Figura 27</span><span class="sxs-lookup"><span data-stu-id="c2ce0-276">Figure 27</span></span>  
> <span data-ttu-id="c2ce0-277">Orientação</span><span class="sxs-lookup"><span data-stu-id="c2ce0-277">Orientation</span></span>  
> ![Orientação][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figura 1: a barra de ferramentas do dispositivo"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Figura 2: identificadores para alterar as dimensões do visor quando no modo de visor responsivo"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Figura 3: mostrar consultas de mídia"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Figura 4: clique em um ponto de interrupção para alterar a largura do visor"  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Figura 5: lista do tipo de dispositivo"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Figura 6: lista de dispositivos"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Figura 7: orientação paisagem"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figura 8: a barra de ferramentas do dispositivo"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Figura 9: mostrar quadro de dispositivo"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Figura 10: o quadro do dispositivo para o iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Figura 11: selecionando editar"  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Figura 12: Criando um dispositivo personalizado"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Figura 13: Mostrar réguas"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Figura 14: réguas acima e à esquerda da viewport"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Figura 15: zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Figura 16: a lista de aceleração"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figura 17: a barra de ferramentas do dispositivo"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Figura 18: lista da CPU"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Figura 19: a lista de aceleração"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Figura 20: o menu de comando"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Figura 21: definindo a limitação de rede no painel desempenho"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figura 22: sensores"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figura 23: mostrar sensores"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Figura 24: geolocalização"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figura 25: sensores"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figura 26: mostrar sensores"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Figura 27: orientação"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/devtools-Guide-Chromium/Remote-Debugging/index "introdução à depuração remota de dispositivos Android"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordem de aproximação-primeira ordem-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="c2ce0-310">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="c2ce0-310">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c2ce0-311">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c2ce0-311">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c2ce0-313">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c2ce0-313">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
