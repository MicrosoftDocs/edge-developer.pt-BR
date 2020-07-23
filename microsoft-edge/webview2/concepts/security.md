---
description: Saiba como desenvolver aplicativos seguros do WebView2
title: Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, borda HTML, segurança
ms.openlocfilehash: f30163954f1906f71afa520b87d58c7647a5250a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894302"
---
# <span data-ttu-id="cce5b-104">Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2</span><span class="sxs-lookup"><span data-stu-id="cce5b-104">Best practices for developing secure WebView2 applications</span></span>  

<span data-ttu-id="cce5b-105">O [controle WebView2][Webview2Main] permite que os desenvolvedores hospedem conteúdo da Web em aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="cce5b-105">The [WebView2 control][Webview2Main] allows developers to host web content in the native applications.</span></span> <span data-ttu-id="cce5b-106">Quando usado corretamente, o conteúdo da Web de hospedagem oferece várias vantagens, como usar a interface do usuário baseada na Web, acessar recursos da plataforma da Web, compartilhamento de código entre plataformas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cce5b-106">When used correctly, hosting web content offers several advantages, such as using web-based UI, accessing features of the web platform, sharing code cross-platform, and so on.</span></span>  <span data-ttu-id="cce5b-107">Para evitar vulnerabilidades que possam surgir na Hospedagem de conteúdo da Web, certifique-se de projetar o aplicativo WebView2 para monitorar atentamente as interações entre o conteúdo da Web e o aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="cce5b-107">To avoid vulnerabilities that can arise from hosting web content, make sure to design your WebView2 application to closely monitor interactions between the web content and the host application.</span></span>  

1.  <span data-ttu-id="cce5b-108">Tratar todo o conteúdo da Web como não seguro.</span><span class="sxs-lookup"><span data-stu-id="cce5b-108">Treat all web content as insecure.</span></span>  
    *   <span data-ttu-id="cce5b-109">Valide as mensagens da Web e os parâmetros de objeto host antes de consumir cada um, porque as mensagens da Web e os parâmetros podem ser malformados \ (não intencionalmente ou maliciosamente \) e fazem com que o aplicativo se comporte inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="cce5b-109">Validate web messages and host object parameters before consuming each, because web messages and parameters can be malformed \(unintentionally or maliciously\) and cause the app to behave unexpectedly.</span></span>
    *   <span data-ttu-id="cce5b-110">Sempre verifique a origem do documento em execução dentro do WebView2 e avalie a confiabilidade do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cce5b-110">Always check the origin of the document running inside WebView2 and assess the trustworthiness of the content.</span></span>  
1.  <span data-ttu-id="cce5b-111">Projetar mensagens da Web específicas e interações de objeto host em vez de usar proxies genéricos.</span><span class="sxs-lookup"><span data-stu-id="cce5b-111">Design specific web messages and host object interactions instead of using generic proxies.</span></span>  
1.  <span data-ttu-id="cce5b-112">Defina as seguintes opções para restringir a funcionalidade de conteúdo da Web modificando [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings].</span><span class="sxs-lookup"><span data-stu-id="cce5b-112">Set the following options to restrict web content functionality by modifying [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings].</span></span>  
    *   <span data-ttu-id="cce5b-113">Definido `AreHostObjectsAllowed` como `false` , se você não espera que o conteúdo da Web acesse objetos de host.</span><span class="sxs-lookup"><span data-stu-id="cce5b-113">Set `AreHostObjectsAllowed` to `false`, if you do not expect the web content to access host objects.</span></span>  
    *   <span data-ttu-id="cce5b-114">Definido `IsWebMessageEnabled` como `false` , se você não espera que o conteúdo da Web poste mensagens da Web em seu aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="cce5b-114">Set `IsWebMessageEnabled` to `false`, if you do not expect the web content to post web messages to your native application.</span></span>  
    *   <span data-ttu-id="cce5b-115">Definido `IsScriptEnabled` como `false` , se você não espera que o conteúdo da Web execute scripts \ (por exemplo, ao Mostrar conteúdo HTML estático \).</span><span class="sxs-lookup"><span data-stu-id="cce5b-115">Set `IsScriptEnabled` to `false`, if you do not expect the web content to run scripts \(for example, when showing static html content\).</span></span>  
    *   <span data-ttu-id="cce5b-116">Definido `AreDefaultScriptDialogsEnabled` como `false` , se você não espera que o conteúdo da Web seja exibido `alert` ou `prompt` caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cce5b-116">Set `AreDefaultScriptDialogsEnabled` to `false`, if you do not expect the web content to show `alert` or `prompt` dialog boxes.</span></span>  
1.  <span data-ttu-id="cce5b-117">Nas etapas a seguir, use as `NavigationStarting` `FrameNavigationStarting` configurações e eventos para atualizar com base na origem da nova página.</span><span class="sxs-lookup"><span data-stu-id="cce5b-117">In the following steps, use the `NavigationStarting` and `FrameNavigationStarting` events to update settings based on the origin of the new page.</span></span>  
    1.  <span data-ttu-id="cce5b-118">Para impedir que seu aplicativo navegue para determinadas páginas, use os eventos para verificar e, em seguida, bloquear a navegação em páginas ou quadros.</span><span class="sxs-lookup"><span data-stu-id="cce5b-118">To prevent your application from navigating to certain pages, use the events to check and then block page or frame navigation.</span></span>  
    1.  <span data-ttu-id="cce5b-119">Ao navegar para uma nova página, talvez seja necessário ajustar os valores de propriedade em [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] ou [CoreWebView2Settings (.net)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="cce5b-119">When navigating to a new page, you may need to adjust the property values on [ICoreWebView2Settings (Win32)][Webview2ReferenceWin3209538Icorewebview2settings] or [CoreWebView2Settings (.NET)][Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings] as previously described.</span></span>  
1.  <span data-ttu-id="cce5b-120">Ao navegar para um novo documento, use o `ContentLoading` evento para remover objetos de host expostos usando `RemoveHostObjectFromScript` .</span><span class="sxs-lookup"><span data-stu-id="cce5b-120">When navigating to a new document, use the `ContentLoading` event to remove exposed host objects using `RemoveHostObjectFromScript`.</span></span>  

<!--## Security

Always check the Source property of the WebView before using `ExecuteScript`, `PostWebMessageAsJson`, `PostWebMessageAsString`, or any other method to send information into the WebView. The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation. Similarly, be very careful with `AddScriptToExecuteOnDocumentCreated`. All future `navigations` run the same script and if it provides access to information intended only for a certain origin, any HTML document may have access.

When examining the result of an `ExecuteScript` method call, a `WebMessageReceived` event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.

When constructing a message to send into a WebView, prefer using `PostWebMessageAsJson` and construct the JSON string parameter using a JSON library. This avoids any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script. -->  

<!-- links -->  

[Webview2Main]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[Webview2ReferenceWin3209538Icorewebview2settings]: ../reference/win32/0-9-538/icorewebview2settings.md "interface ICoreWebView2Settings | Documentos da Microsoft"  

[Webview2ReferenceWin3209538MicrosoftWebWebview2CoreCorewebview2settings]: ../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings.md "Classe Microsoft. Web. WebView2. Core. CoreWebView2Settings | Documentos da Microsoft"  
