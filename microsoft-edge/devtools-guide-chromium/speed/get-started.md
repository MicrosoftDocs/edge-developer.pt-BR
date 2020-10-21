---
description: Saiba como usar o Microsoft Edge DevTools para encontrar formas de fazer com que seus sites sejam carregados mais rapidamente.
title: Otimizar a velocidade do site com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: af655941fdc836759651e8d8202e41d8d03331c5
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125486"
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

# Otimizar a velocidade do site com o Microsoft Edge DevTools  

## Objetivo do tutorial  

Este tutorial ensina a usar o Microsoft Edge DevTools para encontrar formas de fazer com que seus sites sejam carregados mais rapidamente.  

## Pré-requisitos  

*   Você deve ter experiência básica de desenvolvimento na Web, semelhante ao que é ensinado nesta [introdução à classe de desenvolvimento na Web][CourseraIntroductionWebDevelopmentClass].  
*   Você não precisa saber nada sobre o desempenho da carga.  Saiba mais sobre isso neste tutorial!  

## Introdução  

Isso é Tony.  Tony é muito famoso na sociedade da gato.  Ele criou um site para que seus fãs possam aprender sobre seus alimentos favoritos.  Seus fãs adoram o site, mas o Tony mantém reclamações auditivas que o site carrega lentamente.  Tony solicitou que você o ajude a acelerar o site.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony o gato" lightbox="../media/speed-tony.msft.png":::
   Tony o gato  
:::image-end:::  

## Etapa 1: auditar o site  

Sempre que você se configurar para melhorar o desempenho de carga de um site, **sempre comece com uma auditoria**.  
A auditoria tem duas funções importantes:  

*   Ele cria uma **linha de base** para você medir alterações subsequentes em relação a.  
*   Ele oferece **dicas acionáveis** sobre quais alterações têm o maior impacto possível.  
    
### Configurar  

Primeiro, você deve configurar o site para que possa fazer alterações nele mais tarde.  

