---
description: Use dispositivos virtuais no Microsoft Edge para criar sites do primeiro celular.
title: Emular dispositivos móveis no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, emulação, dispositivo, simulação, celular
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997005"
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

# <span data-ttu-id="63e6c-104">Emular dispositivos móveis no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63e6c-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="63e6c-105">Use a **emulação de dispositivo** para aproximar a aparência da página e responder em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="63e6c-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="63e6c-106">O Microsoft Edge DevTools fornece um conjunto de recursos para ajudá-lo a emular dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="63e6c-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="63e6c-107">A coleção inclui os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e6c-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="63e6c-108">Simular um visor móvel</span><span class="sxs-lookup"><span data-stu-id="63e6c-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="63e6c-109">Acelerar a rede</span><span class="sxs-lookup"><span data-stu-id="63e6c-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="63e6c-110">Acelerar a CPU</span><span class="sxs-lookup"><span data-stu-id="63e6c-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="63e6c-111">Simular geolocalização</span><span class="sxs-lookup"><span data-stu-id="63e6c-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="63e6c-112">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="63e6c-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="63e6c-113">Definir a cadeia de caracteres do agente do usuário</span><span class="sxs-lookup"><span data-stu-id="63e6c-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <span data-ttu-id="63e6c-114">Limitações</span><span class="sxs-lookup"><span data-stu-id="63e6c-114">Limitations</span></span>  

<span data-ttu-id="63e6c-115">**Emulação de dispositivo** é uma [aproximação de primeira ordem][WikiApproximation] da aparência da sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="63e6c-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="63e6c-116">A **emulação de dispositivo** não executa realmente o código em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="63e6c-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="63e6c-117">Em vez disso, você simula a experiência do usuário móvel do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="63e6c-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="63e6c-118">Alguns aspectos de dispositivos móveis nunca são emulados no DevTools.</span><span class="sxs-lookup"><span data-stu-id="63e6c-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="63e6c-119">Por exemplo, a arquitetura de CPUs móveis é diferente da arquitetura de CPUs para laptop ou desktop.</span><span class="sxs-lookup"><span data-stu-id="63e6c-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="63e6c-120">Quando estiver em dúvida, a melhor opção é realmente executar sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="63e6c-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="63e6c-121">Use [depuração remota] [DevToolsRemoteDebugging] para interagir com o código de uma página de seu computador enquanto sua página realmente é executada em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="63e6c-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="63e6c-122">Você pode exibir, alterar, depurar, criar perfil ou todos os quatro enquanto interage com o código.</span><span class="sxs-lookup"><span data-stu-id="63e6c-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="63e6c-123">Seu computador pode ser um notebook ou computador de mesa.</span><span class="sxs-lookup"><span data-stu-id="63e6c-123">Your machine may be a notebook or desktop computer.</span></span>  

## <span data-ttu-id="63e6c-124">Simular um visor móvel</span><span class="sxs-lookup"><span data-stu-id="63e6c-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="63e6c-125">Escolha **alternar emulação de dispositivo**  \ ( ![ alternar barra de ferramentas de dispositivo ][ImageDeviceToolbarIcon] \) ou escolha **Personalizar e controlar devtools** \ ( `...` \) > **emulação de dispositivo** para abrir a interface do usuário que permite simular um visor móvel.</span><span class="sxs-lookup"><span data-stu-id="63e6c-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="63e6c-127">A barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="63e6c-128">Por padrão, a barra de ferramentas do dispositivo é aberta no modo de visor responsivo.</span><span class="sxs-lookup"><span data-stu-id="63e6c-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="63e6c-129">Modo de visor responsivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="63e6c-130">Para testar rapidamente a aparência da sua página em vários tamanhos de tela, arraste as alças para redimensionar o visor para suas dimensões obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="63e6c-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="63e6c-131">Você também pode inserir valores específicos nas caixas largura e altura.</span><span class="sxs-lookup"><span data-stu-id="63e6c-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="63e6c-132">Na figura a seguir, a largura é definida como `626` e a altura é definida como `516` .</span><span class="sxs-lookup"><span data-stu-id="63e6c-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="As alças para alterar as dimensões do visor quando no modo de visor responsivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="63e6c-134">As alças para alterar as dimensões do visor quando no modo de visor responsivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="63e6c-135">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="63e6c-135">Show media queries</span></span>  

