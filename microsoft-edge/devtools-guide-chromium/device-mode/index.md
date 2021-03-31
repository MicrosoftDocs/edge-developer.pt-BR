---
description: Use dispositivos virtuais no Microsoft Edge para criar sites móveis primeiro.
title: Emular dispositivos móveis no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, emulação, dispositivo, simulação, celular
ms.openlocfilehash: bb081ddd5f773e5e9ae6a1b83b5fcb13408df6cb
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439448"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="8dea2-104">Emular dispositivos móveis no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8dea2-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="8dea2-105">Use **a emulação de dispositivo** para aproximar a aparência e a resposta da sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="8dea2-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="8dea2-106">O Microsoft Edge DevTools fornece uma coleção de recursos para ajudá-lo a emular dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="8dea2-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="8dea2-107">A coleção inclui os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="8dea2-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="8dea2-108">Simular um viewport móvel</span><span class="sxs-lookup"><span data-stu-id="8dea2-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="8dea2-109">Acelerar a rede</span><span class="sxs-lookup"><span data-stu-id="8dea2-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="8dea2-110">Acelerar a CPU</span><span class="sxs-lookup"><span data-stu-id="8dea2-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="8dea2-111">Simular localização geográfica</span><span class="sxs-lookup"><span data-stu-id="8dea2-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="8dea2-112">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="8dea2-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="8dea2-113">Definir a cadeia de caracteres do agente do usuário</span><span class="sxs-lookup"><span data-stu-id="8dea2-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <a name="limitations"></a><span data-ttu-id="8dea2-114">Limitações</span><span class="sxs-lookup"><span data-stu-id="8dea2-114">Limitations</span></span>  

<span data-ttu-id="8dea2-115">**A emulação de dispositivo** [é][WikiApproximation] uma aproximação de primeira ordem da aparência da sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="8dea2-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="8dea2-116">**A emulação de dispositivo** não realmente executar seu código em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="8dea2-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="8dea2-117">Em vez disso, você simula a experiência do usuário móvel do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8dea2-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="8dea2-118">Alguns aspectos de dispositivos móveis nunca são emulados no DevTools.</span><span class="sxs-lookup"><span data-stu-id="8dea2-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="8dea2-119">Por exemplo, a arquitetura das CPUs móveis é diferente da arquitetura de CPUs de laptop ou desktop.</span><span class="sxs-lookup"><span data-stu-id="8dea2-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="8dea2-120">Quando estiver em dúvida, sua melhor opção é realmente executar sua página em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="8dea2-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="8dea2-121">Use [Depuração Remota][DevToolsRemoteDebugging] para interagir com o código de uma página do computador enquanto sua página é realmente executado em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="8dea2-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="8dea2-122">Você pode exibir, alterar, depurar, perfil ou todos os quatro enquanto interage com o código.</span><span class="sxs-lookup"><span data-stu-id="8dea2-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="8dea2-123">Seu computador pode ser um bloco de anotações ou computador da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8dea2-123">Your machine may be a notebook or desktop computer.</span></span>  

## <a name="simulate-a-mobile-viewport"></a><span data-ttu-id="8dea2-124">Simular um viewport móvel</span><span class="sxs-lookup"><span data-stu-id="8dea2-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="8dea2-125">Escolha **Alternar** a emulação de dispositivo \( Toggle Device Toolbar \) ou escolha Personalizar e controlar ![ ](../media/toggle-device-toolbar-dark-icon.msft.png) **DevTools** \( `...` \) emulação  de dispositivo > para abrir a interface do usuário que permite simular um modo de exibição móvel.</span><span class="sxs-lookup"><span data-stu-id="8dea2-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar](../media/toggle-device-toolbar-dark-icon.msft.png)\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="8dea2-127">A barra de ferramentas de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="8dea2-128">Por padrão, a Barra de Ferramentas de Dispositivo é aberta no Modo de Exibição Responsivo.</span><span class="sxs-lookup"><span data-stu-id="8dea2-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <a name="responsive-viewport-mode"></a><span data-ttu-id="8dea2-129">Modo de exibição responsivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="8dea2-130">Para testar rapidamente a aparência da sua página em vários tamanhos de tela, arraste as alças para ressizer o viewport para suas dimensões necessárias.</span><span class="sxs-lookup"><span data-stu-id="8dea2-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="8dea2-131">Você também pode inserir valores específicos nas caixas de largura e altura.</span><span class="sxs-lookup"><span data-stu-id="8dea2-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="8dea2-132">Na figura a seguir, a largura é definida como `626` e a altura é definida como `516` .</span><span class="sxs-lookup"><span data-stu-id="8dea2-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="As alças para alterar as dimensões do modo de exibição quando no Modo de Exibição Responsivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="8dea2-134">As alças para alterar as dimensões do modo de exibição quando no Modo de Exibição Responsivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <a name="show-media-queries"></a><span data-ttu-id="8dea2-135">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="8dea2-135">Show media queries</span></span>  

