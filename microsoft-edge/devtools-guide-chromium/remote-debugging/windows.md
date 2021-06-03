---
description: Começar com a Depuração Remota Windows 10 dispositivos
title: Começar com a depuração remota Windows 10 Dispositivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, remoto, depuração, windows 10, windows, device portal
ms.openlocfilehash: e3f60f07ba96aaed8cd9d7348eee1b0a846faecf
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519225"
---
# <a name="get-started-with-remote-debugging-windows-10-devices"></a>Começar com a depuração remota Windows 10 Dispositivos  

Conteúdo ao vivo de depuração remota em um Windows 10 do seu computador Windows ou macOS.  Este tutorial ensina as seguintes tarefas.  

*   Configurar seu dispositivo Windows 10 para depuração remota e conectar-se a ele a partir de sua máquina de desenvolvimento.  
*   Inspecionar e depurar conteúdo ao vivo em seu Windows 10 do seu computador de desenvolvimento.  
*   Conteúdo de screencast do seu Windows 10 em uma instância do DevTools em seu computador de desenvolvimento.  
    
## <a name="step-1-set-up-the-host-debuggee-machine"></a>Etapa 1: Configurar o host (máquina de depuração)  

O host ou a máquina de depuração é o dispositivo Windows 10 que você deseja depurar.  Pode ser um dispositivo remoto difícil de acessar fisicamente ou pode não ter periféricos de teclado e mouse, dificultando a interação com o Microsoft Edge DevTools nesse dispositivo.  Para configurar o computador host \(debuggee\), você precisa concluir as seguintes ações.  

*   Instalar e configurar [Microsoft Edge (Chromium)][MicrosoftEdgeMain]  
*   Instale as [Ferramentas Remotas para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] do [Microsoft Store][MicrosoftStoreAppsWindows]  
*   Ativar [o Modo de Desenvolvedor][WindowsAppsGetStartedEnableYourDeviceForDevelopment] e habilitar o Device [Portal][WindowsUwpDebugTestPerfDevicePortal]  
    
### <a name="install-and-configure-microsoft-edge-chromium"></a>Instalar e configurar Microsoft Edge (Chromium)  

Se você ainda não tiver, instale Microsoft Edge \(Chromium\) [nesta página][MicrosoftEdgeMain].  Se você estiver usando uma versão pré-instalada do Microsoft Edge no computador host \(debuggee\), verifique se você Microsoft Edge \(Chromium\) e não Microsoft Edge \(EdgeHTML\).  Uma maneira rápida de verificar é carregar no navegador e confirmar se o número `edge://settings/help` da versão é 75 ou superior.  

Agora navegue `edge://flags` até Microsoft Edge \(Chromium\).  Em **Sinalizadores de pesquisa,** digite Enable **remote depurgging through Windows Device Portal**.  De definir esse sinalizador **como Habilitado**.  Em seguida, escolha o **botão Reiniciar** para reiniciar Microsoft Edge \(Chromium\).  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png" alt-text="Definindo o sinalizador Habilitar a depuração remota Windows Device Portal como Habilitado" lightbox="../media/remote-debugging-windows-media-edge-flags-on-host.msft.png":::
   Definindo **o sinalizador Habilitar a depuração remota Windows Device Portal** como **Habilitado**  
:::image-end:::  

### <a name="install-the-remote-tools-for-microsoft-edge-beta"></a>Instalar as Ferramentas Remotas para Microsoft Edge (Beta)  

Instale as [Ferramentas Remotas para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] do [Microsoft Store][MicrosoftStoreAppsWindows].  

> [!NOTE]
> O **botão Obter** para as Ferramentas Remotas para Microsoft Edge [(Beta)][MicrosoftStoreApps9p6cmfv44zlt] pode ser desabilitado se você estiver Windows 10 versão 1809 ou anterior.  Para configurar o computador host \(debuggee\), ele deve estar executando Windows 10 versão 1903 ou posterior.  Atualize a máquina host \(debuggee\) para adquirir as Ferramentas Remotas para Microsoft Edge [(Beta)][MicrosoftStoreApps9p6cmfv44zlt].  

:::image type="complex" source="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png" alt-text="As Ferramentas Remotas Microsoft Edge \(Beta\) no Microsoft Store" lightbox="../media/remote-debugging-windows-media-remote-tools-in-store.msft.png":::
   As [Ferramentas Remotas para Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] no [Microsoft Store][MicrosoftStoreAppsWindows]  
:::image-end:::  

Iniciar a caixa de diálogo [Ferramentas Remotas Microsoft Edge (Beta)][MicrosoftStoreApps9p6cmfv44zlt] e, se solicitado, aceitar a caixa de diálogo permissões no aplicativo.  Agora você pode fechar as Ferramentas Remotas para Microsoft Edge [(Beta)][MicrosoftStoreApps9p6cmfv44zlt] e não precisa abri-la para futuras sessões de depuração remota.

