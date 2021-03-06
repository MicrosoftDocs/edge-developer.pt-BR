---
description: Abra o Menu de Comando e execute o comando "Desabilitar JavaScript".
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2067944fa17c332dd15ffb3ef97afe02d35685ed
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398557"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a>Desabilitar JavaScript com o Microsoft Edge DevTools  

Conclua as seguintes ações para exibir a aparência e o comportamento de uma página da Web quando o JavaScript está desabilitado.  

1.  [Abra o Microsoft Edge DevTools][DevToolsOpen].  
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="O Menu De comando" lightbox="../media/javascript-console-command.msft.png":::
       O **Menu De comando**  
    :::image-end:::  
    
1.  Comece a `javascript` digitar, escolha **Desabilitar JavaScript**e, em seguida, selecione `Enter` para executar o comando.  JavaScript agora está desabilitado.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Escolha Desabilitar JavaScript no Menu de Comando" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Escolha **Desabilitar JavaScript** no **Menu de Comando**  
    :::image-end:::  
    
    O ícone de aviso amarelo ao lado **de Fontes** lembra que JavaScript está desabilitado.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="O ícone de aviso ao lado de Fontes" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       O ícone de aviso ao lado de **Fontes**  
    :::image-end:::  
    
JavaScript permanece desabilitado na guia enquanto você tiver DevTools aberto.  

Talvez você queira atualizar a página para revisar se e como a página da Web depende do JavaScript durante o carregamento.  

Para habilitar o JavaScript, conclua as seguintes ações.  

*   Abra o **Menu de Comando** novamente e execute o `Enable JavaScript` comando.  
*   Feche DevTools.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
