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
# <a name="access-local-servers"></a>Acessar servidores locais  

Hospede um site em um servidor Web de máquina de desenvolvimento e, em seguida, acesse o conteúdo de um dispositivo Android.  

Com um cabo USB e o Microsoft Edge DevTools, execute um site de uma máquina de desenvolvimento e, em seguida, veja o site em um dispositivo Android.  

### <a name="summary"></a>Resumo  

*   O encaminhamento de porta permite que você veja o conteúdo hospedado pelo servidor Web em execução em seu computador de desenvolvimento em seu dispositivo Android.  
*   Se o servidor Web estiver usando um domínio personalizado, de configurar seu dispositivo Android para acessar o conteúdo nesse domínio com mapeamento de domínio personalizado.  

## <a name="set-up-port-forwarding"></a>Configurar o encaminhamento de porta  

O encaminhamento de porta permite que seu dispositivo Android acesse o conteúdo que está sendo hospedado no servidor Web em execução em sua máquina de desenvolvimento.  O encaminhamento de porta funciona criando uma porta TCP de escuta em seu dispositivo Android que mapeia para uma porta TCP em sua máquina de desenvolvimento.  O tráfego entre as portas percorre a conexão USB entre seu dispositivo Android e a máquina de desenvolvimento, para que a conexão não dependa da configuração da rede.  

Para habilitar o encaminhamento de porta:  

1.  Configurar a [depuração remota][RemoteDebuggingGettingStarted] entre sua máquina de desenvolvimento e seu dispositivo Android.  Quando terminar, seu dispositivo Android deverá ser exibido no menu à esquerda da caixa de diálogo **Inspecionar Dispositivos** e um **indicador** de status conectado.  
1.  Na caixa **de diálogo Inspecionar Dispositivos** no DevTools, habilita **o encaminhamento de porta**.  
1.  Escolha **Adicionar regra**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Adicionar uma regra de encaminhamento de porta" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Adicionar uma regra de encaminhamento de porta  
    :::image-end:::  
    
1.  Na caixa **de texto porta** de dispositivo à esquerda, insira o número da porta a partir do qual você deseja acessar o site em seu dispositivo `localhost` Android.  Por exemplo, se você quisesse acessar o site a partir de `localhost:5000` enter `5000` .  
1.  Na caixa **de texto** Endereço local à direita, insira o endereço IP ou o nome do host no qual seu site está hospedado no servidor Web em execução em sua máquina de desenvolvimento, seguido pelo número da porta.  Por exemplo, se seu site estiver sendo executado na `localhost:7331` entrada `localhost:7331` .  
1.  Escolha **Adicionar**.  
    
O encaminhamento de porta agora está definido.  Examine o indicador de status da porta para frente na guia em seu dispositivo na caixa **de diálogo Inspecionar Dispositivos.**  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Status de encaminhamento de porta" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Status de encaminhamento de porta  
:::image-end:::  

Para exibir o conteúdo, abra o Microsoft Edge em seu dispositivo Android e vá para a porta especificada `localhost` no campo Porta **do** dispositivo.  Por exemplo, se você entrou `5000` no campo, visite `localhost:5000` .  

## <a name="map-to-custom-local-domains"></a>Mapear para domínios locais personalizados  

O mapeamento de domínio personalizado permite que você veja o conteúdo em um dispositivo Android de um servidor Web em sua máquina de desenvolvimento que está usando um domínio personalizado.  

Por exemplo, suponha que seu site use uma biblioteca JavaScript de terceiros que só funciona no domínio `microsoft-edge.devtools` .  Portanto, você cria uma entrada em seu arquivo em sua máquina de desenvolvimento para mapear esse `hosts` domínio para `localhost` \(por exemplo, `127.0.0.1 microsoft-edge.devtools` \).  Depois de configurar o mapeamento de domínio personalizado e o encaminhamento de porta, exibir o site em seu dispositivo Android na URL `microsoft-edge.devtools` .  

### <a name="set-up-port-forwarding-to-proxy-server"></a>Configurar o encaminhamento de porta para o servidor proxy  

Para mapear um domínio personalizado, você deve executar um servidor proxy em sua máquina de desenvolvimento.  Exemplos de servidores proxy são [Carlos][CharlesWebDebuggingProxy], [Lula][SquidOptimisingWebDelivery]e [Fiddler][FiddlerWebDebuggingProxy].  

Para configurar o encaminhamento de porta para um proxy:  

1.  Execute o servidor proxy e grave a porta que ele está usando.  
    
    > [!NOTE]
    > O servidor proxy e seu servidor Web devem ser executados em portas diferentes.  
    
1.  Configurar o [encaminhamento de porta para](#set-up-port-forwarding) seu dispositivo Android.  Para o **campo de endereço local,** digite seguido pela porta em `localhost:` que o servidor proxy está sendo executado.  Por exemplo, se estiver sendo executado na `8000` porta, navegue até `localhost:8000` .  No campo **porta do** dispositivo, insira o número que você deseja que seu dispositivo Android ouça, como `3333` .  
    
### <a name="configure-proxy-settings-on-your-device"></a>Configurar configurações de proxy em seu dispositivo  

Em seguida, você precisa configurar seu dispositivo Android para se comunicar com o servidor proxy.  

1.  Em seu dispositivo Android, navegue até **Configurações**  >  **Wi-Fi**.  
1.  Pressione o nome da rede à qual você está conectado no momento.  
    
    > [!NOTE]
    > As configurações de proxy se aplicam por rede.  
    
1.  Escolha **Modificar rede**.  
1.  Escolha **Opções avançadas**.  As configurações de proxy são exibidas.  
1.  Escolha o **menu Proxy** e escolha **Manual**.  
1.  Para o **campo Nome do host proxy,** digite `localhost` .  
1.  Para o **campo porta proxy,** insira o número da porta que você inspeu para a **porta do** dispositivo na seção anterior.  
1.  Escolha **Salvar**.  
    
Com essas configurações, seu dispositivo encaminha todas as suas solicitações para o proxy em seu computador de desenvolvimento.  O proxy faz solicitações em nome do dispositivo, portanto, as solicitações para o domínio local personalizado são resolvidas corretamente.  

Agora, acesse domínios personalizados em seu dispositivo Android exatamente como na máquina de desenvolvimento.  

Se o servidor Web estiver sendo executado em uma porta não padrão, lembre-se de especificar a porta ao solicitar o conteúdo do dispositivo Android.  Por exemplo, se seu servidor Web estiver usando o domínio personalizado na porta , quando você exibir o site do dispositivo Android, você deverá `microsoft-edge.devtools` `7331` usar a URL `microsoft-edge.devtools:7331` .  

> [!TIP]
> Para retomar a navegação normal, lembre-se de reverter as configurações de proxy em seu dispositivo Android depois de desconectar da máquina de desenvolvimento.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de Depuração da Web de Carlos"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "lula : Otimizando a Entrega da Web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler - Proxy de Depuração da Web Gratuito"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
