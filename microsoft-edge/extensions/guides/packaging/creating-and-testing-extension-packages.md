---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Saiba mais sobre como empacotar a extensão do Microsoft Edge manualmente e testá-la para ver se ela está empacotada corretamente.
title: Criando e testando pacotes de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, empacotamento
ms.custom: seodec18
ms.openlocfilehash: a76737d76c8f08c8e79992f0804fdbd34d4ed970
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561182"
---
# Criando e testando um pacote AppX de extensão do Microsoft Edge  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

As extensões do Microsoft Edge são empacotadas como AppX, semelhante à forma como os aplicativos universais do Windows são empacotados. Desde a atualização de aniversário do Windows 10, foi introduzido um novo esquema para AppX que permite que um AppX inclua uma extensão do Microsoft Edge como conteúdo.

Se você já sabe como a extensão do Microsoft Edge AppXs é criada, você pode ignorar o [uso do ManifoldJS para a extensão do pacote](./using-manifoldjs-to-package-extensions.md) para aprender a usar uma ferramenta baseada em node. js para fazer tudo isso para você!

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito. Depois de criar, empacotar e testar sua extensão, envie uma solicitação em nosso formulário de [envio de extensão](https://aka.ms/extension-request).



## Preparando a pasta de envio

Para preparar a extensão para envio, você precisa criar uma pasta com a seguinte estrutura:

![imagem da estrutura da pasta. Na pasta minha extensão é AppxManifest. xml, pasta de extensão e ativos](./../../media/packaging_folder-structure.png)

Na raiz da pasta, você deve incluir um arquivo AppXManifest. xml. Esse arquivo é usado para especificar o conteúdo e o layout do pacote.

Você também deve ter uma pasta de ativos que contém os ativos de interface do usuário a serem usados na Microsoft Store e uma pasta de extensão que contém os arquivos da extensão (scripts, ícones etc.).

> [!IMPORTANT]
> Você pode criar uma estrutura de pastas diferente para o pacote, mas a estrutura de pastas deve corresponder aos valores de AppXManifest.

### AppXManifest. xml
O arquivo AppXManifest é um documento XML que contém informações que o sistema precisa para implantar, exibir ou atualizar um aplicativo do Windows. Esse arquivo também inclui a identidade do pacote, recursos e elementos visuais. Cada pacote de aplicativo deve incluir um arquivo AppXManifest.

Os desenvolvedores podem usar o modelo a seguir para o arquivo AppXManifest. xml:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
  xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
  xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
  xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
  IgnorableNamespaces="uap3">

  <Identity
    Name="[REPLACE WITH PACKAGE/IDENTITYNAME]"
    Publisher="[REPLACE WITH PACKAGE/IDENTITY/PUBLISHER]"
    Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]"/>

  <Properties>
    <DisplayName>[REPLACE WITH RESERVED STORE NAME]</DisplayName>
    <PublisherDisplayName>[REPLACE WITH PACKAGE/PROPERTIES/PUBLISHERDISPLAYNAME]</PublisherDisplayName>
    <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
  </Properties>

  <Dependencies>
    <TargetDeviceFamily Name="Windows.Desktop"
      MinVersion="10.0.14393.0"
      MaxVersionTested="10.0.14800.0" />
  </Dependencies>

  <Resources>
    <Resource Language="en-us"/>
  </Resources>

  <Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
        DisplayName="[REPLACE WITH RESERVED STORE NAME]"
        Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
        Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
        Description="This is the description of the extension"
        BackgroundColor="white">
      </uap:VisualElements>
    <Extensions>
    <uap3:Extension Category="windows.appExtension">
    <uap3:AppExtension Name="com.microsoft.edge.extension"
        Id="EdgeExtension"
        PublicFolder="Extension"
      DisplayName="[REPLACE WITH RESERVED STORE NAME]">
    </uap3:AppExtension>
    </uap3:Extension>
    </Extensions>
 </Application>
</Applications>
</Package>
```

#### Valores do modelo de identidade do aplicativo
Depois de [reservar o nome de sua extensão](./extensions-in-the-windows-dev-center.md#name-reservation) por meio do centro de desenvolvimento do Windows, você poderá encontrar as informações necessárias de identidade do pacote necessárias para substituir os seguintes valores no AppXManifest. xml:

- `Name`
- `Publisher`
- `DisplayName`
- `PublisherDisplayName`

Você pode acessar a página de identidade do aplicativo usando as seguintes etapas:

1. Navegue até o [centro de desenvolvimento do Windows](https://developer.microsoft.com/windows/).
2. Conecte-se à sua conta de desenvolvedor.
3. Navegue até o painel.
4. Selecione o nome da sua extensão.

   ![lista de extensões](./../../media/select-app.png)
5. Navegue até a página identidade do aplicativo que está na seção Gerenciamento de aplicativos (após você ter registrado o aplicativo).

   ![página identidade do aplicativo](./../../media/app-identity.png)


Agora você pode preencher o modelo AppXManifest com valores da página identidade do aplicativo, conforme indicado no modelo:


```xml
<Identity
  Name="37369abigailc.MyExtension"
  Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
  Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]" />

<Properties>
  <DisplayName>My Extension</DisplayName>
  <PublisherDisplayName>abigailc</PublisherDisplayName>
  <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
