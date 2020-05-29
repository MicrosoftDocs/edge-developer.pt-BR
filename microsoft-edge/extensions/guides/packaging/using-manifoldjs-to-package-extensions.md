---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Veja como empacotar a extensão do Microsoft Edge em um instantâneo com ManifoldJS, a ferramenta de código-fonte aberto node. js.
title: Usar o ManifoldJS para extensões de pacote
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: cca83a26c9f80eca6454e3b5b329f72a7491b6e2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561173"
---
# Usar o ManifoldJS para criar pacotes AppX de extensão  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS é uma ferramenta de nó de origem aberta. js que permite a criação rápida e fácil de um pacote que você pode usar para envio à Microsoft Store.

Se você usar o recurso de mensagens nativas em sua extensão, deverá ignorar isso e ir para o recurso de [mensagens nativas no Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para instruções de empacotamento. 

Antes de começar, você ainda precisa ler os artigos a seguir:

- [Extensões no centro de desenvolvimento do Windows](./extensions-in-the-windows-dev-center.md)
- [Localizando pacotes de extensão](./localizing-extension-packages.md)

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito. Depois de criar, empacotar e testar sua extensão, envie uma solicitação em nosso formulário de [envio de extensão](https://aka.ms/extension-request).


## Instalando node. js e ManifoldJS

As primeiras coisas que você precisará fazer é instalar [node. js LTS](https://nodejs.org/en/download/).
Depois que você tiver o nó, a partir de uma linha de comando (preferencialmente, PowerShell), execute o seguinte comando para instalar o ManifoldJS:

`npm install -g manifoldjs`

Para verificar se você instalou corretamente o ManifoldJS, execute `manifoldjs` a partir da linha de comando. Se ManifoldJS não for reconhecido, adicione `%APPDATA%\npm` às variáveis de caminho.

## Empacotamento com ManifoldJS

Para iniciar o processo de empacotamento, você precisará abrir uma linha de comando e alterar os diretórios para uma pasta que será o destino da extensão empacotada.

Por exemplo:

`cd C:\manifoldJSTest`

> [!NOTE]
> O ManifoldJS fará a saída no diretório atual e poderá substituir o conteúdo.



Agora que você está em sua pasta de destino, execute o seguinte comando:

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


Este comando pode ser dividido nas seguintes partes:
 -    **-l Debug**: altera o nível de log para "depurar" para ter uma impressão completa.
 -    **-p edgeextension**: define a única plataforma para executar a conversão em edgeextension.
 -    **-f edgeextension**: informa ao programa que o formato do manifesto é um formato edgeextension e não se importa se ele falha na validação.
 -    **-m \ < local da extensão > \manifest.JSON**: o caminho para o manifesto de extensão que você deseja converter.


Após a conclusão da execução do ManifoldJS, você terá uma pasta com o seguinte conteúdo:

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

O arquivo generationInfo. JSON é um log produzido ao executar ManifoldJS e não será incluído no seu pacote de extensão. Somente o conteúdo da pasta de **manifesto** será empacotado. Na pasta de manifesto, a pasta ativos contém as imagens que serão usadas na interface do usuário do Windows e da Microsoft Store, enquanto a pasta extensão tem o conteúdo de sua extensão dentro dela.


Agora que você tem os arquivos corretos, você precisará editar o arquivo AppXManifest gerado na pasta de **manifesto** . Se o arquivo manifest. JSON da extensão tiver uma cadeia de caracteres internacionalizada para o campo "nome", quando ManifoldJS for executado, o nome da pasta da camada mais superior não terá sublinhado e incluirá "MSG".

Por exemplo, um arquivo manifest. JSON com o seguinte `"name"` campo:

`"name" : "__MSG_appName__"`

terá uma pasta de manifesto que reside `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .

No arquivo AppXManifest, você precisará:
 -    Substitua os campos de identidade obrigatórios e o campo PublisherDisplayName conforme descrito [aqui](./creating-and-testing-extension-packages.md#app-identity-template-values). Observe que, se você estiver apenas empacotando para fins de teste ou para distribuição empresarial, poderá usar valores de espaço reservado em vez de se registrar para uma conta do centro de desenvolvimento do Windows.
 -    Substitua os ícones de espaço reservado na pasta ativos por ícones para sua extensão pelos mesmos tamanhos (150x150, 50x50, 44 x 44) e nomes. Consulte o guia de [design](./../design.md#icons-for-packaging) para obter informações sobre onde esses ícones são usados.
 - Se sua extensão for localizada, siga todo o guia de [localização de extensões do Microsoft Edge](./localizing-extension-packages.md) . Se não for localizado, leia somente o [nome de localização e a descrição na seção Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .

Depois que o arquivo appxmanifest. XML for classificado, execute o seguinte comando para criar seu pacote:

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

Agora, seu pacote estará na pasta **Package** localizada na pasta edgeextension. Consulte Criando e testando a seção de [teste](./creating-and-testing-extension-packages.md#testing-an-appx-package) de pacotes de extensão para obter informações sobre como Sideload seu novo pacote.

Depois que o pacote tiver sido testado, sinta-se à vontade para enviar uma solicitação em nosso [formulário de envio de extensão](https://aka.ms/extension-request) para ser considerado para publicação na Microsoft Store.
