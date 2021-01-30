---
description: Uma referência para recursos do WebDriver e opções específicas do Microsoft Edge com suporte do EdgeDriver (Chromium).
title: Recursos e Edgeoptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento na Web, html, css, javascript, desenvolvedor, webdriver, selenium, teste, ferramentas, automação, teste
ms.openlocfilehash: c2842740dfc6d902d1727634e00565f8e556969d
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306231"
---
# Recursos e Edgeoptions  

Recursos são opções que você pode usar para personalizar e configurar uma `EdgeDriver` sessão.  Para saber como iniciar uma nova `EdgeDriver` sessão, navegue até [Automação do Microsoft Edge.][WebdriverIndexDrivingMicrosoftEdgeChromium]  Este artigo descreve todos os recursos com suporte para [o Microsoft Edge][WebdriverIndexInstallMicrosoftEdgeChromium] e detalhes sobre como passar os recursos para `EdgeDriver` sessões.  

Os recursos são passados para uma sessão do WebDriver como um mapa JSON.  As vinculações de idioma do WebDriver normalmente fornecem métodos de conveniência seguros para tipo, para que você não precise configurar o mapa JSON por conta própria.  As diferentes vinculações de idioma do WebDriver usam mecanismos diferentes para configurar recursos.  Navegue até a documentação da [associação de idioma preferencial][WebdriverIndexChooseWebdriverLanguageBinding] para saber mais sobre como configurar recursos.  [Selenium][SeleniumMain] configura recursos por meio da `EdgeOptions` classe.  

## Usando a classe EdgeOptions  

