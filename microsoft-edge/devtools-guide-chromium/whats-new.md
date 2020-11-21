---
description: Recursos adicionados ao Microsoft Edge (Chromium) DevTools em março de 2019
title: O que há de novo no Microsoft Edge (Chromium) DevTools em março de 2019
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/23/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0b592eddbd68b3bbd8ff0a9edf9a1253bd79677e
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182509"
---
# O que há de novo no Microsoft Edge (Chromium) DevTools

Muito obrigado por experimentar uma visualização do novo Microsoft Edge! Com esta versão, desenvolvemos uma grande mudança na plataforma da Web subjacente do Microsoft Edge, adotando o projeto de fonte aberta Chromium. Com essa alteração, será mais fácil para você criar e testar seus sites no Microsoft Edge e garantir que eles ainda funcionarão como esperado, mesmo se seus usuários estiverem procurando em um navegador diferente baseado no Chromium, como Google Chrome, Vivaldi, Opera ou Brave.

## O novo Microsoft Edge (Chromium) DevTools

Se você estiver fazendo check-out do Microsoft Edge e se desenvolve principalmente em um navegador baseado no Chromium, você deve se sentir em casa. As ferramentas de desenvolvedor do Microsoft Edge (Chromium) são exatamente como as ferramentas de desenvolvedor que você já conhece e usa!

![Microsoft Edge (Chromium) DevTools](./media/devtools.png)

Se você estiver fazendo o check-out do novo Microsoft Edge e tiver desenvolvido principalmente no Microsoft Edge (EdgeHTML), temos algumas ferramentas incríveis incríveis que esperamos facilitar e agilizar a criação e teste de seus sites da Web no Microsoft Edge! Para saber mais sobre essas novas ferramentas, confira [o guia do devtools Microsoft Edge (Chromium)](../devtools-guide-chromium.md).

## Novos temas escuros e leves para o DevTools

Projetamos alguns novos temas escuros e leves para a DevTools que achamos que você vai adorar! Por padrão, o DevTools Microsoft Edge (Chromium) vai usar o tema escuro. Para alterar o tema do devtools, pressione `Fn`  +  `F1` no Windows ou Mac ou navegue até configurações usando o `...` botão no canto superior direito do devtools.

![Menu principal do Microsoft Edge (Chromium) DevTools](./media/devtools-main-menu.png)

Em configurações, você pode alterar o tema da DevTools. Se você gostou da maneira como o DevTools procurou em seu navegador baseado no Chromium, você pode fazer com que o Microsoft Edge (Chromium) DevTools tenha exatamente o seguinte selecionando os temas **escuro (Chromium)** ou **leve (Chromium)** , respectivamente. 

## Depurar o Microsoft Edge (Chromium) a partir de código VS

Com o [depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, agora você pode depurar o Microsoft Edge (EdgeHTML) e o Microsoft Edge (Chromium) diretamente do código vs!

![Depurador para borda VS extensão de código](./media/vscode-debugger.png)

Para iniciar o Microsoft Edge (Chromium) em vez do Microsoft Edge (EdgeHTML) a partir do código VS, você precisa adicionar um `version` atributo ao seu **launch.jsexistente na** configuração com a versão do Microsoft Edge (Chromium) que deseja iniciar ( `dev` , `beta` ou ou `canary` ). Aqui está um exemplo **launch.jsna** configuração que iniciará a versão Canárias do Microsoft Edge (Chromium) para o [Bing.com](https://www.bing.com/):

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

No novo Microsoft Edge, qualquer método com o prefixo `ms` não terá suporte. Para saber mais sobre como usar o CDP no Microsoft Edge (Chromium), consulte [devtools Protocol (Chromium)](../devtools-protocol-chromium.md).

## Problemas conhecidos

Muitos links do DevTools Microsoft Edge (Chromium) para conteúdo hospedado em sites de terceiros foram removidos temporariamente. Assim que pudermos substituir esses links, vamos adicioná-los de volta ao DevTools.


Ao depurar o conteúdo da Web em um dispositivo Android do Microsoft Edge (Chromium), a versão do DevTools que é iniciada quando você clica no botão **inspecionar** da ferramenta **dispositivos remotos** pode não corresponder à versão do navegador em seu dispositivo Android. Como resultado, você poderá ver os novos recursos do DevTools que não funcionarão com o navegador em seu dispositivo Android. Se isso for algo que você encontrar, adoraríamos saber isso para fazer comentários sobre o [arquivo](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team).

Por fim, o Visual Studio no Windows e no Mac ainda não é compatível com o Microsoft Edge (Chromium). Inscreva-se [aqui](https://visualstudio.microsoft.com/vs/preview/) para ser o primeiro a saber quando temos uma versão de visualização do Visual Studio que ofereça suporte à depuração do JavaScript dentro do Microsoft Edge (Chromium) para projetos do ASP.net.  