1.  [Abra o código-fonte do site](https://glitch.com/edit/#!/tony).  Esta guia é referida como a **guia Editor**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       A **guia Editor**  
    :::image-end:::  
    
1.  Escolha **Tony**.  Um menu é exibido.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       O menu que aparece depois de clicar em **Tony**  
    :::image-end:::  
    
1.  Escolha **projeto remix**.  O nome do projeto muda de **Tony** para algum nome gerado aleatoriamente.  Agora você tem sua própria cópia editável do código.  Posteriormente, você pode fazer alterações nesse código.  
1.  Escolha **Mostrar** e escolha **em uma nova janela**.  A demonstração é aberta em uma nova guia.  Esta guia é referida como a **guia demonstração**.  Pode levar alguns instantes para que o site seja carregado.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       A guia demonstração  
    :::image-end:::  
    
1.  Selecione `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).  O Microsoft Edge DevTools abre juntamente com a demonstração.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools e a demonstração  
    :::image-end:::  
    
Para o restante das capturas de tela neste tutorial, DevTools é exibido em uma janela separada.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digitando `Undock` e, em seguida, selecione **desencaixar em uma janela separada**.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Tony o gato" lightbox="../media/speed-console.msft.png":::
   DevTools desencaixado  
:::image-end:::  

### Estabelecer uma linha de base  

A linha de base é um registro de como o site foi executado antes de você fazer qualquer melhoria no desempenho.  

1.  Selecione a guia **auditorias** .  Ele pode estar oculto atrás do botão **mais painéis** \ ( ![ mais painéis ][ImageMorePanelsIcon] \).  Há um Lighthouse neste painel porque o projeto que energiza o painel auditorias é denominado **Lighthouse**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Tony o gato" lightbox="../media/speed-audits-performance.msft.png":::
       O painel **auditorias**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Correspondam às suas configurações de auditoria para as da figura anterior.  Aqui está uma explicação das diferentes opções:  
    
    *   **Device**.  A configuração para **celular** altera a cadeia de caracteres do agente do usuário e simula um visor móvel.  A configuração para **área de trabalho** simplesmente desabilita as alterações de **celular** .  
    *   **Auditorias**.  A desativação de uma categoria impede que o painel auditorias execute essas auditorias e exclui essas auditorias do relatório.  Deixe as outras categorias habilitadas, se você quiser ver os tipos de recomendações que são fornecidos.  Desabilitar categorias ligeiramente acelera o processo de auditoria.  
    *   **Limitação**.  Configuração para **Simulated 4G lenta, a lentidão de CPU de 4** simula as condições típicas de navegação em um dispositivo móvel.  Ele é chamado de "simulado" porque o painel auditorias não é controlado na verdade durante o processo de auditoria.  Em vez disso, ele apenas extrapola o tempo que a página levaria para carregar em condições de celular.  A configuração **aplicada...** , por outro lado, efetivamente limita sua CPU e rede, com a compensação de um processo de auditoria mais longo.  
    *   **Limpar o armazenamento**.  Habilitar essa caixa de seleção limpa todo o armazenamento associado à página antes de cada auditoria.  Deixe essa configuração em caso de você desejar auditar como os visitantes da primeira vez que o visitante terão.  Desative essa configuração quando quiser a experiência de visita de repetição.  
    
1.  Escolha **executar auditorias**.  Após 10 a 30 segundos, o painel auditorias mostra um relatório do desempenho do site.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       O relatório para o painel auditorias do desempenho do site  
    :::image-end:::  
    
#### Manipulando erros de relatório  

Se você receber um erro no relatório do painel auditorias, tente executar a guia demonstração em uma janela **InPrivate** sem nenhuma outra guia aberta.  Isso garante que você esteja executando o Microsoft Edge a partir de um estado limpo.  As extensões do Microsoft Edge em particular geralmente interferem no processo de auditoria.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="Tony o gato" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### Entender o relatório  

O número na parte superior do seu relatório é a pontuação de desempenho geral do site.  Posteriormente, ao fazer alterações no código, você verá esse número aumentará.  Uma pontuação mais alta significa melhor desempenho.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   A pontuação geral de desempenho  
:::image-end:::  

A seção **métricas** fornece medidas quantitativas do desempenho do site.  Cada métrica fornece uma visão geral de um aspecto diferente do desempenho.  Por exemplo, a **primeira tinta de conteúdo** informa quando o conteúdo é pintado pela primeira vez na tela, que é uma etapa importante da percepção do usuário da carga da página, enquanto o **tempo para interativo** marca o ponto em que a página parece estar pronta o suficiente para lidar com interações do usuário.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   A seção **métricas**  
:::image-end:::  

Selecione o botão de alternância realçado na figura a seguir para ver uma descrição para cada métrica e escolha **saiba mais** para ler a documentação sobre ela.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Selecione o botão de alternância realçado para expandir os itens de métricas  
:::image-end:::  

As métricas a seguir são uma coleção de capturas de tela que mostram como a página parece ser carregada.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Capturas de tela de como a página ficou ao carregar  
:::image-end:::  

A seção **oportunidades** fornece dicas específicas sobre como melhorar o desempenho de carga dessa página específica.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   A seção **oportunidades**  
:::image-end:::  

Selecione uma oportunidade para saber mais sobre isso.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Eliminar oportunidade de recursos de bloqueio de renderização**  
:::image-end:::  

Escolha **saiba mais** para ver a documentação sobre por que uma oportunidade é importante e recomendações específicas sobre como corrigi-lo.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Tony o gato" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Documentação para a oportunidade de **eliminar recursos de bloqueio de renderização**  
:::image-end:::  

A seção **diagnóstico** fornece mais informações sobre fatores que contribuem para o tempo de carregamento da página.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   A seção **diagnóstico**  
:::image-end:::  

A seção de **auditorias passadas** mostra o que o site está fazendo corretamente.  Selecione para expandir a seção.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   A seção de **auditorias passadas**  
:::image-end:::  

## Etapa 2: Experimente  

A seção oportunidades do seu relatório de auditoria fornece dicas sobre como melhorar o desempenho da página.  Nesta seção, você implementa as alterações recomendadas na base de código, fazendo auditoria do site após cada alteração para medir como ele afeta a velocidade do site.  

### Habilitar a compactação de texto  

O relatório informa que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.  Habilitar a compactação de texto é uma oportunidade de melhorar o desempenho da página.  

A compactação de texto é quando você reduz ou compacta o tamanho de um arquivo de texto antes de enviá-lo pela rede.  Tipo de como você pode compactar uma pasta antes de enviar um email para ela para reduzir o tamanho.  

Antes de habilitar a compactação, aqui estão algumas maneiras de verificar manualmente se os recursos de texto estão compactados.  

1.  Selecione a guia **rede** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       Painel de **rede**  
    :::image-end:::  
    
1.  Selecione o ícone de **configuração de rede** .  
1.  Marque a caixa de seleção **usar linhas de solicitação grandes** .  A altura das linhas na tabela de solicitações de rede aumenta.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Linhas grandes na tabela solicitações de rede  
    :::image-end:::  
    
1.  Se você não vir a coluna **tamanho** na tabela de solicitações de rede, clique no cabeçalho da tabela e escolha **tamanho**.  

Cada célula de **tamanho** mostra dois valores.  O valor principal é o tamanho do recurso baixado.  
O valor secundário é o tamanho do recurso descompactado.  Se os dois valores forem iguais, o recurso não será compactado quando for enviado pela rede.  Por exemplo, na figura anterior, os valores superiores e inferiores para `bundle.js` são `1.2 MB` e `1.2 MB` .  

Verifique a compactação inspecionando os cabeçalhos HTTP de um recurso:  

1.  Escolha **bundle.js**.  
1.  Selecione a guia **cabeçalhos** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       A guia **cabeçalhos**  
    :::image-end:::  
    
1.  Pesquisar o cabeçalho na seção de **cabeçalhos de resposta** `content-encoding` .  Você não deve ver um, o que significa que `bundle.js` não foi compactado.  Quando um recurso é compactado, esse cabeçalho geralmente é definido como `gzip` , `deflate` ou `br` .  Consulte [diretrizes][MDNContentEncodingDirectives] para obter uma explicação desses valores.  

Suficiente com as explicações.  É hora de fazer algumas mudanças!  Habilite a compactação de texto adicionando algumas linhas de código:  

1.  Na guia Editor, escolha **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Editar `server.js`  
    :::image-end:::  
    
1.  Adicione o código a seguir ao **server.js**.  Certifique-se de colocar `app.use(compression())` antes `app.use(express.static('build'))` .  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > Geralmente, você precisa instalar o `compression` pacote por algo semelhante `npm i -S compression` , mas isso já foi feito para você.  
    
1.  Aguarde até que a falha implante a nova compilação do site.  A animação sofisticada ao lado de **ferramentas** significa que o site está sendo recriado e reimplantado.  A alteração estará pronta quando a animação ao lado de **ferramentas** ficar ausente.  Escolha **Mostrar** e escolha novamente **em uma nova janela** .  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Use os fluxos de trabalho que você aprendeu anteriormente para verificar manualmente se a compactação está funcionando:  

1.  Volte para a guia demonstração e recarregue a página.  A coluna **tamanho** agora deve mostrar 2 valores diferentes para recursos de texto, como `bundle.js` .  Na figura após o seguinte, o valor principal de `256 KB` para `bundle.js` é o tamanho do arquivo que foi enviado pela rede e o valor inferior de `1.2 MB` é o tamanho de arquivo descompactado.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       A coluna **tamanho** agora mostra 2 valores diferentes para recursos de texto  
    :::image-end:::  
    
1.  A seção de **cabeçalhos de resposta** para `bundle.js` agora deve incluir um `content-encoding: gzip` cabeçalho.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       A seção de **cabeçalhos de resposta** agora contém um cabeçalho de codificação de conteúdo  
    :::image-end:::  
    
Faça a auditoria da página novamente para medir o tipo de compactação de texto de impacto no desempenho de carga da página:  

1.  Selecione a guia **auditorias** .  
1.  Escolha **executar uma auditoria** \ ( ![ realizar uma auditoria ][ImagePerformIcon] \).  
1.  Deixe as configurações iguais às anteriores.  
1.  Escolha **executar auditoria**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Um relatório de auditorias após a habilitação da compactação de texto  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  A pontuação geral do desempenho deve ter aumentado, o que significa que o site está ficando mais rápido.  

#### Compactação de texto no mundo real  

A maioria dos servidores tem correções simples como essa para habilitar a compactação!  Basta fazer uma busca em como configurar o servidor que você usa para compactar texto.  

### Redimensionar imagens  

O relatório indica que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.  O redimensionamento de imagens ajuda a reduzir o tamanho da carga de rede.  Se o usuário estiver exibindo as imagens em uma tela de dispositivo móvel com 500 pixels de largura, não há nenhum ponto em enviar uma imagem de 1500 pixels para todo o seu país.  O ideal é que você envie uma imagem de 500 pixels para todo o tempo.  

1.  Em seu relatório, escolha **evitar enormes cargas de rede** para ver quais imagens devem ser redimensionadas.  Ele se parece com 2 dos arquivos jpg há mais de 2000 KB, o que é maior do que o necessário.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  De volta na guia Editor, abra `src/model.js` .  
1.  Substituir `const dir = 'big'` por `const dir = 'small'` .  Esse diretório contém cópias das mesmas imagens que foram redimensionadas.  
1.  Faça a auditoria da página novamente para ver como essa alteração afeta o desempenho da carga.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Um relatório de auditorias após o redimensionamento de imagens  
    :::image-end:::  
    
Parece que a alteração tem apenas um efeito secundário na pontuação de desempenho geral.  No entanto, uma coisa que a pontuação não mostra claramente é o número de dados de rede que você está salvando os usuários.  O tamanho total das fotos antigas era cerca de 5,3 megabytes, enquanto agora só há cerca de 0,18 megabytes.  

#### Redimensionamento de imagens no mundo real  

Para um aplicativo pequeno, fazer um redimensionamento único como este pode ser bom o suficiente.  Mas para um aplicativo grande, isso obviamente não é dimensionável.  Aqui estão algumas estratégias para o gerenciamento de imagens em aplicativos grandes:  

*   Redimensione imagens durante o processo de compilação.  
*   Crie vários tamanhos de cada imagem durante o processo de compilação e, em seguida, use `srcset` em seu código.  Em tempo de execução, o navegador cuida da escolha de qual tamanho é melhor para o dispositivo.  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Use um CDN de imagem que permita redimensionar dinamicamente uma imagem quando você solicitá-la.  
*   No mínimo, otimize cada imagem.  Isso pode criar uma grande economia.  
  A otimização é quando você executa uma imagem por meio de um programa especial que reduz o tamanho do arquivo de imagem.  Consulte [otimizações de imagem essenciais][EssentialImageOptimization] para obter mais dicas.  
    
### Eliminar recursos de bloqueio de renderização  

O relatório mais recente diz que eliminar recursos de bloqueio de renderização agora é a maior oportunidade.  

Um recurso de bloqueio de renderização é um arquivo JavaScript ou CSS externo que o navegador deve baixar, analisar e executar antes de exibir a página.  O objetivo é executar somente o código CSS básico e JavaScript que é necessário para exibir a página corretamente.  

A primeira tarefa, então, é encontrar o código que você não precisa executar no carregamento da página.  

1.  Escolha **eliminar recursos de bloqueio de renderização** para ver os recursos que estão bloqueando:  
    `lodash.js` e `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Mais informações sobre a oportunidade de **eliminar recursos de bloqueio de renderização**  
    :::image-end:::  
    
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, comece a digitar `Coverage` e escolha **Mostrar cobertura**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Abrir o menu de comandos do painel **auditorias**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       A guia **cobertura**  
    :::image-end:::  
    
1.  Escolha **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).  A guia **cobertura** fornece uma visão geral da quantidade de código em `bundle.js` , `jquery.js` e `lodash.js` é executada enquanto a página é carregada.  Na figura após o seguinte, cerca de 76% e 30% dos arquivos jQuery e Lodash não são usados, respectivamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       O relatório de cobertura  
    :::image-end:::  
    
