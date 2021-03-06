---
description: Saiba como localizar o pacote de extensão do Microsoft Edge para que ele esteja pronto para várias localidades após a versão.
title: Localizando pacotes de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5dd21f82fd746ad619e9d89a1526ff6a511d615
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397717"
---
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a>Localizando extensões do Microsoft Edge para Windows e Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Este guia explica como localizar sua extensão do Microsoft Edge para que ela esteja pronta para várias localidades após a versão.  Para localização completa da extensão, você precisará seguir as etapas do Windows e da Microsoft Store.  

Se quiser localizar seus recursos de extensão para o Microsoft Edge, saiba como usar a estrutura i18n no guia [Internacionalização.](../internationalization.md)  

> [!NOTE]
> Se sua extensão não tiver suporte para vários idiomas, você poderá ignorar o nome e a descrição de localização [na Microsoft Store.](#localizing-name-and-description-in-the-microsoft-store)  

## <a name="the-localization-process-overview"></a>Visão geral do processo de localização  

A primeira etapa para disponibilizar sua extensão para uma ampla audiência é configurar seu [AppxManifest](#configuring-the-appxmanifest) para vários idiomas.  Na Microsoft Store, isso mostrará aos usuários quais idiomas sua extensão oferece suporte.  Determinados campos no AppxManifest também precisarão ser alterados se você quiser que o nome da sua extensão seja localizado na interface do usuário do Windows e [na Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).  

Depois que o AppxManifest estiver configurado, você precisará criar recursos de cadeia de caracteres [JSON](#creating-json-string-resources) para os idiomas que você indicou como suportados.  Isso requer a criação de um arquivo para cada idioma, onde cada arquivo tem todas as cadeias de caracteres de interface do usuário `.resjson` desse idioma dentro dele.  

Depois que os arquivos dos idiomas com suporte foram feitos, um arquivo de recurso `.resjson` [.pri precisará ser criado](#creating-the-resources-file). Isso será criado usando um arquivo de configuração para a ferramenta MakePRI que vem com o [SDK do Windows 10.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)  

> [!NOTE]
> Se você estiver baixando apenas o SDK do Windows 10 para usar a ferramenta, poderá selecionar apenas as Ferramentas de Assinatura do SDK do Windows para Aplicativos de Área de Trabalho e o SDK do Windows para recursos do Aplicativo Gerenciado `MakePri.exe` **UWP** para manter o download mais claro. ****  A `MakePri.exe` ferramenta aparecerá em subpastas de `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` .  

Depois de carregar sua extensão, a etapa final é localizar o nome e a [descrição na Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).  

> [!NOTE]
> No momento, enviar uma extensão do Microsoft Edge à Microsoft Store é um recurso restrito.  **Entre em contato conosco com** suas solicitações para fazer parte da Microsoft Store e consideraremos você para uma atualização futura.  

## <a name="configuring-the-appxmanifest"></a>Configurando o AppXManifest  

A lista de idiomas com suporte da sua extensão na Microsoft Store é gerada com base em seus valores AppXManifest.  Essa lista é especificada usando o `Resource` elemento.  

![Detalhes do aplicativo](../../media/language-app-details.png)  

Para especificar a lista de idiomas que são suportados pela extensão, você pode adicionar um elemento no formato visto abaixo \(este elemento mostrará suporte para inglês, alemão e francês na `Resource` `Resource` Microsoft Store\):  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

Consulte [Idiomas com suporte para](/windows/uwp/publish/supported-languages) obter informações sobre os códigos de idiomas/idiomas compatíveis com a Microsoft Store.  

Para especificar cadeias de caracteres localizadas para todos os elementos visíveis publicamente no AppxManifest, você terá que usar um identificador de recurso no formato `ms-resource:<resource id>` de .  

Os trechos abaixo fazem um AppxManifest completo. Os seguintes valores devem ser recuperados de arquivos de recursos localizados:  

*   Properties\DisplayName  
*   Properties\Description  
*   Properties\PublisherDisplayName  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   Applications\Application\VisualElements\DisplayName  
*   Applications\Application\VisualElements\Description  
*   Applications\Application\Extensions\Extension\AppExtension\DisplayName  

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

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a>Localizando recursos de extensão para Windows e a Microsoft Store  

Agora que seu AppxManifest está configurado para vários idiomas, há algumas diferenças importantes que você deve saber entre a localização da interface do usuário em sua extensão e a localização de sua extensão para Windows e a Microsoft Store.  

Embora as extensões do Microsoft Edge não são executados fora do Microsoft Edge, o gerenciamento delas pode ocorrer no Windows.  Por exemplo, os usuários podem gerenciar suas extensões no aplicativo Configurações:  

![aplicativo settings](../../media/settings.png)  

O nome da extensão que aparece no aplicativo Configurações no Windows vem do AppXManifest.  Se esse valor for hardcoded em inglês, a versão em inglês do nome será aparecer em dispositivos Windows que não sejam inglês.  Se a identidade visual da extensão for somente em inglês, não há problema em deixá-la codificada.  

> [!NOTE]
> Se você quiser usar nomes localizados para o Microsoft Edge Extension no [](./extensions-in-the-windows-dev-center.md#name-reservation) Windows, certifique-se de que os nomes localizados também estão disponíveis e reservados antes de fazer as alterações no arquivo AppXManifest.  Se os nomes não são reservados, você obterá o seguinte erro ao carregar o pacote final no Centro de Dev do Windows:  
> 
> ![erro de idioma](../../media/language-error.png)  

A infraestrutura de localização baseada em i18n definida para extensões JavaScript só é aplicável no ambiente do Microsoft Edge.  

Fora do Microsoft Edge, no Windows e na Microsoft Store, a única estrutura de localização com suporte é baseada na estrutura de localização da Plataforma Universal do Windows (UWP).  

Embora suportemos recursos baseados em JSON para aplicativos windows baseados em HTML, o esquema para os recursos JSON não é igual ao definido para extensões JavaScript.  

Veja a seguir as principais diferenças em [aplicativos baseados em HTML do Windows:](/previous-versions/windows/apps/hh465228(v=win.10))  

*   Os recursos são especificados em `.resjson` arquivos em vez de `.json` arquivos.  
*   As localidades com suporte devem ser especificadas no arquivo AppXManifest, com a primeira localidade sendo a localidade padrão.  
*   Os recursos de aplicativos do Windows baseados em HTML usam o seguinte esquema:  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    O par nome/valor denotado por um sublinhado são comentários para o recurso de cadeia de caracteres correspondente.  
*   `.resjson` os arquivos são compilados em `.pri` arquivos que devem ser incluídos durante a criação do pacote AppX.  
    
### <a name="creating-json-string-resources"></a>Criando recursos de cadeia de caracteres JSON  

Com um AppxManifest configurado em mãos e as diferenças entre as estruturas de localização i18n e UWP realçadas, você está pronto para criar seus arquivos de recursos.  

Somente uma cadeia de caracteres de recurso no manifesto é aplicável aos pacotes de extensão do Microsoft Edge.  A cadeia de caracteres é geralmente localizada em extensões JavaScript e pode ser facilmente mapeada para os `DisplayName` arquivos que o Windows `.resjson` espera.  Supondo que esse seja o único recurso que você gostaria de localização, aqui está um arquivo de `.resjson` exemplo que deve ser criado:  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

A ID do recurso em cada `.resjson` arquivo precisa corresponder à ID usada no AppXManifest.  Usando o `.resjson` trecho de exemplo acima, a entrada appXManifest correspondente deve ser:  

`DisplayName="ms-resource:DisplayName"`  

Cada idioma compatível com sua extensão deve ter um arquivo de recursos correspondente e `.resjson` ser colocado na seguinte estrutura de pastas:  

![estrutura de pasta de idioma](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a>Criando o arquivo de recursos  

Depois de criar todos os seus arquivos, você estará pronto para criar seu arquivo de índice de recursos do pacote `.resjson` \(PRI\).  Esse arquivo armazena os recursos de todos os idiomas com suporte.  Para fazer isso, você pode usar a **ferramenta MakePRI** que está incluída no SDK do Windows 10.  

Primeiro, você precisará criar o arquivo de configuração.  Isso define os qualificadores padrão e a plataforma para os recursos.  Para este exemplo, faça o idioma padrão `English (US)` e a plataforma Windows 10.  Para fazer isso, crie `priconfig.xml` um arquivo com o seguinte conteúdo no `[Root folder]` :  

![priconfig na pasta](../../media/priconfig.png)  

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

Agora você pode usar o arquivo de configuração e a ferramenta MakePRI para criar o arquivo resources.pri.  Para este exemplo, o local raiz do projeto será `[Root folder]` .  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

Agora você deve ter um arquivo resources.pri em sua pasta raiz:  

![pasta resources](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a>Nome e descrição de localização na Microsoft Store  

Depois de tentar carregar seu pacote completo localizado, o Centro de Desenvolvimento do Windows detectará que há suporte para mais de um idioma e verificará se você tem nomes e descrições localizadas correspondentes para cada um deles.  Se algum dos valores localizados estiver ausente, seu envio será bloqueado até que você forneça os valores.  

Se você estiver interessado apenas em fornecer um nome e uma descrição localizados para a Microsoft Store (e não o Windows), você pode fazer isso [reservando](./extensions-in-the-windows-dev-center.md#name-reservation)todos os nomes localizados para sua extensão .  

Depois de ter reservado nomes localizados adicionais, você pode criar um envio atualizado.  Na seção descrição, você pode gerenciar idiomas adicionais para sua listagem da Microsoft Store:  

![Gerenciar idiomas de descrição](../../media/manage-description-languages.png)  

Depois de selecionar **Gerenciar idiomas**adicionais, você poderá selecionar quais idiomas deseja adicionar à sua listagem da Microsoft Store.  O novo idioma será aparecer como **idioma de descrição adicional** na seção **Descrição.**  

Você pode clicar no link individual na seção **Descrição** para fornecer um nome e uma descrição localizados, notas de versão e ativos visuais para cada idioma.  A descrição da Microsoft Store não é extraída do AppXManifest.  Cada descrição localizada precisa ser inserida manualmente no Centro de Desenvolvimento do Windows:  

![Descrição do aplicativo japonês](../../media/japanese-app-description.png)  

Depois que as descrições localizadas são enviadas e a extensão é publicada, qualquer pessoa acessando uma página localizada da extensão na Microsoft Store verá a interface do usuário a seguir:  

![windows store japonês](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a>Exemplos de AppxManifest  

### <a name="non-localized-appxmanifest"></a>AppxManifest não localizado  

O exemplo a seguir mostra um AppxManifest que não está localizado e dá suporte apenas à `en-us` localidade.  

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

#### <a name="localized-appxmanifest"></a>AppxManifest localizado  

Este exemplo appxManifest é localizado para outras oito localidades além de "en-us". Observe as `ms-resource:<resource id>` ocorrências:  

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
