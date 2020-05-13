---
description: Conheça as ferramentas de desenvolvedor do Microsoft Edge
title: Ferramentas de desenvolvedor do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 47b7a3f4f523170f4dfb6f3ef674cecfdc0e157c
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645326"
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

Continue enviando seus [comentários e solicitações de recursos](#feedback)!

> [!TIP]
> **[Teste no Microsoft Edge gratuitamente em qualquer navegador](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: fizemos parcerias com o [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) para oferecer testes ativos e automáticos do Microsoft Edge.

## Aplicativo da Microsoft Store

O **Microsoft Edge devtools** [agora está disponível para visualização](./devtools-guide/whats-new.md) como um [aplicativo autônomo do Windows 10 da Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), além da experiência com ferramentas no navegador ( `F12` ). Com a versão da loja vem um painel do *seletor* para anexar a abertura de destinos de página locais e remotos e um layout com guias para facilitar a alternância entre instâncias de devtools.

### Depuração local

Para depurar uma página localmente, basta iniciar o aplicativo *Microsoft Edge devtools* . O painel **local** do seletor exibirá todos os processos de conteúdo ativos do EdgeHTML, incluindo guias do navegador Edge aberto, executando [PWAs](./progressive-web-apps-edgehtml/index.md) (processos*WWAHost. exe* ) e controles [WebView](./webview.md) . Clique no destino desejado para anexar e abrir uma nova instância de guia do DevTools.

![Painel local do aplicativo DevTools](./devtools-guide/media/chooser_local.png)

### Depuração remota

O aplicativo *Microsoft Edge devtools* introduz suporte básico para depurar páginas em um computador remoto por meio do [**protocolo devtools**](./devtools-protocol/index.md)recém-lançado. Com este lançamento vem o acesso remoto à funtionality central no painel [**depurador**](./devtools-guide/debugger.md) , subtração inspeção de cache (para armazenamento na Web, trabalho de serviço, API de cache e IndexedDB). A depuração remota está limitada ao *Microsoft Edge* executando hosts de *área de trabalho* , com suporte para outros hosts do EdgeHTML e dispositivos Windows 10 em lançamentos futuros.

Para começar, confira a seção [*devtools do Microsoft Edge*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) dos documentos de [protocolo do devtools](./devtools-protocol/index.md) .

![Painel remoto do aplicativo DevTools](./devtools-guide/media/chooser_remote.png)

## Privacidade Jurídica

Envie-nos seus comentários para que possamos continuar melhorando o Microsoft Edge DevTools para você. Basta abrir as ferramentas ( `F12` ) e clicar no botão [**enviar comentários**](#microsoft-edge-developer-tools) .

Você também pode adicionar e fazer uma votação de solicitações de ferramentas de votação ao nosso [Fórum do UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/84475-f12-developer-tools) e se tornar um [Windows Insider](https://insider.windows.com/) para visualizar os [recursos mais recentes que chegam à devtools](./devtools-guide/whats-new.md). Use o aplicativo **Hub de feedback** do Windows para postar, votar, acompanhar e obter suporte para sugestões gerais do Windows e problemas.

## Atalhos gerais

Esses atalhos controlam a janela principal do DevTools e/ou funcionam em todas as ferramentas.

Ação | Atalho
:------------ | :-------------
Mostrar/ocultar DevTools (abre para o último painel exibido) | F12, Ctrl + Shift + I
Ativar/desativar encaixe (desencaixar/abaixo/à direita) | Ctrl + Shift + D 
Mostrar código-fonte HTML não editável no depurador | CTRL + U
Mostrar/ocultar console na parte inferior de qualquer outra ferramenta  | CTRL +**`**
Alternar para elementos (explorador do DOM) | Ctrl + 1
Alternar para o console |  Ctrl + 2
Alternar para o depurador | CTRL + 3
Alternar para a rede | CTRL + 4
Alternar para o desempenho | CTRL + 5
Alternar para memória | CTRL + 6
Alternar para emulação | CTRL + 7
Documento de ajuda | F1
Próxima ferramenta | Ctrl + F6
Ferramenta anterior | Ctrl + Shift + F6
Ferramenta anterior (do histórico) | Ctrl + Shift + [
Próxima ferramenta (do histórico) | Ctrl + Shift +]
Subquadro seguinte    | F6
Subquadro anterior | Shift + F6
Próxima correspondência na caixa de pesquisa | F3
Correspondência anterior na caixa de pesquisa | Shift + F3
Localizar na caixa de pesquisa | Ctrl+F
Coloque o foco no console na parte inferior | Alt + Shift + I
Ferramentas de encaixe/desencaixe (ativar/desativar encaixe) | Ctrl+P  
Iniciar o DevTools para o console | Ctrl + Shift + J
Atualize a página. **Observação:** se você estiver Depurando e pausado em um ponto de interrupção, isso retomará a execução primeiro. | Ctrl + Shift + F5 ou CTRL + R
