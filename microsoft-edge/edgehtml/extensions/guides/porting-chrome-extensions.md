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
# <span data-ttu-id="072b6-104">Portando uma extensão do Chrome para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="072b6-104">Porting an extension from Chrome to Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="072b6-105">A portabilidade de uma extensão do Chrome para o Microsoft Edge torna-se fácil com a ajuda do [Kit de ferramentas de extensão do Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="072b6-105">Porting an extension from Chrome to Microsoft Edge is made easy with the help of the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span> <span data-ttu-id="072b6-106">Esta ferramenta de desenvolvedor converte uma extensão Chrome desempacotada em uma extensão do Microsoft Edge desempacotada, ligando APIs e faceamento quaisquer erros em seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="072b6-106">This developer tool converts an unpacked Chrome extension to an unpacked Microsoft Edge extension by bridging APIs and surfacing any errors in your `manifest.json` file.</span></span>


### <span data-ttu-id="072b6-107">Pontes de API</span><span class="sxs-lookup"><span data-stu-id="072b6-107">API bridges</span></span>
<span data-ttu-id="072b6-108">Para permitir a portabilidade transparente de APIs Chrome para APIs do Microsoft Edge com suporte, dois scripts são adicionados à pasta da extensão.</span><span class="sxs-lookup"><span data-stu-id="072b6-108">In order to allow for seamless porting of Chrome APIs to supported Microsoft Edge APIs, two scripts are added to your extension's folder.</span></span> <span data-ttu-id="072b6-109">Esses scripts são APIs de ponte (o profiling quando necessário), o que significa que você não precisa se preocupar em alterar qualquer código específico do Chrome em seu script de plano de fundo ou scripts de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="072b6-109">These scripts bridge APIs (polyfiling where necessary), meaning you won't have to worry about changing any Chrome specific code in your background script or content scripts.</span></span>

<span data-ttu-id="072b6-110">Após a conversão, você os verá incluído no arquivo de manifesto da extensão com a `"-ms-preload"` chave:</span><span class="sxs-lookup"><span data-stu-id="072b6-110">After conversion, you will see them included in the manifest file of your extension with the `"-ms-preload"` key:</span></span>

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## <span data-ttu-id="072b6-111">Usar o kit de ferramentas de extensão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="072b6-111">Using the Microsoft Edge Extension Toolkit</span></span>

<span data-ttu-id="072b6-112">As instruções a seguir detalham como converter a extensão Chrome para executar no Microsoft Edge na edição de aniversário do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="072b6-112">The following instructions detail how to convert your Chrome extension to run on Microsoft Edge in the Windows 10 Anniversary Update edition:</span></span>

1. <span data-ttu-id="072b6-113">Instale o [Kit de ferramentas de extensão do Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="072b6-113">Install the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span>
2. <span data-ttu-id="072b6-114">Faça uma cópia da pasta da extensão do Chrome para manter a segurança.</span><span class="sxs-lookup"><span data-stu-id="072b6-114">Make a copy of your Chrome extension's folder for safe keeping.</span></span> <span data-ttu-id="072b6-115">O processo de conversão substituirá o código.</span><span class="sxs-lookup"><span data-stu-id="072b6-115">The conversion process will overwrite the code.</span></span> 
3. <span data-ttu-id="072b6-116">Execute o kit de ferramentas de extensão do Microsoft Edge e carregue a cópia da extensão.</span><span class="sxs-lookup"><span data-stu-id="072b6-116">Run the Microsoft Edge Extension Toolkit and load the copy of your extension.</span></span>  
 ![botão carregar extensão](./../media/save-folder.png)
4. <span data-ttu-id="072b6-118">Corrija todos os erros relatados no editor de texto da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="072b6-118">Correct all the errors that are reported within the tool's text editor.</span></span> <span data-ttu-id="072b6-119">Selecione "revalidar" para verificar se há erros após fazer correções.</span><span class="sxs-lookup"><span data-stu-id="072b6-119">Select "Re-validate" to check for errors after making corrections.</span></span>  
 ![extensão – erros ao localizar o kit de ferramentas](./../media/extension-toolkit.png)
5. <span data-ttu-id="072b6-121">Selecione "salvar arquivos".</span><span class="sxs-lookup"><span data-stu-id="072b6-121">Select "Save files".</span></span>

<span data-ttu-id="072b6-122">Agora você pode sair do kit de ferramentas e carregar a extensão no Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="072b6-122">You can now exit out of the toolkit and load your extension in Microsoft Edge!</span></span> 

<span data-ttu-id="072b6-123">Você pode pesquisar problemas de plataforma conhecidos com o [controlador de problemas do EdgeHTML](http://issues.microsoftedge.com).</span><span class="sxs-lookup"><span data-stu-id="072b6-123">You can search for known platform issues with the [EdgeHTML issue tracker](http://issues.microsoftedge.com).</span></span> <span data-ttu-id="072b6-124">Se você acha que encontrou algo novo, [abra um problema](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span><span class="sxs-lookup"><span data-stu-id="072b6-124">If you think you've found something new, [open an issue](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span></span>
