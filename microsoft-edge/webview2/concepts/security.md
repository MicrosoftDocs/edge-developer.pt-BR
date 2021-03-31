---
description: Saiba como desenvolver aplicativos seguros do WebView2
title: Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, borda HTML, segurança
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118994"
---
# Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2  

O [controle WebView2][Webview2Main] permite que os desenvolvedores hospedem conteúdo da Web em aplicativos nativos. Quando usado corretamente, o conteúdo da Web de hospedagem oferece várias vantagens, como usar a interface do usuário baseada na Web, acessar recursos da plataforma da Web, compartilhamento de código entre plataformas e assim por diante.  Para evitar vulnerabilidades que possam surgir na Hospedagem de conteúdo da Web, certifique-se de projetar o aplicativo WebView2 para monitorar atentamente as interações entre o conteúdo da Web e o aplicativo host.  

1.  Tratar todo o conteúdo da Web como não seguro.  
    *   Valide as mensagens da Web e os parâmetros de objeto host antes de consumir cada um, porque as mensagens da Web e os parâmetros podem ser malformados \(não intencionalmente ou maliciosamente \) e fazem com que o aplicativo se comporte inesperadamente.
    *   Sempre verifique a origem do documento em execução dentro do WebView2 e avalie a confiabilidade do conteúdo.  
1.  Projetar mensagens da Web específicas e interações de objeto host em vez de usar proxies genéricos.  
1.  Defina as seguintes opções para restringir a funcionalidade de conteúdo da Web modificando [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].  
    *   Definido `AreHostObjectsAllowed` como `false` , se você não espera que o conteúdo da Web acesse objetos de host.  
    *   Definido `IsWebMessageEnabled` como `false` , se você não espera que o conteúdo da Web poste mensagens da Web em seu aplicativo nativo.  
    *   Definido `IsScriptEnabled` como `false` , se você não espera que o conteúdo da Web execute scripts \(por exemplo, ao Mostrar conteúdo HTML estático \).  
    *   Definido `AreDefaultScriptDialogsEnabled` como `false` , se você não espera que o conteúdo da Web seja exibido `alert` ou `prompt` caixas de diálogo.  
1.  Nas etapas a seguir, use as `NavigationStarting` `FrameNavigationStarting` configurações e eventos para atualizar com base na origem da nova página.  
    1.  Para impedir que seu aplicativo navegue para determinadas páginas, use os eventos para verificar e, em seguida, bloquear a navegação em páginas ou quadros.  
    1.  Ao navegar para uma nova página, talvez seja necessário ajustar os valores de propriedade em [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] conforme descrito anteriormente.  
1.  Ao navegar para um novo documento, use o `ContentLoading` evento para remover objetos de host expostos usando `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "interface ICoreWebView2Settings | Documentos da Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Classe CoreWebView2Settings (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
