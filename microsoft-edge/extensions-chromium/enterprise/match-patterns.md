---
description: Enterprise de política para Extensões de Borda (Chromium).
title: Padrões de Correspondência
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: fcb87b62cac063c7663f575fa3d992b187408c28
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461245"
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
# <a name="match-patterns"></a>Padrões de Correspondência

Permissões de host e correspondência de script de conteúdo se baseiam em um conjunto de URLs definidas por padrões de correspondência.  Um padrão de match é essencialmente uma URL que começa com um esquema permitido ( , , , ou , e que `http` `https` pode conter ' `file` `ftp` `*` caracteres '.  O padrão especial `<all_urls>` corresponde a qualquer URL que comece com um esquema permitido.  Cada padrão de match tem 3 partes:  

*   _scheme_ — por exemplo, `http` `file` ou ou `*`  

> [!NOTE]
> O acesso `file` a URLs não é automático.  O usuário deve visitar a página de gerenciamento extensões e optar por `file` acessar cada Extensão que o solicitar.  

*   `_host_` — por exemplo, `www.google.com` ou ou ; se o esquema for `*.google.com` `*` arquivo, não haverá parte do host.  
*   `_path_` — por exemplo, `/*` , `/foo*` ou `/foo/bar` .  O caminho deve estar presente em uma permissão de host, mas é sempre tratado como `/*` .  

A sintaxe básica:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

O significado de `*` depende se ele está na parte esquema, host ou caminho.  Se o esquema for `*` , em seguida, ele corresponde `http` ou , e não , ou `https` `file` `ftp` .  Se o host for `*` apenas , então ele corresponde a qualquer host. Se o host for , ele corresponde ao host especificado ou a qualquer `*.hostname` um dos subdomas.  Na seção caminho, cada um `*` corresponde a 0 ou mais caracteres.  A tabela a seguir mostra alguns padrões válidos.  

| Pattern | Função | Exemplos de URLs correspondentes |  
|:--- |:--- |:--- |  
| `http://*/*` | Corresponde a qualquer URL que use o esquema http | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Corresponde a qualquer URL que use o esquema http, em qualquer host, desde que o caminho comece com `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Corresponde a qualquer URL que use o esquema https, está em um `google.com` host \(como `www.google.com` , ou `docs.google.com` `google.com` \), desde que o caminho comece com e `/foo` termine com `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Corresponde à URL especificada | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Corresponde a qualquer arquivo local cujo caminho começa com `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Corresponde a qualquer URL que usa o `http` esquema e está no host `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Corresponde a qualquer URL que comece com `http://mail.google.com` ou `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Corresponde a qualquer URL que use um esquema permitido. \(Consulte o início desta seção para a lista de esquemas permitidos.\) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Aqui estão alguns exemplos de `_invalid_` combinações de padrão:

| Padrão ruim | Por que é ruim |  
|:--- |:--- |  
| `http://www.foo.com` | Não `_path_` |  
| `http://*foo/bar` | ' `*` ' no host pode ser seguido somente por um ' ' ou ' `.` `/` ' |  
| `http://foo.*.bar/baz` | Se ' `*` ' estiver no , ele deve ser o primeiro `_host_` caractere |  
| `http:/bar` | Separador `_scheme_` ausente \(' `/` ' deve ser " `//` "\) |  
| `foo://*` | Inválido `_scheme_` |  

Alguns esquemas não são suportados em todos os contextos.

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/extensions/match_patterns).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
