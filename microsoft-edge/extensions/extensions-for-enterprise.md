---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: Saiba mais sobre os aspectos específicos da empresa de extensões do Microsoft Edge e veja como eles são semelhantes aos aplicativos UWP.
title: Extensões para empresas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.custom: seodec18
ms.openlocfilehash: 8f50c282fce11d2654f990bf135941e0616af3f3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561253"
---
# Extensões para empresas  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

As extensões do Microsoft Edge têm um fluxo de trabalho semelhante quando comparadas a outros aplicativos UWP empresariais. As informações abaixo detalham aspectos específicos da empresa de extensões do Microsoft Edge.

## Pré-requisitos
Os itens a seguir são sugeridos para desenvolver, empacotar e implantar uma extensão do Microsoft Edge para empresas:

+ Conta do portal do desenvolvedor do Windows, para assinar e liberar a extensão para a loja privada da empresa. Consulte [abrindo uma conta de desenvolvedor](/windows/uwp/publish/opening-a-developer-account) para obter mais detalhes.
+ Microsoft Store para empresas ou instituições de ensino para distribuir o aplicativo para a empresa. Confira a [documentação da Microsoft Store para empresas e educação](/microsoft-store/) para obter mais detalhes.
+ Identifique quais versões do Windows 10 executarão a extensão do Microsoft Edge. Veja [as informações de versão do Windows 10](https://www.microsoft.com/itpro/windows-10/release-information) para obter uma listagem de versões existentes do Windows 10.

> [!NOTE]
> O Sideload pode ser considerado uma alternativa para usar o portal do desenvolvedor do Windows para assinar o lançamento da extensão. Consulte o comportamento das extensões de Sideload abaixo para obter mais detalhes.

## Proteção de Informações do Windows
Atualmente, as extensões do Microsoft Edge não obedecem às configurações de WIP (proteção de informações do Windows). Se uma empresa se preocupa com a proteção de dados, o suporte a extensões não deve ser habilitado para o Microsoft Edge.

Para desabilitar as extensões para funcionários, configure a política de grupo e as configurações do Microsoft Intune. Para obter mais informações sobre quais políticas configurar, consulte [políticas disponíveis para o Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).

## Extensões de pacotes
Antes de uma empresa poder distribuir uma extensão a seus funcionários, ela deve primeiro ser empacotada. Instruções sobre extensões de pacotes estão disponíveis no guia de [empacotamento](./guides/packaging.md) .

> [!TIP]
> Certifique-se de testar a instalação e executar a extensão em todas as versões do Windows 10 para garantir que ela funcionará como esperado antes da distribuição.

## Distribuindo extensões
Após o empacotamento, ele pode ser distribuído aos funcionários por meio da Microsoft Store, da Microsoft Store para empresas ou do Sideload.

Extensões distribuídas por meio da Microsoft Store para empresas podem ser atribuídas a funcionários ou adicionadas a um armazenamento privado em que todos os funcionários possam acessá-los. Isso pode ser feito seguindo o guia de [distribuição de aplicativos de linha de negócios (LOB) para empresas](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) .

Para extensões Sideload, os dispositivos (não gerenciados ou gerenciados) devem ser desbloqueados para Sideload. Consulte [Sideload de aplicativos LOB no Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) para obter mais informações sobre como Sideload as extensões empacotadas.

> [!IMPORTANT]
> Se a empresa estiver desenvolvendo e distribuindo a extensão internamente, a empresa exigirá a Microsoft Store para empresas (ou educação) e uma conta do portal do desenvolvedor do Windows.

### Comportamento de extensões Sideload
Diferentemente das extensões distribuídas pela Microsoft Store (ou da Microsoft Store para empresas), as extensões Sideload são tratadas de modo diferente no Microsoft Edge.

A primeira diferença afeta como as extensões Sideload se comportam após a instalação. Diferentemente das extensões da Microsoft Store, as extensões Sideload não exibem imediatamente a notificação "você tem uma nova extensão" e precisa ser ativada manualmente pelo usuário.

Para ativar a extensão, abra o menu **mais (...)** , selecione **"extensões"** e você deve ver a extensão Sideload na lista de extensões instaladas. Clique na extensão e ative-a.

A segunda diferença afeta como as extensões Sideload são exibidas no navegador. Por exemplo, a notificação "você tem uma nova extensão" e a lista de extensões instaladas incluem um aviso adicional informando que a extensão é de uma fonte desconhecida.

![aviso de Sideload 1](./media/sideload-permissionflyout.PNG)

![aviso de Sideload 2](./media/sideload-l1warning.PNG)

A terceira e última diferença afetam como as extensões Sideload se comportam na inicialização do navegador. As extensões do Sideload em dispositivos que fazem parte de um domínio ou MDM habilitadas se comportam como extensões da Microsoft Store. No entanto, as extensões do Sideload em dispositivos que não fazem parte do domínio ou MDM habilitado serão desativadas durante a inicialização do navegador e exigem que o usuário tome uma ação explícita.

Logo após a inicialização do navegador (após cerca de 10 segundos de inatividade) a seguinte notificação será exibida próxima à parte inferior da janela.

![notificação Sideload](./media/sideload-scareUI.PNG)

Cada vez que o Microsoft Edge for iniciado, os usuários precisarão selecionar "ativar de qualquer maneira" para usar a extensão.
