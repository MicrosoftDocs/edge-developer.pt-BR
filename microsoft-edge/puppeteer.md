---
description: Usar o Puppeteer para automatizar e testar no Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento da Web, desenvolvedor, ferramentas, automação, teste
ms.openlocfilehash: e92a863f28c96157b4c7692bd88ba6884cbf8f52
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192230"
---
# <span data-ttu-id="04305-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="04305-104">Puppeteer</span></span>  

<span data-ttu-id="04305-105">[Puppeteer][|::ref1::|Main] é uma biblioteca de [nós][NodejsMain] que fornece uma API de alto nível para controlar o Microsoft Edge \ (Chromium \) usando o [protocolo devtools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="04305-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="04305-106">O Puppeteer inicia [navegadores sem periféricos][WikiHeadlessBrowser] por padrão.</span><span class="sxs-lookup"><span data-stu-id="04305-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="04305-107">Navegadores sem periféricos não exibem uma interface do usuário, portanto, você deve usar a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="04305-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="04305-108">Você também pode configurar o Puppeteer para executar o Microsoft Edge completo \ (não-sem nenhum sem periférico) também.</span><span class="sxs-lookup"><span data-stu-id="04305-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="04305-109">Por padrão, quando você instala o Puppeteer, o instalador baixa uma versão recente do [Chromium][ChromiumHome], o navegador de código aberto que o [Microsoft Edge também tem baseado][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="04305-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="04305-110">Se você tiver o Microsoft Edge \ (Chromium \) instalado, poderá usar o [Puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="04305-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="04305-111">é uma versão leve do Puppeteer que inicia uma instalação do navegador existente, como o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="04305-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="04305-112">Para baixar o Microsoft Edge \ (Chromium \), navegue para [baixar os canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="04305-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <span data-ttu-id="04305-113">Instalando o Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="04305-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="04305-114">Você pode adicionar `puppeteer-core` ao seu site ou aplicativo com um dos seguintes comandos.</span><span class="sxs-lookup"><span data-stu-id="04305-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="04305-115">Iniciar o Microsoft Edge com o Puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="04305-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="04305-116">depende do nó v 8.9.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="04305-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="04305-117">O exemplo a seguir usa `async` / `await` que só tem suporte no nó v 7.6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="04305-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="04305-118">Executar a `node -v` partir da linha de comando para ter certeza de que você tem uma versão compatível do Node.js.</span><span class="sxs-lookup"><span data-stu-id="04305-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="04305-119">deve ser familiar aos usuários de outras estruturas de teste de navegador, como [WebDriver][WebDriverEdgehtmlMain].</span><span class="sxs-lookup"><span data-stu-id="04305-119">should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="04305-120">Você cria uma instância do navegador, abre uma página e, em seguida, a manipula com a API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="04305-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="04305-121">No exemplo de código a seguir, o `puppeteer-core` Microsoft Edge é iniciado no Microsoft Edge \ (Chromium \), navega em `https://www.microsoftedgeinsider.com` e salva uma captura de tela como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="04305-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="04305-122">Copie o trecho de código a seguir e salve-o como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="04305-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="04305-123">Alterar `executablePath` para apontar para a sua instalação do Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="04305-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="04305-124">Por exemplo, no macOS, o `executablePath` para Microsoft Edge Canárias deve ser definido como `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="04305-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="04305-125">Para localizar o `executablePath` , navegue até `edge://version` e copie o **caminho do executável** nessa página ou instale o pacote de [caminhos de borda][npmEdgePaths] com um dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="04305-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="04305-126">O exemplo de código a seguir usa o pacote de [bordas de borda][npmEdgePaths] para localizar programaticamente o caminho para a instalação do Microsoft Edge \ (Chromium \) no seu sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="04305-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="04305-127">Por fim, `executablePath: EDGE_PATH` defina `example.js` .</span><span class="sxs-lookup"><span data-stu-id="04305-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="04305-128">Salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="04305-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="04305-129">O Microsoft Edge \ (EdgeHTML \) não funciona com `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="04305-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="04305-130">Você deve instalar os [canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para continuar seguindo este exemplo.</span><span class="sxs-lookup"><span data-stu-id="04305-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="04305-131">Agora, executar `example.js` a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="04305-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="04305-132">inicia o Microsoft Edge, navega até `https://www.microsoftedgeinsider.com` e salva uma captura de tela da página da Web.</span><span class="sxs-lookup"><span data-stu-id="04305-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="04305-133">Personalize o tamanho da captura de tela com [Page. setviewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="04305-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="O arquivo example.png produzido pela example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="04305-135">O `example.png` arquivo produzido por</span><span class="sxs-lookup"><span data-stu-id="04305-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="04305-136">O exemplo a seguir simples usa cenários de automação e teste habilitados pelo Puppeteer e `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="04305-136">The following simple example uses automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="04305-137">Para obter mais informações sobre o Puppeteer e como ele funciona, navegue até [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="04305-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="04305-138">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="04305-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="04305-139">A equipe de desenvolvimento do Microsoft Edge está ansiosos para ouvir seus comentários sobre como usar o Puppeteer, `puppeteer-core` o e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="04305-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="04305-140">Use o ícone **enviar comentários** no Microsoft Edge devtools ou tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] para permitir que a equipe do Microsoft Edge saiba o que você acha.</span><span class="sxs-lookup"><span data-stu-id="04305-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools" lightbox="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="04305-142">O ícone **enviar comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="04305-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
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

[WebdriverChromiumMain]: ./webdriver-chromium "WebDriver (Chromium) | Documentos da Microsoft"  
[WebdriverEdgehtmlMain]: ./webdriver.md "WebDriver (EdgeHTML) | Documentos da Microsoft"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visualizador de protocolo do Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: aprimorar a Web por meio de mais colaboração de fonte aberta | Blog de experiência da Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Projetos do Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Caminhos de borda | NPM"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Puppeteer versus Puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setviewport (visor) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-poste um tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navegador sem periféricos | Wikipédia"  
