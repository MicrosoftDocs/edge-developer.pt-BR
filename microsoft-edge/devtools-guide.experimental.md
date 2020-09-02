---
description: Conheça as ferramentas de desenvolvedor do Microsoft Edge
title: Ferramentas de desenvolvedor do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 3aee2ab67c6e703a0a31b58b5bf985a23fcbb481
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986217"
---
# Ferramentas de desenvolvedor do Microsoft Edge  

> [!NOTE]
> O Microsoft Edge DevTools ajuda desenvolvedores da Web a criar e testar sites.  Se você abrisse o DevTools acidentalmente, basta pressionar `F12` para fechar.  

O Microsoft Edge DevTools são criados com o [TypeScript](https://www.typescriptlang.org/), com [fonte aberta](https://github.com/Microsoft/ChakraCore), otimizado para fluxos de trabalho de front-end modernos e agora disponível como um [aplicativo autônomo do Windows 10](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) na Microsoft Store!

Para saber mais sobre os recursos mais recentes, confira [*devtools na atualização mais recente do Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Ferramentas principais

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

O Microsoft Edge DevTools inclui:

 - Um painel de [**elementos**](./devtools-guide/elements.md) para editar HTML e CSS, inspecionar Propriedades de acessibilidade, exibir ouvintes de eventos e definir pontos de interrupção de MUTAção dom
 - Um [**console**](./devtools-guide/console.md) para exibir e filtrar mensagens de log, inspecionar objetos JavaScript e nós dom e executar JavaScript no contexto da janela ou do quadro selecionado
 - Um [**depurador**](./devtools-guide/debugger.md) para depurar o código, definir inspeções e pontos de interrupção, editar seu código e inspecionar o armazenamento da Web e os caches de cookies
 - Um painel de [**rede**](./devtools-guide/network.md) para monitorar e inspecionar solicitações e respostas da rede e do cache do navegador 
 - Um painel de [**desempenho**](./devtools-guide/performance.md) para criar o perfil do tempo e dos recursos do sistema necessários para seu site
 - Um painel de [**memória**](./devtools-guide/memory.md) para medir o uso dos recursos de memória e comparar os instantâneos de heap em diferentes Estados de execução de código
 - Um painel de [**emulação**](./devtools-guide/emulation.md) para testar seu site com diferentes perfis de navegador, resoluções de tela e coordenadas de localização de GPS

Continue enviando seus [comentários e solicitações de recursos](#getting-in-touch-with-the-microsoft-edge-devtools-team).

> [!TIP]
> **[Teste no Microsoft Edge gratuitamente em qualquer navegador](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: fizemos parcerias com o [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) para oferecer testes ativos e automáticos do Microsoft Edge.

## Aplicativo da Microsoft Store

O **Microsoft Edge devtools** [agora está disponível para visualização](./devtools-guide/whats-new.md) como um [aplicativo autônomo do Windows 10 da Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), além da experiência com ferramentas no navegador ( `F12` ). Com a versão da loja, há um painel de *seletor* para anexar a abrir destinos de página locais e remotos e um layout com guias para alternar entre instâncias das DevTools.

### Depuração local

Para depurar uma página localmente, basta iniciar o aplicativo *Microsoft Edge devtools* . O painel **local** do seletor exibirá todos os processos de conteúdo ativos do EdgeHTML, incluindo guias do navegador Edge aberto, execução de [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* processos) e controles [WebView](./webview.md) . Clique no destino desejado para anexar e abrir uma nova instância de guia do DevTools.

![Painel local do aplicativo DevTools](./devtools-guide/media/chooser_local.png)

### Depuração remota

O aplicativo *Microsoft Edge devtools* introduz suporte básico para depurar páginas em um computador remoto por meio do [**protocolo devtools**](./devtools-protocol/index.md)recém-lançado. Com este lançamento vem o acesso remoto à funtionality central no painel [**depurador**](./devtools-guide/debugger.md) , subtração inspeção de cache (para armazenamento na Web, trabalho de serviço, API de cache e IndexedDB). A depuração remota está limitada ao *Microsoft Edge* executando hosts de *área de trabalho* , com suporte para outros hosts do EdgeHTML e dispositivos Windows 10 em lançamentos futuros.

Para começar, confira a seção de documentos [Protocolo DevTools](./devtools-protocol/index.md)do[*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview).

![Painel remoto do aplicativo DevTools](./devtools-guide/media/chooser_remote.png)

## Atalhos gerais

Esses atalhos controlam a janela principal do DevTools e/ou funcionam em todas as ferramentas.

Ação | Atalho
:------------ | :-------------
Mostrar/ocultar DevTools (abre para o último painel exibido) | F12, Ctrl + Shift + I
Ativar/desativar encaixe (desencaixar/abaixo/à direita) | Ctrl + Shift + D 
Mostrar código-fonte HTML não editável no depurador | CTRL + U
Mostrar/ocultar Console na parte inferior de qualquer outra ferramenta  | CTRL +**`**
Alternar para elementos (explorador do DOM) | Ctrl + 1
Alternar para Console |  Ctrl + 2
Alternar para Depurador | CTRL + 3
Alternar para Rede | CTRL + 4
Alternar para Desempenho | CTRL + 5
Alternar para Memória | CTRL + 6
Alternar para Emulação | CTRL + 7
Documento de Ajuda | F1
Próxima ferramenta | Ctrl + F6
Guia anterior | Ctrl + Shift + F6
Ferramenta anterior (do histórico) | Ctrl + Shift + [
Próxima ferramenta (do histórico) | Ctrl + Shift +]
Próximo subquadro    | F6
Subquadro anterior | Shift + F6
Próxima correspondência na caixa de pesquisa | F3
Correspondência anterior na caixa de pesquisa | Shift + F3
Procurar na caixa de pesquisa | Ctrl+F
Focalizar o console na parte inferior | Alt + Shift + I
Ferramentas de encaixe/desencaixe (ativar/desativar encaixe) | Ctrl+P  
Iniciar o DevTools para o Console | Ctrl + Shift + J
Atualize a página. **Observação:** se você estiver Depurando e pausado em um ponto de interrupção, isso retomará a execução primeiro. | Ctrl + Shift + F5 ou CTRL + R

## Entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  
