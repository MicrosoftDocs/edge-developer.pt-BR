---
description: Esta página fornece uma visão geral do que há de novo no EdgeHTML 13.
title: Novos recursos e APIs no EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 033b8dacb107492624f3b8c7775a47285c9893dd
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941914"
---
# Novidades do EdgeHTML 13  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Aqui estão as alterações fornecidas com o EdgeHTML 13, o mecanismo que liga o navegador Microsoft Edge na [primeira atualização importante](https://blogs.windows.com/windowsexperience/2015/11/12) para Windows 10 \ (11/2015, Build 10586 \).  Para obter uma visão geral das alterações no navegador geral do Microsoft Edge, consulte [apresentando EdgeHTML 13, nossa primeira atualização de plataforma para o Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).  

Aqui está o link permanente para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .  

## Recursos  

### CSS  

O EdgeHTML 13 oferece suporte a novos recursos CSS, incluindo:  

*   [Pseudo-classes de imutabilidade CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [Pseudo-classes de faixa CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   Palavras-chave CSS [iniciais](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) e de [subdefinição](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue)  

### Extensões de mídia criptografadas  

O Microsoft Edge agora oferece suporte às novas APIs de [extensões de mídia criptografadas sem](https://w3.org/TR/encrypted-media) prefixo.  Extensões de mídia criptografadas \ (EME \) estende os elementos de vídeo e áudio para habilitar o conteúdo protegido do gerenciamento de direitos digitais \ (DRM \) sem usar plug-ins.  Leia mais sobre o EME:  [extensões de mídia criptografadas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).  

### Elementos gráficos  

EdgeHTML 13 introduz as seguintes atualizações de gráficos:  

*   [Elipse da tela](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [Modos de mesclagem de tela](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> sub-elemento](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [Conteúdo externo SVG](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### JavaScript  

O EdgeHTML 13 inclui [grandes melhorias e suporte a novos recursos no Chakra](https://blogs.windows.com/msedgedev/2015/09/30), o mecanismo JavaScript que o Microsoft Edge desliga, incluindo:  

#### Novos recursos  

Ativado por padrão  

*   [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) habilitada por padrão \ ([postagem de blog](https://blogs.windows.com/msedgedev/2015/11/10), [demonstração](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)  
*   [Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \ (ES2015 \)  

#### Recursos de JavaScript experimental  

Habilitado com `about:flags`  

*   [Funções assíncronas](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \ (ES2016 \)  
*   [Operador de exponenciação](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \ (ES2016 \)  
*   [Deestruturando](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \ (ES2015 \)  

### Entrada do usuário  

Os seguintes recursos introduzidos no EdgeHTML 13 aprimoram a entrada do usuário:  

*   [<meter> sub-elemento](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [manipulador de eventos oninvalid para o elemento e a janela do documento](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### Bloqueio de ponteiro  

O Microsoft Edge agora dá suporte à API de bloqueio de ponteiro \ (anteriormente chamada de bloqueio do mouse \) para acessar o movimento bruto do mouse, bloqueando o destino de eventos do mouse para um único elemento, eliminando os limites de quão longe o movimento do mouse pode ir em uma única direção e removendo o cursor do modo de exibição.  

## Novas APIs no EdgeHTML 13  

Aqui está a lista completa de APIs novas em EdgeHTML 13.  Elas são listadas no formato de `[interface name].[api name]` .  

<iframe height='584' scrolling='no' title='Novas APIs no EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'>Veja a caneta <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> New APIs no EdgeHTML 13 </a> ao Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='http://codepen.io'> CodePen </a> .</iframe>  
