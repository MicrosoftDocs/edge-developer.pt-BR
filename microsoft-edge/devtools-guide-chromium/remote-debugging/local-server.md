---
description: Hospede um site em um servidor Web de máquina de desenvolvimento e acesse o conteúdo de um dispositivo Android.
title: Acessar servidores locais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 51ef0d951d587d310b6474698924d9f87cf68607
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461259"
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
# <a name="access-local-servers"></a><span data-ttu-id="e63ec-104">Acessar servidores locais</span><span class="sxs-lookup"><span data-stu-id="e63ec-104">Access local servers</span></span>  

<span data-ttu-id="e63ec-105">Hospede um site em um servidor Web de máquina de desenvolvimento e, em seguida, acesse o conteúdo de um dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="e63ec-106">Com um cabo USB e o Microsoft Edge DevTools, execute um site de uma máquina de desenvolvimento e, em seguida, veja o site em um dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <a name="summary"></a><span data-ttu-id="e63ec-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="e63ec-107">Summary</span></span>  

*   <span data-ttu-id="e63ec-108">O encaminhamento de porta permite que você veja o conteúdo hospedado pelo servidor Web em execução em seu computador de desenvolvimento em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="e63ec-109">Se o servidor Web estiver usando um domínio personalizado, de configurar seu dispositivo Android para acessar o conteúdo nesse domínio com mapeamento de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="e63ec-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <a name="set-up-port-forwarding"></a><span data-ttu-id="e63ec-110">Configurar o encaminhamento de porta</span><span class="sxs-lookup"><span data-stu-id="e63ec-110">Set up port forwarding</span></span>  

<span data-ttu-id="e63ec-111">O encaminhamento de porta permite que seu dispositivo Android acesse o conteúdo que está sendo hospedado no servidor Web em execução em sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="e63ec-112">O encaminhamento de porta funciona criando uma porta TCP de escuta em seu dispositivo Android que mapeia para uma porta TCP em sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="e63ec-113">O tráfego entre as portas percorre a conexão USB entre seu dispositivo Android e a máquina de desenvolvimento, para que a conexão não dependa da configuração da rede.</span><span class="sxs-lookup"><span data-stu-id="e63ec-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="e63ec-114">Para habilitar o encaminhamento de porta:</span><span class="sxs-lookup"><span data-stu-id="e63ec-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="e63ec-115">Configurar a [depuração remota][RemoteDebuggingGettingStarted] entre sua máquina de desenvolvimento e seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="e63ec-116">Quando terminar, seu dispositivo Android deverá ser exibido no menu à esquerda da caixa de diálogo **Inspecionar Dispositivos** e um **indicador** de status conectado.</span><span class="sxs-lookup"><span data-stu-id="e63ec-116">When you are finished, your Android device should be displayed in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="e63ec-117">Na caixa **de diálogo Inspecionar Dispositivos** no DevTools, habilita **o encaminhamento de porta**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="e63ec-118">Escolha **Adicionar regra**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Adicionar uma regra de encaminhamento de porta" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="e63ec-120">Adicionar uma regra de encaminhamento de porta</span><span class="sxs-lookup"><span data-stu-id="e63ec-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e63ec-121">Na caixa **de texto porta** de dispositivo à esquerda, insira o número da porta a partir do qual você deseja acessar o site em seu dispositivo `localhost` Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="e63ec-122">Por exemplo, se você quisesse acessar o site a partir de `localhost:5000` enter `5000` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="e63ec-123">Na caixa **de texto** Endereço local à direita, insira o endereço IP ou o nome do host no qual seu site está hospedado no servidor Web em execução em sua máquina de desenvolvimento, seguido pelo número da porta.</span><span class="sxs-lookup"><span data-stu-id="e63ec-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="e63ec-124">Por exemplo, se seu site estiver sendo executado na `localhost:7331` entrada `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="e63ec-125">Escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="e63ec-126">O encaminhamento de porta agora está definido.</span><span class="sxs-lookup"><span data-stu-id="e63ec-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="e63ec-127">Examine o indicador de status da porta para frente na guia em seu dispositivo na caixa **de diálogo Inspecionar Dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="e63ec-127">Review the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Status de encaminhamento de porta" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="e63ec-129">Status de encaminhamento de porta</span><span class="sxs-lookup"><span data-stu-id="e63ec-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="e63ec-130">Para exibir o conteúdo, abra o Microsoft Edge em seu dispositivo Android e vá para a porta especificada `localhost` no campo Porta **do** dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e63ec-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="e63ec-131">Por exemplo, se você entrou `5000` no campo, visite `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <a name="map-to-custom-local-domains"></a><span data-ttu-id="e63ec-132">Mapear para domínios locais personalizados</span><span class="sxs-lookup"><span data-stu-id="e63ec-132">Map to custom local domains</span></span>  

