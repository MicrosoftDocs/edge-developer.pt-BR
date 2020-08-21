---
description: Esta página fornece uma visão geral do que há de novo no EdgeHTML 14.
title: Novos recursos e APIs no EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 7f3fcbbf84873fbf0851e1652bde48632e6c4378
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941909"
---
# O que há de novo no EdgeHTML 14  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Aqui estão as alterações fornecidas com o EdgeHTML 14, a partir da [atualização de aniversário do Windows 10](https://blogs.windows.com/windowsexperience/2016/06/29) \ (08/2016, Build 14393 \).  Para obter uma visão geral das alterações no navegador geral do Microsoft Edge, consulte [apresentando o EdgeHTML 14 com a atualização de aniversário do Windows 10](https://blogs.windows.com/msedgedev/2016/08/04).  

Aqui está o link permanente para a seguinte lista de alterações: [https://aka.ms/devguide_edgehtml_14](./edgehtml-14.md) .  

## Novos recursos  

### Extensões  

As extensões são pequenos programas que podem ser usados para adicionar novos recursos ao Microsoft Edge ou modificar a funcionalidade existente.  As extensões têm a finalidade de melhorar a experiência de navegação de um usuário fornecendo funcionalidades de nicho que são importantes para os públicos-alvo.  O Microsoft Edge oferece suporte a um novo modelo de extensão baseado em HTML, JavaScript e CSS.  Esse novo modelo é compatível com o Chrome, o que significa que os desenvolvedores de extensão Chrome existentes poderão migrar suas extensões para o Microsoft Edge com alterações mínimas.  Para obter mais informações, confira documentos para desenvolvedores de [extensões do Microsoft Edge](../../extensions/index.md) .  

### API de busca  
A [API de busca](https://fetch.spec.whatwg.org#fetch-api) usa o `fetch` método para buscar recursos.  Antes disso, foi atingido `XMLHttpRequest` .  A busca não só é mais simples de usar, além de oferecer acesso de nível inferior a solicitações e respostas.  Leia mais sobre a API de busca na postagem de blog do Microsoft Edge, [busque (ou as limitações não negadas de XHR)](https://blogs.windows.com/msedgedev/2016/05/24).  

### JavaScript  

O EdgeHTML 14 traz vários recursos novos e experimentais para Chakra, o mecanismo de JavaScript que desliga o Microsoft Edge:  

#### Novos recursos  

Ativado por padrão  

*   [Parâmetros padrão](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) \ (ES2015 \)
*   [Operador de exponenciação](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) \ (ES2016 \)
*   [Array. prototype. inclui](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) \ (ES2016 \)
*   [Object. Values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) e [Object. Entries](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) \ (ES2017 \)  

#### Recursos de JavaScript experimental  

Habilitado com `about:flags`  

*   [Módulos](https://blogs.windows.com/msedgedev/2016/05/17) \ (ES2015 \)  
*   [Async/Await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) \ (ES2017 \)  
*   [Símbolos Regex](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) \ (ES2015 \)  

Para obter mais detalhes, confira a [visualização de módulos ES6 e muito mais do ES2015, do ES2016 e de versões mais recentes,](https://blogs.windows.com/msedgedev/2016/05/17) e [o código assíncrono fica mais fácil com o suporte à função assíncrona ES2016 no Chakra e no Microsoft Edge](https://blogs.windows.com/msedgedev/2015/09/30).  

### API de autenticação da Web  

API Web do FIDO 2,0  

A API da autenticação da Web \ (anteriormente FIDO 2,0 \) no Microsoft Edge permite que os aplicativos da Web usem a biometria do [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) para autenticação de usuário, para que você e seus usuários possam evitar todas as complicações e riscos de gerenciamento de senhas, incluindo adivinhação de senha, phishing e ataques de registro em log de registros.  A implementação atual do Microsoft Edge \ ( `ms-` prefixado \) baseia-se em um rascunho anterior da especificação de autenticação da Web e provavelmente mudará no futuro.  Leia mais sobre autenticação na Web:  [autenticação da Web e Windows Hello](../windows-integration/web-authentication.md).

### Notificações da Web
As notificações da Web permitem que os sites exibam notificações para alertar os usuários fora do contexto da página da Web e do navegador, mantendo os usuários informados sobre novas mensagens ou alertas e permitindo que os sites aprimorem o envolvimento do usuário.  As notificações da Web no Microsoft Edge são totalmente integradas à plataforma de notificação e à central de ações no Windows 10, fornecendo uma experiência consistente com outros aplicativos em todo o sistema e controles fáceis de permissões e de horas de silêncio.  Verifique as [notificações da Web no Microsoft Edge](https://blogs.windows.com/msedgedev/2016/05/16) para obter mais informações.  

### API Web Speech
A [API de voz da Web](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) é uma API JavaScript composta por duas partes: reconhecimento de fala e sintetização de fala \ (ou texto em fala \).  No momento, o Microsoft Edge aceita apenas a sintetização de fala.  A sintetização de fala envolve a conversão de texto em fala que um usuário ouve através de seus alto-falantes.  Confira o artigo [da Web Speech:](https://developer.mozilla.org/docs/Web/API/Web_Speech_API) guia do desenvolvedor de síntese de fala para obter mais informações.  

## Novas APIs no EdgeHTML 14

Aqui está a lista completa de novas APIs no EdgeHTML 14.  Elas são listadas no formato de `[interface name].[api name]` .  

<iframe height='585' scrolling='no' title='Novas APIs no EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Veja a caneta <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> New APIs no EdgeHTML 14 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>  
