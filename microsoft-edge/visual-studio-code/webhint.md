---
description: Como usar webhint no Visual Studio Code
title: webhint Visual Studio Code extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, vs code, código do visual studio, webhint
ms.openlocfilehash: 3dfd900bf818d02dbc8123c00e7928e56d9b6ade
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399271"
---
# <a name="webhint-vs-code-extension"></a><span data-ttu-id="fff82-104">Extensão webhint vs code</span><span class="sxs-lookup"><span data-stu-id="fff82-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="fff82-105">Use [webhint][WebhintMain], uma ferramenta de linting personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, PWA compatibilidade e a segurança do seu site.</span><span class="sxs-lookup"><span data-stu-id="fff82-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="fff82-106">Ele verifica seu código em busca de práticas recomendadas e erros comuns.</span><span class="sxs-lookup"><span data-stu-id="fff82-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="fff82-107">Este projeto de código aberto, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte do [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="fff82-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="fff82-108">A Microsoft Edge equipe continua a contribuir para Webhint junto com os desenvolvedores da Web na comunidade.</span><span class="sxs-lookup"><span data-stu-id="fff82-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão Visual Studio Code webhint":::
   <span data-ttu-id="fff82-110">Captura de tela da extensão Visual Studio Code webhint</span><span class="sxs-lookup"><span data-stu-id="fff82-110">Screenshot of webhint Visual Studio Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="fff82-111">Identifique e corrige problemas em seu HTML, CSS, JavaScript, TypeScript e muito mais adicionando a extensão [webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="fff82-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="fff82-112">As dicas aparecem como sublinhados em linha e são resumidas no painel **Problemas.**</span><span class="sxs-lookup"><span data-stu-id="fff82-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <a name="configuration"></a><span data-ttu-id="fff82-113">Configuração</span><span class="sxs-lookup"><span data-stu-id="fff82-113">Configuration</span></span>  

<span data-ttu-id="fff82-114">Essa extensão usa um arquivo [json][GithubWebhintioIndexjson] de configuração padrão que ativa dicas e analisadores para HTML, CSS, sistemas de templating \(JSX/TSX, Angular e assim por diante\), JavaScript/TypeScript e muito mais.</span><span class="sxs-lookup"><span data-stu-id="fff82-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

```json
{
    "connector": "local",
    "extends": [
        "accessibility",
        "progressive-web-apps"
    ],
    "formatters": [
        "html",
        "summary"
    ],
    "hints": [
        "apple-touch-icons",
        "button-type",
        "compat-api/css",
        "compat-api/html",
        "create-element-svg",
        "css-prefix-order",
        "disown-opener",
        "highest-available-document-mode",
        "manifest-exists",
        "meta-charset-utf-8",
        "meta-viewport",
        "no-bom",
        "no-protocol-relative-urls",
        "scoped-svg-styles",
        "sri",
        "typescript-config/consistent-casing",
        "typescript-config/import-helpers",
        "typescript-config/is-valid",
        "typescript-config/no-comments",
        "typescript-config/strict",
        "typescript-config/target"
    ],
    "hintsTimeout": 10000,
    "parsers": [
        "babel-config",
        "css",
        "html",
        "javascript",
        "jsx",
        "less",
        "sass",
        "typescript",
        "typescript-config",
        "webpack-config"
    ]
}
```  

<span data-ttu-id="fff82-115">Se você quiser mais controle sobre as dicas e analisadores que são ativadas, crie um arquivo local `.hintrc` para configurar a webhint.</span><span class="sxs-lookup"><span data-stu-id="fff82-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="fff82-116">Para ajuda com a saída de dicas específicas, navegue até [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="fff82-116">For help with output from specific hints, navigate to [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <a name="getting-in-touch-with-the-webhint-team"></a><span data-ttu-id="fff82-117">Entrar em contato com a equipe webhint</span><span class="sxs-lookup"><span data-stu-id="fff82-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="fff82-118">Envie seus comentários [arquivando um problema][GithubWebhintioIssuesNew] na [webhint GitHub repo][GithubWebhintio].</span><span class="sxs-lookup"><span data-stu-id="fff82-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="fff82-119">Para contribuir com a extensão, navegue até [Webhint Visual Studio Code guia de contribuição de extensão][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="fff82-119">To contribute to the extension, navigate to [webhint Visual Studio Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <a name="see-also"></a><span data-ttu-id="fff82-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fff82-120">See also</span></span>  

*   [<span data-ttu-id="fff82-121">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="fff82-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="fff82-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fff82-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Acessibilidade | Microsoft Docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio Code | Microsoft Docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribuição - webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.json - webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Novos problemas - webhintio/| GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configurando o webhint | Documentação webhint"  
[WebhintMain]:  https://webhint.io "webhint"  
