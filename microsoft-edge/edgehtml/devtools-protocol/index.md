---
description: Use o protocolo DevTools do Microsoft Edge para inspecionar e depurar o navegador Microsoft Edge (EdgeHTML).
title: Protocolo DevTools Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2ba81e51d3f9abd2aa2011993532566885ce553f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231680"
---
# Protocolo de DevTools Microsoft Edge (EdgeHTML)

> [!NOTE]
> O protocolo DevTools do Microsoft Edge (EdgeHTML) funciona apenas em versões de [abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões posteriores.

Ferramentas de desenvolvedor podem usar o **protocolo de devtools Microsoft Edge (EdgeHTML)** para inspecionar e depurar o navegador Microsoft Edge (EdgeHTML). Ele fornece um conjunto de métodos e eventos organizados em diferentes [domínios](0.2/domains/index.md) de instrumentação do mecanismo EdgeHTML.

 Os clientes de ferramentas podem chamar esses métodos e monitorar esses eventos por meio de mensagens JSON Web Socket trocadas com o *servidor devtools* hospedado pelo Microsoft Edge (EdgeHTML) ou pelo Windows Device Portal. O Microsoft Edge (EdgeHTML) DevTools usa esse protocolo para habilitar a [depuração remota](0.2/clients.md#microsoft-edge-devtools-preview) de um computador host executando o Microsoft Edge (EdgeHTML) a partir do cliente de devtools autônomo disponível na [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

O protocolo do DevTools Microsoft Edge (EdgeHTML) foi projetado para se alinhar ao máximo com o protocolo Chrome DevTools (consulte o [W3C WICG para protocolos devtools](https://github.com/WICG/devtools-protocol/)), mas há lacunas de interoperabilidade conhecidos nesta versão.

## Usando o protocolo

Veja como anexar um cliente de ferramentas personalizado ao servidor DevTools no Microsoft Edge (EdgeHTML). Veja as instruções de [depuração remota](0.2/clients.md#microsoft-edge-devtools-preview) se você estiver usando o Microsoft Edge devtools como seu cliente.

1. Inicie o Microsoft Edge (EdgeHTML) com a porta de depuração remota aberta, especificando a URL que você deseja abrir. Por exemplo:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Se a borda já estiver iniciada, o parâmetro de URL é opcional. Um botão será exibido ao lado da barra de endereços do navegador para indicar que o **servidor de ferramentas de desenvolvedor** começou:

    ![Servidor de ferramentas de desenvolvedor](media/developer-tools-server.png) 

2. Use este [ponto de extremidade http](0.2/http.md) para obter uma lista de destinos de página anexáveis:

    ```http
    http://localhost:9222/json/list
    ```

3. Conecte-se à lista `webSocketDebuggerUrl` de páginas desejada para executar [comandos de protocolo](0.2/domains/index.md) adicionais e receber mensagens de evento por meio do servidor de soquete devtools.

## Status e comentários

A [versão 0,2](0.2/index.md) do protocolo devtools fornece novos domínios para a depuração de estilo e o layout (somente leitura) e APIs de console, além da funcionalidade de depuração de script principal introduzida na [versão 0,1](0.1/index.md). Na interface do usuário do Microsoft Edge DevTools, isso se traduz em funcionalidades disponíveis nos painéis de [**elementos**](../devtools-guide/elements.md), [**console**](../devtools-guide/console.md) e [**depurador**](../devtools-guide/debugger.md) .

Obrigado por experimentar o protocolo Edge DevTools! Adoraríamos saber seus comentários em:

 - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): devtools ideias de recursos e solicitações

 - [**Controlador de problemas do EdgeHTML**](https://developer.microsoft.com/microsoft-edge/platform/issues/): erros e problemas na plataforma de protocolo, devtools e EdgeHTML

 - [**Hub de feedback do Microsoft Edge devtools**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): problemas de protocolo e DevToolss e sugestões pelo aplicativo Hub de feedback

## Perguntas frequentes

#### Vários clientes podem conectar-se ao mesmo servidor DevTools?
Não, não simultaneamente quando os clientes estão Depurando. O último cliente a se conectar iniciará o anterior. No futuro, quando houver suporte para ferramentas adicionais, elas provavelmente serão compatíveis com conexões de cliente simultâneas.

#### Preciso usar o 9222 como a porta do servidor DevTools?
Não. Você pode especificar qualquer porta, mas certifique-se de selecionar uma que ainda não esteja em uso. A porta 9222 para depuração remota é usada pela Convenção.

#### Como faço para conectar meu cliente de ferramentas personalizado ao Microsoft Edge (EdgeHTML) que executa o DevTools Server?
Consulte [*usando as instruções de protocolo*](#using-the-protocol) acima para anexar ao Microsoft Edge (EdgeHTML) em execução no computador local. Se você estiver tentando dar suporte à depuração remota, será necessário planejar um fluxo de trabalho de usuário para instalar o certificado SSL do computador host no cliente, por exemplo, com uma caixa de diálogo de instalação conforme [o Microsoft Edge devtools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) é usado.

#### Se eu estiver usando a depuração remota usando o Edge DevTools, preciso iniciar o processo do navegador host com a opção *de linha de comando do navegador do devtools-Server-Port* ? 
Não. Se você estiver configurando a [depuração remota usando o Microsoft Edge devtools Preview](./0.2/clients.md#microsoft-edge-devtools-preview), a `--devtools-server-port` opção de linha de comando não é necessária para iniciar o Edge. Nesse caso, o Windows *Device portal* está hospedando o servidor devtools em nome do navegador.

#### Posso usar o protocolo Edge DevTools para depurar remotamente um processo de WWAHost.exe ou WebView?
No momento, o protocolo Edge DevTools oferece suporte somente a guias do navegador. Não há suporte para processos WWAHost.exe e WebView.
