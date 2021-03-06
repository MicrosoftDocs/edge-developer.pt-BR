---
description: Saiba como usar o Microsoft Edge DevTools para encontrar maneiras de fazer com que seus sites carreguem mais rápido.
title: Otimizar a velocidade do site com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7de97ab27528e89e2373e0a0d1002e8c86e37613
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398109"
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

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a>Otimizar a velocidade do site com o Microsoft Edge DevTools  

## <a name="goal-of-tutorial"></a>Objetivo do tutorial  

Este tutorial ensina como usar o Microsoft Edge DevTools para encontrar maneiras de fazer com que seus sites carreguem mais rapidamente.  

## <a name="prerequisites"></a>Pré-requisitos  

*   Você deve ter uma experiência básica de desenvolvimento da Web, semelhante ao que é ensinada nesta classe [Introdução ao Desenvolvimento da Web.][CourseraIntroductionWebDevelopmentClass]  
*   Você não precisa saber nada sobre o desempenho da carga.  Você aprenderá sobre isso neste tutorial.  

## <a name="introduction"></a>Introdução  

Este é Tony.  Tony é muito famoso na sociedade de gatos.  Ele criou um site para que seus fãs aprendam sobre suas comidas favoritas.  Seus fãs adoram o site, mas Tony continua ouvindo reclamações de que o site é carregado lentamente.  Tony pediu para ajudá-lo a acelerar o site.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony, o gato" lightbox="../media/speed-tony.msft.png":::
   Tony, o gato  
:::image-end:::  

## <a name="step-1-audit-the-site"></a>Etapa 1: Auditar o site  

Sempre que você se definir para melhorar o desempenho de carga de um site, **sempre comece com uma auditoria**.  
A auditoria tem duas funções importantes:  

*   Ele cria uma **linha de base** para você medir as alterações subsequentes.  
*   Ele fornece dicas **a actionable sobre** quais alterações têm mais impacto.  
    
### <a name="set-up"></a>Configurar  

Primeiro, você deve configurar o site para que possa fazer alterações nele mais tarde.  