1.  Selecione a linha **jquery.js** .  DevTools abre o arquivo no painel fontes.  Uma linha de código foi executada se tiver uma barra azul ao lado dela.  Uma barra vermelha significa que ela não foi executada e não é necessária na carga da página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Visualizar o arquivo jQuery no painel **fontes**  
    :::image-end:::  
    
1.  Role pelo código jQuery um pouco.  Na verdade, algumas das linhas que recebem "executar" são apenas comentários.  Executar esse código por meio de um Minifier que retira comentários é outra maneira de reduzir o tamanho do arquivo.  

Resumindo, quando você estiver trabalhando com seu próprio código, a guia cobertura o ajudará a analisar o código, linha por linha, e enviar somente o código necessário para a carga da página.  

Os `jquery.js` arquivos e os `lodash.js` arquivos ainda são necessários para carregar a página?  A guia solicitar bloqueio exibe o que acontece quando os recursos não estão disponíveis.  

1.  Selecione a guia **rede** .  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando novamente.  
1.  Comece a digitar `blocking` e escolha **Mostrar bloqueio de solicitações**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       A guia **bloqueio de solicitação**  
    :::image-end:::  
    
1.  Escolha **Adicionar padrão** \ ( ![ Adicionar padrão ][ImageAddPatternIcon] \), tipo `/libs/*` e, em seguida, selecione `Enter` para confirmar.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Adicionar um padrão para bloquear qualquer solicitação ao `libs` diretório  
    :::image-end:::  
    
