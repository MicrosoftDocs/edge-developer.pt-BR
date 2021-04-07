---
description: Usar o Puppeteer para automatizar e testar no Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento da Web, desenvolvedor, ferramentas, automação, teste
ms.openlocfilehash: 89a4dad3319f8e61f27487973509a8ee5ac23b6a
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480164"
---
# <a name="puppeteer-overview"></a>Visão geral do Puppeteer  

[O Puppeteer][|::ref1::|Main] é uma biblioteca [node][NodejsMain] que fornece uma API de alto nível para controlar o Microsoft Edge \(Chromium\) usando o [Protocolo DevTools][GithubChromedevtoolsProtocol].  O Puppeteer inicia [navegadores sem cabeça][WikiHeadlessBrowser] por padrão.  Navegadores sem cabeça não exibem uma interface do usuário, portanto, em vez disso, você deve usar a linha de comando.  Você também pode configurar o Puppeteer para executar o Microsoft Edge completo \(non-headless\).  

Por padrão, quando você instala o Puppeteer, o instalador baixa uma versão recente do [Chromium][ChromiumHome], o navegador de código aberto em que o Microsoft Edge também [é criado.][MicrosoftBlogsWindowsExperience20181206]  Se você tiver o Microsoft Edge \(Chromium\) instalado, poderá usar [o puppeteer-core][PuppeteerApivscore].  `puppeteer-core` é uma versão leve do Puppeteer que inicia uma instalação de navegador existente, como o Microsoft Edge \(Chromium\).  Para baixar o Microsoft Edge \(Chromium\), navegue até [Baixar canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload].  

## <a name="installing-puppeteer-core"></a>Instalando o titer-core  

Você pode adicionar `puppeteer-core` ao seu site ou aplicativo com um dos seguintes comandos.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a>Iniciar o Microsoft Edge com o puppeteer-core  

> [!NOTE]
> `puppeteer-core` depende do Nó v8.9.0 ou posterior.  O exemplo a seguir usa o que só é `async` / `await` suportado no Nó v7.6.0 ou posterior.  Execute `node -v` a partir da linha de comando para garantir que você tenha uma versão compatível do Node.js.  

`puppeteer-core` deve estar familiarizado com os usuários de outras estruturas de teste de navegador, como [WebDriver][WebdriverChromiumMain].  Crie uma instância do navegador, abra uma página e manipule-a com a API do Puppeteer.  No exemplo de código a seguir, inicia o `puppeteer-core` Microsoft Edge \(Chromium\), navega para e salva `https://www.microsoftedgeinsider.com` uma captura de tela como `example.png` .  

Copie o trecho de código a seguir e salve-o como `example.js` .  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

Altere `executablePath` para apontar para a instalação do Microsoft Edge \(Chromium\).  Por exemplo, no macOS, o `executablePath` para o Microsoft Edge Canary deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .  Para encontrar o , navegue até e copie o caminho Executável nessa página ou instale o pacote de caminhos de borda `executablePath` com um dos seguintes `edge://version` comandos. **** [][npmEdgePaths]  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
O exemplo de código a seguir usa o pacote [de][npmEdgePaths] caminhos de borda para encontrar programaticamente o caminho para sua instalação do Microsoft Edge \(Chromium\) em seu sistema operacional.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Por fim, desem conjunto `executablePath: EDGE_PATH` em `example.js` .  Salve suas alterações.  

> [!NOTE]
> O Microsoft Edge \(EdgeHTML\) não funciona com `puppeteer-core` .  Você deve instalar os canais [do Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para continuar seguindo este exemplo.  

Agora, execute `example.js` a partir da linha de comando.  

```shell
node example.js
```  

`puppeteer-core` inicia o Microsoft Edge, navega para e salva `https://www.microsoftedgeinsider.com` uma captura de tela da página da Web.  Personalizar o tamanho da captura de tela [com page.setViewport()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="O arquivo example.png produzido por example.js" lightbox="./media/puppeteer-example.png":::
   O `example.png` arquivo produzido por `example.js`  
:::image-end:::  

Este é apenas um exemplo simples dos cenários de automação e teste habilitados pelo Puppeteer e `puppeteer-core` .  Para obter mais informações sobre o Puppeteer e como ele funciona, navegue até [Puppeteer][|::ref2::|Main].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

A equipe do Desenvolvedor do Microsoft Edge está ávida para ouvir seus comentários sobre como usar o Puppeteer `puppeteer-core` e o Microsoft Edge.  Use o **ícone Enviar Comentários** no Microsoft Edge DevTools ou @EdgeDevTools para permitir que a equipe do Microsoft Edge saiba o que você acha. [][TwitterIntentTweetEdgedevtools]  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Feedback no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   O **ícone Enviar Feedback** no Microsoft Edge DevTools  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge:  Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Microsoft Docs"  

<!--  [ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visualizador de Protocolo chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: tornando a Web melhor por meio de mais colaboração de código aberto | Microsoft Experience Blog"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Os projetos Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Caminhos de Borda | npm"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer vs. puppeteer-core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools - Poste um tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem | Wikipédia"  