### <a name="activate-developer-mode-and-enable-device-portal"></a>Ativar o Modo de Desenvolvedor e habilitar o Device Portal  

Se você estiver em uma rede WiFi, verifique se a rede está marcada como **Domínio** ou **Particular**.  Você pode verificar o estado abrindo o aplicativo **Segurança do Windows,** escolhendo no **Firewall &** de rede e verificando se sua rede está listada como uma rede **domínio** ou **rede** privada.  

Se ele estiver listado como **** **Público,** navegue até Configurações  >  **Rede & Internet**  >  **Wi-Fi,** **** escolha em sua rede e alterne o botão Perfil de rede como **Privado**.  

Agora, abra o aplicativo **Configurações.**  Em **Encontrar uma configuração,** digite `Developer settings` e escolha-a.  Alternar no **modo de desenvolvedor**.  Agora, você pode ativar o **Device Portal** definindo **Ativar diagnósticos remotos em conexões** de rede de área local como **Ativar**.  Você pode, opcionalmente, ativar a **Autenticação** para que o dispositivo cliente \(depurador\) forneça as credenciais corretas para se conectar a esse dispositivo.  

> [!NOTE]
> Se **ativar diagnósticos remotos em conexões de rede de área local.** foi anteriormente ligado, você deve a desativar e a ativar novamente para que o **Device Portal** funcione com as Ferramentas Remotas para Microsoft Edge [(Beta)][MicrosoftStoreApps9p6cmfv44zlt].  Se uma **seção Para desenvolvedores** não for exibida no Configurações **,** o **Device Portal** já pode estar ligado, portanto, tente reiniciar o dispositivo Windows 10 em vez disso.

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings.msft.png" alt-text="O Configurações aplicativo com o Modo de Desenvolvedor e o Portal de Dispositivos configurados" lightbox="../media/remote-debugging-windows-media-host-settings.msft.png":::
   O **Configurações** aplicativo com o **Modo** de Desenvolvedor e o Portal **de Dispositivos** configurados  
:::image-end:::  

Observe o endereço IP do computador e a porta de conexão exibidas **em Conexão usando:**.  O endereço IP na imagem abaixo é `192.168.86.78` e a porta de conexão é `50080` .  

:::image type="complex" source="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png" alt-text="Observe o endereço IP e a porta de conexão no Configurações" lightbox="../media/remote-debugging-windows-media-host-settings-ip-address.msft.png":::
   Observe o endereço IP e a porta de conexão no **Configurações**  
:::image-end:::  

