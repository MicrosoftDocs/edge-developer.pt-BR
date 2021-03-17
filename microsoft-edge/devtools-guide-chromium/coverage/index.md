---
description: Como encontrar e analisar o JavaScript e o código CSS nãoutilados no Microsoft Edge DevTools.
title: Encontre JavaScript e Código CSS nãoutilados com o painel Cobertura no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2a2d48bda34daa95b9f500c31a12859a1cb08625
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439195"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a>Encontre o JavaScript e o código CSS nãoutilados com o painel Cobertura no Microsoft Edge DevTools  

O **painel Cobertura** no Microsoft Edge DevTools ajuda você a encontrar código JavaScript e CSS não-utilado.  A remoção de código nãousado pode acelerar a carga da página e salvar os dados celulares dos usuários móveis.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analisando a cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Analisando a cobertura de código  
:::image-end:::  

> [!WARNING]
> Localizar código nãousado é relativamente fácil.  Mas a refactoração de uma base de código para que cada página só envia o JavaScript e CSS necessários pode ser difícil.  Este guia não abrange como refactor uma base de código para evitar o código nãousado, pois esses refatores dependem muito da sua pilha de tecnologia.  

## <a name="overview"></a>Visão geral  

O envio de JavaScript ou CSS nãousado é um problema comum no desenvolvimento da Web.  Por exemplo, suponha que você queira usar o [componente do botão Bootstrap][BootstrapButtons] em sua página.  Para usar o componente de botão, você precisa adicionar um link à folha de estilos Bootstrap em seu HTML, assim:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Esta folha de estilos não inclui apenas o código do componente do botão.  Ele contém o CSS para **todos os** componentes Bootstrap.  Mas você não está usando nenhum dos outros componentes Bootstrap.  Portanto, sua página está baixando um monte de CSS que ela não precisa.  Esse CSS extra é um problema pelos seguintes motivos.  

*   O código extra reduz a carga da página.  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   Se um usuário acessar a página em um dispositivo móvel, o código extra usará seus dados celulares.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a>Abra o painel Cobertura  

1.  [Abra o Menu de Comando][DevToolsCommandMenu].  
1.  Comece a digitar `coverage` , selecione o comando Mostrar **Cobertura** e, em seguida, selecione para executar `Enter` o comando.  O **painel Cobertura** é aberto na **Gaveta**.  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="O painel Cobertura" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       O **painel Cobertura**  
    :::image-end:::  
    
## <a name="record-code-coverage"></a>Cobertura de código de registro  

1.  Escolha um dos seguintes botões no painel **Cobertura.**  
    *   Escolha **Iniciar a Cobertura de Instrumentação** e Recarregar Página \( Iniciar Cobertura de Instrumentação e Recarregar Página \) se quiser revisar qual código é necessário para carregar a ![ ](../media/reload-icon.msft.png) página.  
    *   Escolha **Cobertura de** Instrumento \( Cobertura de Instrumento \) se quiser revisar qual código é usado após interagir com a ![ ](../media/record-icon.msft.png) página.  
1.  Escolha **Parar a cobertura de instrumentação e mostrar resultados** \( Parar a cobertura de instrumentação e mostrar resultados \) quando quiser parar de gravar a cobertura de ![ ](../media/stop-icon.msft.png) código.  
    
## <a name="analyze-code-coverage"></a>Analisar a cobertura de código  

A tabela no painel **Cobertura** exibe os recursos que foram analisados e quanto código é usado em cada recurso.  Escolha uma linha para abrir esse recurso no painel **Fontes** e revise uma divisão linha por linha do código usado e do código não usado.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Um relatório de cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Um relatório de cobertura de código  
:::image-end:::  

*   A **coluna URL** é a URL do recurso que foi analisado.  
*   A **coluna Type** diz se o recurso contém CSS, JavaScript ou ambos.  
*   A **coluna Total de Bytes** é o tamanho total do recurso em bytes.  
*   A **coluna Bytes não utilizados** é o número de bytes que não foram usados.  
*   A última coluna sem nome é uma visualização das colunas **Bytes Totais** e **Bytes NãoUsados.**  A seção vermelha da barra é bytes nãousados.  A seção verde é usada bytes.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botões - Bootstrap"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/coverage/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
