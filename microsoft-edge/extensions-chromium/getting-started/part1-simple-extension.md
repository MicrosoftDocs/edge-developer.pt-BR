---
description: Extensões sendo iniciadas parte 1
title: Criar uma extensão simples que é exibida na imagem de NASA do dia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 826401869b98d339e9b156a3727d94bd1182063d
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015762"
---
# Criar uma extensão simples que é exibida na imagem de NASA do dia 
 
<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart1]  
-->  

## Visão geral  

Na parte 1, o objetivo é criar uma extensão Chromium de borda muito simples, começando com um diretório vazio.  A meta para esta extensão é concluir as tarefas a seguir.  

*   Criar ícones para a extensão que podem ser usadas em vários locais e em diferentes tamanhos  
*   Criar um `manifest.json` arquivo simples  
*   Exibir um ícone de inicialização quando selecionado exibe uma janela pop-up contendo a imagem da NASA do dia  

## Noções básicas sobre o arquivo de manifesto  

Cada pacote de extensão deve ter um `manifest.json` arquivo na raiz.  Você deve pensar nisso como o plano gráfico da extensão.  Ele informa ao mecanismo de navegador qual versão da API de extensão a extensão espera, o nome e a descrição da extensão e muitos outros detalhes, muitos dos quais são abordados neste guia de introdução à extensão de várias partes.  

Veja a seguir uma simples  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## Configuração de ícones de extensão  

Em seguida, adicione alguns ícones ao `manifest.json` arquivo \ (e crie um novo `/icons` diretório com os arquivos de ícones \).  Os ícones são usados para a imagem de plano de fundo do botão que o usuário seleciona para iniciar a extensão \ (se houver um \) e outros locais apropriados.  

`PNG` é o formato recomendado, mas você também pode usar `BMP` , `GIF` `ICO` e `JPEG` .  Recomenda-se sempre ter pelo menos um ícone de tamanho de pixels de 128 x 128 e o navegador o redimensiona automaticamente conforme necessário.  

A estrutura do diretório deve ter a aparência do diagrama a seguir.  

<!--  
:::image type="complex" source="./media/part1-heirarchy.png" alt-text="Directory Structure":::
   Directory Structure
:::image-end:::
-->  

<!--![Directory Structure][ImagePart1Heirarchy]  -->  

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

O `manifest.json` arquivo atualizado deve aparecer da seguinte maneira.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

> [!NOTE]
> Os arquivos de ícone `png` listados no código anterior estão disponíveis no download do zip, mencionado na parte superior desta página.  

## Adicionar uma caixa de diálogo pop-up padrão  

Agora, crie um `HTML` arquivo que seja executado automaticamente quando o usuário selecionar o ícone de extensão.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Ícone de selo da barra de ferramentas":::
   Ícone de selo da barra de ferramentas
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

O arquivo HTML é chamado `popup/popup.html` .  Selecionar o ícone de extensão é iniciado `popup/popup.html` como uma caixa de diálogo modal que fica ativa até você selecionar fora da caixa de diálogo.  

Para isso, registre o arquivo como um pop-up padrão no `manifest.json` `browser_action` no código a seguir.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium Extension to show the NASA Picture of the Day.",
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

No `popup` diretório, adicione o arquivo `popup.html` e faça com que ele renderize a imagem de estrelas.  Aqui está o `popup.html` arquivo.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA Picture of the Day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="stars" />
        </div>
    </body>
</html>
```  

 Além disso, adicione um arquivo de imagem `images/stars.jpeg` referenciado no `popup.html` arquivo.  

A estrutura de diretório para o exemplo de extensão é exibida no diagrama a seguir.  

<!--  
:::image type="complex" source="./media/part1-heirarchy1.png" alt-text="Directory Structure for Extension":::
   Directory Structure for Extension
:::image-end:::
-->  

<!--![Directory Structure for Extension][ImagePart1Heirarchy1]  -->  

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

<!--  
> [!NOTE]
> The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].  
-->  

Isso é tudo o que você precisa para criar uma extensão em funcionamento.  Tudo o que resta para fazer é testá-lo.  

A seção a seguir explica como carregar a extensão \ (às vezes chamado de carregamento lateral \) no navegador Microsoft Edge \ (Chromium \) para testá-la.  

## Executar a extensão localmente no navegador ao desenvolver \ (carregando \)  

O navegador Microsoft Edge \ (Chromium \) fornece uma maneira segura e simples para você executar e depurar as extensões durante o desenvolvimento.  

O processo é muito simples.  Primeiro você deve selecionar os três pontos na parte superior do seu navegador.  Em seguida, escolha no `Extensions` menu de contexto, como mostrado na imagem a seguir.  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Escolher extensões":::
   Escolher extensões
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

Quando estiver na página **extensões** , conforme mostrado na imagem a seguir, habilite o **modo de desenvolvedor** habilitando a alternância na parte inferior esquerda da página, como mostrado na imagem a seguir.  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Habilitar o modo de desenvolvedor":::
   Habilitar o modo de desenvolvedor
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## Instalando e atualizando extensões de carregamento lado a lado  

Na primeira vez que você quiser instalar a extensão, escolha a `Load Unpacked` opção conforme mostrado na imagem a seguir.  Isso solicitará a você um diretório em que você tem o arquivo de ativos de extensão por meio do arquivo.  Isso instalará a extensão como se você a tivesse baixado de uma loja.  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Extensões instaladas":::
   Extensões instaladas
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

Depois de instalar a extensão, você pode atualizá-la selecionando o `Reload` botão abaixo de sua lista de extensão.  

Para remover a extensão do seu navegador, clique no `Remove` botão na parte inferior da listagem de extensão.  

## Extensões de depuração  

Extensões de depuração é muito fácil e dão suporte a todos os recursos no Edge Chromium DevTools.  Esses detalhes no entanto não são abordados neste guia de introdução, mas são muito importantes para criar extensões com êxito.  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Fonte do pacote de extensão concluída para esta parte | Documentos da Microsoft"  
