---
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no Microsoft Edge.
title: Novidades no EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor, devtools
ms.custom: RS5
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6b53163115ad7db8e5b792cadda0c59b93b6711b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399222"
---
# <a name="microsoft-edge-developer-guide"></a>Guia do Desenvolvedor do Microsoft Edge  

> [!TIP]
> Fizemos parceria [](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) com outros navegadores e com a comunidade da Web na adoção de [Documentos Web do MDN](https://developer.mozilla.org/) como o local definitivo para a documentação agnóstica útil, sembias do navegador para tecnologias Web baseadas em padrões atuais e emergentes.  Você pode encontrar detalhes sobre o suporte à API EdgeHTML diretamente em cada página da biblioteca de referência [da Web MDN.](https://developer.mozilla.org/docs/Web)  Visite o status da [Plataforma do](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) Microsoft Edge para ver os recursos mais recentes com suporte no Microsoft Edge.  

## <a name="whats-new-in-edgehtml-18"></a>Novidades no EdgeHTML 18  

O EdgeHTML 18 inclui os seguintes recursos novos e atualizados enviados na versão atual da plataforma Microsoft Edge, a partir da Atualização de Outubro de [2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) \(10/2018, Build 17763\).  Para alterações em builds [específicos do Windows Insider](https://insider.windows.com) Preview, consulte o [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) e [Novidades no EdgeHTML](./whats-new.md).  

Aqui está o permalink para a seguinte lista de alterações: [https://docs.microsoft.com/microsoft-edge/dev-guide](#new-apis-in-edgehtml-18) .  

## <a name="new-and-updated-features"></a>Recursos novos e atualizados  

### <a name="autoplay-policies"></a>Políticas de reprodução automática  

Com a Atualização de Outubro de 2018 do Windows 10, o Microsoft Edge oferece aos clientes a capacidade de personalizar suas preferências de navegação em sites que reprodução automática de mídia com som para minimizar distrações na Web e economizar largura de banda.  Os usuários podem personalizar o comportamento de mídia com controles de reprodução automática globais e por site.  Além disso, o Microsoft Edge suprime automaticamente a reprodução automática de mídia em guias em segundo plano.  

Confira o guia [Políticas de Reprodução](./browser-features/autoplay-policies.md) Automática para obter detalhes e práticas recomendadas para garantir uma boa experiência do usuário com mídia hospedada em seu site.  

### <a name="chakra-improvements"></a>Melhorias de Chakra  

O EdgeHTML 18 inclui atualizações para o mecanismo JavaScript de Chakra para dar suporte a novos recursos ES e WASM, além de melhorias de desempenho e interoperabilidade.  Confira as [Notas de Versão do ChakraCore 1.11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) para obter detalhes.  

### <a name="css-updates"></a>Atualizações CSS  

Fizemos mais progressos em nossa implementação experimental de [mascaramento CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) \(atrás do sinalizador Habilitar Mascaramento *CSS\)* com suporte adicionado para máscara [composta,](https://developer.mozilla.org/docs/Web/CSS/mask-composite) [posição de](https://developer.mozilla.org/docs/Web/CSS/mask-position)máscara e repetição [de máscara.](https://developer.mozilla.org/docs/Web/CSS/mask-repeat)  Para compatibilidade com o site, o Microsoft Edge também oferece suporte às seguintes propriedades *-webkit-mask,* -webkit-mask-composite, -webkit-mask-image, -webkit-mask-position, -webkit-mask-position-x, -webkit-mask-position-y, -webkit-mask-repeat, -webkit-mask-size.  

Além disso, o Microsoft Edge agora tem suporte para [excesso de wrap](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap) e suporte parcial para [overscroll-behavior](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) \( `auto` and `contain` values\).  

### <a name="developer-tools"></a>Ferramentas de Desenvolvedor  

A atualização mais recente do Microsoft Edge DevTools adiciona uma série de conveniências à interface do usuário e sob o capa, incluindo novos painéis dedicados para Funcionários de Serviço e Armazenamento, ferramentas de pesquisa de arquivo de origem no Depurador e novos domínios do Protocolo DevTools de Borda para APIs de depuração de estilo/layout e console.  

[O DevTools na atualização mais recente do Windows 10 (EdgeHTML 18)](./whats-new.md) tem todos os detalhes.  

### <a name="listening-to-your-feedback"></a>Ouvir seus comentários  

Escutamos seus comentários e implementamos o suporte para várias APIs solicitadas no EdgeHTML 18, incluindo o [método DataTransfer.setDragImage()](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) usado para definir uma imagem personalizada ao arrastar e soltar e [secureConnectionStart](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart), uma propriedade da API de Tempo de Recursos de Desempenho, que pode ser usada para retornar um data/hora imediatamente antes do navegador iniciar o processo de handshake para proteger a conexão atual.  

Além disso, ninguém gosta de enumerar a coleção de atributos, portanto, adicionamos suporte a [Element.getAttributeNames](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) para retornar os nomes de atributo do elemento como uma Matriz de cadeias de caracteres, bem [como, Element.toggleAttribute](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) para alternar um atributo booleano \(removendo se presente e adicionando se não\).  

### <a name="progressive-web-apps"></a>Aplicativos Web progressivos  

#### <a name="lifetime-background-script"></a>Script em segundo plano de vida  

Os aplicativos JavaScript do Windows 10 \(aplicativos Web em execução em um processo\) agora suportam um script de plano de fundo opcional por aplicativo que começa antes de qualquer exibição ser ativado e executado durante a duração do `WWAHost.exe` processo.  Com isso, você pode monitorar e modificar navegaçãos, controlar o estado em navegação, monitorar erros de navegação e executar código antes que os exibições sejam ativados.  

Quando especificado como [StartPage](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) no manifesto do [aplicativo,](/uwp/schemas/appxpackage/appx-package-manifest)cada uma das exibições do aplicativo \(windows\) é exposta ao script como instâncias da nova [classe WebUIView,](/uwp/api/windows.ui.webui.webuiview) fornecendo os mesmos eventos, propriedades e métodos como um [WebView](/uwp/api/windows.web.ui.iwebviewcontrol)geral \(Win32\) .  Seu script pode escutar o [evento NewWebUIViewCreated](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) para interceptar o controle da navegação para um novo modo de exibição:  

```javascript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```  

 Qualquer ativação de aplicativo com o script em segundo plano como `StartPage` o dependerá do próprio script para navegação.  

#### <a name="text-scaling"></a>Dimensionamento de texto  

A Atualização do Windows 10 de outubro [](/windows/uwp/design/input/text-scaling#user-experience) de 2018 apresenta a configuração Tornar o texto maior para acessibilidade aprimorada do usuário final, e os PWAs instalados no Windows \(além de UWP e a maioria dos aplicativos de área de trabalho\) agora suportam esse recurso automaticamente.  Para controles PWAs e WebView, a escala de texto funciona da mesma forma que o dimensionamento de DPI.  Se um usuário altera a escala de texto e a escala DPI, o resultado é o produto dos dois.  

 Para obter orientações de design, confira o guia UWP de [dimensionamento](/windows/uwp/design/input/text-scaling) de texto no *Centro de Desenvolvimento do Windows.*  

### <a name="service-worker-updates"></a>Atualizações do Service Worker  

Para uma atualização sobre o que são os Funcionários do Serviço e como eles funcionam, confira o resumo da [API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) do Trabalhador do Serviço escrito por nossos parceiros no MDN.  Houve várias atualizações para Os Funcionários de Serviço de Suporte do Microsoft Edge no EdgeHTML 18.  O permite que o Service Worker use preloadResponse para promessa de uma resposta e o `fetchEvent` [ResultingClientId](https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) para retornar a ID do Cliente que o funcionário de serviço atual está controlando. [](https://developer.mozilla.org/docs/Web/API/FetchEvent)  
A interface [NavigationPreloadManager](https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) fornece métodos para gerenciar o pré-carregamento de recursos, permitindo que você faça uma solicitação em paralelo enquanto um funcionário de serviço está inicializando, evitando qualquer atraso de tempo.  Confira as propriedades [da API recém-suportadas](#new-apis-in-edgehtml-18) para a lista de métodos e propriedades de pré-carregamento do Service Worker.  

### <a name="web-authentication"></a>Autenticação Web  

O Microsoft Edge agora inclui suporte não [pré-corrigido](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge) para a nova API de Autenticação da Web \(também conhecida como [WebAuthN](https://w3c.github.io/webauthn)\).  A Autenticação Web fornece uma solução aberta, escalonável e interoperável para simplificar a autenticação, permitindo experiências de usuário melhores e mais seguras substituindo senhas por credenciais mais fortes vinculadas a hardware.  A implementação no Microsoft Edge permite que o uso do [Windows Hello](https://www.microsoft.com/windows/windows-hello) permita que os usuários entrem com seu rosto, impressão digital ou PIN, além de autenticadores [externos,](https://fidoalliance.org) como Chaves de Segurança FIDO2 ou Chaves de Segurança do FIDO U2F, para autenticar com segurança os sites.  

Para obter mais informações, vá para a postagem do blog [Apresentando a autenticação da Web no Microsoft Edge.](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge)  

### <a name="webdriver"></a>WebDriver  

O WebDriver agora é um Recurso do [Windows](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) sob Demanda \(FoD\) tornando mais fácil do que nunca automatizar testes no Microsoft Edge e obter a versão certa para seu dispositivo.  Você não precisará mais corresponder ao build/branch/flavor manualmente ao instalar o WebDriver, o [WebDriver](https://www.w3.org/TR/webdriver) será atualizado automaticamente para corresponder a todas as novas atualizações do Windows 10.  

Você pode instalar o WebDriver a partir do Modo de Desenvolvedor **** ou instalá-lo como autônomo, indo para Configurações  >  **Aplicativos**  >  **aplicativos & recursos Gerenciar**recursos  >  **opcionais**.  Para obter mais informações, confira o [comunicado do WebDriver no site do Blog do Windows.](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand)  

### <a name="web-notification-properties"></a>Propriedades de Notificação da Web  

Agora, há suporte para quatro novas propriedades para notificações da  [Web:](https://developer.mozilla.org/docs/Web/API/notification/actions) [ações,](https://developer.mozilla.org/docs/Web/API/notification/badge) [selo,](https://developer.mozilla.org/docs/Web/API/notification/image)imagem e , melhorando nossa capacidade de criar notificações na Web compatíveis com sistemas de notificação existentes, enquanto permanecem independentes da  `maxActions` plataforma.  

### <a name="webview"></a>WebView  

#### <a name="service-workers"></a>Profissionais de serviço  

[Os funcionários](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) de serviço agora têm suporte no controle WebView, além do navegador do Microsoft Edge e aplicativos JavaScript do Windows 10.  Todos os sabores do Webview do Microsoft Edge \([PWA,](/microsoft-edge/hosting/webview) [UWP,](/uwp/api/Windows.UI.Xaml.Controls.WebView) [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)\) suportam os funcionários de serviço, no entanto, lembre-se de que a [API push](https://developer.mozilla.org/docs/Web/API/Push_API) ainda não está disponível para as versões UWP e Win32.  

As arquiteturas de aplicativo x64 exigem pacotes Neutro \(Qualquer CPU\) ou x64, pois os funcionários do serviço não têm suporte em processos WoW64.  \(Para conservar o espaço em disco, a versão WoW das DLLs necessárias não está incluída de forma nativa no Windows.\)  

#### <a name="win32-webview-updates"></a>Atualizações do Win32 WebView  

Os aplicativos edgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) para área de trabalho do Windows \(Win32\) foram atualizados com vários novos recursos, incluindo a capacidade de injetar scripts no carregamento da página antes que quaisquer outros scripts na página sejam executados \([AddInitializeScript](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript)\) e saber quando um WebViewControl específico recebe ou perde o foco \([GotFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [LostFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus)\).  

Além disso, agora você pode criar um novo WebViewControl como a janela aberta de [window.open](https://developer.mozilla.org/docs/Web/API/Window/open).  O evento [NewWindowRequested](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) ainda notifica um aplicativo quando um script dentro da janela de chamadas WebViewControl.open como sempre fez, mas com o EdgeHTML 18 seu [NewWindowRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) inclui a capacidade de fazer um adiamento \([GetDeferral](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral)\) para definir um novo WebViewControl \([NewWindow](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow)\) como o destino para a janela.open:  

```csharp
WebViewControlProcess wvProc;
WebViewControl webView;

void OnWebViewControlNewWindowRequested(WebViewControl sender, WebViewControlNewWindowRequestedEventArgs args)
{

    if (args.Uri.Domain == "mydomain.com")
    {
        using deferral = args.GetDeferral();
        args.NewWindow = await wvProc.CreateWebViewControlAsync(
            parentWindow, targetWebViewBounds);
        deferral.Complete();
    }
    else
    {
        // Prevent WebView from launching in the default browser.
        args.Handled = true;
    }
}

String htmlContent = "<html><script>window.open('http://mydomain.com')</script><body></body></html>";

webView.NavigateToString(htmlContent);
```  

Por fim, os usuários de energia podem notar a aprovação do Visualizador da Web de Aplicativos de Área de Trabalho \(anteriormente chamado Win32WebViewHost\), um aplicativo de sistema interno que representa o WebView do Win32, nos seguintes locais:  

*   No Centro de Ações do Windows 10.  A origem dessas notificações deve ser compreendida como de um WebView hospedado de um aplicativo Win32.  
*   Na interface do usuário das configurações de acesso do dispositivo \( `Settings`  >  `Privacy`  >  `Camera/Location/Microphone` \).  Desabilitar qualquer uma dessas configurações nega o acesso de todos os WebViews hospedados em aplicativos Win32.  

![Configuração de acesso de dispositivo do Visualizador da Web do Aplicativo da Área de Trabalho](./media/desktop-app-web-viewer.png)  

## <a name="deprecated-features"></a>Recursos preterido  

### <a name="xss-filter-now-retired"></a>Filtro XSS agora retirado  

Com o EdgeHTML 18, estamos retirando o filtro XSS no Microsoft Edge.  Nossos clientes permanecem protegidos graças a padrões modernos, como a Política de Segurança de Conteúdo [(CSP),](https://developer.mozilla.org/docs/Web/HTTP/CSP)que fornecem mecanismos mais poderosos, performantes e seguros para proteger contra ataques de injeção de conteúdo, com alta compatibilidade em navegadores modernos.  

## <a name="new-apis-in-edgehtml-18"></a>Novas APIs no EdgeHTML 18  

Confira a lista completa de novas APIs no EdgeHTML 18.  Eles estão listados no formato de [nome da interface]. [nome da api].  

> [!NOTE] 
> Embora as APIs a seguir sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento e oculto atrás de um sinalizador experimental.  Consulte o  [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para o suporte oficial do word on feature.  

<iframe height='580' scrolling='no' title='Novas APIs no EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulte as APIs de Caneta <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> Novas na BordaHTML 18 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) em </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

## <a name="previous-edgehtml-releases"></a>Versões anteriores do EdgeHTML  

[EdgeHTML 13 / build do Windows 10586 (11/2015)](./whats-new/edgehtml-13.md)  

[EdgeHTML 14 / Build do Windows 14393 (8/2016)](./whats-new/edgehtml-14.md)  

[EdgeHTML 15 / build do Windows 15063 (4/2017)](./whats-new/edgehtml-15.md)  

[EdgeHTML 16 / build do Windows 16299 (10/2017)](./whats-new/edgehtml-16.md)  

[EdgeHTML 17 / Build do Windows 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)  
