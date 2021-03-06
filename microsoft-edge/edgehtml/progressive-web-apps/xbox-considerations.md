---
description: Verifique se o PWA oferece uma ótima experiência para o Xbox
title: Aplicativos Web Progressivos para Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3ac4174c821f221d6d666a25880867275ca5cbd5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397668"
---
# <a name="progressive-web-apps-for-xbox-one"></a>Aplicativos Web Progressivos para Xbox One  

Você pode estender um aplicativo Web e torná-lo disponível como um aplicativo Xbox One por meio da Microsoft Store enquanto continua a usar suas estruturas, CDN e back-end de servidor existentes.  E, como todos os aplicativos da Plataforma Universal do Windows \(UWP\), os Aplicativos Web Progressivos \(PWAs\) em execução no Xbox One também podem chamar APIs nativas do Windows 10.  Já há vários PWAs disponíveis para o Xbox One, especialmente na categoria de aplicativos de [reprodução de mídia.](#media-pwas-on-xbox)  

Na maioria das vezes, você pode empacotar seu PWA para Xbox One da mesma maneira que faria para [o Windows,](./windows-features.md)usando as ferramentas do Construtor do [PWA](https://www.pwabuilder.com) ou o IDE do [Visual Studio](https://visualstudio.microsoft.com/vs) para gerar o arquivo necessário para executar o PWA como um aplicativo `appxmanifest` UWP.  No entanto, há várias diferenças importantes que este guia orientará você.  

## <a name="deploying-and-testing-pwas-on-xbox"></a>Implantando e testando PWAs no Xbox  

Para começar, siga estas etapas [para ativar o modo de desenvolvedor do *Xbox One.*](/windows/uwp/xbox-apps/devkit-activation)  Com o Modo de Desenvolvedor ativado, configurar o [ *Device Portal para Xbox* ](/windows/uwp/debug-test-perf/device-portal-xbox) para obter acesso remoto ao seu Xbox a partir do navegador em seu ambiente de desenvolvimento.  

Agora você está pronto para implantar seu aplicativo para testes usando o Construtor do PWA ou Visual Studio.  

### <a name="option-1--pwa-builder"></a>Opção 1: Construtor do PWA  

[O Construtor de PWA](https://www.pwabuilder.com) é um Node.js que você pode instalar a partir do Nó Gerenciador de Pacotes \(NPM\).  Ele usa os metadados do seu site para gerar aplicativos hospedados nativos no Android, iOS e Windows.  Se o seu site já tiver um [manifesto do aplicativo Web,](https://developer.mozilla.org/docs/Web/Manifest)o Construtor do PWA o usará para gerar pacotes de instalação específicos da plataforma.  Caso contrário, o Construtor do PWA gerará um arquivo `manifest.json` básico com base nas características do seu site.  

#### <a name="requirements"></a>Requisitos  

*   [Node.js](https://nodejs.org), que inclui NPM.  

#### <a name="setup"></a>Configuração  

1.  Abra um prompt de comando Node para instalar o Construtor do PWA:  
    
    ```shell
    npm install pwabuilder --global
    ```  
    
1.  Execute o Construtor do PWA na URL do seu site:  
    
    ```shell
    pwabuilder https://example.com/ -windows10
    ```  
    
    O *sinalizador -windows10* limita a geração de pacotes para o Windows 10 \(UWP\).  Você pode omitir a geração de pacotes em todas as plataformas com suporte, incluindo iOS e Android.  Consulte os [documentos do Construtor do PWA](https://docs.pwabuilder.com) para obter mais informações.  
    
1.  No Device [Portal para Xbox,](/windows/uwp/debug-test-perf/device-portal-xbox)vá para **Home**Meus jogos & aplicativos Adicionar , escolha a opção para carregar arquivos soltos e selecione a pasta de manifesto do aplicativo  >  ****  >  **** Windows 10 **** gerada pelo Construtor do PWA no diretório atual.  
1.  Passo a passo pelo assistente para concluir o processo de instalação.  Depois de instalado.  você poderá ver e iniciar seu PWA no painel do Xbox One.  
    
### <a name="option-2--visual-studio"></a>Opção 2: Visual Studio  

O Visual Studio [Community 2017](https://visualstudio.microsoft.com/vs/community) gratuito e completo inclui ferramentas de desenvolvedor do Windows 10, modelos de aplicativos universais, um editor de código, um poderoso depurador, emuladores do Windows Mobile, suporte a idiomas ricos e muito mais, tudo pronto para uso na produção.  As [versões Professional e Enterprise](https://visualstudio.microsoft.com/vs/compare) fornecem ainda mais recursos.  

#### <a name="requirements"></a>Requisitos  

*   [Visual Studio 2017](https://visualstudio.microsoft.com/vs): Qualquer versão, incluindo a edição gratuita da Comunidade.  
*   [SDK do Windows 10](/windows/uwp/xbox-apps/development-environment-setup): selecione este componente opcional no Visual Studio Instalador 2017.  

#### <a name="setup"></a>Configuração  

1.  Siga as etapas para [configurar e executar seu PWA como um aplicativo Universal do Windows.](./windows-features.md#set-up-and-run-your-universal-windows-app)  Com isso, você terá um aplicativo Windows 10 totalmente funcional capaz de acessar APIs Universais do Windows.  
1.  Agora você pode implantar e depurar seu PWA \(como um aplicativo UWP\) no Xbox One \(como em qualquer outro dispositivo remoto do Windows 10\) usando o depurador remoto [Visual Studio](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017&preserve-view=true
).  Como alternativa, você pode instalar o PWA usando o [Device Portal para Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) usando as etapas a seguir.  
1.  No Device Portal para Xbox, vá para **Home**  >  **My games \& apps**Adicionar , escolha a opção para carregar o Pacote de Aplicativos e  >  **** **Dependências**.  
1.  Navegue até a pasta de pacote gerada para seu aplicativo na Etapa 1 e selecione o `.appx` arquivo para carregamento.  O [arquivo .appx](/windows/uwp/packaging/packaging-uwp-apps) é um arquivo de pacote de aplicativo UWP que pode ser sideload em qualquer dispositivo para fins de teste.  
1.  Em seguida, **toque no botão** Dependências e selecione a `dependencies` sub-pasta para seu aplicativo e carregue cada uma delas.  Esta etapa só é necessária para implantar aplicativos do Device Portal para Xbox.  Visual Studio oferece dependências quando a depuração remota e o computador do usuário final já as terá instaladas quando entregues da Microsoft Store.  
1.  Com o pacote do aplicativo e as dependências carregadas, clique no botão **Ir** na seção *Implantar* e o aplicativo será instalado.  Você está pronto para iniciar seu aplicativo no Xbox!  

## <a name="ux-considerations-for-pwas-on-xbox"></a>Considerações sobre o UX para PWAs no Xbox  

### <a name="design-for-the-10-foot-experience"></a>Design para a "Experiência de 3 metros"  

O Xbox One é considerado uma "experiência de 3 metros", o que significa que seus usuários provavelmente estarão sentados a pelo menos 3 metros da tela.  Como tal, considere como seu aplicativo pode ser usado nessa distância, em vez da experiência tradicional do navegador da Web da área de trabalho com um mouse e teclado.  Para obter orientações sobre design eux, confira [Designing for Xbox and TV](/windows/uwp/design/devices/designing-for-tv).  

### <a name="understand-the-tv-safezone"></a>Entenda o "TV SafeZone"  

Os fabricantes de televisão aplicarão [uma zona segura](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) em torno do conteúdo que pode cortar seu aplicativo.  Por padrão, aplicamos uma borda segura ao redor do seu aplicativo para levar em conta isso, no entanto, você pode garantir que seu aplicativo use o tamanho da tela inteira chamando [setDesiredBoundsMode](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) e especificando [useCoreWindow](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode):  

```javascript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```  

Para saber mais, confira a documentação do namespace [Windows.UI.ViewManagement.](/uwp/api/windows.ui.viewmanagement)  

### <a name="manage-xy-focus-and-navigation"></a>Gerenciar o foco e a navegação XY  

Os métodos de entrada do usuário para Xbox são gamepad ou controle remoto, que usam um sistema de navegação [XY,](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction)permitindo que o usuário mude o foco do controle para o controle movendo para cima, para baixo, para a esquerda e para a direita.  

Dessa forma, você vai querer garantir que seu aplicativo funcione bem com a navegação XY.  Além disso, certifique-se de desabilitar o modo de mouse [,](/windows/uwp/xbox-apps/how-to-disable-mouse-mode)que está em por padrão para aplicativos UWP \(e provavelmente não se aplica à experiência do Xbox do seu aplicativo\).  

O código a seguir desliga o modo e permite que a entrada `mouse` do gamepad gere eventos de teclado DOM:  

```javascript
navigator.gamepadInputEmulation = "keyboard";
```  

Como alternativa, você pode especificar , que também desliga o mouse, não gera eventos de teclado DOM e permite que você use as APIs padrão `gamepad` do gamepad Web e/ou WinRT.  

Para habilitar a navegação direcional, confira a [biblioteca TVJS](#tvjs), abordada em seguida.  

### <a name="tvjs"></a>TVJS  

[TVJS é uma coleção de bibliotecas auxiliares](https://github.com/Microsoft/TVHelpers) que facilitam a complicação web para a TV.  Se você estiver criando um aplicativo Web hospedado que também será executado no ** Xbox, o TVJS poderá ajudar a adicionar suporte para navegação direcional, bem como fornecer vários controles que facilitam a interação com o conteúdo na TV.  

[A navegação direcional](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) é um recurso TVJS que fornece navegação bidimensional automática dentro das páginas do seu aplicativo de TV.  Com ele, não é necessário interceptar e manipular a navegação dentro das páginas do aplicativo ou especificar explicitamente todos os destinos de foco válidos para cada elemento na interface do usuário.  A manipulação automática de foco permite que os usuários possam navegar de forma intuitiva e robusta.  

À medida que o usuário navega na interface do usuário do aplicativo com os botões de direção do controlador, o algoritmo de foco automático analisa o conjunto de possíveis destinos de foco, determina o próximo elemento para o qual se mover e define automaticamente o foco para esse elemento.  Para determinar o próximo elemento, o algoritmo combina entrada direcional, histórico de foco passado e o layout físico dos elementos da interface do usuário na página.  

Para habilitar a navegação direcional, inclua a seguinte referência de script:  

```html
<script src="directionalnavigation-1.0.0.0.js"></script>
```  

Por padrão, somente `<a>` , , , e elementos são `<button>` `<input>` `<select>` `<textarea>` focalizados.  Para habilitar o foco em outros elementos, atribua a eles um [tabindex válido.](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)  

```html
<div tabindex="0″>This div is eligible for focus</div>
```  

Confira a [documentação DirectionalNavigation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) para saber como alterar o elemento raiz, definir o foco inicial, substituir o próximo foco, otimizar controles para foco, personalizar a entrada.  Há também uma série de outros exemplos úteis.

## <a name="media-pwas-on-xbox"></a>PWAs de mídia no Xbox  

Se você estiver criando um PWA de reprodução de mídia para Xbox One, esteja ciente das seguintes considerações.  

### <a name="encrypted-media-extensions-eme-in-the-browser"></a>Extensões de Mídia Criptografadas (EME) no navegador  

O navegador do Microsoft Edge no Xbox One não dá suporte a [Extensões de Mídia Criptografadas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) \(EME\).  Se o PWA de mídia o usar para gerenciamento de direitos digitais \(DRM\), você não poderá executar isso do navegador em seu Xbox.  Em vez disso, protótipo e teste-o como um [aplicativo Xbox One usando PWABuilder ou Visual Studio](#deploying-and-testing-pwas-on-xbox), conforme descrito acima.  Você também pode executar no navegador do Microsoft Edge no Windows, onde o EME é totalmente suportado.  

### <a name="integrating-with-system-media-transport-controls"></a>Integração com controles de transporte de mídia do sistema  

Se seu aplicativo for um aplicativo de mídia, é importante que seu aplicativo responda aos controles de mídia [](/windows/uwp/audio-video-camera/system-media-transport-controls) iniciados pelo usuário por meio de botões na tela, comandos de voz da [Cortana](https://support.xbox.com/xbox-one/console/cortana-voice-commands), Controles de Transporte de Mídia do Sistema no painel de nav ou os aplicativos [Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) e [Xbox One SmartGlass](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) em outros dispositivos.  Confira o controle [MediaPlayer](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) da biblioteca [TVJS](#tvjs), que se integra automaticamente a esses controles.  Como alternativa, você pode integrar [manualmente com os Controles de Transporte](/windows/uwp/audio-video-camera/system-media-transport-controls)de Mídia do Sistema.  

### <a name="playready-content-encryption"></a>Criptografia de conteúdo PlayReady  

No momento da escrita, o suporte à codificação de [cbcs](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) é limitado ao cliente PlayReady para XBox One \(versão 1709 ou superior\).  Se a mídia do seu PWA só dá suporte à criptografia **cbcs,** esteja ciente de que a funcionalidade do aplicativo provavelmente será limitada \(ou completamente indisponível\) no Windows.  

## <a name="see-also"></a>Veja também  

[Vídeo de South Ridge](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video): um aplicativo de vídeo de exemplo para Xbox criado com React.js e hospedado em um servidor Web.  

[Projetando para Xbox](/windows/uwp/design/devices/designing-for-tv)e TV : Projete seu aplicativo da Plataforma Universal do Windows \(UWP\) para que ele pareça bom e funcione bem no Xbox One e nas telas de televisão.  

[Práticas recomendadas do Xbox:](/windows/uwp/xbox-apps/tailoring-for-xbox)siga estas práticas recomendadas para adaptar seu aplicativo para Xbox One.  

[PWAs na Microsoft Store](./microsoft-store.md): Veja como \(e por quê?\) enviar seu PWA para a Microsoft Store.  

[UWP no Xbox One](/windows/uwp/xbox-apps/index): um guia completo para o desenvolvimento de aplicativos UWP para Xbox One.  
