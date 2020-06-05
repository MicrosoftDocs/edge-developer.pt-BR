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
# Extensão de código do webhint vs  

Use [webhint][WebhintMain], uma ferramenta de redimensionamento personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade do PWA e a segurança do seu site.  Ele verifica o código em busca de práticas recomendadas e erros comuns. Este projeto de código aberto, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte da [Fundação OpenJS][OpenjsFoundation].  A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão de código do webhint VS":::
   Captura de tela da extensão de código do webhint VS  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

Identifique e corrija problemas em HTML, CSS, JavaScript, TypeScript e muito mais adicionando a [extensão webhint para o código vs][VisualstudioMarketplaceWebhint].  As dicas aparecem como sublinhados embutidos e são resumidas no painel **problemas** .  

## Configuração  

Essa extensão usa um arquivo JSON de [configuração padrão][GithubWebhintioIndexjson] que ativa dicas e analisadores para HTML, CSS, sistemas de templating \ (JSX/TSX, angular e assim por diante \), JavaScript/TypeScript e muito mais.  

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

Se quiser ter mais controle sobre as dicas e analisadores que são ativados, crie um `.hintrc` arquivo local para configurar a dica na webquerer.  Para obter ajuda com a saída de dicas específicas, consulte [Guia do usuário da WebDicas][WebhintDocsUserguideConfiguringSummary].  

## Como entrar em contato com a equipe webhint  

Envie seus comentários por meio do [arquivamento de um problema][GithubWebhintioIssuesNew] na [webhint do repositório do GitHub][GithubWebhintio].  

Para contribuir para a extensão, consulte [Guia de contribuição da extensão de código do vs][GithubWebhintioExtensionVscodeContributing].  

## Consulte também  

*   [Acessibilidade][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

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