<span data-ttu-id="8dea2-136">Se você tiver definido consultas de mídia em sua página, pule para as dimensões do viewport onde essas consultas de mídia entrarão em vigor mostrando pontos de interrupção de consulta de mídia acima do seu viewport.</span><span class="sxs-lookup"><span data-stu-id="8dea2-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="8dea2-137">Escolha **Mais opções**Mostrar consultas de  >  **mídia**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas de mídia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="8dea2-139">Mostrar consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="8dea2-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="8dea2-140">Escolha um ponto de interrupção para alterar a largura do modo de exibição para que a consulta de mídia seja disparada.</span><span class="sxs-lookup"><span data-stu-id="8dea2-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Escolha um ponto de interrupção para alterar a largura do viewport" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="8dea2-142">Escolha um ponto de interrupção para alterar a largura do viewport</span><span class="sxs-lookup"><span data-stu-id="8dea2-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <a name="set-the-device-type"></a><span data-ttu-id="8dea2-143">Definir o tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-143">Set the device type</span></span>  

<span data-ttu-id="8dea2-144">Use a **lista Tipo de** Dispositivo para simular um dispositivo móvel ou dispositivo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8dea2-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="A lista Tipo de Dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="8dea2-146">A **lista Tipo de** Dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="8dea2-147">A tabela a seguir descreve as diferenças entre as opções de tipo de dispositivo disponível.</span><span class="sxs-lookup"><span data-stu-id="8dea2-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="8dea2-148">A coluna método Rendering refere-se a se o Microsoft Edge renderiza a página como um modo de exibição móvel ou de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8dea2-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="8dea2-149">A coluna Ícone do Cursor refere-se a que tipo de cursor é exibido quando você passar o mouse na página.</span><span class="sxs-lookup"><span data-stu-id="8dea2-149">The Cursor icon column refers to what type of cursor is displayed when you hover on the page.</span></span>  <span data-ttu-id="8dea2-150">A coluna Eventos disparados refere-se a se a página dispara ou ocorre `touch` `click` quando você interage com a página.</span><span class="sxs-lookup"><span data-stu-id="8dea2-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="8dea2-151">Opção</span><span class="sxs-lookup"><span data-stu-id="8dea2-151">Option</span></span> | <span data-ttu-id="8dea2-152">Método Rendering</span><span class="sxs-lookup"><span data-stu-id="8dea2-152">Rendering method</span></span> | <span data-ttu-id="8dea2-153">Ícone do cursor</span><span class="sxs-lookup"><span data-stu-id="8dea2-153">Cursor icon</span></span> | <span data-ttu-id="8dea2-154">Eventos disparados</span><span class="sxs-lookup"><span data-stu-id="8dea2-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="8dea2-155">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="8dea2-155">Mobile</span></span> | <span data-ttu-id="8dea2-156">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="8dea2-156">Mobile</span></span> | <span data-ttu-id="8dea2-157">Circle</span><span class="sxs-lookup"><span data-stu-id="8dea2-157">Circle</span></span> | <span data-ttu-id="8dea2-158">touch</span><span class="sxs-lookup"><span data-stu-id="8dea2-158">touch</span></span> |  
| <span data-ttu-id="8dea2-159">Mobile \(no touch\)</span><span class="sxs-lookup"><span data-stu-id="8dea2-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="8dea2-160">Dispositivos móveis</span><span class="sxs-lookup"><span data-stu-id="8dea2-160">Mobile</span></span> | <span data-ttu-id="8dea2-161">Normal</span><span class="sxs-lookup"><span data-stu-id="8dea2-161">Normal</span></span> | <span data-ttu-id="8dea2-162"> escolha </span><span class="sxs-lookup"><span data-stu-id="8dea2-162">choose</span></span> |  
| <span data-ttu-id="8dea2-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="8dea2-163">Desktop</span></span> | <span data-ttu-id="8dea2-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="8dea2-164">Desktop</span></span> | <span data-ttu-id="8dea2-165">Normal</span><span class="sxs-lookup"><span data-stu-id="8dea2-165">Normal</span></span> | <span data-ttu-id="8dea2-166"> escolha </span><span class="sxs-lookup"><span data-stu-id="8dea2-166">choose</span></span> |  
| <span data-ttu-id="8dea2-167">Área de trabalho \(touch\)</span><span class="sxs-lookup"><span data-stu-id="8dea2-167">Desktop \(touch\)</span></span> | <span data-ttu-id="8dea2-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="8dea2-168">Desktop</span></span> | <span data-ttu-id="8dea2-169">Circle</span><span class="sxs-lookup"><span data-stu-id="8dea2-169">Circle</span></span> | <span data-ttu-id="8dea2-170">touch</span><span class="sxs-lookup"><span data-stu-id="8dea2-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="8dea2-171">Se a **lista Tipo de** Dispositivo não for exibida, escolha **Mais**opções Adicionar tipo  >  **de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <a name="mobile-device-viewport-mode"></a><span data-ttu-id="8dea2-172">Modo de exibição de dispositivo móvel</span><span class="sxs-lookup"><span data-stu-id="8dea2-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="8dea2-173">Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na **lista Dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="A lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="8dea2-175">A **lista de** dispositivos</span><span class="sxs-lookup"><span data-stu-id="8dea2-175">The **Device** list</span></span>  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a><span data-ttu-id="8dea2-176">Girar o viewport para orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="8dea2-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="8dea2-177">Teste sua página da Web na orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="8dea2-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="8dea2-178">Para girar o viewport para orientação paisagem, escolha **Girar** \( ![ Girar ](../media/rotate-dark-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="8dea2-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Página exibida na orientação paisagem" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="8dea2-180">Página exibida na orientação paisagem</span><span class="sxs-lookup"><span data-stu-id="8dea2-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="8dea2-181">O **botão Girar** desaparecerá se a barra de ferramentas do **dispositivo** for estreita.</span><span class="sxs-lookup"><span data-stu-id="8dea2-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="8dea2-183">A **barra de ferramentas de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="8dea2-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="8dea2-184">Para obter mais informações, navegue até [Definir orientação](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="8dea2-184">For more information, navigate to [Set orientation](#set-orientation).</span></span>  

#### <a name="show-device-frame"></a><span data-ttu-id="8dea2-185">Mostrar quadro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-185">Show device frame</span></span>  

<span data-ttu-id="8dea2-186">Exibe o quadro de dispositivo físico ao redor do visor quando você simula as dimensões de um dispositivo móvel específico, como um iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="8dea2-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="8dea2-187">Abra **mais opções**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="8dea2-188">Escolha **Mostrar quadro do dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="8dea2-189">Se um quadro de dispositivo para um determinado dispositivo não for exibido, isso significa que o DevTools não tem arte para a opção.</span><span class="sxs-lookup"><span data-stu-id="8dea2-189">If a device frame for a particular device is not displayed, it means that DevTools does not have art for the option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar quadro do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="8dea2-191">Mostrar quadro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="O quadro do dispositivo para o iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="8dea2-193">O quadro do dispositivo para o iPhone 6</span><span class="sxs-lookup"><span data-stu-id="8dea2-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a><span data-ttu-id="8dea2-194">Adicionar um dispositivo móvel personalizado</span><span class="sxs-lookup"><span data-stu-id="8dea2-194">Add a custom mobile device</span></span>  

<span data-ttu-id="8dea2-195">Se a opção de dispositivo móvel de que você precisa não estiver incluída na lista padrão, você poderá adicionar um dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="8dea2-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="8dea2-196">Para adicionar um dispositivo personalizado, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8dea2-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="8dea2-197">Escolha a **lista De** dispositivos > **Editar**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Escolha Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="8dea2-199">Escolha **Editar**</span><span class="sxs-lookup"><span data-stu-id="8dea2-199">Choose **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8dea2-200">Escolha **Adicionar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="8dea2-201">Em **Dispositivos Emulados,** insira um nome de dispositivo, largura de tela e altura da tela para o dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="8dea2-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="8dea2-202">A [taxa de pixel do dispositivo,][MDNWindowDevicePixelRatio]a cadeia de [caracteres][MDNUserAgent]do agente do usuário e os campos de tipo [de](#set-the-device-type) dispositivo são opcionais.</span><span class="sxs-lookup"><span data-stu-id="8dea2-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="8dea2-203">O campo tipo de dispositivo padrão para **Mobile**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Criar um dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="8dea2-205">Criar um dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="8dea2-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <a name="show-rulers"></a><span data-ttu-id="8dea2-206">Mostrar réguas</span><span class="sxs-lookup"><span data-stu-id="8dea2-206">Show rulers</span></span>  

<span data-ttu-id="8dea2-207">Se você precisar medir dimensões de tela, poderá usar réguas para medir o tamanho da tela em pixels.</span><span class="sxs-lookup"><span data-stu-id="8dea2-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="8dea2-208">Escolha **Mais opções**Mostrar  >  **réguas** para exibir réguas acima e à esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="8dea2-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Item de menu para exibir réguas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="8dea2-210">Item de menu para exibir réguas</span><span class="sxs-lookup"><span data-stu-id="8dea2-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Réguas acima e à esquerda do viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="8dea2-212">Réguas acima e à esquerda do viewport</span><span class="sxs-lookup"><span data-stu-id="8dea2-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a><span data-ttu-id="8dea2-213">Ampliar o viewport</span><span class="sxs-lookup"><span data-stu-id="8dea2-213">Zoom the viewport</span></span>  

<span data-ttu-id="8dea2-214">Para testar a aparência da sua página em vários níveis de zoom, use a **lista Zoom** para ampliar ou diminuir o zoom.</span><span class="sxs-lookup"><span data-stu-id="8dea2-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="8dea2-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="8dea2-216">Zoom</span></span>**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a><span data-ttu-id="8dea2-217">Acelerar a rede e a CPU</span><span class="sxs-lookup"><span data-stu-id="8dea2-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="8dea2-218">Dispositivos móveis geralmente têm restrições de rede e CPU.</span><span class="sxs-lookup"><span data-stu-id="8dea2-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="8dea2-219">Certifique-se de testar a rapidez com que sua página é carregada e como ela responde em velocidades diferentes da Internet e da CPU.</span><span class="sxs-lookup"><span data-stu-id="8dea2-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="8dea2-220">Reduza a rede e a CPU.</span><span class="sxs-lookup"><span data-stu-id="8dea2-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="8dea2-221">Escolha **Lista de** aceleração e altere a predefinição para celular de camada **média** ou **celular low-end.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="8dea2-222">**O dispositivo móvel de** camada intermediária `fast 3G` simula e acelera sua CPU.</span><span class="sxs-lookup"><span data-stu-id="8dea2-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="8dea2-223">É quatro vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="8dea2-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="8dea2-224">**O celular de baixo** nível simula `slow 3G` e acelera sua CPU.</span><span class="sxs-lookup"><span data-stu-id="8dea2-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="8dea2-225">É seis vezes mais lento do que o normal.</span><span class="sxs-lookup"><span data-stu-id="8dea2-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="8dea2-226">Toda a throttling se baseia na funcionalidade normal do laptop ou da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8dea2-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="A lista De aceleração na barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="8dea2-228">A **lista De** aceleração na barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dea2-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8dea2-229">Se a **lista De limitação** estiver oculta, sua Barra de **Ferramentas de Dispositivo** será muito estreita.</span><span class="sxs-lookup"><span data-stu-id="8dea2-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="8dea2-230">Para acessar a **lista De aceleração,** aumente a largura da Barra **de Ferramentas de Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="8dea2-232">A **barra de ferramentas de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="8dea2-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a><span data-ttu-id="8dea2-233">Acelerar somente a CPU</span><span class="sxs-lookup"><span data-stu-id="8dea2-233">Throttle the CPU only</span></span>  

<span data-ttu-id="8dea2-234">Para acelerar apenas a CPU e não a rede, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8dea2-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="8dea2-235">Escolha o **painel Desempenho** e escolha **Configurações de** Captura \( ![ Configurações de Captura ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="8dea2-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>
1.  <span data-ttu-id="8dea2-236">Escolha **a lentidão**da CPU  >  **4x** ou **6x de lentidão**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="A lista de CPU no painel Desempenho" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="8dea2-238">A **lista de CPU** no painel **Desempenho**</span><span class="sxs-lookup"><span data-stu-id="8dea2-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a><span data-ttu-id="8dea2-239">Apenas acelerar a rede</span><span class="sxs-lookup"><span data-stu-id="8dea2-239">Throttle the network only</span></span>  

<span data-ttu-id="8dea2-240">Para acelerar apenas a rede, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8dea2-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="8dea2-241">Escolha a **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-241">Choose the **Network** tool.</span></span>
1.  <span data-ttu-id="8dea2-242">Escolha **Online**  >  **Fast 3G** ou Slow **3G**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="A lista De aceleração no painel Rede" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="8dea2-244">A **lista De** aceleração no painel Rede</span><span class="sxs-lookup"><span data-stu-id="8dea2-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="8dea2-245">Ou selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\)  `3G`   para abrir o Menu de Comando , digite e escolha Habilitar a desaceleração 3G rápida ou Habilitar a desaceleração lenta do 3G .</span><span class="sxs-lookup"><span data-stu-id="8dea2-245">Or select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="O Menu De comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="8dea2-247">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="8dea2-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="8dea2-248">Você também pode definir a throttling de rede a partir do **painel Desempenho.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="8dea2-249">Escolha **Configurações de** Captura \( Configurações de Captura \) e escolha a lista Rede e altere a ![ ](../media/capture-settings-icon.msft.png) predefinição para Fast **3G** ou **Slow 3G**. </span><span class="sxs-lookup"><span data-stu-id="8dea2-249">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Definir a throttling de rede do painel Desempenho" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="8dea2-251">Definir a throttling de rede do **painel Desempenho**</span><span class="sxs-lookup"><span data-stu-id="8dea2-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <a name="override-geolocation"></a><span data-ttu-id="8dea2-252">Substituir geolocalização</span><span class="sxs-lookup"><span data-stu-id="8dea2-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8dea2-253">Se sua página depender das informações de localização geográfica de um dispositivo móvel para renderizar corretamente, forneça diferentes localizações geográficas usando a interface do usuário de sobrelocação geográfica.</span><span class="sxs-lookup"><span data-stu-id="8dea2-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="8dea2-254">Escolha **Personalizar e controlar o DevTools** \( `...` \) > Mais sensores de   >  **ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores para localização geográfica" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="8dea2-256">**Sensores** para localização geográfica</span><span class="sxs-lookup"><span data-stu-id="8dea2-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="8dea2-257">Abra o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="8dea2-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="8dea2-258">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="8dea2-258">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="8dea2-259">Digite `Sensors` e escolha Mostrar **Sensores**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar Sensores para localização geográfica" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="8dea2-261">**Mostrar Sensores** para localização geográfica</span><span class="sxs-lookup"><span data-stu-id="8dea2-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8dea2-262">No painel **Sensores,** você pode selecionar um dos locais predefinidos incluídos no DevTools usando o **menu** suspenso Local.</span><span class="sxs-lookup"><span data-stu-id="8dea2-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="8dea2-263">Para inserir um local personalizado, escolha **Outro...**</span><span class="sxs-lookup"><span data-stu-id="8dea2-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="8dea2-264">e insira as coordenadas de sua localização personalizada.</span><span class="sxs-lookup"><span data-stu-id="8dea2-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="8dea2-265">Para testar sua página em um estado de erro quando as informações de local não estão disponíveis, escolha **Local indisponível**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Painel sensores com um local predefinido selecionado" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="8dea2-267">**Painel** de sensores com um local predefinido selecionado.</span><span class="sxs-lookup"><span data-stu-id="8dea2-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <a name="set-orientation"></a><span data-ttu-id="8dea2-268">Definir orientação</span><span class="sxs-lookup"><span data-stu-id="8dea2-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8dea2-269">Se sua página depender das informações de orientação de um dispositivo móvel para renderizar corretamente, abra a interface do usuário de orientação.</span><span class="sxs-lookup"><span data-stu-id="8dea2-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="8dea2-270">Escolha **Personalizar e controlar o DevTools** \( `...` \) > Mais sensores de   >  **ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores para orientação" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="8dea2-272">**Sensores** para orientação</span><span class="sxs-lookup"><span data-stu-id="8dea2-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="8dea2-273">Abra o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="8dea2-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="8dea2-274">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="8dea2-274">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="8dea2-275">Digite `Sensors` e escolha Mostrar **Sensores**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar Sensores para orientação" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="8dea2-277">**Mostrar Sensores** para orientação</span><span class="sxs-lookup"><span data-stu-id="8dea2-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8dea2-278">No painel **Sensores,** você pode selecionar uma orientação predefinida no menu suspenso **Orientação.**</span><span class="sxs-lookup"><span data-stu-id="8dea2-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="8dea2-279">Para inserir sua própria orientação, escolha **Orientação personalizada**e insira seus próprios valores [alfa,][MDNDeviceOrientaitonAlpha] [beta][MDNDeviceOrientaitonBeta]e [gama.][MDNDeviceOrientaitonGamma]</span><span class="sxs-lookup"><span data-stu-id="8dea2-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Opções de orientação no painel Sensores" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="8dea2-281">**Opções** de orientação no painel **Sensores**</span><span class="sxs-lookup"><span data-stu-id="8dea2-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <a name="set-user-agent-string"></a><span data-ttu-id="8dea2-282">Definir cadeia de caracteres de agente do usuário</span><span class="sxs-lookup"><span data-stu-id="8dea2-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8dea2-283">Se sua página depender da cadeia de caracteres do  agente do usuário de um dispositivo móvel para renderizar corretamente, use o painel Condições de rede para fornecer cadeias de caracteres de agente de usuário diferentes.</span><span class="sxs-lookup"><span data-stu-id="8dea2-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="8dea2-284">Escolha **Personalizar e controlar o DevTools** \( `...` \) > Mais **ferramentas**Condições  >  **de rede**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrada de condições de rede no menu Mais ferramentas" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="8dea2-286">**Entrada de condições** de rede no menu **Mais ferramentas**</span><span class="sxs-lookup"><span data-stu-id="8dea2-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="8dea2-287">Abra o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="8dea2-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="8dea2-288">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="8dea2-288">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="8dea2-289">Digite `Network conditions` e escolha Mostrar condições de **rede**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Mostrar condições de rede" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="8dea2-291">Mostrar condições de rede</span><span class="sxs-lookup"><span data-stu-id="8dea2-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8dea2-292">Ao lado **de Agente de usuário,** desempure a **caixa de seleção Selecionar** automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8dea2-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="8dea2-293">Em seguida, escolha **Personalizado...** para selecionar em uma lista de cadeias de caracteres de agente de usuário predefinidos.</span><span class="sxs-lookup"><span data-stu-id="8dea2-293">Then, choose **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="8dea2-294">Para inserir sua própria cadeia de caracteres de agente de usuário, insira a cadeia de caracteres em **Enter a custom user agent**.</span><span class="sxs-lookup"><span data-stu-id="8dea2-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Definir a cadeia de caracteres de agente do usuário como Microsoft Edge no macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="8dea2-296">Definir a cadeia de caracteres de agente do usuário como Microsoft Edge no macOS</span><span class="sxs-lookup"><span data-stu-id="8dea2-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8dea2-297">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8dea2-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "User Agent | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordem de Aproximação - Primeira Ordem - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="8dea2-305">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8dea2-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8dea2-306">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8dea2-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8dea2-308">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8dea2-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