1.  Atualize a página.  As solicitações jQuery e Lodash são vermelhas, o que significa que as solicitações foram bloqueadas.   A página ainda é carregada e é interativa, portanto, parece que esses recursos não são necessários!  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       O painel **rede** mostra que as solicitações foram bloqueadas  
    :::image-end:::  
    
1.  Escolha **remover todos os padrões** \ ( ![ remover todos os padrões ][ImageRemoveIcon] \) para excluir o `/libs/*` padrão de bloqueio.  
    
Em geral, a guia bloqueio de solicitação é útil para simular como a sua página se comporta quando um determinado recurso não está disponível.  

Agora, remova as referências a esses arquivos do código e faça a auditoria da página novamente:  

1.  De volta na guia Editor, abra `template.html` .  
1.  Exclua `<script src="/libs/lodash.js">` e `<script src="/libs/jquery.js"></script>`.  
1.  Aguarde até que o site reconstrua e implante novamente.  
1.  Faça a auditoria da página novamente no painel **auditorias** .  Sua pontuação geral deve ter sido aprimorada novamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Um relatório de **auditorias** após a remoção dos recursos de bloqueio de renderização  
    :::image-end:::  
    
#### Otimizando o caminho de renderização crítica no mundo real  

O **caminho de renderização crítica** se refere ao código que você precisa para carregar uma página.  Em geral, acelere a carga da página, enviando apenas o código Critical durante o carregamento da página e, em seguida, carregando tudo o mais.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   É improvável que você possa encontrar scripts que você pode remover, mas pode encontrar muitos scripts que você não precisa solicitar durante o carregamento da página e, em vez disso, pode ser solicitado de forma assíncrona.  <!--See [Using async or defer][async].  -->  
*   Se você estiver usando uma estrutura, verifique se ela tem um modo de produção.  Esse modo pode usar um recurso como o de uma [árvore][WebpackTreeShaking] para eliminar o código desnecessário que está bloqueando o render crítico.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### Executar menos trabalho do thread principal  

