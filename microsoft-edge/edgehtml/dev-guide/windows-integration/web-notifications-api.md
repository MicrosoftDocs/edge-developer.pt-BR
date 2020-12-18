---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Saiba como a API de notificações da Web pode ser usada para permitir que os sites enviem notificações de usuários fora do contexto do navegador Microsoft Edge.
title: API de notificações da Web-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2be201a790c6fca1526c8b6eb13e4203e8e53206
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231718"
---
# API de Notificações Web  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

A API de notificações da Web permite que os sites enviem notificações de usuários fora do contexto de uma página da Web dentro do navegador Microsoft Edge.  Um exemplo desse recurso em ação seria com um aplicativo de mensagens como o Skype.  Quando um usuário receber uma nova mensagem, uma notificação apareceria na área de trabalho, alertando-a sobre a mensagem.  As notificações da Web são totalmente integradas à plataforma de notificação e à central de ações no Windows 10.  

## Criando uma notificação  

A CodePen abaixo cria uma notificação de imitação do Skype fazendo um objeto de [notificação](https://msdn.microsoft.com/library/mt710818) com o [título](https://msdn.microsoft.com/library/mt710826), o [ícone](https://msdn.microsoft.com/library/mt710814)e as opções de [corpo](https://msdn.microsoft.com/library/mt710811) definidas:  

<iframe height='295' scrolling='no' title='Notificações da Web' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulte as <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificações da Web da caneta </a> por documentos do Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>  

É altamente recomendável que um **ícone** seja especificado para cada notificação.  Isso não apenas melhora uma notificação de um ponto de vista da interface do usuário, mas também ajuda a alertar os usuários de onde a notificação está sendo enviada.  

Assista ao vídeo abaixo para obter instruções passo a passo sobre a criação de uma notificação da Web e para ver isso é o comportamento no Windows 10!  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### Propriedades da notificação  

As notificações podem ser definidas com as seguintes propriedades:  

:::row:::
   :::column span="1":::
      [body](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      O corpo do texto da notificação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [dir](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      A direção do texto da notificação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [icon](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      A URL da notificação que é usada para seu ícone.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [lang](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      O idioma da notificação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [permissão](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      A permissão de exibição de notificação atual que o usuário concedeu para a origem atual.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [tag](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      A marca da notificação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [title](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      O título da notificação.  
   :::column-end:::
:::row-end:::  

### Eventos de notificação  

Os eventos a seguir são usados com o objeto [Notification](https://developer.mozilla.org/docs/Web/API/Notification) :  

:::row:::
   :::column span="1":::
      [OnClick](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      Acionado quando uma notificação é clicada pelo usuário.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onclose](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      Acionado quando uma notificação é fechada pelo usuário ou um tempo limite automático.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [AoOcorrerErro](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      Acionado quando ocorre um erro durante a manipulação de uma notificação.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [OnShow](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      Acionado quando uma notificação é exibida.  
   :::column-end:::
:::row-end:::  

### Métodos de notificação  

Os métodos a seguir são usados com o objeto [Notification](https://developer.mozilla.org/docs/Web/API/Notification) :  

:::row:::
   :::column span="1":::
      [close](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      Fecha uma notificação exibida.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      Solicita permissão do usuário para permitir que as notificações sejam exibidas pela origem atual.  
   :::column-end:::
:::row-end:::  

## Permissões de notificação  

O Microsoft Edge permite que os usuários gerenciem as permissões de notificações para cada domínio de site específico.  O usuário pode selecionar **Sim** ou **não** quando solicitado pelo domínio para que ele mostre notificações.  O método [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) é usado para sinalizar o estado de permissão `granted` como `denied` ou, ou `default` .  Um valor `default` indica que o usuário não fez uma decisão, que é vista como o equivalente de `denied` .  

## Referência de API  

[Notificações da Web](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## Especificada  

[Notificações da Web](https://notifications.spec.whatwg.org)  
