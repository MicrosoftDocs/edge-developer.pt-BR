---
description: Como exibir e editar localStorage com o painel armazenamento local e o console.
title: Exibir e editar armazenamento local com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 25404e454187db941dc12d356dfe5ae7437d833b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125416"
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

# Exibir e editar armazenamento local com o Microsoft Edge DevTools  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir, editar e excluir pares de chave-valor de [localStorage][MDNWindowsLocalStorage] .  

## Exibir chaves e valores de localStorage  

1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel **manifestar** é mostrado por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       Painel de **manifesto**  
    :::image-end:::  
    
1.  Expanda o menu **armazenamento local** .  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-local-storage.msft.png":::
       O menu **armazenamento local**  
    :::image-end:::  
    
1.  Selecione um domínio para ver os pares de valor chave.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Os `localStorage` pares de valor chave do `https://www.bing.com` domínio  
    :::image-end:::  
    
1.  Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Exibir o valor da `eventLogQueue_Online` chave  
    :::image-end:::  
    
## Criar um novo par de chave-valor localStorage  

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Clique duas vezes na parte vazia da tabela.  O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave  
    :::image-end:::  
    
## Editar chaves ou valores de localStorage  

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Editar uma `localStorage` chave  
    :::image-end:::  
    
## Excluir pares de chave-valor de localStorage  

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Selecione o par chave-valor que você deseja excluir.  O DevTools realça tudo em azul para indicar que está selecionado.  
1.  Pressione a `Delete` tecla ou escolha **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).  
    
## Excluir todos os `localStorage` pares de valores chave de um domínio  

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Escolha **limpar tudo** \ ( ![ limpar tudo ][ImageClearIcon] \).  
    
## Interagir com o localStorage a partir do console  

Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `localStorage` partir do **console**.  

1.  Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se você quiser acessar os `localStorage` pares de valores chave de um domínio que não sejam a página exibida.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-console-local-storage.msft.png":::
       Alterar o contexto JavaScript do console  
    :::image-end:::  
    
1.  Execute suas `localStorage` expressões no console, o mesmo que você faz em seu JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interagir com `localStorage` base no **console**  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