Insira as informações sobre o dispositivo cliente \(depurador\) na [próxima seção](#step-2-set-up-the-client-debugger-machine).  Abra guias em Microsoft Edge e [PWAs (Progressive Web Apps)][DevtoolsProgressiveWebApps] no computador host \(debuggee\) que você deseja depurar do computador cliente \(depurador\).  

## <a name="step-2-set-up-the-client-debugger-machine"></a>Etapa 2: Configurar o cliente (máquina de depurador)  

O cliente ou a máquina de depurador é o dispositivo de onde você deseja depurar.  Esse dispositivo pode ser sua máquina de desenvolvimento diária ou pode ser apenas seu computador ou MacBook ao trabalhar em casa.  

Para configurar o computador cliente \(depurador\), instale-o Microsoft Edge \(Chromium\) nesta página se ainda não tiver sido instalado. [][MicrosoftEdgeMain]  Se você estiver usando uma versão pré-instalada do Microsoft Edge no computador host \(debuggee\), verifique se você Microsoft Edge \(Chromium\) e não Microsoft Edge \(EdgeHTML\).  Uma maneira rápida de verificar é carregar no navegador e confirmar se o número `edge://settings/help` da versão é 75 ou superior.  

Agora navegue `edge://flags` até Microsoft Edge \(Chromium\).  Em **Sinalizadores de pesquisa,** digite **Habilitar a depuração**Windows dispositivo remoto em edge://inspect .  De definir esse sinalizador **como Habilitado**.  Em seguida, escolha o **botão Reiniciar** para reiniciar Microsoft Edge \(Chromium\).  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png" alt-text="Definir o sinalizador Habilitar Windows depuração de dispositivo remoto por meio edge://inspect como Habilitado" lightbox="../media/remote-debugging-windows-media-edge-flags-on-client.msft.png":::
   Definindo **o sinalizador Habilitar Windows dispositivo de edge://inspect** remoto como **Habilitado**  
:::image-end:::  

Agora navegue até `edge://inspect` a página Microsoft Edge \(Chromium\).  Por padrão, você deve estar na **seção Dispositivos.**  Em Conexão para um dispositivo Windows remoto, insira o endereço IP e **a**porta de conexão do computador host \(debuggee\) na caixa de texto seguindo este padrão: http:// `IP address` : `connection port` .  Agora escolha **Conexão para Device**.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect.msft.png" alt-text="A edge://inspect no cliente" lightbox="../media/remote-debugging-windows-media-edge-inspect.msft.png":::
   A `edge://inspect` página no cliente  
:::image-end:::  

Se você configurar a autenticação para o computador host \(debuggee\), **** será solicitado a inserir o nome de usuário e a senha do computador cliente \(depurador\) para se conectar com êxito. ****  

### <a name="using-https-instead-of-http"></a>Usando https em vez de http  

Se você quiser se conectar ao computador host \(depurador\) usando, em vez de , você deve navegar para Microsoft Edge no computador `https` `http` cliente `http://IP address:50080/config/rootcertificate` \(depurador\).  Isso baixa automaticamente um certificado de segurança chamado `rootcertificate.cer` .

Escolha `rootcertificate.cer` .  Isso abre a [Windows do Gerenciador de Certificados.][DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]

Escolha **Instalar certificado...**, verifique se **o Usuário Atual** está ligado e escolha **Próximo**.  Agora escolha **Colocar todos os certificados no armazenamento a seguir** e escolha **Procurar...**.  Escolha o **armazenamento autoridades de certificação raiz confiáveis** e escolha **OK**.  Escolha **Próximo** e, em seguida, escolha **Concluir**.  Se solicitado, confirme se deseja instalar esse certificado no armazenamento **autoridades de** certificação raiz confiáveis.

Agora, ao se conectar ao computador host \(debuggee\) do computador cliente \(depurador\) usando a página, você deve `edge://inspect` usar um valor `connection port` diferente.  Por padrão, para Windows desktop, o Device Portal `50080` usa como o para `connection port` `http` .  For `https` , the Device Portal uses so follow this `50043` pattern: https:// : on the `IP address` `50043` `edge://inspect` page.  [Leia mais sobre as portas padrão usadas pelo Device Portal][WindowsUwpDebugTestPerfDevicePortalSetup].  

> [!NOTE]
> A porta padrão para é e a porta padrão para é, mas nem sempre é o caso como o Device Portal em portas de declarações da área de trabalho no intervalo efêmero `http` `50080` `https` `50043` \(\>50.000\) para evitar colisões com declarações de porta existentes no dispositivo.  Para saber mais, navegue até a seção [Porta Configurações][WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal] Portal de Dispositivos Windows área de trabalho.  

## <a name="step-3-debug-content-on-the-host-from-the-client"></a>Etapa 3: Depurar conteúdo no host do cliente  

Se a máquina cliente \(depurador\) se conectar com êxito ao computador host \(debuggee\), a página no cliente agora exibirá uma lista das guias no Microsoft Edge e em qualquer PWAs aberto no `edge://inspect` host.  

:::image type="complex" source="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png" alt-text="A edge://inspect no cliente exibe as guias em Microsoft Edge e PWAs no host" lightbox="../media/remote-debugging-windows-media-edge-inspect-connected.msft.png":::
   A `edge://inspect` página no cliente exibe as guias em Microsoft Edge e PWAs no host  
:::image-end:::  

Determine o conteúdo que você deseja depurar e escolha **inspecionar**.  O Microsoft Edge DevTools abre em uma nova guia e exibe o conteúdo do computador host \(debuggee\) para o computador cliente \(depurador\).  Agora você pode usar a potência total do Microsoft Edge DevTools no cliente para conteúdo em execução no host.  Saiba mais sobre como usar o Microsoft Edge DevTools [aqui][DevtoolsIndex].  

:::image type="complex" source="../media/remote-debugging-windows-media-devtools-client.msft.png" alt-text="O Microsoft Edge DevTools no cliente depurando uma guia Microsoft Edge no host" lightbox="../media/remote-debugging-windows-media-devtools-client.msft.png":::
   O [Microsoft Edge DevTools][DevtoolsIndex] no cliente depurando uma guia Microsoft Edge no host  
:::image-end:::  

### <a name="inspect-elements"></a>Inspecionar elementos  

Por exemplo, tente inspecionar um elemento.  Navegue até a ferramenta **Elements** da sua instância de DevTools no cliente e passe o mouse em um elemento para realça-lo no viewport do dispositivo host.  

Você também pode tocar em um elemento na tela do dispositivo host para escolher na **ferramenta Elements.**  Escolha **Selecionar Elemento** em sua instância de DevTools no cliente e toque no elemento na tela do dispositivo host.  

> [!NOTE]
> **Select Element** é desabilitado após o primeiro toque, portanto, você precisa acioná-lo novamente sempre que quiser usar esse recurso.  

> [!IMPORTANT]
> O **painel Ouvintes de** Eventos na ferramenta **Elementos** está em branco Windows 10 versão 1903.  Esse é um problema conhecido e a equipe planeja corrigir o painel **Ouvintes** de Eventos em uma atualização de manutenção para Windows 10 versão 1903.  

## <a name="step-4-screencast-your-host-screen-to-your-client-device"></a>Etapa 4: screencast your host screen to your client device  

Por padrão, a instância DevTools no cliente tem a screencasting ativado, o que permite exibir o conteúdo no dispositivo host em sua instância de DevTools em seu dispositivo cliente.  Escolha **Alternar Screencast** para desativar ou ativar esse recurso.  

:::image type="complex" source="../media/remote-debugging-windows-media-toggle-screencast.msft.png" alt-text="O botão Toggle Screencast no Microsoft Edge DevTools no cliente" lightbox="../media/remote-debugging-windows-media-toggle-screencast.msft.png":::
   O **botão Toggle Screencast** no Microsoft Edge DevTools no cliente  
:::image-end:::  

Você pode interagir com o screencast de várias maneiras:  
*   As escolha são traduzidas em toques, disparando eventos de toque apropriados no dispositivo.  
*   Teclas de teclas em seu computador são enviadas para o dispositivo.  
*   Para simular um gesto de pinça, segure `Shift` enquanto arrasta.  
*   Para rolar, use o trackpad ou a roda do mouse ou arremesse com o ponteiro do mouse.  

Algumas anotações em screencasts:  
*   Os screencasts exibem apenas o conteúdo da página.  Partes transparentes do screencast representam interfaces de dispositivo, como a barra de endereços Microsoft Edge, a barra de tarefas Windows 10 ou o teclado Windows 10.  
*   Screencasts afetam negativamente as taxas de quadros.  Desabilite o screencasting durante a medição de rolagem ou animações para obter uma imagem mais precisa do desempenho da sua página.  
*   Se a tela do dispositivo host for travada, o conteúdo do screencast desaparecerá.  Desbloqueie a tela do dispositivo host para retomar automaticamente a screencast.  

## <a name="known-issues"></a>Problemas Conhecidos  

O **painel Ouvintes de** Eventos na ferramenta **Elementos** está em branco Windows 10 versão 1903.  A equipe planeja corrigir o painel **Ouvintes** de Eventos em uma atualização de manutenção para Windows 10 versão 1903.  

O **painel Cookies** no painel **Aplicativo** está em branco na Windows 10 versão 1903.  A equipe planeja corrigir o painel **Cookies** em uma atualização de serviço para Windows 10 versão 1903.  

A **ferramenta Auditorias,** a ferramenta De exibição **3D,** a seção **** Dispositivos **Emulados** no **Configurações**e o painel de árvore acessibilidade na ferramenta **Elements** não estão funcionando como esperado.  A equipe planeja corrigir as ferramentas listadas em uma atualização futura de Microsoft Edge.  

O explorador de arquivos não é lançado a partir do DevTools na ferramenta **Sources** ou no painel **Segurança** quando você depura remotamente.  A equipe planeja corrigir as ferramentas em uma atualização futura de Microsoft Edge.  

<!-- links -->

[DevtoolsIndex]: ../index.md "Visão geral das Ferramentas para Desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicativos Web progressivos | Microsoft Docs"  

[DotnetFrameworkWcfFeatureDetailsHowToViewCertificatesWithMmcSnapInViewCertificatesWithCertificateManagerTool]: /dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in#view-certificates-with-the-certificate-manager-tool "Exibir certificados com a ferramenta Gerenciador de Certificados - Como: Exibir certificados com o snap-in MMC | Microsoft Docs"  

[WindowsAppsGetStartedEnableYourDeviceForDevelopment]: /windows/apps/get-started/enable-your-device-for-development "Habilitar seu dispositivo para desenvolvimento | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Windows Visão geral do Device Portal | Microsoft Docs"  
[WindowsUwpDebugTestPerfDevicePortalSetup]: /windows/uwp/debug-test-perf/device-portal#setup "Instalação - Windows visão geral do Device Portal | Microsoft Docs"  
[WindowsUwpDebugTestPerfDevicePortalDesktopRegistryBasedConfigurationForDevicePortal]: /windows/uwp/debug-test-perf/device-portal-desktop#registry-based-configuration-for-device-portal "Configuração baseada no Registro para o Device Portal - Device Portal para Windows desktop | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Baixar Novo Microsoft Edge Navegador"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Aplicativos | Microsoft Store"  

[MicrosoftStoreApps9p6cmfv44zlt]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Ferramentas remotas para Microsoft Edge (Beta) | Microsoft Store"  
