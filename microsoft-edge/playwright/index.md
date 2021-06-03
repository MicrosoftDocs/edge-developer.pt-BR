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
# <span data-ttu-id="43be5-104">Playwright</span><span class="sxs-lookup"><span data-stu-id="43be5-104">Playwright</span></span>  

<span data-ttu-id="43be5-105">[O][|::ref1::|Main] [dramaturgo éNode.js][NodejsMain] biblioteca para automatizar Chromium, [Firefox][FirefoxMain]e [][ChromiumHome] [WebKit][|::ref2::|Main] com uma única API.</span><span class="sxs-lookup"><span data-stu-id="43be5-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="43be5-106">O dramaturgo foi criado para habilitar a automação da Web entre navegadores que seja sempre verde, capaz, confiável e rápida.</span><span class="sxs-lookup"><span data-stu-id="43be5-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="43be5-107">Como Microsoft Edge é criado na plataforma web de Chromium de código [aberto,][MicrosoftBlogsWindowsExperience20181206]o Atordoado também é capaz de automatizar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="43be5-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="43be5-108">O [dramaturgo inicia navegadores sem cabeça][WikiHeadlessBrowser] por padrão.</span><span class="sxs-lookup"><span data-stu-id="43be5-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="43be5-109">Navegadores sem cabeça não exibem uma interface do usuário, portanto, em vez disso, você deve usar a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="43be5-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="43be5-110">Você também pode configurar o Atordoamento para executar a ação completa \(non-headless\) Microsoft Edge também.</span><span class="sxs-lookup"><span data-stu-id="43be5-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="43be5-111">Por padrão, quando você instala o Dramaturgo, o instalador baixa [Chromium,][ChromiumHome] [Firefox][FirefoxMain]e [WebKit.][|::ref3::|Main]</span><span class="sxs-lookup"><span data-stu-id="43be5-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="43be5-112">Se você tiver Microsoft Edge \(Chromium\) instalado também, o Atordogo precisa apenas de uma alteração de código de uma linha para testar seu site ou aplicativo no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="43be5-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="43be5-113">Para baixar Microsoft Edge \(Chromium\), navegue até [Baixar Microsoft Edge][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="43be5-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="43be5-114">Instalando o Dramaturgo</span><span class="sxs-lookup"><span data-stu-id="43be5-114">Installing Playwright</span></span>  

<span data-ttu-id="43be5-115">Instale [o Atordoar][|::ref4::|Main] para testar seu site ou aplicativo com o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="43be5-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="43be5-116">Iniciar Microsoft Edge com o Atordogo</span><span class="sxs-lookup"><span data-stu-id="43be5-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="43be5-117">[O][|::ref5::|Main] dramaturgo Node.js versão 10.17 ou superior.</span><span class="sxs-lookup"><span data-stu-id="43be5-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="43be5-118">Execute `node -v` a partir da linha de comando para garantir que você tenha uma versão compatível do Node.js.</span><span class="sxs-lookup"><span data-stu-id="43be5-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="43be5-119">Os binários do navegador para Chromium, Firefox e WebKit funcionam em Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="43be5-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="43be5-120">Para obter mais informações, navegue até [Requisitos do Sistema de Dramaturgo.][PlaywrightSystemRequirements]</span><span class="sxs-lookup"><span data-stu-id="43be5-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="43be5-121">O dramaturgo deve estar familiarizado com os usuários de outras estruturas de teste de navegador, como [WebDriver][WebDriverChromiumMain] ou [Puppeteer.][PuppeteerMain]</span><span class="sxs-lookup"><span data-stu-id="43be5-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="43be5-122">Crie uma instância do navegador, abra uma página e manipule-a com a [API de Dramaturgia.][PlaywrightAPIReference]</span><span class="sxs-lookup"><span data-stu-id="43be5-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="43be5-123">No trecho de código a seguir, o Dramaturgo inicia Microsoft Edge \(Chromium\), navega para e salva uma captura de tela `https://www.microsoft.com/edge` como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="43be5-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="43be5-124">Copie o trecho de código a seguir e salve-o como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="43be5-124">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="43be5-125">Altere `executablePath` para apontar para a instalação do Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="43be5-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="43be5-126">Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canary deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="43be5-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="43be5-127">Para encontrar o , navegue até e copie o caminho Executável nessa página ou instale o pacote de caminhos de borda `executablePath` `edge://version` com o seguinte comando. \*\*\*\* [][npmEdgePaths]</span><span class="sxs-lookup"><span data-stu-id="43be5-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="43be5-128">O trecho de código a seguir usa o pacote [de][npmEdgePaths] caminhos de borda para encontrar programaticamente o caminho para sua instalação do Microsoft Edge \(Chromium\) em seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="43be5-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="43be5-129">Por fim, desem conjunto `executablePath: EDGE_PATH` em `example.js` .</span><span class="sxs-lookup"><span data-stu-id="43be5-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="43be5-130">Salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="43be5-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="43be5-131">Microsoft Edge \(EdgeHTML\) não funciona com o Dramaturgo.</span><span class="sxs-lookup"><span data-stu-id="43be5-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="43be5-132">Você deve instalar [Microsoft Edge \(Chromium\) para][MicrosoftEdgeDownload] continuar seguindo este exemplo.</span><span class="sxs-lookup"><span data-stu-id="43be5-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="43be5-133">Agora, `example.js` execute a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="43be5-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="43be5-134">O ator inicia Microsoft Edge, navega para e salva `https://www.microsoft.com/edge` uma captura de tela da página.</span><span class="sxs-lookup"><span data-stu-id="43be5-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="43be5-135">Você pode personalizar o tamanho da página [com page.setViewportSize()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="43be5-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="O arquivo example.png produzido por example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="43be5-137">O `example.png` arquivo produzido por</span><span class="sxs-lookup"><span data-stu-id="43be5-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="43be5-138">é apenas uma demonstração simples dos cenários de automação e teste habilitados pelo Dramaturgo.</span><span class="sxs-lookup"><span data-stu-id="43be5-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="43be5-139">Para fazer capturas de tela em vários navegadores da Web, altere o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="43be5-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="43be5-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="43be5-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="43be5-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="43be5-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="43be5-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="43be5-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="43be5-143">Para obter mais informações sobre o Dramaturgo, navegue até o [site do Atordogo.][|::ref6::|Main]</span><span class="sxs-lookup"><span data-stu-id="43be5-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="43be5-144">Confira o [repo do Dramaturgo][PlaywrightRepo] GitHub.</span><span class="sxs-lookup"><span data-stu-id="43be5-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="43be5-145">Para compartilhar seus comentários sobre como automatizar e testar seu site ou aplicativo com o Atordoamento, [arquivo um problema.][PlaywrightRepoNewIssue]</span><span class="sxs-lookup"><span data-stu-id="43be5-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="43be5-146">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="43be5-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
