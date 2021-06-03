---
description: Entender como desenvolver aplicativos WebView2 seguros
title: Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, html de borda, segurança
ms.openlocfilehash: d53417cc1ac98b44565692edbaec06216f7c110b
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118994"
---
# Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros  

O [controle WebView2][Webview2Main] permite que os desenvolvedores hospedem conteúdo da Web nos aplicativos nativos. Quando usado corretamente, hospedar conteúdo da Web oferece várias vantagens, como usar a interface do usuário baseada na Web, acessar recursos da plataforma Web, compartilhar código entre plataformas e assim por diante.  Para evitar vulnerabilidades que podem surgir da hospedagem de conteúdo da Web, certifique-se de projetar seu aplicativo WebView2 para monitorar de perto as interações entre o conteúdo da Web e o aplicativo host.  

1.  Trate todo o conteúdo da Web como inseguro.  
    *   Valide as mensagens da Web e os parâmetros de objeto host antes de consumir cada um deles, pois as mensagens da Web e os parâmetros podem ser malformados \(intencionalmente ou mal-intencionados\) e fazer com que o aplicativo se comporte inesperadamente.
    *   Sempre verifique a origem do documento em execução no WebView2 e avalie a confiabilidade do conteúdo.  
1.  Projete mensagens da Web específicas e interações de objeto host em vez de usar proxies genéricos.  
1.  De definir as opções a seguir para restringir a funcionalidade de conteúdo da Web modificando [iCoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] ou [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings].  
    *   De `AreHostObjectsAllowed` acordo com , se você não espera que o conteúdo da Web acesse objetos `false` host.  
    *   De `IsWebMessageEnabled` acordo com , se você não espera que o conteúdo da Web `false` poste mensagens da Web em seu aplicativo nativo.  
    *   De acordo com , se você não espera que o conteúdo da Web execute `IsScriptEnabled` `false` scripts \(por exemplo, ao mostrar conteúdo html estático\).  
    *   De `AreDefaultScriptDialogsEnabled` acordo com , se você não espera que o conteúdo da Web mostre ou caixas de `false` `alert` `prompt` diálogo.  
1.  Nas etapas a seguir, use os eventos e para atualizar as configurações com base na `NavigationStarting` `FrameNavigationStarting` origem da nova página.  
    1.  Para impedir que seu aplicativo navegou até determinadas páginas, use os eventos para verificar e bloquear a navegação de página ou quadro.  
    1.  Ao navegar para uma nova página, talvez seja necessário ajustar os valores de propriedade em [ICoreWebView2Settings (Win32)][Webview2ReferenceWin32Icorewebview2settings] ou [CoreWebView2Settings (.NET)][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings] conforme descrito anteriormente.  
1.  Ao navegar para um novo documento, use o evento `ContentLoading` para remover objetos host expostos usando `RemoveHostObjectFromScript` .  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2settings]: /microsoft-edge/webview2/reference/win32/icorewebview2settings "interface ICoreWebView2Settings | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2settings]: /dotnet/api/microsoft.web.webview2.core.corewebview2settings "Classe CoreWebView2Settings (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
