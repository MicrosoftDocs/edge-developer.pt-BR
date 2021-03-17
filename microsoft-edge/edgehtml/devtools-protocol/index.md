---
description: Use o Microsoft Edge DevTools Protocol para inspecionar e depurar o navegador do Microsoft Edge (EdgeHTML).
title: Microsoft Edge DevTools Protocol
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bc95f6c167479e958ffd16137176418aba872a43
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439307"
---
# <a name="microsoft-edge-edgehtml-devtools-protocol"></a>Protocolo de DevTools Microsoft Edge (EdgeHTML)

> [!NOTE]
> O Protocolo DevTools do Microsoft Edge (EdgeHTML) só funciona no [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e nas versões posteriores.

As ferramentas de desenvolvedor podem usar o **Microsoft Edge (EdgeHTML) DevTools Protocol** para inspecionar e depurar o navegador do Microsoft Edge (EdgeHTML). Ele fornece um conjunto de métodos e eventos que são organizados em diferentes [domínios](0.2/domains/index.md) de instrumentação de mecanismoHTML de Borda.

 Os clientes de ferramentas podem chamar esses métodos e monitorar esses eventos por meio de mensagens de soquete da Web JSON trocadas com o *DevTools Server* hospedado pelo Microsoft Edge (EdgeHTML) ou pelo Portal de Dispositivos do Windows. O Microsoft Edge (EdgeHTML) DevTools usa esse protocolo para habilitar a [depuração](0.2/clients.md#microsoft-edge-devtools-preview) remota de uma máquina host que executa o Microsoft Edge (EdgeHTML) do cliente Autônomo DevTools disponível na [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

O Protocolo DevTools do Microsoft Edge (EdgeHTML) foi projetado para alinhar-se de perto com o Protocolo Chrome DevTools (consulte [w3C WICG para Protocolos DevTools),](https://github.com/WICG/devtools-protocol/)embora haja lacunas de interoperabilidade conhecidas nesta versão.

## <a name="using-the-protocol"></a>Usando o protocolo

Veja como anexar um cliente de ferramentas personalizado ao DevTools Server no Microsoft Edge (EdgeHTML). Consulte as [instruções de depuração](0.2/clients.md#microsoft-edge-devtools-preview) remota se estiver usando o Microsoft Edge DevTools como seu cliente.

1. Iniciar o Microsoft Edge (EdgeHTML) com a porta de depuração remota aberta, especificando a URL que você deseja abrir. Por exemplo:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Se Edge já tiver sido lançado, o parâmetro URL será opcional. Um botão aparecerá ao lado da barra de endereços do navegador para indicar que o servidor de ferramentas **do desenvolvedor** foi iniciado:

    ![Servidor de ferramentas de desenvolvedor](media/developer-tools-server.png) 

2. Use este [ponto de extremidade HTTP](0.2/http.md) para obter uma lista de destinos de página anexados:

    ```http
    http://localhost:9222/json/list
    ```

3. Conecte-se à lista da página desejada para emitir outros comandos de protocolo e receber mensagens de evento por meio do servidor `webSocketDebuggerUrl` de soquete de devtools. [](0.2/domains/index.md)

## <a name="status-and-feedback"></a>Status e comentários

A [versão 0.2](0.2/index.md) do Protocolo DevTools fornece novos domínios para depuração de estilo e layout (somente leitura) e APIs de console, além da funcionalidade de depuração de script principal introduzida na versão [0.1](0.1/index.md). Na interface do usuário do Microsoft Edge DevTools, isso se traduz na funcionalidade disponível nos painéis [**Elementos,**](../devtools-guide/elements.md) [**Console**](../devtools-guide/console.md) e [**Depurador.**](../devtools-guide/debugger.md)

Obrigado por tentar o Protocolo Edge DevTools! Gostariamos de ouvir seus comentários em:

<!-- - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): DevTools feature ideas and requests-->  

 - [**EdgeHTML Issue Tracker**](https://developer.microsoft.com/microsoft-edge/platform/issues/): Protocol, DevTools e EdgeHTML platform bugs and issues

 - [**Hub de Comentários do Microsoft Edge DevTools**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): Problemas e sugestões de Protocolo e DevTools por meio do aplicativo Hub de Feedback

## <a name="faq"></a>Perguntas frequentes

#### <a name="can-multiple-clients-connect-to-the-same-devtools-server"></a>Vários clientes podem se conectar ao mesmo Servidor DevTools?
Não, não simultaneamente quando os clientes estão depurando. O último cliente a se conectar dará início ao anterior. No futuro, quando há suporte para ferramentas adicionais, elas provavelmente darão suporte a conexões simultâneas de cliente.

#### <a name="do-i-have-to-use-9222-as-the-devtools-server-port"></a>Preciso usar o 9222 como porta do DevTools Server?
Não. Você pode especificar qualquer porta, embora não se esqueça de escolher uma que ainda não está em uso. A porta 9222 para depuração remota é usada por convenção.

#### <a name="how-do-i-connect-my-custom-tooling-client-to-microsoft-edge-edgehtml-running-the-devtools-server"></a>Como conectar meu cliente de ferramentas personalizado ao Microsoft Edge (EdgeHTML) executando o Servidor DevTools?
Consulte [*Usando as instruções de*](#using-the-protocol) protocolo acima para anexar ao Microsoft Edge (EdgeHTML) em execução no computador local. Se você estiver procurando dar suporte à depuração remota, precisará criar um fluxo de trabalho de usuário para instalar o certificado SSL do computador host no cliente, por exemplo, com uma caixa de diálogo de instalação como o [Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) usa.

#### <a name="if-im-remote-debugging-using-edge-devtools-do-i-need-to-start-the-host-browser-process-with---devtools-server-port-cmd-line-switch"></a>Se estou depurando remotamente usando o Edge DevTools, preciso iniciar o processo do navegador host com a opção de linha cmd *--devtools-server-port?* 
Não. Se você estiver configurando a depuração remota usando [o Microsoft Edge DevTools Preview,](./0.2/clients.md#microsoft-edge-devtools-preview)a opção de linha de comando não `--devtools-server-port` será necessária para iniciar o Edge. Nesse caso, o Windows *Device Portal* está hospedando o DevTools Server em nome do navegador.

#### <a name="can-i-use-the-edge-devtools-protocol-to-remotely-debug-a-wwahostexe-or-webview-process"></a>Posso usar o Protocolo DevTools de Borda para depurar remotamente um processo WWAHost.exe webview?
O Protocolo Edge DevTools atualmente oferece suporte apenas a guias do navegador. WWAHost.exe e processos webview não são suportados.
