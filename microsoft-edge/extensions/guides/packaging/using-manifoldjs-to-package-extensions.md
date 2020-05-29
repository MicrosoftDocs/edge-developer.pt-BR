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
# <span data-ttu-id="448a7-104">Usar o ManifoldJS para criar pacotes AppX de extensão</span><span class="sxs-lookup"><span data-stu-id="448a7-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="448a7-105">ManifoldJS é uma ferramenta de nó de origem aberta. js que permite a criação rápida e fácil de um pacote que você pode usar para envio à Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="448a7-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>

<span data-ttu-id="448a7-106">Se você usar o recurso de mensagens nativas em sua extensão, deverá ignorar isso e ir para o recurso de [mensagens nativas no Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para instruções de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="448a7-106">If you use native messaging in your extension, you should skip this and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span> 

<span data-ttu-id="448a7-107">Antes de começar, você ainda precisa ler os artigos a seguir:</span><span class="sxs-lookup"><span data-stu-id="448a7-107">Before getting started, you will still need to read up on the following articles:</span></span>

- [<span data-ttu-id="448a7-108">Extensões no centro de desenvolvimento do Windows</span><span class="sxs-lookup"><span data-stu-id="448a7-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)
- [<span data-ttu-id="448a7-109">Localizando pacotes de extensão</span><span class="sxs-lookup"><span data-stu-id="448a7-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)

> [!NOTE]
> <span data-ttu-id="448a7-110">No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="448a7-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="448a7-111">Depois de criar, empacotar e testar sua extensão, envie uma solicitação em nosso formulário de [envio de extensão](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="448a7-111">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>


## <span data-ttu-id="448a7-112">Instalando node. js e ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="448a7-112">Installing Node.js and ManifoldJS</span></span>

<span data-ttu-id="448a7-113">As primeiras coisas que você precisará fazer é instalar [node. js LTS](https://nodejs.org/en/download/).</span><span class="sxs-lookup"><span data-stu-id="448a7-113">The first things you'll need to do is install [Node.js LTS](https://nodejs.org/en/download/).</span></span>
<span data-ttu-id="448a7-114">Depois que você tiver o nó, a partir de uma linha de comando (preferencialmente, PowerShell), execute o seguinte comando para instalar o ManifoldJS:</span><span class="sxs-lookup"><span data-stu-id="448a7-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS:</span></span>

`npm install -g manifoldjs`

<span data-ttu-id="448a7-115">Para verificar se você instalou corretamente o ManifoldJS, execute `manifoldjs` a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="448a7-115">To verify that you've correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="448a7-116">Se ManifoldJS não for reconhecido, adicione `%APPDATA%\npm` às variáveis de caminho.</span><span class="sxs-lookup"><span data-stu-id="448a7-116">If ManifoldJS wasn't recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>

## <span data-ttu-id="448a7-117">Empacotamento com ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="448a7-117">Packaging with ManifoldJS</span></span>

<span data-ttu-id="448a7-118">Para iniciar o processo de empacotamento, você precisará abrir uma linha de comando e alterar os diretórios para uma pasta que será o destino da extensão empacotada.</span><span class="sxs-lookup"><span data-stu-id="448a7-118">To start the packaging process, you'll need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>

<span data-ttu-id="448a7-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="448a7-119">For example:</span></span>

`cd C:\manifoldJSTest`

> [!NOTE]
> <span data-ttu-id="448a7-120">O ManifoldJS fará a saída no diretório atual e poderá substituir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="448a7-120">ManifoldJS will output in the current directory and can overwrite content.</span></span>



<span data-ttu-id="448a7-121">Agora que você está em sua pasta de destino, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="448a7-121">Now that you're in your destination folder, run the following command:</span></span>

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


<span data-ttu-id="448a7-122">Este comando pode ser dividido nas seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="448a7-122">This command can be broken down into the following parts:</span></span>
 -    <span data-ttu-id="448a7-123">**-l Debug**: altera o nível de log para "depurar" para ter uma impressão completa.</span><span class="sxs-lookup"><span data-stu-id="448a7-123">**-l debug**: Changes the log level to "debug" to get a full print out.</span></span>
 -    <span data-ttu-id="448a7-124">**-p edgeextension**: define a única plataforma para executar a conversão em edgeextension.</span><span class="sxs-lookup"><span data-stu-id="448a7-124">**-p edgeextension**: Sets the only platform to run the conversion on to edgeextension.</span></span>
 -    <span data-ttu-id="448a7-125">**-f edgeextension**: informa ao programa que o formato do manifesto é um formato edgeextension e não se importa se ele falha na validação.</span><span class="sxs-lookup"><span data-stu-id="448a7-125">**-f edgeextension**: Tells the program that the format of the manifest is an edgeextension format and not to care if it fails validation.</span></span>
 -    <span data-ttu-id="448a7-126">**-m \ < local da extensão > \manifest.JSON**: o caminho para o manifesto de extensão que você deseja converter.</span><span class="sxs-lookup"><span data-stu-id="448a7-126">**-m \<EXTENSION LOCATION>\manifest.json**: The path to the extension manifest that you want to convert.</span></span>


<span data-ttu-id="448a7-127">Após a conclusão da execução do ManifoldJS, você terá uma pasta com o seguinte conteúdo:</span><span class="sxs-lookup"><span data-stu-id="448a7-127">After ManifoldJS has finished running, you'll have a folder with the following contents:</span></span>

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

<span data-ttu-id="448a7-128">O arquivo generationInfo. JSON é um log produzido ao executar ManifoldJS e não será incluído no seu pacote de extensão.</span><span class="sxs-lookup"><span data-stu-id="448a7-128">The generationInfo.json file is a log produced by running ManifoldJS and won't be included in your extension package.</span></span> <span data-ttu-id="448a7-129">Somente o conteúdo da pasta de **manifesto** será empacotado.</span><span class="sxs-lookup"><span data-stu-id="448a7-129">Only the contents of the **manifest** folder will be packaged.</span></span> <span data-ttu-id="448a7-130">Na pasta de manifesto, a pasta ativos contém as imagens que serão usadas na interface do usuário do Windows e da Microsoft Store, enquanto a pasta extensão tem o conteúdo de sua extensão dentro dela.</span><span class="sxs-lookup"><span data-stu-id="448a7-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>


<span data-ttu-id="448a7-131">Agora que você tem os arquivos corretos, você precisará editar o arquivo AppXManifest gerado na pasta de **manifesto** .</span><span class="sxs-lookup"><span data-stu-id="448a7-131">Now that you have the correct files, you'll need to edit the generated AppXManifest file within the **manifest** folder.</span></span> <span data-ttu-id="448a7-132">Se o arquivo manifest. JSON da extensão tiver uma cadeia de caracteres internacionalizada para o campo "nome", quando ManifoldJS for executado, o nome da pasta da camada mais superior não terá sublinhado e incluirá "MSG".</span><span class="sxs-lookup"><span data-stu-id="448a7-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="448a7-133">Por exemplo, um arquivo manifest. JSON com o seguinte `"name"` campo:</span><span class="sxs-lookup"><span data-stu-id="448a7-133">For example, a manifest.json file with the following `"name"` field:</span></span>

`"name" : "__MSG_appName__"`

<span data-ttu-id="448a7-134">terá uma pasta de manifesto que reside `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="448a7-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>

<span data-ttu-id="448a7-135">No arquivo AppXManifest, você precisará:</span><span class="sxs-lookup"><span data-stu-id="448a7-135">In the AppXManifest file, you'll need to:</span></span>
 -    <span data-ttu-id="448a7-136">Substitua os campos de identidade obrigatórios e o campo PublisherDisplayName conforme descrito [aqui](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="448a7-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="448a7-137">Observe que, se você estiver apenas empacotando para fins de teste ou para distribuição empresarial, poderá usar valores de espaço reservado em vez de se registrar para uma conta do centro de desenvolvimento do Windows.</span><span class="sxs-lookup"><span data-stu-id="448a7-137">Note that if you're only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>
 -    <span data-ttu-id="448a7-138">Substitua os ícones de espaço reservado na pasta ativos por ícones para sua extensão pelos mesmos tamanhos (150x150, 50x50, 44 x 44) e nomes.</span><span class="sxs-lookup"><span data-stu-id="448a7-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="448a7-139">Consulte o guia de [design](./../design.md#icons-for-packaging) para obter informações sobre onde esses ícones são usados.</span><span class="sxs-lookup"><span data-stu-id="448a7-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>
 - <span data-ttu-id="448a7-140">Se sua extensão for localizada, siga todo o guia de [localização de extensões do Microsoft Edge](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="448a7-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="448a7-141">Se não for localizado, leia somente o [nome de localização e a descrição na seção Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="448a7-141">If it isn't localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>

<span data-ttu-id="448a7-142">Depois que o arquivo appxmanifest. XML for classificado, execute o seguinte comando para criar seu pacote:</span><span class="sxs-lookup"><span data-stu-id="448a7-142">Once your appxmanifest.xml file is sorted out, run the following command to create your package:</span></span>

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

<span data-ttu-id="448a7-143">Agora, seu pacote estará na pasta **Package** localizada na pasta edgeextension.</span><span class="sxs-lookup"><span data-stu-id="448a7-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="448a7-144">Consulte Criando e testando a seção de [teste](./creating-and-testing-extension-packages.md#testing-an-appx-package) de pacotes de extensão para obter informações sobre como Sideload seu novo pacote.</span><span class="sxs-lookup"><span data-stu-id="448a7-144">See Creating and testing extension packages' [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section for info on how to sideload your new package.</span></span>

<span data-ttu-id="448a7-145">Depois que o pacote tiver sido testado, sinta-se à vontade para enviar uma solicitação em nosso [formulário de envio de extensão](https://aka.ms/extension-request) para ser considerado para publicação na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="448a7-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>
