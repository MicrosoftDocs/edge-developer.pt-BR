---
description: Usar o Puppeteer para automatizar e testar no Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento da Web, desenvolvedor, ferramentas, automação, teste
ms.openlocfilehash: bef3f0d7472f7bc595998829546fb540041f20fc
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986154"
---
# Puppeteer  

[Puppeteer][|::ref1::|Main] é uma biblioteca de [nós][NodejsMain] que fornece uma API de alto nível para controlar o Microsoft Edge \ (Chromium \) sobre o [protocolo devtools][GithubChromedevtoolsProtocol].  O Puppeteer é executado sem [periféricos][WikiHeadlessBrowser] , o que significa que você não vê uma interface do usuário e, em vez disso, deve usar a linha de comando.  Você também pode configurar o Puppeteer para executar o Microsoft Edge ou o Chromium completo \ (não-sem nenhum sem periférico) também.  

Por padrão, quando você instala o Puppeteer, o instalador baixa uma versão recente do [Chromium][ChromiumHome], o navegador de código aberto que o [Microsoft Edge também tem baseado][MicrosoftBlogsWindowsExperience20181206].  Se você tiver o Microsoft Edge \ (Chromium \) instalado, poderá usar o [Puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` é uma versão leve do Puppeteer que inicia uma instalação do navegador existente, como o Microsoft Edge \ (Chromium \).  Para baixar o Microsoft Edge \ (Chromium \), consulte [baixar canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload].

## Instalando o Puppeteer-Core  

Você pode adicionar `puppeteer-core` ao seu site ou aplicativo com um dos seguintes comandos.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Iniciar o Microsoft Edge com o Puppeteer-Core  

> [!NOTE]
> `puppeteer-core` depende do nó v 8.9.0 ou posterior.  O exemplo a seguir usa `async` / `await` que só tem suporte no nó v 7.6.0 ou posterior.  Executar a `node -v` partir da linha de comando para ter certeza de que você tem uma versão compatível do Node.js.  

`puppeteer-core` deve ser familiar aos usuários de outros frameworks de teste de navegador, como o [WebDriver][WebDriverEdgehtmlMain].  Você cria uma instância do navegador, abre uma página e, em seguida, a manipula com a API Puppeteer.  No exemplo de código a seguir, o `puppeteer-core` Microsoft Edge é iniciado no Microsoft Edge \ (Chromium \), navega em `https://www.microsoftedgeinsider.com` e salva uma captura de tela como `example.png` .  

Copie o exemplo de código abaixo e salve-o como `example.js` .  

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

Alterar `executablePath` para apontar para a sua instalação do Microsoft Edge \ (Chromium \).  Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canárias deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .  Para localizar o `executablePath` , navegue até `edge://version` e copie o **caminho do executável** nessa página ou instale o pacote de [caminhos de borda][npmEdgePaths] com um dos comandos a seguir.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
O exemplo de código a seguir usa o pacote de [bordas de borda][npmEdgePaths] para localizar programaticamente o caminho para a instalação do Microsoft Edge \ (Chromium \) no seu sistema operacional.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Por fim, `executablePath: EDGE_PATH` defina `example.js` .  Salve suas alterações.  

> [!NOTE]
> O Microsoft Edge \ (EdgeHTML \) não funciona com `puppeteer-core` .  Você deve instalar os [canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para continuar seguindo este exemplo.  

Agora são executados `example.js` a partir da linha de comando.  

```shell
node example.js
```  

`puppeteer-core` inicia o Microsoft Edge, navega até `https://www.microsoftedgeinsider.com` e salva uma captura de tela do 800px x 600px da página.  Você pode personalizar o tamanho da página com [Page. setviewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="O arquivo example.png produzido pela example.js":::
   Figura 1: o `example.png` arquivo produzido por `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

Isso é apenas um exemplo simples dos cenários de automação e teste habilitados pelo Puppeteer e `puppeteer-core` .  Para obter mais informações sobre o Puppeteer e como ele funciona, consulte [Puppeteer][|::ref2::|Main].  

## Entrar em contato com a equipe do Microsoft Edge DevTools  

A equipe de desenvolvimento do Microsoft Edge está ansiosos para ouvir seus comentários sobre como usar o Puppeteer, `puppeteer-core` o e o Microsoft Edge.  Use o ícone **enviar comentários** no Microsoft Edge devtools ou tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] para permitir que a equipe do Microsoft Edge saiba o que você acha.  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools":::
   O ícone **enviar comentários** no Microsoft Edge devtools  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "WebDriver (Chromium)"  
[WebdriverEdgehtmlMain]: ./webdriver.md "WebDriver (EdgeHTML)"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visualizador de protocolo do Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: aprimorar a Web por meio de mais colaboração de fonte aberta | Blog de experiência da Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Projetos do Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "NPM | Caminhos de borda"

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Puppeteer versus Puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setviewport (visor) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-poste um tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem periféricos | Wikipédia"  
