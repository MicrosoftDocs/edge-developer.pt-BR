---
description: Verifique se o seu PWA oferece uma excelente experiência para o Xbox
title: Aplicativos Web progressivos para Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ms.openlocfilehash: dfa2b2d252bb788c0010017de57ab147d407c5f7
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882846"
---
# Aplicativos Web progressivos para Xbox One  

Você pode estender um aplicativo Web e disponibilizá-lo como um aplicativo Xbox One via Microsoft Store e continuar a usar as estruturas existentes, a CDN e o back-end do servidor.  E, assim como todos os aplicativos da plataforma universal do Windows (UWP), os aplicativos Web progressivos (PWAs) em execução no Xbox One também podem chamar APIs nativas do Windows 10.  Já existem vários PWAs disponíveis para o Xbox One, principalmente na categoria de aplicativos de reprodução de [mídia](#media-pwas-on-xbox).  

Na maioria das vezes, você pode empacotar seu PWA do Xbox One da [mesma forma que faria](./windows-features.md)com o Windows, usando as ferramentas do [PWA Builder](https://www.pwabuilder.com/) ou o IDE do [Visual Studio](https://visualstudio.microsoft.com/vs/) para gerar o arquivo *appxmanifest* necessário para executar o PWA como um aplicativo UWP. No entanto, há várias diferenças importantes em que este guia vai orientá-lo.

## Implantando e testando o PWAs no Xbox

Para começar, siga estas [etapas para ativar o *modo de desenvolvedor do Xbox One* ](/windows/uwp/xbox-apps/devkit-activation) . Com o modo de desenvolvedor ativado, [Configure o *Device portal para Xbox* ](/windows/uwp/debug-test-perf/device-portal-xbox) para obter acesso remoto ao seu Xbox a partir do navegador em seu ambiente de desenvolvimento.

Agora, você está pronto para implantar seu aplicativo para testar usando o *PWA Builder* ou o *Visual Studio*.

### Opção 1: criador do PWA

O [construtor do PWA](https://www.pwabuilder.com/) é um aplicativo Node.js que você pode instalar do Gerenciador de pacotes de nó (NPM). Ele usa os metadados do seu site para gerar aplicativos hospedados nativos em Android, iOS e Windows. Se seu site já tem um [manifesto do aplicativo Web](https://developer.mozilla.org/docs/Web/Manifest), o construtor do PWA o usará para gerar pacotes de instalação específicos da plataforma. Caso contrário, o PWA Builder irá gerar um *manifest.jsbásico em* arquivos com base nas características do seu site.

#### Requisitos
 - [Node.js](https://nodejs.org/en/), que inclui o NPM.

#### Configuração

1. Abrir um prompt de comando do nó para instalar o PWA Builder:

    ```
    npm install pwabuilder --global
    ```

2. Executar o construtor do PWA na URL do seu site:

    ```
    pwabuilder https://example.com/ -windows10
    ```

    O sinalizador *-windows10* limita a geração de pacotes para o Windows 10 (UWP). Você pode omiti-lo para gerar pacotes em todas as plataformas com suporte, incluindo iOS e Android. Consulte os [documentos do PWA Builder](https://docs.pwabuilder.com/) para obter mais informações.

3. No [Device portal para Xbox](/windows/uwp/debug-test-perf/device-portal-xbox), vá para **página inicial**  >  **meus jogos & aplicativos**  >  **Adicionar**, escolha a opção para *carregar arquivos soltos*e selecione a pasta manifesto do aplicativo do Windows 10 gerada pelo PWA Builder no diretório atual.

4. Siga as etapas do assistente para concluir o processo de instalação. Depois de instalado. Você poderá ver e iniciar o PWA no painel Xbox One.


### Opção 2: Visual Studio

A comunidade completa do [Visual Studio 2017](https://visualstudio.microsoft.com/vs/community/) inclui ferramentas de desenvolvedor do Windows 10, modelos de aplicativos universais, um editor de código, um depurador poderoso, emuladores do Windows Mobile, suporte a idiomas avançados e muito mais — tudo pronto para uso na produção. As versões [ *Professional* e *Enterprise* ](https://visualstudio.microsoft.com/vs/compare/) oferecem ainda mais recursos.

#### Requisitos

 - [**Visual Studio 2017**](https://visualstudio.microsoft.com/vs/
): qualquer versão, incluindo a edição gratuita *da Comunidade* .
 - [**SDK do Windows 10**](/windows/uwp/xbox-apps/development-environment-setup): selecione esse componente opcional no *instalador do Visual Studio 2017*.

#### Configuração

1. Siga as etapas para [configurar e executar o PWA como um aplicativo universal do Windows](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#set-up-and-run-your-universal-windows-app). Com isso, você terá um aplicativo totalmente funcional do Windows 10 capaz de acessar as APIs universais do Windows.

2. Agora você pode implantar e depurar o PWA (como um aplicativo UWP) no Xbox One (como em qualquer outro dispositivo remoto do Windows 10) usando o [depurador remoto do Visual Studio](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017
). Como alternativa, você pode instalar o PWA usando o [Device portal para Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) usando as etapas a seguir.

3. No Device portal para Xbox, vá para página inicial > meus jogos & aplicativos > adicionar, escolha a opção para carregar o *pacote e as dependências do aplicativo*.

4. Navegue até a pasta do pacote que você gerou para seu aplicativo na etapa 1 e selecione o arquivo *. Appx* para carregar. O [arquivo *. Appx* ](/windows/uwp/packaging/packaging-uwp-apps) é um arquivo de pacote de aplicativo UWP que pode ser sideloaddo em qualquer dispositivo para fins de teste.

5. Em seguida, toque no botão **dependências** e selecione a subpasta *dependências* para o seu aplicativo e carregar cada uma. Esta etapa só é necessária para implantar aplicativos do Device portal para Xbox. O Visual Studio oferece dependências quando a depuração remota e a máquina do usuário final já têm instaladas quando são entregues pela Microsoft Store.

6. Com o pacote do aplicativo e as dependências carregadas, clique no botão **ir** na seção *implantar* e o aplicativo será instalado. Você está pronto para iniciar seu aplicativo a partir do Xbox!

## Considerações sobre a experiência do PWAs no Xbox

### Design para a "experiência de 3 metros"

O Xbox One é considerado uma "experiência de 3 metros", o que significa que seus usuários provavelmente ficarão com um mínimo de 10 metros de distância na tela. Assim, considere como seu aplicativo pode ser usado nessa distância em oposição à experiência tradicional do navegador da Web para área de trabalho com um mouse e um teclado. Para obter orientação de design e UX, confira [design para Xbox e TV](/windows/uwp/design/devices/designing-for-tv).

### Entender a "TV SafeZone"

Os fabricantes de televisão aplicarão uma ["zona segura"](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) em torno do conteúdo que pode recortar seu aplicativo. Por padrão, aplicamos uma borda segura ao seu aplicativo para fazer isso, no entanto, você pode garantir que seu aplicativo leve o tamanho da tela inteira chamando [`setDesiredBoundsMode`](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) e especificando [`useCoreWindow`](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode) :

```JavaScript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```

Para saber mais, confira a [`Windows.UI.ViewManagement`](/uwp/api/windows.ui.viewmanagement) documentação do namespace.

### Gerenciar o foco e a navegação XY

Os métodos de entrada do usuário para o Xbox são gamepad ou controle remoto, que usam um [sistema de navegação XY](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction), permitindo que o usuário mova o foco de controle para o controle movendo-se para cima, para baixo, para a esquerda e para a direita.

Assim, você desejará certificar-se de que seu aplicativo funciona bem com a navegação XY. Além disso, certifique-se de [desabilitar o *modo de mouse*](/windows/uwp/xbox-apps/how-to-disable-mouse-mode), que é ativado por padrão para aplicativos UWP (e provavelmente não se aplica à experiência do Xbox do seu aplicativo).

O código a seguir desativa o `mouse` modo e habilita a entrada do gamepad para gerar eventos de teclado dom:

```JavaScript
navigator.gamepadInputEmulation = "keyboard";
```

Como alternativa, você pode especificar `gamepad` , que também desliga o mouse, não gera eventos de teclado dom e permite que você use as APIs de gamepad padrão Web e/ou WinRT.

Para habilitar a navegação direcional, confira a [biblioteca TVJS](#tvjs), abordada a seguir.

### TVJS

[TVJS é uma coleção de bibliotecas auxiliares](https://github.com/Microsoft/TVHelpers) que facilitam a criação de aplicativos Web para a TV. Se você estiver criando um aplicativo Web hospedado que também será executado no Xbox, o TVJS pode ajudar a adicionar suporte à *navegação direcional*, além de oferecer vários controles que facilitam a interação com o conteúdo na TV.

A [navegação direcional](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) é um recurso TVJS que fornece navegação bidimensional automática nas páginas do aplicativo de TV. Com ele, não é necessário interceptar e manipular a navegação dentro das páginas do seu aplicativo ou para especificar explicitamente todos os destinos de foco válidos para cada elemento da interface do usuário. O tratamento automático de foco permite que os usuários possam navegar de uma maneira intuitiva e robusta.

Conforme o usuário navega pela interface do usuário do aplicativo com os botões de direção do controlador, o algoritmo de foco automático analisa o conjunto de alvos de foco em potencial, determina o próximo elemento para o qual se mover e define automaticamente o foco para esse elemento. Para determinar o próximo elemento, o algoritmo combina a entrada direcional, o histórico de foco anterior e o layout físico dos elementos da interface do usuário na página.

Para habilitar a navegação direcional, inclua a seguinte referência de script:

```HTML
<script src="directionalnavigation-1.0.0.0.js"></script>
```

Por padrão, somente `<a>` ,,, `<button>` e os `<input>` `<select>` `<textarea>` elementos podem ser focados. Para habilitar o foco em outros elementos, atribua um [TabIndex](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)válido.

```HTML
<div tabindex="0″>This div is eligible for focus</div>
```

Confira a documentação do [DirectionalNavigation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) para saber como alterar o elemento raiz, definir o foco inicial, substituir o próximo foco, otimizar controles para o foco, personalizar a entrada. Há também vários outros exemplos úteis.

## Media PWAs no Xbox

Se você estiver criando um PWA de reprodução de mídia para o Xbox One, lembre-se das seguintes considerações.

### Extensões de mídia criptografadas (EME) no navegador

O navegador Microsoft Edge no Xbox One não oferece suporte a [extensões de mídia criptografadas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) (EME). Se a mídia PWA a usa para o gerenciamento de direitos digitais (DRM), você não poderá executá-la a partir do navegador no Xbox. Em vez disso, crie um protótipo e teste-o como um [aplicativo Xbox One usando o PWABuilder ou o Visual Studio](#deploying-and-testing-pwas-on-xbox), conforme descrito acima. Você também pode executá-lo no navegador Microsoft Edge no Windows, onde há suporte total para EME.

### Integração com controles de transporte de mídia do sistema

Se seu aplicativo for um aplicativo de mídia, é importante que seu aplicativo responda aos controles de mídia iniciados pelo usuário por meio de botões na tela, [comandos de voz da Cortana](https://support.xbox.com/xbox-one/console/cortana-voice-commands), [controles de transporte de mídia do sistema](/windows/uwp/audio-video-camera/system-media-transport-controls) no painel de navegação ou aplicativos do Xbox e [Xbox One SmartGlass](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) em outros dispositivos. [Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) Dê uma olhada no controle do [MediaPlayer](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) na [biblioteca do TVJS](#tvjs), que se integra automaticamente a esses controles. Como alternativa, você pode [integrar-se manualmente com os controles de transporte de mídia do sistema](https://msdn.microsoft.com/windows/uwp/audio-video-camera/system-media-transport-controls).

### Criptografia de conteúdo do PlayReady

No momento da redação, a [ `cbcs` codificação do suporte é limitada](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) ao cliente PlayReady para Xbox One (versão 1709 ou superior). Se a mídia do seu PWA só oferecer suporte à criptografia *CBCs* , lembre-se de que a funcionalidade do seu aplicativo será provavelmente limitada (ou completamente indisponível) no Windows.



## Consulte também
[Vídeo de saliência do Sul](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video): um exemplo de aplicativo de vídeo para Xbox baseado em React.js e hospedado em um servidor Web.

[Projetando para Xbox e TV](/windows/uwp/design/devices/designing-for-tv): projete seu aplicativo da plataforma universal do Windows (UWP) para que ele tenha uma aparência boa e funcione bem em telas do Xbox One e da televisão.

[Práticas recomendadas do Xbox](/windows/uwp/xbox-apps/tailoring-for-xbox): Siga estas práticas recomendadas para personalizar seu aplicativo para Xbox One.

[PWAs na Microsoft Store](/microsoft-edge/progressive-web-apps-edgehtml/microsoft-store): Veja como (e por quê!) enviar seu PWA para a Microsoft Store.

[UWP no Xbox One](/windows/uwp/xbox-apps/): um guia completo para o desenvolvimento de aplicativos UWP para Xbox One.
