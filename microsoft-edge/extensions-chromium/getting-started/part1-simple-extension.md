---
description: Criar uma extensão que aparece na imagem do dia da NASA
title: Criar um tutorial de extensão - Parte 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: dfbe7893ce576c223d2b1d39ec21b6c5f46d8356
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397507"
---
# <a name="create-an-extension-tutorial---part-1"></a>Criar um tutorial de extensão - Parte 1  

## <a name="overview"></a>Visão geral  

O objetivo deste tutorial é criar uma extensão Microsoft Edge (Chromium) começando com um diretório vazio.  Você está criando uma extensão que aparece na imagem da NASA do dia. Neste tutorial, saiba como criar uma extensão concluindo as seguintes ações.  

*   Criando um `manifest.json` arquivo.  
*   Adicionando ícones.  
*   Abrindo uma caixa de diálogo pop-up padrão.  

## <a name="before-you-begin"></a>Antes de começar

Para testar a extensão concluída que você está criando neste tutorial, baixe o [código-fonte][ArchiveExtensionGettingStartedPart1].  

## <a name="step-1-create-a-manifestjson-file"></a>Etapa 1: Criar um manifest.jsno arquivo

Cada pacote de extensão deve ter `manifest.json` um arquivo na raiz.  O manifesto fornece detalhes sobre sua extensão, a versão do pacote de extensão, o nome e a descrição da extensão e assim por diante.  

O trecho de código a seguir descreve as informações básicas necessárias em seu `manifest.json` arquivo.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a>Etapa 2: Adicionar ícones  

Comece criando o `icons` diretório em seu projeto para armazenar os arquivos de imagem do ícone.  Os ícones são usados para a imagem de plano de fundo do botão que os usuários selecionam para iniciar a extensão.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Ícone na barra de ferramentas para abrir sua extensão":::
   Ícone na barra de ferramentas para abrir sua extensão  
:::image-end:::  

Para ícones, recomendamos usar: 
*   `PNG` para ícones, mas você também pode usar `BMP` `GIF` , ou `ICO` `JPEG` formatos.  
*   Imagens de 128 x 128 px, que são resized pelo navegador, se necessário.  

Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Em seguida, adicione os ícones ao `manifest.json` arquivo. Atualize seu arquivo com as informações de ícones para `manifest.json` que ele corresponde ao trecho de código a seguir. Os arquivos listados no código a seguir `png` estão disponíveis no arquivo de download mencionado anteriormente neste artigo.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <a name="step-3-open-a-default-pop-up-dialog"></a>Etapa 3: Abrir uma caixa de diálogo pop-up padrão  

Agora, crie um `HTML` arquivo para ser executado quando o usuário iniciar sua extensão.  Crie o arquivo HTML nomeado `popup.html` em um diretório chamado `popup` .  Quando os usuários selecionam o ícone para iniciar a extensão, `popup/popup.html` é exibido como uma caixa de diálogo modal.  

Adicione o código do trecho de código a seguir para `popup.html` exibir a imagem de estrelas.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

Certifique-se de adicionar o arquivo de `images/stars.jpeg` imagem à pasta de imagens.  Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

Por fim, certifique-se de registrar o pop-up `manifest.json` em , conforme mostrado no trecho de código a `browser_action` seguir.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## <a name="next-steps"></a>Próximas etapas
Isso é tudo o que você precisa para desenvolver uma extensão de trabalho.  Agora, continue fazendo sideload e teste sua extensão. Para obter mais informações, navegue até [Sideload de uma extensão][TestExtensionSideload].  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Fonte de pacote de extensão concluída | Microsoft Docs"

[TestExtensionSideload]: ./extension-sideloading.md "Teste sua extensão (Sideloading) | Microsoft Docs"
