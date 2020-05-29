---
description: Usar o painel calculado para compreender como a CSS usa e computa em elementos de página
title: DevTools-elementos-calculados
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/10/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, elementos, CSS, valor calculado, modelo de caixa
ms.custom: seodec18
ms.openlocfilehash: c7b1b7c86f30e6947442c9b3d0e8856074ce4c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562214"
---
# <span data-ttu-id="b8052-104">Calculado</span><span class="sxs-lookup"><span data-stu-id="b8052-104">Computed</span></span>

<span data-ttu-id="b8052-105">Veja um diagrama de modelo de caixa (largura, preenchimento, borda, valores de margem e deslocamento) do elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="b8052-105">See a box model diagram (width, padding, border, margin and offset values) of the selected element.</span></span> <span data-ttu-id="b8052-106">Se você ativar a ferramenta de **realce de elemento** ( `Ctrl+Shift+L` ), as mesmas regiões coloridas no diagrama (para largura, enchimento etc.) que sobrepõem o elemento renderizado quando você seleciona-lo na página.</span><span class="sxs-lookup"><span data-stu-id="b8052-106">If you turn on the **Element highlighting** tool (`Ctrl+Shift+L`), the same colored regions in the diagram (for width, padding, etc.) that will overlay the rendered element when you select it on the page.</span></span> <span data-ttu-id="b8052-107">Você pode editar qualquer valor no diagrama clicando nele.</span><span class="sxs-lookup"><span data-stu-id="b8052-107">You can edit any value in the diagram by clicking it.</span></span> 

<span data-ttu-id="b8052-108">Abaixo do diagrama de modelo de caixa, há uma lista filtrada e editável de propriedades de estilo calculadas.</span><span class="sxs-lookup"><span data-stu-id="b8052-108">Below the box model diagram is a filterable and editable list of computed style properties.</span></span> <span data-ttu-id="b8052-109">Desativar uma propriedade ativa no momento ativa a próxima Propriedade na cascata, se houver.</span><span class="sxs-lookup"><span data-stu-id="b8052-109">Turning off a currently active property activates the next property in the cascade, if one exists.</span></span> <span data-ttu-id="b8052-110">Você pode exibir as alterações no painel [**alterações**](./changes.md) .</span><span class="sxs-lookup"><span data-stu-id="b8052-110">You can view your changes in the [**Changes**](./changes.md) pane.</span></span>

<span data-ttu-id="b8052-111">O botão **Exibir somente estilos do usuário** está ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="b8052-111">The **Display user styles only** button is on by default.</span></span> <span data-ttu-id="b8052-112">A descompactação do botão incluirá estilos da *folha* de estilos padrão do Microsoft Edge na lista de estilos calculados.</span><span class="sxs-lookup"><span data-stu-id="b8052-112">Depressing the button will include styles from the *default stylesheet* of Microsoft Edge in the computed styles list.</span></span>

![Painel calculado](../media/elements_computed.png)