---
description: Saiba como desenvolver aplicativos seguros do WebView2
title: Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, borda HTML, segurança
ms.openlocfilehash: e71dbe9ad98b7156d8888da074e30a96683469d5
ms.sourcegitcommit: e49b86082da884299fdd485d3311d63a7688c0d0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/22/2020
ms.locfileid: "10755389"
---
# Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2

O [controle WebView2](https://docs.microsoft.com/microsoft-edge/webview2/) permite que os desenvolvedores hospedem conteúdo da Web em seus aplicativos nativos. Quando usado corretamente, o conteúdo da Web de hospedagem oferece várias vantagens, como usar a interface do usuário baseada na Web, acessar recursos da plataforma da Web, compartilhamento de código entre plataformas e assim por diante. Para evitar vulnerabilidades que possam surgir na Hospedagem de conteúdo da Web, certifique-se de projetar o aplicativo WebView2 para monitorar atentamente as interações entre o conteúdo da Web e o aplicativo host. 

1. Tratar todo o conteúdo da Web como não seguro
    - Valide mensagens da Web e parâmetros de objeto host antes de consumi-los, pois as mensagens da Web e os parâmetros podem ser malformados (não intencionalmente ou maliciosamente) e fazer com que o aplicativo se comporte inesperadamente.
    - Sempre verifique a origem do documento em execução dentro do WebView2 e avalie a confiabilidade do conteúdo. 

2. Projetar mensagens da Web específicas e interações de objeto host em vez de usar proxies genéricos.

3. Restrinja a funcionalidade de conteúdo da Web modificando [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) ou [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) da seguinte maneira:
    - Definido `AreHostObjectsAllowed` como `false` , se você não espera que o conteúdo da Web acesse objetos de host.
    - Definido `IsWebMessageEnabled` como `false` , se você não espera que o conteúdo da Web poste mensagens da Web em seu aplicativo nativo. 
    - Definido `IsScriptEnabled` como `false` , se você não espera que o conteúdo da Web execute scripts (por exemplo, ao Mostrar conteúdo HTML estático).
    - Definido `AreDefaultScriptDialogsEnabled` como `false` , se você não espera que o conteúdo da Web seja exibido `alert` ou `prompt` caixas de diálogo.

4.  Use os `NavigationStarting` `FrameNavigationStarting` eventos e para atualizar as configurações com base na origem da nova página da seguinte maneira:
    1.  Para impedir que seu aplicativo navegue para determinadas páginas, use esses eventos para verificar e, em seguida, bloquear a navegação em páginas ou quadros. 
    2.  Ao navegar para uma nova página, talvez seja necessário ajustar os valores de propriedade em [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) ou [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) ' conforme descrito acima.

5. Ao navegar para um novo documento, use o `ContentLoading` evento para remover objetos de host expostos usando `RemoveHostObjectFromScript` . 