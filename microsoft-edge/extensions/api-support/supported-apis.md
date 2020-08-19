---
description: Encontre informações sobre APIs atuais e futuras, bem como problemas conhecidos/incompatibilidades com o Chrome.
title: Extensões-APIs com suporte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: fceba67f5fab1a223cfc94abf7f19a0a9d1bcdf0
ms.sourcegitcommit: 0879b205aa88c6b73d84f106b4b435d5a0e8cadc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/18/2020
ms.locfileid: "10937179"
---
# APIs com suporte  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Veja a seguir uma lista detalhada dos membros da API com suporte. O desenvolvimento da plataforma de extensão está em andamento, portanto verifique com frequência se há atualizações!

> [!NOTE]
>  - Para o Microsoft Edge, todas as APIs de extensão estão sob o `browser` namespace, por exemplo `browser.browserAction.disable()` .
>  - As APIs de extensão do Microsoft Edge usam retornos de chamada, e não prometem.


## Problemas abrangentes

Os seguintes problemas conhecidos se estendem pela plataforma de extensão e serão corrigidos em breve:

- Ao usar a `url()` propriedade CSS, URLs absolutas usando `ms-browser-extension://` não funcionarão como as do Chrome. Para ignorar esse problema, use caminhos relativos para recursos (iniciando no diretório de extensão raiz) em vez disso.
- `window.open()` Não funciona em scripts em segundo plano de extensão. `browser.windows.create()`Em vez disso, use.
- Os cookies compartilhados têm suporte, mas o script de plano de fundo de extensão não terá acesso aos cookies de sessão definidos na guia antes de a extensão ser habilitada. Esse problema não afeta os cookies persistentes.
- Se apenas as permissões sem suporte forem especificadas para uma extensão, ou seja, `activeTab`, a tentativa de sideloadr a extensão fará com que a extensão seja desinstalada com a seguinte mensagem exibida: "algo deu errado com suas extensões, portanto tivemos que reinstalá-las. Você precisará ativá-las novamente. "
- O disparo de um download por meio de uma marca de âncora oculta falhará dos scripts em segundo plano. Isso deve ser feito em uma página de extensão em vez disso.


## indicadores

`bookmarks`Há suporte para as seguintes APIs:

| API                                   | Problemas conhecidos                                             | Incompatibilidades do Chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [indicadores](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks) | | |
| [bookmarks. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/create) | | |
| [indicadores. remover](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/remove) | | |
| [bookmarks. gettree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/getTree) |  | |
| [indicadores. mover](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/move) | | |
| [bookmarks. removeTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/removeTree) | | |
| [bookmarks. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/update)            | | |


## BrowserAction

`browserAction`Há suporte para as seguintes APIs:

| API                                   | Problemas conhecidos                                             | Incompatibilidades do Chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [BrowserAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction) | | |
| [BrowserAction. Disable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/disable) | | |
| [BrowserAction. Enable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/enable) | | |
| [BrowserAction. getBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeBackgroundColor) |  | |
| [BrowserAction. setBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeBackgroundColor) | | |
| [BrowserAction. onclickd](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/onClicked) | | |
| [BrowserAction. setBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeText)            | | |
| [BrowserAction. setpopup](https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setPopup)  | | |
| [BrowserAction. getBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeText)   | | |
| [BrowserAction. SetIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setIcon) | `browserAction.setIcon` Não é persistente. <br/><br/> `imageData`Não há suporte para o parâmetro. <br/><br/> `path` é um parâmetro obrigatório.| |
| [BrowserAction. GetTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getTitle) | | |
| [BrowserAction. setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setTitle) | | |

## contextMenus

`contextMenus`Há suporte para as seguintes APIs:

