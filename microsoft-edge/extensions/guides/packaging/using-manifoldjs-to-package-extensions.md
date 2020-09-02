---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Veja como empacotar a extensão do Microsoft Edge em um instantâneo com o ManifoldJS, a ferramenta de código-fonte aberto Node.js.
title: Usar ManifoldJS para extensões de pacote
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: 83aa57ae0e4ae302b1360be50e5158782b6fbb76
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986203"
---
# Usar o ManifoldJS para criar pacotes AppX de extensão  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

O ManifoldJS é uma ferramenta de Node.js de código aberto que permite a criação rápida e fácil de um pacote que você pode usar para envio à Microsoft Store.  

Se você usar o recurso de mensagens nativas em sua extensão, deverá ignorar o artigo a seguir e ir para o recurso de [mensagens nativas no Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para instruções de empacotamento.  

Antes de começar, você ainda precisará ler os artigos a seguir.  

*   [Extensões no Centro de Desenvolvimento do Windows](./extensions-in-the-windows-dev-center.md)  
*   [Localizando pacotes de extensão](./localizing-extension-packages.md)  

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.  Depois de criar, empacotar e testar sua extensão, envie uma solicitação em nosso formulário de [envio de extensão](https://developer.microsoft.com/microsoft-edge/extensions/requests).  

## Instalando o Node.js e o ManifoldJS  

As primeiras coisas que você precisará fazer é instalar o [Node.js LTS](https://nodejs.org/en/download).  
Depois que você tiver o nó, a partir de uma linha de comando (preferencialmente, PowerShell), execute o seguinte comando para instalar o ManifoldJS.  

```shell
npm install -g manifoldjs
```  

Para verificar se você instalou corretamente o ManifoldJS, execute `manifoldjs` a partir da linha de comando. Se ManifoldJS não for reconhecido, adicione `%APPDATA%\npm` às variáveis de caminho.  

## Empacotamento com ManifoldJS  

Para iniciar o processo de empacotamento, você precisará abrir uma linha de comando e alterar os diretórios para uma pasta que será o destino da extensão empacotada.  

Por exemplo:

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> O `manifoldjs` comando gera no diretório atual e substitui o conteúdo.  

Agora que você está em sua pasta de destino, execute o seguinte comando.  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

O `mainifoldjs` comando pode ser dividido nas partes a seguir.  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      Altera o nível de log para `debug` obter uma impressão completa.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      Define a única plataforma para a qual executar a conversão `edgeextension` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      Informa ao programa que o formato do manifesto é um `edgeextension` formato e não se importa se ele falha na validação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      O caminho para o manifesto de extensão que você deseja converter.  
   :::column-end:::
:::row-end:::  

Depois que o ManifoldJS terminar de ser executado, você terá uma pasta com o conteúdo a seguir.  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...
-->  

O generationInfo.jsem arquivo é um log produzido ao executar ManifoldJS e não será incluído no seu pacote de extensão. Somente o conteúdo da `manifest` pasta será empacotado. Na pasta de manifesto, a pasta ativos contém as imagens que serão usadas na interface do usuário do Windows e da Microsoft Store, enquanto a pasta extensão tem o conteúdo de sua extensão dentro dela.  

Agora que você tem os arquivos corretos, será necessário editar o arquivo AppXManifest gerado dentro da `manifest` pasta. Se o manifest.jsdo ramal do arquivo tiver uma cadeia de caracteres internacionalizada para o campo "nome", quando ManifoldJS for executado, o nome da pasta da camada mais superior não terá sublinhado e incluirá "MSG".

Por exemplo, um manifest.jsem um arquivo com o `"name"` campo a seguir.  

```shell
"name" : "__MSG_appName__"
```  

terá uma pasta de manifesto que reside `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .  

No arquivo AppXManifest, será necessário:  

 *   Substitua os campos de identidade obrigatórios e o campo PublisherDisplayName conforme descrito [aqui](./creating-and-testing-extension-packages.md#app-identity-template-values). Observe que, se você estiver apenas empacotando para fins de teste ou para distribuição empresarial, poderá usar valores de espaço reservado em vez de se registrar para uma conta do centro de desenvolvimento do Windows.  
 *   Substitua os ícones de espaço reservado na pasta ativos por ícones para sua extensão pelos mesmos tamanhos (150x150, 50x50, 44 x 44) e nomes. Consulte o guia de [design](./../design.md#icons-for-packaging) para obter informações sobre onde esses ícones são usados.  
 *   Se sua extensão for localizada, siga todo o guia de [localização de extensões do Microsoft Edge](./localizing-extension-packages.md) . Se não estiver localizado, leia somente o [nome de localização e a descrição na seção Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .  

Depois que o `appxmanifest.xml` arquivo for classificado, execute o seguinte comando para criar seu pacote.  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

Agora, seu pacote estará na pasta **Package** localizada na pasta edgeextension. Para obter mais informações sobre como Sideload seu novo pacote, consulte seção [testando](./creating-and-testing-extension-packages.md#testing-an-appx-package) criando e testando pacotes de extensão.  

Depois que o pacote tiver sido testado, sinta-se à vontade para enviar uma solicitação em nosso [formulário de envio de extensão](https://aka.ms/extension-request) para ser considerado para publicação na Microsoft Store.  
