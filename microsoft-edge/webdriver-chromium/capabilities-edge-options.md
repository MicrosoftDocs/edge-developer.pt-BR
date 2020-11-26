---
description: Uma referência para recursos do WebDriver e opções específicas do Microsoft Edge compatíveis com o EdgeDriver (Chromium).
title: Recursos e Edgeoptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desenvolvimento na Web, HTML, CSS, JavaScript, desenvolvedor, WebDriver, Selenium, testes, ferramentas, automação, teste
ms.openlocfilehash: 1f6dca1b7ce3eb4fab3aaaab6450eee7cbf3eae5
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192237"
---
# Recursos e Edgeoptions  

Recursos são opções que você pode usar para personalizar e configurar uma `EdgeDriver` sessão.  Para iniciar uma `EdgeDriver` sessão, navegue até [dirigindo o Microsoft Edge][DrivingEdgeWebDriverIndex].  Este artigo documenta todos os recursos compatíveis com o [Microsoft Edge][DownloadEdgeWebDriverIndex] e detalhes adicionais para passar os recursos para uma `EdgeDriver` sessão.  

As associações de linguagem do WebDriver fornecem maneiras de passar recursos para `EdgeDriver` .  O mecanismo exato depende da [Associação de idioma que você escolher][ChooseLanguageBindingWebDriverIndex].  No [Selenium][SeleniumMain], as funcionalidades são fornecidas por meio da `EdgeOptions` classe.  

## Usar a classe Edgeoptions  

