---
description: Lista de referências para domínios com suporte no protocolo Microsoft Edge DevTools versão 0,1.
title: Domains-DevTools protocolo versão 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: b3cf3411a8402b7407012eb789f8bf267b4997a8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561353"
---
# <span data-ttu-id="b12b1-103">Domínios de protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="b12b1-103">DevTools Protocol Domains</span></span>
## [<span data-ttu-id="b12b1-104">Depurador</span><span class="sxs-lookup"><span data-stu-id="b12b1-104">Debugger</span></span>](debugger.md)
<span data-ttu-id="b12b1-105">O domínio do depurador expõe recursos de depuração JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b12b1-105">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="b12b1-106">Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.</span><span class="sxs-lookup"><span data-stu-id="b12b1-106">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>
## [<span data-ttu-id="b12b1-107">Página</span><span class="sxs-lookup"><span data-stu-id="b12b1-107">Page</span></span>](page.md)
<span data-ttu-id="b12b1-108">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="b12b1-108">Actions and events related to the inspected page belong to the page domain.</span></span>
## [<span data-ttu-id="b12b1-109">Classpath</span><span class="sxs-lookup"><span data-stu-id="b12b1-109">Runtime</span></span>](runtime.md)
<span data-ttu-id="b12b1-110">O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos.</span><span class="sxs-lookup"><span data-stu-id="b12b1-110">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="b12b1-111">Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior.</span><span class="sxs-lookup"><span data-stu-id="b12b1-111">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="b12b1-112">Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.</span><span class="sxs-lookup"><span data-stu-id="b12b1-112">Original objects are maintained in memory unless they are either explicitly released.</span></span>
## [<span data-ttu-id="b12b1-113">Esquema</span><span class="sxs-lookup"><span data-stu-id="b12b1-113">Schema</span></span>](schema.md)
<span data-ttu-id="b12b1-114">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="b12b1-114">Provides information about the protocol schema.</span></span>