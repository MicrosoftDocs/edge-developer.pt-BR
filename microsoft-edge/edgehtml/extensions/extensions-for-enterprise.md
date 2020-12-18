---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: Saiba mais sobre os aspectos específicos da empresa de extensões do Microsoft Edge e veja como eles são semelhantes aos aplicativos UWP.
title: Extensões para empresas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7c23bc24e20b7b00b8779f209dcac8c795067fd5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231939"
---
# <span data-ttu-id="0ff54-104">Extensões para empresas</span><span class="sxs-lookup"><span data-stu-id="0ff54-104">Extensions for Enterprise</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="0ff54-105">As extensões do Microsoft Edge têm um fluxo de trabalho semelhante quando comparadas a outros aplicativos UWP empresariais.</span><span class="sxs-lookup"><span data-stu-id="0ff54-105">Microsoft Edge extensions have a similar workflow when compared to other enterprise UWP apps.</span></span> <span data-ttu-id="0ff54-106">As informações abaixo detalham aspectos específicos da empresa de extensões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff54-106">The information below details enterprise specific aspects of Microsoft Edge extensions.</span></span>

## <span data-ttu-id="0ff54-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0ff54-107">Prerequisites</span></span>
<span data-ttu-id="0ff54-108">Os itens a seguir são sugeridos para desenvolver, empacotar e implantar uma extensão do Microsoft Edge para empresas:</span><span class="sxs-lookup"><span data-stu-id="0ff54-108">The following items are suggested to develop, package, and deploy a Microsoft Edge extension for enterprise:</span></span>

