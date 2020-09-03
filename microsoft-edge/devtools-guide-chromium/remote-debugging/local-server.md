---
description: Hospede um site em um servidor Web do computador de desenvolvimento e acesse o conteúdo de um dispositivo Android.
title: Acessar Servidores Locais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 373cd7ce5cd262bad9fa5460bb2187241246cd75
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993482"
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





# Acessar servidores locais   




Hospede um site em um servidor Web do computador de desenvolvimento e acesse o conteúdo de um dispositivo Android.  

Com um cabo USB e o Microsoft Edge DevTools, execute um site a partir de um computador de desenvolvimento e, em seguida, exiba o site em um dispositivo Android.  

### Resumo  

*   O encaminhamento de porta permite que você veja o conteúdo hospedado pelo servidor Web em execução em seu computador de desenvolvimento em seu dispositivo Android.  
*   Se seu servidor Web estiver usando um domínio personalizado, configure seu dispositivo Android para acessar o conteúdo nesse domínio com mapeamento de domínio personalizado.  

## Configurar o encaminhamento de porta   

O encaminhamento de porta permite que seu dispositivo Android acesse o conteúdo que está sendo hospedado no servidor Web em execução na máquina de desenvolvimento.  O encaminhamento de porta funciona criando uma porta TCP de escuta em seu dispositivo Android que mapeia para uma porta TCP em seu computador de desenvolvimento.  O tráfego entre as portas trafegam pela conexão USB entre seu dispositivo Android e seu computador de desenvolvimento, portanto, a conexão não depende da configuração da sua rede.  

Para habilitar o encaminhamento de porta:  

1.  Configure a [depuração remota][RemoteDebuggingGettingStarted] entre sua máquina de desenvolvimento e seu dispositivo Android.  Quando terminar, você verá seu dispositivo Android no menu à esquerda da caixa de diálogo **inspecionar dispositivos** e um indicador de status **conectado** .  
1.  Na caixa de diálogo **inspecionar dispositivos** no devtools, habilite o **encaminhamento de porta**.  
1.  Selecione **Adicionar regra**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Adicionando uma regra de encaminhamento de porta" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Adicionando uma regra de encaminhamento de porta  
    :::image-end:::  
    
1.  Na caixa de texto **porta do dispositivo** à esquerda, insira o `localhost` número da porta da qual você deseja poder acessar o site no seu dispositivo Android.  Por exemplo, se você quisesse acessar o site de `localhost:5000` Enter `5000` .  
1.  Na caixa de texto **local do endereço** à direita, digite o endereço IP ou o nome do host em que seu site está hospedado no servidor Web em execução na máquina de desenvolvimento, seguido do número da porta.  Por exemplo, se o seu site estiver sendo executado durante a `localhost:7331` entrada `localhost:7331` .  
1.  Selecione **Adicionar**.  
    
O encaminhamento de portas agora está configurado.  Consulte o indicador de status para que a porta encaminhe na guia do seu dispositivo na caixa de diálogo **inspecionar dispositivos** .  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Status de encaminhamento de porta" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Status de encaminhamento de porta  
:::image-end:::  

Para exibir o conteúdo, abra o Microsoft Edge no seu dispositivo Android e vá para a `localhost` porta que você especificou no campo **porta do dispositivo** .  Por exemplo, se você inseriu `5000` no campo, acesse `localhost:5000` .  

## Mapear para domínios locais personalizados   

O mapeamento de domínio personalizado permite exibir o conteúdo em um dispositivo Android de um servidor Web na máquina de desenvolvimento que está usando um domínio personalizado.  

Por exemplo, suponha que seu site usa uma biblioteca JavaScript de terceiros que só funciona no domínio `microsoft-edge.devtools` .  Portanto, você cria uma entrada em seu `hosts` arquivo em seu computador de desenvolvimento para mapear esse domínio para `localhost` \ (por exemplo, `127.0.0.1 microsoft-edge.devtools` \).  Depois de configurar o mapeamento de domínio personalizado e o encaminhamento de porta, exiba o site em seu dispositivo Android na URL `microsoft-edge.devtools` .  

### Configurar o encaminhamento de porta para o servidor proxy  

Para mapear um domínio personalizado, você deve executar um servidor proxy em seu computador de desenvolvimento.  Exemplos de servidores proxy são [Charles][CharlesWebDebuggingProxy], [Lula][SquidOptimisingWebDelivery]e [Fiddler][FiddlerWebDebuggingProxy].  

Para configurar o encaminhamento de porta para um proxy:  

1.  Execute o servidor proxy e grave a porta que ele está usando.  
    
    > [!NOTE]
    > O servidor proxy e o servidor Web devem ser executados em diferentes portas.  
    
1.  Configure o [encaminhamento de porta](#set-up-port-forwarding) para seu dispositivo Android.  Para o campo **endereço local** , insira `localhost:` seguido pela porta em que o servidor proxy está em execução.  Por exemplo, se estiver em execução na porta `8000` , acesse `localhost:8000` .  No campo **porta do dispositivo** , digite o número que você deseja que seu dispositivo Android Ouça, como `3333` .  
    
### Definir configurações de proxy em seu dispositivo  

Em seguida, você precisa configurar seu dispositivo Android para se comunicar com o servidor proxy.  

1.  Em seu dispositivo Android, vá para **configurações**  >  **Wi-Fi**.  
1.  Longo-pressione o nome da rede à qual você está conectado no momento.  
    
    > [!NOTE]
    > As configurações de proxy se aplicam por rede.  
    
1.  Selecione **Modificar rede**.  
1.  Selecione **Opções avançadas**.  As configurações de proxy são exibidas.  
1.  Selecione o menu **proxy** e selecione **manual**.  
1.  Para o campo **hostname do proxy** , insira `localhost` .  
1.  Para o campo **porta de proxy** , insira o número da porta que você inseriu para a porta do **dispositivo** na seção anterior.  
1.  Selecione **Salvar**.  
    
Com essas configurações, seu dispositivo encaminha todas as suas solicitações para o proxy no seu computador de desenvolvimento.  O proxy faz solicitações em nome do seu dispositivo, portanto, as solicitações para o seu domínio local personalizado são corretamente resolvidas.  

Acesse agora os domínios personalizados em seu dispositivo Android, exatamente como no computador de desenvolvimento.  

Se seu servidor Web estiver fora de uma porta não padrão, lembre-se de especificar a porta ao solicitar o conteúdo do seu dispositivo Android.  Por exemplo, se seu servidor Web estiver usando o domínio personalizado `microsoft-edge.devtools` na porta `7331` , quando você exibir o site do seu dispositivo Android, você deverá usar a URL `microsoft-edge.devtools:7331` .  

> [!TIP]
> Para retomar a navegação normal, lembre-se de reverter as configurações de proxy em seu dispositivo Android após desconectar-se da máquina de desenvolvimento.  

<!--  
  


-->  
<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introdução à depuração remota de dispositivos Android | Documentos da Microsoft"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de depuração da Web Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Lula: Optimising Web Delivery"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler – proxy de depuração de Web gratuito"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