</Properties>
```

#### Valores de modelo de manifesto JSON
Alguns valores no AppXManifest precisam corresponder àqueles definidos no manifesto JSON. Atualize os seguintes valores no appxmanifest. XML com base em seu manifesto JSON de extensão:

- `Version` -Esta é a versão listada no manifesto JSON de extensão. A cadeia de caracteres precisa coincidir com o formato X. X. X. X em que o último inteiro precisa ser 0. Ex. 1.2.3.0

   ```xml
   <Identity
     Name="37369abigailc.MyExtension"
     Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
     Version="1.0.0.0" />
   ```

- `Description` -Esta é uma cópia da descrição no manifesto JSON de extensão.

  ```xml
  <uap:VisualElements
    AppListEntry="none"
    DisplayName="My Extension"
    Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
    Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
    Description="This extension will allow you to quickly print by clicking the browser action."
    BackgroundColor="white">
  </uap:VisualElements>
  ```


### Pasta ativos

Na pasta ativos, você precisará de três tamanhos de ícone diferentes. Esses ícones serão usados na Microsoft Store e na interface do usuário do Windows. Para obter mais informações sobre esses ícones, consulte o guia de [design](./../design.md#icons-for-packaging) .

![pasta ativos com três tamanhos de ícone](./../../media/assets-folder.png)

Depois de criar os ativos de interface do usuário necessários, atualize AppXManifest. xml para apontar para os arquivos corretos:

- 44x44

   ```xml
   Square44x44Logo="Assets/icon_44.png"
   ```

- 50x50

  ```xml
   <Logo>Assets/icon_50.png</Logo>
  ```

- 150x150

  ```xml
  Square150x150Logo="Assets/icon_150.png"
  ```


### Pasta de extensão
Copie os arquivos de extensão (mantendo a estrutura de pastas) para a pasta de extensão. Certifique-se `manifest.json` de que esteja na pasta raiz de extensão.

![pasta de extensão com todos os arquivos de extensão](./../../media/extension-folder.png)


### Suporte a mais de uma localidade
Se a extensão oferecer suporte a mais de um idioma, talvez você queira configurar o pacote AppX com todas as localidades necessárias para que o ícone e a descrição corretos localizados sejam exibidos na Microsoft Store. Para saber mais, consulte [localizando pacotes de extensão](./localizing-extension-packages.md) para obter mais informações.

### Criando um Appx

Para criar um Appx, você precisará encontrar o caminho para makeappx. Isso geralmente está localizado no seguinte local se você estiver em um computador de 64 bits.

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

Execute o seguinte comando para criar o pacote AppX para sua extensão:

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

Isso deve ter uma aparência assim que você preencher os caminhos:

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### Descompactar um Appx
Você pode querer descompactar um AppX gerado anteriormente e usá-lo como ponto de partida para a próxima iteração da extensão ou para confirmar que o AppX foi criado corretamente.

Para fazer isso, você pode executar o seguinte comando para descompactar o pacote AppX da extensão do Microsoft Edge:

`[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]`

Isso deve ser algo assim quando preenchido:

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"`





## Testando um pacote AppX

Você pode testar o pacote AppX da extensão do Microsoft Edge fazendo o Sideload no Microsoft Edge. Sideload o pacote AppX de extensão é semelhante ao Sideload de um aplicativo universal do Windows. Será necessário criar um certificado para assinar o pacote e, em seguida, adicionar o pacote ao Windows.

### Assinou

Veja [como criar um certificado de assinatura de pacote de aplicativo](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) e [como assinar um pacote de aplicativo usando Signtool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) para obter informações sobre o processo de autenticação e certificação para pacotes.

> [!NOTE]
> Você não precisa assinar um pacote de extensão antes de enviá-lo para a Microsoft Store; o processo de inclusão da loja cuidará disso para você.

Depois de assinar o pacote com o certificado que você criou, o certificado ainda não é confiável para a máquina local para a implantação de pacotes de aplicativos até que você o instale no repositório de certificados confiáveis do computador local. Você pode usar o Certutil. exe, que vem com o Windows, para fazer isso.

Para instalar certificados com o WindowsCertutil. exe, execute cmd. exe como administrador e execute o seguinte comando:

`Certutil -addStore TrustedPeople MyKey.cer`

Depois que os certificados não estiverem mais em uso, recomendamos que você os remova executando o seguinte comando em um prompt de comando de administrador:

`Certutil -delStore TrustedPeople certID`

O certid é o número de série do certificado. Para determinar o número de série do certificado, execute o seguinte comando:

`Certutil -store TrustedPeople`

### Implantando
Você pode implantar o pacote AppX da extensão do Microsoft Edge executando o seguinte comando no PowerShell (como administrador):

`Add-AppxPackage [path to AppX]`

## Teste automatizado com o WebDriver

Desde a atualização de aniversário, você pode Sideload programaticamente a sua extensão no Microsoft Edge com o WebDriver, permitindo o teste automatizado de extensões quando o Microsoft Edge for iniciado no modo WebDriver. Isso permitirá que você configure testes automatizados para qualquer extensão que manipule conteúdo em uma página e verifique se o comportamento correto está sendo exibido.

Para Sideload a extensão do teste automatizado, você precisará armazenar a pasta da extensão em `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` . Depois que sua extensão estiver no `LocalState` diretório, você precisará criar um [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) objeto e adicionar a `extensionPaths` funcionalidade a ele. O valor dessa funcionalidade é uma matriz de caminhos absolutos para as extensões (no `LocalState` diretório) que você deseja que o lado seja carregado quando o Microsoft Edge iniciar no modo WebDriver.

Confira o seguinte [arquivo em C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) para obter um exemplo completo sobre extensões de carregamento lado a lado do Microsoft Edge com WebDriver.
