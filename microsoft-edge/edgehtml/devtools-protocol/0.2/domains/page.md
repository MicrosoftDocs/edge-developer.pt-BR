---
description: Referência do Protocolo DevTools Versão 0.2 (EdgeHTML) para o Domínio da Página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Domínio da Página - DevTools Protocol Versão 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398844"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a>Domínio da Página - DevTools Protocol Versão 0.2 (EdgeHTML)  

Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.  

| Classificação | Membros |  
|:--- |:--- |  
| [Métodos](#methods) | [habilitar](#enable), [desabilitar, navegar](#navigate), [getFrameTree](#getframetree) [](#disable) |  
| [Eventos](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired,](#loadeventfired) [domContentEventFired](#domcontenteventfired) |  
| [Tipos](#types) | [FrameId,](#frameid) [Frame](#frame), [FrameTree](#frametree) |  

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
| frameId \(optional\) | [FrameId](#frameid) | ID do quadro para navegar.  Se não for especificado, navegará pela página superior. |  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID do quadro que será navegada. |  

---  

### <a name="getframetree"></a>getFrameTree  

Retorna a estrutura da árvore de quadros atual.  

| Retorna | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frameTree | [FrameTree](#frametree) | Estrutura da árvore de quadros presente. |  

---  

## <a name="events"></a>Eventos  

### <a name="frameattached"></a>frameAttached  

Acionado quando o quadro foi anexado ao pai.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID do quadro anexado. |  
| parentFrameId | [FrameId](#frameid) | Identificador de quadro pai. |  
| stack \(optional\) | [Runtime.StackTrace](./runtime.md#stacktrace) | Rastreamento de pilha JavaScript de quando o quadro foi anexado, somente definido se o quadro tiver sido iniciado a partir do script. |  

---  

### <a name="framedetached"></a>frameDetached  

Acionado quando o quadro foi desvinculado de seu pai.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frameId | [FrameId](#frameid) | ID do quadro que foi desvinculado. |  

---  

### <a name="framenavigated"></a>frameNavigated  

Acionado depois que a navegação do quadro tiver sido concluída.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frame | [Quadro](#frame) | Objeto Frame. |  

---  

### <a name="loadeventfired"></a>loadEventFired  

Corresponde ao `window.onload` evento.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| timestamp | `number` | Número de milissegundos desde a época. |  

---  

### <a name="domcontenteventfired"></a>domContentEventFired  

Corresponde ao `document.onDOMContentLoaded` evento.  

| Parâmetros | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| timestamp | `number` | Número de milissegundos desde a época. |  

---  

## <a name="types"></a>Tipos  

### <a name="frameid-string"></a>Cadeia de caracteres FrameId  

<a name="frameid"></a>  

Identificador de quadro exclusivo.  

&nbsp;  

---  

### <a name="frame-object"></a>Objeto Frame  

<a name="frame"></a>  

Informações sobre o Quadro na Página.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| id | [FrameId](#frameid) | Identificador exclusivo do quadro. |  
| parentId \(optional\) | [FrameId](#frameid) | Identificador exclusivo do quadro pai. |  
| nome \(opcional\) | `string` | O nome do quadro conforme especificado na marca. |  
| url | `string` | URL do documento do quadro. |  
| securityOrigin | `string` | Origem da segurança do documento do quadro. |  
| mimeType | `string` | MimeType do documento de quadro conforme determinado pelo navegador. |  

---  

### <a name="frametree-object"></a>Objeto FrameTree  

<a name="frametree"></a>  

Informações sobre a hierarquia frame.  

| Propriedades | Tipo | Detalhes |  
|:--- |:--- |:--- |  
| frame | [Quadro](#frame) | Informações de quadro para este item de árvore. |  
| childFrames \(optional\) | [FrameTree[]](#frametree) | Quadros filho. |  

---  
