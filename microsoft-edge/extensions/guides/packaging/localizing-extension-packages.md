---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Saiba como localizar seu pacote de extensão do Microsoft Edge para que ele esteja pronto para várias localidades durante o lançamento.
title: Localizando pacotes de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: a6a920b80e915bb14c7ea24abcc54105e5b34eb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561177"
---
# <span data-ttu-id="07489-104">Localizando extensões do Microsoft Edge para Windows e a Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="07489-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="07489-105">Este guia percorre como localizar sua extensão do Microsoft Edge para que ele esteja pronto para várias localidades durante o lançamento.</span><span class="sxs-lookup"><span data-stu-id="07489-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span> <span data-ttu-id="07489-106">Para localizar completamente sua extensão, você precisará seguir as etapas para o Windows e para a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="07489-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>

<span data-ttu-id="07489-107">Se quiser localizar seus recursos de extensão para o Microsoft Edge, você pode aprender a usar a estrutura de i18n no [Guia de internacionalização](../internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="07489-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>


> [!NOTE]
> <span data-ttu-id="07489-108">Se a extensão não oferecer suporte a vários idiomas, você poderá ignorar [o nome e a descrição da localização na Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="07489-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>


## <span data-ttu-id="07489-109">A visão geral do processo de localização</span><span class="sxs-lookup"><span data-stu-id="07489-109">The localization process overview</span></span>

<span data-ttu-id="07489-110">A primeira etapa para obter a extensão disponível para um público largo é [Configurar o AppxManifest](#configuring-the-appxmanifest) para vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="07489-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span> <span data-ttu-id="07489-111">Na Microsoft Store, isso mostrará aos usuários quais idiomas sua extensão oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="07489-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span> <span data-ttu-id="07489-112">Certos campos na AppxManifest também precisarão ser alterados se você quiser que o nome de sua extensão seja [localizado na interface do usuário do Windows e na Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="07489-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>


<span data-ttu-id="07489-113">Depois de configurar o AppxManifest, você precisará [criar recursos de cadeia de caracteres JSON](#creating-json-string-resources) para os idiomas que você indicou como suportados.</span><span class="sxs-lookup"><span data-stu-id="07489-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span> <span data-ttu-id="07489-114">Isso requer a criação de um arquivo. resjson para cada idioma, em que cada arquivo tem todas as cadeias de caracteres da interface do usuário do idioma dentro dele.</span><span class="sxs-lookup"><span data-stu-id="07489-114">This requires creating a .resjson file for each language, where each file has all the UI strings of that language within it.</span></span>


<span data-ttu-id="07489-115">Após a criação dos arquivos. resjson para os idiomas com suporte, [será necessário criar um arquivo de recursos. pri](#creating-the-resources-file).</span><span class="sxs-lookup"><span data-stu-id="07489-115">After the .resjson files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="07489-116">Isso será criado usando um arquivo de configuração para a ferramenta **MakePRI** que vem com o [SDK do Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="07489-116">This will be created by using a configuration file to the **MakePRI** tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> 

> [!NOTE]
> <span data-ttu-id="07489-117">Se você estiver baixando o SDK do Windows 10 para usar a ferramenta MakePri. exe, poderá selecionar apenas os recursos "ferramentas de assinatura do SDK do Windows para aplicativos da área de trabalho" e "SDK do Windows para aplicativos da UWP gerenciados" para manter o download mais claro.</span><span class="sxs-lookup"><span data-stu-id="07489-117">If you are only downloading the Windows 10 SDK to use the MakePri.exe tool, you can select only the "Windows SDK Signing Tools for Desktop Apps" and "Windows SDK for UWP Managed Apps" features to keep the download lighter.</span></span> <span data-ttu-id="07489-118">A ferramenta MakePri. exe será exibida em subpastas de C:\Program Files (x86) \Windows Kits\10\bin\10.0.17713.0.</span><span class="sxs-lookup"><span data-stu-id="07489-118">The MakePri.exe tool will appear in subfolders of C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0.</span></span>


<span data-ttu-id="07489-119">Depois de carregar a extensão, a etapa final será [localizar o nome e a descrição na Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="07489-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>

> [!NOTE]
> <span data-ttu-id="07489-120">No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="07489-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="07489-121">Entre [em contato conosco](https://aka.ms/extension-request) com suas solicitações para fazer parte da Microsoft Store, e consideraremos você para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="07489-121">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>



## <span data-ttu-id="07489-122">Configurando o AppXManifest</span><span class="sxs-lookup"><span data-stu-id="07489-122">Configuring the AppXManifest</span></span>

<span data-ttu-id="07489-123">A lista de "idiomas com suporte" da extensão na Microsoft Store é gerada com base em seus valores de AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="07489-123">Your extension's "Supported languages" list in the Microsoft Store is generated based on its AppXManifest values.</span></span> <span data-ttu-id="07489-124">Essa lista é especificada usando o `Resource` elemento.</span><span class="sxs-lookup"><span data-stu-id="07489-124">This list is specified using the `Resource` element.</span></span>


![imagem de configurações](./../../media/language-app-details.png)

<span data-ttu-id="07489-126">Para especificar a lista de idiomas com suporte na sua extensão, você pode adicionar um `Resource` elemento no formato visto abaixo (esse `Resource` elemento mostrará o suporte para inglês, alemão e francês na Microsoft Store):</span><span class="sxs-lookup"><span data-stu-id="07489-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below (this `Resource` element will show support for English, German, and French in the Microsoft Store):</span></span>

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

<span data-ttu-id="07489-127">Consulte [idiomas com suporte](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) para obter informações sobre os idiomas/códigos de idioma com suporte na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="07489-127">See [Supported languages](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>


<span data-ttu-id="07489-128">Para especificar cadeias de caracteres localizadas para todos os elementos publicamente visíveis no AppxManifest, você precisará usar um identificador de recurso no formato de `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="07489-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>

<span data-ttu-id="07489-129">Os snippets abaixo fazem uma AppxManifest completa.</span><span class="sxs-lookup"><span data-stu-id="07489-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="07489-130">Os seguintes valores devem ser recuperados de arquivos de recursos localizados:</span><span class="sxs-lookup"><span data-stu-id="07489-130">The following values should be retrieved from localized resource files:</span></span>

- <span data-ttu-id="07489-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="07489-131">Properties\DisplayName</span></span>
- <span data-ttu-id="07489-132">Properties\Description</span><span class="sxs-lookup"><span data-stu-id="07489-132">Properties\Description</span></span>
- <span data-ttu-id="07489-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="07489-133">Properties\PublisherDisplayName</span></span>


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- <span data-ttu-id="07489-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="07489-134">Applications\Application\VisualElements\DisplayName</span></span>
- <span data-ttu-id="07489-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="07489-135">Applications\Application\VisualElements\Description</span></span>
- <span data-ttu-id="07489-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="07489-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```


## <span data-ttu-id="07489-137">Localizando recursos de extensão para Windows e a Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="07489-137">Localizing extension resources for Windows and the Microsoft Store</span></span>

<span data-ttu-id="07489-138">Agora que o AppxManifest está configurado para vários idiomas, há algumas diferenças importantes que você deve saber entre localizar a interface do usuário dentro da extensão e localizar sua extensão para Windows e a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="07489-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>

<span data-ttu-id="07489-139">Embora as extensões do Microsoft Edge não sejam executadas fora do Microsoft Edge, o gerenciamento delas pode ocorrer dentro do Windows.</span><span class="sxs-lookup"><span data-stu-id="07489-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span> <span data-ttu-id="07489-140">Por exemplo, os usuários podem gerenciar as extensões no aplicativo configurações:</span><span class="sxs-lookup"><span data-stu-id="07489-140">For example, users can manage their extensions in the Settings app:</span></span>


![imagem de configurações](./../../media/settings.png)



<span data-ttu-id="07489-142">O nome da extensão que aparece no aplicativo Configurações do Windows vem do AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="07489-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span> <span data-ttu-id="07489-143">Se esse valor for codificado em inglês, a versão em inglês do nome aparecerá em dispositivos Windows que não estejam em inglês.</span><span class="sxs-lookup"><span data-stu-id="07489-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span> <span data-ttu-id="07489-144">Se a identidade visual da extensão for somente em inglês, não há problema em deixá-la codificada.</span><span class="sxs-lookup"><span data-stu-id="07489-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>


> [!NOTE]
> <span data-ttu-id="07489-145">Se você quiser usar nomes localizados para a extensão do Microsoft Edge no Windows, certifique-se de que os nomes localizados também estejam [disponíveis e reservados](./extensions-in-the-windows-dev-center.md#name-reservation) antes de fazer as alterações no arquivo AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="07489-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span> <span data-ttu-id="07489-146">Se os nomes não forem reservados, você receberá o seguinte erro ao carregar o pacote final para o centro de desenvolvimento do Windows:</span><span class="sxs-lookup"><span data-stu-id="07489-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span></br></br>

![erro de idioma](./../../media/language-error.png)</br></br>


<span data-ttu-id="07489-148">A infraestrutura de localização baseada em i18n definida para extensões JavaScript só se aplica dentro do ambiente Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="07489-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>

<span data-ttu-id="07489-149">Fora do Microsoft Edge, no Windows e na Microsoft Store, a única estrutura de localização com suporte é baseada na estrutura de localização da plataforma universal do Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="07489-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>

<span data-ttu-id="07489-150">Enquanto damos suporte a recursos baseados em JSON para aplicativos do Windows baseados em HTML, o esquema dos recursos JSON não corresponde a um definido para extensões JavaScript.</span><span class="sxs-lookup"><span data-stu-id="07489-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>


<span data-ttu-id="07489-151">Estas são as principais diferenças em [aplicativos do Windows baseados em HTML](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span><span class="sxs-lookup"><span data-stu-id="07489-151">The following are the key differences in [HTML based Windows apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span></span>
-    <span data-ttu-id="07489-152">Os recursos são especificados em arquivos. resjson em vez de arquivos. JSON.</span><span class="sxs-lookup"><span data-stu-id="07489-152">Resources are specified in .resjson files instead of .json files.</span></span>
-    <span data-ttu-id="07489-153">As localidades com suporte devem ser especificadas no arquivo AppXManifest, com a primeira localidade sendo a localidade padrão.</span><span class="sxs-lookup"><span data-stu-id="07489-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>
-    <span data-ttu-id="07489-154">Os recursos de aplicativos baseados em HTML do Windows usam o seguinte esquema:</span><span class="sxs-lookup"><span data-stu-id="07489-154">HTML based Windows apps resources use the following schema:</span></span>
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    <span data-ttu-id="07489-155">O par nome/valor indicado por um sublinhado é um comentário para o recurso de cadeia de caracteres correspondente.</span><span class="sxs-lookup"><span data-stu-id="07489-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>
-    <span data-ttu-id="07489-156">os arquivos. resjson são compilados em arquivos. pri que devem ser incluídos durante a criação do pacote AppX.</span><span class="sxs-lookup"><span data-stu-id="07489-156">.resjson files are compiled into .pri files which must be included during AppX package creation.</span></span>


### <span data-ttu-id="07489-157">Criando recursos de cadeia de caracteres JSON</span><span class="sxs-lookup"><span data-stu-id="07489-157">Creating JSON string resources</span></span>
<span data-ttu-id="07489-158">Com uma AppxManifest configurada em mãos e as diferenças entre as estruturas de localização da i18n e da UWP realçadas, você está pronto para criar seus arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="07489-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>

<span data-ttu-id="07489-159">Apenas uma cadeia de caracteres de recurso no manifesto se aplica aos pacotes de extensão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="07489-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span> <span data-ttu-id="07489-160">`DisplayName`Geralmente, a cadeia de caracteres é localizada em extensões JavaScript e pode ser facilmente mapeada para os arquivos. resjson esperados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="07489-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the .resjson files that Windows expects.</span></span> <span data-ttu-id="07489-161">Pressupondo que este seja o único recurso que você gostaria de localizar, aqui está um arquivo. resjson de exemplo que deve ser criado:</span><span class="sxs-lookup"><span data-stu-id="07489-161">Assuming that this is the only resource that you would like to localize, here is a sample .resjson file that should be created:</span></span>

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

<span data-ttu-id="07489-162">A ID do recurso em cada arquivo. resjson precisa corresponder à identificação usada no AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="07489-162">The resource ID in each .resjson file needs to match the ID used in the AppXManifest.</span></span> <span data-ttu-id="07489-163">Usando o trecho de exemplo de resjson acima, a entrada AppXManifest correspondente deve ser:</span><span class="sxs-lookup"><span data-stu-id="07489-163">Using the example .resjson snippet above, the corresponding AppXManifest entry should be:</span></span>

`DisplayName="ms-resource:DisplayName"`

<span data-ttu-id="07489-164">Cada idioma compatível com a extensão deve ter um arquivo Resources. resjson correspondente e ser colocado na seguinte estrutura de pastas:</span><span class="sxs-lookup"><span data-stu-id="07489-164">Each language that your extension supports should have a corresponding resources.resjson file and be placed in the following folder structure:</span></span>

![estrutura da pasta de idiomas](./../../media/resources-folder.png)


### <span data-ttu-id="07489-166">Criando o arquivo de recursos</span><span class="sxs-lookup"><span data-stu-id="07489-166">Creating the resources file</span></span>
<span data-ttu-id="07489-167">Depois de criar todos os arquivos. resjson, você estará pronto para criar seu arquivo de índice de recursos de pacote (PRI).</span><span class="sxs-lookup"><span data-stu-id="07489-167">Once you've created all your .resjson files, you're ready to create your package resource index (PRI) file.</span></span> <span data-ttu-id="07489-168">Esse arquivo armazena os recursos de todos os idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="07489-168">This file stores the resources for all your supported languages.</span></span> <span data-ttu-id="07489-169">Para fazer isso, você pode usar a ferramenta **MakePRI** incluída com o SDK do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="07489-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>


<span data-ttu-id="07489-170">Primeiro, você precisará criar o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="07489-170">First you'll need to create the configuration file.</span></span> <span data-ttu-id="07489-171">Isso define os qualificadores e a plataforma padrão para os recursos.</span><span class="sxs-lookup"><span data-stu-id="07489-171">This defines the default qualifiers and platform for the resources.</span></span> <span data-ttu-id="07489-172">Para este exemplo, torne o idioma padrão Inglês (EUA) e a plataforma Windows 10.</span><span class="sxs-lookup"><span data-stu-id="07489-172">For this example, make the default language English (US) and the platform Windows 10.</span></span> <span data-ttu-id="07489-173">Para fazer isso, crie um arquivo priconfig. XML com o seguinte conteúdo na [pasta raiz]:</span><span class="sxs-lookup"><span data-stu-id="07489-173">To do this, create a priconfig.xml file with the following content in the [Root folder]:</span></span>

![priconfig na pasta](./../../media/priconfig.png)


```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```

<span data-ttu-id="07489-175">Agora você pode usar o arquivo de configuração e a ferramenta MakePRI para criar o arquivo Resources. pri.</span><span class="sxs-lookup"><span data-stu-id="07489-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span> <span data-ttu-id="07489-176">Para este exemplo, o local raiz para o projeto será [pasta raiz].</span><span class="sxs-lookup"><span data-stu-id="07489-176">For this example, the root location for the project will be [Root folder].</span></span>


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

<span data-ttu-id="07489-177">Agora você deve ter um arquivo Resources. pri na sua pasta raiz:</span><span class="sxs-lookup"><span data-stu-id="07489-177">You should now have one resources.pri file in your root folder:</span></span>

![pasta recursos](./../../media/resources.png)


## <span data-ttu-id="07489-179">Localizando o nome e a descrição na Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="07489-179">Localizing name and description in the Microsoft Store</span></span>

<span data-ttu-id="07489-180">Depois de tentar carregar o pacote completo e localizado, o centro de desenvolvimento do Windows detectará se há mais de um idioma com suporte e verificará se você tem descrições e nomes localizados correspondentes para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="07489-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span> <span data-ttu-id="07489-181">Se algum dos valores localizados estiver ausente, o envio será bloqueado até você fornecer os valores.</span><span class="sxs-lookup"><span data-stu-id="07489-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>

<span data-ttu-id="07489-182">Se você estiver interessado apenas em fornecer um nome localizado e uma descrição para a Microsoft Store (e não para Windows), é possível fazer isso, [reservindo todos os nomes localizados para a extensão](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="07489-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>


<span data-ttu-id="07489-183">Depois de reservar nomes localizados adicionais, você pode criar um envio atualizado.</span><span class="sxs-lookup"><span data-stu-id="07489-183">Once you've reserved additional localized names, you can create an updated submission.</span></span> <span data-ttu-id="07489-184">Na seção Descrição, você pode gerenciar idiomas adicionais para a listagem da Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="07489-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>

![Descrição do aplicativo japonês](./../../media/manage-description-languages.png)

<span data-ttu-id="07489-186">Depois de selecionar "gerenciar idiomas adicionais", você terá que selecionar quais idiomas deseja adicionar à listagem da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="07489-186">Once you've selected "Manage additional languages", you'll get to select which languages you want to add to your Microsoft Store listing.</span></span> <span data-ttu-id="07489-187">O novo idioma será exibido como ' idioma de descrição adicional ' na seção "Descrição".</span><span class="sxs-lookup"><span data-stu-id="07489-187">The new language will show up as 'Additional description language' in the "Description" section.</span></span>

<span data-ttu-id="07489-188">Você pode clicar no link individual na seção "Descrição" para fornecer um nome localizado e uma descrição, notas de versão e ativos visuais para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="07489-188">You can click on the individual link in the "Description" section to provide a localized name and description, release notes, and visual assets for each language.</span></span> <span data-ttu-id="07489-189">A descrição da Microsoft Store não é extraída da AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="07489-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span> <span data-ttu-id="07489-190">Cada descrição localizada precisa ser inserida manualmente no centro de desenvolvimento do Windows:</span><span class="sxs-lookup"><span data-stu-id="07489-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>

![Descrição do aplicativo japonês](./../../media/japanese-app-description.png)

<span data-ttu-id="07489-192">Depois que as descrições localizadas são enviadas e a extensão é publicada, qualquer pessoa que acesse uma página localizada da extensão na Microsoft Store irá ver a seguinte interface do usuário:</span><span class="sxs-lookup"><span data-stu-id="07489-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>

![Windows Store japonês](./../../media/japanese-windows-store.png)
 

## <span data-ttu-id="07489-194">Exemplos de AppxManifest</span><span class="sxs-lookup"><span data-stu-id="07489-194">AppxManifest samples</span></span>

### <span data-ttu-id="07489-195">AppxManifest não localizado</span><span class="sxs-lookup"><span data-stu-id="07489-195">Non-localized AppxManifest</span></span>
<span data-ttu-id="07489-196">O exemplo a seguir mostra um AppxManifest que não está localizado e só tem suporte para a localidade "en-US".</span><span class="sxs-lookup"><span data-stu-id="07489-196">The following example shows an AppxManifest that isn't localized, and only supports the "en-us" locale.</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```


#### <span data-ttu-id="07489-197">AppxManifest localizado</span><span class="sxs-lookup"><span data-stu-id="07489-197">Localized AppxManifest</span></span>
<span data-ttu-id="07489-198">Este exemplo de AppxManifest é localizado para oito outros locais além de "en-US".</span><span class="sxs-lookup"><span data-stu-id="07489-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="07489-199">Observe as `ms-resource:<resource id>` ocorrências:</span><span class="sxs-lookup"><span data-stu-id="07489-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```