1.  [Abra o código-fonte do site](https://glitch.com/edit/#!/tony).  Essa guia é conhecida como a **guia editor**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="A guia editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       A **guia editor**  
    :::image-end:::  
    
1.  Escolha **tony**.  Um menu é exibido.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="O menu que aparece depois de escolher Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       O menu que aparece depois de escolher **Tony**  
    :::image-end:::  
    
1.  Escolha **Projeto de Remix**.  O nome do projeto muda de **tony** para algum nome gerado aleatoriamente.  Agora você tem sua própria cópia editável do código.  Mais tarde, você pode fazer alterações nesse código.  
1.  Escolha **Mostrar** e escolher **Em uma nova janela**.  A demonstração é aberta em uma nova guia.  Essa guia é chamada de guia **de demonstração**.  Pode levar algum tempo para o site ser carregado.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="A guia demonstração" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       A guia demonstração  
    :::image-end:::  
    
1.  Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  O Microsoft Edge DevTools abre junto com a demonstração.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools e a demonstração" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools e a demonstração  
    :::image-end:::  
    
Para o restante das capturas de tela neste tutorial, DevTools é mostrado em uma janela separada.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Undock` **** para abrir o Menu de Comando, digitando e selecionando Desfazer em janela separada.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools DevTools desfaçada" lightbox="../media/speed-console.msft.png":::
   DevTools DevTools desfaçada  
:::image-end:::  

### <a name="establish-a-baseline"></a>Estabelecer uma linha de base  

A linha de base é um registro de como o site foi executado antes de você fazer quaisquer melhorias de desempenho.  

1.  Escolha a **ferramenta Auditorias.**  Ele pode estar oculto atrás do **botão Mais Painéis** \( ![ Mais ][ImageMorePanelsIcon] Painéis \).  Há um Farol neste painel porque o projeto que alimenta o painel de Auditorias é chamado **de Farol**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="A ferramenta Auditorias" lightbox="../media/speed-audits-performance.msft.png":::
       A **ferramenta Auditorias**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Corresponder as configurações de auditoria às da figura anterior.  Aqui está uma explicação das diferentes opções:  
    
    *   **Dispositivo**.  Definir como **Móvel** altera a cadeia de caracteres do agente do usuário e simula um visualizador móvel.  Definir como **Área de** Trabalho praticamente desliga as alterações **móveis.**  
    *   **Auditorias**.  Desativar uma categoria para impedir que o painel **de Auditorias** executa essas auditorias e exclui essas auditorias do seu relatório.  Deixe as outras categorias ativas, se quiser exibir os tipos de recomendações fornecidas.  Desativar categorias para acelerar ligeiramente o processo de auditoria.  
    *   **Throttling**.  Definido como **4G lento simulado,** a lentidão da CPU 4x simula as condições típicas de navegação em um dispositivo móvel.  Ele é chamado de "simulado" porque o painel De auditorias não realmente acelera durante o processo de auditoria.  Em vez disso, ele apenas extrapola quanto tempo a página leva para carregar em condições móveis.  A **configuração Aplicada...** por outro lado, realmente acelera sua CPU e rede, com a troca de um processo de auditoria mais longo.  
    *   **Limpar Armazenamento**.  Ativar a caixa de seleção para limpar todo o armazenamento associado à página antes de cada auditoria.  Deixe essa configuração em caso de você querer auditar como os visitantes pela primeira vez experimentam seu site.  Desativar essa configuração quando quiser a experiência de visita repetida.  
    
1.  Escolha **Executar Auditorias**.  Após 10 a 30 segundos, o painel **Auditorias** exibe um relatório do desempenho do site.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="O relatório do painel Auditorias do desempenho do site" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       O relatório do painel Auditorias do desempenho do site  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a>Manipulando erros de relatório  

Se você receber um erro no relatório do painel Auditorias, tente executar a guia demonstração de uma janela **InPrivate** sem nenhuma outra guia aberta.  Isso garante que você está executando o Microsoft Edge de um estado limpo.  Extensões do Microsoft Edge, em particular, frequentemente interferem no processo de auditoria.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a>Compreender seu relatório  

O número na parte superior do relatório é a pontuação geral de desempenho do site.  Mais tarde, conforme você faz alterações no código, o número exibido deve aumentar.  Uma pontuação mais alta significa melhor desempenho.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="A pontuação geral do desempenho" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   A pontuação geral do desempenho  
:::image-end:::  

A **seção Metrics** fornece medidas quantitativos do desempenho do site.  Cada métrica fornece informações sobre um aspecto diferente do desempenho.  Por exemplo, First **Contentful Paint** informa quando o conteúdo é pintado pela primeira vez na tela, o que é um marco importante na percepção do usuário sobre a carga da página, enquanto Time **To Interactive** marca o ponto no qual a página aparece pronta o suficiente para lidar com interações do usuário.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="A seção Métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   A **seção Métricas**  
:::image-end:::  

Escolha o botão de alternância realçada na figura a seguir para exibir uma descrição para cada métrica e escolha **Saber mais** para ler a documentação sobre ela.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Escolha o botão de alternância realçada para expandir os itens Metrics" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Escolha o botão de alternância realçada para expandir os itens Metrics  
:::image-end:::  

Abaixo Métricas está uma coleção de capturas de tela que mostram como a página era carregada.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de tela de como a página era durante o carregamento" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Capturas de tela de como a página era durante o carregamento  
:::image-end:::  

A **seção Oportunidades** fornece dicas específicas sobre como melhorar o desempenho da carga desta página específica.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="A seção Oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   A **seção Oportunidades**  
:::image-end:::  

Escolha uma oportunidade para saber mais sobre isso.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar a oportunidade de recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Eliminar a oportunidade de recursos de bloqueio de** renderização  
:::image-end:::  

Escolha **Saiba mais para** exibir a documentação sobre por que uma oportunidade é importante e recomendações específicas sobre como corrigi-la.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentação para a oportunidade de eliminar recursos de bloqueio de renderização" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Documentação para a **oportunidade de eliminar recursos de bloqueio de renderização**  
:::image-end:::  

A **seção Diagnóstico** fornece mais informações sobre fatores que contribuem para o tempo de carregamento da página.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="A seção Diagnóstico" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   A **seção Diagnóstico**  
:::image-end:::  

A **seção Auditorias Passadas** mostra o que o site está fazendo corretamente.  Escolha expandir a seção.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="A seção Auditorias Aprovadas" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   A **seção Auditorias Aprovadas**  
:::image-end:::  

## <a name="step-2-experiment"></a>Etapa 2: Experimento  

A seção Oportunidades do relatório de auditoria fornece dicas sobre como melhorar o desempenho da página.  Nesta seção, você implementa as alterações recomendadas na base de código, auditando o site após cada alteração para medir como ele afeta a velocidade do site.  

### <a name="enable-text-compression"></a>Habilitar compactação de texto  

Seu relatório diz que evitar enormes cargas de rede é uma das principais oportunidades para melhorar o desempenho da página.  Habilenciar a compactação de texto é uma oportunidade para melhorar o desempenho da página.  

A compactação de texto é quando você reduz ou compacta o tamanho de um arquivo de texto antes de enviá-lo pela rede.  Semelhante à forma como você pode arquivar um diretório antes de enviá-lo para reduzir o tamanho.  

Antes de habilitar a compactação, aqui estão algumas maneiras de verificar manualmente se os recursos de texto são compactados.  

1.  Escolha a **ferramenta Rede.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="O painel Rede" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       A **ferramenta Rede**  
    :::image-end:::  
    
1.  Escolha o **ícone de configuração de** rede.  
1.  Escolha a **caixa de seleção Usar linhas de solicitação** grandes.  A altura das linhas na tabela de solicitações de rede aumenta.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Linhas grandes na tabela de solicitações de rede" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Linhas grandes na tabela de solicitações de rede  
    :::image-end:::  
    
1.  Se a **coluna Tamanho** na tabela de solicitações de rede não for exibida, escolha o header de tabela > **Size**.  

Cada **célula Size** mostra dois valores.  O valor superior é o tamanho do recurso baixado.  
O valor inferior é o tamanho do recurso não compactado.  Se os dois valores são os mesmos, o recurso não está sendo compactado quando é enviado pela rede.  Por exemplo, na figura anterior, os valores superior e inferior `bundle.js` para são `1.2 MB` e `1.2 MB` .  

Verifique se há compactação inspecionando os cabeçalhos HTTP de um recurso:  

1.  Escolha `bundle.js` .  
1.  Escolha o **painel Headers.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="O painel Headers" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       O **painel Headers**  
    :::image-end:::  
    
1.  **Pesquise** na seção Headers de Resposta para um `content-encoding` header.  Um `content-encoding` título não é exibido, o que significa que não foi `bundle.js` compactado.  Quando um recurso é compactado, esse header geralmente é definido como `gzip` `deflate` , ou `br` .  Para uma explicação dos valores, navegue até [Diretivas][MDNContentEncodingDirectives].  

Chega de explicações.  Hora de fazer algumas alterações.  Habilita a compactação de texto adicionando algumas linhas de código:  

1.  Na guia editor, escolha **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Editar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Editar `server.js`  
    :::image-end:::  
    
1.  Adicione o código a seguir ** aserver.js**.  Certifique-se de colocar `app.use(compression())` antes `app.use(express.static('build'))` .  

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
    > Normalmente, você precisa instalar o pacote por meio de algo como , mas `compression` isso já foi feito para `npm i -S compression` você.  
    
1.  Aguarde a falha para implantar a nova com build do site.  A animação sofisticada ao lado **de Ferramentas** significa que o site está sendo reconstruído e reimplantado.  A alteração estará pronta quando a animação ao lado de **Ferramentas** desaparecer.  Escolha **Mostrar** e escolha **Em uma nova janela** novamente.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Use os fluxos de trabalho que você aprendeu anteriormente para verificar manualmente se a compactação está funcionando:  

1.  Volte para a guia demonstração e atualize a página.  A **coluna Tamanho** agora deve mostrar 2 valores diferentes para recursos de texto como `bundle.js` .  Na figura após o seguinte, o valor superior de for é o tamanho do arquivo que foi enviado pela rede, e o valor inferior de é o tamanho do arquivo não `256 KB` `bundle.js` `1.2 MB` compactado.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="A coluna Tamanho agora mostra 2 valores diferentes para recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       A **coluna Tamanho** agora mostra 2 valores diferentes para recursos de texto  
    :::image-end:::  
    
1.  A **seção Headers de** Resposta agora deve incluir um `bundle.js` `content-encoding: gzip` header.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="A seção Headers de Resposta agora contém um header de codificação de conteúdo" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       A **seção Headers de** Resposta agora contém um header de codificação de conteúdo  
    :::image-end:::  
    
Audite a página novamente para medir que tipo de compactação de texto de impacto tem no desempenho da carga da página:  

1.  Escolha a **ferramenta Auditorias.**  
1.  Escolha **Executar uma auditoria** \( Executar uma auditoria ![ ][ImagePerformIcon] \).  
1.  Deixe as configurações da mesma forma de antes.  
1.  Escolha **Executar auditoria**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Um relatório de Auditorias após habil passada a compactação de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Um relatório de Auditorias após habil passada a compactação de texto  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Sua pontuação geral de desempenho deve ter aumentado, o que significa que o site está ficando mais rápido.  

#### <a name="text-compression-in-the-real-world"></a>Compactação de texto no mundo real  

A maioria dos servidores realmente tem correções simples como esta para habilenciar a compactação!  Basta fazer uma pesquisa sobre como configurar qualquer servidor que você usa para compactar texto.  

### <a name="resize-images"></a>Resize imagens  

Seu relatório indica que evitar cargas de rede enormes é uma das principais oportunidades para melhorar o desempenho da página.  Resizing images helps reduce the size of the network payload.  Se o usuário estiver exibindo suas imagens em uma tela de dispositivo móvel com 500 pixels de largura, não há realmente nenhum ponto em enviar uma imagem de 1500 pixels de largura.  O ideal é enviar uma imagem de 500 pixels no máximo.  

1.  No relatório, escolha **Evitar cargas de** rede enormes para exibir quais imagens devem ser resized.  Parece que 2 dos arquivos jpg têm mais de 2.000 KB, o que é maior do que o necessário.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  De volta à guia editor, abra `src/model.js` .  
1.  Substitua `const dir = 'big'` por `const dir = 'small'` .  Esse diretório contém cópias das mesmas imagens que foram resized.  
1.  Audite a página novamente para exibir como a alteração afeta o desempenho da carga.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Um relatório de auditorias após rea reizing imagens" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Um relatório de auditorias após rea reizing imagens  
    :::image-end:::  
    
A alteração exibida tem apenas um pequeno efeito na pontuação geral do desempenho.  No entanto, uma coisa que a pontuação não mostra claramente é quantos dados de rede você está salvando seus usuários.  O tamanho total das fotos antigas era de cerca de 5,3 megabytes, enquanto agora é de apenas cerca de 0,18 megabytes.  

#### <a name="resizing-images-in-the-real-world"></a>Resizing images in the real world  

Para um aplicativo pequeno, fazer um resize único como este pode ser bom o suficiente.  Mas para um aplicativo grande, isso obviamente não é escalonável.  Aqui estão algumas estratégias para gerenciar imagens em aplicativos grandes:  

*   Resize imagens durante o processo de com build.  
*   Crie vários tamanhos de cada imagem durante o processo de com build e use `srcset` em seu código.  Em tempo de execução, o navegador cuida de escolher qual tamanho é melhor para o dispositivo.  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Use uma CDN de imagem que permite reorganizar dinamicamente uma imagem ao solicitá-la.  
*   No mínimo, otimize cada imagem.  Isso pode criar grandes economias.  
  Otimização é quando você executar uma imagem por meio de um programa especial que reduz o tamanho do arquivo de imagem.  Para obter mais dicas, navegue até [Essential Image Optimization][EssentialImageOptimization].  
    
### <a name="eliminate-render-blocking-resources"></a>Eliminar recursos de bloqueio de renderização  

Seu relatório mais recente diz que a eliminação de recursos de bloqueio de renderização agora é a maior oportunidade.  

Um recurso de bloqueio de renderização é um arquivo JavaScript ou CSS externo que o navegador deve baixar, analisar e executar antes de exibir a página.  O objetivo é executar apenas o CSS principal e o código JavaScript necessário para exibir a página corretamente.  

A primeira tarefa, então, é encontrar o código que você não precisa executar no carregamento da página.  

1.  Escolha **Eliminar recursos de bloqueio de renderização** para exibir os recursos que estão bloqueando:  
    `lodash.js` e `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Mais informações sobre a oportunidade De eliminar recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Mais informações sobre a oportunidade **De eliminar recursos de bloqueio de renderização**  
    :::image-end:::  
    
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) `Coverage` **** para abrir o Menu de Comando, começar a digitar e, em seguida, escolher Mostrar Cobertura .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abra o Menu de Comando no painel Auditorias" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Abra o Menu de Comando no **painel Auditorias**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="A ferramenta Coverage" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       A **ferramenta Coverage**  
    :::image-end:::  
    
