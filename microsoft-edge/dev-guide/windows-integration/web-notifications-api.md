---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Saiba como a API de notificações da Web pode ser usada para permitir que os sites enviem notificações de usuários fora do contexto do navegador Microsoft Edge.
title: API de notificações da Web-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 24b8a7b25fb3e0f0221f6d81b105d5d0374ea423
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941805"
---
# <span data-ttu-id="4ba72-104">API de Notificações Web</span><span class="sxs-lookup"><span data-stu-id="4ba72-104">Web Notifications API</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="4ba72-105">A API de notificações da Web permite que os sites enviem notificações de usuários fora do contexto de uma página da Web dentro do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4ba72-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span>  <span data-ttu-id="4ba72-106">Um exemplo desse recurso em ação seria com um aplicativo de mensagens como o Skype.</span><span class="sxs-lookup"><span data-stu-id="4ba72-106">An example of this feature in action would be with a messaging application like Skype.</span></span>  <span data-ttu-id="4ba72-107">Quando um usuário receber uma nova mensagem, uma notificação apareceria na área de trabalho, alertando-a sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4ba72-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span>  <span data-ttu-id="4ba72-108">As notificações da Web são totalmente integradas à plataforma de notificação e à central de ações no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ba72-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span>  

## <span data-ttu-id="4ba72-109">Criando uma notificação</span><span class="sxs-lookup"><span data-stu-id="4ba72-109">Creating a notification</span></span>  