Crie uma instância de `EdgeOptions` , que tem métodos convenientes para configurar recursos específicos do Microsoft Edge.  Depois de configurar o `EdgeOptions` objeto, passe `EdgeOptions` para o `EdgeDriver` Construtor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Para recursos que ainda não têm um método conveniente, use o `AddAdditionalCapability` método.  Você deve saber o nome da funcionalidade e o tipo de valor que ela aceita.  Para revisar a lista completa, navegue até o [objeto edgeoptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Funcionalidades reconhecidas  

Para obter recursos padrão que `EdgeDriver` aceitam, navegue até a [documentação do Selenium][SharedCapabilitiesSeleniumDocumentation] e o [padrão W3C do WebDriver][CapabilitiesW3cWebdriver].  Este artigo só lista recursos específicos do Microsoft Edge.  

## Objeto edgeoptions  

A maioria das funcionalidades específicas do Microsoft Edge são expostas por meio do `EdgeOptions` objeto.  Em alguns idiomas, os recursos são implementados pela `EdgeOptions` classe.  Em outros idiomas, os recursos são armazenados sob o `ms:edgeOptions` dicionário em `DesiredCapabilities` .  

| Funcionalidade | Tipo | Valor padrão | Detalhes |  
|:--- |:--- |:--- |:--- |  
| args | lista de cadeias de caracteres |  | Lista de argumentos de linha de comando a serem usados ao iniciar o Microsoft Edge.  Os argumentos com um valor associado devem ser separados por um `=` sinal \ (por exemplo, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \).  |  
| biblioteca | string |  | Caminho para o binário do Microsoft Edge usar \ (no macOS, o caminho deve ser o binário real, não apenas o aplicativo.  por exemplo, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \).  |  
| Extensions | lista de cadeias de caracteres |  | Uma lista de extensões a serem instaladas na inicialização.  Cada item na lista deve ser uma extensão empacotada de base-64 \ ( `.crx` \).  |  
| localstate | dicionário |  | Um dicionário com cada entrada que consiste no nome da preferência e seu valor.  As preferências são aplicadas ao arquivo de estado local na pasta dados do usuário.  |  
| prefs | dicionário |  | Um dicionário com cada entrada que consiste no nome da preferência e seu valor.  As preferências são aplicadas apenas ao perfil de usuário em uso.  Para obter exemplos, navegue até o `Preferences` arquivo no diretório de dados do usuário do Microsoft Edge.  |  
| encaixa | booliano | false | Se falso, o Microsoft Edge fechará quando `EdgeDriver` terminar, se a sessão for encerrada ou não.  Se verdadeiro, o Microsoft Edge só será encerrado se a sessão for encerrada \ (ou fechada \).  **Observação**: se for true, e a sessão não sair, não `EdgeDriver` limpará o diretório de dados do usuário temporário usado pela instância do Microsoft Edge.  |  
| debuggerAddress | string |  | Um endereço de um servidor de depurador ao qual se conectar, na forma de <HostName/IP: Port>, por exemplo  `127.0.0.1:38947` .  |
| excludeSwitches | lista de cadeias de caracteres |  | Lista de opções de linha de comando do Microsoft Edge para excluir que o EdgeDriver por padrão é aprovado ao iniciar o Microsoft Edge.  Não Prefixe opções com `--` .  |  
| minidumpPath | string |  | Diretório para armazenar minidespejos do Microsoft Edge.  \ (Compatível apenas com Linux. \) |  
| mobileEmulation | dicionário |  | Um dicionário com um valor de `deviceName` ou valores para `deviceMetrics` and `userAgent` .  |  
| perfLoggingPrefs | dicionário |  | Um dicionário opcional que especifica as preferências de registro de desempenho.  para obter mais informações, navegue até [objeto perfLoggingPrefs](#perfloggingprefs-object).  |  
| windowTypes | lista de cadeias de caracteres |  | Uma lista de tipos de janela que são exibidos na lista de alças da janela.  Para acessar elementos da WebView Android, inclua `webview` na lista.  |  
| wdpAddress | string |  | Um endereço de um servidor do Windows Device portal ao qual você se conecta, na forma de `hostname/ip:port` , por exemplo  `127.0.0.1:50080` .  Para obter mais informações, navegue até [depuração remota-dispositivos Windows 10][DevtoolsRemoteDebuggingWindows].  |  
| wdpUsername | string |  | Nome de usuário opcional para usar quando se conectar a um servidor do Windows Device Portal.  Obrigatório se o servidor tiver a autenticação habilitada.  |  
| wdpPassword | string |  | Senha opcional para usar quando se conectar a um servidor do Windows Device Portal.  Obrigatório se o servidor tiver a autenticação habilitada.  |  
| windowsApp | string |  | ID do modelo do usuário do aplicativo de um pacote do aplicativo Microsoft Edge para iniciar, por exemplo `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Use `windowsApp` em vez de `binary` quando estiver se conectando a um dispositivo Windows 10x ou emulador usando o Windows Device Portal.  |  

## objeto perfLoggingPrefs  

O `perfLoggingPrefs` dicionário tem o seguinte formato \ (todas as chaves são opcionais \).  

| Chave | Tipo | Valor padrão | Detalhes |  
|:--- |:--- |:--- |:--- |  
| enableNetwork | boolean | true | Para coletar eventos \ (ou não coletar \) do domínio de rede.  |  
| enablePage | boolean | true | Para coletar eventos \ (ou não coletar \) do domínio da página.  |  
| traceCategories | string | \ (vazio \) | Uma cadeia de caracteres separada por vírgula das categorias de rastreamento do Microsoft Edge para as quais os eventos de rastreamento devem ser coletados.  Uma cadeia de caracteres não especificada ou vazia desabilita o rastreamento.  |  
| bufferUsageReportingInterval | inteiro positivo | 1000 | O número solicitado de milissegundos entre os eventos de uso do buffer de rastreamento do DevTools.  Por exemplo, se 1000, então uma vez por segundo, o DevTools relata como o buffer de rastreamento é completo.  Se um relatório indicar que o uso do buffer é 100%, um aviso será emitido.  |  

## Recursos retornados  

A lista a seguir contém todos os recursos específicos do Microsoft Edge que `EdgeDriver` retornam quando você cria uma nova sessão.  

| Funcionalidade | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | A versão do EdgeDriver. |  
| msedge.userDataDir | string | O caminho para o diretório de dados do usuário usado pela instância do Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introdução à depuração remota de dispositivos Windows 10 | Documentos da Microsoft"  
[DrivingEdgeWebDriverIndex]: ./index.md#driving-microsoft-edge-chromium "Dirigir o Microsoft Edge (Chromium) | Documentos da Microsoft"    
[DownloadEdgeWebDriverIndex]: ./index.md#install-microsoft-edge-chromium "Instalar o Microsoft Edge (Chromium) | Documentos da Microsoft"  
[ChooseLanguageBindingWebDriverIndex]: ./index.md#choose-a-webdriver-language-binding "Escolher uma associação de linguagem do WebDriver | Documentos da Microsoft"

[SeleniumMain]: https://www.selenium.dev "Automação do navegador SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Recursos compartilhados | Documentação do Selenium"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver/#capabilities "Recursos – especificação do WebDriver | W3C"   
