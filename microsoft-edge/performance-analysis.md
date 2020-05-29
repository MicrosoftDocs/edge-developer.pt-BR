---
ms.assetid: 7a5f9fd0-90a9-43db-b271-178c06da5896
description: Use as ferramentas de desenvolvedor F12 para analisar o desempenho geral dos sites.
title: Análise de desempenho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/08/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 7bf71744298502c9edf8ee1262fceff5640bedf1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562481"
---
# Análise de desempenho

Se você não tem experiência com o desempenho, consulte o [Guia de devtools F12](./devtools-guide.md).
As [Ferramentas F12](./devtools-guide.md) incorporadas ao Microsoft Edge podem ser usadas para analisar o desempenho geral de um site da Web. Ele fornece recursos semelhantes (mas mais limitados) ao [Kit de ferramentas de desempenho do Windows](https://docs.microsoft.com/windows-hardware/test/wpt/index) diretamente no navegador.



Se você quiser uma análise mais profunda do desempenho do navegador, a equipe do Microsoft Edge usa o [Windows Performance Toolkit](https://docs.microsoft.com/windows-hardware/test/wpt/index) (WPT). O WPT foi criado pela equipe do Windows para realizar análises detalhadas de desempenho do programa. Ele se espalha pelos limites entre o site JavaScript e o código nativo do Microsoft Edge, permitindo que ambos sejam exibidos dentro da mesma ferramenta. WPT pode ser usado para:
 - Medir o tempo de CPU usado para o software concluir o trabalho
 - Calcular a memória alocada por software
 - Mostrar os detalhes do download de arquivos de servidores remotos
 - Avalie a taxa de quadros.


Para começar a usar o kit de ferramentas de desempenho do Windows para analisar seu site, você precisa primeiro baixar o [Kit de avaliação e implantação do Windows 10 (ADK)](https://developer.microsoft.com/windows/hardware/windows-assessment-deployment-kit). Selecione a opção *Windows Performance Toolkit* durante a instalação:

![Opções de instalação do ADK](./media/adk-installoptions.png)

Aqui, abordaremos como gravar e analisar um rastreamento de desempenho. Para saber mais sobre o que está incluído no kit de ferramentas de desempenho do Windows, confira a documentação completa do [WPT](https://docs.microsoft.com/windows-hardware/test/wpt/index).

## Gravando um rastreamento
Em seguida, configure o cenário do usuário e prepare-se para coletar um rastreamento usando o gravador de desempenho do Windows.
Veja como criar o perfil do seu cenário da Web com o *gravador de desempenho do Windows (WPR)*.

### 1. preparar seu ambiente para coletar um rastreamento de desempenho
Encerre o maior número possível de programas em execução para evitar ruído no rastreamento que você está prestes a gravar. O ideal é que o único software em execução seja o gravador de desempenho do Windows (WPR) e o navegador.

### 2. Inicie o gravador de desempenho do Windows (WPR) e selecione opções
Inicie o gravador de desempenho do Windows e assegure-se de que **mais opções** de alternância sejam expandidas. Selecione as caixas de seleção do *navegador de bordas* e cenário de *capacidade de resposta HTML* .

![Opções de registro de desempenho do Windows](./media/wprui-options.png)

#### Dicas e truques para reunir rastreamentos
- Tente manter a atividade em segundo plano em um mínimo obrigatório absoluto. Processos em segundo plano podem distorcer o desempenho percebido e as características de desempenho real e afetar os resultados. Idealmente, não há outros aplicativos em execução ao lado do navegador e do WPR.
- Identifique os cenários que você está analisando e tente mantê-los o mais atômico possível. Por exemplo, se o seu site tiver problemas de desempenho ao carregar a página, a rolagem e a seleção de algo em uma tabela, separe os problemas em três cenários:
  - Carregamento da página (desde o início da navegação até a carga da página concluída)
  - Rolagem
  - Selecionar algo na tabela
- Se um cenário envolve navegar para um site, considere iniciar o cenário em sobre: em branco. A partir de: em branco, evitará a sobrecarga da página anterior. Se ele envolver a navegação longe de um site, navegue até sobre: em branco para concluir o cenário. Isso impedirá o ruído de outros sites do rastreamento, a menos que a interação específica entre sites seja o problema de investigação.

### 3. Registre o cenário
Clique em **Iniciar** para começar a gravar. A ferramenta irá relatar o tamanho do buffer que está usando para ajudar você a prever o tamanho do arquivo gerado. Execute o cenário do usuário que você deseja medir e, em seguida, clique em **salvar** para parar a gravação e salvar o rastreamento. Salvar logo após concluir o cenário ajudará a minimizar o tamanho do arquivo de rastreamento.

![Início do registro de desempenho do Windows](./media/wprui-recording.png)

A ferramenta WPR indicará que as informações de rastreamento foram salvas com êxito:

![Início do registro de desempenho do Windows](./media/wprui-savecomplete.png)


## Analisando um rastreamento
Agora que você coletou seus dados de desempenho, pode analisar o rastreamento usando o analisador de desempenho do Windows para ver quais otimizações podem ser feitas.
Veja aqui como analisar seus dados de desempenho do cenário Web.

### 1. abrir o Windows Performance Analyzer (WPA)
Inicie o analisador de desempenho do Windows e abra o `.etl` arquivo a ser analisado (**arquivo**  >  **aberto...**).

### 2. carregar símbolos e aplicar o perfil de *análise HTML*

>[!WARNING]
> Carregar símbolos pela primeira vez exigirá um download grande e levará um tempo significativo em uma conexão de Internet típica.

Carregue seus símbolos selecionando **rastrear**  >  **carregar símbolos** no menu. Os símbolos serão armazenados em cache em disco e os rastreamentos futuros carregarão os símbolos muito mais rapidamente.

Você pode carregar símbolos de forma mais rápida, restringindo o carregamento para o Microsoft Edge e o host de aplicativos Web. Selecione **rastrear**  >  **Configurar símbolos** e restringir as **configurações de carregar** apenas `MicrosoftEdgeCP.exe` e `WWAHost.exe` .

![Restrições de símbolo](./media/wpa-symbolrestrictions.png)

Depois que os símbolos começarem a ser carregados, aplique o *perfil de análise HTML* (**perfis**  >  **se aplicam...**  >  **Procurar catálogo..**  >  . **HtmlResponsivenessAnalysis. wpaProfile**) o perfil irá carregar vários gráficos e tabelas para a sua análise. Para praticamente todas as investigações de sites, recomendamos iniciar com este perfil.

![Visão geral](./media/wpa-bigpicture.png)


#### O perfil de análise de capacidade de resposta HTML
O perfil de análise de *capacidade de resposta HTML* fornece quatro guias:

**Visão geral** : isso é útil para confirmar que não há fontes inesperadas de atividade da CPU e o navegador está usando todos os recursos disponíveis. Verifique o uso da CPU e certifique-se de que nenhum processo contribua significativamente com o uso da CPU diferente do navegador.

**Análise de quadros** -esta seção é usada para análise básica. O gráfico *uso da CPU (atribuído)* permite um relance rápido para a compreensão dos subsistemas responsáveis pelo uso da CPU. Quebrar os exemplos na tabela *uso da CPU (amostrad)* no *thread da interface do usuário HTML* é útil para identificar afunilamentos de desempenho críticos.

**Marcadores de rastreamento** -esta seção mostra todos os marcadores de rastreamento que vêm do navegador (Microsoft Edge), incluindo *msWriteProfilerMark*, que fornece pontos precisos para medir o código. Para ver o rastreamento do *msWriteProfilerMark* , role para baixo até o gráfico de *eventos genéricos* e selecione **HTML msWriteProfilerMark** no menu suspenso.

**Análise de atraso de threads** – essa guia geralmente é usada pelos desenvolvedores do Microsoft Edge para investigar quando um thread está bloqueado e aguardando em outro. Em raras ocasiões, também pode ser útil para os desenvolvedores da Web.


### 3. zoom para remover o resumo do rastreamento
Você pode focalizar sua análise removendo as seções de *Resumo de rastreamento* de rastros vazias de seus gráficos. Em qualquer um dos gráficos que está mostrando:
 - Clique com o botão esquerdo no início dos dados do gráfico que você deseja investigar
 - Segure, arraste e solte para selecionar a região desejada
 - Clique com o botão direito do mouse e selecione **zoom**

O zoom será aplicado a todos os gráficos e gráficos na guia ativa.

![Postar zoom](./media/wpa-postzoom.png)


### 4. investigue o que está ocupando ciclos de CPU
 A tabela **uso da CPU (amostraada)** na guia **análise de quadro** é onde a maior parte da sua análise provavelmente acontecerá. Você pode expandir os vários processos para identificar o código JavaScript e o código do navegador com maior volume de computação. Geralmente, um único pouco de JavaScript é responsável por um problema de desempenho e levar o tempo para otimizá-lo pode fazer uma diferença significativa.

### 5. analisar em qualquer código JavaScript de execução lenta
A análise de chamadas de DOM de baixo pode ser útil para identificar o JavaScript responsável por ocupar a maioria do tempo durante o cenário. Isso é especialmente útil quando muitas chamadas de nível superior são reutilizadas as mesmas bibliotecas JavaScript.

Comece examinando a *divisão de uso da CPU (amostrad) por processo, thread, atividade, pilha*. Clique em qualquer célula na coluna **empilhada** . Pressione *Ctrl + F* e procure por *ExternalFunctionThunk*.

>[!NOTE] 
>Isso só funcionará se você tiver carregado símbolos com êxito.

![Procurar ExternalFunctionThunk](./media/wpa-externalfunctionthunk.png)

Investigue todas as linhas com o *ExternalFunctionThunk*. Essa é a interface do mecanismo JavaScript Chakra para o mecanismo Microsoft Edge. Ele mostra onde as pontes de código do navegador para a execução de JavaScript. Clique com o botão direito do mouse na linha e selecione **Exibir chamadas**  >  **por módulo** para ver uma lista ponderada das funções mais longas do mecanismo do navegador.

![Exibir chamadas](./media/wpa-viewcallees.png)

Para identificar todo o JavaScript chamando uma API específica, clique com o botão direito do mouse nele e selecione **Exibir chamadores**  >  **por função** e expanda a árvore para exibir e comparar os pesos relativos.
