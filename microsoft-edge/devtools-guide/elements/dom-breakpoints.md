---
description: Usar pontos de interrupção DOM para depurar visualmente falhas de layout na página
title: DevTools-elementos-pontos de interrupção DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, elementos, pontos de interrupção dom, mutação do dom
ms.custom: seodec18
ms.openlocfilehash: 4e9eab4727cf1c3ef74b69495dd972838985e589
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562213"
---
# Pontos de interrupção DOM

Gerencie seus pontos de interrupção de mutação DOM deste painel, incluindo desabilitar, excluí-los e revinculá-los.

Você pode usar pontos de interrupção de mutação DOM para invadir o depurador sempre que um nó de elemento selecionado é alterado. Isso é útil para acompanhar o código responsável por causar problemas visuais com a sua interface do usuário sem precisar definir pontos de interrupção individuais em cada uma das APIs DOM de 450 + no *EdgeHTML* que podem disparar tais alterações. 

Para definir um ponto de interrupção DOM, clique com o botão direito do mouse em qualquer elemento no *modo de exibição de árvore HTML* do painel **elementos** para abrir o menu de contexto.

![Menu de contexto de pontos de interrupção DOM](../media/elements_dom_breakpoints_contextmenu.png)

Você pode definir qualquer um dos seguintes pontos de interrupção:

 - **Quebra no nó removido**: pausa no depurador quando o elemento selecionado é removido do documento (árvore DOM).

 - **Interrupção na subárvore modificada**: quebra no depurador quando qualquer um dos descendentes do elemento selecionado é alterado (adicionado, removido ou suas subárvores são modificadas). Isso não será interrompido quando atributos forem modificados (consulte a próxima opção para isso).

 - **Interrupção no atributo modificado**: quebra no depurador quando um atributo do elemento selecionado é adicionado, removido ou alterado em value.

O painel **pontos de interrupção dom** listará o elemento selecionado (gerando um seletor que descreve sua localização no dom) e os tipos de pontos de interrupção que você definiu (*nó removido, subárvore modificada, atributo modificado*). Aqui, você também pode *reassociar*, *desabilitar*ou *excluir* seus pontos de interrupção, individualmente (a partir do menu de contexto de clique de RT) ou todos ao mesmo tempo (usando os botões).

![Painel pontos de interrupção DOM](../media/elements_dom_breakpoints.png)

## Persistência de ponto de interrupção

Os pontos de interrupção são armazenados (e definidos como escopo para a URL da página em que estão definidos) como parte de suas configurações do DevTools. Quando a página for recarregada ou as ferramentas forem fechadas e reabertas, o DevTools tentará reassociar seus pontos de interrupção aos elementos associados.

Os pontos de interrupção que não puderam ser revinculados automaticamente são indicados com um ícone de aviso no círculo do ponto de interrupção. Para isso, você pode esperar para reassociar o elemento manualmente (usando o botão de **ponto de interrupção de reassociação** e/ou a opção de menu de contexto) quando um elemento correspondente aparecer no dom (e o ícone de ponto de interrupção não mostrar mais o indicador de aviso) ou **excluir** o ponto de interrupção completamente.

![Indicador de ponto de interrupção não associado](../media/elements_dom_breakpoint_unbound.png)

Além desse painel de *pontos de interrupção dom* , você também pode gerenciar seus [pontos de interrupção dom](../debugger.md#dom-breakpoints) no **depurador**.

## Limitações atuais

Lembre-se das seguintes limitações da depuração de ponto de interrupção DOM no Edge DevTools:

- O Edge DevTools não dá suporte no momento a reassociação de pontos de interrupção dentro de [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe). Se você definir um ponto de interrupção em um iframe e fechar o DevTools de borda ou atualizar a página, o ponto de interrupção será perdido.

- Se o seu script encontrar um ponto de interrupção de execução síncrona antes da conclusão do DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) , você não poderá definir um ponto de interrupção dom enquanto o depurador estiver pausado. Geralmente, você pode corrigir essa situação definindo os [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) atributos de script ou.

- Para scripts síncronos, disparamos a reassociação automática de pontos de interrupção quando o [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) evento é chamado. Nesse caso, podemos perder pontos de interrupção de associação que podem disparar durante a compilação inicial orientada por script do DOM. Para scripts assíncronos, disparamos uma tentativa de reassociar antes do primeiro script ser executado, portanto, os pontos de interrupção podem reassociar e disparar conforme desejado.
