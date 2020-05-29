---
title: Exibir e editar armazenamento local com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612008"
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



Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir, editar e excluir [`localStorage`][MDNWindowsLocalStorage] pares de valores de chave.  

## Exibir chaves e valores de localStorage   

1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel **manifestar** é mostrado por padrão.  
    
    > ##### Figura 1  
    > Painel de manifesto  
    > ![Painel de manifesto][ImageManifest]  

1.  Expanda o menu **armazenamento local** .  
    
    > ##### Figura 2  
    > O menu **armazenamento local** mostra dois domínios: `https://business.bing.com` e `https://www.bing.com`  
    > ![O menu armazenamento local][ImageLocalStorageMenu]  

1.  Selecione um domínio para ver os pares de valor chave.  
    
    > ##### Figura 3  
    > Os `localStorage` pares de valor chave do `https://www.bing.com` domínio  
    > ![Os pares de chave-valor de localStorage para o https://www.bing.com domínio][ImageLocalStorage]  

1.  Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.  
    
    > ##### Figura 4  
    > Exibir o valor da `eventLogQueue_Online` chave  
    > ![Exibir o valor da chave eventLogQueue_Online][ImageLocalStorageViewer]  

## Criar um novo `localStorage` par chave-valor   

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Clique duas vezes na parte vazia da tabela.  O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .  
    
    > ##### Figura 5  
    > A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave  
    > ![A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave][ImageLocalStorageCreate]  

## Editar `localStorage` chaves ou valores   

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.  
    
    > ##### Figura 6  
    > Editando uma `localStorage` chave  
    > ![Editando uma chave localStorage][ImageLocalStorageEdit]  

## Excluir `localStorage` pares de chave-valor   

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  
1.  Selecione o par chave-valor que você deseja excluir.  O DevTools realça tudo em azul para indicar que está selecionado.  

1.  Pressione a `Delete` tecla ou clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] .  

## Excluir todos os `localStorage` pares de valores chave de um domínio   

1.  [Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).  

1.  Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] .  

## Interagir com `localStorage` base no console   

Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `localStorage` partir do **console**.  

1.  Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se você quiser acessar os `localStorage` pares de valores chave de um domínio que não sejam a página exibida.  
    
    > ##### Figura 7  
    > Alterando o contexto JavaScript do **console**  
    > ![Alterando o contexto JavaScript do console][ImageJSContext]  

1.  Execute suas `localStorage` expressões no console, o mesmo que você faz em seu JavaScript.  
    
    > ##### Figura 8  
    > Interagindo com `localStorage` o do **console**  
    > ![Interagindo com o localStorage a partir do console][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Figura 2: o menu armazenamento local"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Figura 3: os pares de chave-valor de localStorage para o https://www.bing.com domínio"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Figura 4: exibindo o valor da tecla eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Figura 5: a parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Figura 6: editando uma chave localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Figura 7: alterando o contexto JavaScript do console"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Figura 8: interagindo com o localStorage a partir do console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

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
