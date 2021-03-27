---
description: Mover usuários para o Microsoft Edge do Internet Explorer
title: Mover usuários para o Microsoft Edge do Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web, Internet Explorer
ms.openlocfilehash: c2106955ed79bd28dc1f847dee220944bb014689
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461133"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a>Mover usuários para o Microsoft Edge do Internet Explorer  

Muitos sites modernos têm designs incompatíveis com o Internet Explorer \(IE\).  Quando um usuário do IE visita um site público incompatível, o usuário pode receber uma mensagem.  A mensagem afirma que o site é incompatível com o navegador.  Depois que a mensagem for exibida, o usuário deverá alternar manualmente para um navegador moderno.  Para minimizar as interrupções, a partir da versão 84, o Microsoft Edge oferece suporte a um novo recurso que redireciona automaticamente os usuários.  Quando um usuário do IE navega para um site incompatível com o IE, o Windows redireciona automaticamente o usuário para o Microsoft Edge.  Para revisar os sites na lista, navegue até [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].

Este artigo descreve os seguintes conceitos.  

*   Por que um site é adicionado à lista  
*   A experiência do usuário para redirecionamento  
*   Solicitar uma atualização para a lista  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a>Por que um site é adicionado à lista de compatibilidade do IE?  

A Lista de compatibilidade do IE só adiciona um site quando as ações a seguir ocorrem.  

*   Mostra a um usuário do IE uma mensagem sugerindo que o usuário deve usar um navegador diferente por motivos de compatibilidade.  
*   O proprietário solicita adicionar o site à lista de compatibilidade do IE.  

## <a name="redirection-experience"></a>Experiência de redirecionamento

Ao redirecionar para o Microsoft Edge, o usuário é mostrado a caixa de diálogo única na próxima captura de tela.  A caixa de diálogo fornece ao usuário as seguintes informações.  

*   Ele explica por que o site está sendo redirecionado.  
*   Ele solicita ao usuário consentimento para copiar dados de navegação e preferências do IE para o Microsoft Edge.  

:::row:::
   :::column span="":::
      Os dados de navegação a seguir são importados.  
      
      *   Favoritos  
      *   Senhas  
      *   Mecanismos de pesquisa  
      *   Abrir guias  
      *   Histórico  
      *   Configurações  
      *   Cookies  
      *   A Home Page  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notificação de navegação e prompt para importar dados e preferências" lightbox="../media/neededge-dialog1.msft.png":::
         Notificação de navegação e prompt para importar dados e preferências  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Se o usuário não consentir escolhendo a caixa de seleção Sempre trazer meus dados de **** navegação e preferências do **Internet Explorer,** o usuário poderá escolher Continuar a navegação para continuar a sessão   de navegação.  

Por fim, um banner de incompatibilidade de site é exibido na barra de endereços para cada redirecionamento.  Um exemplo de uma faixa de incompatibilidade de site é exibido na figura a seguir.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificação sobre sites modernos e prompt para definir o Microsoft Edge como navegador padrão ou explorar o Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Notificação sobre sites modernos e prompt para definir o Microsoft Edge como navegador padrão ou explorar o Microsoft Edge  
:::image-end:::

A faixa de incompatibilidade do site fornece os seguintes detalhes para o usuário.  

*   Recomenda que o usuário alternar para o Microsoft Edge.  
*   Oferece para definir o Microsoft Edge como o navegador padrão.  
*   Oferece ao usuário a opção de explorar o Microsoft Edge.    
    
Quando um site é redirecionado do Internet Explorer para o Microsoft Edge, ocorre uma das seguintes ações.

*   Se a guia IE ativa não tiver conteúdo anterior, ela será fechada.  
*   Se a guia do IE ativo tiver conteúdo anterior, ela navegará até a página de suporte da Microsoft que explica por que o site foi [redirecionado para o Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].  

> [!NOTE]
> Após um redirecionamento, os usuários podem continuar a usar o IE para sites que não estão na lista de compatibilidade do IE.  

## <a name="request-an-update-to-the-ie-compatibility-list"></a>Solicitar uma atualização para a lista de compatibilidade do IE  

A lista de compatibilidade do IE é um arquivo XML no [microsoft.com][MicrosoftOfficialHome].  A lista é atualizada regularmente em resposta a solicitações de desenvolvedores de sites e usuários para que os sites tenham sido adicionados ou removidos.  As atualizações da lista são baixadas automaticamente para máquinas de usuário.  

Envie as informações a seguir [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que seu site seja adicionado ou removido da lista de compatibilidade do IE.    

*   Nome do proprietário  
*   Título corporativo  
*   Email  
*   Nome da empresa  
*   Rua  
*   Endereço do site  
    
A lista de compatibilidade do IE é atualizada dentro de uma semana.

> [!NOTE]
> A lista de compatibilidade do IE foi projetada para funcionar somente com sites públicos.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Envie um email para ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Precisa do Microsoft Edge list v1 xml | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "O site que você estava tentando alcançar não funciona com o Internet Explorer | Microsoft Office Suporte"  
