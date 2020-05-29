---
description: Como usar webhint no código do Visual Studio
title: extensão de código do webhint VS
author: hxlnt
ms.author: raweil
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, código vs, código do Visual Studio, dica da Web
ms.openlocfilehash: d3102bf4d8d4a8bba9225d8d3f68432197f775ac
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562455"
---
# <span data-ttu-id="81366-104">extensão de código do webhint VS</span><span class="sxs-lookup"><span data-stu-id="81366-104">webhint VS Code extension</span></span>

<span data-ttu-id="81366-105">Use [webhint](https://webhint.io), uma ferramenta de redimensionamento personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade do PWA e a segurança do seu site.</span><span class="sxs-lookup"><span data-stu-id="81366-105">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="81366-106">Ele verifica o código em busca de práticas recomendadas e erros comuns.</span><span class="sxs-lookup"><span data-stu-id="81366-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="81366-107">Este projeto de código aberto, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte da [Fundação OpenJS](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="81366-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="81366-108">A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.</span><span class="sxs-lookup"><span data-stu-id="81366-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Captura de tela da extensão de código do webhint VS](./media/webhint-extension.png)

<span data-ttu-id="81366-110">Identifique e corrija problemas em HTML, CSS, JavaScript, TypeScript e muito mais adicionando a [extensão webhint para o código vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="81366-110">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="81366-111">As dicas aparecem como sublinhados embutidos e são resumidas no painel problemas.</span><span class="sxs-lookup"><span data-stu-id="81366-111">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

## <span data-ttu-id="81366-112">Configuração</span><span class="sxs-lookup"><span data-stu-id="81366-112">Configuration</span></span>

<span data-ttu-id="81366-113">Essa extensão usa um arquivo JSON de [configuração padrão](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) que ativa dicas e analisadores para HTML, CSS, sistemas de TEMPLATING (JSX/TSX, angular e assim por diante), JavaScript/TypeScript e muito mais.</span><span class="sxs-lookup"><span data-stu-id="81366-113">This extension uses a [default configuration](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) json file that activates hints and parsers for HTML, CSS, templating systems (JSX/TSX, Angular, and so on), JavaScript/TypeScript, and more.</span></span>

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

<span data-ttu-id="81366-114">Se quiser ter mais controle sobre as dicas e analisadores que são ativados, crie um `.hintrc` arquivo local para configurar a dica na webquerer.</span><span class="sxs-lookup"><span data-stu-id="81366-114">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span> <span data-ttu-id="81366-115">Para obter ajuda com a saída de dicas específicas, consulte o [Guia do usuário do webhint](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span><span class="sxs-lookup"><span data-stu-id="81366-115">For help with output from specific hints, see the [webhint user guide](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span></span>

## <span data-ttu-id="81366-116">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="81366-116">Feedback</span></span>

<span data-ttu-id="81366-117">Envie-nos seus comentários ao [arquivar um problema](https://github.com/webhintio/hint/issues/new) no [webhint do repositório do GitHub](https://github.com/webhintio/hint).</span><span class="sxs-lookup"><span data-stu-id="81366-117">Send us your feedback by [filing an issue](https://github.com/webhintio/hint/issues/new) on the [webhint GitHub repo](https://github.com/webhintio/hint).</span></span> 

<span data-ttu-id="81366-118">Para contribuir para a extensão, leia o [Guia de contribuição da extensão de código do webhint vs](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="81366-118">To contribute to the extension, please read the [webhint VS Code extension contribution guide](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span></span>

## <span data-ttu-id="81366-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81366-119">See also</span></span>
  - [<span data-ttu-id="81366-120">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="81366-120">Accessibility</span></span>](/microsoft-edge/accessibility)
  - [<span data-ttu-id="81366-121">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="81366-121">Visual Studio Code</span></span>](/microsoft-edge/visual-studio-code/)
