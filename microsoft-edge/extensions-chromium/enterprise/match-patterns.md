---
description: Documentação de política empresarial para extensões Edge (Chromium).
title: Padrões de Correspondência
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 59427769a010ca774833a809d3025e7594634202
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015657"
---
# <span data-ttu-id="1744f-104">Padrões de Correspondência</span><span class="sxs-lookup"><span data-stu-id="1744f-104">Match Patterns</span></span>

<span data-ttu-id="1744f-105">As permissões de host e a correspondência de script de conteúdo se baseiam em um conjunto de URLs definidas por padrões de correspondência.</span><span class="sxs-lookup"><span data-stu-id="1744f-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="1744f-106">Um padrão de correspondência é essencialmente uma URL que começa com um esquema permitido (,,, `http` `https` `file` ou `ftp` , e que pode conter `*` caracteres ' '.</span><span class="sxs-lookup"><span data-stu-id="1744f-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="1744f-107">O padrão especial `<all_urls>` corresponde a qualquer URL que comece com um esquema permitido.</span><span class="sxs-lookup"><span data-stu-id="1744f-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="1744f-108">Cada padrão de correspondência tem 3 partes:</span><span class="sxs-lookup"><span data-stu-id="1744f-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="1744f-109">_esquema_ — por exemplo, `http` ou `file` ou</span><span class="sxs-lookup"><span data-stu-id="1744f-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="1744f-110">O acesso a `file` URLs não é automático.</span><span class="sxs-lookup"><span data-stu-id="1744f-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="1744f-111">O usuário deve acessar a página Gerenciamento de extensões e aceitar o `file` Access para cada extensão que a solicita.</span><span class="sxs-lookup"><span data-stu-id="1744f-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="1744f-112">— por exemplo, `www.google.com` ou `*.google.com` ou `*` ; se o esquema for arquivo, não há parte do host.</span><span class="sxs-lookup"><span data-stu-id="1744f-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="1744f-113">-por exemplo, `/*` , `/foo*` ou `/foo/bar` .</span><span class="sxs-lookup"><span data-stu-id="1744f-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="1744f-114">O caminho deve estar presente em uma permissão de host, mas é sempre tratado como `/*` .</span><span class="sxs-lookup"><span data-stu-id="1744f-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="1744f-115">A sintaxe básica:</span><span class="sxs-lookup"><span data-stu-id="1744f-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="1744f-116">O significado de `*` depende se ele está no esquema, no host ou na parte do caminho.</span><span class="sxs-lookup"><span data-stu-id="1744f-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="1744f-117">Se o esquema estiver `*` , ele corresponderá a `http` ou `https` , e não `file` ou `ftp` .</span><span class="sxs-lookup"><span data-stu-id="1744f-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="1744f-118">Se o host for apenas `*` , ele corresponderá a qualquer host.</span><span class="sxs-lookup"><span data-stu-id="1744f-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="1744f-119">Se o host estiver `*.hostname` , ele corresponderá ao host especificado ou a qualquer um dos subdomínios.</span><span class="sxs-lookup"><span data-stu-id="1744f-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="1744f-120">Na seção caminho, cada um `*` corresponde a 0 ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="1744f-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="1744f-121">A tabela a seguir mostra alguns padrões válidos.</span><span class="sxs-lookup"><span data-stu-id="1744f-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="1744f-122">Pattern</span><span class="sxs-lookup"><span data-stu-id="1744f-122">Pattern</span></span> | <span data-ttu-id="1744f-123">Função</span><span class="sxs-lookup"><span data-stu-id="1744f-123">What it does</span></span> | <span data-ttu-id="1744f-124">Exemplos de URLs correspondentes</span><span class="sxs-lookup"><span data-stu-id="1744f-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="1744f-125">Corresponde a qualquer URL que use o esquema http</span><span class="sxs-lookup"><span data-stu-id="1744f-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="1744f-126">Corresponde a qualquer URL que use o esquema http, em qualquer host, desde que o caminho comece com</span><span class="sxs-lookup"><span data-stu-id="1744f-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="1744f-127">Corresponde a qualquer URL que usa o esquema HTTPS, está em um `google.com` host \ (como `www.google.com` , `docs.google.com` ou `google.com` \), desde que o caminho comece `/foo` e termine com</span><span class="sxs-lookup"><span data-stu-id="1744f-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="1744f-128">Corresponde à URL especificada</span><span class="sxs-lookup"><span data-stu-id="1744f-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="1744f-129">Corresponde a qualquer arquivo local cujo caminho comece com</span><span class="sxs-lookup"><span data-stu-id="1744f-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="1744f-130">Corresponde a qualquer URL que use o `http` esquema e esteja no host</span><span class="sxs-lookup"><span data-stu-id="1744f-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="1744f-131">Corresponde a qualquer URL que comece com `http://mail.google.com` ou `https://mail.google.com` .</span><span class="sxs-lookup"><span data-stu-id="1744f-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="1744f-132">Corresponde a qualquer URL que use um esquema permitido.</span><span class="sxs-lookup"><span data-stu-id="1744f-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="1744f-133">\ (Consulte o início desta seção para obter a lista de esquemas permitidos. \)</span><span class="sxs-lookup"><span data-stu-id="1744f-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="1744f-134">Estes são alguns exemplos de `_invalid_` padrões correspondentes:</span><span class="sxs-lookup"><span data-stu-id="1744f-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="1744f-135">Padrão ruim</span><span class="sxs-lookup"><span data-stu-id="1744f-135">Bad pattern</span></span> | <span data-ttu-id="1744f-136">Por que é ruim</span><span class="sxs-lookup"><span data-stu-id="1744f-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="1744f-137">Não</span><span class="sxs-lookup"><span data-stu-id="1744f-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="1744f-138">' `*` ' no host só pode ser seguido por um ' `.` ' ou ' `/` '</span><span class="sxs-lookup"><span data-stu-id="1744f-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="1744f-139">Se ' `*` ' estiver no `_host_` , deve ser o primeiro caractere</span><span class="sxs-lookup"><span data-stu-id="1744f-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="1744f-140">Faltando `_scheme_` separador \ (' `/` ' deve ser " `//` " \)</span><span class="sxs-lookup"><span data-stu-id="1744f-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="1744f-141">Inválido</span><span class="sxs-lookup"><span data-stu-id="1744f-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="1744f-142">Alguns esquemas não são compatíveis com todos os contextos.</span><span class="sxs-lookup"><span data-stu-id="1744f-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="1744f-143">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1744f-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1744f-144">A página original foi encontrada [aqui](https://developer.chrome.com/extensions/match_patterns/).</span><span class="sxs-lookup"><span data-stu-id="1744f-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns/).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1744f-146">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1744f-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
