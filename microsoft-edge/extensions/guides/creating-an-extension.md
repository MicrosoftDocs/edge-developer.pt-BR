---
description: Saiba como criar uma extensão do Microsoft Edge
title: Criando uma extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683648"
---
# Criando uma extensão do Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Neste guia, aprenda a criar uma extensão para o Microsoft Edge.  Este exemplo de extensão permite manipular um CSS específico para páginas [docs.Microsoft.com][MicrosoftDocs] , incluindo a criação de um arquivo de manifesto, a interface do usuário e scripts de tela de fundo e de conteúdo.  

:::image type="complex" source="../media/color-changer_header.png" alt-text="O corpo do Docs.microsoft.com é alterado para azul":::
   O corpo do Docs.microsoft.com é alterado para azul
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

Este tutorial pressupõe que você tenha noções básicas sobre o que é uma extensão de navegador e como ela funciona.  Para obter mais imformation sobre os blocos de construção para extensões, consulte [anatomia de uma extensão][MDNAnatomyExtension].  

Baixe o código para o [exemplo completo no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Criando o arquivo de manifesto  

Para começar, crie um diretório para a sua extensão e nomeie-o `color-changer` .  

Na `color-changer` pasta, crie um arquivo chamado `manifest.json` .  O `manifest.json` arquivo é necessário para todas as extensões e fornece informações importantes para a extensão, variando do nome da extensão às permissões.  

> [!NOTE] 
> Este guia o orienta através de todas as chaves de manifesto que você deve usar neste guia, mas para obter uma lista de todas as chaves de manifesto recomendadas e compatíveis, consulte [chaves de manifesto com suporte][ExtensionsApisupportManifestKeys].  

Dentro `manifest.json` , adicione o código a seguir.  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### Definições da chave do manifesto  

| Chave | Detalhes |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | O nome da extensão.  |  
| [autor][MDNManifestjsonAuthor] | O autor da extensão.  |  
| [version][MDNManifestjsonVersion] | O número da versão da extensão.  |  
| [description][MDNManifestjsonDescription] | A descrição da extensão exibida na seção sobre do menu extensão no Microsoft Edge.  |  
| [Elas][MDNManifestjsonPermissions] | Uma matriz de cadeias de caracteres que solicitam permissões para a extensão.  Para sua extensão, você está solicitando permissões para ver os sites visitados \ ("guias" \) e para atualizar o conteúdo em URLs correspondentes a " `*://docs.microsoft.com/*` ".  |  
| [browser_action][MDNManifestjsonBrowserAction] | Contém as informações para um ícone. O ícone é colocado na barra de ferramentas do Microsoft Edge, à direita da barra de endereços.  |  

#### definições de chave browser_action  

| Chave | Detalhes |  
|:--- |:--- |  
| `default_icon` | O ícone usado na barra de ferramentas.  |  
| `default_title` | O texto que é exibido quando um usuário passa o mouse sobre o ícone na barra de ferramentas.  |  
| `default_popup` | O caminho para o arquivo HTML da janela pop-up.  |  

Agora que você criou o arquivo de manifesto, precisa de uma interface do usuário para a extensão.  

## Criando o pop-up  

Para sua extensão, crie um pop-up para a interface do usuário, como abaixo.  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="A interface pop-up da extensão":::
   A interface pop-up da extensão
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

Crie um arquivo chamado `popup.html` na raiz da `color-changer` pasta.  Cole o código a seguir em `popup.html` .  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

No `popup.html` , você cria um título, um parágrafo e três botões \ (AliceBlue, Cornsilk e reset \).  

Agora, crie uma pasta chamada `css` e dentro crie um arquivo chamado `styles.css` .  Adicione os estilos abaixo.  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

Esse CSS dá à nossa extensão alguns estilos básicos.  Sinta-se à vontade para adicionar mais estilos para personalizar a extensão.  

Em seguida, você deve criar o arquivo JavaScript que interage com o pop-up.  Crie uma `js` pasta e um arquivo nomeado `popup.js` dentro.  Atualize `popup.js` com o código a seguir.  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

No `popup.js` , a API de [guias][MDNApiTabs] permite que você interaja com as guias do navegador e injeta scripts e estilos no conteúdo da página.  Usando o método [Tabs. insertCSS ()][MDNApiTabsInsertcss] , você INJETA a CSS especificada na página que altera o cabeçalho em [docs.Microsoft.com][MicrosoftDocs] para uma cor diferente quando o botão especificado é clicado.  

Agora que você tem a funcionalidade pop-up básica, adicione ícones à extensão.  

## Adicionando ícones  

Os ícones são usados para representar a extensão na barra de ferramentas do navegador, o menu extensões e outros locais.  Baixe os [ícones da extensão no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]. Para obter mais informações sobre ícones de extensão no Microsoft Edge, consulte [Guia de design][ExtensionsGuidesDesignIcons].  

Depois de baixar os ícones de extensão, salve os ícones em uma `images` pasta dentro `color-changer` .  

O ícone que aparece na barra de ferramentas é definido usando-se `default_icon` dentro da chave [browser_action][MDNManifestjsonBrowserAction] , que você já adicionou ao arquivo de manifesto em uma seção anterior.  

A `icons` chave define quais ícones devem ser usados nos menus de configurações de extensões.  Abaixo, você está especificando vários ícones com diferentes tamanhos para fazer uma conta com diferentes resoluções de tela.  O nome dos ícones `25` e `48` a altura em pixels dos ícones.  

No arquivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , inclua uma chave de nível superior para `icons` .  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### Definições da chave do manifesto  

| Chave | Detalhes |  
|:--- |:--- |  
| [ícones][MDNManifestjsonIcons] | Os ícones da extensão com pares chave-valor do tamanho da imagem em `px` e o caminho da imagem em relação ao diretório raiz da extensão. |  

> [!NOTE]
> Use os ícones nomeados `inactive##.png` localizados na pasta imagens mais adiante neste guia.  

## Testando a extensão  

Agora que você adicionou a interface do usuário e os ícones criados, teste a extensão.  Siga as etapas para [Adicionar uma extensão][ExtensionsGuidesAddingRemovingExtensionsAdding] ao Microsoft Edge.  Depois, retorne a este guia.  

Depois de adicionar a extensão, navegue até qualquer página do [docs.Microsoft.com][MicrosoftDocs] .  Você deve ver o pop-up a seguir depois de clicar na ação do navegador.  A cor do corpo da [docs.Microsoft.com][MicrosoftDocs] também deve mudar de cor.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="O cabeçalho Docs.microsoft.com mudou para AliceBlue":::
         O cabeçalho Docs.microsoft.com mudou para AliceBlue :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="O cabeçalho Docs.microsoft.com mudou para Cornsilk":::
         O cabeçalho Docs.microsoft.com mudou para Cornsilk :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

Se você encontrar erros ou funcionalidades que não funcionam, consulte o guia de [extensões de depuração][ExtensionsGuidesDebuggingExtensions] ou baixe a [amostra completa no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Adicionando conteúdo e scripts em segundo plano  

Siga um passo adiante e adicione lógica para desabilitar a extensão de trabalhar em páginas fora do domínio do [docs.Microsoft.com][MicrosoftDocs] .  

Primeiro, você deve criar um [script de conteúdo][MDNContentScripts].  Em seguida, você deve criar scripts de conteúdo que são executados no contexto de uma determinada página da Web, podem acessar o conteúdo de uma página da Web e podem se comunicar com scripts em segundo plano.  No seu `js` diretório, crie um arquivo denominado `content.js` e adicione o código a seguir.  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

Esse script Obtém a URL da página atual `document.location.href` e verifica se a página atual está no domínio [docs.Microsoft.com][MicrosoftDocs] .  Se a página não estiver no domínio [docs.Microsoft.com][MicrosoftDocs] \ (por exemplo, [https://www.bing.com/][|::ref1::|] \), os caminhos para os ícones inativos \ (ícones em cinza \) serão enviados para o script em segundo plano usando o [tempo de execução. SendMessage ()][MDNApiRuntimeSendmessage].  

Você deve atualizar o arquivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] para incluir a chave a seguir `content_scripts` .  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### Definições da chave do manifesto  

| Chave | Detalhes |  
|:--- |:---- |  
| [content_scripts][MDNManifestjsonContentScripts] | Contém as informações sobre quais scripts de conteúdo o navegador deve carregar. |  

#### definições de chave content_scripts  

| Chave | Detalhes |  
|:--- |:---- |  
| `matches` \ (obrigatório \) | O padrão de URL correspondente antes de carregar o script de conteúdo. |  
| `js` | O script que deve ser carregado em URLs correspondentes. |  
| `run_at` | Especifica onde os arquivos JavaScript da `js` chave são injetados. |  

Em seguida, você deve criar um [script de tela de fundo][MDNAnatomyExtensionBackgroundScripts].  Os scripts em segundo plano são executados em segundo plano do navegador, executados independentemente do tempo de vida de uma página da Web ou janela do navegador e podem se comunicar com scripts de conteúdo.  

Na sua `js` pasta, crie um arquivo denominado `background.js` e adicione o código a seguir.  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

O método [Runtime. onMessage][MDNApiRuntimeOnmessage] escuta o [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] do script de conteúdo.  Se o domínio da página não for [docs.Microsoft.com][MicrosoftDocs], o método [BrowserAction. SetIcon ()][MDNApiBrowseractionSeticon] define os caminhos dos ícones para as imagens inativas.  

O script também desabilita a ação do navegador \ ([BrowserAction. Disable][MDApiBrowseractionDisable]\), para que os usuários não sejam capazes de clicar na ação do navegador fora de uma página do [docs.Microsoft.com][MicrosoftDocs] .  

Você deve adicionar o script de tela de fundo ao arquivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .  Adicione a chave a seguir `background` ao seu manifesto.  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### Definições da chave do manifesto  

| Chave | Detalhes|  
|:--- |:--- |  
| [tela de fundo][MDNManifestjsonBackground] | Contém os scripts em segundo plano. |  

#### definições da chave em segundo plano  

| Chave | Detalhes |  
|:--- |:--- |  
| `scripts` | O caminho para um arquivo JavaScript. |  
| `persistent` (obrigatório) | Isso deve ser definido como `true` ou `false` .  Se definido como `true` , o script de plano de fundo é carregado e persiste para toda a seção de navegação.  Se definido como `false` , o script em segundo plano é carregado com um atraso e persiste para a sessão de navegação. |  

Recarregue a extensão e teste novamente.  Para recarregar a extensão: clique em **...** para obter configurações e mais no Microsoft Edge, clique em **extensões**, clique em sua extensão \ (**alterador de cor**\) e clique em **recarregar extensão**.  

Agora, abra uma nova guia ou atualize uma guia existente que não seja uma página do [docs.Microsoft.com][MicrosoftDocs] .  Você deve ver o ícone inativo e não pode clicar na ação do navegador.  

Parabéns!  Você criou uma extensão para o Microsoft Edge!  Veja a [amostra completa no GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  Continue lendo para saber mais sobre as extensões.  

## Gravando uma extensão mais complexa  

Deseja escrever uma extensão mais complexa?  Dê uma olhada na extensão Beastify em MDN no artigo, [sua segunda extensão][MDNYourSecondWebextension].  O modelo de extensão para o Microsoft Edge difere ligeiramente do modelo de extensão do Firefox, a extensão Beastify criada na [sua segunda extensão][MDNYourSecondWebextension] foi adaptada para funcionar no Microsoft Edge.  Dê uma olhada no [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].  

Ao percorrer o artigo sobre MDN, [sua segunda extensão][MDNYourSecondWebextension], lembre-se das seções a seguir.  

### APIs  

Consulte a página [APIs com suporte][ExtensionsAPIsupportApis] para obter uma lista de APIs de extensões com suporte no Microsoft Edge.  

### Tamanhos de ícone  

Os tamanhos de ícone de extensão preferencial para o Microsoft Edge são `20px` , `25px` , `30px` , e `40px` .  Outros tamanhos compatíveis são `19px` , `35px` e `38px` .  Para obter mais informações sobre tamanhos de ícone e práticas recomendadas, consulte o guia de [design][ExtensionsGuidesDesign] .  

### JavaScript  

O modelo de extensão do Microsoft Edge não oferece suporte a promessas de JavaScript.  Em vez disso, use retornos de chamada.  Para obter mais exemplos de como usar retornos de chamada em uma extensão, dê uma olhada nas demonstrações [rápidas de impressão][GithubMicrosoftEdgeExtensionsDemosQuickPrint] e [troca de texto][GithubMicrosoftEdgeExtensionsDemosTextSwap] .  

Percorra o exemplo de [impressão rápida][GithubMicrosoftEdgeExtensionsDemosQuickPrint] no vídeo a seguir.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### Manifest. JSON  

*   A `author` chave é necessária no Microsoft Edge  
*   `activeTab`Não há suporte para a chave no Microsoft Edge  

Para obter mais informações sobre [extensões do navegador][MDNBrowserExtensions], consulte [MDN Web docs][MDNWebDocs].  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Adicionando uma extensão-adicionando, movendo e removendo extensões do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Extensões de depuração | Documentos da Microsoft"  
[ExtensionsGuidesDesign]: ./design.md "Diretrizes de design para extensões do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Ícones – diretrizes de design para extensões do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md "APIs com suporte | Documentos da Microsoft"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Chaves de manifesto com suporte | Documentos da Microsoft"  

[MicrosoftDocs]: https://docs.microsoft.com "Documentos da Microsoft"  

[MDNWebDocs]: https://developer.mozilla.org "Documentos da Web do MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Extensões do navegador | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomia de uma extensão | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Scripts em segundo plano-anatomia de uma extensão | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "BrowserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserAction. SetIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onMessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "guias-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de conteúdo | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "Author-manifest. JSON | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "plano de fundo-manifesto. JSON | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest. JSON | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Descrição-manifest. JSON | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "ícones-manifest. JSON | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest. JSON | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "permissões-manifest. JSON | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "versão-manifest. JSON | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Sua segunda extensão | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Alterador de cor-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Imagens-alterador de cor-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest. JSON-alterador de cor-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Impressão rápida-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Troca de texto-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
