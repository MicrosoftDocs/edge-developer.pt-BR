---
description: Como usar webhint no código do Visual Studio
title: extensão de código do webhint VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, código vs, código do Visual Studio, dica da Web
ms.openlocfilehash: ec218fab8cbfb8181a0416c8e0eadc0e00412529
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695856"
---
# <span data-ttu-id="3a777-104">Extensão de código do webhint vs</span><span class="sxs-lookup"><span data-stu-id="3a777-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="3a777-105">Use [webhint][WebhintMain], uma ferramenta de redimensionamento personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade do PWA e a segurança do seu site.</span><span class="sxs-lookup"><span data-stu-id="3a777-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="3a777-106">Ele verifica o código em busca de práticas recomendadas e erros comuns.</span><span class="sxs-lookup"><span data-stu-id="3a777-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="3a777-107">Este projeto de código aberto, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte da [Fundação OpenJS][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="3a777-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="3a777-108">A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.</span><span class="sxs-lookup"><span data-stu-id="3a777-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão de código do webhint VS":::
   <span data-ttu-id="3a777-110">Captura de tela da extensão de código do webhint VS</span><span class="sxs-lookup"><span data-stu-id="3a777-110">Screenshot of webhint VS Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="3a777-111">Identifique e corrija problemas em HTML, CSS, JavaScript, TypeScript e muito mais adicionando a [extensão webhint para o código vs][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="3a777-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="3a777-112">As dicas aparecem como sublinhados embutidos e são resumidas no painel **problemas** .</span><span class="sxs-lookup"><span data-stu-id="3a777-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <span data-ttu-id="3a777-113">Configuração</span><span class="sxs-lookup"><span data-stu-id="3a777-113">Configuration</span></span>  

<span data-ttu-id="3a777-114">Essa extensão usa um arquivo JSON de [configuração padrão][GithubWebhintioIndexjson] que ativa dicas e analisadores para HTML, CSS, sistemas de templating \ (JSX/TSX, angular e assim por diante \), JavaScript/TypeScript e muito mais.</span><span class="sxs-lookup"><span data-stu-id="3a777-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="3a777-115">Se quiser ter mais controle sobre as dicas e analisadores que são ativados, crie um `.hintrc` arquivo local para configurar a dica na webquerer.</span><span class="sxs-lookup"><span data-stu-id="3a777-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="3a777-116">Para obter ajuda com a saída de dicas específicas, consulte [Guia do usuário da WebDicas][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="3a777-116">For help with output from specific hints, see [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <span data-ttu-id="3a777-117">Como entrar em contato com a equipe webhint</span><span class="sxs-lookup"><span data-stu-id="3a777-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="3a777-118">Envie seus comentários por meio do [arquivamento de um problema][GithubWebhintioIssuesNew] na [webhint do repositório do GitHub][GithubWebhintio].</span><span class="sxs-lookup"><span data-stu-id="3a777-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="3a777-119">Para contribuir para a extensão, consulte [Guia de contribuição da extensão de código do vs][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="3a777-119">To contribute to the extension, see [webhint VS Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <span data-ttu-id="3a777-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3a777-120">See also</span></span>  

*   [<span data-ttu-id="3a777-121">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="3a777-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="3a777-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="3a777-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint VS Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Acessibilidade | Documentos da Microsoft"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Código do Visual Studio | Documentos da Microsoft"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Colaborador-dica da GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index. JSON-webhintio/Hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Novos problemas-webhintio/dica | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "Base do OpenJS"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configurando webhint | Documentação do webhint"  
[WebhintMain]:  https://webhint.io "webhint"  
