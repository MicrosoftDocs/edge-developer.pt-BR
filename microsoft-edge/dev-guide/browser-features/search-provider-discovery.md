---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Se você for um provedor de pesquisa, consulte Como garantir que o Microsoft Edge dê suporte ao seu serviço.
title: Guia de desenvolvimento-descoberta de provedores de pesquisa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: ac23c2c62d436d5772b498208a56ad306eb8cb3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560564"
---
# Descoberta de provedores de pesquisa


A integração de pesquisa avançada está embutida na barra de endereços do Microsoft Edge, incluindo sugestões de pesquisa, resultados da Web, seu histórico de navegação e favoritos. O Microsoft Edge segue a especificação [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) para descobrir e usar provedores de pesquisa na Web. Se você for um provedor de pesquisa, veja como garantir que o Microsoft Edge dê suporte ao seu serviço.

**Para a segurança e a privacidade do usuário, o Microsoft Edge requer que todas as pesquisas sejam conduzidas via SSL.** Os recursos a seguir devem ser especificados como `https` URLs para habilitar a integração do Microsoft Edge do seu mecanismo de pesquisa:
* O site que contém a referência ao documento de descrição
* A URL para o próprio documento de descrição
* O modelo de consulta de pesquisa 

1.  Forneça um arquivo de descrição OpenSearch, que contém o nome do provedor de pesquisa, e o modelo a ser usado para construir a pesquisa. Aqui está um exemplo de documento:

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  Inclua uma referência ao arquivo de descrição do OpenSearch na seção de cabeçalho de suas páginas (geralmente isso inclui a home page do site e as páginas de resultados da pesquisa), por exemplo:

    ```html
    <html>
        <head>
            <link rel="search" 
                type="application/opensearchdescription+xml"  
                href="https://contoso.com/content-search.xml" 
                title="Contoso search" /> 
        </head> 
        <body> 
        ...
    ```

Quando um usuário navega para o serviço de pesquisa, sua descrição OpenSearch será automaticamente removida e salva para uso posterior. O usuário poderá acessar as configurações do Microsoft Edge e escolher Adicionar seu serviço de pesquisa à sua lista de provedores de pesquisa para a barra de endereços do Microsoft Edge.

Consulte a especificação [opensearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) para obter detalhes adicionais sobre como criar seu documento de descrição do OpenSearch.