O relatório mais recente mostra algumas economias em potencial mínimas na seção oportunidades, mas se você olhar para baixo na seção diagnósticos, parece que o maior afunilamento é muito grande na atividade thread principal.  

O thread principal é onde o navegador faz a maior parte do trabalho necessário para exibir uma página, como análise e execução de HTML, CSS e JavaScript.  

O objetivo é usar o painel desempenho para analisar qual trabalho o thread principal está fazendo enquanto a página é carregada e localizar maneiras de adiar ou remover o trabalho desnecessário.  

1.  Selecione a guia **desempenho** .  
1.  Escolha **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureIcon] \).  
1.  Defina a **rede** para 3G e **CPU** **lenta** para **6X de lentidão**.  Dispositivos móveis geralmente têm mais restrições de hardware do que laptops ou desktops, portanto, essas configurações permitem que você experimente a carga da página como se estivesse usando um dispositivo menos potente.  
1.  Escolha **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).  O DevTools atualiza a página e, em seguida, produz uma visualização de todo o trabalho realizado para carregar a página.  Essa visualização é chamada de **rastreamento**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       O rastreamento do painel **desempenho** do carregamento da página  
    :::image-end:::  
    
O rastreamento mostra a atividade cronologicamente, da esquerda para a direita.  Os gráficos de FPS, CPU e NET na parte superior fornecem uma visão geral de quadros por segundo, atividade de CPU e atividade de rede.  O bloco de amarelo selecionado que você vê na figura após o seguinte, a CPU estava completamente ocupada com a atividade de script.  Trata-se de uma pista de que você pode acelerar o carregamento da página fazendo menos trabalho em JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   A seção visão geral do rastreamento  
:::image-end:::  

Investigue o rastreamento para encontrar formas de fazer menos trabalho em JavaScript:  

1.  Selecione a seção **intervalos** para expandi-la.  De acordo com o fato de que pode haver uma série de medidas de [tempo][MDNUserTimingApi] de reagir, parece que o aplicativo de Tony está usando o modo de desenvolvimento de reagir.  Alternar para o modo de produção de reagir pode produzir um pouco de desempenho simples.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       A seção **intervalos**  
    :::image-end:::  
    
1.  Escolha **intervalos** novamente para recolher a seção.  
1.  Procure a seção **principal** .  Esta seção mostra um log cronológico da atividade de thread principal, da esquerda para a direita.  O eixo y (de cima para baixo) mostra o motivo pelo qual os eventos ocorreram.  Por exemplo, no figyre após o seguinte, o `Evaluate Script` evento causou a `(anonymous)` execução da função, que causou a execução `(anonymous)` , que causou `__webpack__require__` a execução e assim por diante.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       A seção **principal**  
    :::image-end:::  
    