| API                    | Problemas conhecidos | Incompatibilidades do Chrome
|------------------------|--------------|----------------------|
| [contextMenus](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus)  |  | |
| [contextMenus. ContextType](https://developer.mozilla.org/Add-ons/WebExtensions/API/contextMenus/ContextType) | `"page_action"` `ContextType` não aparecerá no menu de contexto da ação da página.| O Microsoft Edge não é compatível com o `"launcher"` `ContextType` .|
| [contextMenus. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/create)    | Quando as extensões não fornecem um `contextmenuid` , o `id` gerado não é exclusivo. | |
| [contextMenus. onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/onClicked) | | |
| [contextMenus. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/remove) | | |
| [contextMenus. removeAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/removeAll) | | |
| [contextMenus. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/update) | | |

## cookies

`cookies`Há suporte para as seguintes APIs:

| API                    | Problemas conhecidos | Incompatibilidades do Chrome
|------------------------|--------------|----------------------|
| [cookies](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/cookies)  |  | |
| [cookies. Obtenha](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/get)    |  | |
| [cookies. getAll](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAll) |   | Se nenhuma URL for fornecida, os cookies serão recuperados somente para URLs em guias abertas no momento. No Chrome, isso obtém todos os cookies na máquina de um usuário. |
| [cookies. getAllCookieStores](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAllCookieStores)  | | Sempre retorna o mesmo repositório de cookies padrão com ID "0". Todos os cookies pertencem a essa loja. |
| [cookies. OnChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/onChanged)    | | Sem suporte. |
| [cookies. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/remove) |  | |
| [cookies. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/set)    |  | |



## prorroga

`extension`Há suporte para as seguintes APIs:

| API                                   | Problemas conhecidos | Incompatibilidades do Chrome
|---------------------------------------|----------------------------------------------------------|-------------|
[prorroga](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension) | | |
[extensão. getBackgroundPage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getBackgroundPage) | | |
[extensão. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getURL) | | |
[extensão. GetViews](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/getViews) | | |
[extensão. isAllowedIncognitoAccess](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/isAllowedIncognitoAccess) | | | 
[extension.inIncognitoContext](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/inIncognitoContext) | | | 



## nacional

`i18n`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------| :-------- | :---------------------
[nacional](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n) | | |
[i18n. getAcceptLanguages](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getAcceptLanguages) | | |
[i18n. getMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/i18n/getMessage) | `i18n.getMessage` com a chave inválida, gera uma exceção em vez de não ter falhado normalmente. <br/><br/> `i18n.getMessage` o argumento espera cadeias de caracteres, mas também deve permitir um int ou gerar uma exceção. | |
[i18n. getUILanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getUILanguage) | | |

## ociosidade

`idle`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------| :-------- | :---------------------
[ociosidade](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle) | | |
[Idle. setDetectionInterval](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/setDetectionInterval) | | |
[Idle. QueryState](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/queryState) | | |

## notificações

`notifications`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------| :-------- | :---------------------
[notificações](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) | | |
[Enviar. Notificationoptions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/NotificationOptions) | | |
[Enviar. TemplateType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/TemplateType) | | |
[notificações. limpar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/clear) | | |
[notificações. criar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/create) | | |
[notificações. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/getAll) | | |
[notificações. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/update) | | |
[notificações. onButtonClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onButtonClicked) | | |
[notificações. onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClicked) | | |
[notificações. OnClosed](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClosed) | | |
notificações. onPermissionLevelChanged | | |
notificações. getPermissionLevel | | |

## página de anotações

`pageAction`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :--------------------
[página de anotações](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction) | | |
[PageAction. getpopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getPopup) | | |
[PageAction. GetTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getTitle) | | |
[PageAction. Hide](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/hide) | | |
[PageAction. onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/onClicked) | | |
[PageAction. SetIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setIcon) | | `imageData`Não há suporte para o parâmetro. <br/><br/> `path` é um parâmetro obrigatório. |
[PageAction. setpopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setPopup) | | |
[PageAction. setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle) | | |
[PageAction. show](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/show) | | |



## classpath

`runtime`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :-------------------
[classpath](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime) | | |
[tempo de execução. Port. Disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[tempo de execução. Port. OnDisconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. CreateMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Connect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connect) | | |
[tempo de execução. connectNative](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) | | |
[runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id) | | |
[tempo de execução. getBackgroundPage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/getBackgroundPage) | | |
[Runtime. getmanifest](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getManifest) | | |
[tempo de execução. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getURL) | | |
[tempo de execução. lastError](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/lastError) | | |
[tempo de execução. recarregar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/reload) | | |
[Runtime. sendMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage) | As páginas de extensão do Microsoft Edge podem `runtime.sendMessage` / `onMessage` ser usadas para enviar mensagens para si mesmo. <br/><br/> `runtime.sendmessage` Não é compatível com páginas do site. | O Microsoft Edge não oferece suporte para o `options` parâmetro.|
[tempo de execução. sendNativeMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) | | |
[tempo de execução. setUninstallUrl](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/setUninstallUrl) | | |
[Runtime. OnConnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onConnect) | | |
[tempo de execução. oninstalled](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onInstalled) | | |
[tempo de execução. onMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onMessage) | `tab` o objeto no `runtime.onMessage` evento não está totalmente implementado. | `MessageSender.tlsChannelId` Não é compatível com o Microsoft Edge.|

## armazenamento

`storage`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :------------------------
[armazenamento](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage) |  | |
[Storage. local. obter](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/get)  | | |
[Storage. local. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/remove)  | | |
[Storage. local. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/set)  | | |
[armazenamento. local. limpar](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/clear) | | |
[Storage. local. getBytesInUse](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/getBytesInUse) | | `storage.local` os dados persistem em um formato diferente do Chrome, fazendo com que um valor diferente seja retornado ao fazer uma chamada `storage.local.getBytesInUse` .  <br/><br/>Por exemplo: `storage.local.set({ "k": { "s": "âas" } }` retorna 13 no Chrome e no 50 no Microsoft Edge.|
[Storage. Sync. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/get) | Se a quantidade combinada de caracteres nos `name` campos e do `author` manifesto exceder 31 caracteres, o `storage.sync` namespace pode não funcionar. | |
[Storage. Sync. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/remove) | | |
[Storage. Sync. Set](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/set) | | |
[Storage. OnChanged](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/onChanged) | | |

## efetua

`tabs`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :----------------
[efetua](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Tabs. captureVisibleTab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/captureVisibleTab) | | |
[Tab. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/create) | | `selected`, `pinned` e `openerTabId` não são compatíveis. |
[Tabs. detectLanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/detectLanguage) | | |
[tabs.executeScript](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/executeScript) | `runAt` é ignorado, porém selecionado. Ainda não há suporte para executar o script em um quadro específico. | |
[guias. obter](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/get) | Páginas de opções, ao perguntar sobre uma guia que não está na janela, reprovar esta chamada. | |
[Tab. GetCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/getCurrent) | | |
[Tabs. insertCSS](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/insertCSS) | `runAt` é ignorado, porém selecionado. | `cssOrigin` Não é suportada. |
[guias. OnActivated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onActivated) | | |
[Tabs. onattached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onAttached) | | |
[guias. OnCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onCreated) | | |
[guias. ondetached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[guias. OnRemoved](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onRemoved) | | |
[guias. onreplaced](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/onReplaced) | | |
[guias. OnUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onUpdated) | Após a desinstalação/reinstalação, a URL não será recebida até que o Microsoft Edge seja reiniciado. | |
[guias. consulta](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/query) | `pinned`, `audible` e `muted` ainda não têm suporte. <br/><br/> `"popup"` `windowType` Ainda não tem suporte. | `highlighted` Não é suportada. <br/><br/> `"panel"`, `"app"` e `"devtools"` `windowType` não são compatíveis. |
[guias. recarregar](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/reload) | | O Microsoft Edge não é compatível com promessas. |
[guias. remover](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/remove) | | |
[Tabs. sendMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/sendMessage) | O sistema de mensagens ainda não tem suporte para um quadro específico. `tabs.sendMessage` nunca envia uma resposta após uma atualização de tabulação se nenhum `runtime.onMessage` ouvinte estiver presente na guia recebimento. | |
[efetua. Abas](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/Tab) | `audible`as propriedades,,, `mutedInfo` `inPrivate` `width` e `height` ainda não têm suporte. | `openerTabId``selected`Propriedades, e `highlighted` não são suportadas. |
[guias. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/update) | `pinned` e `muted` ainda não têm suporte. | `highlighted` e `selected` não são compatíveis. |


## webnavigation

`webNavigation`Há suporte para as seguintes APIs:


| API                                                                                                                                                           | Problemas conhecidos                                | Incompatibilidades do Chrome                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [webnavigation](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation)                                                     | As IDs de tabulação estão incorretas.                      | Não há suporte para filtragem, TransitionTypes e TransitionQualifiers. <br/><br/> Para uma guia, todos `processIds` serão iguais. |
| [webnavigation. getAllFrames](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getAllFrames)                           | Não inclui elementos Object-to-iframe. |                                                                                                                             |
| [webnavigation. GetFrame](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getFrame)                                   |                                             |                                                                                                                             |
| [webnavigation. onBeforeNavigate](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onBeforeNavigate)                   |                                             |                                                                                                                             |
| [webnavigation. oncommitd](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onCommitted)                                           |                                             |                                                                                                                             |
| [webnavigation. OnCompleted](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCompleted)                             |                                             |                                                                                                                             |
| [webnavigation. onCreatedNavigationTarget](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCreatedNavigationTarget) |                                             |                                                                                                                             |
| [webnavigation. onDOMContentLoaded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onDOMContentLoaded)               |                                             |                                                                                                                             |
| [webnavigation. onErrorOccurred](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onErrorOccurred)                     |                                             |                                                                                                                             |
| [webnavigation. onHistoryStateUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onHistoryStateUpdated)         |                                             |                                                                                                                             |
| [webnavigation. onReferenceFragmentUpdated](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onReferenceFragmentUpdated)            |                                             |                                                                                                                             |
| [webnavigation. onTabReplaced](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onTabReplaced)                         |                                             | Sem suporte.                                                                                                              |
| [webnavigation. Transitiontype](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionType)                       |                                             |                                                                                                                             |
| [webnavigation. TransitionQualifier](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionQualifier)             |                                             |                                                                                                                             |

## webRequest

`webRequest`Há suporte para as seguintes APIs:

API | Problemas conhecidos | Incompatibilidades do Chrome
:------ | :----- | :-------
[webRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest) | `webRequest` sem suporte para síncrono `XmlHttpRequests` . | Não há suporte para solicitações de rede de extensões, como opções, páginas de plano de fundo ou páginas pop-up.<br/><br/> `<object>`Não há suporte para as solicitações de rede de `<embed>` elementos e.<br/><br/> Os cabeçalhos não podem ser modificados para solicitações armazenadas em cache.  |
[handlerBehaviorChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/handlerBehaviorChanged) | | As alterações do manipulador são manipuladas automaticamente no Microsoft Edge.<br/><br/>Chamar isso não tem efeito.  |
[onAuthRequired](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onAuthRequired) | | |
[onBeforeRedirect](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRedirect) | | |
[onBeforeRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRequest) | | `requestBody` Não é suportada. |
[onBeforeSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeSendHeaders) | | |
[onCompleted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onCompleted) | | |
[onErrorOccurred](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onErrorOccurred) | | |
[onHeadersReceived](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onHeadersReceived) | |  |
[onResponseStarted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onResponseStarted) | |  |
[onSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onSendHeaders) | | |

## windows

`windows`Há suporte para as seguintes APIs:


| API                                                                                                                               | Problemas conhecidos                                                   | Incompatibilidades do Chrome                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [windows](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows)                                     |                                                                | `Window` objetos não dão suporte à `alwaysOnTop` propriedade no Microsoft Edge. <br/><br/>Não há suporte para InPrivate. |
| [Windows. CreateType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/CreateType)                            |                                                                | `"panel"` e `"detached_panel"` não são compatíveis com o Microsoft Edge.                                           |
| [Windows. Create](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/create)                                    |                                                                | `tabId` Não há suporte para o parâmetro de desdivisão de uma guia.                                                       |
| [Windows. obter](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/get)                             |                                                                |                                                                                                                 |
| [Windows. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getAll)                       | `windows.getAll({populate: true})` Não tem a `tabs` propriedade. |                                                                                                                 |
| [Windows. GetCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getCurrent)               |                                                                |                                                                                                                 |
| [Windows. getLastFocused](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getLastFocused)       |                                                                |                                                                                                                 |
| [Windows. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/update)                       | Não há suporte para especificar a posição.                          | `"minimized"`/`"maximized"`/`"fullscreen"` e `drawAttention` não são compatíveis com o Microsoft Edge.             |
| [Windows. OnCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/onCreated)                 |                                                                | `WindowType` Não há suporte para o filtro.                                                                           |
| [Windows. onfocuschanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/onFocusChanged)                    |                                                                | `WindowType` Não há suporte para o filtro.                                                                           |
| [Windows. WindowState](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowState)                          | `"minimized"`, `"maximized"` , `"fullscreen"` não são suportados. | `"docked"` Não é compatível com o Microsoft Edge.                                                                  |
| [Windows. Windowtype](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowType)                            |                                                                | `"panel"`, `"app"` e `"devtools"` não são compatíveis com o Microsoft Edge.                                       |
| [Windows. WINDOW_ID_CURRENT](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_CURRENT) |                                                                |                                                                                                                 |
| [Windows. WINDOW_ID_NONE](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_NONE)       |                                                                |                                                                                                                 |
