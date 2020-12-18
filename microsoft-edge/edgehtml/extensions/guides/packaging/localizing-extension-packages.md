---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Saiba como localizar seu pacote de extensão do Microsoft Edge para que ele esteja pronto para várias localidades durante o lançamento.
title: Localizando pacotes de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cfa85eda47fd71099bb5d201d1cf85992931228c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231825"
---
# Localizando extensões do Microsoft Edge para Windows e a Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Este guia percorre como localizar sua extensão do Microsoft Edge para que ele esteja pronto para várias localidades durante o lançamento. Para localizar completamente sua extensão, você precisará seguir as etapas para o Windows e para a Microsoft Store.

Se quiser localizar seus recursos de extensão para o Microsoft Edge, você pode aprender a usar a estrutura de i18n no [Guia de internacionalização](../internationalization.md).


> [!NOTE]
> Se a extensão não oferecer suporte a vários idiomas, você poderá ignorar [o nome e a descrição da localização na Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).


## A visão geral do processo de localização

A primeira etapa para obter a extensão disponível para um público largo é [Configurar o AppxManifest](#configuring-the-appxmanifest) para vários idiomas. Na Microsoft Store, isso mostrará aos usuários quais idiomas sua extensão oferece suporte. Certos campos na AppxManifest também precisarão ser alterados se você quiser que o nome de sua extensão seja [localizado na interface do usuário do Windows e na Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).


Depois de configurar o AppxManifest, você precisará [criar recursos de cadeia de caracteres JSON](#creating-json-string-resources) para os idiomas que você indicou como suportados. Isso requer a criação de um arquivo. resjson para cada idioma, em que cada arquivo tem todas as cadeias de caracteres da interface do usuário do idioma dentro dele.


Após a criação dos arquivos. resjson para os idiomas com suporte, [será necessário criar um arquivo de recursos. pri](#creating-the-resources-file). Isso será criado usando um arquivo de configuração para a ferramenta **MakePRI** que vem com o [SDK do Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk). 

> [!NOTE]
> Se você estiver baixando o SDK do Windows 10 para usar a ferramenta MakePri.exe, poderá selecionar apenas os recursos "ferramentas de assinatura do SDK do Windows para aplicativos da área de trabalho" e "SDK do Windows para aplicativos da UWP Managed" para manter o download mais claro. A ferramenta MakePri.exe aparecerá em subpastas de C:\Program Files (x86) \Windows Kits\10\bin\10.0.17713.0.


Depois de carregar a extensão, a etapa final será [localizar o nome e a descrição na Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito. Entre [em contato conosco](https://aka.ms/extension-request) com suas solicitações para fazer parte da Microsoft Store, e consideraremos você para uma atualização futura.



## Configurando o AppXManifest

A lista de "idiomas com suporte" da extensão na Microsoft Store é gerada com base em seus valores de AppXManifest. Essa lista é especificada usando o `Resource` elemento.


![imagem das configurações – detalhes do aplicativo de linguagem](./../../media/language-app-details.png)

Para especificar a lista de idiomas com suporte na sua extensão, você pode adicionar um `Resource` elemento no formato visto abaixo (esse `Resource` elemento mostrará o suporte para inglês, alemão e francês na Microsoft Store):

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

Consulte [idiomas com suporte](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) para obter informações sobre os idiomas/códigos de idioma com suporte na Microsoft Store.


Para especificar cadeias de caracteres localizadas para todos os elementos publicamente visíveis no AppxManifest, você precisará usar um identificador de recurso no formato de `ms-resource:<resource id>` .

Os snippets abaixo fazem uma AppxManifest completa. Os seguintes valores devem ser recuperados de arquivos de recursos localizados:

- Properties\DisplayName
- Properties\Description
- Properties\PublisherDisplayName


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- Applications\Application\VisualElements\DisplayName
- Applications\Application\VisualElements\Description
- Applications\Application\Extensions\Extension\AppExtension\DisplayName

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


## Localizando recursos de extensão para Windows e a Microsoft Store

Agora que o AppxManifest está configurado para vários idiomas, há algumas diferenças importantes que você deve saber entre localizar a interface do usuário dentro da extensão e localizar sua extensão para Windows e a Microsoft Store.

Embora as extensões do Microsoft Edge não sejam executadas fora do Microsoft Edge, o gerenciamento delas pode ocorrer dentro do Windows. Por exemplo, os usuários podem gerenciar as extensões no aplicativo configurações:


![imagem de configurações](./../../media/settings.png)



O nome da extensão que aparece no aplicativo Configurações do Windows vem do AppXManifest. Se esse valor for codificado em inglês, a versão em inglês do nome aparecerá em dispositivos Windows que não estejam em inglês. Se a identidade visual da extensão for somente em inglês, não há problema em deixá-la codificada.


> [!NOTE]
> Se você quiser usar nomes localizados para a extensão do Microsoft Edge no Windows, certifique-se de que os nomes localizados também estejam [disponíveis e reservados](./extensions-in-the-windows-dev-center.md#name-reservation) antes de fazer as alterações no arquivo AppXManifest. Se os nomes não forem reservados, você receberá o seguinte erro ao carregar o pacote final para o centro de desenvolvimento do Windows:</br></br>

![erro de idioma](./../../media/language-error.png)</br></br>


A infraestrutura de localização baseada em i18n definida para extensões JavaScript só se aplica dentro do ambiente Microsoft Edge.

Fora do Microsoft Edge, no Windows e na Microsoft Store, a única estrutura de localização com suporte é baseada na estrutura de localização da plataforma universal do Windows (UWP).

Enquanto damos suporte a recursos baseados em JSON para aplicativos do Windows baseados em HTML, o esquema dos recursos JSON não corresponde a um definido para extensões JavaScript.


Estas são as principais diferenças em [aplicativos do Windows baseados em HTML](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):
-    Os recursos são especificados em arquivos. resjson em vez de arquivos. JSON.
-    As localidades com suporte devem ser especificadas no arquivo AppXManifest, com a primeira localidade sendo a localidade padrão.
-    Os recursos de aplicativos baseados em HTML do Windows usam o seguinte esquema:
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    O par nome/valor indicado por um sublinhado é um comentário para o recurso de cadeia de caracteres correspondente.
-    os arquivos. resjson são compilados em arquivos. pri que devem ser incluídos durante a criação do pacote AppX.


### Criando recursos de cadeia de caracteres JSON
Com uma AppxManifest configurada em mãos e as diferenças entre as estruturas de localização da i18n e da UWP realçadas, você está pronto para criar seus arquivos de recursos.

Apenas uma cadeia de caracteres de recurso no manifesto se aplica aos pacotes de extensão do Microsoft Edge. `DisplayName`Geralmente, a cadeia de caracteres é localizada em extensões JavaScript e pode ser facilmente mapeada para os arquivos. resjson esperados pelo Windows. Pressupondo que este seja o único recurso que você gostaria de localizar, aqui está um arquivo. resjson de exemplo que deve ser criado:

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

A ID do recurso em cada arquivo. resjson precisa corresponder à identificação usada no AppXManifest. Usando o trecho de exemplo de resjson acima, a entrada AppXManifest correspondente deve ser:

`DisplayName="ms-resource:DisplayName"`

Cada idioma compatível com a extensão deve ter um arquivo Resources. resjson correspondente e ser colocado na seguinte estrutura de pastas:

![estrutura da pasta de idiomas](./../../media/resources-folder.png)


### Criando o arquivo de recursos
Depois de criar todos os arquivos. resjson, você estará pronto para criar seu arquivo de índice de recursos de pacote (PRI). Esse arquivo armazena os recursos de todos os idiomas com suporte. Para fazer isso, você pode usar a ferramenta **MakePRI** incluída com o SDK do Windows 10.


Primeiro, você precisará criar o arquivo de configuração. Isso define os qualificadores e a plataforma padrão para os recursos. Para este exemplo, torne o idioma padrão Inglês (EUA) e a plataforma Windows 10. Para fazer isso, crie um arquivo priconfig.xml com o seguinte conteúdo na [pasta raiz]:

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

Agora você pode usar o arquivo de configuração e a ferramenta MakePRI para criar o arquivo Resources. pri. Para este exemplo, o local raiz para o projeto será [pasta raiz].


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

Agora você deve ter um arquivo Resources. pri na sua pasta raiz:

![pasta recursos](./../../media/resources.png)


## Localizando o nome e a descrição na Microsoft Store

Depois de tentar carregar o pacote completo e localizado, o centro de desenvolvimento do Windows detectará se há mais de um idioma com suporte e verificará se você tem descrições e nomes localizados correspondentes para cada um deles. Se algum dos valores localizados estiver ausente, o envio será bloqueado até você fornecer os valores.

Se você estiver interessado apenas em fornecer um nome localizado e uma descrição para a Microsoft Store (e não para Windows), é possível fazer isso, [reservindo todos os nomes localizados para a extensão](./extensions-in-the-windows-dev-center.md#name-reservation).


Depois de reservar nomes localizados adicionais, você pode criar um envio atualizado. Na seção Descrição, você pode gerenciar idiomas adicionais para a listagem da Microsoft Store:

![Descrição do aplicativo japonês-gerenciar](./../../media/manage-description-languages.png)

Depois de selecionar "gerenciar idiomas adicionais", você terá que selecionar quais idiomas deseja adicionar à listagem da Microsoft Store. O novo idioma será exibido como ' idioma de descrição adicional ' na seção "Descrição".

Você pode clicar no link individual na seção "Descrição" para fornecer um nome localizado e uma descrição, notas de versão e ativos visuais para cada idioma. A descrição da Microsoft Store não é extraída da AppXManifest. Cada descrição localizada precisa ser inserida manualmente no centro de desenvolvimento do Windows:

![Descrição do aplicativo japonês](./../../media/japanese-app-description.png)

Depois que as descrições localizadas são enviadas e a extensão é publicada, qualquer pessoa que acesse uma página localizada da extensão na Microsoft Store irá ver a seguinte interface do usuário:

![Windows Store japonês](./../../media/japanese-windows-store.png)
 

## Exemplos de AppxManifest

### AppxManifest não localizado
O exemplo a seguir mostra um AppxManifest que não está localizado e só tem suporte para a localidade "en-US".


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


#### AppxManifest localizado
Este exemplo de AppxManifest é localizado para oito outros locais além de "en-US". Observe as `ms-resource:<resource id>` ocorrências:


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