<span data-ttu-id="63e6c-136">Se você definiu consultas de mídia em sua página, vá para as dimensões do visor em que essas consultas de mídia entram em vigor mostrando pontos de interrupção de consulta de mídia acima do visor.</span><span class="sxs-lookup"><span data-stu-id="63e6c-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="63e6c-137">Escolha **mais opções**  >  **Mostrar consultas de mídia**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas de mídia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="63e6c-139">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="63e6c-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="63e6c-140">Escolha um ponto de interrupção para alterar a largura do visor para que a consulta de mídia seja disparada.</span><span class="sxs-lookup"><span data-stu-id="63e6c-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Escolher um ponto de interrupção para alterar a largura do visor" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="63e6c-142">Escolher um ponto de interrupção para alterar a largura do visor</span><span class="sxs-lookup"><span data-stu-id="63e6c-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="63e6c-143">Definir o tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-143">Set the device type</span></span>  

<span data-ttu-id="63e6c-144">Use a lista **tipo de dispositivo** para simular um dispositivo móvel ou um dispositivo de desktop.</span><span class="sxs-lookup"><span data-stu-id="63e6c-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="A lista tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="63e6c-146">A lista **tipo de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="63e6c-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="63e6c-147">A tabela a seguir descreve as diferenças entre as opções de tipo de dispositivo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="63e6c-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="63e6c-148">A coluna método de renderização refere-se ao Microsoft Edge renderiza a página como um visor móvel ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="63e6c-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="63e6c-149">A coluna do ícone do cursor refere-se ao tipo de cursor que você vê quando passa o mouse sobre a página.</span><span class="sxs-lookup"><span data-stu-id="63e6c-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span></span>  <span data-ttu-id="63e6c-150">A coluna eventos disparados se refere a um gatilho de página `touch` ou `click` eventos quando você interage com a página.</span><span class="sxs-lookup"><span data-stu-id="63e6c-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="63e6c-151">Opção</span><span class="sxs-lookup"><span data-stu-id="63e6c-151">Option</span></span> | <span data-ttu-id="63e6c-152">Método de renderização</span><span class="sxs-lookup"><span data-stu-id="63e6c-152">Rendering method</span></span> | <span data-ttu-id="63e6c-153">Ícone de cursor</span><span class="sxs-lookup"><span data-stu-id="63e6c-153">Cursor icon</span></span> | <span data-ttu-id="63e6c-154">Eventos disparados</span><span class="sxs-lookup"><span data-stu-id="63e6c-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="63e6c-155">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="63e6c-155">Mobile</span></span> | <span data-ttu-id="63e6c-156">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="63e6c-156">Mobile</span></span> | <span data-ttu-id="63e6c-157">Circle</span><span class="sxs-lookup"><span data-stu-id="63e6c-157">Circle</span></span> | <span data-ttu-id="63e6c-158">touch</span><span class="sxs-lookup"><span data-stu-id="63e6c-158">touch</span></span> |  
| <span data-ttu-id="63e6c-159">Celular \ (sem toque \)</span><span class="sxs-lookup"><span data-stu-id="63e6c-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="63e6c-160">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="63e6c-160">Mobile</span></span> | <span data-ttu-id="63e6c-161">Normal</span><span class="sxs-lookup"><span data-stu-id="63e6c-161">Normal</span></span> | <span data-ttu-id="63e6c-162"> clique em </span><span class="sxs-lookup"><span data-stu-id="63e6c-162">click</span></span> |  
| <span data-ttu-id="63e6c-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="63e6c-163">Desktop</span></span> | <span data-ttu-id="63e6c-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="63e6c-164">Desktop</span></span> | <span data-ttu-id="63e6c-165">Normal</span><span class="sxs-lookup"><span data-stu-id="63e6c-165">Normal</span></span> | <span data-ttu-id="63e6c-166"> clique em </span><span class="sxs-lookup"><span data-stu-id="63e6c-166">click</span></span> |  
| <span data-ttu-id="63e6c-167">Área de trabalho \ (Touch \)</span><span class="sxs-lookup"><span data-stu-id="63e6c-167">Desktop \(touch\)</span></span> | <span data-ttu-id="63e6c-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="63e6c-168">Desktop</span></span> | <span data-ttu-id="63e6c-169">Circle</span><span class="sxs-lookup"><span data-stu-id="63e6c-169">Circle</span></span> | <span data-ttu-id="63e6c-170">touch</span><span class="sxs-lookup"><span data-stu-id="63e6c-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="63e6c-171">Se a lista **tipo de dispositivo** não for exibida, escolha **mais opções**  >  **Adicionar tipo de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <span data-ttu-id="63e6c-172">Modo visor do dispositivo móvel</span><span class="sxs-lookup"><span data-stu-id="63e6c-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="63e6c-173">Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="63e6c-175">Lista de **dispositivos**</span><span class="sxs-lookup"><span data-stu-id="63e6c-175">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="63e6c-176">Girar o visor para a orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="63e6c-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="63e6c-177">Teste sua página da Web na orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="63e6c-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="63e6c-178">Para girar o visor para a orientação paisagem, escolha **girar** \ ( ![ girar ][ImageRotateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="63e6c-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Página exibida na orientação paisagem" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="63e6c-180">Página exibida na orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="63e6c-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="63e6c-181">O botão **girar** desaparecerá se a **barra de ferramentas** do seu dispositivo for estreita.</span><span class="sxs-lookup"><span data-stu-id="63e6c-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="63e6c-183">A **barra de ferramentas do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="63e6c-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="63e6c-184">Para obter mais informações, vá para [definir orientação](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="63e6c-184">For more information, go to [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="63e6c-185">Mostrar quadro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-185">Show device frame</span></span>  

<span data-ttu-id="63e6c-186">Exiba o quadro do dispositivo físico ao lado do visor ao simular as dimensões de um dispositivo móvel específico, como um iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="63e6c-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="63e6c-187">Abrir **mais opções**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="63e6c-188">Escolha **Mostrar quadro de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="63e6c-189">Se você não vir um quadro de dispositivo para um dispositivo específico, isso significa que o DevTools não tem arte para essa opção.</span><span class="sxs-lookup"><span data-stu-id="63e6c-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar quadro de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="63e6c-191">Mostrar quadro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="O quadro do dispositivo para o iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="63e6c-193">O quadro do dispositivo para o iPhone 6</span><span class="sxs-lookup"><span data-stu-id="63e6c-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="63e6c-194">Adicionar um dispositivo móvel personalizado</span><span class="sxs-lookup"><span data-stu-id="63e6c-194">Add a custom mobile device</span></span>  

<span data-ttu-id="63e6c-195">Se a opção de dispositivo móvel necessária não estiver incluída na lista padrão, você poderá adicionar um dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="63e6c-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="63e6c-196">Para adicionar um dispositivo personalizado, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e6c-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="63e6c-197">Escolha a lista de **dispositivos** > **Editar**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Selecione Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="63e6c-199">Selecione **Editar**</span><span class="sxs-lookup"><span data-stu-id="63e6c-199">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="63e6c-200">Escolha **Adicionar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="63e6c-201">Em **dispositivos emulados**, insira um nome de dispositivo, a largura da tela e a altura da tela do dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="63e6c-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="63e6c-202">A [taxa de pixels de dispositivo][MDNWindowDevicePixelRatio], a [cadeia de caracteres do agente do usuário][MDNUserAgent]e os campos do tipo de [dispositivo](#set-the-device-type) são opcionais.</span><span class="sxs-lookup"><span data-stu-id="63e6c-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="63e6c-203">O campo tipo de dispositivo é definido como padrão para **celular**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Criar um dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="63e6c-205">Criar um dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="63e6c-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="63e6c-206">Mostrar réguas</span><span class="sxs-lookup"><span data-stu-id="63e6c-206">Show rulers</span></span>  

<span data-ttu-id="63e6c-207">Se precisar medir as dimensões da tela, você pode usar réguas para medir o tamanho da tela em pixels.</span><span class="sxs-lookup"><span data-stu-id="63e6c-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="63e6c-208">Escolha **mais opções**  >  **Mostrar réguas** para exibir réguas acima e à esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="63e6c-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Item de menu para exibir réguas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="63e6c-210">Item de menu para exibir réguas</span><span class="sxs-lookup"><span data-stu-id="63e6c-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Réguas acima e à esquerda da viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="63e6c-212">Réguas acima e à esquerda da viewport</span><span class="sxs-lookup"><span data-stu-id="63e6c-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="63e6c-213">Aplicar zoom ao visor</span><span class="sxs-lookup"><span data-stu-id="63e6c-213">Zoom the viewport</span></span>  

<span data-ttu-id="63e6c-214">Para testar a aparência da sua página em vários níveis de zoom, use a lista de **zoom** para ampliar ou reduzir.</span><span class="sxs-lookup"><span data-stu-id="63e6c-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="63e6c-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="63e6c-216">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="63e6c-217">Acelerar a rede e a CPU</span><span class="sxs-lookup"><span data-stu-id="63e6c-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="63e6c-218">Os dispositivos móveis geralmente têm restrições de rede e CPU.</span><span class="sxs-lookup"><span data-stu-id="63e6c-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="63e6c-219">Certifique-se de testar a rapidez com que sua página é carregada e como ela responde em velocidades de CPU e de Internet diferentes.</span><span class="sxs-lookup"><span data-stu-id="63e6c-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="63e6c-220">Acelera a rede e a CPU.</span><span class="sxs-lookup"><span data-stu-id="63e6c-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="63e6c-221">Escolha lista de **aceleração** e altere a predefinição para móvel médio ou **celular de baixo** **nível** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="63e6c-222">O **celular de nível intermediário** simula `fast 3G` e acelera a CPU.</span><span class="sxs-lookup"><span data-stu-id="63e6c-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="63e6c-223">É quatro vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="63e6c-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="63e6c-224">O **celular low-end** simula `slow 3G` e acelera a CPU.</span><span class="sxs-lookup"><span data-stu-id="63e6c-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="63e6c-225">É seis vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="63e6c-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="63e6c-226">Toda a limitação se baseia na funcionalidade normal do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="63e6c-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="A lista de aceleração na barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="63e6c-228">A lista de **aceleração** na barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="63e6c-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="63e6c-229">Se a **lista de aceleração** estiver oculta, a **barra de ferramentas** do seu dispositivo é estreita demais.</span><span class="sxs-lookup"><span data-stu-id="63e6c-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="63e6c-230">Para acessar a **lista de aceleração**, aumente a largura da **barra de ferramentas do dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="63e6c-232">A **barra de ferramentas do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="63e6c-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="63e6c-233">Acelerar apenas a CPU</span><span class="sxs-lookup"><span data-stu-id="63e6c-233">Throttle the CPU only</span></span>  

<span data-ttu-id="63e6c-234">Para acelerar apenas a CPU e não a rede, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e6c-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="63e6c-235">Escolha o painel **desempenho** e escolha **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="63e6c-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="63e6c-236">Escolha a **CPU**  >  **4x lentidão** ou **lentidão 6x**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Lista CPU no painel desempenho" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="63e6c-238">Lista **CPU** no painel **desempenho**</span><span class="sxs-lookup"><span data-stu-id="63e6c-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="63e6c-239">Acelerar somente a rede</span><span class="sxs-lookup"><span data-stu-id="63e6c-239">Throttle the network only</span></span>  

<span data-ttu-id="63e6c-240">Para controlar apenas a rede, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e6c-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="63e6c-241">Escolha o painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-241">Choose the **Network** panel.</span></span>
1.  <span data-ttu-id="63e6c-242">Escolha **online**  >  **Fast 3G** ou **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="A lista de aceleração no painel de rede" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="63e6c-244">A lista de **aceleração** no painel de rede</span><span class="sxs-lookup"><span data-stu-id="63e6c-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="63e6c-245">Ou selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**, digite `3G` e escolha **habilitar a limitação de 3G rápido** ou **habilitar a limitação 3G lenta**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-245">Or select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="63e6c-247">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="63e6c-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="63e6c-248">Você também pode definir a limitação de rede no painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="63e6c-249">Escolha **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureIcon] \) e escolha a lista de **redes** e altere a predefinição para 3G **rápido** ou **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Definir a limitação de rede no painel desempenho" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="63e6c-251">Definir a limitação de rede no painel **desempenho**</span><span class="sxs-lookup"><span data-stu-id="63e6c-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="63e6c-252">Substituir geolocalização</span><span class="sxs-lookup"><span data-stu-id="63e6c-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="63e6c-253">Se sua página depende de informações de localização geográfica de um dispositivo móvel para renderização apropriada, forneça geolocalidades diferentes usando a interface do usuário de substituição de localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="63e6c-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="63e6c-254">Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais**  >  **sensores**de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="63e6c-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores de localização geográfica" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="63e6c-256">**Sensores** de localização geográfica</span><span class="sxs-lookup"><span data-stu-id="63e6c-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="63e6c-257">Abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="63e6c-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="63e6c-258">Selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="63e6c-258">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="63e6c-259">Digite `Sensors` e escolha **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores de localização geográfica" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="63e6c-261">**Mostrar sensores** de localização geográfica</span><span class="sxs-lookup"><span data-stu-id="63e6c-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="63e6c-262">No painel **sensores** , você pode selecionar um dos locais predefinidos incluídos no devtools usando o menu suspenso **Location** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="63e6c-263">Para inserir um local personalizado, escolha **outros...**</span><span class="sxs-lookup"><span data-stu-id="63e6c-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="63e6c-264">e insira as coordenadas do seu local personalizado.</span><span class="sxs-lookup"><span data-stu-id="63e6c-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="63e6c-265">Para testar sua página em um estado de erro quando as informações de localização não estiverem disponíveis, escolha **local indisponível**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Painel de sensores com um local predefinido selecionado" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="63e6c-267">Painel de **sensores** com um local predefinido selecionado.</span><span class="sxs-lookup"><span data-stu-id="63e6c-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <span data-ttu-id="63e6c-268">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="63e6c-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="63e6c-269">Se sua página depende de informações de orientação de um dispositivo móvel para renderização apropriada, abra a interface do usuário de orientação.</span><span class="sxs-lookup"><span data-stu-id="63e6c-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="63e6c-270">Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais**  >  **sensores**de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="63e6c-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores para orientação" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="63e6c-272">**Sensores** para orientação</span><span class="sxs-lookup"><span data-stu-id="63e6c-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="63e6c-273">Abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="63e6c-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="63e6c-274">Selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="63e6c-274">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="63e6c-275">Digite `Sensors` e escolha **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores para orientação" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="63e6c-277">**Mostrar sensores** para orientação</span><span class="sxs-lookup"><span data-stu-id="63e6c-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="63e6c-278">No painel **sensores** , você pode selecionar uma orientação predefinida no menu suspenso **orientação** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="63e6c-279">Para inserir sua própria orientação, escolha **orientação personalizada**e insira seus próprios valores [alfa][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta]e [gama][MDNDeviceOrientaitonGamma] .</span><span class="sxs-lookup"><span data-stu-id="63e6c-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Opções de orientação no painel sensores" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="63e6c-281">Opções de **orientação** no painel **sensores**</span><span class="sxs-lookup"><span data-stu-id="63e6c-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="63e6c-282">Definir cadeia de caracteres do agente do usuário</span><span class="sxs-lookup"><span data-stu-id="63e6c-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="63e6c-283">Se sua página depende da cadeia de caracteres do agente do usuário de um dispositivo móvel para renderizar corretamente, use o painel de **condições de rede** para fornecer diferentes cadeias de agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="63e6c-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="63e6c-284">Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais ferramentas**  >  **condições de rede**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrada de condições de rede no menu mais ferramentas" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="63e6c-286">Entrada de **condições de rede** no menu **mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="63e6c-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="63e6c-287">Abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="63e6c-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="63e6c-288">Selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="63e6c-288">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="63e6c-289">Digite `Network conditions` e escolha **Mostrar condições de rede**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Mostrar condições de rede" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="63e6c-291">Mostrar condições de rede</span><span class="sxs-lookup"><span data-stu-id="63e6c-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="63e6c-292">Ao lado de **agente do usuário**, desmarque a caixa de seleção **selecionar automaticamente** .</span><span class="sxs-lookup"><span data-stu-id="63e6c-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="63e6c-293">Em seguida, selecione **personalizado...** para selecionar em uma lista de cadeias de caracteres de agente do usuário predefinidas.</span><span class="sxs-lookup"><span data-stu-id="63e6c-293">Then, select **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="63e6c-294">Para inserir sua cadeia de caracteres de agente do usuário, insira a cadeia de caracteres em **digite um agente de usuário personalizado**.</span><span class="sxs-lookup"><span data-stu-id="63e6c-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Definir a cadeia de caracteres do agente do usuário como Microsoft Edge no macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="63e6c-296">Definir a cadeia de caracteres do agente do usuário como Microsoft Edge no macOS</span><span class="sxs-lookup"><span data-stu-id="63e6c-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <span data-ttu-id="63e6c-297">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63e6c-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "comece a usar dispositivos Android de depuração remota | Documentos da Microsoft "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. alfa | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. gama | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordem de aproximação-primeira ordem-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="63e6c-305">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="63e6c-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63e6c-306">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="63e6c-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="63e6c-308">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63e6c-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
