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
# <a name="puppeteer-overview"></a><span data-ttu-id="74221-104">Visão geral do Puppeteer</span><span class="sxs-lookup"><span data-stu-id="74221-104">Puppeteer overview</span></span>  

<span data-ttu-id="74221-105">[O Puppeteer][|::ref1::|Main] é uma biblioteca [node][NodejsMain] que fornece uma API de alto nível para controlar o Microsoft Edge \(Chromium\) usando o [Protocolo DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="74221-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="74221-106">O Puppeteer inicia [navegadores sem cabeça][WikiHeadlessBrowser] por padrão.</span><span class="sxs-lookup"><span data-stu-id="74221-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="74221-107">Navegadores sem cabeça não exibem uma interface do usuário, portanto, em vez disso, você deve usar a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="74221-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="74221-108">Você também pode configurar o Puppeteer para executar o Microsoft Edge completo \(non-headless\).</span><span class="sxs-lookup"><span data-stu-id="74221-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="74221-109">Por padrão, quando você instala o Puppeteer, o instalador baixa uma versão recente do [Chromium][ChromiumHome], o navegador de código aberto em que o Microsoft Edge também [é criado.][MicrosoftBlogsWindowsExperience20181206]</span><span class="sxs-lookup"><span data-stu-id="74221-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="74221-110">Se você tiver o Microsoft Edge \(Chromium\) instalado, poderá usar [o puppeteer-core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="74221-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="74221-111">é uma versão leve do Puppeteer que inicia uma instalação de navegador existente, como o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="74221-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="74221-112">Para baixar o Microsoft Edge \(Chromium\), navegue até [Baixar canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="74221-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <a name="installing-puppeteer-core"></a><span data-ttu-id="74221-113">Instalando o titer-core</span><span class="sxs-lookup"><span data-stu-id="74221-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="74221-114">Você pode adicionar `puppeteer-core` ao seu site ou aplicativo com um dos seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="74221-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a><span data-ttu-id="74221-115">Iniciar o Microsoft Edge com o puppeteer-core</span><span class="sxs-lookup"><span data-stu-id="74221-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="74221-116">depende do Nó v8.9.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="74221-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="74221-117">O exemplo a seguir usa o que só é `async` / `await` suportado no Nó v7.6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="74221-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="74221-118">Execute `node -v` a partir da linha de comando para garantir que você tenha uma versão compatível do Node.js.</span><span class="sxs-lookup"><span data-stu-id="74221-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="74221-119">deve estar familiarizado com os usuários de outras estruturas de teste de navegador, como [WebDriver][WebdriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="74221-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="74221-120">Crie uma instância do navegador, abra uma página e manipule-a com a API do Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="74221-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="74221-121">No exemplo de código a seguir, inicia o `puppeteer-core` Microsoft Edge \(Chromium\), navega para e salva `https://www.microsoftedgeinsider.com` uma captura de tela como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="74221-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="74221-122">Copie o trecho de código a seguir e salve-o como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="74221-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="74221-123">Altere `executablePath` para apontar para a instalação do Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="74221-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="74221-124">Por exemplo, no macOS, o `executablePath` para o Microsoft Edge Canary deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="74221-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="74221-125">Para encontrar o , navegue até e copie o caminho Executável nessa página ou instale o pacote de caminhos de borda `executablePath` com um dos seguintes `edge://version` comandos. \*\*\*\* [][npmEdgePaths]</span><span class="sxs-lookup"><span data-stu-id="74221-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="74221-126">O exemplo de código a seguir usa o pacote [de][npmEdgePaths] caminhos de borda para encontrar programaticamente o caminho para sua instalação do Microsoft Edge \(Chromium\) em seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="74221-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="74221-127">Por fim, desem conjunto `executablePath: EDGE_PATH` em `example.js` .</span><span class="sxs-lookup"><span data-stu-id="74221-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="74221-128">Salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="74221-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="74221-129">O Microsoft Edge \(EdgeHTML\) não funciona com `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="74221-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="74221-130">Você deve instalar os canais [do Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para continuar seguindo este exemplo.</span><span class="sxs-lookup"><span data-stu-id="74221-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="74221-131">Agora, execute `example.js` a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="74221-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="74221-132">inicia o Microsoft Edge, navega para e salva `https://www.microsoftedgeinsider.com` uma captura de tela da página da Web.</span><span class="sxs-lookup"><span data-stu-id="74221-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="74221-133">Personalizar o tamanho da captura de tela [com page.setViewport()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="74221-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="O arquivo example.png produzido por example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="74221-135">O `example.png` arquivo produzido por</span><span class="sxs-lookup"><span data-stu-id="74221-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="74221-136">Este é apenas um exemplo simples dos cenários de automação e teste habilitados pelo Puppeteer e `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="74221-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="74221-137">Para obter mais informações sobre o Puppeteer e como ele funciona, navegue até [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="74221-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="74221-138">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="74221-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="74221-139">A equipe do Desenvolvedor do Microsoft Edge está ávida para ouvir seus comentários sobre como usar o Puppeteer `puppeteer-core` e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="74221-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="74221-140">Use o **ícone Enviar Comentários** no Microsoft Edge DevTools ou @EdgeDevTools para permitir que a equipe do Microsoft Edge saiba o que você acha. [][TwitterIntentTweetEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="74221-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Feedback no Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="74221-142">O **ícone Enviar Feedback** no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="74221-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
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
