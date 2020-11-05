---
description: Mover usuários para o Microsoft Edge do Internet Explorer
title: Mover usuários para o Microsoft Edge do Internet Explorer
author: MSEdgeTeam
ms.date: 11/04/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web, Internet Explorer
ms.openlocfilehash: 48f0f4121fb444d80603dcbb408397679c64753d
ms.sourcegitcommit: 7b4441b7656c8317139650f904b70cc87797d37e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154326"
---
# Mover usuários para o Microsoft Edge do Internet Explorer 

Muitos sites modernos têm designs que são incompatíveis com o Internet Explorer \ (IE \).  Quando um usuário do IE visita um site público incompatível, o usuário pode receber uma mensagem.  A mensagem informa que o site é incompatível com o navegador.  Depois que a mensagem é exibida, o usuário deve alternar manualmente para um navegador moderno.  Para minimizar as interrupções, começando com a versão 84, o Microsoft Edge aceita uma nova funcionalidade que redireciona os usuários automaticamente.  Quando um usuário do IE navega para um site que é incompatível com o IE, o Windows redireciona automaticamente o usuário para o Microsoft Edge.  Para revisar os sites na lista, navegue até a [lista necessária do Microsoft Edge][MicrosoftEdgeNeededgeV1].

Este artigo descreve os conceitos a seguir.  

*   A experiência do usuário para redirecionamento  
*   Como adicionar seu site à lista de compatibilidade do IE  
*   Como remover seu site da lista de compatibilidade do IE  
    
## Por que um site foi adicionado à lista de compatibilidade do IE?  

A lista de compatibilidade do IE adiciona apenas um site quando as seguintes ações ocorrem.  

*   Mostra um usuário do IE que uma mensagem sugerindo o usuário deve usar um navegador diferente por motivos de compatibilidade.  
*   As solicitações de proprietário para adicionar o site à lista de compatibilidade do IE.  
    
## Atualizar a lista de compatibilidade do IE  

A lista de compatibilidade do IE é um arquivo XML no [Microsoft.com][MicrosoftOfficialHome].  A lista é atualizada regularmente em resposta a solicitações de desenvolvedores de sites e usuários para que os sites sejam adicionados ou removidos.  As atualizações da lista são baixadas automaticamente para computadores dos usuários.  

Envie por email as informações a seguir para [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que o seu site seja adicionado ou removido da lista de compatibilidade do IE.    

*   Nome do proprietário  
*   Título corporativo  
*   Email  
*   Nome da empresa  
*   Rua  
*   Endereço do site  
<!--  *   Telephone number  -->  
<!--  *   Target platform \(desktop, phone, Xbox\)  -->  
    
<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar um email para ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "É preciso ter o Microsoft Edge List v1 XML | Microsoft Edge"  
