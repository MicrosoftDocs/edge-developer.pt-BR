---
description: Códigos de erro para aplicativos do Windows Runtime usando JavaScript
title: Códigos de erro para aplicativos do Windows Runtime usando JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
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
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e7241d675a6f488e70eefb20c40149683f965c8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398487"
---
# <a name="error-codes-for-windows-runtime-apps-using-javascript"></a>Códigos de erro para aplicativos do Windows Runtime usando JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Aqui estão os códigos de erro exibidos pelo console do Microsoft Visual Studio ao desenvolver aplicativos do Windows Runtime usando JavaScript.  

| Erro | Comentários |  
|:--- |:--- |  
| APPHOST9601: "Não é possível carregar *remoteURI*.  Um aplicativo não pode carregar conteúdo da Web remoto no contexto local." | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [Recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "'javascript:' é um valor de atributo inválido e será ignorado.  Não use URIs 'javascript:' no contexto local." | Por motivos de segurança, você não pode usar URIs 'javascript:' no contexto local.  Para obter mais informações sobre o que é permitido no contexto local, consulte [Recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "Não é possível carregar o ActiveX plug-in que tenha a ID *de classe classID*.  Os aplicativos não podem carregar ActiveX controles." | Os aplicativos do Windows Runtime usando JavaScript não suportam controles personalizados do Microsoft ActiveXcontrols.  Se você precisar de um controle de interface do usuário, use um controle Web padrão, uma biblioteca de controles ou crie seu próprio controle personalizado.  Se precisar executar a lógica personalizada, crie um objeto do Windows Runtime personalizado.  Para obter informações sobre outras diferenças html, CSS e JavaScript, consulte [HTML, CSS e JavaScript features and differences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "Não é possível navegar até *uri* porque usa uma codificação de caracteres inválida.  Um aplicativo só pode navegar até arquivos codificados com UTF8." | Todos os HTML, JavaScript e CSS acessados por um Windows Runtime devem ser codificados como Formato de Transformação Unicode de 8 bits (UTF-8).  Para obter informações sobre outras diferenças html, CSS e JavaScript, consulte [HTML, CSS e JavaScript features and differences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "Não é possível navegar até *targetURI* a partir do *sourceURI* porque o URI de destino está em uma zona de segurança mais alta.  Você não pode navegar de uma zona com menor segurança para uma zona com segurança mais alta, a menos que você esteja navegando para um URI de contexto local a partir de um URI de contexto da Web e tenha registrado o URI de contexto local com o método MSApp.addPublicLocalApplicationUri." | Para obter mais informações, consulte [MSApp.addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: "Não é possível carregar *uri* porque ele usa uma conexão HTTP e o elemento meta ms-https-connections-only está presente.  Somente as conexões HTTPS são permitidas quando você usa o elemento meta ms-https-connections-only.  Use uma conexão HTTPS ou, se você não precisar de uma conexão segura, remova o elemento meta." | Para obter mais informações, [consulte Como exigir uma conexão HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "O aplicativo não pode iniciar o URI no *uri* devido a esse erro: *failureCode*." | Um recurso ausente ou um arquivo inválido são causas comuns desse erro.  |  
| APPHOST9608: "O aplicativo não pôde navegar para a página about:blank devido a este erro: *errorCode*." |  |  

| Erro | Comentários |  
|:--- |:--- |  
| APPHOST9610: "O aplicativo encontrou um erro ao se preparar para navegar até uma página de erro personalizada: *errorCode*." |  |  
| APPHOST9611: "O aplicativo não pôde navegar até uma página de erro personalizada devido a esse erro: *errorCode*." |  |  
| APPHOST9613: "O aplicativo não pôde navegar até *uri*  devido a esse erro: *errorCode*." |  |  
| APPHOST9614: "Um documento em um iframe solicitou o modo de doc *requestedDocMode,* mas o sistema impõe o modo de doc *currentDocMode.*  O iframe usará o *modo de doc currentDocMode."* | Para obter mais informações sobre como exibir conteúdo da Web remoto, consulte [Como vincular a páginas da Web externas.][PreviousVersionsWindowsAppsHh780594]  |  
| APPHOST9615: "O aplicativo não pode baixar o arquivo no *uri* porque foi invocado programaticamente fora do contexto local". | Ocorre quando o conteúdo no contexto da Web tenta baixar programaticamente um arquivo.  |  
| APPHOST9616: "Esse URI não pode usar APIs de localização geográfica.  AS APIs de localização geográfica só podem ser invocadas de um URI que faz parte do pacote ou que está incluído no elemento ApplicationContentUris do manifesto." | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [Recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: "Esse URI não pode usar APIs de área de transferência.  As APIs da área de transferência só podem ser invocadas de um URI que faz parte do pacote ou que está incluído no elemento ApplicationContentUris do manifesto." | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [Recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: "Esse URI não pode usar window.close.  O método window.close só pode ser invocado do conteúdo empacotado que foi carregado com um esquema de URI ms-appx." | Para obter mais informações sobre o que é permitido no contexto da Web, consulte [Recursos e restrições por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: "O aplicativo não pode navegar até *uri* porque uma página no contexto da Web não pode ser o documento de nível superior do aplicativo.  Carregue a página em um iframe em vez disso." | Você não pode navegar sua página de nível superior para uma página da Web remota, mas seu aplicativo pode exibir uma página da Web em [um iframe][MDNIframe].  Para obter mais informações sobre como exibir conteúdo da Web remoto, consulte [Como vincular a páginas da Web externas.][PreviousVersionsWindowsAppsHh780594]  |  

| Erro | Comentários |  
|:--- |:--- |  
| APPHOST9620: "Este aplicativo foi fechado porque ele usou uma conexão HTTP e o elemento meta ms-https-connections-only está presente.  Somente as conexões HTTPS são permitidas quando você usa o elemento meta ms-https-connections-only.  Use uma conexão HTTPS ou, se você não exigir uma conexão segura, remova o elemento meta." | Para obter mais informações, [consulte Como exigir uma conexão HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: "O aplicativo não pôde resolver *a URL devido* a esse erro: *errorCode*." | Uma causa comum desse erro é um arquivo ausente.  |  
| APPHOST9624: "O aplicativo não pode usar script para carregar a *URL* da URL porque a url inicia outro aplicativo.  Somente a interação direta do usuário pode iniciar outro aplicativo." | Os aplicativos não podem iniciar outros aplicativos diretamente.  Outros aplicativos podem ser lançados pelo usuário quando o aplicativo implementa determinados contratos.  Para saber mais, consulte as [extensões e contratos de aplicativo][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Uma referência direta ao arquivo de recursos `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` foi detectada.  Essa referência causa falhas quando usadas fora do ambiente de depuração." | Devido ao caminho do arquivo de , esse arquivo PNG é tratado como um recurso localizado, causando o erro em que os recursos localizados não podem ser `logo.scale-140.png` referenciados diretamente.  Consulte [Globalizando seu aplicativo (HTML)][PreviousVersionsWindowsAppsHh465006] se você pretende usar esse arquivo como um recurso de idioma.  Caso contrário, tente renomear o diretório problemático.  |  

## <a name="see-also"></a>Veja também  

[Usando o Tempo de Execução do Windows no JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usando o Tempo de Execução do Windows no JavaScript | Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Classe Geolocator | Microsoft Docs"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "Método addPublicLocalApplicationUri | Microsoft Docs"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Como exigir uma conexão HTTPS (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Contratos de aplicativo e extensões (aplicativos do Windows Runtime) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalizando seu aplicativo (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Recursos e restrições por contexto (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Recursos HTML, CSS e JavaScript e diferenças (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Como vincular a páginas da Web externas (HTML) | Microsoft Docs"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: o elemento Frame em linha | MDN"  
