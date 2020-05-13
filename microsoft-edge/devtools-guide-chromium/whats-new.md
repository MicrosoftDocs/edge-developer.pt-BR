---
description: Recursos adicionados ao Microsoft Edge (Chromium) DevTools em março de 2019
title: O que há de novo no Microsoft Edge (Chromium) DevTools em março de 2019
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: bf1919b0ab46df378880d664dd4e59aee96605e5
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645319"
---
# O que há de novo no Microsoft Edge (Chromium) DevTools

Muito obrigado por experimentar uma visualização da próxima versão do Microsoft Edge! Com esta versão, desenvolvemos uma grande mudança na plataforma da Web subjacente do Microsoft Edge, adotando o projeto de fonte aberta Chromium. Com essa alteração, será mais fácil para você criar e testar seus sites no Microsoft Edge e garantir que eles ainda funcionarão como esperado, mesmo se seus usuários estiverem procurando em um navegador diferente baseado no Chromium, como Google Chrome, Vivaldi, Opera ou Brave.

## O novo Microsoft Edge (Chromium) DevTools

Se você estiver fazendo check-out do Microsoft Edge e se desenvolve principalmente em um navegador baseado no Chromium, você deve se sentir em casa. As ferramentas de desenvolvedor do Microsoft Edge (Chromium) são exatamente como as ferramentas de desenvolvedor que você já conhece e usa!

![Microsoft Edge (Chromium) DevTools](./media/devtools.png)

Se você estiver fazendo check-out da próxima versão do Microsoft Edge e tiver desenvolvido principalmente no Microsoft Edge (EdgeHTML), temos algumas ótimas ferramentas novas que esperamos tornar mais fácil e rápido criar e testar seus sites no Microsoft Edge! Para saber mais sobre essas novas ferramentas, confira [o guia do devtools Microsoft Edge (Chromium)](../devtools-guide-chromium.md).

## Novos temas escuros e leves para o DevTools

Projetamos alguns novos temas escuros e leves para a DevTools que achamos que você vai adorar! Por padrão, o DevTools Microsoft Edge (Chromium) vai usar o tema escuro. Para alterar o tema do devtools, pressione `Fn`  +  `F1` no Windows ou Mac ou navegue até configurações usando o `...` botão no canto superior direito do devtools.

![Menu principal do Microsoft Edge (Chromium) DevTools](./media/devtools-main-menu.png)

Em configurações, você pode alterar o tema da DevTools. Se você gostou da maneira como o DevTools procurou em seu navegador baseado no Chromium, você pode fazer com que o Microsoft Edge (Chromium) DevTools tenha exatamente o seguinte selecionando os temas **escuro (Chromium)** ou **leve (Chromium)** , respectivamente. 

## Depurar o Microsoft Edge (Chromium) a partir de código VS

Com o [depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, agora você pode depurar o Microsoft Edge (EdgeHTML) e o Microsoft Edge (Chromium) diretamente do código vs!

![Depurador para borda VS extensão de código](./media/vscode-debugger.png)

Para iniciar o Microsoft Edge (Chromium) em vez do Microsoft Edge (EdgeHTML) a partir de código VS, você precisa adicionar um `version` atributo à sua configuração **Iniciar. JSON** existente com a versão do Microsoft Edge (Chromium) que deseja iniciar ( `dev` , `beta` , ou `canary` ). Aqui está uma configuração de exemplo de **inicialização. JSON** que iniciará a versão Canárias do Microsoft Edge (Chromium) para o [Bing.com](https://www.bing.com/):

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

Para obter mais informações, confira [como depurar o Microsoft Edge (Chromium) a partir de código vs](../visual-studio-code/debugger-for-edge.md).

## Atualização do protocolo DevTools Edge

Com o turno na plataforma da Web subjacente do Microsoft Edge, o protocolo Edge DevTools não receberá mais nenhuma atualização. O DevTools Microsoft Edge (Chromium) usará o protocolo de DevTools do Chrome ou a CDP. Para fazer referência à documentação dos domínios e métodos no CDP, consulte [o Visualizador de CDP](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).

Na próxima versão do Microsoft Edge, não haverá suporte para os métodos com prefixos `ms` . Para saber mais sobre como usar o CDP no Microsoft Edge (Chromium), consulte [devtools Protocol (Chromium)](../devtools-protocol-chromium.md).

## Problemas conhecidos

Muitos links do DevTools Microsoft Edge (Chromium) para conteúdo hospedado em sites de terceiros foram removidos temporariamente. Assim que pudermos substituir esses links, vamos adicioná-los de volta ao DevTools.


Ao depurar o conteúdo da Web em um dispositivo Android do Microsoft Edge (Chromium), a versão do DevTools que é iniciada quando você clica no botão **inspecionar** da ferramenta **dispositivos remotos** pode não corresponder à versão do navegador em seu dispositivo Android. Como resultado, você poderá ver os novos recursos do DevTools que não funcionarão com o navegador em seu dispositivo Android. Se isso for algo que você encontrar, adoraríamos saber isso para fazer comentários sobre o [arquivo](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team).

Por fim, o Visual Studio no Windows e no Mac ainda não é compatível com o Microsoft Edge (Chromium). Inscreva-se [aqui](https://visualstudio.microsoft.com/vs/preview/) para ser o primeiro a saber quando temos uma versão de visualização do Visual Studio que ofereça suporte à depuração do JavaScript dentro do Microsoft Edge (Chromium) para projetos do ASP.net.  