<span data-ttu-id="4ba72-110">A CodePen abaixo cria uma notificação de imitação do Skype fazendo um objeto de [notificação](https://msdn.microsoft.com/library/mt710818) com o [título](https://msdn.microsoft.com/library/mt710826), o [ícone](https://msdn.microsoft.com/library/mt710814)e as opções de [corpo](https://msdn.microsoft.com/library/mt710811) definidas:</span><span class="sxs-lookup"><span data-stu-id="4ba72-110">The CodePen below creates a mock Skype notification by making a [Notification](https://msdn.microsoft.com/library/mt710818) object with the [title](https://msdn.microsoft.com/library/mt710826), [icon](https://msdn.microsoft.com/library/mt710814), and [body](https://msdn.microsoft.com/library/mt710811) options set:</span></span>  

<iframe height='295' scrolling='no' title='<span data-ttu-id="4ba72-111">Notificações da Web</span><span class="sxs-lookup"><span data-stu-id="4ba72-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="4ba72-112">Consulte as <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificações da Web da caneta </a> por documentos do Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="4ba72-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

<span data-ttu-id="4ba72-113">É altamente recomendável que um **ícone** seja especificado para cada notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-113">It is strongly recommended that an **icon** be specified for each notification.</span></span>  <span data-ttu-id="4ba72-114">Isso não apenas melhora uma notificação de um ponto de vista da interface do usuário, mas também ajuda a alertar os usuários de onde a notificação está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="4ba72-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>  

<span data-ttu-id="4ba72-115">Assista ao vídeo abaixo para obter instruções passo a passo sobre a criação de uma notificação da Web e para ver isso é o comportamento no Windows 10!</span><span class="sxs-lookup"><span data-stu-id="4ba72-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### <span data-ttu-id="4ba72-116">Propriedades da notificação</span><span class="sxs-lookup"><span data-stu-id="4ba72-116">Notification properties</span></span>  

<span data-ttu-id="4ba72-117">As notificações podem ser definidas com as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="4ba72-117">Notifications can be set with the following properties:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-118">body</span><span class="sxs-lookup"><span data-stu-id="4ba72-118">body</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-119">O corpo do texto da notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-119">The body text of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-120">dir</span><span class="sxs-lookup"><span data-stu-id="4ba72-120">dir</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-121">A direção do texto da notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-121">The direction of the notification's text.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-122">icon</span><span class="sxs-lookup"><span data-stu-id="4ba72-122">icon</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-123">A URL da notificação que é usada para seu ícone.</span><span class="sxs-lookup"><span data-stu-id="4ba72-123">The notification's URL that is used for its icon.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-124">lang</span><span class="sxs-lookup"><span data-stu-id="4ba72-124">lang</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-125">O idioma da notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-125">The language of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-126">permissão</span><span class="sxs-lookup"><span data-stu-id="4ba72-126">permission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-127">A permissão de exibição de notificação atual que o usuário concedeu para a origem atual.</span><span class="sxs-lookup"><span data-stu-id="4ba72-127">The current notification display permission the user has granted for the current origin.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-128">tag</span><span class="sxs-lookup"><span data-stu-id="4ba72-128">tag</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-129">A marca da notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-129">The tag of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-130">title</span><span class="sxs-lookup"><span data-stu-id="4ba72-130">title</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-131">O título da notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-131">The title of the notification.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="4ba72-132">Eventos de notificação</span><span class="sxs-lookup"><span data-stu-id="4ba72-132">Notification events</span></span>  

<span data-ttu-id="4ba72-133">Os eventos a seguir são usados com o objeto [Notification](https://developer.mozilla.org/docs/Web/API/Notification) :</span><span class="sxs-lookup"><span data-stu-id="4ba72-133">The following events are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-134">OnClick</span><span class="sxs-lookup"><span data-stu-id="4ba72-134">onclick</span></span>](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-135">Acionado quando uma notificação é clicada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4ba72-135">Fires when a notification is clicked by the user.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-136">onclose</span><span class="sxs-lookup"><span data-stu-id="4ba72-136">onclose</span></span>](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-137">Acionado quando uma notificação é fechada pelo usuário ou um tempo limite automático.</span><span class="sxs-lookup"><span data-stu-id="4ba72-137">Fires when a notification is closed by the user or an auto timeout.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-138">AoOcorrerErro</span><span class="sxs-lookup"><span data-stu-id="4ba72-138">onerror</span></span>](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-139">Acionado quando ocorre um erro durante a manipulação de uma notificação.</span><span class="sxs-lookup"><span data-stu-id="4ba72-139">Fires when an error occurs while handling a notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-140">OnShow</span><span class="sxs-lookup"><span data-stu-id="4ba72-140">onshow</span></span>](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-141">Acionado quando uma notificação é exibida.</span><span class="sxs-lookup"><span data-stu-id="4ba72-141">Fires when a notification is displayed.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="4ba72-142">Métodos de notificação</span><span class="sxs-lookup"><span data-stu-id="4ba72-142">Notification methods</span></span>  

<span data-ttu-id="4ba72-143">Os métodos a seguir são usados com o objeto [Notification](https://developer.mozilla.org/docs/Web/API/Notification) :</span><span class="sxs-lookup"><span data-stu-id="4ba72-143">The following methods are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-144">close</span><span class="sxs-lookup"><span data-stu-id="4ba72-144">close</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-145">Fecha uma notificação exibida.</span><span class="sxs-lookup"><span data-stu-id="4ba72-145">Closes a displayed notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="4ba72-146">requestPermission</span><span class="sxs-lookup"><span data-stu-id="4ba72-146">requestPermission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ba72-147">Solicita permissão do usuário para permitir que as notificações sejam exibidas pela origem atual.</span><span class="sxs-lookup"><span data-stu-id="4ba72-147">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="4ba72-148">Permissões de notificação</span><span class="sxs-lookup"><span data-stu-id="4ba72-148">Notification permissions</span></span>  

<span data-ttu-id="4ba72-149">O Microsoft Edge permite que os usuários gerenciem as permissões de notificações para cada domínio de site específico.</span><span class="sxs-lookup"><span data-stu-id="4ba72-149">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span>  <span data-ttu-id="4ba72-150">O usuário pode selecionar **Sim** ou **não** quando solicitado pelo domínio para que ele mostre notificações.</span><span class="sxs-lookup"><span data-stu-id="4ba72-150">It's up to the user to either select **Yes** or **No** when asked by the domain to let it show notifications.</span></span>  <span data-ttu-id="4ba72-151">O método [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) é usado para sinalizar o estado de permissão `granted` como `denied` ou, ou `default` .</span><span class="sxs-lookup"><span data-stu-id="4ba72-151">The [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span>  <span data-ttu-id="4ba72-152">Um valor `default` indica que o usuário não fez uma decisão, que é vista como o equivalente de `denied` .</span><span class="sxs-lookup"><span data-stu-id="4ba72-152">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>  

## <span data-ttu-id="4ba72-153">Referência de API</span><span class="sxs-lookup"><span data-stu-id="4ba72-153">API reference</span></span>  

[<span data-ttu-id="4ba72-154">Notificações da Web</span><span class="sxs-lookup"><span data-stu-id="4ba72-154">Web Notifications</span></span>](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## <span data-ttu-id="4ba72-155">Especificada</span><span class="sxs-lookup"><span data-stu-id="4ba72-155">Specification</span></span>  

[<span data-ttu-id="4ba72-156">Notificações da Web</span><span class="sxs-lookup"><span data-stu-id="4ba72-156">Web Notifications</span></span>](https://notifications.spec.whatwg.org)  
