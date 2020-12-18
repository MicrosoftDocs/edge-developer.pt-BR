---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Saiba como fazer a portabilidade da extensão Chrome para o Microsoft Edge usando o kit de ferramentas de extensão do Microsoft Edge.
title: Compatibilizar Extensões do Chrome
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f226d79dbc9efdc43eb68bfb353fa12748198371
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231812"
---
# Portando uma extensão do Chrome para o Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

A portabilidade de uma extensão do Chrome para o Microsoft Edge torna-se fácil com a ajuda do [Kit de ferramentas de extensão do Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb). Esta ferramenta de desenvolvedor converte uma extensão Chrome desempacotada em uma extensão do Microsoft Edge desempacotada, ligando APIs e faceamento quaisquer erros em seu `manifest.json` arquivo.


### Pontes de API
Para permitir a portabilidade transparente de APIs Chrome para APIs do Microsoft Edge com suporte, dois scripts são adicionados à pasta da extensão. Esses scripts são APIs de ponte (o profiling quando necessário), o que significa que você não precisa se preocupar em alterar qualquer código específico do Chrome em seu script de plano de fundo ou scripts de conteúdo.

Após a conversão, você os verá incluído no arquivo de manifesto da extensão com a `"-ms-preload"` chave:

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## Usar o kit de ferramentas de extensão do Microsoft Edge

As instruções a seguir detalham como converter a extensão Chrome para executar no Microsoft Edge na edição de aniversário do Windows 10.

1. Instale o [Kit de ferramentas de extensão do Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).
2. Faça uma cópia da pasta da extensão do Chrome para manter a segurança. O processo de conversão substituirá o código. 
3. Execute o kit de ferramentas de extensão do Microsoft Edge e carregue a cópia da extensão.  
 ![botão carregar extensão](./../media/save-folder.png)
4. Corrija todos os erros relatados no editor de texto da ferramenta. Selecione "revalidar" para verificar se há erros após fazer correções.  
 ![extensão – erros ao localizar o kit de ferramentas](./../media/extension-toolkit.png)
5. Selecione "salvar arquivos".

Agora você pode sair do kit de ferramentas e carregar a extensão no Microsoft Edge! 

Você pode pesquisar problemas de plataforma conhecidos com o [controlador de problemas do EdgeHTML](http://issues.microsoftedge.com). Se você acha que encontrou algo novo, [abra um problema](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!
