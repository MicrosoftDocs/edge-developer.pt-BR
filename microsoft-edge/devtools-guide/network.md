---
description: Usar o painel rede para monitorar e criar o perfil de solicitações de recursos de página
title: DevTools-rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, rede, tempo de carregamento, http, HTTPS, cache do navegador, HAR
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561396"
---
# Rede

Use o painel **rede** para monitorar, inspecionar e criar perfil das solicitações e respostas enviadas pela transmissão. Com ele, você pode:

 - [Procurar um registro de todas as solicitações de recursos](#network-summary) feitas pela página
 - [Meça o tempo de carregamento do seu site](#summary-bar) para novos e devolver usuários 
 - [Inspecione os cabeçalhos, corpos de mensagens, parâmetros e cookies](#request-details) trocados entre a sua página e a rede
 - [Identifique os eventos de rede que causam afunilamentos](#timings) no tempo de carregamento do seu site

![O painel de rede do Microsoft Edge DevTools](./media/network.png)

## Resumo da rede

Quando você abre o DevTools, a criação de perfil de rede é ativada por padrão. Todo o tráfego de rede da guia ativa do navegador é gravado na lista Resumo da rede, mesmo quando você está trabalhando em um painel DevTools diferente da *rede*.

![Indicador de perfil de rede em andamento](./media/network_profile_indicator.png)

### Barra de ferramentas

A barra de ferramentas fornece controles para perfilar e filtrar a atividade de rede de sua página. 

![Barra de ferramentas perfil de rede](./media/network_toolbar.png)

1. **Iniciar/parar sessão de criação de perfil**: por padrão, o profiling de rede está ativado, e o tráfego de rede será registrado na lista do [**perfil de rede**](#network-request-list) . Você pode desativar a captura de rede com o botão **parar** ( `Ctrl+E` ).

2. **Exportar como Har**: você pode salvar a sessão atual de criação de perfil de rede ( `Ctrl+S` ) como um arquivo de arquivo http formatado para JSON [(Har)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) . 

3. **Filtro de tipo de conteúdo**: filtrar a lista de solicitações de rede por solicitações de conteúdo específicas (*documentos, folhas de estilos, imagens, scripts, mídia, fontes, XHR, outros*). Por padrão, todos os tipos de conteúdo são mostrados.

4. **Find**: Filter ( `Ctrl+F` ) a lista de solicitação de rede por nomes de entrada (caminhos de recursos) contendo uma cadeia de pesquisa especificada.

5. **Sempre atualizar do servidor**: a desativação desse botão forçará os recursos da página a carregar da rede, em vez do cache do navegador. Você pode atualizar a página da rede de uma única vez pressionando `Ctrl+F5` .

6. **Ignorar o trabalho de serviço para todas as solicitações de rede**: Desabilite seus trabalhadores de serviço cadastrados como proxies de rede. 

7. Botões limpar

   - **Limpar cache**: Remove todos os recursos armazenados no cache do navegador (e emula uma experiência de primeira hora carregando a página).
   - **Limpar cookies**: Remove todos os cookies para o domínio especificado (e emula uma experiência de primeira vez do site).
   - **Limpar entradas ao navegar**: o tráfego gravado é limpo na navegação da página. Isso é ativado por padrão.
   - **Limpar sessão**: limpa todas as entradas de solicitação de rede na lista **Resumo da rede** .

### Lista de solicitações de rede

Todo o tráfego de rede é gravado em uma lista (até ser limpo após a navegação, desmarcada manualmente ou DevTools são fechadas). Clicar em qualquer entrada abrirá uma [visão mais detalhada da solicitação](#request-details).

![Lista de solicitações de rede](./media/network_request_list.png)

A lista de solicitações de rede inclui as seguintes informações: 

Coluna | Descrição 
:------------ | :------------- 
**Name** | Nome e caminho da URL da solicitação
**Protocolo** |  Tipo de protocolo para a solicitação (por exemplo *, HTTPS, http/2*)
**Método** |    [Método http](https://developer.mozilla.org/docs/Web/HTTP/Methods) usado para a solicitação
**Resultado** |    Código de [status de resposta http](https://developer.mozilla.org/docs/Web/HTTP/Status)
**Tipo de conteúdo** |  Tipo de mídia solicitada ([tipo MIME](https://en.wikipedia.org/wiki/Media_type))
**Recebido** | Tamanho da resposta conforme entregue pelo servidor (não calculado para respostas em cache)
**Hora** |  Tempo para carregar a resposta do servidor (não calculadas para respostas em cache)
**Inicia** | Subsistema responsável por iniciar a solicitação (como *Parser, redirecionar, script, outros*)
**Linha do Tempo** | Linha do tempo visual dos eventos de rede da solicitação (por exemplo *, interrupções, resolução (DNS), conexão (TCP), SSL, envio, espera (TTFB), baixando*). Passar o mouse sobre o gráfico fornece a divisão mais granular dos [intervalos de rede](#timings)de rede).

### Barra de resumo

A barra na parte inferior do painel de **rede** resumirá o número total de erros de rede http, solicitações, dados transferidos e tempos de carregamento durante a sessão de criação de perfil de rede (ou seja, como o devtools foi aberto e gravando o tráfego de rede).

![Barra de resumo da rede](./media/network_summary_bar.png)

**Tempo decorrido** significa o tempo entre o início da sessão de criação de perfil e quando o último recurso foi baixado da rede. Os recursos buscados no cache do navegador não acumulam tempo para este número. 

**Tempo de carregamento do dom** significa o tempo entre o início da sessão de criação de perfil e quando o evento [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) foi disparado para indicar que a estrutura do documento de página foi carregada e analisada (mas não necessariamente qualquer folha de estilos, imagem ou subquadros).

Tempo de **carregamento de página** significa o tempo entre o início da sessão de criação de perfil e quando o evento [Load](https://developer.mozilla.org/docs/Web/Events/load) foi disparado para indicar que o documento da página (e todos os seus recursos) foi totalmente carregado.

## Detalhes da solicitação

Clicar em qualquer entrada na lista [**Resumo da rede**](#network-summary) abrirá o painel [**detalhes da solicitação**](#request-details) com informações adicionais em cada uma das guias a seguir.

![Painel detalhes da solicitação de rede](./media/network_request_details.png)

### Cabeçalhos
Exibe os [cabeçalhos HTTP](https://developer.mozilla.org/docs/Web/HTTP/Headers) enviados para e recebidos do servidor. Clique com o botão direito do mouse em qualquer entrada de cabeçalho para copiá-lo ( `Ctrl+C` ) para a área de transferência. Você também pode selecionar várias entradas mantendo pressionada a `Shift` tecla ou selecionando ALL ( `Ctrl+A` ).

### Body
Exibe os dados do corpo (se disponíveis) das cargas de solicitação e resposta.

Conteúdo da imagem é exibido com dimensões e dados de tamanho.

O conteúdo de texto é exibido em um editor (somente leitura) com opções para formatar o conteúdo do minified com uma **superimposição de impressão** e/ou **quebra automática de texto** para facilitar a leitura.

![Guia corpo do painel detalhes da solicitação](./media/network_details_body.png)

### Parâmetros
Exibe parâmetros da cadeia de caracteres de consulta para solicitações GET. Enquanto os parâmetros de solicitações POST são enviados nos cabeçalhos, as solicitações GET são incluídas na URL. Elas são desmembradas aqui para facilitar a leitura.

Clique com o botão direito do mouse em qualquer linha para copiá-la ( `Ctrl+C` ) para a área de transferência. Você também pode selecionar várias entradas mantendo pressionada a `Shift` tecla ou selecionando ALL ( `Ctrl+A` ).

### Cookies
Exibe cookies que são enviados ou recebidos como pares de chave/valor.

Clique com o botão direito do mouse em qualquer linha para copiá-la ( `Ctrl+C` ) para a área de transferência. Você também pode selecionar várias entradas mantendo pressionada a `Shift` tecla ou selecionando ALL ( `Ctrl+A` ).

Você pode limpar os cookies armazenados para o domínio especificado na [barra de ferramentas](#network-summary) (botão**Limpar cookies** ). 

### Intervalos

A guia **intervalos** fornece uma linha do tempo de eventos de rede envolvidos no carregamento do recurso selecionado. Isso é semelhante às informações encontradas na coluna *linha do tempo* da lista de [solicitação de rede](#network-request-list), mas também inclui os eventos que levaram à solicitação que está sendo enviada pela conexão, como o tempo gasto aguardando (*parado*) na fila de solicitações, a resolução DNS e o estabelecimento da conexão TCP. 

![Guia intervalos do painel detalhes da solicitação](./media/network_details_timings.png)

Os redirecionamentos de/para outros recursos são observados e clicar no link definirá o foco para esse recurso no painel de [detalhes da solicitação](#request details) de rede.

Os redirecionamentos carregados do cache não são afetados pela latência da rede, portanto, nenhum gráfico de *tempo* de rede será exibido.

![Recurso Redirecionado carregado do cache](./media/network_details_timings_cache_redirect.png)

Aqui estão os diferentes eventos de rede que podem ser exibidos para um determinado recurso, em ordem cronológica:

#### Paralisação

Tempo gasto aguardando uma conexão de rede disponível na fila de solicitações. Para HTTP 1.0/1.1, o Microsoft Edge permite um máximo de seis (6) conexões TCP simultâneas por nome de host. 

#### Resolvendo (DNS)

Tempo gasto procurando o endereço IP do nome do host do recurso no DNS (sistema de[nome de domínio](https://en.wikipedia.org/wiki/Domain_Name_System)).

#### Conectando (TCP)

Tempo gasto para estabelecer a conexão TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).

#### SSL

Tempo gasto na negociação de uma conexão SSL ([Secure Sockets](https://en.wikipedia.org/wiki/Transport_Layer_Security)Layer) com o [servidor proxy](https://en.wikipedia.org/wiki/Proxy_server) para o host.

#### Envie

Tempo gasto para enviar a solicitação de recurso.

#### Aguardando (TTFB)

Tempo gasto aguardando o primeiro byte da resposta do servidor host ("tempo até o primeiro byte" ou *TTFB*).

#### Baixá

Tempo gasto na leitura da resposta do servidor.

## Teclado

| Ação                         | Atalho     |
|:-------------------------------|:-------------|
| Iniciar/parar sessão de criação de perfil | `Ctrl` + `E` |
| Exportar como HAR                  | `Ctrl` + `S` |
| Localizar                           | `Ctrl` + `F` |
| Copiar                           | `Ctrl` + `C` |

## Problemas conhecidos

### Falha ao iniciar o agente de coleta de rede.

Se você vir esta mensagem de erro: **o agente de coleta de rede falhou ao iniciar** na ferramenta de rede, siga estas etapas para solucionar o problema.

1. Pressione `Windows Key`  +  `R` .

2. Na caixa de diálogo Executar, digite **Services. msc**.
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .

6. Agora você deve ver um emblema de reprodução ao lado de **rede** e solicitações de rede para a sua página da Web.
![conhecidos-problemas-4](./media/known_issues_4-network.PNG)

Ainda está com problemas? Envie-nos seus comentários usando o ícone **enviar comentários** ! 

![conhecidos-problemas-5](./media/known_issues_5.PNG)

### Falha ao parar o agente de coleta de rede.

Se você vir esta mensagem de erro: **o agente de coleta de rede não parou** na ferramenta de rede, siga estas etapas para solucionar o problema.

1. Pressione `Windows Key`  +  `R` .

2. Na caixa de diálogo Executar, digite **Services. msc**.
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .

6. Agora você deve ver um emblema de reprodução ao lado de **rede** e solicitações de rede para a sua página da Web.
![conhecidos-problemas-4](./media/known_issues_4-network.PNG)

Ainda está com problemas? Envie-nos seus comentários usando o ícone **enviar comentários** ! 

![conhecidos-problemas-5](./media/known_issues_5.PNG)
