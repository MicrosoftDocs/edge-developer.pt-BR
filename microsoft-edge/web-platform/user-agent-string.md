---
description: Esta página fornece documentação sobre a cadeia de caracteres do agente de usuário do Microsoft Edge
title: Cadeia de caracteres do agente de usuário do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web, Cadeia de caracteres do agente do usuário, Cadeia de UA, substituição de UA
ms.openlocfilehash: 73401219b7708a739292a46b6131fe40765e9c8c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562532"
---
# Cadeia de caracteres do agente de usuário do Microsoft Edge (Desktop)  

Uma cadeia de caracteres de agente do usuário \ (UA \) pode ser usada para detectar qual versão de um navegador específico está sendo usada em um determinado sistema operacional.  Como outros navegadores, o Microsoft Edge inclui essas informações no `User-Agent` cabeçalho http sempre que faz uma solicitação para um site.  Ele também pode ser acessado via JavaScript consultando o valor de `navigator.userAgent` .  

A Microsoft recomenda que os desenvolvedores da Web façam uso da [detecção de recursos](https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection) sempre que possível para melhorar a manutenção do código, reduzir o código Fragility e eliminar o risco de quebra de código no caso de atualizações de cadeia de caracteres do UA futuras.  

Para casos em que a detecção de recursos não é aplicável e a detecção de UA deve ser usada, o formato do Microsoft Edge UA na área de trabalho é o seguinte:

O `User-Agent` cabeçalho da solicitação está no seguinte formato:

```http
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43
``` 

O valor de retorno de `navigator.userAgent` está no seguinte formato:

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43"
```  

Os identificadores de plataforma mudam com base no sistema operacional sendo usado, e os números de versão também são incrementados conforme o tempo passar.  Esse formato é o mesmo que o UA Chromium com a adição de um novo `Edg` token no final.  A Microsoft selecionou o `Edg` token para evitar problemas de compatibilidade que podem ser causados pelo uso da cadeia de caracteres `Edge` , que é usada pela versão do Microsoft Edge baseada no EdgeHTML.  O `Edg` token também é consistente com os [tokens existentes](https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer/) usados em Ios e Android.

## Mapeando cadeia de caracteres de UA para o nome do navegador
Mapear tokens de cadeia de caracteres de UA para um nome de navegador mais legível pelo homem para uso no código é um padrão comum na Web hoje. Ao mapear o novo `Edg` token para um nome de navegador, a Microsoft recomenda usar um nome diferente do que os desenvolvedores usados para a versão herdada do Microsoft Edge para evitar aplicar acidentalmente qualquer solução alternativa herdada que não se aplica a navegadores baseados em Chromium.

## Substituições de agente do usuário  

Às vezes, um site não reconhece a versão atualizada do Microsoft Edge UA.  Como resultado, um conjunto de recursos desse site pode não funcionar corretamente.  Quando a Microsoft é notificado sobre esses tipos de problemas, os proprietários do site são contatados e informados sobre o UA atualizado.  

Os sites geralmente precisam de algum tempo para atualizar e testar a lógica de detecção de UA para solucionar os problemas que a Microsoft informa para os proprietários de sites.  Nesses casos, a Microsoft usa uma lista de substituições de UA em nossos canais beta e estável para maximizar a compatibilidade para os usuários que acessam esses sites.  As substituições especificam novos valores de UA que o Microsoft Edge deve enviar em vez do UA padrão para sites específicos.  Você pode visualizar a lista de substituições de UA que estão sendo aplicadas ao navegar `edge://compat/useragent` nos canais beta e estável do Microsoft Edge. 

Os canais Canárias e dev não recebem substituições de UA no momento para que os desenvolvedores da Web tenham um ambiente onde possam facilmente reproduzir problemas em seus sites causados pelo Microsoft Edge UA padrão.  Se, por algum motivo, você precisar desabilitar substituições do UA nos canais beta ou estável do Microsoft Edge, será possível executar o executável do Microsoft Edge usando o seguinte argumento de linha de comando:  

```shell
--disable-domain-action-user-agent-override
```  
