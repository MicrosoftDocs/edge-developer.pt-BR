---
description: Se você estiver digitando as mesmas expressões JavaScript no console repetidamente, experimente expressões dinâmicas em vez disso.
title: Assista aos valores de expressão JavaScript no Real-Time com expressões ao vivo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f6787455863f738d0fa4e014ca8fc318ad83a9cb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125227"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Assista aos valores de expressão JavaScript no Real-Time com expressões ao vivo  

Se você mesmo digitar a mesma expressão de JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.  Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.  O valor da expressão é atualizado em tempo real quase em tempo real.  

## Criar uma expressão ao vivo  

1.  [Abra o console][DevToolsConsoleReferenceOpenConsole].  
1.  Escolha **criar expressão ao vivo** \ ( ![ criar expressão ao vivo ][ImageCreateLiveExpressionIcon] \).  A caixa de texto **expressão ao vivo** é exibida.  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Digitando documento. ActiveElement na caixa de texto expressão dinâmica" lightbox="../media/console-create-live-expression.msft.png":::
       Digitando `document.activeElement` na caixa de texto **expressão dinâmica**  
    :::image-end:::  
    
1.  Selecione `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \) para salvar a expressão ou escolha fora da caixa de texto de **expressão ao vivo** .  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Abrir o console-referência do console | Documentos da Microsoft"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
