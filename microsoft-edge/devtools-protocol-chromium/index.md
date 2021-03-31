---
description: Atualizar para o protocolo Microsoft Edge DevTools
title: Atualização do protocolo Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 15b13e2b93d1dbd013a82ea52b643071fa5b6f7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231728"
---
# Visão geral do protocolo DevTools Microsoft Edge (Chromium)  

Com o turno na plataforma da Web subjacente do Microsoft Edge com o Chromium, o [protocolo de devtools do Microsoft Edge (EdgeHTML)](../edgehtml/devtools-protocol/index.md) não receberá mais atualizações.  O protocolo DevTools do Microsoft Edge \(Chromium \) corresponderá às APIs do protocolo Chrome DevTools em andamento.  

Você pode encontrar documentação sobre esses domínios e métodos fazendo referência ao Visualizador de [protocolo do Chrome devtools](https://chromedevtools.github.io/devtools-protocol/tot/).  

> [!NOTE]
> Qualquer método que tenha sido prefixado `ms` no [protocolo devtools Microsoft Edge (EdgeHTML)](../edgehtml/devtools-protocol/index.md) não tem mais suporte no protocolo devtools do Microsoft Edge \(Chromium \).  

## Usar o protocolo DevTools  

Veja como anexar um cliente de ferramentas personalizado ao servidor DevTools no Microsoft Edge \(Chromium \).  

1.  Verifique se todas as instâncias do Microsoft Edge \(Chromium \) estão fechadas.  
1.  Inicie o Microsoft Edge \(Chromium \) com a porta de depuração remota:. 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  Opcionalmente, você pode iniciar uma instância separada do Edge usando um perfil de usuário distinto, se desejado.  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  Em seguida, use o `list` ponto de extremidade http para obter uma lista de destinos de página anexáveis.  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  Por fim, conecte-se aos `webSocketDebuggerUrl` comandos de destino e problema desejados/assine mensagens de evento por meio do devtools Web Socket Server.  

## Pontos de extremidade HTTP do protocolo DevTools  

O protocolo DevTools do Microsoft Edge \(Chromium \) dá suporte aos seguintes pontos de extremidade HTTP.  

## /json/version  

Fornece informações sobre o navegador do computador host e qual versão do protocolo DevTools ele suporta.  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```  

## /json/protocol  

Fornece toda a superfície de API de protocolo serializada como JSON.  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.  

## /json/list  

Fornece uma lista de candidatos de alvos de página para depuração.  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## /json/close  

Fecha o processo de destino \(por exemplo, no Microsoft Edge \(Chromium \), fecha a guia da página \).  

**Parâmetros**  

ID de destino  

**Objeto de retorno**  

```
String(“Target is closing”)
```  

## Ferramentas remotas para Microsoft Edge (beta)  

Agora você pode instalar as [ferramentas remotas para o Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) da [Microsoft Store](https://www.microsoft.com/store/apps/windows).  Este aplicativo permite que você depure remotamente o Microsoft Edge (Chromium) em execução em um dispositivo com Windows 10 da sua máquina de desenvolvimento.  

Para saber como configurar seu dispositivo Windows 10 e conectar-se a ele a partir de seu computador de desenvolvimento, navegue até [introdução à depuração remota de dispositivos Windows 10](../devtools-guide-chromium/remote-debugging/windows.md).  

As [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usam o mesmo protocolo devtools Microsoft Edge (Chromium) que o [devtools](../devtools-guide-chromium/index.md) para se comunicar com o Microsoft Edge em execução no dispositivo Windows 10 que você deseja depurar.  Esse aplicativo apenas precede `/msedge/` e uma ID de processo ( `pid` ) antes de cada chamada para o protocolo.  Ele é compatível com os seguintes pontos de extremidade HTTP.  

### /msedge/json/list  

Fornece uma lista de candidatos de todos os `msedge.exe` processos \(incluindo [PWAs](../progressive-web-apps-chromium/index.md) e todas as guias em todas as instâncias do Microsoft Edge \) no dispositivo Windows 10 para depuração.  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, ...  ]
```  

### /msedge/  

Funcionalmente equivalente a [/msedge/JSON/List](#msedgejsonlist).  

### /msedge/[pid]/JSON/List  

Fornece uma lista de candidatos de destinos de página para a instância do Microsoft Edge que corresponde à fornecida `[pid]` para depuração.  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, ...  ]
```  

### /msedge/[pid]/JSON/Version  

Fornece informações sobre a instância do Microsoft Edge que corresponde ao fornecido `[pid]` e à versão do protocolo devtools que ele suporta.  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```  

### /msedge/[pid]/JSON/Protocol/  

Fornece a superfície de API de protocolo inteira serializada como JSON para a instância do Microsoft Edge que corresponde ao fornecido `[pid]` .  

**Parâmetros**  

**Nenhum(a)**  

**Objeto de retorno**  

Objeto JSON que representa a superfície de API disponível para a versão do protocolo que a instância do Microsoft Edge correspondente à fornecida `[pid]` está usando.  
