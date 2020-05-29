---
title: Desabilitar JavaScript com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581807"
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



Para ver como uma página da Web tem a aparência e se comporta quando o JavaScript está desabilitado:  

1.  [Abra o Microsoft Edge devtools][DevToolsOpen].  
1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
    
    > ##### Figura 1  
    > O menu de comando  
    > ![O menu de comando][ImageCommandMenu]  
    
1.  Comece a digitar `javascript` , selecione **desativar JavaScript**e pressione `Enter` para executar o comando.  JavaScript agora está desabilitado.  
    
    > ##### Figura 2  
    > Selecionar **desativar JavaScript** no menu de comando  
    > ![Selecionar desativar JavaScript no menu de comando][ImageDisableJS]  
    
    O ícone de aviso amarelo ao lado de **fontes** lembra que o JavaScript está desabilitado.  
    
    > ##### Figura 3  
    > O ícone de aviso ao lado de **fontes**  
    > ![O ícone de aviso ao lado de fontes][ImageDisableJSWarning]  

O JavaScript permanece desabilitado nessa guia por quanto tempo você tiver o DevTools aberto.  

Você pode querer recarregar a página para ver se e como a página depende de JavaScript durante o carregamento.  

Para habilitar novamente o JavaScript:  

*   Abra o **menu de comandos** novamente e execute o `Enable JavaScript` comando.  
*   Feche o DevTools.  

## Privacidade Jurídica   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Figura 1: menu de comando"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Figura 2: selecionando desabilitar JavaScript no menu de comando"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Figura 3: o ícone de aviso ao lado de fontes"  

<!-- links -->  

[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
