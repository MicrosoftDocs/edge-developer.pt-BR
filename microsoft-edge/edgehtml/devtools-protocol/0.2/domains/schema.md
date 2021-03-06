---
description: Referência do Protocolo DevTools Versão 0.2 (EdgeHTML) para o Domínio de Esquema. Fornece informações sobre o esquema de protocolo.
title: Domínio do Esquema - DevTools Protocol Versão 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398144"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a>Domínio do Esquema - DevTools Protocol Versão 0.2 (EdgeHTML)  

Fornece informações sobre o esquema de protocolo.  

| Classificação | Membros |  
|:--- |:--- |  
| [Métodos](#methods) | [getDomains](#getdomains) |  
| [Tipos](#types) | [Objeto Domain](#domain) |  

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
