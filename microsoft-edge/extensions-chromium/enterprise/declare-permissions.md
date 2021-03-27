---
description: Saiba como declarar permissões para APIs em seu manifesto
title: Declarar permissões de API em manifestos de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 987279a8072388d3fd47ee8b7cbf5f9bb3c483e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461487"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="declare-api-permissions-in-extension-manifests"></a>Declarar permissões de API em manifestos de extensão  

Para usar a maioria das `chrome.*` APIs, sua extensão deve declarar `permissions` o no manifesto.  Você pode declarar permissões usando uma cadeia de caracteres de permissão da tabela a seguir ou usar um padrão para corresponder a cadeias de caracteres semelhantes.  As permissões ajudam a restringir sua extensão se ela for comprometida por malware.  Algumas permissões podem ser exibidas para os usuários antes da instalação da extensão usando Avisos de Permissão.  

Se uma API exigir que você declare permissões no manifesto, revise a documentação dessa API para entender as permissões necessárias.  Por exemplo, a página api de armazenamento descreve como declarar a `storage` permissão.  

O trecho de código a seguir descreve como declarar permissões no arquivo de manifesto.  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

A tabela a seguir lista as cadeias de caracteres de permissão disponíveis no momento para usar em seu manifesto e as descrições.  

| Cadeia de caracteres de permissão | Detalhes |  
|:--- |:--- |  
| `activeTab` | Solicita que a extensão seja concedida permissões de acordo com a `activeTab` especificação. |  
| `alarms` | Fornece acesso de extensão à `chrome.alarms` API. |  
| `background` | Faz com que o Microsoft Edge inicie cedo e desligue tarde, para que as extensões possam ter uma vida mais longa.  Quando qualquer extensão instalada tem permissão, o Microsoft Edge é executado invisivelmente assim que o usuário faz logons no computador do usuário e antes de o usuário iniciar o `background` Microsoft Edge.  A permissão também faz com que o Microsoft Edge continue em execução, mesmo após o fechamento da última janela, até que o usuário saia `background` explicitamente do Microsoft Edge.  Essa permissão não afeta extensões que estão desligadas no navegador.  A `background` permissão normalmente é usada em uma página em segundo plano. |  
| `bookmarks` | Fornece acesso de extensão à `chrome.bookmarks` API. |  
| `browsingData` | Fornece acesso de extensão à `chrome.browsingData` API. |  
| `certificateProvider` | Fornece acesso de extensão à `chrome.certificateProvider` API. |  
| `clipboardRead` | Obrigatório se a extensão usar `document.execCommand('paste')` . |  
| `clipboardWrite` | Indica que a extensão usa `document.execCommand('copy')` ou `document.execCommand('cut')` . |  
| `contentSettings` | Fornece acesso de extensão à `chrome.contentSettings` API. |  
| `contextMenus` | Fornece acesso de extensão à `chrome.contextMenus` API. |  
| `cookies` | Fornece acesso de extensão à `chrome.cookies` API. |  
| `debugger` | Fornece acesso de extensão à `chrome.debugger` API. |  
| `declarativeContent` | Fornece acesso de extensão à `chrome.declarativeContent` API. |  
| `declarativeNetRequest` | Fornece acesso de extensão à `chrome.declarativeNetRequest` API. |  
| `declarativeNetRequestFeedback` | Concede o acesso de extensão a eventos e métodos dentro da API, que `chrome.declarativeNetRequest` retorna informações sobre regras declarativas que corresponderam. |  
| `declarativeWebRequest` | Fornece acesso de extensão à `chrome.declarativeWebRequest` API. |  
| `desktopCapture` | Fornece acesso de extensão à `chrome.desktopCapture` API. |  
| `documentScan` | Fornece acesso de extensão à `chrome.documentScan` API. |  
| `downloads` | Fornece acesso de extensão à `chrome.downloads` API. |  
| `enterprise.deviceAttributes` | Fornece acesso de extensão à `chrome.enterprise.deviceAttributes` API. |  
| `enterprise.hardwarePlatform` | Fornece acesso de extensão à `chrome.enterprise.hardwarePlatform` API. |  
| `enterprise.networkingAttributes` | Fornece acesso de extensão à `chrome.enterprise.networkingAttributes` API. |  
| `enterprise.platformKeys` | Fornece acesso de extensão à `chrome.enterprise.platformKeys` API. |  
| `experimental` | Obrigatório se a extensão usar qualquer `chrome.experimental.*` API. |  
| `fileBrowserHandler` | Fornece acesso de extensão à `chrome.fileBrowserHandler` API. |  
| `fileSystemProvider` | Fornece acesso de extensão à `chrome.fileSystemProvider` API. |  
| `fontSettings` | Fornece acesso de extensão à `chrome.fontSettings` API. |  
| `geolocation` | Permite que a extensão use a API de localização geográfica sem solicitar permissão ao usuário. |  
| `history` | Fornece acesso de extensão à `chrome.history` API. |  
| `identity` | Fornece acesso de extensão à `chrome.identity` API. |  
| `idle` | Fornece acesso de extensão à `chrome.idle` API. |  
| `loginState` | Fornece acesso de extensão à `chrome.loginState` API. |  
| `management` | Fornece acesso de extensão à `chrome.management` API. |  
| `nativeMessaging` | Fornece acesso de extensão à API de mensagens nativa. |  
| `notifications` | Fornece acesso de extensão à `chrome.notifications` API. |  
| `pageCapture` | Fornece acesso de extensão à `chrome.pageCapture` API. |  
| `platformKeys` | Fornece acesso de extensão à `chrome.platformKeys` API. |  
| `power` | Fornece acesso de extensão à `chrome.power` API. |  
| `printerProvider` | Fornece acesso de extensão à `chrome.printerProvider` API. |  
| `printing` | Fornece acesso de extensão à `chrome.printing` API. |  
| `printingMetrics` | Fornece acesso de extensão à `chrome.printingMetrics` API. |  
| `privacy` | Fornece acesso de extensão à `chrome.privacy` API. |  
| `processes` | Fornece acesso de extensão à `chrome.processes` API. |  
| `proxy` | Fornece acesso de extensão à `chrome.proxy` API. |  
| `scripting` | Fornece acesso de extensão à `chrome.scripting` API. |  
| `search` | Fornece acesso de extensão à `chrome.search` API. |  
| `sessions` | Fornece acesso de extensão à `chrome.sessions` API. |  
| `signedInDevices` | Fornece acesso de extensão à `chrome.signedInDevices` API. |  
| `storage` | Fornece acesso de extensão à `chrome.storage` API. |  
| `system.cpu` | Fornece acesso de extensão à `chrome.system.cpu` API. |  
| `system.display` | Fornece acesso de extensão à `chrome.system.display` API. |  
| `system.memory` | Fornece acesso de extensão à `chrome.system.memory` API. |  
| `system.storage` | Fornece acesso de extensão à `chrome.system.storage` API. |  
| `tabCapture` | Fornece acesso de extensão à `chrome.tabCapture` API. |  
| `tabGroups` | Fornece acesso de extensão à `chrome.tabGroups` API. |  
| `tabs` | Fornece acesso de extensão a campos privilegiados dos objetos que podem ser usados por `Tab` várias APIs, incluindo `chrome.tabs` e `chrome.windows` .  Em muitas circunstâncias, sua extensão não precisa declarar a `tabs` permissão para usar essas APIs. |  
| `topSites` | Fornece acesso de extensão à `chrome.topSites` API. |  
| `tts` | Fornece acesso de extensão à `chrome.tts` API. |  
| `ttsEngine` | Fornece acesso de extensão à `chrome.ttsEngine` API. |  
| `unlimitedStorage` | Fornece uma cota ilimitada para armazenar dados do lado do cliente, como bancos de dados e arquivos de armazenamento local.  Sem essa permissão, a extensão é limitada a 5 MB de armazenamento local. |  
| `vpnProvider` | Fornece acesso de extensão à `chrome.vpnProvider` API. |  
| `wallpaper` | Fornece acesso de extensão à `chrome.wallpaper` API. |  
| `webNavigation` | Fornece acesso de extensão à `chrome.webNavigation` API. |  
| `webRequest` | Fornece acesso de extensão à `chrome.webRequest` API. |  
| `webRequestBlocking` | Obrigatório se a extensão usar a `chrome.webRequest` API para bloquear solicitações. |  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
