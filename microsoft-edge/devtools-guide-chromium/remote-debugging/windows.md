---
title: Introdução à depuração remota de dispositivos Windows 10
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, remoto, depuração, Windows 10, Windows, Device Portal
ms.openlocfilehash: b944e1f16d4c26f4db83e3eb131f1da8ea938c97
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561495"
---
# Introdução à depuração remota de dispositivos Windows 10  

Depuração remota do conteúdo ao vivo em um dispositivo com o Windows 10 a partir do seu computador com Windows ou macOS.  Este tutorial ensina a:  

*   Configure seu dispositivo Windows 10 para depuração remota e conecte-se a ele a partir de seu computador de desenvolvimento.  
*   Inspecione e depure conteúdo dinâmico em seu dispositivo Windows 10 a partir de seu computador de desenvolvimento.  
*   O conteúdo do screencast do seu dispositivo Windows 10 para uma instância do DevTools em seu computador de desenvolvimento.  

## Etapa 1: configurar o host (computador depurado)  

O host ou computador que o está depurando é o dispositivo Windows 10 que você deseja depurar.  Pode ser um dispositivo remoto difícil para você acessar fisicamente ou pode não ter periféricos do teclado e do mouse, tornando difícil interagir com o Microsoft Edge DevTools nesse dispositivo.  Para configurar o computador host (que está depurando), você precisará:  

