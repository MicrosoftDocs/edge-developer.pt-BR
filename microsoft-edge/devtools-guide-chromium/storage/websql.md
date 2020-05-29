---
title: Exibir dados do SQL da Web com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7a1e3e47f6761cfdb23488683107ed0df6a8f4e2
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612057"
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





# Exibir dados do SQL da Web com o Microsoft Edge DevTools   



> [!WARNING]
> A especificação SQL da Web [não está sendo mantida][W3CWebSQLStatus].  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar dados SQL da Web.  

## Exibir dados do SQL Web   

1.  Selecione a guia **fontes** para abrir o painel **fontes** .  O painel de **manifesto** geralmente abre por padrão.  
    
    > ##### Figura 1  
    > Painel de manifesto  
    > ![Painel de manifesto][ImageManifestPane]  
    
1.  Expanda a seção **SQL Web** para exibir bancos de dados e tabelas.  Na [Figura 2](#figure-2) abaixo de **html5meetup** , um banco de dados e **salas** é uma tabela.  
    
    > ##### Figura 2  
    > O painel SQL Web  
    > ![O painel SQL Web][ImageWebSQLPane]  

1.  Selecione uma tabela para exibir os dados dessa tabela.  
    
    > ##### Figura 3  
    > Exibindo os dados da tabela SQL da Web **Rooms**  
    > ![Exibindo os dados de uma tabela SQL da Web][ImageWebSQLTable]  

## Editar dados do SQL da Web   

Você não pode editar dados SQL da Web ao exibir uma tabela SQL da Web, como na **Figura 3** acima.  Mas você pode executar instruções a partir do console SQL Web que edita ou exclui tabelas.  Consulte [executar consultas do SQL Web](#run-web-sql-queries).  

## Executar consultas do SQL da Web   

1.  Selecione um banco de dados para abrir um console para esse banco de dados.  

1.  Digite uma instrução SQL da Web e pressione `Enter` para executá-la.  
    
    > ##### Figura 4  
    > Usar o console do SQL Web para excluir uma linha da tabela **salas**  
    > ![Usar o console do SQL Web para excluir uma linha de uma tabela][ImageWebSQLEdit]  

## Atualizar uma tabela SQL da Web   

O DevTools não atualiza tabelas em tempo real.  Para atualizar os dados em uma tabela:  

1.  [Exiba os dados em uma tabela SQL da Web](#view-web-sql-data).  
1.  Selecione **Atualizar** ![ atualização ][ImageRefreshIcon] .  

## Filtrar colunas em uma tabela SQL da Web   

1.  [Exiba os dados em uma tabela SQL da Web](#view-web-sql-data).  
1.  Use a caixa de texto **colunas visíveis** para especificar quais colunas você deseja mostrar.  Forneça os nomes de coluna como uma lista de CSV.  
    
    > ##### Figura 5  
    > Usar a caixa de texto **colunas visíveis** para mostrar apenas `room_name` as `last_updated` colunas e  
    > ![Usar a caixa de texto colunas visíveis para reduzir o número de colunas exibidas][ImageWebSQLFilter]  

## Excluir todos os dados SQL da Web   

1.  Abrir o painel **limpar armazenamento** .  
1.  Verifique se a caixa de seleção **SQL da Web** está habilitada.  
    
    > ##### Figura 6  
    > A caixa de seleção **SQL da Web**  
    > ![A caixa de seleção SQL da Web][ImageWebSQLCheckbox]  

1.  Selecione **limpar dados do site**.  
    
    > ##### Figura 7  
    > O botão **limpar dados do site**  
    > ![O botão limpar dados do site][ImageClearWebSQL]  

 



<!-- image links -->  

[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageWebSQLPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql.msft.png "Figura 2: painel SQL Web"  
[ImageWebSQLTable]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png "Figura 3: exibindo os dados de uma tabela SQL Web"  
[ImageWebSQLEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-commands.msft.png "Figura 4: usar o console do SQL Web para excluir uma linha de uma tabela"  
[ImageWebSQLFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png "Figura 5: usar a caixa de texto colunas visíveis para reduzir o número de colunas exibidas"  
[ImageWebSQLCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-web-sql.msft.png "Figura 6: caixa de seleção SQL da Web"  
[ImageClearWebSQL]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-clear-site-data-button.msft.png "Figura 7: botão limpar dados do site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Banco de dados SQL Web | W3C"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/websql) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
