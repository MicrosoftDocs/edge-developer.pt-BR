---
title: Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612085"
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

  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir e alterar dados do [IndexedDB][MDNIndexedDBAPI] .  Ele pressupõe que você esteja familiarizado com o DevTools.  Ele também pressupõe que você esteja familiarizado com o IndexedDB.  Caso contrário, consulte [usando o IndexedDB][MDNUsingIndexedDB].  

## Exibir dados do IndexedDB   

1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel de **manifesto** geralmente abre por padrão.  
    
    > ##### Figura 1  
    > Painel de manifesto  
    > ![Painel de manifesto][ImageManifest]  

1.  Expanda o menu **IndexedDB** para ver quais bancos de dados estão disponíveis.  
    
    > ##### Figura 2  
    > O menu **IndexedDB**  
    > ![O menu IndexedDB][ImageIndexedDBMenu]  
    
    *   ![Ícone de banco de dados ][ImageDatabaseIcon] `notes - https://mdn.github.io` representa um banco de dados, onde `notes` é o nome do banco de dados e `https://mdn.github.io` é a origem que acessa o banco de dados.  
    *   ![][ImageObjectStoreIcon] `notes` O ícone de repositório de objetos é um repositório de objetos.  
    *   **título** e **corpo** são [índices][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitação conhecida**  Os bancos de dados de terceiros não estão visíveis.  Por exemplo, se você usar um `<iframe>` para inserir um anúncio em sua página, e sua rede de AD usar o IndexedDB, os dados do IndexedDB para a sua rede de anúncios não serão visíveis.  Veja o [problema #943770][ChromiumIssue943770].  
    
1.  Selecione um banco de dados para ver a origem e o número da versão.  
    
    > ##### Figura 3  
    > O banco de dados **anotações**  
    > ![O banco de dados anotações][ImageIndexedDBDatabase]  
    
1.  Selecione um repositório de objetos para ver os pares de valor chave.  
    
    > [!NOTE]
    > Os dados do IndexedDB não são atualizados em tempo real.  Consulte [atualizar dados do IndexedDB](#refresh-indexeddb-data).  
    
    > ##### Figura 4  
    > O repositório de objetos **anotações**  
    > ![O repositório de objetos anotações][ImageIndexedDBObjectStore]  

    *   **Total de entradas** é o número total de pares de valores chave no repositório de objetos.  
    *   O **valor do gerador de chave** é a próxima chave disponível.  Este campo é mostrado apenas ao usar [geradores de chaves][MDNBasicConceptsKeyGenerator].  

1.  Selecione uma célula na coluna **valor** para expandir esse valor.  
    
    > ##### Figura 5  
    > Exibindo um valor de IndexedDB  
    > ![Exibindo um valor de IndexedDB][ImageIndexedBDValue]  
    
1.  Selecione um índice, como **título** ou **corpo** na [Figura 6](#figure-6), para classificar o repositório de objetos de acordo com os valores desse índice.  
   
    > ##### Figura 6  
    > Um repositório de objetos que é classificado em ordem alfabética de acordo com a chave de **título**  
    > ![Classificando um repositório de objetos por um índice][ImageIndexedDBIndex]  

## Atualizar dados do IndexedDB   

Os valores de IndexedDB no painel do **aplicativo** não são atualizados em tempo real.  Selecione **Atualizar** ![ atualização ][ImageReloadIcon] ao exibir um repositório de objetos para atualizar os dados ou exibir um banco de dados e clique em **Atualizar banco** de dados para atualizar todos os dados.  

> ##### Figura 7  
> Exibir um banco de dados  
> ![Exibir um banco de dados][ImageIndexedDBDatabase2]  

## Editar dados do IndexedDB   

As chaves e os valores do IndexedDB não podem ser editados no painel do **aplicativo** .  No entanto, como o DevTools tem acesso ao contexto da página, você pode executar o código JavaScript dentro do DevTools para editar os dados do IndexedDB.  

### Editar dados do IndexedDB com snippets   

Os [trechos][DevtoolsJavascriptSnippets] de código são uma maneira de armazenar e executar blocos de código JavaScript dentro do devtools.  Quando você executa um snippet, o resultado é registrado no **console**.  Você pode usar um snippet para executar o código JavaScript para editar um banco de dados do IndexedDB.  

> ##### Figura 8  
> Usando um trecho para interagir com IndexedDB  
> ![Usando um trecho para interagir com IndexedDB][ImageIndexedDBSnippet]  

## Excluir dados do IndexedDB   

### Excluir um par de valor-chave IndexedDB   

1.  [Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).  
1.  Selecione o par chave-valor que você deseja excluir.  O DevTools a destaca para indicar que está selecionado.  
    
    > ##### Figura 9  
    > Selecionando um par de valores chave para excluí-lo  
    > ![Selecionando um par de valores chave para excluí-lo][ImageIndexedDBKeyValuePair]  

1.  Pressione a `Delete` tecla ou clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] .  
    
    > ##### Figura 10  
    > Como a loja de objetos se parece após o par de valor chave ter sido excluído  
    > ![Como a loja de objetos se parece após o par de valor chave ter sido excluído][ImageIndexedDBKeyValuePairDeleted]  

### Excluir todos os pares de valores chave em um repositório de objetos   

1.  [Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).  
    
    > ##### Figura 11  
    > Exibir um repositório de objetos  
    > ![Exibir um repositório de objetos][ImageIndexedDBObjectStore]  

1.  Selecione **limpar repositório de objetos** ![ limpar repositório de objetos ][ImageClearIcon] .  

### Excluir um banco de dados do IndexedDB   

1.  [Exiba o banco de dados do IndexedDB](#view-indexeddb-data) que você deseja excluir.  
1.  Selecione **excluir banco de dados**.  
    
    > ##### Figura 12  
    > O botão **excluir banco de dados**  
    > ![O botão excluir banco de dados][ImageIndexedDBDatabase]  

### Excluir todo o armazenamento do IndexedDB   

1.  Abrir o painel **limpar armazenamento** .  

1.  Verifique se a caixa de seleção **IndexedDB** está habilitada.  

1.  Selecione **limpar dados do site**.  
    
    > ##### Figura 13  
    > O painel **limpar armazenamento** ![ o painel limpar armazenamento][ImageIndexedDBClearStorage]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Figura 1: o painel manifestar"  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Figura 2: o menu IndexedDB"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Figura 3: o banco de dados do notes_db"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Figura 4: o repositório de objetos notes_os"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Figura 5: exibindo um valor de IndexedDB"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Figura 6: classificando um repositório de objetos por um índice"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Figura 7: exibindo um banco de dados"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Figura 8: usando um snippet para interagir com IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Figura 9: selecionando um par de valor chave para excluí-lo"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Figura 10: qual a aparência do repositório de objetos após o par de valor chave ter sido excluído"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Figura 11: exibindo um repositório de objetos"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Figura 12: botão excluir banco de dados"  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Figura 13: o painel limpar armazenamento"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: show iframe IndexedDB bancos de dados-Chromium-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de chave-conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando o IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice-usando IndexedDB | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
