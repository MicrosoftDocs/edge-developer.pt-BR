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
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231080"
---
# <span data-ttu-id="c475f-104">Playwright</span><span class="sxs-lookup"><span data-stu-id="c475f-104">Playwright</span></span>  

<span data-ttu-id="c475f-105">[Playwright][|::ref1::|Main] é uma biblioteca de [Node.js][NodejsMain] para automatizar o [Chromium][ChromiumHome], o [Firefox][FirefoxMain]e o [WebKit][|::ref2::|Main] com uma única API.</span><span class="sxs-lookup"><span data-stu-id="c475f-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="c475f-106">O playwright foi desenvolvido para habilitar a automação da Web em vários navegadores que seja sempre verde, compatível, confiável e rápido.</span><span class="sxs-lookup"><span data-stu-id="c475f-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="c475f-107">Como [o Microsoft Edge é criado na plataforma de Web Chromium de código-fonte aberto][MicrosoftBlogsWindowsExperience20181206], o playwright também pode automatizar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c475f-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="c475f-108">O playwright inicia [navegadores sem periféricos][WikiHeadlessBrowser] por padrão.</span><span class="sxs-lookup"><span data-stu-id="c475f-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="c475f-109">Navegadores sem periféricos não exibem uma interface do usuário, portanto, você deve usar a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c475f-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="c475f-110">Você também pode configurar o playwright para executar o Microsoft Edge completo \(não-sem nenhum sem periférico) também.</span><span class="sxs-lookup"><span data-stu-id="c475f-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="c475f-111">Por padrão, quando você instala o playwright, o instalador baixa [Chromium][ChromiumHome], [Firefox][FirefoxMain]e [WebKit][|::ref3::|Main].</span><span class="sxs-lookup"><span data-stu-id="c475f-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="c475f-112">Se você tiver o Microsoft Edge \(Chromium \) instalado também, playwright precisará apenas uma alteração de código em uma linha para testar seu site ou aplicativo no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c475f-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="c475f-113">Para baixar o Microsoft Edge \(Chromium \), navegue até [baixar o Microsoft Edge][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="c475f-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="c475f-114">Instalando o playwright</span><span class="sxs-lookup"><span data-stu-id="c475f-114">Installing Playwright</span></span>  

<span data-ttu-id="c475f-115">Instale o [playwright][|::ref4::|Main] para testar seu site ou aplicativo com o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="c475f-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="c475f-116">Iniciar o Microsoft Edge com o playwright</span><span class="sxs-lookup"><span data-stu-id="c475f-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="c475f-117">O [playwright][|::ref5::|Main] requer Node.js versão 10,17 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c475f-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="c475f-118">Executar a `node -v` partir da linha de comando para ter certeza de que você tem uma versão compatível do Node.js.</span><span class="sxs-lookup"><span data-stu-id="c475f-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="c475f-119">Os binários do navegador para Chromium, Firefox e WebKit funcionam no Windows, no macOS e no Linux.</span><span class="sxs-lookup"><span data-stu-id="c475f-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="c475f-120">Para obter mais informações, navegue até [playwright requisitos do sistema][PlaywrightSystemRequirements].</span><span class="sxs-lookup"><span data-stu-id="c475f-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="c475f-121">Playwright deve ser familiar aos usuários de outras estruturas de teste de navegador, como [WebDriver][WebDriverChromiumMain] ou [Puppeteer][PuppeteerMain].</span><span class="sxs-lookup"><span data-stu-id="c475f-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="c475f-122">Você cria uma instância do navegador, abre uma página e, em seguida, a manipula com a [API playwright][PlaywrightAPIReference].</span><span class="sxs-lookup"><span data-stu-id="c475f-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="c475f-123">No trecho de código a seguir, o playwright inicia o Microsoft Edge \(Chromium \), navega até `https://www.microsoft.com/edge` e salva uma captura de tela como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="c475f-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="c475f-124">Copie o trecho de código a seguir e salve-o como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="c475f-124">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="c475f-125">Alterar `executablePath` para apontar para a sua instalação do Microsoft Edge \(Chromium \).</span><span class="sxs-lookup"><span data-stu-id="c475f-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c475f-126">Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canárias deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="c475f-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="c475f-127">Para localizar o `executablePath` , navegue até `edge://version` e copie o **caminho do executável** nessa página ou instale o pacote de [caminhos de borda][npmEdgePaths] com o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="c475f-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="c475f-128">O trecho de código a seguir usa o pacote de [bordas de borda][npmEdgePaths] para localizar programaticamente o caminho para a instalação do Microsoft Edge \(Chromium \) no seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c475f-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="c475f-129">Por fim, `executablePath: EDGE_PATH` defina `example.js` .</span><span class="sxs-lookup"><span data-stu-id="c475f-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="c475f-130">Salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="c475f-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="c475f-131">O Microsoft Edge \(EdgeHTML \) não funciona com o playwright.</span><span class="sxs-lookup"><span data-stu-id="c475f-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="c475f-132">Você deve instalar [o Microsoft Edge \(Chromium \)][MicrosoftEdgeDownload] para continuar seguindo este exemplo.</span><span class="sxs-lookup"><span data-stu-id="c475f-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="c475f-133">Agora, execute `example.js` a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c475f-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="c475f-134">O playwright inicia o Microsoft Edge, navega até `https://www.microsoft.com/edge` e salva uma captura de tela da página.</span><span class="sxs-lookup"><span data-stu-id="c475f-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="c475f-135">Você pode personalizar o tamanho da página com [Page. setViewportSize ()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="c475f-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="O arquivo example.png produzido pela example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="c475f-137">O `example.png` arquivo produzido por</span><span class="sxs-lookup"><span data-stu-id="c475f-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="c475f-138">é uma simples demonstração dos cenários de automação e teste habilitados pelo playwright.</span><span class="sxs-lookup"><span data-stu-id="c475f-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="c475f-139">Para fazer capturas de tela em vários navegadores da Web, altere o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c475f-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="c475f-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="c475f-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="c475f-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="c475f-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="c475f-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="c475f-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="c475f-143">Para obter mais informações sobre o playwright, navegue até o [site do playwright][|::ref6::|Main].</span><span class="sxs-lookup"><span data-stu-id="c475f-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="c475f-144">Confira o  [repositório do playwright][PlaywrightRepo] no github.</span><span class="sxs-lookup"><span data-stu-id="c475f-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="c475f-145">Para compartilhar seus comentários sobre como automatizar e testar seu site ou aplicativo com o playwright, [arquivo um problema][PlaywrightRepoNewIssue].</span><span class="sxs-lookup"><span data-stu-id="c475f-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="c475f-146">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c475f-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Documentos da Microsoft"  
[PuppeteerMain]: ../puppeteer/index.md "Puppeteer | Documentos da Microsoft"  

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
