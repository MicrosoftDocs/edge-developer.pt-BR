---
description: Como localizar e analisar o código JavaScript e CSS não utilizados no Microsoft Edge DevTools.
title: Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 19bc15578e00e5a9f3389529f589e9790280a0e4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993090"
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





# Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools   



A guia cobertura no Microsoft Edge DevTools ajuda você a localizar código JavaScript e CSS não utilizados.  A remoção de um código não usado pode acelerar a carga da página e salvar os dados da rede celular dos seus usuários móveis.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analisando cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Analisando cobertura de código  
:::image-end:::  

> [!WARNING]
> Localizar código não usado é relativamente fácil.  Mas refatorar uma codebase para que cada página só entregue o JavaScript e o CSS necessários, pode ser difícil.  Este guia não aborda como refatorar uma codebase para evitar código não usado, pois esses refactores dependem muito do seu conjunto de tecnologias.  

## Visão geral   

O envio de JavaScript ou CSS não usado é um problema comum no desenvolvimento na Web.  Por exemplo, suponha que você queira usar o [componente botão Bootstrap][BootstrapButtons] na página.  Para usar o componente Button, você precisa adicionar um link para a folha de estilo Bootstrap em seu HTML, assim:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Essa folha de estilos não inclui apenas o código do componente Button.  Ele contém a CSS para **todos** os componentes de bootstrap.  Mas você não está usando nenhum dos outros componentes de inicialização.  Portanto, sua página está baixando um grupo de CSS que não precisa.  Essa CSS extra é um problema pelos motivos a seguir.  

*   O código extra reduz a carga da página.  <!--See [Render-Blocking CSS][render].  -->  
*   Se um usuário acessar a página em um dispositivo móvel, o código adicional usará seus dados da rede celular.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## Abrir a guia cobertura   

1.  [Abrir o menu de comandos][DevToolsCommandMenu].  
1.  Comece `coverage` a digitar, selecione o comando **Mostrar cobertura** e pressione `Enter` para executar o comando.  A guia **cobertura** é aberta na **gaveta**.  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="A guia cobertura" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       A guia **cobertura**  
    :::image-end:::  
    
## Cobertura de código de registro   

1.  Clique em um dos seguintes botões na guia **cobertura** :  
    *   Clique em **Iniciar cobertura de instrumentação e recarregar página** \ ( ![ Iniciar cobertura de instrumentação e carregar página ][ImageReloadIcon] \) se você quiser ver qual código é necessário para carregar a página.  
    *   Clique em **cobertura do instrumento** \ (cobertura do ![ instrumento ][ImageRecordIcon] \) se você quiser ver qual código será usado depois de interagir com a página.  
1.  Clique em **interromper a cobertura de instrumentação e mostrar resultados** \ ( ![ interromper a cobertura de instrumentação e mostrar resultados ][ImageStopIcon] \) quando quiser parar de gravar a cobertura de código.  
    
## Analisar cobertura de código   

A tabela na guia **cobertura** mostra quais recursos foram analisados e quanto de código é usado dentro de cada recurso.  Clique em uma linha para abrir esse recurso no painel **fontes** e ver uma divisão linha por linha de código usado e código não usado.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Um relatório de cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Um relatório de cobertura de código  
:::image-end:::  

*   A coluna **URL** é a URL do recurso que foi analisado.  
*   A coluna **tipo** indica se o recurso contém CSS, JavaScript ou ambos.  
*   A coluna **total de bytes** é o tamanho total do recurso em bytes.  
*   A coluna **bytes não utilizados** é o número de bytes que não foram usados.  
*   A última coluna sem nome é uma visualização das colunas **total de bytes** e **bytes não utilizados** .  A seção vermelha da barra é bytes não utilizados.  A seção verde é usada bytes.  
    
<!--  
 


-->  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botões-Bootstrap"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/coverage/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
