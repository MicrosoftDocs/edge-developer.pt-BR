---
description: Começar a usar WebViews de Depuração Remota em seus aplicativos Android nativos usando Microsoft Edge Ferramentas de Desenvolvedor.
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 75d948465c62c63c9ccbe0fcd46616819a04e79d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565075"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="get-started-with-remote-debugging-android-webviews"></a>Introdução à depuração remota de dispositivos Android  

Depurar o Android WebViews em seus aplicativos Android nativos usando Microsoft Edge Ferramentas de Desenvolvedor.  

No Android 4.4 \(KitKat\) ou posterior, use DevTools para depurar o conteúdo webView em aplicativos Android nativos.  

### <a name="summary"></a>Resumo  

*   Ativar a depuração do Android WebView em seu aplicativo Android nativo; depurar o Android WebViews Microsoft Edge DevTools.  
*   Para exibir a lista dos WebViews do Android com a depuração ativas, navegue até `edge://inspect` .  
*   Depurar o Android WebViews da mesma maneira que você depura uma página da Web por meio [da depuração remota.][RemoteDebuggingGettingStarted]  

## <a name="configure-android-webviews-to-debug"></a>Configurar WebViews do Android para depurar  

A depuração do Android WebView deve estar 100% ativas no aplicativo.  Para ativar a depuração do Android WebView, execute o [método estático setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] na `WebView` classe.  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

A configuração se aplica a todos os WebViews do Android do aplicativo.  

> [!TIP]
> A depuração do Android WebView não é afetada pelo estado `debuggable` do sinalizador no manifesto do aplicativo.  Se você quiser ativar a depuração do Android WebView somente quando o sinalizador estiver , teste o `debuggable` sinalizador no tempo de `true` execução.  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a>Abrir um WebView do Android no DevTools  

Para exibir uma lista dos WebViews do Android com a depuração ativas que são executados em seu dispositivo, navegue até `edge://inspect` .  

Para iniciar a depuração, no WebView do Android que você deseja depurar, escolha **inspecionar**.  Use DevTools da mesma maneira que você faz uma guia de navegador remoto.  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a>Solução de problemas  

Seus WebViews do Android não são exibidos na `edge://inspect` página?  

*   Verifique se a depuração do Android WebView está ativas para seu aplicativo.  
*   Em seu dispositivo, abra o aplicativo com o Android WebView que você deseja depurar.  Em seguida, atualize `edge://inspect` .  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introdução com dispositivos Android de depuração remota | Microsoft Docs"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled - WebView | Desenvolvedores Android"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
