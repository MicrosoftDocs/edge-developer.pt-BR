---
description: Como usar webhint no Visual Studio Code
title: webhint Visual Studio de código
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
# <a name="webhint-vs-code-extension"></a>Extensão webhint vs code  

Use [webhint][WebhintMain], uma ferramenta de linting personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade com o PWA e a segurança do seu site.  Ele verifica seu código em busca de práticas recomendadas e erros comuns. Este projeto de código aberto, inicialmente desenvolvido pela equipe do Microsoft Edge, agora faz parte do [OpenJS Foundation][OpenjsFoundation].  A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores web na comunidade.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão Visual Studio Código da Web":::
   Captura de tela da extensão Visual Studio Código da Web  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

Identifique e corrige problemas em seu HTML, CSS, JavaScript, TypeScript e muito mais adicionando a extensão [webhint para Visual Studio Código][VisualstudioMarketplaceWebhint].  As dicas aparecem como sublinhados em linha e são resumidas no painel **Problemas.**  

## <a name="configuration"></a>Configuração  

Essa extensão usa um arquivo [json][GithubWebhintioIndexjson] de configuração padrão que ativa dicas e analisadores para HTML, CSS, sistemas de templating \(JSX/TSX, Angular e assim por diante\), JavaScript/TypeScript e muito mais.  

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

Se você quiser mais controle sobre as dicas e analisadores que são ativadas, crie um arquivo local `.hintrc` para configurar a webhint.  Para ajuda com a saída de dicas específicas, navegue até [webhint user guide][WebhintDocsUserguideConfiguringSummary].  

## <a name="getting-in-touch-with-the-webhint-team"></a>Entrar em contato com a equipe webhint  

Envie seus comentários [arquivando um problema][GithubWebhintioIssuesNew] no [repositório do GitHub da Webhint.][GithubWebhintio]  

Para contribuir com a extensão, navegue até [Webhint Visual Studio Guia de contribuição][GithubWebhintioExtensionVscodeContributing]de extensão de código.  

## <a name="see-also"></a>Veja também  

*   [Acessibilidade][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Acessibilidade | Microsoft Docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio código | Microsoft Docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribuição - webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.json - webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Novos problemas - webhintio/| GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configurando o webhint | Documentação webhint"  
[WebhintMain]:  https://webhint.io "webhint"  
