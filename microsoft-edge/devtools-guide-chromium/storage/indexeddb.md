---
description: Como exibir e alterar dados IndexedDB com o painel de aplicativos e trechos.
title: Exibir e alterar dados IndexedDB com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 719348067b1343ca3d7781737fa6441f92ad7ba1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439707"
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

# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a>Exibir e alterar dados IndexedDB com o Microsoft Edge DevTools  

Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para exibir e alterar [dados IndexedDB.][MDNIndexedDBAPI]  Ele supõe que você está familiarizado com o DevTools.  Ele também supõe que você está familiarizado com IndexedDB.  Caso não, navegue até [Using IndexedDB][MDNUsingIndexedDB].  

## <a name="view-indexeddb-data"></a>Exibir dados IndexedDB  

1.  Escolha a **guia Aplicativo** para abrir a **ferramenta Aplicativo.**  O **painel** Manifesto geralmente é aberto por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       O **painel** Manifesto  
    :::image-end:::  
    
1.  Expanda o menu **IndexedDB** para revisar quais bancos de dados estão disponíveis.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="O menu IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       O **menu IndexedDB**  
    :::image-end:::  
    
    *   \( Ícone de banco de dados \) representa um banco de dados, onde é o nome do banco de dados e é a origem que ![ acessa o banco de ](../media/database-icon.msft.png) `notes - https://mdn.github.io` `notes` `https://mdn.github.io` dados.  
    *   \( ![ Ícone do Armazenamento de Objetos ](../media/object-store-icon.msft.png) \) é um armazenamento de `notes` objetos.  
    *   **title** e **body** são [índices][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Limitação Conhecida**  Bancos de dados de terceiros não estão visíveis.  Por exemplo, se você usar um para inserir um comercial em sua página e sua rede de comentários usar IndexedDB, os dados IndexedDB para sua rede de ad não estarão `<iframe>` visíveis.  Navegue [até emitir #943770][ChromiumIssue943770].  
    
1.  Escolha um banco de dados para analisar a origem e o número da versão.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="O banco de dados de anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       O **banco de dados de anotações**  
    :::image-end:::  
    
1.  Escolha um armazenamento de objetos para revisar os pares de valores-chave.  
    
    > [!NOTE]
    > Os dados indexedDB não são atualizados em tempo real.  Navegue [até Atualizar dados indexadosDB](#refresh-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="O armazenamento de objetos notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       O **armazenamento de objetos** notes  
    :::image-end:::  
    
    *   **Entradas totais** é o número total de pares de valores-chave no armazenamento de objetos.  
    *   **O valor do gerador de** chaves é a próxima chave disponível.  O campo só é mostrado ao usar [geradores de chaves][MDNBasicConceptsKeyGenerator].  
    
1.  Escolha uma célula na coluna **Valor** para expandir o valor.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Exibir um valor IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       Exibir um **valor IndexedDB**  
    :::image-end:::  
    
1.  Escolha um índice, como **título** ou **corpo** na figura a seguir, para classificar o armazenamento de objetos de acordo com os valores desse índice.  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Classificar um armazenamento de objetos por um índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       Classificar um armazenamento de objetos por um índice  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a>Atualizar dados IndexedDB  

Os valores indexadosDB na **ferramenta Application** não são atualizados em tempo real.  Escolha **Atualizar** \( Atualizar \) ao exibir um armazenamento de objetos para atualizar os dados ou exibir um banco de dados e escolher Atualizar banco de dados para ![ atualizar todos os ](../media/reload-icon.msft.png) dados. ****  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Exibir um banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   Exibir um banco de dados  
:::image-end:::  

## <a name="edit-indexeddb-data"></a>Editar dados IndexedDB  

As teclas indexadasDB e os valores não podem ser editáveis na **ferramenta Application.**  Como o DevTools tem acesso ao contexto da página, no entanto, você pode executar código JavaScript no DevTools para editar dados indexadosDB.  

### <a name="edit-indexeddb-data-with-snippets"></a>Editar dados indexadosdb com trechos  

[Trechos de código][DevtoolsJavascriptSnippets] são uma maneira de armazenar e executar blocos de código JavaScript no DevTools.  Quando você executar um trecho de código, o resultado será registrado no **Console**.  Você pode usar um trecho para executar código JavaScript para editar um banco de dados IndexedDB.  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar um trecho de código para interagir com IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   Usar um trecho de código para interagir com IndexedDB  
:::image-end:::  

## <a name="delete-indexeddb-data"></a>Excluir dados IndexedDB  

### <a name="delete-an-indexeddb-key-value-pair"></a>Excluir um par de valores de chave IndexedDB  

1.  [Exibir um armazenamento de objetos IndexedDB](#view-indexeddb-data).  
1.  Escolha o par de valores-chave que você deseja excluir.  O DevTools realça-o para indicar que ele está selecionado.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Escolha um par de valores-chave para excluí-lo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       Escolha um par de valores-chave para excluí-lo  
    :::image-end:::  
    
1.  Selecione a `Delete` chave ou escolha Excluir **Selecionado** \( Excluir ![ Selecionado ](../media/delete-icon.msft.png) \).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Como o armazenamento de objetos se parece após a exclusão do par de valores-chave" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       Como o armazenamento de objetos se parece após a exclusão do par de valores-chave  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a>Excluir todos os pares de valores-chave em um armazenamento de objetos  

1.  [Exibir um armazenamento de objetos IndexedDB](#view-indexeddb-data).  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Exibir um armazenamento de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       Exibir um armazenamento de objetos  
    :::image-end:::  
    
1.  Escolha **Limpar o armazenamento de objetos** \( Limpar o armazenamento de objetos ![ ](../media/clear-icon.msft.png) \).  
    
### <a name="delete-an-indexeddb-database"></a>Excluir um banco de dados IndexedDB  

1.  [Exibir o banco de dados IndexedDB](#view-indexeddb-data) que você deseja excluir.  
1.  Escolha **Excluir banco de dados**.  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="O botão Excluir banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       O **botão Excluir banco de dados**  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a>Excluir todo o armazenamento IndexedDB  

1.  Abra o **painel Limpar armazenamento.**  
1.  Verifique se a **caixa de seleção IndexedDB** está habilitada.  
1.  Escolha **Limpar dados do site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="O painel Limpar armazenamento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       O **painel Limpar armazenamento**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: Mostrar bancos de dados indexadosdb iframe - chromium - Monotrilho"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de Chaves - Conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Api IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice - Usando indexadoDB | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
