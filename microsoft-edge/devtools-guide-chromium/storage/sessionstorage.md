---
title: Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612078"
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





# Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools   

  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir, editar e excluir [`sessionStorage`][MDNSessionStorage] pares de valores de chave.  

## Exibir chaves e valores de sessionStorage   

1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel **manifestar** é mostrado por padrão.  
    
    > ##### Figura 1  
    > Painel de manifesto  
    > ![Painel de manifesto][ImageManifest]  

1.  Expanda o menu **armazenamento da sessão** .  
    
    > ##### Figura 2  
    > O menu de **armazenamento de sessão**  
    > ![O menu de armazenamento de sessão][ImageSessionStorageMenu]  

1.  Selecione um domínio para ver os pares de valor chave.  
    
    > ##### Figura 3  
    > Os pares de chave-valor de sessionStorage  
    > ![Os pares de chave-valor ' sessionStorage '][ImageSessionStorage]  

1.  Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.  
    
    > ##### Figura 4  
    > Exibir o valor da `x-sid` chave  
    > ![Exibir o valor da chave x-Sid][ImageSessionStorageViewer]  

## Criar um novo par de chave-valor sessionStorage   

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Clique duas vezes na parte vazia da tabela.  O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .  
    
    > ##### Figura 5  
    > A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave  
    > ![A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave][ImageSessionStorageCreate]  

## Editar chaves ou valores de sessionStorage   

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.  
    
    > ##### Figura 6  
    > Editando uma `sessionStorage` chave  
    > ![Editando uma chave sessionStorage][ImageSessionStorageEdit]  

## Excluir pares de chave-valor de sessionStorage   

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Selecione o par chave-valor que você deseja excluir.  O DevTools realça tudo em azul para indicar que está selecionado.  

1.  Pressione a `Delete` tecla ou clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] .  

## Excluir todos os pares de chave-valor sessionStorage de um domínio   

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  

1.  Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] .  

## Interagir com o sessionStorage a partir do console   

Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `sessionStorage` partir do **console**.  

1.  Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se desejar acessar os `sessionStorage` pares de valores chave de um domínio que não sejam a página em que você está.  
    
    > ##### Figura 7  
    > Alterando o contexto JavaScript do **console**  
    > ![Alterando o contexto JavaScript do console][ImageJSContext]  

1.  Execute suas `sessionStorage` expressões no console, da mesma forma que faria no JavaScript.  
    
    > ##### Figura 8  
    > Interagindo com `sessionStorage` o do **console**  
    > ![Interagindo com o sessionStorage a partir do console][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Figura 2: o menu de armazenamento da sessão"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Figura 3: os pares de chave-valor de sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Figura 4: exibindo o valor da chave x-Sid"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Figura 5: a parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave"  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Figura 6: editando uma chave sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Figura 7: alterando o contexto JavaScript do console"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Figura 8: interagindo com o sessionStorage a partir do console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
