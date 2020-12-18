---
description: Como exibir e alterar dados do IndexedDB com o painel do aplicativo e Snippets.
title: Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231199"
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

# Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir e alterar dados do [IndexedDB][MDNIndexedDBAPI] .  Ele pressupõe que você esteja familiarizado com o DevTools.  Ele também pressupõe que você esteja familiarizado com o IndexedDB.  Caso contrário, navegue até [usando o IndexedDB][MDNUsingIndexedDB].  

## Exibir dados do IndexedDB  

1.  Escolha a guia **aplicativo** para abrir a ferramenta **aplicativo** .  O painel de **manifesto** geralmente abre por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Painel de **manifesto**  
    :::image-end:::  
    
1.  Expanda o menu **IndexedDB** para verificar quais bancos de dados estão disponíveis.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="O menu IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       O menu **IndexedDB**  
    :::image-end:::  
    
    *   \ ( ![ Ícone de banco de dados ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` representa um banco de dados, onde `notes` é o nome do banco de dados e `https://mdn.github.io` é a origem que acessa o banco de dados.  
    *   \ ( ![ Ícone de repositório de objetos ][ImageObjectStoreIcon] \) `notes` é um repositório de objetos.  
    *   **título** e **corpo** são [índices][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitação conhecida**  Os bancos de dados de terceiros não estão visíveis.  Por exemplo, se você usar um `<iframe>` para inserir um anúncio em sua página, e sua rede de AD usar o IndexedDB, os dados do IndexedDB para a sua rede de anúncios não serão visíveis.  Navegue até o [problema #943770][ChromiumIssue943770].  
    
1.  Escolha um banco de dados para revisar a origem e o número da versão.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="O banco de dados anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       O banco de dados **anotações**  
    :::image-end:::  
    
1.  Escolha um repositório de objetos para examinar os pares de valor chave.  
    
    > [!NOTE]
    > Os dados do IndexedDB não são atualizados em tempo real.  Navegue para [atualizar os dados do IndexedDB](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="O repositório de objetos anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       O repositório de objetos **anotações**  
    :::image-end:::  
    
    *   **Total de entradas** é o número total de pares de valores chave no repositório de objetos.  
    *   O **valor do gerador de chave** é a próxima chave disponível.  O campo só é mostrado ao usar os [geradores de chave][MDNBasicConceptsKeyGenerator].  
    
1.  Escolha uma célula na coluna **valor** para expandir o valor.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Exibir um valor de IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Exibir um valor de **IndexedDB**  
    :::image-end:::  
    
1.  Escolha um índice, como **título** ou **corpo** na figura a seguir, para classificar o repositório de objetos de acordo com os valores desse índice.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Classificar um repositório de objetos por um índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Classificar um repositório de objetos por um índice  
    :::image-end:::  
    
## Atualizar dados do IndexedDB  

Os valores de IndexedDB na ferramenta do **aplicativo** não são atualizados em tempo real.  Escolha **Atualizar** \ ( ![ Atualizar ][ImageReloadIcon] \) ao exibir um repositório de objetos para atualizar os dados ou exibir um banco de dados e escolha **Atualizar banco** de dados para atualizar todos os dados.  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Exibir um banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Exibir um banco de dados  
:::image-end:::  

## Editar dados do IndexedDB  

As chaves e os valores de IndexedDB não são editáveis na ferramenta do **aplicativo** .  No entanto, como o DevTools tem acesso ao contexto da página, você pode executar o código JavaScript dentro do DevTools para editar os dados do IndexedDB.  

### Editar dados do IndexedDB com snippets  

Os [trechos][DevtoolsJavascriptSnippets] de código são uma maneira de armazenar e executar blocos de código JavaScript dentro do devtools.  Quando você executa um snippet, o resultado é registrado no **console**.  Você pode usar um snippet para executar o código JavaScript para editar um banco de dados do IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar um trecho para interagir com IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Usar um trecho para interagir com IndexedDB  
:::image-end:::  

## Excluir dados do IndexedDB  

### Excluir um par de valor-chave IndexedDB  

1.  [Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).  
1.  Selecione o par chave-valor que você deseja excluir.  O DevTools a destaca para indicar que está selecionado.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Selecionar um par de valor chave para excluí-lo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Selecionar um par de valor chave para excluí-lo  
    :::image-end:::  
    
1.  Pressione a `Delete` tecla ou escolha **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Como a loja de objetos se parece após o par de valor chave ter sido excluído" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Como a loja de objetos se parece após o par de valor chave ter sido excluído  
    :::image-end:::  
    
### Excluir todos os pares de valores chave em um repositório de objetos  

1.  [Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Exibir um repositório de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Exibir um repositório de objetos  
    :::image-end:::  
    
1.  Escolha **limpar repositório de objetos** \ ( ![ limpar repositório de objetos ][ImageClearIcon] \).  
    
### Excluir um banco de dados do IndexedDB  

1.  [Exiba o banco de dados do IndexedDB](#view-indexeddb-data) que você deseja excluir.  
1.  Escolha **excluir banco de dados**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="O botão excluir banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       O botão **excluir banco de dados**  
    :::image-end:::  
    
### Excluir todo o armazenamento do IndexedDB  

1.  Abrir o painel **limpar armazenamento** .  
1.  Verifique se a caixa de seleção **IndexedDB** está habilitada.  
1.  Escolha **limpar dados do site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="O painel limpar armazenamento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       O painel **limpar armazenamento**  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools | Documentos da Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: show iframe IndexedDB bancos de dados-Chromium-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de chave-conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando o IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice-usando IndexedDB | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