*   Instalar e configurar [o Microsoft Edge (Chromium)](https://www.microsoft.com/edge)  
*   Instalar as [ferramentas remotas para o Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) da [Microsoft Store](https://www.microsoft.com/store/apps/windows)  
*   Ativar o [modo de desenvolvedor](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development) e habilitar o [Device portal](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal)  

### Instalar e configurar o Microsoft Edge (Chromium)  

Se ainda não fez isso, instale o Microsoft Edge (Chromium) [desta página](https://www.microsoft.com/edge).  Se você estiver usando uma versão pré-instalada do Microsoft Edge no computador host (Depurando), verifique se você tem o Microsoft Edge (Chromium) e não o Microsoft Edge (EdgeHTML).  Uma maneira rápida de verificar é carregar `edge://settings/help` no navegador e confirmar se o número da versão é 75 ou superior.  

Agora, navegue até `edge://flags` o Microsoft Edge (Chromium).  Em **sinalizadores de pesquisa**, digite **habilitar a depuração remota pelo Windows Device portal**.  Defina esse sinalizador como **habilitado**.  Em seguida, clique no botão **reiniciar** para reiniciar o Microsoft Edge (Chromium).  

> ##### Figura 1  
> Definindo o sinalizador **habilitar a depuração remota por meio do Windows Device portal** como **habilitado**  
> ![Definindo o sinalizador habilitar a depuração remota por meio do Windows Device portal como habilitado](./windows-media/edge-flags-on-host.png)  

### Instalar as ferramentas remotas para o Microsoft Edge (beta)  

Instale as [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) da [Microsoft Store](https://www.microsoft.com/store/apps/windows).  

> [!NOTE]
> O botão **obter** para as [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) pode ser desabilitado se você estiver no Windows 10 versão 1809 ou anterior.  Para configurar o computador host (que está depurando), ele deve estar executando o Windows 10 versão 1903 ou posterior.  Atualize a máquina do host (Depurando) para adquirir as [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT).  

> ##### Figura 2  
> [Ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) na [Microsoft Store](https://www.microsoft.com/store/apps/windows)  
> ![Ferramentas remotas para Microsoft Edge (beta) na Microsoft Store](./windows-media/remote-tools-in-store.png)  

Inicie as [ferramentas remotas do Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) e, se solicitado, aceite a caixa de diálogo permissões no aplicativo. Agora você pode fechar as [ferramentas remotas do Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) e não precisa abri-las para sessões futuras de depuração remota.

### Ativar o modo de desenvolvedor e habilitar o Device Portal  

Se você estiver em uma rede WiFi, verifique se a rede está marcada como **Domain** ou **Private**.  Você pode verificar isso abrindo o aplicativo **de segurança do Windows** , clicando em **Firewall & proteção de rede** e verificando se a rede está listada como uma rede de **domínio** ou **privada** .  

Se estiver listado como **público**, acesse **configurações**  >  **rede & Internet**  >  **Wi-Fi**, clique em sua rede e alterne o botão do **perfil de rede** para **particular**.  

Agora, abra o aplicativo **configurações** .  Em **Localizar uma configuração**, insira **configurações do desenvolvedor** e selecione-a.  Ative o **modo de desenvolvedor**.  Agora você pode habilitar o **Device portal** **definindo a opção** **Ativar diagnóstico remoto em conexões de rede local** .  Opcionalmente, você pode ativar a **autenticação** para que o dispositivo cliente (depurador) deva fornecer as credenciais corretas para se conectar a este dispositivo.  

> [!NOTE]
> Se **ativar o diagnóstico remoto em conexões de rede local.** foi habilitado anteriormente, você deve desabilitá-lo e habilitá-lo novamente para que o **Device portal** funcione com as [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT). Se você não vir uma seção **para desenvolvedores** em **configurações**, o **Device portal** pode já estar habilitado, portanto, tente reiniciar o dispositivo Windows 10.

> ##### Figura 3  
> O aplicativo **configurações** com **modo de desenvolvedor** e **Device portal** configurado  
> ![O aplicativo configurações com modo de desenvolvedor e Device portal configurado](./windows-media/host-settings.png)  

Observe o endereço IP do computador e a porta de conexão exibidos em **conectar usando:**.  O endereço IP na imagem abaixo é `192.168.86.78` a porta de conexão `50080` .  

> ##### Figura 4  
> Observe o endereço IP e a porta de conexão nas **configurações**  
> ![Observe o endereço IP e a porta de conexão nas configurações](./windows-media/host-settings-ip-address.png)  

Você inserirá essas informações no dispositivo cliente (depurador) na [próxima seção](#step-2-set-up-the-client-debugger-machine).  Abra as guias no Microsoft Edge e nos [aplicativos Web progressivos (PWAs)](../progressive-web-apps.md) na máquina host (depurada) que você gostaria de Depurar da máquina cliente (depurador).  

## Etapa 2: configurar o cliente (computador do depurador)  

O cliente ou computador do depurador é o dispositivo do qual você deseja fazer a depuração.  Este dispositivo pode ser seu computador de desenvolvimento diário ou pode ser o seu computador ou MacBook quando estiver trabalhando em casa.  

Para configurar o computador cliente (depurador), instale o Microsoft Edge (Chromium) [nesta página](https://www.microsoft.com/edge) se ainda não tiver feito isso.  Se você estiver usando uma versão pré-instalada do Microsoft Edge no computador host (Depurando), verifique se você tem o Microsoft Edge (Chromium) e não o Microsoft Edge (EdgeHTML).  Uma maneira rápida de verificar é carregar `edge://settings/help` no navegador e confirmar se o número da versão é 75 ou superior.  

Agora, navegue até `edge://flags` o Microsoft Edge (Chromium).  Em **sinalizadores de pesquisa**, digite **Habilitar depuração de dispositivo remoto do Windows no Edge://inspect**.  Defina esse sinalizador como **habilitado**.  Em seguida, clique no botão **reiniciar** para reiniciar o Microsoft Edge (Chromium).  

> ##### Figura 5  
> Configurar a **depuração de dispositivo remoto do Windows por meio** do sinalizador Edge://inspect como **habilitado**  
> ![Configurar a depuração de dispositivo remoto do Windows por meio do sinalizador edge://inspect como habilitado](./windows-media/edge-flags-on-client.png)  

Agora, navegue até a `edge://inspect` página no Microsoft Edge (Chromium).  Por padrão, você deve estar na seção **Devices** .  Em **conectar a um dispositivo Windows remoto**, insira o endereço IP e a porta de conexão da máquina host (depurada) na caixa de texto após este padrão: http:// `IP address` : `connection port` .  Agora, clique em **conectar ao dispositivo**.  

> ##### Figura 6  
> A `edge://inspect` página no cliente  
> ![A página edge://inspect no cliente](./windows-media/edge-inspect.png)  

Se você configurar a autenticação para o host (depurador), você será solicitado a inserir o **nome de usuário** e a **senha** do computador cliente (depurador) para se conectar com êxito.  

### Usar HTTPS em vez de http  

Se quiser se conectar ao computador host (que está depurando) usando `https` em vez de `http` , você deve Navgiate `http://IP address:50080/config/rootcertificate` no Microsoft Edge na máquina do cliente (depurador). Isso fará o download automático de um certificado de segurança chamado `rootcertificate.cer` .

Clique em `rootcertificate.cer` . Será aberta a [ferramenta Gerenciador de certificados do Windows](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool).

Clique em **Instalar certificado..**., verifique se o **usuário atual** está selecionado e clique em **Avançar**. Agora, selecione **colocar todos os certificados no repositório a seguir** e clique em **procurar...**. Selecione o repositório de **autoridades de certificação raiz confiáveis** e clique em **OK**. Clique em **Avançar** e clique em **Concluir**. Se for solicitado, confirme que você deseja instalar esse certificado no repositório de **autoridades de certificação raiz confiáveis** .

Agora, ao se conectar ao computador host (que está depurando) a partir da máquina do cliente (depurador) usando a `edge://inspect` página, você deve usar um `connection port` valor diferente.  Por padrão, para janelas da área de trabalho, o Device portal será usado `50080` como o `connection port` para `http` .  Para `https` o Device portal usa `50043` isso, siga este padrão: https:// `IP address` : `50043` na `edge://inspect` página.  [Leia mais sobre as portas padrão usadas pelo Device portal](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal#setup).  

> [!NOTE]
> A porta padrão `http` é `50080` e a porta padrão para `https` é `50043` , mas esse não é sempre o caso porque o Device portal na área de trabalho alega portas no intervalo efêmera (>50.000) para impedir colisões com declarações de porta existentes no dispositivo.  Para saber mais, consulte a seção [configurações de porta](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal) do Device portal na área de trabalho do Windows.  

## Etapa 3: depurar o conteúdo do host do cliente  

Se o computador cliente (depurador) se conectar com êxito ao computador host (Depurando), a `edge://inspect` página no cliente exibirá uma lista das guias no Microsoft Edge e qualquer PWAs aberto no host.  

> ##### Figura 7  
> A `edge://inspect` página no cliente exibe as guias no Microsoft Edge e no PWAs no host  
> ![A página edge://inspect no cliente exibe as guias no Microsoft Edge e no PWAs no host](./windows-media/edge-inspect-connected.png)  

Determine o conteúdo que você deseja depurar e clique em **inspecionar**.  O Microsoft Edge DevTools será aberto em uma nova guia e no screencast o conteúdo do computador host (Depurando) na máquina do cliente (depurador).  Agora você pode usar todo o potencial do Microsoft Edge DevTools no cliente para conteúdo em execução no host.  Saiba mais sobre como usar o Microsoft Edge DevTools [aqui](../../devtools-guide-chromium.md).  

> ##### Figura 8  
> O [Microsoft Edge devtools](../../devtools-guide-chromium.md) no cliente Depurando uma guia no Microsoft Edge no host  
> ![O Microsoft Edge DevTools no cliente Depurando uma guia no Microsoft Edge no host](./windows-media/devtools-client.png)  

### Inspecionar elementos  

Por exemplo, tente inspecionar um elemento.  Vá para o painel **elementos** da sua instância do devtools no cliente e passe o mouse sobre um elemento para realçá-lo na viewport do dispositivo host.  

Você também pode tocar em um elemento na tela do dispositivo host para selecioná-lo no painel de **elementos** .  Clique em **selecionar elemento** na sua instância do devtools no cliente e, em seguida, toque no elemento na tela do dispositivo host.  Observe que o **elemento select** está desabilitado após o primeiro toque, portanto, você precisa habilitá-lo sempre que quiser usar esse recurso.  

> [!IMPORTANT]
> O painel **ouvintes de eventos** no painel **elementos** está em branco no Windows 10 versão 1903.  Esse é um problema conhecido e corrigiremos o painel **ouvintes de evento** em uma atualização de serviço para a versão 1903 do Windows 10.  

## Etapa 4: screencast a tela do host em seu dispositivo cliente  

Por padrão, a instância DevTools no cliente terá o screencast ativado, que permite que você visualize o conteúdo do dispositivo host na sua instância do DevTools em seu dispositivo cliente.  Clique em **alternar screencast** para desativar ou nesse recurso.  

> ##### Figura 9  
> O botão **alternar screencast** na devtools do Microsoft Edge no cliente  
> ![O botão Alternar screencast na DevTools do Microsoft Edge no cliente](./windows-media/toggle-screencast.png)  

Você pode interagir com o screencast de várias maneiras:  
*   Os cliques são convertidos em toques, disparando eventos de toque apropriados no dispositivo.  
*   Os pressionamentos de teclas do computador são enviados para o dispositivo.  
*   Para simular um gesto de pinçagem, mantenha pressionado `Shift` enquanto arrasta.  
*   Para rolar, use a trackpad ou a roda do mouse, ou Fling com o ponteiro do mouse.  

Algumas observações sobre screencasts:  
*   Screencasts exibem apenas o conteúdo da página.  Partes transparentes do screencast representam interfaces de dispositivos, como a barra de endereços do Microsoft Edge, a barra de tarefas do Windows 10 ou o teclado do Windows 10.  
*   Os screencasts afetam negativamente as tarifas de quadro.  Desabilite o screencast enquanto estiver medindo rolagens ou animações para obter uma imagem mais precisa do desempenho da página.  
*   Se a tela do dispositivo host for bloqueada, o conteúdo do screencast desaparecerá.  Desbloqueie a tela do dispositivo de host para continuar o screencast automaticamente.  

## Problemas conhecidos  

O painel **ouvintes de eventos** no painel **elementos** está em branco no Windows 10 versão 1903.  Corrigiremos o painel **ouvintes de evento** em uma atualização de serviço para a versão 1903 do Windows 10.  

O painel **cookies** no painel do **aplicativo** está em branco na versão 1903 do Windows 10.  Corrigiremos o painel **cookies** em uma atualização de serviço para a versão 1903 do Windows 10.  

O **painel auditorias** , o **painel modo de exibição 3D** , a seção **dispositivos emulados** em **configurações**, e o painel de **árvore de acessibilidade** no painel **elementos** não está funcionando como esperado no momento.  Corrigiremos essas ferramentas em uma atualização futura do Microsoft Edge.  

O explorador de arquivos não será iniciado a partir do DevTools no painel **fontes** ou no painel de **segurança** quando a depuração remota.  Corrigiremos essas ferramentas em uma atualização futura do Microsoft Edge.  
