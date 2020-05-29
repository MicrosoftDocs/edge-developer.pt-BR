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
# Internacionalização  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Para tornar sua extensão acessível para uma variedade de pessoas diferentes, é importante desenvolver com outros países em mente. O Microsoft Edge Extensions permite que você adicione diferentes cadeias de caracteres de idioma às suas extensões para que o idioma possa ser alterado facilmente.

Para saber mais sobre como internacionalizar a extensão, consulte o [Guia de internacionalização](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)do MDN.


## Testando idiomas

Para testar as cadeias de caracteres de idioma, você precisa primeiro definir o idioma de exibição do Windows para o idioma que você deseja testar.

Siga as etapas abaixo para alterar o idioma de exibição do Windows:

1. Abra o aplicativo configurações.

   ![aplicativo configurações](./../media/loc-settings.png)
2. Selecione "hora & idioma".
3. Selecione "região & idioma".
4. Selecione "+ adicionar um idioma" para adicionar o idioma à lista de idiomas possíveis.
5. Escolha o idioma na lista "idiomas" que você deseja testar.
6. Selecione o botão "definir como padrão" (talvez seja necessário reiniciar o computador).
7. Abra o Microsoft Edge e verifique se as cadeias de caracteres definidas para a localidade aparecem como esperado.

Usando a propriedade [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) , você pode verificar se o idioma que o Microsoft Edge determinou ser o idioma de exibição do Windows está correto.

Clique no botão na CodePen abaixo para ver o idioma de exibição do navegador.

<iframe height='300' scrolling='no' title='Obter localidade' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulte a guia <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> obter a localidade </a> por MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='http://codepen.io'> CodePen </a> .
</iframe>
