---
description: Saiba mais sobre algumas dicas e truques úteis em relação às extensões do Microsoft Edge
title: Extensões-dicas e truques
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, extensões
ms.openlocfilehash: db15aa49649432a6c4400b4e6830501c40485a83
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561159"
---
# <span data-ttu-id="a70dc-104">Dicas e truques</span><span class="sxs-lookup"><span data-stu-id="a70dc-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="a70dc-105">Não importa se você está trabalhando em uma extensão do Microsoft Edge ou já publicou uma, as dicas e truques a seguir podem ser úteis.</span><span class="sxs-lookup"><span data-stu-id="a70dc-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>

## <span data-ttu-id="a70dc-106">Obter um link direto para sua extensão na Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="a70dc-106">Get a direct link to your extension in the Microsoft Store</span></span>
<span data-ttu-id="a70dc-107">No painel do centro de desenvolvimento do Windows, você pode encontrar um link direto para sua extensão na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a70dc-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span> <span data-ttu-id="a70dc-108">Esse link pode ser útil para publicidade e compartilhamento de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="a70dc-108">This link can be useful for advertising and sharing out your extension.</span></span>


<span data-ttu-id="a70dc-109">Depois de fazer logon no centro de desenvolvimento do Windows e navegar para sua extensão por meio do painel, na página identidade do aplicativo, você encontrará o link na linha do **link do protocolo da loja** :</span><span class="sxs-lookup"><span data-stu-id="a70dc-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>

![link do protocolo da loja](./media/store-link.png)
 
## <span data-ttu-id="a70dc-111">Verifique se você está acompanhando a política da Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="a70dc-111">Make sure you’re following the Microsoft Store Policy</span></span>
<span data-ttu-id="a70dc-112">Ao criar sua extensão, certifique-se de ter em mente as diretrizes para enviar para a Microsoft Store realçada na [política da Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span><span class="sxs-lookup"><span data-stu-id="a70dc-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span></span> 
 
<span data-ttu-id="a70dc-113">O Microsoft Edge Extensions também tem um conjunto de políticas adicional para acompanhar [aqui](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span><span class="sxs-lookup"><span data-stu-id="a70dc-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span>

## <span data-ttu-id="a70dc-114">Melhorar a capacidade de descoberta da extensão na Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="a70dc-114">Improve your extension’s discoverability in the Microsoft Store</span></span>

<span data-ttu-id="a70dc-115">Você pode adicionar palavras-chave ao envio de extensão para imporove sua capacidade de descoberta pelas pesquisas.</span><span class="sxs-lookup"><span data-stu-id="a70dc-115">You can add keywords to your extension submission to imporove its discoverability through searches.</span></span> <span data-ttu-id="a70dc-116">Por exemplo, "extensões Microsoft Edge" e "nome da minha extensão".</span><span class="sxs-lookup"><span data-stu-id="a70dc-116">For example, "Microsoft Edge Extensions" and "name of my extension".</span></span> 

<span data-ttu-id="a70dc-117">Isso pode ser feito no centro de desenvolvimento do Windows na seção Descrição da extensão.</span><span class="sxs-lookup"><span data-stu-id="a70dc-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span> <span data-ttu-id="a70dc-118">Essas palavras-chave precisarão ser adicionadas para cada idioma ao qual a extensão for compatível.</span><span class="sxs-lookup"><span data-stu-id="a70dc-118">These keywords will need to be added for every language your extension supports.</span></span>

![Enviar uma resposta a uma crítica](./media/keywords.png)

## <span data-ttu-id="a70dc-120">Automatizar o envio para a Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="a70dc-120">Automate your submission to the Microsoft Store</span></span>
<span data-ttu-id="a70dc-121">Você pode automatizar e simplificar seus envios para a Microsoft Store usando a nova API de envio da Microsoft Store, que permite atualizar aplicativos/jogos, Complementos (compras no aplicativo) e pacotes de pré-lançamento por meio de uma API REST.</span><span class="sxs-lookup"><span data-stu-id="a70dc-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons (in-app purchases), and package flights through a REST API.</span></span> <span data-ttu-id="a70dc-122">Confira a [documentação e os exemplos](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) ou use a [extensão do VSTS da API de envio](https://github.com/Microsoft/windows-dev-center-vsts-extension) do código-fonte aberto para começar.</span><span class="sxs-lookup"><span data-stu-id="a70dc-122">Check out the [documentation and samples](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>

## <span data-ttu-id="a70dc-123">Usar o Hub de feedback do Windows para reunir comentários/análises/solicitações de recursos</span><span class="sxs-lookup"><span data-stu-id="a70dc-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>

<span data-ttu-id="a70dc-124">Você pode direcionar os usuários para a subcategoria do hub de feedback do Windows para sua extensão inserindo um link que aponta para ele.</span><span class="sxs-lookup"><span data-stu-id="a70dc-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span> <span data-ttu-id="a70dc-125">Será necessário criar esse link usando o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a70dc-125">This link will need to be created using the following format:</span></span> 

`feedback-hub://?tabid=2&appid=<PFN>!App`

<span data-ttu-id="a70dc-126">Você precisará substituir `<PFN>` pelo nome da família de pacotes pela extensão.</span><span class="sxs-lookup"><span data-stu-id="a70dc-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span> <span data-ttu-id="a70dc-127">Isso pode ser encontrado na seção **identidade do aplicativo** para sua extensão no centro de desenvolvimento do Windows.</span><span class="sxs-lookup"><span data-stu-id="a70dc-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>

## <span data-ttu-id="a70dc-128">Confira suas classificações e avaliações</span><span class="sxs-lookup"><span data-stu-id="a70dc-128">Check out your ratings and reviews</span></span>
<span data-ttu-id="a70dc-129">Faça logon regularmente para verificar suas análises e classificações de usuários.</span><span class="sxs-lookup"><span data-stu-id="a70dc-129">Log in regularly to check your user reviews and ratings.</span></span> <span data-ttu-id="a70dc-130">Embora o aplicativo UWP só tenha informações sobre o mercado atual do usuário, fazer logon no centro de desenvolvimento do Windows exibirá a classificação média em todos os mercados.</span><span class="sxs-lookup"><span data-stu-id="a70dc-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>

## <span data-ttu-id="a70dc-131">Responder às críticas do usuário</span><span class="sxs-lookup"><span data-stu-id="a70dc-131">Respond to user reviews</span></span>
<span data-ttu-id="a70dc-132">Você pode responder às críticas do usuário na Microsoft Store por meio do painel do centro de desenvolvimento do Windows.</span><span class="sxs-lookup"><span data-stu-id="a70dc-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span> <span data-ttu-id="a70dc-133">Navegue até sua extensão e em análises selecione **análises**.</span><span class="sxs-lookup"><span data-stu-id="a70dc-133">Navigate to your extension and under Analytics select **Reviews**.</span></span> <span data-ttu-id="a70dc-134">Um link será exibido abaixo de cada revisão que permitirá que você responda diretamente ao cliente.</span><span class="sxs-lookup"><span data-stu-id="a70dc-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span> <span data-ttu-id="a70dc-135">Este canal de comunicação permite que você ofereça feedback, resoluções ou envie um agradecimento para a revisão!</span><span class="sxs-lookup"><span data-stu-id="a70dc-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>

![Enviar uma resposta a uma crítica](./media/reviews.png)
