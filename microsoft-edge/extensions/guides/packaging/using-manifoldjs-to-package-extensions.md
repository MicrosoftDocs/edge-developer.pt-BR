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
# <span data-ttu-id="bb83b-104">Usar o ManifoldJS para criar pacotes AppX de extensão</span><span class="sxs-lookup"><span data-stu-id="bb83b-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="bb83b-105">O ManifoldJS é uma ferramenta de Node.js de código aberto que permite a criação rápida e fácil de um pacote que você pode usar para envio à Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bb83b-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>  

<span data-ttu-id="bb83b-106">Se você usar o recurso de mensagens nativas em sua extensão, deverá ignorar o artigo a seguir e ir para o recurso de [mensagens nativas no Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para instruções de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="bb83b-106">If you use native messaging in your extension, you should skip the following article and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span>  

<span data-ttu-id="bb83b-107">Antes de começar, você ainda precisará ler os artigos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb83b-107">Before getting started, you will still need to read up on the following articles.</span></span>  

*   [<span data-ttu-id="bb83b-108">Extensões no Centro de Desenvolvimento do Windows</span><span class="sxs-lookup"><span data-stu-id="bb83b-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)  
*   [<span data-ttu-id="bb83b-109">Localizando pacotes de extensão</span><span class="sxs-lookup"><span data-stu-id="bb83b-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)  

> [!NOTE]
> <span data-ttu-id="bb83b-110">No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="bb83b-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="bb83b-111">Depois de criar, empacotar e testar sua extensão, envie uma solicitação em nosso formulário de [envio de extensão](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span><span class="sxs-lookup"><span data-stu-id="bb83b-111">Once you have created, packaged and tested your extension, please submit a request on our [extension submission form](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span></span>  

## <span data-ttu-id="bb83b-112">Instalando o Node.js e o ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="bb83b-112">Installing Node.js and ManifoldJS</span></span>  

<span data-ttu-id="bb83b-113">As primeiras coisas que você precisará fazer é instalar o [Node.js LTS](https://nodejs.org/en/download).</span><span class="sxs-lookup"><span data-stu-id="bb83b-113">The first things you will need to do is install [Node.js LTS](https://nodejs.org/en/download).</span></span>  
<span data-ttu-id="bb83b-114">Depois que você tiver o nó, a partir de uma linha de comando (preferencialmente, PowerShell), execute o seguinte comando para instalar o ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="bb83b-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS.</span></span>  

```shell
npm install -g manifoldjs
```  

<span data-ttu-id="bb83b-115">Para verificar se você instalou corretamente o ManifoldJS, execute `manifoldjs` a partir da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="bb83b-115">To verify that you have correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="bb83b-116">Se ManifoldJS não for reconhecido, adicione `%APPDATA%\npm` às variáveis de caminho.</span><span class="sxs-lookup"><span data-stu-id="bb83b-116">If ManifoldJS was not recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>  

## <span data-ttu-id="bb83b-117">Empacotamento com ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="bb83b-117">Packaging with ManifoldJS</span></span>  

<span data-ttu-id="bb83b-118">Para iniciar o processo de empacotamento, você precisará abrir uma linha de comando e alterar os diretórios para uma pasta que será o destino da extensão empacotada.</span><span class="sxs-lookup"><span data-stu-id="bb83b-118">To start the packaging process, you will need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>  

<span data-ttu-id="bb83b-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="bb83b-119">For example:</span></span>

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> <span data-ttu-id="bb83b-120">O `manifoldjs` comando gera no diretório atual e substitui o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bb83b-120">The `manifoldjs` command outputs in the current directory and overwrites content.</span></span>  

<span data-ttu-id="bb83b-121">Agora que você está em sua pasta de destino, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="bb83b-121">Now that you are in your destination folder, run the following command.</span></span>  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

<span data-ttu-id="bb83b-122">O `mainifoldjs` comando pode ser dividido nas partes a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb83b-122">The `mainifoldjs` command can be broken down into the following parts.</span></span>  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bb83b-123">Altera o nível de log para `debug` obter uma impressão completa.</span><span class="sxs-lookup"><span data-stu-id="bb83b-123">Changes the log level to `debug` to get a full print out.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bb83b-124">Define a única plataforma para a qual executar a conversão `edgeextension` .</span><span class="sxs-lookup"><span data-stu-id="bb83b-124">Sets the only platform to run the conversion on to `edgeextension`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bb83b-125">Informa ao programa que o formato do manifesto é um `edgeextension` formato e não se importa se ele falha na validação.</span><span class="sxs-lookup"><span data-stu-id="bb83b-125">Tells the program that the format of the manifest is an `edgeextension` format and not to care if it fails validation.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bb83b-126">O caminho para o manifesto de extensão que você deseja converter.</span><span class="sxs-lookup"><span data-stu-id="bb83b-126">The path to the extension manifest that you want to convert.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="bb83b-127">Depois que o ManifoldJS terminar de ser executado, você terá uma pasta com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb83b-127">After ManifoldJS has finished running, you will have a folder with the following contents.</span></span>  

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

<span data-ttu-id="bb83b-128">O generationInfo.jsem arquivo é um log produzido ao executar ManifoldJS e não será incluído no seu pacote de extensão.</span><span class="sxs-lookup"><span data-stu-id="bb83b-128">The generationInfo.json file is a log produced by running ManifoldJS and will not be included in your extension package.</span></span> <span data-ttu-id="bb83b-129">Somente o conteúdo da `manifest` pasta será empacotado.</span><span class="sxs-lookup"><span data-stu-id="bb83b-129">Only the contents of the `manifest` folder will be packaged.</span></span> <span data-ttu-id="bb83b-130">Na pasta de manifesto, a pasta ativos contém as imagens que serão usadas na interface do usuário do Windows e da Microsoft Store, enquanto a pasta extensão tem o conteúdo de sua extensão dentro dela.</span><span class="sxs-lookup"><span data-stu-id="bb83b-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>  

<span data-ttu-id="bb83b-131">Agora que você tem os arquivos corretos, será necessário editar o arquivo AppXManifest gerado dentro da `manifest` pasta.</span><span class="sxs-lookup"><span data-stu-id="bb83b-131">Now that you have the correct files, you will need to edit the generated AppXManifest file within the `manifest` folder.</span></span> <span data-ttu-id="bb83b-132">Se o manifest.jsdo ramal do arquivo tiver uma cadeia de caracteres internacionalizada para o campo "nome", quando ManifoldJS for executado, o nome da pasta da camada mais superior não terá sublinhado e incluirá "MSG".</span><span class="sxs-lookup"><span data-stu-id="bb83b-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="bb83b-133">Por exemplo, um manifest.jsem um arquivo com o `"name"` campo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb83b-133">For example, a manifest.json file with the following `"name"` field.</span></span>  

```shell
"name" : "__MSG_appName__"
```  

<span data-ttu-id="bb83b-134">terá uma pasta de manifesto que reside `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="bb83b-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>  

<span data-ttu-id="bb83b-135">No arquivo AppXManifest, será necessário:</span><span class="sxs-lookup"><span data-stu-id="bb83b-135">In the AppXManifest file, you will need to:</span></span>  

 *   <span data-ttu-id="bb83b-136">Substitua os campos de identidade obrigatórios e o campo PublisherDisplayName conforme descrito [aqui](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="bb83b-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="bb83b-137">Observe que, se você estiver apenas empacotando para fins de teste ou para distribuição empresarial, poderá usar valores de espaço reservado em vez de se registrar para uma conta do centro de desenvolvimento do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb83b-137">Note that if you are only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>  
 *   <span data-ttu-id="bb83b-138">Substitua os ícones de espaço reservado na pasta ativos por ícones para sua extensão pelos mesmos tamanhos (150x150, 50x50, 44 x 44) e nomes.</span><span class="sxs-lookup"><span data-stu-id="bb83b-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="bb83b-139">Consulte o guia de [design](./../design.md#icons-for-packaging) para obter informações sobre onde esses ícones são usados.</span><span class="sxs-lookup"><span data-stu-id="bb83b-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>  
 *   <span data-ttu-id="bb83b-140">Se sua extensão for localizada, siga todo o guia de [localização de extensões do Microsoft Edge](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="bb83b-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="bb83b-141">Se não estiver localizado, leia somente o [nome de localização e a descrição na seção Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="bb83b-141">If it is not localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>  

<span data-ttu-id="bb83b-142">Depois que o `appxmanifest.xml` arquivo for classificado, execute o seguinte comando para criar seu pacote.</span><span class="sxs-lookup"><span data-stu-id="bb83b-142">Once your `appxmanifest.xml` file is sorted out, run the following command to create your package.</span></span>  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

<span data-ttu-id="bb83b-143">Agora, seu pacote estará na pasta **Package** localizada na pasta edgeextension.</span><span class="sxs-lookup"><span data-stu-id="bb83b-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="bb83b-144">Para obter mais informações sobre como Sideload seu novo pacote, consulte seção [testando](./creating-and-testing-extension-packages.md#testing-an-appx-package) criando e testando pacotes de extensão.</span><span class="sxs-lookup"><span data-stu-id="bb83b-144">For more information about how to sideload your new package, see [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing extension packages.</span></span>  

<span data-ttu-id="bb83b-145">Depois que o pacote tiver sido testado, sinta-se à vontade para enviar uma solicitação em nosso [formulário de envio de extensão](https://aka.ms/extension-request) para ser considerado para publicação na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bb83b-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>  
