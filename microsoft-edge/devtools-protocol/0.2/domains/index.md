---
description: Lista de referências para domínios com suporte no protocolo Microsoft Edge DevTools versão 0,2.
title: Domains-DevTools protocolo versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 32634df94320e6474170726dfcd6164c5d02631a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561335"
---
# Domínios de protocolo DevTools
## [CSS](css.md)
Esse domínio expõe operações CSS de leitura/gravação. Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado. Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes. Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM). Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.
## [DOM](dom.md)
Esse domínio apresenta operações DOM de leitura/gravação. Cada nó DOM é representado com seu objeto espelho que tem um `id` . Isso `id` pode ser usado para obter informações adicionais sobre o nó, solucioná-lo para o invólucro do objeto JavaScript, etc. É importante que o cliente receba eventos DOM somente para os nós conhecidos do cliente. O back-end mantém o controle dos nós que foram enviados para o cliente e nunca envia o mesmo nó duas vezes. É responsabilidade do cliente coletar informações sobre os nós que foram enviados ao cliente.<p>Observe que `iframe` os elementos Owner retornarão elementos de documento correspondentes como seus nós filho.</p>
## [DOMDebugger](domdebugger.md)
A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM. A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.
## [Depurador](debugger.md)
O domínio do depurador expõe recursos de depuração JavaScript. Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.
## [Sobreposição](overlay.md)
Domínio sobreposto expõe a interação visual adorners e seleção de nós
## [Página](page.md)
Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
## [Classpath](runtime.md)
O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos. Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.
## [Esquema](schema.md)
Fornece informações sobre o esquema de protocolo.