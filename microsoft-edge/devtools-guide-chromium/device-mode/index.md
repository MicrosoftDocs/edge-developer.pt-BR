---
title: Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6973f28a0cb530e8928976adb1354fa7471ee343
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985208"
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





# <span data-ttu-id="ca2dd-103">Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ca2dd-103">Simulate mobile devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="ca2dd-104">Use o modo de dispositivo para aproximar a aparência e a execução de sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="ca2dd-105">O modo de dispositivo é o nome para a coleção flexível de recursos no Microsoft Edge DevTools que ajudam você a simular dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="ca2dd-106">Esses recursos incluem:</span><span class="sxs-lookup"><span data-stu-id="ca2dd-106">These features include:</span></span>  

*   [<span data-ttu-id="ca2dd-107">Simulando um visor móvel</span><span class="sxs-lookup"><span data-stu-id="ca2dd-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="ca2dd-108">Otimizando a rede</span><span class="sxs-lookup"><span data-stu-id="ca2dd-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="ca2dd-109">Otimizando a CPU</span><span class="sxs-lookup"><span data-stu-id="ca2dd-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="ca2dd-110">Simulação de localização geográfica</span><span class="sxs-lookup"><span data-stu-id="ca2dd-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="ca2dd-111">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="ca2dd-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="ca2dd-112">Limitações</span><span class="sxs-lookup"><span data-stu-id="ca2dd-112">Limitations</span></span>   

<span data-ttu-id="ca2dd-113">Pense no modo de dispositivo como uma [aproximação de primeira ordem][WikiApproximation] de como a sua página se parece e se sente em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="ca2dd-114">Com o modo de dispositivo, você não executa o código em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="ca2dd-115">Você simula a experiência do usuário móvel do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="ca2dd-116">Há alguns aspectos dos dispositivos móveis que o DevTools nunca poderá simular.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="ca2dd-117">Por exemplo, a arquitetura de CPUs móveis é muito diferente da arquitetura de CPUs para laptop ou desktop.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="ca2dd-118">Quando estiver em dúvida, a melhor opção é realmente executar sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="ca2dd-119">Use [depuração remota] [DevToolsRemoteDebugging] para exibir, alterar, depurar e criar o perfil do código de uma página do laptop ou da área de trabalho, enquanto ela é executada em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="ca2dd-120">Simular um visor móvel</span><span class="sxs-lookup"><span data-stu-id="ca2dd-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="ca2dd-121">Clique em **alternar barra de ferramentas de dispositivo** \ ( ![ alternar barra ][ImageDeviceToolbarIcon] de ferramentas de dispositivo \) para abrir a interface do usuário que permite simular um visor móvel.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-121">Click **Toggle Device Toolbar** \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="ca2dd-123">A barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca2dd-123">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="ca2dd-124">Por padrão, a barra de ferramentas do dispositivo é aberta no modo de visor responsivo.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-124">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="ca2dd-125">Modo de visor responsivo</span><span class="sxs-lookup"><span data-stu-id="ca2dd-125">Responsive Viewport Mode</span></span>   

<span data-ttu-id="ca2dd-126">Arraste as alças para redimensionar o visor para qualquer dimensão necessária.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-126">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="ca2dd-127">Ou insira valores específicos nas caixas largura e altura.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-127">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="ca2dd-128">Na figura a seguir, a largura é definida como `626` e a altura é definida como `516` .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-128">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="As alças para alterar as dimensões do visor quando no modo de visor responsivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   <span data-ttu-id="ca2dd-130">As alças para alterar as dimensões do visor quando no modo de visor responsivo</span><span class="sxs-lookup"><span data-stu-id="ca2dd-130">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="ca2dd-131">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="ca2dd-131">Show media queries</span></span>   

<span data-ttu-id="ca2dd-132">Para mostrar pontos de interrupção de consulta de mídia acima do visor, clique em **mais opções** e selecione **Mostrar consultas de mídia**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-132">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas de mídia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="ca2dd-134">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="ca2dd-134">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="ca2dd-135">Clique em um ponto de interrupção para alterar a largura do visor para que o ponto de interrupção seja disparado.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-135">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Clique em um ponto de interrupção para alterar a largura do visor" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="ca2dd-137">Clique em um ponto de interrupção para alterar a largura do visor</span><span class="sxs-lookup"><span data-stu-id="ca2dd-137">Click a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="ca2dd-138">Definir o tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca2dd-138">Set the device type</span></span>   

<span data-ttu-id="ca2dd-139">Use a lista **tipo de dispositivo** para simular um dispositivo móvel ou um dispositivo de desktop.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-139">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="A lista tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="ca2dd-141">A lista **tipo de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-141">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="ca2dd-142">A tabela a seguir descreve as diferenças entre as opções.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-142">The table below describes the differences between the options.</span></span>  <span data-ttu-id="ca2dd-143">**Método de renderização** refere-se ao Microsoft Edge renderiza a página como um visor móvel ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-143">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="ca2dd-144">**Ícone do cursor** refere-se ao tipo de cursor que você vê quando passa o mouse sobre a página.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-144">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="ca2dd-145">Os **eventos acionados** referem-se à página `touch` ou `click` eventos quando você interage com a página.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-145">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="ca2dd-146">Opção</span><span class="sxs-lookup"><span data-stu-id="ca2dd-146">Option</span></span> | <span data-ttu-id="ca2dd-147">Método de renderização</span><span class="sxs-lookup"><span data-stu-id="ca2dd-147">Rendering method</span></span> | <span data-ttu-id="ca2dd-148">Ícone de cursor</span><span class="sxs-lookup"><span data-stu-id="ca2dd-148">Cursor icon</span></span> | <span data-ttu-id="ca2dd-149">Eventos acionados</span><span class="sxs-lookup"><span data-stu-id="ca2dd-149">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="ca2dd-150">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="ca2dd-150">Mobile</span></span> | <span data-ttu-id="ca2dd-151">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="ca2dd-151">Mobile</span></span> | <span data-ttu-id="ca2dd-152">Circle</span><span class="sxs-lookup"><span data-stu-id="ca2dd-152">Circle</span></span> | <span data-ttu-id="ca2dd-153">touch</span><span class="sxs-lookup"><span data-stu-id="ca2dd-153">touch</span></span> |  
| <span data-ttu-id="ca2dd-154">Celular \ (sem toque \)</span><span class="sxs-lookup"><span data-stu-id="ca2dd-154">Mobile \(no touch\)</span></span> | <span data-ttu-id="ca2dd-155">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="ca2dd-155">Mobile</span></span> | <span data-ttu-id="ca2dd-156">Normal</span><span class="sxs-lookup"><span data-stu-id="ca2dd-156">Normal</span></span> | <span data-ttu-id="ca2dd-157"> clique em </span><span class="sxs-lookup"><span data-stu-id="ca2dd-157">click</span></span> |  
| <span data-ttu-id="ca2dd-158">Desktop</span><span class="sxs-lookup"><span data-stu-id="ca2dd-158">Desktop</span></span> | <span data-ttu-id="ca2dd-159">Desktop</span><span class="sxs-lookup"><span data-stu-id="ca2dd-159">Desktop</span></span> | <span data-ttu-id="ca2dd-160">Normal</span><span class="sxs-lookup"><span data-stu-id="ca2dd-160">Normal</span></span> | <span data-ttu-id="ca2dd-161"> clique em </span><span class="sxs-lookup"><span data-stu-id="ca2dd-161">click</span></span> |  
| <span data-ttu-id="ca2dd-162">Área de trabalho \ (Touch \)</span><span class="sxs-lookup"><span data-stu-id="ca2dd-162">Desktop \(touch\)</span></span> | <span data-ttu-id="ca2dd-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="ca2dd-163">Desktop</span></span> | <span data-ttu-id="ca2dd-164">Circle</span><span class="sxs-lookup"><span data-stu-id="ca2dd-164">Circle</span></span> | <span data-ttu-id="ca2dd-165">touch</span><span class="sxs-lookup"><span data-stu-id="ca2dd-165">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="ca2dd-166">Se você não vir a lista **tipo de dispositivo** , clique em **mais opções** e selecione **Adicionar tipo de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-166">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="ca2dd-167">Modo visor do dispositivo móvel</span><span class="sxs-lookup"><span data-stu-id="ca2dd-167">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="ca2dd-168">Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-168">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="ca2dd-170">Lista de **dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-170">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="ca2dd-171">Girar o visor para a orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="ca2dd-171">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="ca2dd-172">Clique em **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar o visor para a orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-172">Click **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Orientação paisagem" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   <span data-ttu-id="ca2dd-174">Orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="ca2dd-174">Landscape orientation</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ca2dd-175">O botão **girar** desaparecerá se a **barra de ferramentas** do seu dispositivo for estreita.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-175">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="ca2dd-177">A **barra de ferramentas do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-177">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="ca2dd-178">Consulte também [definir orientação](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="ca2dd-178">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="ca2dd-179">Mostrar quadro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca2dd-179">Show device frame</span></span>   

<span data-ttu-id="ca2dd-180">Ao simular as dimensões de um dispositivo móvel específico, como um iPhone 6, abra **mais opções** e selecione **Mostrar quadro de dispositivo** para mostrar a estrutura do dispositivo físico em torno do visor.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-180">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="ca2dd-181">Se você não vir um quadro de dispositivo para um dispositivo específico, provavelmente significa que o DevTools não tem arte para essa opção específica.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-181">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar quadro de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="ca2dd-183">Mostrar quadro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca2dd-183">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="O quadro do dispositivo para o iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="ca2dd-185">O quadro do dispositivo para o iPhone 6</span><span class="sxs-lookup"><span data-stu-id="ca2dd-185">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="ca2dd-186">Adicionar um dispositivo móvel personalizado</span><span class="sxs-lookup"><span data-stu-id="ca2dd-186">Add a custom mobile device</span></span>   

<span data-ttu-id="ca2dd-187">Para adicionar um dispositivo personalizado:</span><span class="sxs-lookup"><span data-stu-id="ca2dd-187">To add a custom device:</span></span>  

1.  <span data-ttu-id="ca2dd-188">Clique na lista de **dispositivos** e, em seguida, selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-188">Click the **Device** list and then select **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Selecione Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="ca2dd-190">Selecione **Editar**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-190">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ca2dd-191">Clique em **Adicionar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-191">Click **Add custom device**.</span></span>  
1.  <span data-ttu-id="ca2dd-192">Insira um nome, uma largura e uma altura para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-192">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="ca2dd-193">A [taxa de pixels de dispositivo][MDNWindowDevicePixelRatio], a [cadeia de caracteres do agente do usuário][MDNUserAgent]e os campos do tipo de [dispositivo](#set-the-device-type) são opcionais.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-193">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="ca2dd-194">O campo tipo de dispositivo é a lista definida como **celular** por padrão.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-194">The device type field is the list that is set to **Mobile** by default.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Criar um dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="ca2dd-196">Criar dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="ca2dd-196">Createa custom device</span></span>  
    :::image-end:::  

### <span data-ttu-id="ca2dd-197">Mostrar réguas</span><span class="sxs-lookup"><span data-stu-id="ca2dd-197">Show rulers</span></span>   

<span data-ttu-id="ca2dd-198">Clique em **mais opções** e selecione **Mostrar réguas** para ver as réguas acima e à esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-198">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="ca2dd-199">A unidade de dimensionamento das réguas é pixels.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-199">The sizing unit of the rulers is pixels.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Mostrar réguas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **<span data-ttu-id="ca2dd-201">Mostrar réguas</span><span class="sxs-lookup"><span data-stu-id="ca2dd-201">Show rulers</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Réguas acima e à esquerda da viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="ca2dd-203">Réguas acima e à esquerda da viewport</span><span class="sxs-lookup"><span data-stu-id="ca2dd-203">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="ca2dd-204">Aplicar zoom ao visor</span><span class="sxs-lookup"><span data-stu-id="ca2dd-204">Zoom the viewport</span></span>   

<span data-ttu-id="ca2dd-205">Use a lista **zoom** para ampliar ou reduzir.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-205">Use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="ca2dd-207">Zoom</span><span class="sxs-lookup"><span data-stu-id="ca2dd-207">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="ca2dd-208">Acelerar a rede e a CPU</span><span class="sxs-lookup"><span data-stu-id="ca2dd-208">Throttle the network and CPU</span></span>   

<span data-ttu-id="ca2dd-209">Para acelerar a rede e a CPU, selecione celular de **nível intermediário** ou **móvel de baixo** nível na lista **acelerador** .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-209">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Lista de aceleração" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="ca2dd-211">Lista de **aceleração**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-211">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="ca2dd-212">O **Mobile de nível intermediário** simula a rede 3G rápida e acelera a CPU para que seja 4 vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-212">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="ca2dd-213">O **celular low-end** simula a 3G lenta e acelera a CPU 6 vezes mais lenta do que o normal.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-213">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="ca2dd-214">Lembre-se de que a limitação é relativa à funcionalidade normal do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-214">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="ca2dd-215">A lista de **aceleração** fica oculta se a **barra de ferramentas** do seu dispositivo for estreita.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-215">The **Throttle** list is hidden if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="ca2dd-217">A **barra de ferramentas do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-217">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="ca2dd-218">Acelerar apenas a CPU</span><span class="sxs-lookup"><span data-stu-id="ca2dd-218">Throttle the CPU only</span></span>   

<span data-ttu-id="ca2dd-219">Para controlar apenas a CPU e não a rede, vá para o painel **desempenho** , clique em **configurações de captura** \ (configurações de ![ captura ][ImageCaptureIcon] \) e selecione **4x** lentidão ou **lentidão 6x** na lista **CPU** .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-219">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\), and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Lista da CPU" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   <span data-ttu-id="ca2dd-221">Lista **da CPU**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-221">The **CPU** list</span></span>  
:::image-end:::  

### <span data-ttu-id="ca2dd-222">Acelerar somente a rede</span><span class="sxs-lookup"><span data-stu-id="ca2dd-222">Throttle the network only</span></span>   

<span data-ttu-id="ca2dd-223">Para limitar apenas a rede e não a CPU, vá até **Network** o painel de rede **e selecione 3G** ou a **3G lento** na lista **aceleração** .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-223">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Lista de aceleração" lightbox="../media/device-mode-network-throttle.msft.png":::
   <span data-ttu-id="ca2dd-225">Lista de **aceleração**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-225">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="ca2dd-226">Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**, digite `3G` e selecione Habilitar a aceleração **3G rápida** ou **habilitar a limitação 3G lenta**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-226">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   <span data-ttu-id="ca2dd-228">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-228">The **Command Menu**</span></span>  
:::image-end:::  

<span data-ttu-id="ca2dd-229">Você também pode definir a limitação de rede no painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-229">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="ca2dd-230">Clique em **configurações de captura** \ ( ![ capturar configurações ][ImageCaptureIcon] \) e, em seguida, selecione 3G **rápido** ou **3G lento** na lista **rede** .</span><span class="sxs-lookup"><span data-stu-id="ca2dd-230">Click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Definir a limitação de rede no painel desempenho" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   <span data-ttu-id="ca2dd-232">Definir a limitação de rede no painel **desempenho**</span><span class="sxs-lookup"><span data-stu-id="ca2dd-232">Set network throttling from the **Performance** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="ca2dd-233">Substituir geolocalização</span><span class="sxs-lookup"><span data-stu-id="ca2dd-233">Override geolocation</span></span>   

<span data-ttu-id="ca2dd-234">Para abrir a interface do usuário que substitui a localização geográfica, clique em **Personalizar e controle devtools** \ ( `...` \) e selecione **mais**  >  **sensores**de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-234">To open the geolocation overriding UI click **Customize and control DevTools** \(`...`\) and then select **More tools** > **Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **<span data-ttu-id="ca2dd-236">Sensores</span><span class="sxs-lookup"><span data-stu-id="ca2dd-236">Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="ca2dd-237">Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-237">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **<span data-ttu-id="ca2dd-239">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="ca2dd-239">Show Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="ca2dd-240">Selecione uma das predefinições **na lista geolocalização** ou selecione **local personalizado** para inserir suas próprias coordenadas ou selecione **localização indisponível** para testar como a sua página se comporta quando a localização geográfica está em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-240">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Geolocalização" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **<span data-ttu-id="ca2dd-242">Geolocalização</span><span class="sxs-lookup"><span data-stu-id="ca2dd-242">Geolocation</span></span>**  
:::image-end:::  

## <span data-ttu-id="ca2dd-243">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="ca2dd-243">Set orientation</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="ca2dd-244">Para abrir a interface do usuário de orientação, clique em **Personalizar e controle devtools** `...` e selecione **mais**  >  **sensores**de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-244">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **<span data-ttu-id="ca2dd-246">Sensores</span><span class="sxs-lookup"><span data-stu-id="ca2dd-246">Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ca2dd-247">Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-247">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **<span data-ttu-id="ca2dd-249">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="ca2dd-249">Show Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="ca2dd-250">Selecione uma das predefinições na lista **orientação** ou selecione **orientação personalizada** para definir seus próprios valores Alfa, beta e gama.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-250">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Orientação" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **<span data-ttu-id="ca2dd-252">Orientação</span><span class="sxs-lookup"><span data-stu-id="ca2dd-252">Orientation</span></span>**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "comece a usar dispositivos Android de depuração remota | Documentos da Microsoft "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordem de aproximação-primeira ordem-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="ca2dd-257">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ca2dd-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ca2dd-258">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ca2dd-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ca2dd-260">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ca2dd-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
