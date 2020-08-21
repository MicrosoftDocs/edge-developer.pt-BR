---
title: Códigos de erro para aplicativos do Windows Runtime usando JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- JavaScript, Windows Runtime error codes
- VS.WebClient.Help.APPHOST9601
- VS.WebClient.Help.APPHOST9602
- VS.WebClient.Help.APPHOST9603
- VS.WebClient.Help.APPHOST9604
- VS.WebClient.Help.APPHOST9605
- VS.WebClient.Help.APPHOST9606
- VS.WebClient.Help.APPHOST9607
- VS.WebClient.Help.APPHOST9608
- VS.WebClient.Help.APPHOST9610
- VS.WebClient.Help.APPHOST9611
- VS.WebClient.Help.APPHOST9613
- VS.WebClient.Help.APPHOST9614
- VS.WebClient.Help.APPHOST9615
- VS.WebClient.Help.APPHOST9616
- VS.WebClient.Help.APPHOST9617
- VS.WebClient.Help.APPHOST9618
- VS.WebClient.Help.APPHOST9619
- VS.WebClient.Help.APPHOST9620
- VS.WebClient.Help.APPHOST9623
- VS.WebClient.Help.APPHOST9624
- VS.WebClient.Help.APPHOST9626
ms.assetid: 4c6d4e90-602a-4b56-ae74-3458929da442
caps.latest.revision: 1
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7779da61da9f011e55eeb496c7332e5b7cd5a023
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942154"
---
# Códigos de erro para aplicativos do Windows Runtime usando JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Veja a seguir os códigos de erro exibidos pelo console do Microsoft Visual Studio ao desenvolver aplicativos do Windows Runtime usando JavaScript.  

