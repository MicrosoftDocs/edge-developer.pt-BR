---
description: Criar uma extensão que exibe a imagem da NASA do dia
title: Criar um tutorial de extensão-parte 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 3809bfac714621cf97184127132487ed93958a2f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104704"
---
# Criar um tutorial de extensão-parte 1  

## Visão geral  

A meta deste tutorial é criar uma extensão do Microsoft Edge (Chromium) a partir de um diretório vazio. Criaremos uma extensão que exibe a imagem da NASA do dia. Neste tutorial, você aprenderá a criar uma extensão por:

*   Criando um `manifest.json` arquivo.  
*   Adicionando ícones.  
*   Abrir uma caixa de diálogo pop-up padrão.  

## Antes de começar

Se quiser testar a extensão concluída que você criará neste tutorial, baixe o [código-fonte][ArchiveExtensionGettingStartedPart1].  

## Etapa 1: criar um `manifest.json` arquivo

Cada pacote de extensão deve ter um `manifest.json` arquivo na raiz.  O manifesto fornece detalhes da extensão, a versão do pacote de extensão, o nome e a descrição da extensão e assim por diante.  

O trecho de código a seguir destaca as informações básicas necessárias no seu `manifest.json` arquivo.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## Etapa 2: Adicionar ícones  

Comece criando o `icons` diretório em seu projeto para armazenar os arquivos de imagem do ícone.  Os ícones são usados para a imagem de plano de fundo do botão que os usuários selecionam para iniciar a extensão.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Ícone na barra de ferramentas para abrir a extensão&quot;:::
   Ícone na barra de ferramentas para abrir a extensão
:::image-end:::

Para ícones, recomendamos usar: 
*   `PNG` Formatar para ícones, mas você também pode usar `BMP` , `GIF` `ICO` ou `JPEG` formatos.  
*   Imagens que são 128 x 128 px, que são redimensionadas pelo navegador, se necessário.  

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

Em seguida, adicione os ícones ao `manifest.json` arquivo. Atualize o `manifest.json` arquivo com as informações dos ícones para que ele corresponda ao trecho de código a seguir. Os `png` arquivos listados no código a seguir estão disponíveis no arquivo de download mencionado anteriormente neste artigo.  

```json
{
    &quot;name&quot;: &quot;NASA picture of the day viewer&quot;,
    &quot;version&quot;: &quot;0.0.0.1&quot;,
    &quot;manifest_version&quot;: 2,
    &quot;description&quot;: &quot;A chromium extension to show the NASA picture of the day.&quot;,
    &quot;icons&quot;: {
        &quot;16&quot;: &quot;icons/nasapod16x16.png&quot;,
        &quot;32&quot;: &quot;icons/nasapod32x32.png&quot;,
        &quot;48&quot;: &quot;icons/nasapod48x48.png&quot;,
        &quot;128&quot;: &quot;icons/nasapod128x128.png"
    }
}
```  

## Etapa 3: abrir uma caixa de diálogo pop-up padrão  

Agora, crie um `HTML` arquivo que seja executado quando o usuário iniciar a extensão.  Crie o arquivo HTML chamado `popup.html` em um diretório chamado `popup` .  Quando os usuários selecionam o ícone para iniciar a extensão, ele `popup/popup.html` é exibido como uma caixa de diálogo modal.  

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

Certifique-se de adicionar o arquivo de imagem `images/stars.jpeg` à pasta images.  Os diretórios do seu projeto devem ser semelhantes à estrutura a seguir.   

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

Por fim, certifique-se de registrar o pop-up em `manifest.json` `browser_action` , conforme mostrado no trecho de código a seguir.  

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

## Próximas etapas
Isso é tudo o que você precisa para desenvolver uma extensão funcional. Agora, continue em Sideload e teste a extensão. Para obter mais informações, consulte [Sideload uma extensão][TestExtensionSideload].  


<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Fonte do pacote de extensão concluída | Documentos da Microsoft"

[TestExtensionSideload]: ./extension-sideloading.md "Testar sua extensão (Sideload) | Documentos da Microsoft"
