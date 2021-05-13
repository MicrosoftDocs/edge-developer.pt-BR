---
description: Como exibir e editar localStorage com o painel Local Armazenamento e o Console.
title: Exibir e editar Armazenamento local com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5088a1b9d7ab2b92051d099e76b8b07bbd5db5f8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565047"
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
# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a>Exibir e editar o armazenamento local com Microsoft Edge DevTools  

Este guia mostra como usar Microsoft Edge [DevTools][MicrosoftEdgeDevTools] para exibir, editar e excluir pares de valores de chave [localStorage.][MDNWindowsLocalStorage]  

## <a name="view-localstorage-keys-and-values"></a>Exibir chaves e valores localStorage  

1.  Escolha a **guia Aplicativo** para abrir a **ferramenta Aplicativo.**  O **painel** Manifesto é mostrado por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       O **painel** Manifesto  
    :::image-end:::  
    
1.  Expanda **o menu Local Armazenamento.**  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="O menu Armazenamento local" lightbox="../media/storage-application-local-storage.msft.png":::
       O **menu Armazenamento** local  
    :::image-end:::  
    
1.  Escolha um domínio para exibir os pares de valores-chave.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Os pares de valores de chave localStorage para o https://www.bing.com domínio" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       Os `localStorage` pares de valores-chave para o `https://www.bing.com` domínio  
    :::image-end:::  
    
1.  Escolha uma linha da tabela para exibir o valor no visualizador abaixo da tabela.  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Exibir o valor da tecla eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       Exibir o valor da `eventLogQueue_Online` chave  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a>Criar um novo par de valores de chave localStorage  

1.  [Exibir os pares de valores de chave localStorage de um domínio](#view-localstorage-keys-and-values).  
1.  Clique duas vezes na parte vazia da tabela.  O DevTools cria uma nova linha e concentra seu cursor na **coluna** Chave.  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="A parte vazia da tabela para clicar duas vezes para criar um novo par de valores de chave" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       A parte vazia da tabela para clicar duas vezes para criar um novo par de valores de chave  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a>Editar chaves ou valores localStorage  

1.  [Exibir os pares de valores de chave localStorage de um domínio](#view-localstorage-keys-and-values).  
1.  Clique duas vezes em uma célula na coluna **Chave** ou **Valor** para editar essa chave ou valor.  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Editar uma chave localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       Editar uma `localStorage` chave  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a>Excluir pares de valores de chave localStorage  

1.  [Exibir os `localStorage` pares de valores-chave de um domínio](#view-localstorage-keys-and-values).  
1.  Escolha o par de valores-chave que você deseja excluir.  O DevTools realça o azul para indicar que ele está selecionado.  
1.  Selecione a `Delete` chave ou escolha Excluir **Selecionado** \( Excluir ![ Selecionado ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a>Excluir todos `localStorage` os pares de valores-chave para um domínio  

1.  [Exibir os `localStorage` pares de valores-chave de um domínio](#view-localstorage-keys-and-values).  
1.  Escolha **Limpar Tudo** \( Limpar Tudo ![ ](../media/clear-icon.msft.png) \).  
    
## <a name="interact-with-localstorage-from-the-console"></a>Interagir com localStorage do Console  

Como você é capaz de executar JavaScript no **Console**e, como o **Console** tem acesso aos contextos JavaScript da página, é possível interagir com a partir do `localStorage` **Console**.  

1.  Use o menu **de contextos JavaScript** para alterar o contexto JavaScript do **Console** se você quiser acessar os pares de valores-chave de um domínio diferente da página `localStorage` exibida.  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Alterar o contexto JavaScript do Console" lightbox="../media/storage-console-local-storage.msft.png":::
       Alterar o contexto JavaScript do Console  
    :::image-end:::  
    
1.  Execute suas `localStorage` expressões no Console, da mesma forma que você faz em seu JavaScript.  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagir com localStorage do Console" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       Interagir `localStorage` com a partir do **Console**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Ferramentas de desenvolvedor | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
