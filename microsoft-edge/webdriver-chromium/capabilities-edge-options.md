---
description: Uma referência para recursos do WebDriver e Microsoft Edge opções específicas com suporte do EdgeDriver (Chromium).
title: Recursos e Edgeoptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desenvolvimento da Web, html, css, javascript, desenvolvedor, webdriver, selenium, teste, ferramentas, automação, teste
ms.openlocfilehash: 33b9d53b72a16a9c02a03a43679137d25de0025f
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624763"
---
# <a name="capabilities-and-edgeoptions"></a>Recursos e Edgeoptions  

Recursos são opções que você pode usar para personalizar e configurar uma `EdgeDriver` sessão.  Para saber mais sobre como iniciar uma nova `EdgeDriver` sessão, navegue até [Automating Microsoft Edge][WebdriverIndexAutomateMicrosoftEdgeChromium].  Este artigo descreve todos os recursos com suporte para [Microsoft Edge][WebdriverIndexInstallMicrosoftEdgeChromium] e detalhes sobre como passar os recursos para `EdgeDriver` sessões.  

Os recursos são passados para uma sessão do WebDriver como um mapa JSON.  Uma estrutura de teste do WebDriver fornece uma associação de idioma do WebDriver.  Normalmente, as vinculações de idioma webDriver fornecem métodos de conveniência seguros de tipo para que você não precise configurar o mapa JSON por conta própria.  As diferentes vinculações de idioma do WebDriver usam mecanismos diferentes para configurar recursos.  [Selenium][SeleniumMain] configura os recursos por meio da `EdgeOptions` classe.

Para saber mais sobre como configurar recursos, consulte a documentação da estrutura de teste do WebDriver preferencial.  Para obter mais informações, navegue [até Escolher uma estrutura de teste do WebDriver.][WebdriverIndexChooseAWebdriverTestingFramework]

## <a name="using-the-edgeoptions-class"></a>Usando a classe EdgeOptions  

