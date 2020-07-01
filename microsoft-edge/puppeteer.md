---
description: Usar o Puppeteer para automatizar e testar no Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento da Web, desenvolvedor, ferramentas, automação, teste
ms.openlocfilehash: ccca46426a006651a417a22e54c8b528834b5f81
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844009"
---
# <span data-ttu-id="ae5c9-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="ae5c9-104">Puppeteer</span></span>  

<span data-ttu-id="ae5c9-105">[Puppeteer][|::ref1::|Main] é uma biblioteca de [nós][NodejsMain] que fornece uma API de alto nível para controlar o Microsoft Edge \ (Chromium \) sobre o [protocolo devtools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="ae5c9-106">O Puppeteer é executado sem [periféricos][WikiHeadlessBrowser] , o que significa que você não vê uma interface do usuário e, em vez disso, deve usar a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-106">Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.</span></span>  <span data-ttu-id="ae5c9-107">Você também pode configurar o Puppeteer para executar o Microsoft Edge ou o Chromium completo \ (não-sem nenhum sem periférico) também.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-107">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.</span></span>  

<span data-ttu-id="ae5c9-108">Por padrão, quando você instala o Puppeteer, o instalador baixa uma versão recente do [Chromium][ChromiumHome], o navegador de código aberto que o [Microsoft Edge também tem baseado][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-108">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="ae5c9-109">Se você tiver o Microsoft Edge \ (Chromium \) instalado, poderá usar o [Puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-109">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="ae5c9-110">é uma versão leve do Puppeteer que inicia uma instalação do navegador existente, como o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="ae5c9-110">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ae5c9-111">Para baixar o Microsoft Edge \ (Chromium \), consulte [baixar canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-111">To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>

## <span data-ttu-id="ae5c9-112">Instalando o Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="ae5c9-112">Installing puppeteer-core</span></span>  

<span data-ttu-id="ae5c9-113">Você pode adicionar `puppeteer-core` ao seu site ou aplicativo com um dos seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-113">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="ae5c9-114">Iniciar o Microsoft Edge com o Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="ae5c9-114">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="ae5c9-115">depende do nó v 8.9.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-115">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="ae5c9-116">O exemplo a seguir usa `async` / `await` que só tem suporte no nó v 7.6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-116">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="ae5c9-117">Executar a `node -v` partir da linha de comando para ter certeza de que você tem uma versão compatível do Node.js.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-117">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="ae5c9-118">deve ser familiar aos usuários de outros frameworks de teste de navegador, como o [WebDriver][WebDriverEdgehtmlMain].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-118">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="ae5c9-119">Você cria uma instância do navegador, abre uma página e, em seguida, a manipula com a API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-119">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="ae5c9-120">No exemplo de código a seguir, o `puppeteer-core` Microsoft Edge é iniciado no Microsoft Edge \ (Chromium \), navega em `https://www.microsoftedgeinsider.com` e salva uma captura de tela como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="ae5c9-120">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="ae5c9-121">Copie o exemplo de código abaixo e salve-o como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ae5c9-121">Copy the code sample below and save it as `example.js`.</span></span>  

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

<span data-ttu-id="ae5c9-122">Alterar `executablePath` para apontar para a sua instalação do Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="ae5c9-122">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ae5c9-123">Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canárias deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="ae5c9-123">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="ae5c9-124">Para localizar o `executablePath` , navegue até `edge://version` e copie o **caminho do executável** nessa página ou instale o pacote de [caminhos de borda][npmEdgePaths] com um dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-124">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="ae5c9-125">O exemplo de código a seguir usa o pacote de [bordas de borda][npmEdgePaths] para localizar programaticamente o caminho para a instalação do Microsoft Edge \ (Chromium \) no seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-125">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="ae5c9-126">Por fim, `executablePath: EDGE_PATH` defina `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ae5c9-126">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="ae5c9-127">Salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-127">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="ae5c9-128">O Microsoft Edge \ (EdgeHTML \) não funciona com `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ae5c9-128">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="ae5c9-129">Você deve instalar os [canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para continuar seguindo este exemplo.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-129">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="ae5c9-130">Agora são executados `example.js` a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-130">Now run `example.js` from the command-line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="ae5c9-131">inicia o Microsoft Edge, navega até `https://www.microsoftedgeinsider.com` e salva uma captura de tela do 800px x 600px da página.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-131">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.</span></span>  <span data-ttu-id="ae5c9-132">Você pode personalizar o tamanho da página com [Page. setviewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-132">You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="O arquivo example.png produzido pela example.js":::
   <span data-ttu-id="ae5c9-134">Figura 1: o `example.png` arquivo produzido por</span><span class="sxs-lookup"><span data-stu-id="ae5c9-134">Figure 1:  The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

<span data-ttu-id="ae5c9-135">Isso é apenas um exemplo simples dos cenários de automação e teste habilitados pelo Puppeteer e `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ae5c9-135">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="ae5c9-136">Para obter mais informações sobre o Puppeteer e como ele funciona, consulte [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="ae5c9-136">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="ae5c9-137">Enviar Comentários</span><span class="sxs-lookup"><span data-stu-id="ae5c9-137">Send Feedback</span></span>  

<span data-ttu-id="ae5c9-138">A equipe de desenvolvimento do Edge está ansiosos para ouvir seus comentários sobre como usar o Puppeteer, `puppeteer-core` o e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-138">The Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="ae5c9-139">Use o ícone **enviar comentários** no Microsoft Edge devtools ou tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] para permitir que a equipe do Microsoft Edge saiba o que você acha.</span><span class="sxs-lookup"><span data-stu-id="ae5c9-139">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="O ícone de comentários no Microsoft Edge DevTools":::
   <span data-ttu-id="ae5c9-141">Figura 2: o ícone de **comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="ae5c9-141">Figure 2:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
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