1.  Escolha **Atualizar** \( ![ Atualizar ][ImageRefreshIcon] \).  A **ferramenta Coverage** fornece uma visão geral de quanto do código em , e é executado enquanto a página é `bundle.js` `jquery.js` `lodash.js` carregada.  Na figura após o seguinte, cerca de 76% e 30% dos arquivos jQuery e Lodash não são usados, respectivamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="O relatório de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       O relatório de cobertura  
    :::image-end:::  
    
1.  Escolha a **linhajquery.js.**  O DevTools abre o arquivo no painel Fontes.  Uma linha de código foi seguida se tiver uma barra azul ao lado dela.  Uma barra vermelha significa que não foi executado e, definitivamente, não é necessário no carregamento da página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Exibindo o arquivo jQuery no painel Fontes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Exibindo o arquivo jQuery no painel **Fontes**  
    :::image-end:::  
    
1.  Role um pouco pelo código jQuery.  Algumas das linhas que são "executar" são, na verdade, apenas comentários.  Executar esse código por meio de um minifier que tira comentários é outra maneira de reduzir o tamanho desse arquivo.  

Em resumo, quando você está trabalhando com seu próprio código, a ferramenta **Coverage** ajuda você a analisar seu código, linha por linha e apenas enviar o código necessário para a carga da página.  

