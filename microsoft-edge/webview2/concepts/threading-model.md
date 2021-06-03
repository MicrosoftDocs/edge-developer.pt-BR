---
description: Modelo de threading
title: Threading model | WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 9a7ce3d66e53b832d4430afb153e6539d97e5db7
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535605"
---
# <a name="threading-model"></a>Modelo de threading 

:::row:::
   :::column span="1":::
      Plataformas com suporte:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

O controle WebView2 baseia-se no Modelo de Objeto de Componente [(COM)][WindowsWin32ComTheComponentObjectModel] e deve ser executado em um thread STA [(Single Threaded Apartments).][WindowsWin32ComSingleThreadedApartments]  

## <a name="thread-safety"></a>Segurança de thread  

O WebView2 deve ser criado em um thread da interface do usuário.  Especificamente, um thread com uma bomba de mensagem.  Todos os retornos de chamada ocorrem nesse thread e as solicitações no WebView2 devem ser feitas nesse thread.  Não é seguro usar o WebView2 de outro thread.  

A única exceção é para a `Content` propriedade `CoreWebView2WebResourceRequest` de .  O `Content` fluxo de propriedades é lido de um thread em segundo plano.  O fluxo deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar a degradação de desempenho para o thread da interface do usuário.  

## <a name="re-entrancy"></a>Re-entrada  

Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.  
Depois de executar um manipulador de eventos e iniciar um loop de mensagem, você não poderá executar qualquer manipulador de eventos ou retorno de chamada de conclusão de uma maneira de nova entrada.  

## <a name="deferrals"></a>Adiamentos  

Alguns eventos WebView2 leem valores definidos nos argumentos de evento relacionados ou iniciam alguma ação depois que o manipulador de eventos é concluído.  Se você também precisar executar uma operação assíncrona como um manipulador de eventos, use o método nos argumentos de evento `GetDeferral` dos eventos associados.  O objeto retornado garante que o manipulador de eventos não seja considerado concluído até que o `Deferral` `Complete` método do seja `Deferral` solicitado.  

Por exemplo, você pode usar o evento para fornecer um para se conectar como uma janela filha quando o manipulador `NewWindowRequested` `CoreWebView2` de eventos for concluído.  Mas se você precisar criar de forma assíncrona o método , solicite o `CoreWebView2` método no `GetDeferral` `NewWindowRequestedEventArgs` .  Depois de criar de forma assíncrona e definir a propriedade na solicitação , no objeto, será retornado `CoreWebView2` `NewWindow` usando o `NewWindowRequestedEventArgs` `Complete` `Deferral` `GetDeferral` método.  

## <a name="block-the-ui-thread"></a>Bloquear o thread da interface do usuário  

O WebView2 depende da mensagem do thread da interface do usuário para executar retornos de chamada do manipulador de eventos e retornos de chamada de conclusão do método assíncrono.  Se você usar métodos que bloqueiam a mensagem, como ou , seus manipuladores de eventos WebView2 e manipuladores de conclusão do método `Task.Result` `WaitForSingleObject` assíncrono não são executados.  Por exemplo, o código a seguir não é concluído, porque interrompe a mensagem enquanto `Task.Result` aguarda a `ExecuteScriptAsync` conclusão.  Como a mensagem está bloqueada, `ExecuteScriptAsync` o não é capaz de ser concluído.   

```csharp
private void Button_Click(object sender, EventArgs e)
{
    string result = webView2Control.CoreWebView2.ExecuteScriptAsync("'test'").Result;
    MessageBox.Show(this, result, "Script Result");
}
```  

Use um mecanismo assíncrono como e , que não bloqueia a mensagem ou `await` o thread da interface do `async` `await` usuário.  

```csharp
private async void Button_Click(object sender, EventArgs e)
{
    string result = await webView2Control.CoreWebView2.ExecuteScriptAsync("'test'");
    MessageBox.Show(this, result, "Script Result");
}
```  

## <a name="see-also"></a>Consulte também  

*   Para começar a usar WebView2, navegue até [WebView2 Introdução Guias.][Webview2IndexGetStarted]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] em GitHub.  
*   Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[WindowsWin32ComSingleThreadedApartments]: /windows/win32/com/single-threaded-apartments "Apartamentos com thread único | Microsoft Docs"  
[WindowsWin32ComTheComponentObjectModel]: /windows/win32/com/the-component-object-model "O modelo de objeto component | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
