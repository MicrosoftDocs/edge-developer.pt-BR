---
description: Documentação de política empresarial para extensões Edge (Chromium).
title: Padrões de correspondência
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 16f54fcdc127822e89e050c367a681d886b0c8d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561311"
---
# Padrões de correspondência

As permissões de host e a correspondência de script de conteúdo se baseiam em um conjunto de URLs definidas por padrões de correspondência.  Um padrão de correspondência é essencialmente uma URL que começa com um esquema permitido (,,, `http` `https` `file` ou `ftp` , e que pode conter `*` caracteres ' '.  O padrão especial `<all_urls>` corresponde a qualquer URL que comece com um esquema permitido.  Cada padrão de correspondência tem 3 partes:  

*   _esquema_ — por exemplo, `http` ou `file` ou `*`  

> [!NOTE]
> O acesso a `file` URLs não é automático.  O usuário deve acessar a página Gerenciamento de extensões e aceitar o `file` Access para cada extensão que a solicita.  

*   `_host_` — por exemplo, `www.google.com` ou `*.google.com` ou `*` ; se o esquema for arquivo, não há parte do host.  
*   `_path_` -por exemplo, `/*` , `/foo*` ou `/foo/bar` .  O caminho deve estar presente em uma permissão de host, mas é sempre tratado como `/*` .  

A sintaxe básica:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

O significado de `*` depende se ele está no esquema, no host ou na parte do caminho.  Se o esquema estiver `*` , ele corresponderá a `http` ou `https` , e não `file` ou `ftp` .  Se o host for apenas `*` , ele corresponderá a qualquer host. Se o host estiver `*.hostname` , ele corresponderá ao host especificado ou a qualquer um dos subdomínios.  Na seção caminho, cada um `*` corresponde a 0 ou mais caracteres.  A tabela a seguir mostra alguns padrões válidos.  

| Pattern | O que ele faz | Exemplos de URLs correspondentes |  
|:--- |:--- |:--- |  
| `http://*/*` | Corresponde a qualquer URL que use o esquema http | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Corresponde a qualquer URL que use o esquema http, em qualquer host, desde que o caminho comece com `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Corresponde a qualquer URL que usa o esquema HTTPS, está em um `google.com` host \ (como `www.google.com` , `docs.google.com` ou `google.com` \), desde que o caminho comece `/foo` e termine com `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Corresponde à URL especificada | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Corresponde a qualquer arquivo local cujo caminho comece com `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Corresponde a qualquer URL que use o `http` esquema e esteja no host `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Corresponde a qualquer URL que comece com `http://mail.google.com` ou `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Corresponde a qualquer URL que use um esquema permitido. \ (Consulte o início desta seção para obter a lista de esquemas permitidos. \) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Estes são alguns exemplos de `_invalid_` padrões correspondentes:

| Padrão ruim | Por que é ruim |  
|:--- |:--- |  
| `http://www.foo.com` | Não `_path_` |  
| `http://*foo/bar` | ' `*` ' no host só pode ser seguido por um ' `.` ' ou ' `/` ' |  
| `http://foo.*.bar/baz` | Se ' `*` ' estiver no `_host_` , deve ser o primeiro caractere |  
| `http:/bar` | Faltando `_scheme_` separador \ (' `/` ' deve ser " `//` " \) |  
| `foo://*` | Inválido `_scheme_` |  

Alguns esquemas não são compatíveis com todos os contextos.

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/extensions/match_patterns/).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
