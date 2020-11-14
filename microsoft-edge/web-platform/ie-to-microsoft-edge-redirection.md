---
description: Mover usuários para o Microsoft Edge do Internet Explorer
title: Mover usuários para o Microsoft Edge do Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web, Internet Explorer
ms.openlocfilehash: 872bd5ec52f471e4958ef7354c046ec30f1ba72e
ms.sourcegitcommit: 62258ce0ef469948ca8af42141d02aa9719243f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168356"
---
# Mover usuários para o Microsoft Edge do Internet Explorer  

Muitos sites modernos têm designs que são incompatíveis com o Internet Explorer \ (IE \).  Quando um usuário do IE visita um site público incompatível, o usuário pode receber uma mensagem.  A mensagem informa que o site é incompatível com o navegador.  Depois que a mensagem é exibida, o usuário deve alternar manualmente para um navegador moderno.  Para minimizar as interrupções, começando com a versão 84, o Microsoft Edge aceita uma nova funcionalidade que redireciona os usuários automaticamente.  Quando um usuário do IE navega para um site que é incompatível com o IE, o Windows redireciona automaticamente o usuário para o Microsoft Edge.  Para revisar os sites na lista, navegue até a [lista necessária do Microsoft Edge][MicrosoftEdgeNeededgeV1].

Este artigo descreve os conceitos a seguir.  

*   Por que um site é adicionado à lista  
*   A experiência do usuário para redirecionamento  
*   Solicitar uma atualização para a lista  
    
## Por que um site foi adicionado à lista de compatibilidade do IE?  

A lista de compatibilidade do IE adiciona apenas um site quando as seguintes ações ocorrem.  

*   Mostra um usuário do IE que uma mensagem sugerindo o usuário deve usar um navegador diferente por motivos de compatibilidade.  
*   As solicitações de proprietário para adicionar o site à lista de compatibilidade do IE.  

## Experiência de redirecionamento

No redirecionamento para o Microsoft Edge, o usuário é mostrado na caixa de diálogo única na próxima captura de tela.  A caixa de diálogo fornece ao usuário as informações a seguir.  

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
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notificação de navegação e solicitação para importar dados e preferências" lightbox="../media/neededge-dialog1.msft.png":::
         Notificação de navegação e solicitação para importar dados e preferências  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Se o usuário não consentir, escolha a caixa de seleção **sempre trazer os meus dados de navegação e preferências do Internet Explorer** , o usuário pode escolher **continuar navegando**   para continuar a sessão de navegação.  

Por fim, uma faixa de incompatibilidade de site é exibida na barra de endereços para cada redirecionamento.  Um exemplo de uma faixa de incompatibilidade de site é exibido na figura a seguir.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificação sobre sites modernos e solicitação para definir o Microsoft Edge como navegador padrão ou explorar o Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Notificação sobre sites modernos e solicitação para definir o Microsoft Edge como navegador padrão ou explorar o Microsoft Edge  
:::image-end:::

A faixa de incompatibilidade do site fornece os seguintes detalhes para o usuário.  

*   Recomenda que o usuário alterne para o Microsoft Edge.  
*   Oferece para definir o Microsoft Edge como o navegador padrão.  
*   Oferece ao usuário a opção de explorar o Microsoft Edge.    
    
Quando um site é redirecionado do Internet Explorer para o Microsoft Edge, uma das ações a seguir ocorre.

*   Se a guia ativa do IE não tiver conteúdo anterior, será fechada.  
*   Se a guia ativa do IE tinha conteúdo anterior, ele navega para a [página de suporte da Microsoft que explica por que o site foi redirecionado para o Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].  

> [!NOTE]
> Após um redirecionamento, os usuários podem continuar a usar o IE para sites que não estão na lista de compatibilidade do IE.  

## Solicitar uma atualização para a lista de compatibilidade do IE  

A lista de compatibilidade do IE é um arquivo XML no [Microsoft.com][MicrosoftOfficialHome].  A lista é atualizada regularmente em resposta a solicitações de desenvolvedor de usuário e de site para que os sites sejam adicionados ou removidos.  As atualizações da lista são baixadas automaticamente para computadores dos usuários.  

Envie por email as informações a seguir para [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que o seu site seja adicionado ou removido da lista de compatibilidade do IE.    

*   Nome do proprietário  
*   Título corporativo  
*   Email  
*   Nome da empresa  
*   Rua  
*   Endereço do site  
    
> [!NOTE]
> A lista de compatibilidade do IE foi projetada para funcionar somente com sites públicos.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar um email para ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Microsoft Official Home"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "É preciso ter o Microsoft Edge List v1 XML | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "O site que você estava tentando contactar não funciona com o Internet Explorer | Suporte do Microsoft Office"  