Os `jquery.js` arquivos e `lodash.js` são necessários para carregar a página?  A **ferramenta de bloqueio** solicitação exibe o que acontece quando os recursos não estão disponíveis.  

1.  Escolha a **ferramenta Rede.**  
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) para abrir o Menu de Comando novamente.  
1.  Comece a digitar `blocking` e escolha Mostrar Bloqueio de **Solicitação.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="A ferramenta de bloqueio solicitação" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       A **ferramenta de bloqueio solicitação**  
    :::image-end:::  
    
1.  Escolha **Adicionar Padrão** \( Adicionar Padrão ![ ][ImageAddPatternIcon] \), digite e selecione `/libs/*` `Enter` confirmar.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Adicionar um padrão para bloquear qualquer solicitação ao diretório libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Adicionar um padrão para bloquear qualquer solicitação ao `libs` diretório  
    :::image-end:::  
    
1.  Atualize a página.  As solicitações jQuery e Lodash são vermelhas, o que significa que as solicitações foram bloqueadas.   A página ainda é carregada e interativa, portanto, parece que esses recursos não são necessários!  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="O painel Rede mostra que as solicitações foram bloqueadas" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       A **ferramenta Rede** mostra que as solicitações foram bloqueadas  
    :::image-end:::  
    
1.  Escolha **Remover todos os padrões** \( Remover todos os padrões ![ ][ImageRemoveIcon] \) para excluir o padrão de `/libs/*` bloqueio.  
    
