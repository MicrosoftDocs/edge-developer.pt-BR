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
# <span data-ttu-id="d8348-104">Descoberta de provedores de pesquisa</span><span class="sxs-lookup"><span data-stu-id="d8348-104">Search provider discovery</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="d8348-105">A integração de pesquisa avançada está embutida na barra de endereços do Microsoft Edge, incluindo sugestões de pesquisa, resultados da Web, seu histórico de navegação e favoritos.</span><span class="sxs-lookup"><span data-stu-id="d8348-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="d8348-106">O Microsoft Edge segue a especificação [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para descobrir e usar provedores de pesquisa na Web.</span><span class="sxs-lookup"><span data-stu-id="d8348-106">Microsoft Edge follows the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification to discover and use web search providers.</span></span>  <span data-ttu-id="d8348-107">Se você for um provedor de pesquisa, veja como garantir que o Microsoft Edge dê suporte ao seu serviço.</span><span class="sxs-lookup"><span data-stu-id="d8348-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>  

> <span data-ttu-id="d8348-108">PRINCIPAIS Para a segurança e a privacidade do usuário, o Microsoft Edge requer que todas as pesquisas sejam conduzidas via SSL.</span><span class="sxs-lookup"><span data-stu-id="d8348-108">[IMPORTANT] For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>  

<span data-ttu-id="d8348-109">Os recursos a seguir devem ser especificados como `https` URLs para habilitar a integração do Microsoft Edge do seu mecanismo de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="d8348-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>  

*   <span data-ttu-id="d8348-110">O site que contém a referência ao documento de descrição</span><span class="sxs-lookup"><span data-stu-id="d8348-110">The site that contains the reference to the description document</span></span>  
*   <span data-ttu-id="d8348-111">A URL para o próprio documento de descrição</span><span class="sxs-lookup"><span data-stu-id="d8348-111">The URL to the description document itself</span></span>  
*   <span data-ttu-id="d8348-112">O modelo de consulta de pesquisa</span><span class="sxs-lookup"><span data-stu-id="d8348-112">The search query template</span></span>  

1.  <span data-ttu-id="d8348-113">Forneça um arquivo de descrição OpenSearch, que contém o nome do provedor de pesquisa, e o modelo a ser usado para construir a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d8348-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span>  <span data-ttu-id="d8348-114">Aqui está um exemplo de documento:</span><span class="sxs-lookup"><span data-stu-id="d8348-114">Here is an example document:</span></span>  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  <span data-ttu-id="d8348-115">Inclua uma referência ao arquivo de descrição do OpenSearch na seção de cabeçalho de suas páginas (geralmente isso inclui a home page do site e as páginas de resultados da pesquisa), por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8348-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>  
    
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
    
<span data-ttu-id="d8348-116">Quando um usuário navega para o serviço de pesquisa, sua descrição OpenSearch será automaticamente removida e salva para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="d8348-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span>  <span data-ttu-id="d8348-117">O usuário poderá acessar as configurações do Microsoft Edge e escolher Adicionar seu serviço de pesquisa à sua lista de provedores de pesquisa para a barra de endereços do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d8348-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>  

<span data-ttu-id="d8348-118">Consulte a especificação [opensearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para obter detalhes adicionais sobre como criar seu documento de descrição do OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="d8348-118">See the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification for further details on creating your OpenSearch description document.</span></span>  
