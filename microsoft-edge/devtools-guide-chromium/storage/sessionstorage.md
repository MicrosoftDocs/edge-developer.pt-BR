---
description: Como exibir e editar sessionStorage com o painel armazenamento da sessão e o console.
title: Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6543c03f04ff80b1bba1d244598a901d066db13a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125472"
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
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       Painel de **manifesto**  
    :::image-end:::  
    
1.  Expanda o menu **armazenamento da sessão** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       O menu de **armazenamento de sessão**  
    :::image-end:::  
    
1.  Selecione um domínio para ver os pares de valor chave.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Os `sessionStorage` pares de valor chave  
    :::image-end:::  
    
1.  Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Exibir o valor da `x-sid` chave  
    :::image-end:::  
    
## Criar um novo par de chave-valor sessionStorage  

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Clique duas vezes na parte vazia da tabela.  O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave  
    :::image-end:::  
    
## Editar chaves ou valores de sessionStorage  

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Editar uma `sessionStorage` chave  
    :::image-end:::  
    
## Excluir pares de chave-valor de sessionStorage  

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Selecione o par chave-valor que você deseja excluir.  O DevTools realça tudo em azul para indicar que está selecionado.  
1.  Pressione a `Delete` tecla ou escolha **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).  
    
## Excluir todos os pares de chave-valor sessionStorage de um domínio  

1.  [Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Escolha **limpar tudo** \ ( ![ limpar tudo ][ImageClearIcon] \).  
    
## Interagir com o sessionStorage a partir do console  

Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `sessionStorage` partir do **console**.  

1.  Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se desejar acessar os `sessionStorage` pares de valores chave de um domínio que não sejam a página em que você está.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-console-domain-selection.msft.png":::
       Alterar o contexto JavaScript do console  
    :::image-end:::  
    
1.  Execute suas `sessionStorage` expressões no console, da mesma forma que faria no JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interagir com `sessionStorage` base no **console**  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

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
