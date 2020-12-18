---
description: Abra a guia "renderização" e selecione "emular mídia CSS" > "imprimir".
title: Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a036e710de998f03e876126581956929d8652f1e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230919"
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

# Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)  

A [consulta imprimir mídia][MDNUsingMediaQueries] controla a aparência da sua página quando impressa.  Para forçar sua página no modo de visualização de impressão:  

1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Digite `rendering` , escolha **Mostrar renderização**e, em seguida, selecionar `Enter` .  
1.  Em **emular mídia CSS**, escolha **Imprimir**.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Modo de visualização de impressão" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Modo de visualização de impressão  
    :::image-end:::  
    
Aqui, você pode exibir e alterar seu CSS, como qualquer outra página da Web.  Navegue até [introdução ao exibir e alterar CSS][DevToolsCSSGetStarted].  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
