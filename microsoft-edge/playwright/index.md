---
description: Usar o Atordogo para automatizar e testar Microsoft Edge
title: Playwright
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento da Web, desenvolvedor, ferramentas, automação, teste, dramaturgo, nó, javascript, npm
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231080"
---
# Playwright  

[O][|::ref1::|Main] [dramaturgo éNode.js][NodejsMain] biblioteca para automatizar Chromium, [Firefox][FirefoxMain]e [][ChromiumHome] [WebKit][|::ref2::|Main] com uma única API.  O dramaturgo foi criado para habilitar a automação da Web entre navegadores que seja sempre verde, capaz, confiável e rápida.  Como Microsoft Edge é criado na plataforma web de Chromium de código [aberto,][MicrosoftBlogsWindowsExperience20181206]o Atordoado também é capaz de automatizar Microsoft Edge.  

O [dramaturgo inicia navegadores sem cabeça][WikiHeadlessBrowser] por padrão.  Navegadores sem cabeça não exibem uma interface do usuário, portanto, em vez disso, você deve usar a linha de comando.  Você também pode configurar o Atordoamento para executar a ação completa \(non-headless\) Microsoft Edge também.  

Por padrão, quando você instala o Dramaturgo, o instalador baixa [Chromium,][ChromiumHome] [Firefox][FirefoxMain]e [WebKit.][|::ref3::|Main]  Se você tiver Microsoft Edge \(Chromium\) instalado também, o Atordogo precisa apenas de uma alteração de código de uma linha para testar seu site ou aplicativo no Microsoft Edge.  Para baixar Microsoft Edge \(Chromium\), navegue até [Baixar Microsoft Edge][MicrosoftEdgeDownload].  

## Instalando o Dramaturgo  

Instale [o Atordoar][|::ref4::|Main] para testar seu site ou aplicativo com o seguinte comando.  

```shell
npm i playwright
```  

## Iniciar Microsoft Edge com o Atordogo  

> [!NOTE]
> [O][|::ref5::|Main] dramaturgo Node.js versão 10.17 ou superior. Execute `node -v` a partir da linha de comando para garantir que você tenha uma versão compatível do Node.js.  Os binários do navegador para Chromium, Firefox e WebKit funcionam em Windows, macOS e Linux. Para obter mais informações, navegue até [Requisitos do Sistema de Dramaturgo.][PlaywrightSystemRequirements]  

O dramaturgo deve estar familiarizado com os usuários de outras estruturas de teste de navegador, como [WebDriver][WebDriverChromiumMain] ou [Puppeteer.][PuppeteerMain]  Crie uma instância do navegador, abra uma página e manipule-a com a [API de Dramaturgia.][PlaywrightAPIReference]  No trecho de código a seguir, o Dramaturgo inicia Microsoft Edge \(Chromium\), navega para e salva uma captura de tela `https://www.microsoft.com/edge` como `example.png` .  

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

Altere `executablePath` para apontar para a instalação do Microsoft Edge \(Chromium\).  Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canary deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .  Para encontrar o , navegue até e copie o caminho Executável nessa página ou instale o pacote de caminhos de borda `executablePath` `edge://version` com o seguinte comando. **** [][npmEdgePaths]  

```shell
npm i edge-paths
```  

O trecho de código a seguir usa o pacote [de][npmEdgePaths] caminhos de borda para encontrar programaticamente o caminho para sua instalação do Microsoft Edge \(Chromium\) em seu sistema operacional.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Por fim, desem conjunto `executablePath: EDGE_PATH` em `example.js` .  Salve suas alterações.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) não funciona com o Dramaturgo.  Você deve instalar [Microsoft Edge \(Chromium\) para][MicrosoftEdgeDownload] continuar seguindo este exemplo.  

Agora, `example.js` execute a partir da linha de comando.  

```shell
node example.js
```  

O ator inicia Microsoft Edge, navega para e salva `https://www.microsoft.com/edge` uma captura de tela da página.  Você pode personalizar o tamanho da página [com page.setViewportSize()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="O arquivo example.png produzido por example.js" lightbox="../media/playwright-example.png":::
    O `example.png` arquivo produzido por `example.js`  
:::image-end:::  

`example.js` é apenas uma demonstração simples dos cenários de automação e teste habilitados pelo Dramaturgo.  Para fazer capturas de tela em vários navegadores da Web, altere o código a seguir.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Para obter mais informações sobre o Dramaturgo, navegue até o [site do Atordogo.][|::ref6::|Main]  Confira o [repo do Dramaturgo][PlaywrightRepo] GitHub.  Para compartilhar seus comentários sobre como automatizar e testar seu site ou aplicativo com o Atordoamento, [arquivo um problema.][PlaywrightRepoNewIssue]  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Microsoft Docs"  
[PuppeteerMain]: ../puppeteer/index.md "| Microsoft Docs"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: melhorar a Web por meio de mais colaboração de código aberto | Microsoft Experience Blog"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Baixar Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Os Chromium projetos"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "edge-paths | npm"  

[PlaywrightMain]: https://playwright.dev "Dramaturgo"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Referência da API de Dramaturgia"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "page.setViewportSize(viewportSize) | Referência da API de Dramaturgia"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Requisitos do sistema de dramaturgia"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "| GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Novo problema no | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem | Wikipédia"  