1.  Role a tela para baixo até a parte inferior da seção **principal** .  Quando você usa uma estrutura, a maior parte da atividade superior é causada pela estrutura, que normalmente está fora do seu controle.  A atividade causada pelo aplicativo geralmente está na parte inferior.  Nesse aplicativo, parece que uma função nomeada `App` está causando muitas solicitações para uma `mineBitcoin` função.  Parece que Tony pode estar usando os dispositivos de seus fãs para o meu cryptocurrency...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Passe o mouse sobre a `mineBitcoin` atividade  
    :::image-end:::  
    
    > [!NOTE]
    > Embora as solicitações que a sua estrutura fazer normalmente sejam de seu controle, às vezes você pode estruturar seu aplicativo de uma maneira que faz com que a estrutura seja executada ineficientemente.  Reestruturar seu aplicativo para usar a estrutura com eficiência é uma maneira de fazer menos trabalho do thread principal.  No entanto, isso exige uma compreensão profunda de como a estrutura funciona e o tipo de alterações feitas em seu próprio código para usar a estrutura com mais eficiência.  
    
1.  Expanda a seção de **baixo para cima** .  Esta guia quebra quais atividades levaram mais tempo.  Se você não vir nada na seção Bottom-Up, clique no rótulo da seção **principal** .  A seção de **baixo para cima** mostra apenas as informações sobre qualquer atividade ou grupo de atividades selecionado no momento.  Por exemplo, se você clicou em uma das `mineBitcoin` atividades, a seção de **baixo para cima** só irá mostrar as informações de uma atividade.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       A guia **seta para baixo**  
    :::image-end:::  
    
A coluna **autotempo** mostra quanto tempo foi gasto diretamente em cada atividade.  Por exemplo, na figura a seguir, cerca de 63% do tempo do thread principal foi gasto na `mineBitcoin` função.  

Tempo para ver se o uso do modo de produção e da redução da atividade JavaScript pode acelerar o carregamento da página.  Comece com o modo de produção:  

1.  Na guia Editor, abra `webpack.config.js` .  
1.  Alterar `"mode":"development"` para `"mode":"production"` .  
1.  Aguarde até que a nova compilação seja implementada.  
1.  Faça a auditoria da página novamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Um relatório de auditorias após a configuração do webpack para usar o modo de produção  
    :::image-end:::  
    
Para reduzir a atividade do JavaScript, remova a solicitação para `mineBitcoin` :  

1.  Na guia Editor, abra `src/App.jsx` .  
1.  Comente a solicitação para `this.mineBitcoin(1500)` no (a) `constructor` .  
1.  Aguarde até que a nova compilação seja implementada.  
1.  Faça a auditoria da página novamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Tony o gato" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Um relatório de auditorias após remover o trabalho em JavaScript desnecessário  
    :::image-end:::  
    
Parece que essa última alteração causou um salto maciço no desempenho!  

> [!NOTE]
> Esta seção forneceu uma introdução breve ao painel desempenho.  Consulte [referência de análise de desempenho][DevtoolsEvaluatePerformanceReference] para saber mais sobre como analisar o desempenho da página.  

<!--todo: add section when available -->  

#### Como fazer o trabalho de threads principais no mundo real  

Em geral, o painel **desempenho** é a maneira mais comum de entender quais atividades o seu site faz ao carregar e encontrar maneiras de remover atividades desnecessárias.  

Se você preferir uma abordagem que se pareça mais `console.log()` , a [API de tempo do usuário][MDNUserTimingApi] permite marcar arbitrariamente determinadas fases do ciclo de vida do aplicativo, para controlar quanto tempo leva cada uma dessas fases.  

## Resumo  

*   Sempre que você tiver sido configurado para otimizar o desempenho de carga de um site, sempre comece com uma auditoria.  A auditoria estabelece uma linha de base e fornece dicas sobre como melhorar.  
*   Faça uma alteração de cada vez e faça a auditoria da página após cada alteração para ver como essa alteração afeta o desempenho.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referência de análise de desempenho | Documentos da Microsoft"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introdução à classe de desenvolvimento da Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Otimização de imagem essencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Diretivas-codificação de conteúdo | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de tempo do usuário | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Aperto de árvore | webpack"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