Crie uma instância `EdgeOptions` de , que fornece métodos de conveniência para definir recursos específicos do Microsoft Edge.  Depois de configurar o `EdgeOptions` objeto, passe `EdgeOptions` para o `EdgeDriver` construtor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Para usar recursos que não têm um método de conveniência associado, use o `AddAdditionalCapability` método.  Você deve passar o nome completo da funcionalidade e um valor com o tipo correto.  Para revisar a lista completa de recursos aceitos e tipos de valor, navegue até [o objeto EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Recursos reconhecidos  

Para recursos padrão que aceitam, navegue até a documentação `EdgeDriver` [Selenium][SharedCapabilitiesSeleniumDocumentation] e o [padrão W3C WebDriver.][CapabilitiesW3cWebdriver]  Este artigo lista apenas recursos específicos do Microsoft Edge.  

## Objeto EdgeOptions  

A maioria dos recursos específicos do Microsoft Edge é exposta por meio do `EdgeOptions` objeto.  Em alguns idiomas, os recursos são implementados pela `EdgeOptions` classe.  Em outros idiomas, os recursos são armazenados no `ms:edgeOptions` dicionário em `DesiredCapabilities` .  

| Funcionalidade | Tipo | Valor padrão | Detalhes |  
|:--- |:--- |:--- |:--- |  
| args | lista de cadeias de caracteres |  | Lista de argumentos de linha de comando a ser usada ao iniciar o Microsoft Edge.  Os argumentos com um valor associado devem ser separados por um `=` sinal \(por exemplo, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \). |  
| binário | string |  | Caminho para o binário do Microsoft Edge a ser usado \(no macOS, o caminho deve ser o binário real, não apenas o aplicativo.  por exemplo, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Um endereço de um servidor de depurador ao qual se conectar, na forma `hostname/ip:port` de , por exemplo `127.0.0.1:38947` . |
| desconectar | boolean | `false` | If `false` , Microsoft Edge quits when the WebDriver service shuts down, even if the WebDriver local end hasn't closed the session.  If `true` , Microsoft Edge only quits if the WebDriver local end closes the session.  Se , e o final local do WebDriver não fechar a sessão, não limpará a pasta de dados do usuário temporária usada `true` pela instância do Microsoft `EdgeDriver` Edge. |  
| excludeSwitches | lista de cadeias de caracteres |  | Lista de opções de linha de comando do Microsoft Edge para excluir esse EdgeDriver por padrão passa ao iniciar o Microsoft Edge.  Evite o `--` prefixo para as opções. |  
| extensions | lista de cadeias de caracteres |  | Uma lista de extensões a instalar na inicialização.  Cada item na lista deve ser uma extensão empacotada codificada em base 64 \( `.crx` \). |  
| localState | dicionário |  | Um dicionário com cada entrada que consiste no nome da preferência e no valor.  As preferências são aplicadas ao arquivo estado local na pasta de dados do usuário. |  
| minidumpPath | string |  | Diretório para armazenar minidumps do Microsoft Edge.  \(Suportado somente no Linux.\) |  
| mobileEmulation | dicionário |  | Um dicionário com um valor para `deviceName` , ou valores para e `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | dicionário |  | Um dicionário opcional que especifica as preferências de log de desempenho.  para obter mais informações, navegue [até o objeto perfLoggingPrefs](#perfloggingprefs-object). |  
| prefs | dicionário |  | Um dicionário com cada entrada que consiste no nome da preferência e no valor.  As preferências são aplicadas apenas ao perfil de usuário em uso.  Para exemplos, navegue até o `Preferences` arquivo na pasta de dados do usuário do Microsoft Edge. |  
| wdpAddress | string |  | Um endereço de um servidor do Windows Device Portal ao qual você se conecta, na forma `hostname/ip:port` de , por exemplo  `127.0.0.1:50080` .  Para obter mais informações, navegue até [Depuração Remota - dispositivos Windows 10.][DevtoolsRemoteDebuggingWindows] |  
| wdpPassword | string |  | Senha opcional a ser usada ao se conectar a um servidor do Windows Device Portal.  Obrigatório se o servidor tiver a autenticação habilitada. |  
| wdpUsername | string |  | Nome de usuário opcional a ser usado ao se conectar a um servidor do Windows Device Portal.  Obrigatório se o servidor tiver a autenticação habilitada. |  
| windowsApp | string |  | ID do modelo de usuário do aplicativo de um pacote de aplicativos do Microsoft Edge para iniciar, por `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` exemplo.  Use `windowsApp` em vez de se conectar a um dispositivo Windows `binary` 10X ou emulador usando o Windows Device Portal. |  
| windowTypes | lista de cadeias de caracteres |  | Uma lista de tipos de janela que são exibidos na lista de alças de janela.  Para acessar elementos webview do Android, `webview` inclua na lista. |  

## Objeto perfLoggingPrefs  

O `perfLoggingPrefs` dicionário tem o seguinte formato \(todas as chaves são opcionais\).  

| Chave | Tipo | Valor padrão | Detalhes |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | inteiro positivo | 1000 | O número solicitado de milissegundos entre eventos de uso do buffer de rastreamento do DevTools.  Por exemplo, se 1000, uma vez por segundo, o DevTools relata o buffer de rastreamento completo.  Se um relatório indicar que o uso do buffer é 100%, um aviso será emitido. |  
| enableNetwork | boolean | true | Para coletar eventos \(ou não coletar\) do domínio de rede. |  
| enablePage | boolean | true | Para coletar eventos \(ou não coletar\) do domínio Page. |  
| traceCategories | string | \(empty\) | Uma cadeia de caracteres separada por vírgulas de categorias de rastreamento do Microsoft Edge para as quais os eventos de rastreamento devem ser coletados.  Uma cadeia de caracteres vazia ou não especificada desabilita o rastreamento. |  

## Recursos retornados  

A lista a seguir contém todos os recursos específicos do Microsoft Edge que `EdgeDriver` retornam quando você cria uma nova sessão.  

| Funcionalidade | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | A versão do EdgeDriver. |  
| msedge.userDataDir | string | O caminho para a pasta de dados do usuário usada pela instância do Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Começar a trabalhar com dispositivos Windows 10 de depuração remota | Microsoft Docs"  
[WebdriverIndexChooseWebdriverLanguageBinding]: ./index.md#choose-a-webdriver-language-binding "Escolha uma associação de idioma do WebDriver - aplicativo WebDriver (Chromium) | Microsoft Docs"
[WebdriverIndexDrivingMicrosoftEdgeChromium]: ./index.md#automating-microsoft-edge-chromium "Automatizando o Microsoft Edge (Chromium) - webdriver (Chromium) | Microsoft Docs"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Instalar o Microsoft Edge (Chromium) - Aplicativo WebDriver (Chromium) | Microsoft Docs"  

[SeleniumMain]: https://www.selenium.dev "Automação do Navegador SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Recursos compartilhados | Documentação selenium"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Recursos - Especificação do WebDriver | W3C"   