Em geral, a **ferramenta de** bloqueio solicitação é útil para simular como sua página se comporta quando um determinado recurso não está disponível.  

Agora, remova as referências a esses arquivos do código e audite a página novamente:  

1.  De volta à guia editor, abra `template.html` .  
1.  Exclua `<script src="/libs/lodash.js">` e `<script src="/libs/jquery.js"></script>`.  
1.  Aguarde até que o site seja rea build and re-deploy.  
1.  Audite a página novamente da **ferramenta Auditorias.**  Sua pontuação geral deve ter melhorado novamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Um relatório de auditorias após remover os recursos de bloqueio de renderização" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Um **relatório de auditorias** após remover os recursos de bloqueio de renderização  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a>Otimizando o Caminho crítico de renderização no mundo real  

O **Caminho de Renderização Crítico** refere-se ao código que você precisa carregar uma página.  Em geral, acelere a carga da página enviando apenas código crítico durante a carga da página e carregando todo o resto.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   É improvável que você consiga encontrar scripts que você possa remover de imediato, mas pode encontrar muitos scripts que você não precisa solicitar durante a carga da página e, em vez disso, pode ser solicitado de forma assíncrona.  <!--Navigate to [Using async or defer][async].  -->  
*   Se você estiver usando uma estrutura, verifique se ela tem um modo de produção.  Esse modo pode usar um recurso como [tremedeira][WebpackTreeShaking] de árvore para eliminar o código desnecessário que está bloqueando a renderização crítica.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a>Fazer menos trabalho de thread principal  

