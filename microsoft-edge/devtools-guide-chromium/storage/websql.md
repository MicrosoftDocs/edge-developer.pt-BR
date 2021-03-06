---
description: Como exibir dados SQL Web no painel Aplicativo do Microsoft Edge DevTools.
title: Exibir dados SQL Web com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 326fe492a3436a40d81c8e31db99a26da4ea054f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397549"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a>Exibir dados SQL Web com o Microsoft Edge DevTools  

> [!WARNING]
> A especificação SQL Web [não está sendo mantida.][W3CWebSQLStatus]  

Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspecionar dados SQL Web.  

## <a name="view-web-sql-data"></a>Exibir dados SQL Web  

1.  Escolha a **ferramenta Fontes** para abrir a **ferramenta Sources.**  O **painel** Manifesto geralmente é aberto por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       O **painel** Manifesto  
    :::image-end:::  
    
1.  Expanda a **seção SQL** Web para exibir bancos de dados e tabelas.  Na figura a seguir, abaixo **html5meetup** está um banco de dados e **salas** é uma tabela.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="O painel SQL Web" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       O **painel SQL** Web  
    :::image-end:::  
    
1.  Escolha uma tabela para exibir os dados dessa tabela.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Exibir os dados de uma tabela de SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Exibir os dados de uma tabela de SQL Web  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a>Editar dados SQL Web  

Você não é capaz de editar dados SQL Web ao exibir uma tabela SQL Web, como na anterior acima.  Mas você pode executar instruções do Console web SQL que editam ou excluem tabelas.  Navegue [até Executar consultas SQL Web.](#run-web-sql-queries)  

## <a name="run-web-sql-queries"></a>Executar consultas SQL Web  

1.  Escolha um banco de dados para abrir um console para esse banco de dados.  
1.  Digite uma instrução SQL Web e selecione `Enter` para executar.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Usar o Console SQL Web para excluir uma linha de uma tabela" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Usar o Console SQL Web para excluir uma linha de uma tabela  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a>Atualizar uma tabela SQL Web  

O DevTools não atualiza tabelas em tempo real.  Para atualizar os dados em uma tabela, conclua as seguintes ações.  

1.  [Exibir os dados em uma tabela SQL Web.](#view-web-sql-data)  
1.  Escolha **Atualizar** \( ![ Atualizar ][ImageRefreshIcon] \).  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a>Filtrar colunas em uma tabela SQL Web  

1.  [Exibir os dados em uma tabela SQL Web.](#view-web-sql-data)  
1.  Use a **caixa de texto Colunas** Visíveis para especificar quais colunas você deseja mostrar.  Forneça os nomes das colunas como uma lista CSV.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Use a caixa de texto Colunas Visíveis para reduzir o número de colunas mostradas" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Use a **caixa de texto Colunas** Visíveis para reduzir o número de colunas mostradas  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a>Excluir todos os dados SQL Web  

1.  Abra o **painel Limpar Armazenamento.**  
1.  Verifique se a caixa de **SQL** Web está 100% 100% 2000.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Caixa de SQL Web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       Caixa **de SQL** Web  
    :::image-end:::  
    
1.  Escolha **Limpar dados do site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="O botão Limpar Dados do Site" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       O **botão Limpar Dados do Site**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL banco de dados | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/websql) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
