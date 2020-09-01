---
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 587f4780432b1b2b964462d2d7f5779f447f1313
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982904"
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



Para ver como uma página da Web tem uma aparência e se comporta quando o JavaScript está desabilitado.  

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
    
O JavaScript permanece desabilitado nessa guia por quanto tempo você tiver o DevTools aberto.  

Você pode querer recarregar a página para ver se e como a página depende de JavaScript durante o carregamento.  

Para habilitar novamente o JavaScript, conclua as ações a seguir.  

*   Abra o **menu de comandos** novamente e execute o `Enable JavaScript` comando.  
*   Feche o DevTools.  

<!--  
## Feedback   


-->  

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