Seu relatório mais recente mostra algumas pequenas economias potenciais na seção Oportunidades, mas se você olhar para baixo na seção Diagnósticos, parece que o maior a gargalo é a atividade de thread principal demais.  

O thread principal é onde o navegador faz a maior parte do trabalho necessário para exibir uma página, como analisar e executar HTML, CSS e JavaScript.  

O objetivo é usar o painel Desempenho para analisar o trabalho que o thread principal está fazendo enquanto a página é carregada e encontrar maneiras de adiar ou remover o trabalho desnecessário.  

1.  Escolha a **ferramenta Desempenho.**  
1.  Escolha **Configurações de Captura** \( ![ Configurações de Captura ][ImageCaptureIcon] \).  
1.  Definir **Rede como** Slow **3G** e **CPU** como **6x de lentidão**.  Dispositivos móveis geralmente têm mais restrições de hardware do que laptops ou desktops, portanto, essas configurações permitem que você experimente a carga da página como se você estivesse usando um dispositivo menos poderoso.  
1.  Escolha **Atualizar** \( ![ Atualizar ][ImageRefreshIcon] \).  O DevTools atualiza a página e produz uma visualização de todo o trabalho executado para carregar a página.  Essa visualização é chamada de **rastreamento**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="O rastreamento da ferramenta Performance da carga da página" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       O **rastreamento da** ferramenta Performance da carga da página  
    :::image-end:::  
    
O rastreamento mostra a atividade cronologicamente, da esquerda para a direita.  Os gráficos FPS, CPU e NET na parte superior dão uma visão geral dos quadros por segundo, atividade da CPU e atividade de rede.  O bloco de amarelo realçado na figura após o próximo, a CPU estava completamente ocupada com a atividade de script.  Esta é uma dica de que você pode ser capaz de acelerar a carga da página fazendo menos trabalho javaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="A seção Visão geral do rastreamento" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   A seção Visão geral do rastreamento  
:::image-end:::  

Investigue o rastreamento para encontrar maneiras de fazer menos trabalho do JavaScript:  

1.  Escolha a **seção Timings** para expandi-la.  Com base no fato de que pode haver várias medidas de [Timings][MDNUserTimingApi] do React, parece que o aplicativo de Tony está usando o modo de desenvolvimento do React.  Alternar para o modo de produção do React pode gerar algumas vitórias de desempenho fáceis.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="A seção Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       A **seção Timings**  
    :::image-end:::  
    
1.  Escolha **Timings** novamente para fechar essa seção.  
1.  Navegue pela **seção** Principal.  Esta seção mostra um log cronologicamente da atividade principal do thread, da esquerda para a direita.  O eixo y (de cima para baixo) mostra por que os eventos ocorreram.  Por exemplo, na figueira após o seguinte, o evento fez com que a função seja executado, o que causou a sua executar, o que causou a sua realização `Evaluate Script` `(anonymous)` e assim por `(anonymous)` `__webpack__require__` diante.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="A seção Principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       A **seção** Principal  
    :::image-end:::  
    
