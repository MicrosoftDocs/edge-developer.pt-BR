---
description: Usar o playwright para automatizar e testar no Microsoft Edge
title: Playwright
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento da Web, desenvolvedor, ferramentas, automação, teste, playwright, nó, JavaScript, NPM
ms.openlocfilehash: ac03923fb25da00f07cb70e81ac06b106a6e1452
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192209"
---
# Playwright  

[Playwright][|::ref1::|Main] é uma biblioteca de [Node.js][NodejsMain] para automatizar o [Chromium][ChromiumHome], o [Firefox][FirefoxMain]e o [WebKit][|::ref2::|Main] com uma única API.  O playwright foi desenvolvido para habilitar a automação da Web em vários navegadores que seja sempre verde, compatível, confiável e rápido.  Como [o Microsoft Edge é criado na plataforma de Web Chromium de código-fonte aberto][MicrosoftBlogsWindowsExperience20181206], o playwright também pode automatizar o Microsoft Edge.  

O playwright inicia [navegadores sem periféricos][WikiHeadlessBrowser] por padrão.  Navegadores sem periféricos não exibem uma interface do usuário, portanto, você deve usar a linha de comando.  Você também pode configurar o playwright para executar o Microsoft Edge completo \ (não-sem nenhum sem periférico) também.  

Por padrão, quando você instala o playwright, o instalador baixa [Chromium][ChromiumHome], [Firefox][FirefoxMain]e [WebKit][|::ref3::|Main].  Se você tiver o Microsoft Edge \ (Chromium \) instalado também, playwright precisará apenas uma alteração de código em uma linha para testar seu site ou aplicativo no Microsoft Edge.  Para baixar o Microsoft Edge \ (Chromium \), navegue até [baixar o Microsoft Edge][MicrosoftEdgeDownload].  

## Instalando o playwright  

Instale o [playwright][|::ref4::|Main] para testar seu site ou aplicativo com o seguinte comando.  

```shell
npm i playwright
```  

## Iniciar o Microsoft Edge com o playwright  

> [!NOTE]
> O [playwright][|::ref5::|Main] requer Node.js versão 10,17 ou posterior. Executar a `node -v` partir da linha de comando para ter certeza de que você tem uma versão compatível do Node.js.  Os binários do navegador para Chromium, Firefox e WebKit funcionam no Windows, no macOS e no Linux. Para obter mais informações, navegue até [playwright requisitos do sistema][PlaywrightSystemRequirements].  

Playwright deve ser familiar aos usuários de outras estruturas de teste de navegador, como [WebDriver][WebDriverChromiumMain] ou [Puppeteer][PuppeteerMain].  Você cria uma instância do navegador, abre uma página e, em seguida, a manipula com a [API playwright][PlaywrightAPIReference].  No trecho de código a seguir, o playwright inicia o Microsoft Edge \ (Chromium \), navega até `https://www.microsoft.com/edge` e salva uma captura de tela como `example.png` .  

Copie o trecho de código a seguir e salve-o como `example.js` .  

```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoft.com/edge');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

Alterar `executablePath` para apontar para a sua instalação do Microsoft Edge \ (Chromium \).  Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canárias deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .  Para localizar o `executablePath` , navegue até `edge://version` e copie o **caminho do executável** nessa página ou instale o pacote de [caminhos de borda][npmEdgePaths] com o comando a seguir.  

```shell
npm i edge-paths
```  

O trecho de código a seguir usa o pacote de [bordas de borda][npmEdgePaths] para localizar programaticamente o caminho para a instalação do Microsoft Edge \ (Chromium \) no seu sistema operacional.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Por fim, `executablePath: EDGE_PATH` defina `example.js` .  Salve suas alterações.  

> [!NOTE]
> O Microsoft Edge \ (EdgeHTML \) não funciona com o playwright.  Você deve instalar [o Microsoft Edge \ (Chromium \)][MicrosoftEdgeDownload] para continuar seguindo este exemplo.  

Agora, execute `example.js` a partir da linha de comando.  

```shell
node example.js
```  

O playwright inicia o Microsoft Edge, navega até `https://www.microsoft.com/edge` e salva uma captura de tela da página.  Você pode personalizar o tamanho da página com [Page. setViewportSize ()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="O arquivo example.png produzido pela example.js" lightbox="../media/playwright-example.png":::
    O `example.png` arquivo produzido por `example.js`  
:::image-end:::  

`example.js` é uma simples demonstração dos cenários de automação e teste habilitados pelo playwright.  Para fazer capturas de tela em vários navegadores da Web, altere o código a seguir.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Para obter mais informações sobre o playwright, navegue até o [site do playwright][|::ref6::|Main].  Confira o  [repositório do playwright][PlaywrightRepo] no github.  Para compartilhar seus comentários sobre como automatizar e testar seu site ou aplicativo com o playwright, [arquivo um problema][PlaywrightRepoNewIssue].  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Documentos da Microsoft"  
[PuppeteerMain]: ../puppeteer.md "Puppeteer | Documentos da Microsoft"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: aprimorar a Web por meio de mais colaboração de fonte aberta | Blog de experiência da Microsoft"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Baixar o Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Projetos do Chromium"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "borda-caminhos | NPM"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Referência de API playwright"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "Page. setViewportSize (viewportSize) | Referência de API playwright"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Requisitos do sistema do playwright"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Novo problema no repositório do playwright | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem periféricos | Wikipédia"  
