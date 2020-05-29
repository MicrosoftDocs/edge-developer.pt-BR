---
description: Modo IE e o Microsoft Edge (Chromium) DevTools
title: Modo Internet Explorer e o DevTools
author: robpaveza
ms.author: ropaveza
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, ie11, Internet Explorer 11, modo IE
ms.openlocfilehash: 18e5f029d277e446857ec48b9cf129149f219256
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562095"
---
# Modo Internet Explorer e o DevTools

Este documento descreve como o Internet Explorer Mode (modo IE) integra-se com o DevTools Microsoft Edge (Chromium).

## Noções básicas sobre o modo IE

O modo IE é um mecanismo pelo qual as empresas podem especificar um conjunto de sites que, até agora, funcionavam apenas no Internet Explorer 11. Quando esses sites da Web são exibidos no Microsoft Edge (Chromium), uma instância completa do Internet Explorer 11 está em execução e renderizada na guia. Isso permite que as empresas gerenciem a compatibilidade de modos de documentos do IE, controles ActiveX e outros componentes herdados que atualmente não são compatíveis com qualquer navegador da Web moderno.

No modo IE, o processo de renderização é totalmente baseado no Internet Explorer 11. O processo do Gerenciador do Microsoft Edge (Chromium) gerencia o tempo de vida do processo de renderização, mas é restrito ao tempo de vida da guia em um determinado site ou aplicativo. Quando uma guia é renderizada no modo IE, um emblema é exibido na barra de endereços para a guia fornecida:

![Selo do modo do IE na barra de endereços](./media/ie-mode-badge.png)

O modo do IE está disponível atualmente no Windows 10 versão 1903 (maio de 2019), mas estará disponível em breve para todas as plataformas do Windows com suporte.

## Iniciando o DevTools em uma guia no modo IE

Se você estiver tentando exibir o modo de documento de um site no modo IE, poderá clicar no emblema na barra de endereços.

![Exibir o modo de documento via selo do modo IE](./media/ie-mode-badge-doc-mode.png)

Enquanto estiver em uma guia no modo do IE, o DevTools não irá funcionar. Pressione `F12` ou `Ctrl` + `Shift` + `I` só iniciará uma instância em branco do devtools Microsoft Edge (Chromium) com uma mensagem que diz: "as ferramentas de desenvolvedor não estão disponíveis no modo Internet Explorer. Para depurar a página, abra-a no Internet Explorer 11. " A **exibição da fonte** iniciará o bloco de notas, e o **elemento inspecionar** não ficará visível no menu de contexto no modo IE.

Isso ocorre porque vários componentes na DevTools (como as ferramentas de rede e desempenho) seriam interrompidos quando o mecanismo de renderização muda do Chromium para o Internet Explorer 11 no modo IE. Para nos enviar comentários, clique no `:)` ícone.

![DevTools iniciado no modo IE](./media/ie-mode-devtools.png)

Se você estiver desenvolvendo ou mantendo um site ou aplicativo da Web baseado no Internet Explorer 11, recomendamos navegar para a mesma página no Internet Explorer 11. No Windows 10, você pode encontrar o atalho para o Internet Explorer 11 no menu Iniciar, abaixo de acessórios do Windows. No Windows 7, você pode encontrar o Internet Explorer 11 no menu iniciar principal. Em seguida, você pode iniciar o Internet Explorer DevTools pressionando `F12` ou clicando em **inspecionar elemento** no menu de contexto. Para saber mais sobre como usar essas ferramentas, clique [aqui](/previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85)).

## Depuração remota e modo IE

Você pode iniciar o Microsoft Edge (Chromium) com a depuração remota habilitada, o que normalmente é a forma como as ferramentas como o Visual Studio ou a borda de inicialização do código VS, na linha de comando:

`start msedge --remote-debugging-port=9222`

Quando o Microsoft Edge (Chromium) é iniciado com este argumento da linha de comando, o modo do IE não estará disponível. Você ainda pode navegar para sites ou aplicativos da Web que, de outra forma, estaria no modo IE, mas o conteúdo será renderizado por meio do Chromium, não pelo Internet Explorer 11. Você pode esperar que as partes dessas páginas que dependem do IE11, como os controles ActiveX, não sejam renderizadas corretamente. O selo do modo do IE não será mais exibido na barra de endereços.

O modo do IE permanecerá indisponível até você fechar completamente o Microsoft Edge (Chromium).