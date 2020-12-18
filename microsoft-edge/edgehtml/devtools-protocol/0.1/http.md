---
description: O protocolo Microsoft Edge DevTools versão 0,1 dá suporte aos seguintes pontos de extremidade HTTP.
title: DevTools Protocol versão 0,1 de pontos de extremidade HTTP (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5fe50122728304de137efdfb25ebed7274c55cee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231318"
---
# DevTools Protocol versão 0,1 de pontos de extremidade HTTP (EdgeHTML)  

> [!NOTE]
> O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

O **protocolo DevTools 0,1** dá suporte aos seguintes pontos de extremidade http. Consulte [usando o protocolo](../index.md#using-the-protocol) para saber mais sobre como se conectar a um processo de conteúdo do navegador e a documentação de [domínios](domains/index.md) para a API completa do protocolo devtools baseado na Web Socket.

## /json/version
Fornece informações sobre o navegador da máquina hospedeira e qual versão do protocolo DevTools ele suporta.

**Parâmetros**

*Nenhum(a)*

**Objeto de retorno**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## /json/protocol

Fornece toda a superfície de API de protocolo serializada como JSON.

**Parâmetros**

*Nenhum(a)*

**Objeto de retorno**

Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.

## /json/list

Fornece uma lista de candidatos de alvos de página para depuração.

**Parâmetros**

*Nenhum(a)*

**Objeto de retorno**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## /json/close

Fecha o processo de destino (por exemplo, no Microsoft Edge, fecha a guia página.)

**Parâmetros**

ID de destino 

**Objeto de retorno**

```
String("Target is closing")
```
