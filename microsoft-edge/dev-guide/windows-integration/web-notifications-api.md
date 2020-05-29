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
# <span data-ttu-id="f1e89-104">API de notificações da Web</span><span class="sxs-lookup"><span data-stu-id="f1e89-104">Web Notifications API</span></span>

<span data-ttu-id="f1e89-105">A API de notificações da Web permite que os sites enviem notificações de usuários fora do contexto de uma página da Web dentro do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f1e89-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span> <span data-ttu-id="f1e89-106">Um exemplo desse recurso em ação seria com um aplicativo de mensagens como o Skype.</span><span class="sxs-lookup"><span data-stu-id="f1e89-106">An example of this feature in action would be with a messaging application like Skype.</span></span> <span data-ttu-id="f1e89-107">Quando um usuário receber uma nova mensagem, uma notificação apareceria na área de trabalho, alertando-a sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f1e89-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span> <span data-ttu-id="f1e89-108">As notificações da Web são totalmente integradas à plataforma de notificação e à central de ações no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f1e89-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span> 

## <span data-ttu-id="f1e89-109">Criando uma notificação</span><span class="sxs-lookup"><span data-stu-id="f1e89-109">Creating a notification</span></span>

<span data-ttu-id="f1e89-110">A CodePen abaixo cria uma notificação de imitação do Skype, criando um [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto com o [`title`](https://msdn.microsoft.com/library/mt710826) [`icon`](https://msdn.microsoft.com/library/mt710814) conjunto de opções, e [`body`](https://msdn.microsoft.com/library/mt710811) .</span><span class="sxs-lookup"><span data-stu-id="f1e89-110">The CodePen below creates a mock Skype notification by making a [`Notification`](https://msdn.microsoft.com/library/mt710818) object with the [`title`](https://msdn.microsoft.com/library/mt710826), [`icon`](https://msdn.microsoft.com/library/mt710814), and [`body`](https://msdn.microsoft.com/library/mt710811) options set:</span></span>


<iframe height='295' scrolling='no' title='<span data-ttu-id="f1e89-111">Notificações da Web</span><span class="sxs-lookup"><span data-stu-id="f1e89-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="f1e89-112">Consulte as <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificações da Web da caneta </a> por documentos do Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="f1e89-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>
</iframe>

<span data-ttu-id="f1e89-113">É altamente recomendável que `icon` seja especificado para cada notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-113">It is strongly recommended that an `icon` be specified for each notification.</span></span> <span data-ttu-id="f1e89-114">Isso não apenas melhora uma notificação de um ponto de vista da interface do usuário, mas também ajuda a alertar os usuários de onde a notificação está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="f1e89-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>

<span data-ttu-id="f1e89-115">Assista ao vídeo abaixo para obter instruções passo a passo sobre a criação de uma notificação da Web e para ver isso é o comportamento no Windows 10!</span><span class="sxs-lookup"><span data-stu-id="f1e89-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### <span data-ttu-id="f1e89-116">Propriedades da notificação</span><span class="sxs-lookup"><span data-stu-id="f1e89-116">Notification properties</span></span>

<span data-ttu-id="f1e89-117">As notificações podem ser definidas com as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="f1e89-117">Notifications can be set with the following options:</span></span>

<span data-ttu-id="f1e89-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f1e89-118">Property</span></span> | <span data-ttu-id="f1e89-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1e89-119">Description</span></span>
:-------- | :----------
[<span data-ttu-id="f1e89-120">body</span><span class="sxs-lookup"><span data-stu-id="f1e89-120">body</span></span>](https://msdn.microsoft.com/library/mt710811) | <span data-ttu-id="f1e89-121">O corpo do texto da notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-121">The body text of the notification.</span></span>
[<span data-ttu-id="f1e89-122">dir</span><span class="sxs-lookup"><span data-stu-id="f1e89-122">dir</span></span>](https://msdn.microsoft.com/library/mt710813) | <span data-ttu-id="f1e89-123">A direção do texto da notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-123">The direction of the notification's text.</span></span>
[<span data-ttu-id="f1e89-124">icon</span><span class="sxs-lookup"><span data-stu-id="f1e89-124">icon</span></span>](https://msdn.microsoft.com/library/mt710814) | <span data-ttu-id="f1e89-125">A URL da notificação que é usada para seu ícone.</span><span class="sxs-lookup"><span data-stu-id="f1e89-125">The notification's URL that is used for its icon.</span></span>
[<span data-ttu-id="f1e89-126">lang</span><span class="sxs-lookup"><span data-stu-id="f1e89-126">lang</span></span>](https://msdn.microsoft.com/library/mt710815) | <span data-ttu-id="f1e89-127">O idioma da notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-127">The language of the notification.</span></span>
[<span data-ttu-id="f1e89-128">permissão</span><span class="sxs-lookup"><span data-stu-id="f1e89-128">permission</span></span>](https://msdn.microsoft.com/library/mt670637) | <span data-ttu-id="f1e89-129">A permissão de exibição de notificação atual que o usuário concedeu para a origem atual.</span><span class="sxs-lookup"><span data-stu-id="f1e89-129">The current notification display permission the user has granted for the current origin.</span></span>
[<span data-ttu-id="f1e89-130">tag</span><span class="sxs-lookup"><span data-stu-id="f1e89-130">tag</span></span>](https://msdn.microsoft.com/library/mt710825) | <span data-ttu-id="f1e89-131">A marca da notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-131">The tag of the notification.</span></span>
[<span data-ttu-id="f1e89-132">title</span><span class="sxs-lookup"><span data-stu-id="f1e89-132">title</span></span>](https://msdn.microsoft.com/library/mt710826) | <span data-ttu-id="f1e89-133">O título da notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-133">The title of the notification.</span></span>

### <span data-ttu-id="f1e89-134">Eventos de notificação</span><span class="sxs-lookup"><span data-stu-id="f1e89-134">Notification events</span></span>

<span data-ttu-id="f1e89-135">Os eventos a seguir são usados com o [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:</span><span class="sxs-lookup"><span data-stu-id="f1e89-135">The following events are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="f1e89-136">Evento</span><span class="sxs-lookup"><span data-stu-id="f1e89-136">Event</span></span> | <span data-ttu-id="f1e89-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1e89-137">Description</span></span>
:-------- | :----------
[<span data-ttu-id="f1e89-138">OnClick</span><span class="sxs-lookup"><span data-stu-id="f1e89-138">onclick</span></span>](https://msdn.microsoft.com/library/mt712180) | <span data-ttu-id="f1e89-139">Acionado quando uma notificação é clicada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f1e89-139">Fires when a notification is clicked by the user.</span></span>
[<span data-ttu-id="f1e89-140">onclose</span><span class="sxs-lookup"><span data-stu-id="f1e89-140">onclose</span></span>](https://msdn.microsoft.com/library/mt712178) | <span data-ttu-id="f1e89-141">Acionado quando uma notificação é fechada pelo usuário ou um tempo limite automático.</span><span class="sxs-lookup"><span data-stu-id="f1e89-141">Fires when a notification is closed by the user or an auto timeout.</span></span>
[<span data-ttu-id="f1e89-142">AoOcorrerErro</span><span class="sxs-lookup"><span data-stu-id="f1e89-142">onerror</span></span>](https://msdn.microsoft.com/library/mt712181) | <span data-ttu-id="f1e89-143">Acionado quando ocorre um erro durante a manipulação de uma notificação.</span><span class="sxs-lookup"><span data-stu-id="f1e89-143">Fires when an error occurs while handling a notification.</span></span>
[<span data-ttu-id="f1e89-144">OnShow</span><span class="sxs-lookup"><span data-stu-id="f1e89-144">onshow</span></span>](https://msdn.microsoft.com/library/mt712182) | <span data-ttu-id="f1e89-145">Acionado quando uma notificação é exibida.</span><span class="sxs-lookup"><span data-stu-id="f1e89-145">Fires when a notification is displayed.</span></span>

### <span data-ttu-id="f1e89-146">Métodos de notificação</span><span class="sxs-lookup"><span data-stu-id="f1e89-146">Notification methods</span></span>

<span data-ttu-id="f1e89-147">Os métodos a seguir são usados com o [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:</span><span class="sxs-lookup"><span data-stu-id="f1e89-147">The following methods are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="f1e89-148">Método</span><span class="sxs-lookup"><span data-stu-id="f1e89-148">Method</span></span> | <span data-ttu-id="f1e89-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1e89-149">Description</span></span>
:-------- | :----------
[<span data-ttu-id="f1e89-150">close</span><span class="sxs-lookup"><span data-stu-id="f1e89-150">close</span></span>](https://msdn.microsoft.com/library/mt670636) | <span data-ttu-id="f1e89-151">Fecha uma notificação exibida.</span><span class="sxs-lookup"><span data-stu-id="f1e89-151">Closes a displayed notification.</span></span>
[<span data-ttu-id="f1e89-152">requestPermission</span><span class="sxs-lookup"><span data-stu-id="f1e89-152">requestPermission</span></span>](https://msdn.microsoft.com/library/mt710824) | <span data-ttu-id="f1e89-153">Solicita permissão do usuário para permitir que as notificações sejam exibidas pela origem atual.</span><span class="sxs-lookup"><span data-stu-id="f1e89-153">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>

## <span data-ttu-id="f1e89-154">Permissões de notificação</span><span class="sxs-lookup"><span data-stu-id="f1e89-154">Notification permissions</span></span>

<span data-ttu-id="f1e89-155">O Microsoft Edge permite que os usuários gerenciem as permissões de notificações para cada domínio de site específico.</span><span class="sxs-lookup"><span data-stu-id="f1e89-155">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span> <span data-ttu-id="f1e89-156">O usuário pode selecionar "Sim" ou "não" quando solicitado pelo domínio para que ele mostre notificações.</span><span class="sxs-lookup"><span data-stu-id="f1e89-156">It's up to the user to either select "Yes" or "No" when asked by the domain to let it show notifications.</span></span> <span data-ttu-id="f1e89-157">O [`requestPermission`](https://msdn.microsoft.com/library/mt710824) método é usado para sinalizar o estado de permissão `granted` como `denied` ou, ou `default` .</span><span class="sxs-lookup"><span data-stu-id="f1e89-157">The [`requestPermission`](https://msdn.microsoft.com/library/mt710824) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span> <span data-ttu-id="f1e89-158">Um valor `default` indica que o usuário não fez uma decisão, que é vista como o equivalente de `denied` .</span><span class="sxs-lookup"><span data-stu-id="f1e89-158">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>




## <span data-ttu-id="f1e89-159">Referência de API</span><span class="sxs-lookup"><span data-stu-id="f1e89-159">API reference</span></span>

[<span data-ttu-id="f1e89-160">Notificações da Web</span><span class="sxs-lookup"><span data-stu-id="f1e89-160">Web Notifications</span></span>](https://msdn.microsoft.com/library/mt710827)

## <span data-ttu-id="f1e89-161">Especificada</span><span class="sxs-lookup"><span data-stu-id="f1e89-161">Specification</span></span>

[<span data-ttu-id="f1e89-162">Notificações da Web</span><span class="sxs-lookup"><span data-stu-id="f1e89-162">Web Notifications</span></span>](https://notifications.spec.whatwg.org)