+ <span data-ttu-id="0ff54-109">Conta do portal do desenvolvedor do Windows, para assinar e liberar a extensão para a loja privada da empresa.</span><span class="sxs-lookup"><span data-stu-id="0ff54-109">Windows Developer Portal account, to sign and release the extension to the enterprise private store.</span></span> <span data-ttu-id="0ff54-110">Consulte [abrindo uma conta de desenvolvedor](/windows/uwp/publish/opening-a-developer-account) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0ff54-110">See [Opening a developer account](/windows/uwp/publish/opening-a-developer-account) for more details.</span></span>
+ <span data-ttu-id="0ff54-111">Microsoft Store para empresas ou instituições de ensino para distribuir o aplicativo para a empresa.</span><span class="sxs-lookup"><span data-stu-id="0ff54-111">Microsoft Store for Business or Education, to distribute the application to the enterprise.</span></span> <span data-ttu-id="0ff54-112">Confira a [documentação da Microsoft Store para empresas e educação](/microsoft-store/) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0ff54-112">See the [Microsoft Store for Business and Education documentation](/microsoft-store/) for more details.</span></span>
+ <span data-ttu-id="0ff54-113">Identifique quais versões do Windows 10 executarão a extensão do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff54-113">Identify which versions of Windows 10 will be running the Microsoft Edge extension.</span></span> <span data-ttu-id="0ff54-114">Veja [as informações de versão do Windows 10](https://www.microsoft.com/itpro/windows-10/release-information) para obter uma listagem de versões existentes do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0ff54-114">See [Windows 10 release information](https://www.microsoft.com/itpro/windows-10/release-information) for a listing of existing Windows 10 releases.</span></span>

> [!NOTE]
> <span data-ttu-id="0ff54-115">O Sideload pode ser considerado uma alternativa para usar o portal do desenvolvedor do Windows para assinar o lançamento da extensão.</span><span class="sxs-lookup"><span data-stu-id="0ff54-115">Sideloading can be considered an alternative to using the Windows Developer Portal to sign the release the extension.</span></span> <span data-ttu-id="0ff54-116">Consulte o comportamento das extensões de Sideload abaixo para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0ff54-116">See the behaviour of sideloading extensions below for more details.</span></span>

## <span data-ttu-id="0ff54-117">Proteção de Informações do Windows</span><span class="sxs-lookup"><span data-stu-id="0ff54-117">Windows Information Protection</span></span>
<span data-ttu-id="0ff54-118">Atualmente, as extensões do Microsoft Edge não obedecem às configurações de WIP (proteção de informações do Windows).</span><span class="sxs-lookup"><span data-stu-id="0ff54-118">Microsoft Edge extensions currently don't honor Windows Information Protection (WIP) settings.</span></span> <span data-ttu-id="0ff54-119">Se uma empresa se preocupa com a proteção de dados, o suporte a extensões não deve ser habilitado para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff54-119">If an enterprise is concerned about data protection, extensions support should not be enabled for Microsoft Edge.</span></span>

<span data-ttu-id="0ff54-120">Para desabilitar as extensões para funcionários, configure a política de grupo e as configurações do Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="0ff54-120">To disable extensions for employees, configure Group Policy and Microsoft Intune settings.</span></span> <span data-ttu-id="0ff54-121">Para obter mais informações sobre quais políticas configurar, consulte [políticas disponíveis para o Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).</span><span class="sxs-lookup"><span data-stu-id="0ff54-121">For more info on which policies to configure, see [Available policies for Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).</span></span>

## <span data-ttu-id="0ff54-122">Extensões de pacotes</span><span class="sxs-lookup"><span data-stu-id="0ff54-122">Packaging Extensions</span></span>
<span data-ttu-id="0ff54-123">Antes de uma empresa poder distribuir uma extensão a seus funcionários, ela deve primeiro ser empacotada.</span><span class="sxs-lookup"><span data-stu-id="0ff54-123">Before an enterprise can distribute an extension to its employees, it must first be packaged.</span></span> <span data-ttu-id="0ff54-124">Instruções sobre extensões de pacotes estão disponíveis no guia de [empacotamento](./guides/packaging.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff54-124">Instructions on packaging extensions are available in the [Packaging](./guides/packaging.md) guide.</span></span>

> [!TIP]
> <span data-ttu-id="0ff54-125">Certifique-se de testar a instalação e executar a extensão em todas as versões do Windows 10 para garantir que ela funcionará como esperado antes da distribuição.</span><span class="sxs-lookup"><span data-stu-id="0ff54-125">Be sure to test installing and running your extension on all the versions of Windows 10 to ensure it will work as expected before distributing.</span></span>

## <span data-ttu-id="0ff54-126">Distribuindo extensões</span><span class="sxs-lookup"><span data-stu-id="0ff54-126">Distributing Extensions</span></span>
<span data-ttu-id="0ff54-127">Após o empacotamento, ele pode ser distribuído aos funcionários por meio da Microsoft Store, da Microsoft Store para empresas ou do Sideload.</span><span class="sxs-lookup"><span data-stu-id="0ff54-127">Once an extension has been packaged, it can be distributed to employees through the Microsoft Store, Microsoft Store for Business, or by sideloading.</span></span>

<span data-ttu-id="0ff54-128">Extensões distribuídas por meio da Microsoft Store para empresas podem ser atribuídas a funcionários ou adicionadas a um armazenamento privado em que todos os funcionários possam acessá-los.</span><span class="sxs-lookup"><span data-stu-id="0ff54-128">Extensions distributed though the Microsoft Store for Business can either be assigned to employees, or added to a private store where all employees can access them.</span></span> <span data-ttu-id="0ff54-129">Isso pode ser feito seguindo o guia de [distribuição de aplicativos de linha de negócios (LOB) para empresas](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) .</span><span class="sxs-lookup"><span data-stu-id="0ff54-129">This can be done by following the [Distribute "Line-of-Business" (LOB) apps to enterprises](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) guide.</span></span>

<span data-ttu-id="0ff54-130">Para extensões Sideload, os dispositivos (não gerenciados ou gerenciados) devem ser desbloqueados para Sideload.</span><span class="sxs-lookup"><span data-stu-id="0ff54-130">To sideload extensions, devices (unmanaged or managed) must be unlocked for sideloading.</span></span> <span data-ttu-id="0ff54-131">Consulte [Sideload de aplicativos LOB no Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) para obter mais informações sobre como Sideload as extensões empacotadas.</span><span class="sxs-lookup"><span data-stu-id="0ff54-131">See [Sideload LOB apps in Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) for more info on how to sideload packaged extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ff54-132">Se a empresa estiver desenvolvendo e distribuindo a extensão internamente, a empresa exigirá a Microsoft Store para empresas (ou educação) e uma conta do portal do desenvolvedor do Windows.</span><span class="sxs-lookup"><span data-stu-id="0ff54-132">If the enterprise is both developing and distributing the extension internally, the enterprise will require both the Microsoft Store for Business (or Education) and a Windows Developer Portal account.</span></span>

### <span data-ttu-id="0ff54-133">Comportamento de extensões Sideload</span><span class="sxs-lookup"><span data-stu-id="0ff54-133">Behavior of Sideloaded Extensions</span></span>
<span data-ttu-id="0ff54-134">Diferentemente das extensões distribuídas pela Microsoft Store (ou da Microsoft Store para empresas), as extensões Sideload são tratadas de modo diferente no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0ff54-134">Unlike extensions distributed through the Microsoft Store (or the Microsoft Store for Business), sideloaded extensions are treated differently in Microsoft Edge.</span></span>

<span data-ttu-id="0ff54-135">A primeira diferença afeta como as extensões Sideload se comportam após a instalação.</span><span class="sxs-lookup"><span data-stu-id="0ff54-135">The first difference affects how sideloaded extensions behave after installation.</span></span> <span data-ttu-id="0ff54-136">Diferentemente das extensões da Microsoft Store, as extensões Sideload não exibem imediatamente a notificação "você tem uma nova extensão" e precisa ser ativada manualmente pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0ff54-136">Unlike extensions from the Microsoft Store, sideloaded extensions do not immediately display the "You have a new extension" notification and need to be manually turned on by the user.</span></span>

<span data-ttu-id="0ff54-137">Para ativar a extensão, abra o menu **mais (...)** , selecione **"extensões"** e você deve ver a extensão Sideload na lista de extensões instaladas.</span><span class="sxs-lookup"><span data-stu-id="0ff54-137">To turn on the extension, open the **More (...)** menu, select **"Extensions"** and you should see the sideloaded extension in the list of installed extensions.</span></span> <span data-ttu-id="0ff54-138">Clique na extensão e ative-a.</span><span class="sxs-lookup"><span data-stu-id="0ff54-138">Click on the extension and turn it on.</span></span>

<span data-ttu-id="0ff54-139">A segunda diferença afeta como as extensões Sideload são exibidas no navegador.</span><span class="sxs-lookup"><span data-stu-id="0ff54-139">The second difference affects how sideloaded extensions appear in the browser.</span></span> <span data-ttu-id="0ff54-140">Por exemplo, a notificação "você tem uma nova extensão" e a lista de extensões instaladas incluem um aviso adicional informando que a extensão é de uma fonte desconhecida.</span><span class="sxs-lookup"><span data-stu-id="0ff54-140">For example, both the "You have a new extension" notification and the list of installed extensions include an additional warning stating that the extension is from an unknown source.</span></span>

![aviso de Sideload 1](./media/sideload-permissionflyout.PNG)

![aviso de Sideload 2](./media/sideload-l1warning.PNG)

<span data-ttu-id="0ff54-143">A terceira e última diferença afetam como as extensões Sideload se comportam na inicialização do navegador.</span><span class="sxs-lookup"><span data-stu-id="0ff54-143">The third and final difference affects how sideloaded extensions behave on browser startup.</span></span> <span data-ttu-id="0ff54-144">As extensões do Sideload em dispositivos que fazem parte de um domínio ou MDM habilitadas se comportam como extensões da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0ff54-144">Sideloaded extensions on devices that are either domain-joined or MDM enabled will behave like extensions from the Microsoft Store.</span></span> <span data-ttu-id="0ff54-145">No entanto, as extensões do Sideload em dispositivos que não fazem parte do domínio ou MDM habilitado serão desativadas durante a inicialização do navegador e exigem que o usuário tome uma ação explícita.</span><span class="sxs-lookup"><span data-stu-id="0ff54-145">However, sideloaded extensions on devices that are not domain-joined or MDM enabled will be turned off during browser startup and require the user to take explicit action.</span></span>

<span data-ttu-id="0ff54-146">Logo após a inicialização do navegador (após cerca de 10 segundos de inatividade) a seguinte notificação será exibida próxima à parte inferior da janela.</span><span class="sxs-lookup"><span data-stu-id="0ff54-146">Shortly after browser startup (after ~10 seconds of inactivity) the following notification will appear near the bottom of the window.</span></span>

![notificação Sideload](./media/sideload-scareUI.PNG)

<span data-ttu-id="0ff54-148">Cada vez que o Microsoft Edge for iniciado, os usuários precisarão selecionar "ativar de qualquer maneira" para usar a extensão.</span><span class="sxs-lookup"><span data-stu-id="0ff54-148">Each time Microsoft Edge is launched, users will need to select "Turn on anyway" in order to use the extension.</span></span>
