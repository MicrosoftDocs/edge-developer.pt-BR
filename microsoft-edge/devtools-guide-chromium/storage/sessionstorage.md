---
description: Como exibir e editar sessõesStorage com o painel Armazenamento de Sessão e o Console.
title: Exibir e editar o armazenamento de sessão com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: cf00d71302e7a1f16ba1cceaa17c9380245d12f8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398004"
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

# <a name="view-and-edit-session-storage-with-microsoft-edge-devtools"></a>Exibir e editar o armazenamento de sessão com o Microsoft Edge DevTools  

Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para exibir, editar e excluir pares de valores de chave [sessionStorage.][MDNSessionStorage]  

## <a name="view-sessionstorage-keys-and-values"></a>Exibir teclas e valores sessionStorage  

1.  Escolha a **guia Aplicativo** para abrir a **ferramenta Aplicativo.**  O **painel** Manifesto é mostrado por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       O **painel** Manifesto  
    :::image-end:::  
    
1.  Expanda o menu **Armazenamento de** Sessão.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="O Menu de Armazenamento de Sessão" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       O **Menu de Armazenamento de** Sessão  
    :::image-end:::  
    
1.  Escolha um domínio para exibir os pares de valores-chave.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Os pares de valores de chave sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       Os `sessionStorage` pares de valores-chave  
    :::image-end:::  
    
1.  Escolha uma linha da tabela para exibir o valor no visualizador abaixo da tabela.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Exibir o valor da chave x-sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       Exibir o valor da `x-sid` chave  
    :::image-end:::  
    
## <a name="create-a-new-sessionstorage-key-value-pair"></a>Criar um novo par de valores de chave sessionStorage  

1.  [Exibir os pares de valores de chave sessionStorage de um domínio](#view-sessionstorage-keys-and-values).  
1.  Clique duas vezes na parte vazia da tabela.  O DevTools cria uma nova linha e concentra seu cursor na **coluna** Chave.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="A parte vazia da tabela para clicar duas vezes para criar um novo par de valores de chave" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       A parte vazia da tabela para clicar duas vezes para criar um novo par de valores de chave  
    :::image-end:::  
    
## <a name="edit-sessionstorage-keys-or-values"></a>Editar teclas ou valores sessionStorage  

1.  [Exibir os pares de valores de chave sessionStorage de um domínio](#view-sessionstorage-keys-and-values).  
1.  Clique duas vezes em uma célula na coluna **Chave** ou **Valor** para editar essa chave ou valor.  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Editar uma chave sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       Editar uma `sessionStorage` chave  
    :::image-end:::  
    
## <a name="delete-sessionstorage-key-value-pairs"></a>Excluir pares de valores de chave sessionStorage  

1.  [Exibir os `sessionStorage` pares de valores-chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Escolha o par de valores-chave que você deseja excluir.  O DevTools realça o azul para indicar que ele está selecionado.  
1.  Selecione a `Delete` chave ou escolha Excluir **Selecionado** \( Excluir ![ Selecionado ][ImageDeleteIcon] \).  
    
## <a name="delete-all-sessionstorage-key-value-pairs-for-a-domain"></a>Excluir todos os pares de valores de chave sessionStorage para um domínio  

1.  [Exibir os `sessionStorage` pares de valores-chave de um domínio](#view-sessionstorage-keys-and-values).  
1.  Escolha **Limpar Tudo** \( Limpar Tudo ![ ][ImageClearIcon] \).  
    
## <a name="interact-with-sessionstorage-from-the-console"></a>Interagir com sessionStorage do Console  

Como você pode executar JavaScript no **Console**e, como o **Console** tem acesso aos contextos JavaScript da página, é possível interagir com a partir `sessionStorage` do **Console**.  

1.  Use o menu **de contextos JavaScript** para alterar o contexto JavaScript do **Console** se você quiser acessar os pares de valores-chave de um domínio diferente da página em que `sessionStorage` você está.  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Alterar o contexto JavaScript do Console" lightbox="../media/storage-console-domain-selection.msft.png":::
       Alterar o contexto JavaScript do **Console**  
    :::image-end:::  
    
1.  Execute suas `sessionStorage` expressões no **Console**, da mesma forma que seu JavaScript.  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagir com sessionStorage do Console" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       Interagir `sessionStorage` com a partir do **Console**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window.sessionStorage | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
