---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Para garantir que o ícone da extensão esteja visível enquanto estiver no modo claro e escuro, siga o guia de acessibilidade.
title: Extensões-acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 514e68fc1b797a28c76bda79c8fab88b4ea2216c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561260"
---
# Acessibilidade  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Criando ícones de extensão acessíveis para o Microsoft Edge

Os desenvolvedores de extensão de terceiros são incentivados a usar ativos de imagem que atendam aos requisitos de acessibilidade estritos da Microsoft, de forma que os ícones sejam claramente visíveis para temas claros e escuros. Recomendamos que todos os ícones de extensão tenham uma proporção de 14:1 entre a cor da tela de fundo do ícone e a cor dominante do próprio ícone.


Extensões de primeira empresa desenvolvida pela Microsoft aplicam um tratamento Visual "Stickering" para atender a esses requisitos.

### Exemplos de "Stickering"

O objetivo principal de "Stickering" é tornar o ícone visualmente acessível em qualquer cor de tela de fundo. A proporção de cores recomendável entre o traço externo branco e seu ícone deve ser 14:1 para dar suporte aos requisitos de alto contraste.

#### Ícone bom
Com o Stickering, um ícone essencialmente escuro permanecerá visível em qualquer cor de tela de fundo.


![imagem do ícone visível em qualquer cor do plano de fundo](./../media/accessibility-light-to-dark-good.png)

#### Ícone incorreto
Sem o Stickering, um ícone pode misturar-se com o segundo plano e ter impossível ver.


![imagem do ícone mesclando em tela de fundo preta](./../media/accessibility-light-to-dark-bad.png)

### "Stickering" seu ícone de extensão

As cinco etapas a seguir descrevem o método sugerido de criação de um ícone de extensão que atenda aos requisitos de acessibilidade da Microsoft:


| Etapa 1                                       | Etapa 2                                       | Etapa 3                                                                                 | Etapa 4                                                                          | Etapa 5                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| Defina o ícone na sua grade especificada.    | Reduza o tamanho do ícone em 2 pixels.           | Copie o ícone e cole no lugar. Criar um traçado externo de 2 pixels com cantos arredondados. | Descreva o seu traço, libere o caminho composto e mescle as formas restantes. | Colorir o branco de traço externo e o ícone interno como desejar. |
| ![step1](./../media/accessibility-step1.png) | ![step2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![step4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

