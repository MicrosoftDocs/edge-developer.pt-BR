---
ms.assetid: 8b7f362f-da09-43db-8a42-cfa128c1808c
description: Obtenha as respostas a perguntas comuns que você pode ter ao carregar extensões descompactadas.
title: Extensões-solução de problemas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 78013876ba5c2c6c111289f46c81a9fde3ecc964
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561153"
---
# Solução de problemas  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Se você estiver tentando carregar extensões descompactadas e estiver enfrentando problemas, as informações abaixo podem ajudar:

## 1. eu vejo o erro "não foi possível carregar esta extensão"

Isso geralmente significa que o Microsoft Edge não pode acessar a pasta de extensão que você tentou carregar.

Aqui está um resumo dos possíveis erros que podem ocorrer:

Mensagem de erro | Detalhes
:--------- | :------------
Erro de análise do manifesto: arquivo de manifesto ausente ou malformado. | O arquivo `"manifest.json"` não foi encontrado no local especificado ou há algum problema com o arquivo. Para resolver o problema, verifique se a pasta especificada contém o manifesto no nível superior e, em seguida, clique duas vezes nas vírgulas, nas aspas e nos colchetes.
Erro de análise do manifesto: `"content_scripts"` deve definir uma matriz. | O campo `"content_scripts"` deve ser uma matriz. Para resolver o problema, verifique a sintaxe. Por exemplo: `"content_scripts": [{"matches": [...],"css": [...],"js": [...] }]`
Erro de análise do manifesto: `"content_scripts"` deve definir o valor para a `"matches"` propriedade. | A propriedade `"matches"` é necessária. Para resolver o problema, especifique o valor da propriedade com uma matriz de cadeias de caracteres. Por exemplo: `"content_scripts": [ {... "matches": ["http://www.bing.com"] ...} ]`
Erro de análise do manifesto: `"content_scripts"` deve fazer referência a pelo menos um arquivo. css ou. js. | Pelo menos uma propriedade `"css"` ou `"js"` é necessária. Para resolver o problema, especifique o valor da propriedade com uma matriz de cadeias de caracteres. Por exemplo: `"content_scripts": [ { ... "js": ["myScript1.js", "myScript2.js"] ...} ]`
Erro de análise do manifesto: `"<field>"` deve definir o valor para a <property> Propriedade "". | A propriedade do `<property>` campo `<field>` é necessária. Para resolver o problema, especifique um valor válido para `<property>` .
Erro de análise do manifesto: `"content_scripts"` referencia um valor inválido para o campo "run_at". | A propriedade `"run_at"` especifica um valor desconhecido. Para resolver o problema, especifique um dos `"document_start"` , `"document_end"` ou `"document_idle"` . Por exemplo: `"content_scripts": [ {... "run_at": "document_start" ... } ]`
Erro de análise do manifesto: `"<field>"` campo ausente. | O campo `<field>` é obrigatório. Para resolver o problema, defina o campo com um valor válido.
Erro de análise do manifesto: campo inválido `"<field1>"` encontrado em `"<field2>"` . | O campo do <field1> campo <field2> especifica um valor desconhecido. Para resolver o problema, especifique um valor válido para <field1> .
Erro de análise do manifesto: valor inválido para o <field> campo "". | O campo <field> especifica um valor desconhecido. Para resolver o problema, especifique um valor válido.
Erro de análise do manifesto: não há suporte para a extensão da versão atual do Microsoft Edge. | A propriedade `"minimum_edge_version"` especifica uma versão mais recente do Microsoft Edge do que aquela que você possui. Você pode encontrar a versão atual abrindo o "..". (Mais) menu e, em seguida, selecionando "configurações" (seção inferior "sobre este aplicativo"). Para resolver o problema, atualize o navegador para uma versão mais recente ou altere o valor no manifesto. Por exemplo: `"minimum_edge_version": "x.xxxx.xxxx.x"`
Erro de análise do manifesto: `"background"` deve definir o valor para a propriedade "página" ou "scripts". | A propriedade "página" ou "scripts" é necessária para o campo "plano de fundo". Para resolver o problema, especifique uma cadeia de caracteres para "página" ou uma matriz de cadeias de caracteres para "scripts". Por exemplo: `"background": { ... "scripts": ["background.js"] ... }`
Erro de análise do manifesto: `"background"` deve definir o valor para a `"persistent"` propriedade. | A propriedade `"persistent"` é necessária. Para resolver o problema, especifique um valor verdadeiro ou falso. Por exemplo: `"background": {... "persistent": true ...}`
Erro de análise do manifesto: somente um `"browser_action"` ou `"page_action"` pode ser definido. | Uma extensão não pode definir uma ação de página e uma ação de navegador ao mesmo tempo. Para resolver o problema, remova qualquer uma das definições.
Erro não especificado: `<error>` | Mensagem de erro genérica catch-all. `<error>` será substituído pelo erro especificado.


## 2. não vejo o botão "extensão de carga"
Até que as extensões estejam disponíveis pela Microsoft Store, esse botão *deve* estar visível por padrão. Se você abrir o menu "mais" (...), selecione o item de menu "extensões" e não vir o botão, siga estas etapas:

1. Na barra de endereços, digite **"About: Flags"** e pressione a tecla **"Enter"** .
2. No título **"configurações do desenvolvedor"** , certifique-se de que a caixa de seleção ao lado de **"habilitar recursos de desenvolvedor de extensão"** esteja selecionada.

   ![sobre sinalizadores](./media/aboutflags.PNG)  

3. Feche e abra novamente o Microsoft Edge e verifique se o botão **"carregar extensão"** agora está visível.
