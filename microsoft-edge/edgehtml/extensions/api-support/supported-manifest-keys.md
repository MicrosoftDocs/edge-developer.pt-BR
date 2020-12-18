---
description: Encontre informações sobre as chaves de manifesto com suporte, bem como seus problemas conhecidos/incompatibilidades com o Chrome.
title: Extensões-chaves de manifesto com suporte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f8413193ddb834eb7e31e4101c2b027c48bc501d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231940"
---
# Chaves de manifesto com suporte  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Cada extensão tem um arquivo de manifesto formatado por JSON, chamado manifest.js. Esse arquivo fornece informações importantes para a extensão que variam do seu nome às suas permissões. A menos que especificado em uma observação abaixo, as propriedades do manifesto do Microsoft Edge seguem a mesma implementação do Chrome.

Aqui está um exemplo de um [arquivo de manifesto JSON do Microsoft Edge](./supported-manifest-keys/json-manifest-example.md).

## Teclas obrigatórias

As seguintes teclas são necessárias:

Chave | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :--------------
[autor](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author)  | | 
[name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) | | |
[version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/version) | | |

## Teclas recomendadas

As teclas a seguir são recomendadas:

Chave | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :--------------
browser_specific_settings | | Indica o estado preferencial da extensão no navegador. O navegador pode optar por não respeitar isso em uma versão futura, dependendo dos fatores como a reputação da extensão ou do número total de botões já na barra de endereços do usuário. Isso pode ser usado para indicar a posição padrão do `browserAction` ícone. </br></br> `"browser_specific_settings": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;`"edge": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`"browser_action_next_to_addressbar": true`</br>&nbsp;&nbsp;&nbsp;&nbsp;`}`</br>`}` </br></br> Não é compatível com o Chrome.|
[default_locale](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/default_locale)| | |
[description](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/description) | | |
[ícones](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/icons) | | |
[manifest_version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version) | | Atualmente ignorado no Microsoft Edge.



## teclas de browser_action ou page_action

Você só pode incluir uma das seguintes teclas (ou nenhuma):

Chave | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :--------------
[browser_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action)  | | O Microsoft Edge não suporta a seguinte sintaxe:  `browser_action : {"default_icon" : "icon.png" }`   <br/>O tamanho dos ícones deve ser especificado. <br/>Tamanhos preferenciais: 20px, 25px, 30px, 40px. <br/> Outros tamanhos com suporte: 19px, 35px, 38px.|
[page_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) | | O Microsoft Edge não suporta a seguinte sintaxe:  `page_action : {"default_icon" : "icon.png" }`   <br/>O tamanho dos ícones deve ser especificado. <br/>Tamanhos preferenciais: 20px, 25px, 30px, 40px. <br/>Outros tamanhos com suporte: 19px, 35px, 38px.|

## Teclas opcionais

As teclas a seguir são opcionais:

Chave | Problemas conhecidos | Incompatibilidades do Chrome
:------------ | :------------- | :--------------
[tela de fundo](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) | | Persistente é um campo obrigatório para o Microsoft Edge.
[content_scripts](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_scripts)  | | |
[content_security_policy](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_security_policy)  | A política de segurança de conteúdo de uma página bloqueia WebSockets em scripts de conteúdo, gerando uma exceção indefinida. | Atualmente, as extensões do Microsoft Edge dão suporte apenas a [restrições de política padrão](https://developer.mozilla.org/Add-ons/WebExtensions/Content_Security_Policy#Default_content_security_policy): `script-src 'self'; object-src 'self'` |
[Incognito](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/incognito) | | | 
key  | | |
options_page | | |
[Elas](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions)  | | |
short_name  | | |
[web_accessible_resources](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/web_accessible_resources) | | |

### Permissões com suporte
Há suporte para as seguintes [permissões](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions) :


| Permissão         | Descrição                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<all_urls\>       | Permite que os scripts de tela de fundo e de conteúdo interajam com todas as páginas da Web com [privilégios](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions#Host_permissions)extras.                                                                                  |
| contextMenus       | Dá acesso à `contextMenus` API. Isso permite adicionar itens ao menu de contexto da Microsoft Edge.                                                                                                                                                                                     |
| cookies            | Dá acesso à `cookies` API. Isso permite a consulta e modificação de cookies, bem como ser notificado quando eles mudam.                                                                                                                                                           |
| Geolocation        | Permita que a extensão use a `geolocation` API HTML5 sem solicitar permissão ao usuário.                                                                                                                                                                                   |
| ociosidade               | Dá acesso à `idle` API. Isso permite a detecção de quando o estado ocioso da máquina muda.                                                                                                                                                                                    |
| armazenamento            | Dá acesso à `storage` API. Isso permite armazenar, recuperar e controlar as alterações dos dados do usuário.                                                                                                                                                                             |
| efetua               | Dá acesso à `tabs` API para interagir com o sistema de guia do navegador. Isso permite a criação, modificação e reorganização de guias no navegador, incluindo as URLs associadas a cada guia.                                                                                       |
| unlimitedStorage   | Permite [armazenamento. local](https://developer.mozilla.org/Add-ons/WebExtensions/API/storage/local) para ter armazenamento ilimitado (dependendo dos recursos do sistema) em vez de 5 MB. O par armazenamento por chave de valor máximo também é aumentado de 5 MB a ilimitado (dependendo dos recursos do sistema). |
| webnavigation      | Dá acesso à `webNavigation` API. Isso permite receber notificações sobre o status de solicitações de navegação.                                                                                                                                                              |
| webRequest         | Dá acesso à `webRequest` API. Isso permite observar e analisar o tráfego, bem como interceptar, bloquear ou modificar solicitações em trânsito.                                                                                                                               |
| webRequestBlocking | Obrigatório se uma extensão usa a `webRequest` API de maneira bloqueada.                                                                                                                                                                                                           |

'""'