| Erro | Comentários |  
|:--- |:--- |  
| APPHOST9601: "não é possível carregar o *remoteURI*.  Um aplicativo não pode carregar conteúdo da Web remoto no contexto local. " | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "' JavaScript: ' é um valor de atributo inválido e será ignorado.  Não use URIs ' JavaScript: ' no contexto local. " | Por motivos de segurança, você não pode usar URIs ' JavaScript: ' no contexto local.  Para obter mais informações sobre o que é permitido no contexto local, consulte [recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "não é possível carregar o plug-in do ActiveX que tem a ID de classe *ClassID*.  Os aplicativos não conseguem carregar controles ActiveX. " | Os aplicativos do Windows Runtime que usam JavaScript não são compatíveis com o Microsoft ActiveXcontrols personalizado.  Se você precisar de um controle de interface do usuário, use um controle da Web padrão, uma biblioteca de controles ou crie seu próprio controle personalizado.  Se você precisar executar uma lógica personalizada, crie um objeto do Windows Runtime personalizado em vez disso.  Para obter informações sobre outras diferenças em HTML, CSS e JavaScript, consulte [recursos HTML, CSS e JavaScript e diferenças][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "não é possível navegar para *URI* porque ele usa uma codificação de caracteres inválida.  Um aplicativo pode navegar somente para arquivos com codificação UTF8. " | Todos os códigos HTML, JavaScript e CSS acessados por um tempo de execução do Windows devem ser codificados como UTF-8 (Unicode Transformation Format) de 8 bits.  Para obter informações sobre outras diferenças em HTML, CSS e JavaScript, consulte [recursos HTML, CSS e JavaScript e diferenças][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "não é possível navegar para *targetURI* do *SOURCEURI* porque o URI de destino está em uma zona de segurança mais alta.  Você não pode navegar de uma zona com menos segurança para uma zona com segurança mais alta, a menos que você esteja navegando para um URI de contexto local de um URI de contexto da Web e você tenha registrado o URI de contexto local com o método MSApp. addPublicLocalApplicationUri. " | Para obter mais informações, consulte [MSApp. addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: "não é possível carregar o *URI* porque ele usa uma conexão http e o metaelemento MS-https-Connections-only está presente.  Somente conexões HTTPS são permitidas quando você usa o metaelemento MS-https-Connections-only.  Use uma conexão HTTPS ou, se você não precisar de uma conexão segura, remova o elemento meta. " | Para obter mais informações, consulte [como exigir uma conexão HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "o aplicativo não pode iniciar o URI em *URI* devido a este erro: *failureCode*." | Um recurso ausente ou um arquivo inválido são causas comuns desse erro.  |  
| APPHOST9608: "o aplicativo não pôde navegar para a página About: Blank devido a este erro: *ErrorCode*." |  |  

| Erro | Comentários |  
|:--- |:--- |  
| APPHOST9610: "o aplicativo encontrou um erro ao se preparar para navegar para uma página de erro personalizada: *ErrorCode*." |  |  
| APPHOST9611: "o aplicativo não pôde navegar para uma página de erro personalizada devido a este erro: *ErrorCode*." |  |  
| APPHOST9613: "o aplicativo não pôde navegar para *URI*  devido a este erro: *ErrorCode*." |  |  
| APPHOST9614: "um documento dentro de um iframe solicitou o modo de documento *requestedDocMode* , mas o sistema impõe o modo de *currentDocMode* doc.  O iframe usará o modo de documento *currentDocMode* . " | Para obter mais informações sobre como exibir o conteúdo remoto da Web, consulte [como vincular a páginas externas da Web][PreviousVersionsWindowsAppsHh780594].  |  
| APPHOST9615: "o aplicativo não pode baixar o arquivo em *URI* porque ele foi invocado de forma programática fora do contexto local." | Ocorre quando o conteúdo do contexto da Web tenta baixar um arquivo programaticamente.  |  
| APPHOST9616: "esse URI não pode usar APIs de localização geográfica.  APIs de localização geográfica podem ser invocadas apenas de um URI que faz parte do pacote ou está incluída no elemento ApplicationContentUris do manifesto. " | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: "esse URI não pode usar APIs da área de transferência.  As APIs da área de transferência podem ser invocadas apenas a partir de um URI que faz parte do pacote ou está incluída no elemento ApplicationContentUris do manifesto. " | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: "esse URI não pode usar Window. Close.  O método window. Close pode ser invocado somente a partir do conteúdo empacotado que foi carregado com um esquema de URI MS-Appx. " | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: "o aplicativo não pode navegar para *URI* porque uma página no contexto da Web não pode ser o documento de nível superior do aplicativo.  Em vez disso, carregue a página em um iframe. " | Você não pode navegar na página de nível superior para uma página da Web remota, mas seu aplicativo pode exibir uma página da Web em um [iframe][MDNIframe].  Para obter mais informações sobre como exibir o conteúdo remoto da Web, consulte [como vincular a páginas externas da Web][PreviousVersionsWindowsAppsHh780594].  |  

| Erro | Comentários |  
|:--- |:--- |  
| APPHOST9620: "este aplicativo foi fechado porque usou uma conexão HTTP e o metaelemento MS-https-Connections-only está presente.  Somente conexões HTTPS são permitidas quando você usa o metaelemento MS-https-Connections-only.  Use uma conexão HTTPS ou, se você não exigir uma conexão segura, remova o elemento meta. " | Para obter mais informações, consulte [como exigir uma conexão HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: "o aplicativo não pôde resolver a *URL* devido a este erro: *ErrorCode*." | Uma causa comum desse erro é um arquivo ausente.  |  
| APPHOST9624: "o aplicativo não pode usar o script para carregar a URL da *URL* porque a URL inicia outro aplicativo.  Somente a interação do usuário direta pode iniciar outro aplicativo. " | Os aplicativos não podem iniciar outros aplicativos diretamente.  Outros aplicativos podem ser iniciados pelo usuário quando o aplicativo implementa certos contratos.  Para saber mais, consulte as [extensões e contratos de aplicativo][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "foi detectada uma referência direta ao arquivo de recursos `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` .  Essa referência causa falhas quando usadas fora do ambiente de depuração. " | Devido ao caminho do arquivo de `logo.scale-140.png` , esse arquivo PNG é tratado como um recurso localizado, causando o erro naqueles recursos localizados não pode ser referenciado diretamente.  Consulte [Globalizando seu aplicativo (HTML)][PreviousVersionsWindowsAppsHh465006] se você pretende usar esse arquivo como um recurso de idioma.  Caso contrário, tente renomear o diretório problemático.  |  

## Consulte também  

[Usando o Tempo de Execução do Windows no JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar o tempo de execução do Windows em JavaScript | Documentos da Microsoft"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe geolocator | Documentos da Microsoft"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "método addPublicLocalApplicationUri | Documentos da Microsoft"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Como exigir uma conexão HTTPS (HTML) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Contratos e extensões do aplicativo (aplicativos do Windows Runtime) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalizando seu aplicativo (HTML) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Recursos e restrições por contexto (HTML) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Recursos de HTML, CSS e JavaScript e diferenças (HTML) | Documentos da Microsoft"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Como vincular a páginas da Web externas (HTML) | Documentos da Microsoft"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "> de<iframe: o elemento frame embutido | MDN"  
