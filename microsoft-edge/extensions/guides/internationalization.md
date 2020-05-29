---
description: Torne sua extensão acessível para diferentes idiomas e teste as cadeias de caracteres de idioma com o guia de internacionalização.
title: Extensões-internacionalização
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561199"
---
# <span data-ttu-id="7546a-104">Internacionalização</span><span class="sxs-lookup"><span data-stu-id="7546a-104">Internationalization</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7546a-105">Para tornar sua extensão acessível para uma variedade de pessoas diferentes, é importante desenvolver com outros países em mente.</span><span class="sxs-lookup"><span data-stu-id="7546a-105">In order to make your extension accessible to a variety of different people, it is important to develop with other countries in mind.</span></span> <span data-ttu-id="7546a-106">O Microsoft Edge Extensions permite que você adicione diferentes cadeias de caracteres de idioma às suas extensões para que o idioma possa ser alterado facilmente.</span><span class="sxs-lookup"><span data-stu-id="7546a-106">Microsoft Edge extensions allows you to add different language strings to your extensions so that their language can easily be changed.</span></span>

<span data-ttu-id="7546a-107">Para saber mais sobre como internacionalizar a extensão, consulte o [Guia de internacionalização](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)do MDN.</span><span class="sxs-lookup"><span data-stu-id="7546a-107">For more information on internationalizing your extension, check out MDN's [Internationalization guide](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization).</span></span>


## <span data-ttu-id="7546a-108">Testando idiomas</span><span class="sxs-lookup"><span data-stu-id="7546a-108">Testing languages</span></span>

<span data-ttu-id="7546a-109">Para testar as cadeias de caracteres de idioma, você precisa primeiro definir o idioma de exibição do Windows para o idioma que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="7546a-109">To test your language strings, you first need to set the Windows display language to the language that you want to test for.</span></span>

<span data-ttu-id="7546a-110">Siga as etapas abaixo para alterar o idioma de exibição do Windows:</span><span class="sxs-lookup"><span data-stu-id="7546a-110">Follow the steps below to change the Windows display language:</span></span>

1. <span data-ttu-id="7546a-111">Abra o aplicativo configurações.</span><span class="sxs-lookup"><span data-stu-id="7546a-111">Open the Settings app.</span></span>

   ![aplicativo configurações](./../media/loc-settings.png)
2. <span data-ttu-id="7546a-113">Selecione "hora & idioma".</span><span class="sxs-lookup"><span data-stu-id="7546a-113">Select "Time & language".</span></span>
3. <span data-ttu-id="7546a-114">Selecione "região & idioma".</span><span class="sxs-lookup"><span data-stu-id="7546a-114">Select "Region & language".</span></span>
4. <span data-ttu-id="7546a-115">Selecione "+ adicionar um idioma" para adicionar o idioma à lista de idiomas possíveis.</span><span class="sxs-lookup"><span data-stu-id="7546a-115">Select "+ Add a language" to add the language to the list of possible languages.</span></span>
5. <span data-ttu-id="7546a-116">Escolha o idioma na lista "idiomas" que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="7546a-116">Choose the language from the "Languages" list that you want to test.</span></span>
6. <span data-ttu-id="7546a-117">Selecione o botão "definir como padrão" (talvez seja necessário reiniciar o computador).</span><span class="sxs-lookup"><span data-stu-id="7546a-117">Select the "Set as default" button (you may need to restart your PC).</span></span>
7. <span data-ttu-id="7546a-118">Abra o Microsoft Edge e verifique se as cadeias de caracteres definidas para a localidade aparecem como esperado.</span><span class="sxs-lookup"><span data-stu-id="7546a-118">Open Microsoft Edge and verify that the strings defined for the locale appear as expected.</span></span>

<span data-ttu-id="7546a-119">Usando a propriedade [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) , você pode verificar se o idioma que o Microsoft Edge determinou ser o idioma de exibição do Windows está correto.</span><span class="sxs-lookup"><span data-stu-id="7546a-119">By using the [NavigatorLanguage.language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) property, you can verify that the language Microsoft Edge has determined to be the Windows display language is correct.</span></span>

<span data-ttu-id="7546a-120">Clique no botão na CodePen abaixo para ver o idioma de exibição do navegador.</span><span class="sxs-lookup"><span data-stu-id="7546a-120">Click the button in the CodePen below to see the display language of your browser.</span></span>

<iframe height='300' scrolling='no' title='<span data-ttu-id="7546a-121">Obter localidade</span><span class="sxs-lookup"><span data-stu-id="7546a-121">Get locale</span></span>' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="7546a-122">Consulte a guia <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> obter a localidade </a> por MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="7546a-122">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'>Get locale</a>by MSEdgeDev (<a href='http://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span>
</iframe>
