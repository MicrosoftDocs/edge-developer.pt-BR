---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio de Esquema. Fornece informações sobre o esquema de protocolo.
title: Domínio do Esquema - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398858"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a>Domínio do Esquema - DevTools Protocol Versão 0.1 (EdgeHTML)  

Fornece informações sobre o esquema de protocolo.  

| Classificação | Membros |  
|:--- |:--- |  
| [Métodos](#methods) | [getDomains](#getdomains) |  
| [Tipos](#types) | [Domínio](#domain) |  

## <a name="methods"></a>Métodos  

### <a name="getdomains"></a>getDomains  

Retorna domínios com suporte.  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| domínios | [Domínio[]](#domain) | Lista de domínios com suporte. |  

---  

## <a name="types"></a>Tipos  

### <a name="domain-object"></a>Objeto Domain  

<a name="domain"></a>  

Descrição do domínio do protocolo.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| name | `string` | Nome do domínio. |  
| version | `string` | Versão de domínio. |  

---  
