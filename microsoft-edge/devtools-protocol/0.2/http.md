---
description: O protocolo Microsoft Edge DevTools versão 0,2 dá suporte aos seguintes pontos de extremidade HTTP.
title: Pontos de extremidade HTTP do Microsoft Edge DevTools Protocol versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: cc3d0156d92ab479168e0b588ae2b7c9faa7e58f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561322"
---
# Pontos de extremidade HTTP do protocolo DevTools

> [!NOTE]
> A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10]() e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

O **protocolo DevTools 0,2** dá suporte aos seguintes pontos de extremidade http. Consulte [usando o protocolo](../index.md#using-the-protocol) para saber mais sobre como se conectar a um processo de conteúdo do navegador e a documentação de [domínios](domains/index.md) para a API completa do protocolo devtools baseado na Web Socket.

## /json/version
Fornece informações sobre o navegador da máquina hospedeira e qual versão do protocolo DevTools ele suporta.

**Parâmetros**

*Nenhum(a)*

**Objeto de retorno**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
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
