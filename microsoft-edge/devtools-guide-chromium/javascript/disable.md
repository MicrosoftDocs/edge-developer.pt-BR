---
description: Abrir o menu de comando e executar o comando "desabilitar JavaScript".
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: de756e04c91768c49eed50debce97ae91fdaa3bd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992796"
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

# Desabilitar JavaScript com o Microsoft Edge DevTools  

Conclua as seguintes ações para ver como uma página da Web tem a aparência e se comporta quando o JavaScript está desabilitado.  

1.  [Abra o Microsoft Edge devtools][DevToolsOpen].  
1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="O menu de comando" lightbox="../media/javascript-console-command.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
1.  Comece a digitar `javascript` , selecione **desativar JavaScript**e pressione `Enter` para executar o comando.  JavaScript agora está desabilitado.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Selecionar desativar JavaScript no menu de comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Selecionar **desativar JavaScript** no **menu de comando**  
    :::image-end:::  
    
    O ícone de aviso amarelo ao lado de **fontes** lembra que o JavaScript está desabilitado.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="O ícone de aviso ao lado de fontes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       O ícone de aviso ao lado de **fontes**  
    :::image-end:::  
    
O JavaScript permanece desabilitado na guia pelo tempo em que você tiver o DevTools aberto.  

Você pode querer recarregar a página para ver se e como a página depende de JavaScript durante o carregamento.  

Para habilitar novamente o JavaScript, conclua as ações a seguir.  

*   Abra o **menu de comandos** novamente e execute o `Enable JavaScript` comando.  
*   Feche o DevTools.  

## Entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