1.  Role para baixo até a parte inferior da **seção** Principal.  Quando você usa uma estrutura, a maior parte da atividade superior é causada pela estrutura, que geralmente está fora de seu controle.  A atividade causada pelo aplicativo geralmente está na parte inferior.  Neste aplicativo, parece que uma função chamada `App` está causando muitas solicitações a uma `mineBitcoin` função.  Parece que Tony pode estar usando os dispositivos de seus fãs para minerar a criptografia...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Passe o mouse na atividade mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Passe o mouse na `mineBitcoin` atividade  
    :::image-end:::  
    
    > [!NOTE]
    > Embora as solicitações que sua estrutura faça geralmente estão fora de seu controle, às vezes, você pode estruturar seu aplicativo de uma maneira que faça com que a estrutura seja executado de forma ineficiente.  Reestruturar seu aplicativo para usar a estrutura com eficiência é uma maneira de fazer menos trabalho de thread principal.  No entanto, isso requer uma compreensão profunda de como sua estrutura funciona e que tipo de alterações você faz em seu próprio código para usar a estrutura com mais eficiência.  
    
1.  Expanda **a seção Bottom-Up.**  Essa guia divide quais atividades demorou mais tempo.  Se nada for exibido na seção Bottom-Up, escolha o rótulo para **a seção** Principal.  A **seção Bottom-Up** mostra apenas informações para qualquer atividade ou grupo de atividades que você selecionou no momento.  Por exemplo, se você escolher uma das atividades, a seção `mineBitcoin` **Bottom-Up** mostrará apenas informações para essa atividade.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="A Bottom-Up guia" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       A **guia Bottom-Up**  
    :::image-end:::  
    
A **coluna Tempo Próprio** mostra quanto tempo foi gasto diretamente em cada atividade.  Por exemplo, na figura a seguir, cerca de 63% do tempo de thread principal foi gasto na `mineBitcoin` função.  

Hora de revisar se o uso do modo de produção e a redução da atividade javaScript podem acelerar a carga da página.  Comece com o modo de produção:  

1.  Na guia editor, abra `webpack.config.js` .  
1.  Altere `"mode":"development"` para `"mode":"production"` .  
1.  Aguarde a implantação do novo build.  
1.  Audite a página novamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Um relatório de Auditorias após configurar o webpack para usar o modo de produção" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Um relatório de Auditorias após configurar o webpack para usar o modo de produção  
    :::image-end:::  
    
Reduza a atividade do JavaScript removendo a solicitação para `mineBitcoin` :  

1.  Na guia editor, abra `src/App.jsx` .  
1.  Comente a solicitação `this.mineBitcoin(1500)` no `constructor` .  
1.  Aguarde a implantação do novo build.  
1.  Audite a página novamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Um relatório de auditorias após remover o trabalho desnecessário do JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Um relatório de auditorias após remover o trabalho desnecessário do JavaScript  
    :::image-end:::  
    
Parece que a última alteração causou um grande salto no desempenho!  

> [!NOTE]
> Esta seção forneceu uma breve introdução ao painel Desempenho.  Para saber mais sobre como analisar o desempenho da página, navegue até [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a>Fazendo menos trabalho de thread principal no mundo real  

Em geral, a **ferramenta Performance** é a maneira mais comum de entender quais atividades o site faz à medida que carrega e encontrar maneiras de remover atividades desnecessárias.  

Se você preferir uma abordagem que se parece mais com , a API de Tempo do Usuário permite marcar arbitrariamente determinadas fases do ciclo de vida do aplicativo, a fim de rastrear quanto tempo cada uma dessas `console.log()` fases leva. [][MDNUserTimingApi]  

## <a name="summary"></a>Resumo  

*   Sempre que você se definir para otimizar o desempenho de carga de um site, sempre comece com uma auditoria.  A auditoria estabelece uma linha de base e fornece dicas sobre como melhorar.  
*   Faça uma alteração por vez e audite a página da Web após cada alteração para exibir como essa alteração isolada afeta o desempenho.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

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

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referência de análise de desempenho | Microsoft Docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introdução à classe desenvolvimento web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Otimização de Imagem Essencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Diretivas - Codificação de | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Api de tempo do usuário | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Árvore | webpack"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
