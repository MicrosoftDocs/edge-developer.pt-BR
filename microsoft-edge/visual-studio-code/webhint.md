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
# extensão de código do webhint VS

Use [webhint](https://webhint.io), uma ferramenta de redimensionamento personalizável, para melhorar a acessibilidade, o desempenho, a compatibilidade entre navegadores, a compatibilidade do PWA e a segurança do seu site. Ele verifica o código em busca de práticas recomendadas e erros comuns. Este projeto de código aberto, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte da [Fundação OpenJS](https://openjsf.org/). A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.

![Captura de tela da extensão de código do webhint VS](./media/webhint-extension.png)

Identifique e corrija problemas em HTML, CSS, JavaScript, TypeScript e muito mais adicionando a [extensão webhint para o código vs](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). As dicas aparecem como sublinhados embutidos e são resumidas no painel problemas.

## Configuração

Essa extensão usa um arquivo JSON de [configuração padrão](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) que ativa dicas e analisadores para HTML, CSS, sistemas de TEMPLATING (JSX/TSX, angular e assim por diante), JavaScript/TypeScript e muito mais.

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

Se quiser ter mais controle sobre as dicas e analisadores que são ativados, crie um `.hintrc` arquivo local para configurar a dica na webquerer. Para obter ajuda com a saída de dicas específicas, consulte o [Guia do usuário do webhint](https://webhint.io/docs/user-guide/configuring-webhint/summary/).

## Privacidade Jurídica

Envie-nos seus comentários ao [arquivar um problema](https://github.com/webhintio/hint/issues/new) no [webhint do repositório do GitHub](https://github.com/webhintio/hint). 

Para contribuir para a extensão, leia o [Guia de contribuição da extensão de código do webhint vs](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).

## Consulte também
  - [Acessibilidade](/microsoft-edge/accessibility)
  - [Visual Studio Code](/microsoft-edge/visual-studio-code/)
