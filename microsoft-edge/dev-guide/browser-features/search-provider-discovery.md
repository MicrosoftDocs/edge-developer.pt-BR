---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Se você for um provedor de pesquisa, consulte Como garantir que o Microsoft Edge dê suporte ao seu serviço.
title: Descoberta do provedor de pesquisa-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 4ac8ea966e9c4736834a0be1130a8c2a8dfb2614
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941971"
---
# Descoberta de provedores de pesquisa  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

A integração de pesquisa avançada está embutida na barra de endereços do Microsoft Edge, incluindo sugestões de pesquisa, resultados da Web, seu histórico de navegação e favoritos.  O Microsoft Edge segue a especificação [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para descobrir e usar provedores de pesquisa na Web.  Se você for um provedor de pesquisa, veja como garantir que o Microsoft Edge dê suporte ao seu serviço.  

> PRINCIPAIS Para a segurança e a privacidade do usuário, o Microsoft Edge requer que todas as pesquisas sejam conduzidas via SSL.  

Os recursos a seguir devem ser especificados como `https` URLs para habilitar a integração do Microsoft Edge do seu mecanismo de pesquisa:  

*   O site que contém a referência ao documento de descrição  
*   A URL para o próprio documento de descrição  
*   O modelo de consulta de pesquisa  

1.  Forneça um arquivo de descrição OpenSearch, que contém o nome do provedor de pesquisa, e o modelo a ser usado para construir a pesquisa.  Aqui está um exemplo de documento:  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  Inclua uma referência ao arquivo de descrição do OpenSearch na seção de cabeçalho de suas páginas (geralmente isso inclui a home page do site e as páginas de resultados da pesquisa), por exemplo:  
    
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
    
Quando um usuário navega para o serviço de pesquisa, sua descrição OpenSearch será automaticamente removida e salva para uso posterior.  O usuário poderá acessar as configurações do Microsoft Edge e escolher Adicionar seu serviço de pesquisa à sua lista de provedores de pesquisa para a barra de endereços do Microsoft Edge.  

Consulte a especificação [opensearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para obter detalhes adicionais sobre como criar seu documento de descrição do OpenSearch.  