Crie uma instância de , que fornece métodos de conveniência `EdgeOptions` para definir Microsoft Edge recursos específicos.  Depois de configurar o `EdgeOptions` objeto, passe `EdgeOptions` para o `EdgeDriver` construtor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Para usar recursos que não tenham um método de conveniência associado, use o `AddAdditionalCapability` método.  Você deve passar o nome completo da funcionalidade e um valor com o tipo correto.  Para revisar a lista completa de recursos e tipos de valores aceitos, navegue até [o objeto EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## <a name="recognized-capabilities"></a>Recursos reconhecidos  

Para recursos padrão aceitos, navegue até a documentação `EdgeDriver` [Selenium][SharedCapabilitiesSeleniumDocumentation] e o [padrão W3C WebDriver][CapabilitiesW3cWebdriver].  Este artigo lista apenas recursos específicos Microsoft Edge.  

## <a name="edgeoptions-object"></a>Objeto EdgeOptions  

A maioria Microsoft Edge recursos específicos são expostos por meio do `EdgeOptions` objeto.  Em alguns idiomas, os recursos são implementados pela `EdgeOptions` classe.  Em outros idiomas, os recursos são armazenados no `ms:edgeOptions` dicionário em `DesiredCapabilities` .  

| Funcionalidade | Tipo | Valor padrão | Detalhes |  
|:--- |:--- |:--- |:--- |  
| args | lista de cadeias de caracteres |  | Lista de argumentos de linha de comando a ser usada ao iniciar Microsoft Edge.  Argumentos com um valor associado devem ser separados por um `=` sinal \(por exemplo, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \). |  
| binário | string |  | Caminho para o Microsoft Edge binário a ser usado \(no macOS, o caminho deve ser o binário real, não apenas o aplicativo.  por exemplo, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Um endereço de um servidor de depurador ao qual se conectar, na forma `hostname/ip:port` de , por exemplo `127.0.0.1:38947` . |
| detach | boolean | `false` | Se , Microsoft Edge encerrar quando o serviço WebDriver for desligado, mesmo que o final local do `false` WebDriver não tenha fechado a sessão.  Se `true` , Microsoft Edge encerrar somente se o final local do WebDriver fechar a sessão.  Se , e o final local do WebDriver não fechar a sessão, não limpará a pasta de dados do usuário temporário usada pela `true` `EdgeDriver` instância Microsoft Edge. |  
| excludeSwitches | lista de cadeias de caracteres |  | Lista de Microsoft Edge de linha de comando para excluir que o EdgeDriver por padrão passa ao iniciar Microsoft Edge.  Evite o `--` prefixo para comutadores. |  
| extensões | lista de cadeias de caracteres |  | Uma lista de extensões a ser instalada na inicialização.  Cada item na lista deve ser uma extensão empacotada codificada em base 64 \( `.crx` \). |  
| localState | dicionário |  | Um dicionário com cada entrada que consiste no nome da preferência e no valor.  As preferências são aplicadas ao arquivo Estado Local na pasta de dados do usuário. |  
| minidumpPath | string |  | Diretório para armazenar Microsoft Edge minidumps.  \(Suportado somente no Linux.\) |  
| mobileEmulation | dicionário |  | Um dicionário com um valor `deviceName` para , ou valores para e `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | dicionário |  | Um dicionário opcional que especifica as preferências de registro em log de desempenho.  para obter mais informações, navegue [até perfLoggingPrefs object](#perfloggingprefs-object). |  
| prefs | dicionário |  | Um dicionário com cada entrada que consiste no nome da preferência e no valor.  As preferências são aplicadas apenas ao perfil de usuário em uso.  Por exemplo, navegue até o arquivo na pasta de dados do usuário `Preferences` de Microsoft Edge. |  
| wdpAddress | string |  | Um endereço de um servidor Windows Device Portal ao qual você se conecta, na forma `hostname/ip:port` de , por exemplo `127.0.0.1:50080` .  Para obter mais informações, navegue até [Depuração Remota - Windows 10 dispositivos][DevtoolsRemoteDebuggingWindows]. |  
| wdpPassword | string |  | Senha opcional a ser usada ao se conectar a um servidor Windows Device Portal.  Obrigatório se o servidor tiver a autenticação habilitada. |  
| wdpUsername | string |  | Nome de usuário opcional a ser usado ao se conectar a um servidor Windows Device Portal.  Obrigatório se o servidor tiver a autenticação habilitada. |  
| windowsApp | string |  | ID do modelo de usuário do aplicativo de um pacote Microsoft Edge aplicativo para iniciar, por exemplo `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Use `windowsApp` em vez de se conectar a um dispositivo Windows 10X ou `binary` emulador usando Windows Device Portal. |  
| windowTypes | lista de cadeias de caracteres |  | Uma lista de tipos de janela que são exibidos na lista de alças de janela.  Para acessar os elementos webview do Android, `webview` inclua na lista. |  

## <a name="perfloggingprefs-object"></a>Objeto perfLoggingPrefs  

O `perfLoggingPrefs` dicionário tem o seguinte formato \(todas as teclas são opcionais\).  

| Chave | Tipo | Valor padrão | Detalhes |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | inteiro positivo | 1000 | O número solicitado de milissegundos entre eventos de uso de buffer de rastreamento do DevTools.  Por exemplo, se 1000, uma vez por segundo, DevTools relata o tamanho completo do buffer de rastreamento.  Se um relatório indicar que o uso do buffer é 100%, um aviso será emitido. |  
| enableNetwork | boolean | true | Para coletar \(ou não coletar\) eventos do domínio network. |  
| enablePage | boolean | true | Para coletar \(ou não coletar\) eventos do domínio Page. |  
| traceCategories | string | \(empty\) | Uma cadeia de caracteres separada por vírgulas de Microsoft Edge de rastreamento para as quais os eventos de rastreamento devem ser coletados.  Uma cadeia de caracteres vazia ou não especificada desabilita o rastreamento. |  

## <a name="returned-capabilities"></a>Recursos retornados  

A lista a seguir contém todos os recursos Microsoft Edge específicos do Microsoft Edge que `EdgeDriver` retornam quando você cria uma nova sessão.  

| Funcionalidade | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | A versão do EdgeDriver. |  
| msedge.userDataDir | string | O caminho para a pasta de dados do usuário usada pela instância Microsoft Edge usuário. |  

<!-- links -->  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Começar com a Depuração Remota Windows 10 dispositivos | Microsoft Docs"  
[WebdriverIndexChooseAWebdriverTestingFramework]: ./index.md#choose-a-webdriver-testing-framework "Escolha uma estrutura de teste do WebDriver - Use o WebDriver (Chromium) para testes de automação | Microsoft Docs"
[WebdriverIndexAutomateMicrosoftEdgeChromium]: ./index.md#automate-microsoft-edge-chromium "Automatizar Microsoft Edge (Chromium) - WebDriver (Chromium) | Microsoft Docs"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Instalar Microsoft Edge (Chromium) - WebDriver (Chromium) | Microsoft Docs"  
<!-- external links -->
[SeleniumMain]: https://www.selenium.dev "Automação do Navegador SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Recursos compartilhados | Documentação selenium"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Recursos - especificação do WebDriver | W3C"   
