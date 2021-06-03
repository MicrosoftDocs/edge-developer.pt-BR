---
description: Atualizar para o protocolo Microsoft Edge DevTools
title: Microsoft Edge Atualização do Protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: de7d6c39c09ba321f21b34e6e461ec030f09f6ad
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480157"
---
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a>Microsoft Edge (Chromium) Visão geral do Protocolo DevTools  

Com a mudança na plataforma Web subjacente de Microsoft Edge para Chromium, o Protocolo [Microsoft Edge (EdgeHTML) DevTools não](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) receberá mais atualizações.  O Microsoft Edge \(Chromium\) Protocolo DevTools corresponderá às APIs do Protocolo Chrome DevTools em frente.  

Você pode encontrar documentação sobre esses domínios e métodos referindo-se ao Visualizador de Protocolo [Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot).  

> [!NOTE]
> Todos os métodos que foram prefixados no protocolo `ms` [Microsoft Edge (EdgeHTML) DevTools](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) não são mais suportados no protocolo Microsoft Edge \(Chromium\) DevTools Protocol.  

## <a name="using-the-devtools-protocol"></a>Usando o Protocolo DevTools  

Veja como anexar um cliente de ferramentas personalizado ao Servidor DevTools em Microsoft Edge \(Chromium\).  

1.  Verifique se todas as instâncias de Microsoft Edge \(Chromium\) estão fechadas.  
1.  Iniciar Microsoft Edge \(Chromium\) com a porta de depuração remota:. 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  Opcionalmente, você pode iniciar uma instância separada do Edge usando um perfil de usuário distinto, se desejado.  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  Em seguida, use o ponto de extremidade HTTP `list` para obter uma lista de destinos de página anexados.  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  Por fim, conecte-se ao dos comandos de destino e de emissão desejados/inscreva-se nas mensagens de evento por meio do servidor `webSocketDebuggerUrl` de soquete web DevTools.  

## <a name="devtools-protocol-http-endpoints"></a>Pontos de extremidade HTTP do Protocolo DevTools  

O Microsoft Edge \(Chromium\) Protocolo DevTools oferece suporte aos seguintes pontos de extremidade HTTP.  

## <a name="jsonversion"></a>/json/version  

Fornece informações sobre o navegador do computador host e qual versão do Protocolo DevTools suporta.  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

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

## <a name="jsonprotocol"></a>/json/protocol  

Fornece toda a superfície da API de protocolo serializada como JSON.  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

Objeto JSON que representa a superfície da API disponível para a versão atual do protocolo.  

## <a name="jsonlist"></a>/json/list  

Fornece uma lista de candidatos de destinos de página para depuração.  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

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

## <a name="jsonclose"></a>/json/close  

Fecha o processo de destino \(por exemplo, em Microsoft Edge \(Chromium\), fecha a guia página\).  

**Parâmetros**  

ID de destino  

**Objeto Return**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a>Ferramentas remotas para Microsoft Edge (Beta)  

Agora você pode instalar as Ferramentas Remotas para [Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) do [Microsoft Store](https://www.microsoft.com/store/apps/windows).  Este aplicativo permite que você depure remotamente Microsoft Edge (Chromium) em execução em um dispositivo Windows 10 de seu computador de desenvolvimento.  

Para saber como configurar seu dispositivo Windows 10 e se conectar a ele a partir de sua máquina de desenvolvimento, navegue até Introdução com a [Depuração Remota Windows 10 Dispositivos](../devtools-guide-chromium/remote-debugging/windows.md).  

As Ferramentas Remotas para [Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usam o mesmo protocolo Microsoft Edge (Chromium) DevTools que o [DevTools](../devtools-guide-chromium/index.md) para se comunicar com Microsoft Edge em execução no dispositivo Windows 10 que você deseja depurar.  Este aplicativo apenas se prepara e `/msedge/` uma ID do processo ( `pid` ) antes de cada chamada para o protocolo.  Ele dá suporte aos seguintes pontos de extremidade HTTP.  

### <a name="msedgejsonlist"></a>/msedge/json/list  

Fornece uma lista de candidatos de todos os processos `msedge.exe` \(incluindo [PWAs](../progressive-web-apps-chromium/index.md) e todas as guias em todas as instâncias de Microsoft Edge\) no dispositivo Windows 10 para depuração.  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

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

### <a name="msedge"></a>/msedge/  

Funcionalmente equivalente a [/msedge/json/list](#msedgejsonlist).  

### <a name="msedgepidjsonlist"></a>/msedge/[pid]/json/list  

Fornece uma lista de candidatos de destinos de página para a instância Microsoft Edge que corresponde à `[pid]` fornecida para depuração.  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

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

### <a name="msedgepidjsonversion"></a>/msedge/[pid]/json/version  

Fornece informações sobre a instância Microsoft Edge que corresponde à fornecida e qual versão do `[pid]` Protocolo DevTools ele oferece suporte.  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

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

### <a name="msedgepidjsonprotocol"></a>/msedge/[pid]/json/protocol/  

Fornece toda a superfície da API de protocolo serializada como JSON para a instância Microsoft Edge que corresponde à `[pid]` fornecida .  

**Parâmetros**  

**Nenhum**  

**Objeto Return**  

Objeto JSON que representa a superfície da API disponível para a versão do protocolo que a instância Microsoft Edge que corresponde à `[pid]` fornecida está usando.  
