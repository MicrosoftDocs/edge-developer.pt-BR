---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio da Página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Domínio da Página - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399145"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a>Domínio da Página - DevTools Protocol Versão 0.1 (EdgeHTML)  

Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.  

| Classificação | Membros |  
|:--- |:--- |  
| [**Métodos**](#methods) | [habilitar](#enable), [desabilitar,](#disable) [navegar](#navigate) |  
| [**Tipos**](#types) | [FrameId](#frameid) |  

## <a name="methods"></a>Métodos  

### <a name="enable"></a>Habilitar  

Habilita notificações de domínio de página.  

&nbsp;  

---  

### <a name="disable"></a>Desabilitar   

Desabilita notificações de domínio de página.  

&nbsp;  

---  

### <a name="navigate"></a>navegar  

Navega a página atual para a URL determinada.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| url | `string` | URL para navegar na página. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | **Experimental**.  ID do quadro que será navegada. |  

---  

## <a name="types"></a>Tipos  

### <a name="frameid-string"></a>Cadeia de caracteres FrameId  

<a name="frameid"></a>  

Identificador de quadro exclusivo.  

&nbsp;  

---  
