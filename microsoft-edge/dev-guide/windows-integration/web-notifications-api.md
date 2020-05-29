---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Saiba como a API de notificações da Web pode ser usada para permitir que os sites enviem notificações de usuários fora do contexto do navegador Microsoft Edge.
title: Guia de desenvolvimento-API de notificações da Web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560904"
---
# API de notificações da Web

A API de notificações da Web permite que os sites enviem notificações de usuários fora do contexto de uma página da Web dentro do navegador Microsoft Edge. Um exemplo desse recurso em ação seria com um aplicativo de mensagens como o Skype. Quando um usuário receber uma nova mensagem, uma notificação apareceria na área de trabalho, alertando-a sobre a mensagem. As notificações da Web são totalmente integradas à plataforma de notificação e à central de ações no Windows 10. 

## Criando uma notificação

A CodePen abaixo cria uma notificação de imitação do Skype, criando um [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto com o [`title`](https://msdn.microsoft.com/library/mt710826) [`icon`](https://msdn.microsoft.com/library/mt710814) conjunto de opções, e [`body`](https://msdn.microsoft.com/library/mt710811) .


<iframe height='295' scrolling='no' title='Notificações da Web' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulte as <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificações da Web da caneta </a> por documentos do Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='https://codepen.io'> CodePen </a> .
</iframe>

É altamente recomendável que `icon` seja especificado para cada notificação. Isso não apenas melhora uma notificação de um ponto de vista da interface do usuário, mas também ajuda a alertar os usuários de onde a notificação está sendo enviada.

Assista ao vídeo abaixo para obter instruções passo a passo sobre a criação de uma notificação da Web e para ver isso é o comportamento no Windows 10!


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### Propriedades da notificação

As notificações podem ser definidas com as seguintes opções:

Propriedade | Descrição
:-------- | :----------
[body](https://msdn.microsoft.com/library/mt710811) | O corpo do texto da notificação.
[dir](https://msdn.microsoft.com/library/mt710813) | A direção do texto da notificação.
[icon](https://msdn.microsoft.com/library/mt710814) | A URL da notificação que é usada para seu ícone.
[lang](https://msdn.microsoft.com/library/mt710815) | O idioma da notificação.
[permissão](https://msdn.microsoft.com/library/mt670637) | A permissão de exibição de notificação atual que o usuário concedeu para a origem atual.
[tag](https://msdn.microsoft.com/library/mt710825) | A marca da notificação.
[title](https://msdn.microsoft.com/library/mt710826) | O título da notificação.

### Eventos de notificação

Os eventos a seguir são usados com o [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:

Evento | Descrição
:-------- | :----------
[OnClick](https://msdn.microsoft.com/library/mt712180) | Acionado quando uma notificação é clicada pelo usuário.
[onclose](https://msdn.microsoft.com/library/mt712178) | Acionado quando uma notificação é fechada pelo usuário ou um tempo limite automático.
[AoOcorrerErro](https://msdn.microsoft.com/library/mt712181) | Acionado quando ocorre um erro durante a manipulação de uma notificação.
[OnShow](https://msdn.microsoft.com/library/mt712182) | Acionado quando uma notificação é exibida.

### Métodos de notificação

Os métodos a seguir são usados com o [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:

Método | Descrição
:-------- | :----------
[close](https://msdn.microsoft.com/library/mt670636) | Fecha uma notificação exibida.
[requestPermission](https://msdn.microsoft.com/library/mt710824) | Solicita permissão do usuário para permitir que as notificações sejam exibidas pela origem atual.

## Permissões de notificação

O Microsoft Edge permite que os usuários gerenciem as permissões de notificações para cada domínio de site específico. O usuário pode selecionar "Sim" ou "não" quando solicitado pelo domínio para que ele mostre notificações. O [`requestPermission`](https://msdn.microsoft.com/library/mt710824) método é usado para sinalizar o estado de permissão `granted` como `denied` ou, ou `default` . Um valor `default` indica que o usuário não fez uma decisão, que é vista como o equivalente de `denied` .




## Referência de API

[Notificações da Web](https://msdn.microsoft.com/library/mt710827)

## Especificada

[Notificações da Web](https://notifications.spec.whatwg.org)