<span data-ttu-id="e63ec-133">O mapeamento de domínio personalizado permite que você veja o conteúdo em um dispositivo Android de um servidor Web em sua máquina de desenvolvimento que está usando um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="e63ec-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="e63ec-134">Por exemplo, suponha que seu site use uma biblioteca JavaScript de terceiros que só funciona no domínio `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="e63ec-135">Portanto, você cria uma entrada em seu arquivo em sua máquina de desenvolvimento para mapear esse `hosts` domínio para `localhost` \(por exemplo, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="e63ec-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="e63ec-136">Depois de configurar o mapeamento de domínio personalizado e o encaminhamento de porta, exibir o site em seu dispositivo Android na URL `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <a name="set-up-port-forwarding-to-proxy-server"></a><span data-ttu-id="e63ec-137">Configurar o encaminhamento de porta para o servidor proxy</span><span class="sxs-lookup"><span data-stu-id="e63ec-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="e63ec-138">Para mapear um domínio personalizado, você deve executar um servidor proxy em sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="e63ec-139">Exemplos de servidores proxy são [Carlos][CharlesWebDebuggingProxy], [Lula][SquidOptimisingWebDelivery]e [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="e63ec-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="e63ec-140">Para configurar o encaminhamento de porta para um proxy:</span><span class="sxs-lookup"><span data-stu-id="e63ec-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="e63ec-141">Execute o servidor proxy e grave a porta que ele está usando.</span><span class="sxs-lookup"><span data-stu-id="e63ec-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e63ec-142">O servidor proxy e seu servidor Web devem ser executados em portas diferentes.</span><span class="sxs-lookup"><span data-stu-id="e63ec-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="e63ec-143">Configurar o [encaminhamento de porta para](#set-up-port-forwarding) seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="e63ec-144">Para o **campo de endereço local,** digite seguido pela porta em `localhost:` que o servidor proxy está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e63ec-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="e63ec-145">Por exemplo, se estiver sendo executado na `8000` porta, navegue até `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="e63ec-146">No campo **porta do** dispositivo, insira o número que você deseja que seu dispositivo Android ouça, como `3333` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <a name="configure-proxy-settings-on-your-device"></a><span data-ttu-id="e63ec-147">Configurar configurações de proxy em seu dispositivo</span><span class="sxs-lookup"><span data-stu-id="e63ec-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="e63ec-148">Em seguida, você precisa configurar seu dispositivo Android para se comunicar com o servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="e63ec-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="e63ec-149">Em seu dispositivo Android, navegue até **Configurações**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-149">On your Android device, navigate to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="e63ec-150">Pressione o nome da rede à qual você está conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e63ec-151">As configurações de proxy se aplicam por rede.</span><span class="sxs-lookup"><span data-stu-id="e63ec-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="e63ec-152">Escolha **Modificar rede**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="e63ec-153">Escolha **Opções avançadas**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="e63ec-154">As configurações de proxy são exibidas.</span><span class="sxs-lookup"><span data-stu-id="e63ec-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="e63ec-155">Escolha o **menu Proxy** e escolha **Manual**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-155">Choose the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="e63ec-156">Para o **campo Nome do host proxy,** digite `localhost` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="e63ec-157">Para o **campo porta proxy,** insira o número da porta que você inspeu para a **porta do** dispositivo na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="e63ec-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="e63ec-158">Escolha **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e63ec-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="e63ec-159">Com essas configurações, seu dispositivo encaminha todas as suas solicitações para o proxy em seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="e63ec-160">O proxy faz solicitações em nome do dispositivo, portanto, as solicitações para o domínio local personalizado são resolvidas corretamente.</span><span class="sxs-lookup"><span data-stu-id="e63ec-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="e63ec-161">Agora, acesse domínios personalizados em seu dispositivo Android exatamente como na máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="e63ec-162">Se o servidor Web estiver sendo executado em uma porta não padrão, lembre-se de especificar a porta ao solicitar o conteúdo do dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="e63ec-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="e63ec-163">Por exemplo, se seu servidor Web estiver usando o domínio personalizado na porta , quando você exibir o site do dispositivo Android, você deverá `microsoft-edge.devtools` `7331` usar a URL `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="e63ec-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="e63ec-164">Para retomar a navegação normal, lembre-se de reverter as configurações de proxy em seu dispositivo Android depois de desconectar da máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="e63ec-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e63ec-165">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e63ec-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de Depuração da Web de Carlos"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "lula : Otimizando a Entrega da Web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler - Proxy de Depuração da Web Gratuito"  

> [!NOTE]
> <span data-ttu-id="e63ec-170">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e63ec-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e63ec-171">A página original [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="e63ec-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e63ec-173">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e63ec-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
