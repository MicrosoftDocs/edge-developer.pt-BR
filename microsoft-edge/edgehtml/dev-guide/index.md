---
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no Microsoft Edge.
title: O que há de novo no EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, devtools
ms.custom: RS5
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 15d3321e05f8a307d8014696f1ab78a8967f7129
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231391"
---
# Guia do desenvolvedor do Microsoft Edge

> [!TIP]
> Fizemos [parcerias](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) com outros navegadores e a Comunidade da Web na adoção de [documentos da Web do MDN](https://developer.mozilla.org/) como local definitivo para a documentação útil, não polarizada e independente de navegador para as tecnologias da Web atuais e emergentes baseados em padrões. Você pode encontrar detalhes sobre o suporte à API do EdgeHTML diretamente em cada página da [biblioteca MDN Web Reference](https://developer.mozilla.org/docs/Web). Visite o status da [plataforma](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) do Microsoft Edge para obter os recursos mais recentes com suporte no Microsoft Edge. 

## O que há de novo no EdgeHTML 18

EdgeHTML 18 inclui os seguintes recursos novos e atualizados fornecidos na versão atual da plataforma Microsoft Edge, a partir da atualização do [Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) (10/2018, Build 17763). Para alterações em compilações específicas do [Windows Insider](https://insider.windows.com/) Preview, consulte o [changelog do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) e [o que há de novo no EdgeHTML](./whats-new.md).

Aqui está o link permanente para a seguinte lista de alterações: [https://aka.ms/devguide_edgehtml_18](./whats-new.md) .

## Recursos novos e atualizados

### Políticas de reprodução automática

Com a atualização do Windows 10 de outubro de 2018, o Microsoft Edge fornece aos clientes a capacidade de personalizar suas preferências de navegação em sites que a reprodução de mídia em reprodução automática com som para minimizar distrações na Web e conservar a largura de banda. Os usuários podem personalizar o comportamento de mídia com os controles de reprodução automática global e por site. Além disso, o Microsoft Edge automaticamente suprime a reprodução automática de mídia em guias de plano de fundo.

Confira o guia de [políticas de reprodução automática](./browser-features/autoplay-policies.md) para obter detalhes e práticas recomendadas para garantir uma boa experiência do usuário com mídia hospedada em seu site.

### Melhorias Chakra

EdgeHTML 18 inclui atualizações para o mecanismo JavaScript Chakra para dar suporte a novos recursos ES e WASM, além de melhorias de desempenho e interoperabilidade. Confira as [notas de versão do ChakraCore 1,11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) para obter detalhes.

### Atualizações de CSS

Fizemos mais progressos em nossa implementação de [mascaramento de CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) experimental (por trás do sinalizador *habilitar máscara de CSS* ) com suporte adicional para [Mask-Composite](https://developer.mozilla.org/docs/Web/CSS/mask-composite), [Mask-position](https://developer.mozilla.org/docs/Web/CSS/mask-position)e [Mask-REPEAT](https://developer.mozilla.org/docs/Web/CSS/mask-repeat). Para compatibilidade com o site, o Microsoft Edge também oferece suporte a:- *WebKit-* Properties:-WebKit-Mask,-WebKit-Mask-Composite,-WebKit-Mask-Image,-WebKit-Mask-position,-WebKit-Mask-position-x,-WebKit-Mask-position-y,-WebKit-Mask-REPEAT,-WebKit-Mask-size

Além disso, o Microsoft Edge agora tem suporte para suporte parcial e de [quebra de estouro](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap
) para [sobrescroll-Behavior](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) ( `auto` e `contain` valores).

### Ferramentas de Desenvolvedor

A atualização mais recente do Microsoft Edge DevTools adiciona uma série de conveniências à interface do usuário e nos bastidores, incluindo novos painéis dedicados para trabalhadores de serviço e armazenamento, ferramentas de pesquisa de arquivos de origem no depurador e novos domínios de protocolo de DevTools para a depuração de estilo/layout e APIs do console.

[Devtools na atualização mais recente do Windows 10 (EdgeHTML 18)](../devtools-guide/whats-new.md) tem todos os detalhes.

### Ouvindo seus comentários

Ouvimos seus comentários e implementamos o suporte para várias APIs solicitadas no EdgeHTML 18, incluindo o [`DataTransfer.setDragImage()`](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) método usado para definir uma imagem personalizada ao arrastar e soltar, e [`secureConnectionStart`](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart) uma propriedade da API de tempo de recurso de desempenho, que pode ser usada para retornar um carimbo de data/hora imediatamente antes de o navegador iniciar o processo de handshake para proteger a conexão atual. 

Além disso, ninguém gosta de enumerar a coleção Attributes; portanto, adicionamos suporte para [`Element.getAttributeNames`](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) retornar os nomes de atributo do elemento como uma matriz de cadeias de caracteres, bem como, [`Element.toggleAttribute`](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) para alternar um atributo booliano (removendo se presente e adicionando se não).

### Aplicativos Web progressivos

#### Script em segundo plano da vida útil

Os aplicativos JavaScript do Windows 10 (aplicativos Web em execução em um processo de *WWAHost.exe* ) agora dão suporte a um script de tela de fundo por aplicativo opcional, que é iniciado antes que os modos de exibição sejam ativados e executados durante a duração do processo. Com isso, você pode monitorar e modificar navegações, acompanhar o estado entre navegações, monitorar erros de navegação e executar o código antes de ativar os modos de exibição. 

Quando especificado como [`StartPage`](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) no manifesto do [aplicativo](/uwp/schemas/appxpackage/appx-package-manifest), cada um dos modos de exibição do aplicativo (Windows) são expostos ao script como instâncias da nova [`WebUIView`](/uwp/api/windows.ui.webui.webuiview) classe, fornecendo os mesmos eventos, propriedades e métodos como um [WebView](/uwp/api/windows.web.ui.iwebviewcontrol)geral (Win32). Seu script pode ouvir o [`NewWebUIViewCreated`](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) evento para interceptar o controle da navegação para um novo modo de exibição:

```JavaScript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```

 Qualquer ativação do aplicativo com o script de plano de fundo como o dependerá do `StartPage` próprio script para navegação.

#### Dimensionamento de texto

A atualização do Windows 10 de outubro de 2018 introduz a configuração [*criar texto maior*](/windows/uwp/design/input/text-scaling#user-experience) para melhorar a acessibilidade do usuário final, e o PWAs instalado no Windows (além da UWP e na maioria dos aplicativos da área de trabalho) agora oferece suporte a esse recurso automaticamente. Para os controles PWAs e WebView, a escala de texto funciona da mesma maneira que a escala de DPI. Se um usuário alterar a escala de texto e a escala de DPI, o resultado será o produto dos dois.

 Para obter orientação de design, confira a guia UWP de [dimensionamento de texto](/windows/uwp/design/input/text-scaling) no *centro de desenvolvimento do Windows*.

### Atualizações do trabalho do serviço 

Para um atualizador sobre quais são os funcionários do serviço e como eles funcionam, confira o resumo da [API do serviço de trabalho]( https://developer.mozilla.org/docs/Web/API/Service_Worker_API) escrito por nossos parceiros em MDN.  Havia várias atualizações para os funcionários do serviço de suporte do Microsoft Edge no EdgeHTML 18. O `fetchEvent` trabalhador permite que o trabalhador do serviço use [`preloadResponse`]( https://developer.mozilla.org/docs/Web/API/FetchEvent) para prometer uma resposta e o [`resultingClientId`]( https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) para retornar a ID do cliente que o trabalhador do serviço atual está controlando.  
A [`NavigationPreloadManager`]( https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) interface fornece métodos para gerenciar o pré-carregamento de recursos, permitindo que você faça uma solicitação em paralelo enquanto um trabalho de serviço está sendo inicializado, evitando qualquer atraso de tempo. Dê uma olhada nas [Propriedades de API recém suportadas](#new-apis-in-edgehtml-18) para a lista de métodos e propriedades de pré-carregamento do trabalho do serviço. 

### Autenticação Web

O Microsoft Edge agora inclui [suporte sem prefixo para a nova API de autenticação na Web](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge/) (conhecida como [webauthn](https://w3c.github.io/webauthn/)). A autenticação da Web fornece uma solução aberta, dimensionável e interoperável para simplificar a autenticação, permitindo experiências de usuário melhores e mais seguras ao substituir senhas por credenciais de alta segurança associadas a hardware. A implementação no Microsoft Edge permite o uso do [Windows Hello](https://www.microsoft.com/windows/windows-hello) permitindo que os usuários entrem com seus respectivos face, impressão digital ou PIN, além de [autenticadores externos](https://fidoalliance.org) , como chaves de segurança do FIDO2 ou chaves de segurança do Fido U2F, para autenticar com segurança os sites.

Para obter mais informações, vá para a postagem do blog [apresentando autenticação da Web no Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).

### WebDriver

O WebDriver agora é um [recurso de demanda do Windows](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (função sob demanda) que torna mais fácil do que nunca automatizar o teste no Microsoft Edge e obter a versão certa para o seu dispositivo. Você não precisará mais fazer correspondência entre a compilação/ramificação/flavor manualmente ao instalar o WebDriver, seu [WebDriver](https://www.w3.org/TR/webdriver) será atualizado automaticamente para corresponder a qualquer nova atualização do Windows 10. 

Você pode instalar o WebDriver ativando o modo de desenvolvedor ou instalá-lo como autônomo acessando configurações > aplicativos > aplicativos & recursos > gerenciar recursos opcionais. Para obter mais informações, confira o [anúncio do WebDriver no site do blog do Windows](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).

### Propriedades de notificação da Web
Quatro novas propriedades agora têm suporte para notificações da Web: [`actions`](https://developer.mozilla.org/docs/Web/API/notification/actions) ,, [`badge`](https://developer.mozilla.org/docs/Web/API/notification/badge) [`image`](https://developer.mozilla.org/docs/Web/API/notification/image) e `maxActions` para aprimorar nossa capacidade de criar notificações na Web que sejam compatíveis com os sistemas de notificação existentes, enquanto a opção permanece independente da plataforma.

### WebView

#### Profissionais de serviço
Os [profissionais do serviço](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) agora têm suporte no controle WebView, além do navegador Microsoft Edge e dos aplicativos JavaScript do Windows 10. Todas as versões dos funcionários do serviço de suporte do Microsoft Edge WebView ([PWA](../hosting/webview/index.md), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)), no entanto, lembre-se de que a [API de envio](https://developer.mozilla.org/docs/Web/API/Push_API) ainda não está disponível para as versões UWP e Win32.

as arquiteturas de aplicativos x64 exigem pacotes *neutros* (qualquer CPU) ou *x64* , pois os operadores de serviço não são compatíveis com processos WOW64. (Para conservar espaço em disco, a versão WoW das DLLs necessárias não está incluída nativamente no Windows.)

#### Atualizações da WebView do Win32

O EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) para aplicativos da área de trabalho do Windows (Win32) foi atualizado com vários novos recursos, incluindo a capacidade de injetar um script após a carga da página antes de todos os outros scripts na página serem executados ( [`AddInitializeScript`](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript) ) e saber quando um WebViewControl em particular recebe ou perde o foco ( [`GotFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [`LostFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus) ).

Além disso, agora você pode criar um novo WebViewControl como a janela aberta [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) . O [`NewWindowRequested`](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) evento ainda notifica um aplicativo quando o script está dentro da janela chamadas do WebViewControl. Open como ele sempre tem, mas com EdgeHTML 18, ele [`NewWindowRequestedEventArgs`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) inclui a capacidade de fazer um adiamento ( [`GetDeferral`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral) ) para definir um novo WebViewControl ( [`NewWindow`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow) ) como o destino para a janela. Open:

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

Por fim, os usuários avançados podem perceber a aparência do *Visualizador da Web de aplicativo da área de trabalho* (anteriormente chamado de *Win32WebViewHost*), um aplicativo de sistema interno que representa o WebView Win32, nos seguintes locais:
- Na *central de ações do Windows 10*. A origem dessas notificações deve ser entendida como uma WebView hospedada em um aplicativo Win32.
- Na interface do usuário das configurações de acesso a dispositivo (*configurações->privacidade->câmera/local/microfone*). A desabilitação de qualquer uma dessas configurações nega o acesso de todas as webviews hospedadas em aplicativos Win32.

![Configuração de acesso de dispositivo do visualizador Web App para área de trabalho](./media/desktop-app-web-viewer.png)

## Recursos preteridos

### Filtro XSS agora desativado

Com o EdgeHTML 18, desativamos o filtro XSS no Microsoft Edge. Nossos clientes permanecem protegidos graças a padrões modernos, como o [CSP (política de segurança de conteúdo)](https://developer.mozilla.org/docs/Web/HTTP/CSP), que fornecem mecanismos mais avançados, de melhor forma e seguros para se proteger contra ataques de injeção de conteúdo, com alta compatibilidade entre navegadores modernos.

## Novas APIs no EdgeHTML 18

Confira a lista completa de APIs novas em EdgeHTML 18. Elas são listadas no formato [nome da interface]. [nome da API].

> [!NOTE] 
> Embora as seguintes APIs sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento e estar oculto atrás de um sinalizador experimental. Consulte o  [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para obter a palavra oficial sobre o suporte ao recurso.

<iframe height='580' scrolling='no' title='Novas APIs no EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Veja a caneta <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> novas APIs no EdgeHTML 18 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>

## Versões anteriores do EdgeHTML

[EdgeHTML 13/Build do Windows 10586 (11/2015)](./whats-new/edgehtml-13.md)

[EdgeHTML 14/Build do Windows 14393 (8/2016)](./whats-new/edgehtml-14.md)

[EdgeHTML 15/Build do Windows 15063 (4/2017)](./whats-new/edgehtml-15.md)

[EdgeHTML 16/Build do Windows 16299 (10/2017)](./whats-new/edgehtml-16.md)

[EdgeHTML 17/Build do Windows 17134 (04/2018)](./whats-new/edgehtml-17.md)
