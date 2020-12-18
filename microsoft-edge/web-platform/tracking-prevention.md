---
description: Esta página fornece documentação sobre o recurso de prevenção de rastreamento do Microsoft Edge (Chromium)
title: Prevenção de rastreamento no Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web, prevenção de rastreamento, rastreadores, cookies, armazenamento, bloqueio de anúncios, bloqueio de controladora, proteção contra rastreamento
ms.openlocfilehash: a767e55a44c4d416b6d40ca12eb49f2c3a722010
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231143"
---
# Prevenção de rastreamento no Microsoft Edge (Chromium)  

O recurso de prevenção de rastreamento no Microsoft Edge protege os usuários contra o rastreamento online restringindo a capacidade dos rastreadores de acessar o armazenamento baseado em navegador e a rede.  Ele foi criado para sustentar a promessa de [privacidade do navegador][MicrosoftEdgeBrowserPrivacyPromise] Microsoft Edge e, ao mesmo tempo, garantir que não haja impacto por padrão na compatibilidade do site ou na viabilidade econômica da Web.  

Atualmente o Microsoft Edge oferece aos usuários três níveis de prevenção de rastreamento, que são selecionados ao navegar para `edge://settings/privacy` .  

![Três configurações de prevenção de rastreamento][ImageThreeSettingsTrackingPrevention]  

1.  **Básico** -o nível menos restritivo de prevenção de rastreamento projetado para os usuários que gostam de anúncios personalizados e que não se comportam em rastreio na Web.  O básico só protege os usuários contra rastreadores maliciosos, como impressões digitais e cryptominers.  
1.  **Balanced (padrão)** -o nível padrão de prevenção de rastreamento projetado para os usuários que desejam ver menos anúncios Creepy que os seguem pela Web enquanto navegam.  Balanceados para bloquear rastreadores de sites que os usuários nunca encontram enquanto minimizam o risco de problemas de compatibilidade na Web.  
1.  **Estrito** – o nível mais restritivo de prevenção de rastreamento projetado para usuários que não têm problemas de compatibilidade com o website para obter o máximo de privacidade.  

O recurso de prevenção de rastreamento no Microsoft Edge é composto de três componentes principais que trabalham juntos para determinar se um recurso específico de um site deve ser classificado como um controlador e bloqueado.  Os componentes são os seguintes:  

1.  **Classificação** -a maneira como o Microsoft Edge determina se uma URL pertence a um controlador.  
1.  **Imposição** -as ações executadas para proteger os usuários do Microsoft Edge de URLs classificadas como rastreadores.  
1.  **Atenuações** -os mecanismos fornecidos para garantir que os sites favoritos especificados pelo usuário ainda funcionem, oferecendo proteção padrão forte.  

Cada um dos componentes é explorado e explicado em detalhes nesta página.  

## Classificação  

O primeiro componente do recurso de prevenção de rastreamento no Microsoft Edge é a classificação.  Para classificar os rastreadores online e agrupá-los em categorias, o Microsoft Edge usa as listas [Desconectar][|::ref1::|Main] da [proteção contra rastreamento][GitHubDisconnectMeTrackingProtection]de fonte aberta.  As listas são entregues por meio do componente "listas de proteção de confiança", que podem ser exibidos em `edge://components` .  Após o download, as listas são armazenadas em disco em que você pode usá-las para determinar se/como uma determinada URL está classificada.  

Para determinar se uma URL é considerada um controlador pelo sistema de classificação no Microsoft Edge, uma série de nomes de host são verificadas, começando com uma correspondência exata e, em seguida, continuando a verificar se há correspondências parciais para até quatro rótulos além do domínio de nível superior.  

> **Exemplo**:  
> 
> URL `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Nomes de host testados:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Se qualquer um desses nomes de host for compatível com um nome de host nas [listas][GitHubDisconnectMeTrackingProtection]de [desconexão][|::ref2::|Main] , o Microsoft Edge continuará com a avaliação de ações de imposição para impedir que os usuários sejam acompanhados.  

## Imposição  

Para fornecer proteção contra ações de rastreamento na Web, o Microsoft Edge leva duas ações de imposição contra rastreadores classificados:

*   **Restringir o acesso ao armazenamento** -se um recurso de controle conhecido tentar acessar qualquer armazenamento da Web em que pode tentar manter dados sobre o usuário, o Microsoft Edge bloqueará esse acesso.  Isso inclui restringir a capacidade do controlador de obter ou definir cookies, além de APIs de armazenamento do Access, como `IndexedDB` e `localStorage` .  
*   **Bloquear cargas de recursos** -se um recurso de controle conhecido estiver sendo carregado em um site, o Microsoft Edge poderá bloquear essa carga antes que a solicitação atinja a rede, dependendo do impacto de compatibilidade da carga e da configuração de prevenção de rastreamento definida pelo usuário.  As cargas bloqueadas podem incluir scripts de rastreamento, pixels, iframes e muito mais.  Isso impede que todos os dados sejam enviados ao domínio de rastreamento e possam até mesmo melhorar o tempo de carregamento e o desempenho da página como um efeito colateral.  

Um usuário pode clicar no ícone do submenu de informações da página no lado esquerdo da barra de endereços para descobrir quais rastreadores estavam bloqueados em uma página específica: 

![Rastreadores bloqueados no submenu de informações da página][ImageBlockedTrackersPageInfoFlyout]  

A forma como os enforces são aplicados depende de qual nível de prevenção de rastreamento o usuário selecionou e das atenuações que podem ser aplicáveis.  

## Atenuações  

Para garantir que a compatibilidade da Web seja preservada o máximo possível, o Microsoft Edge tem três reduções para ajudar a balancear aplicações em situações específicas.  Estes são a [atenuação de relações da organização](#org-relationship-mitigation), a [atenuação do compromisso da organização](#org-engagement-mitigation)e a [lista CompatExceptions](#the-compatexceptions-list).  

Antes de se aprofundar na atenuação, vale a pena definir o conceito de "organização" ou "org" por curto.  [Desconectar][|::ref3::|Main] também mantém uma lista chamada [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson] que define grupos de URLs pertencentes à mesma organização/empresa pai.  O recurso de prevenção de rastreamento no Microsoft Edge usa essa lista na [atenuação de relações organizacionais](#org-relationship-mitigation) e a [atenuação do compromisso da organização](#org-engagement-mitigation) para minimizar a ocorrência de problemas de compatibilidade causados pela prevenção de rastreamento que afetam solicitações entre organizações.  

### Mitigação de relações da organização  

Vários sites populares mantêm sites e redes de distribuição de conteúdo \ (CDNs \) para atender a recursos estáticos e conteúdo a esses sites.  Para garantir que esses tipos de cenários não sejam afetados pela prevenção de rastreamento, o Microsoft Edge isenta um site da prevenção de rastreamento quando o site está fazendo solicitações de terceiros para outros sites pertencentes à mesma organização pai \ (conforme definido na [lista desconectar entities.jsna lista][GitHubDisconnectMeTrackingProtectionEntitiesJson]\).  Isso é melhor ilustrado por um exemplo.  

> **Exemplo:**
> 
> Uma organização chamada Org1 é proprietária dos domínios `org1.test` e `org1-cdn.test` , conforme definido na [lista desconectar entities.jsem][GitHubDisconnectMeTrackingProtectionEntitiesJson].  Imagine que `org1-cdn.test` é classificado como um controlador e normalmente teria imposição de prevenção de rastreamento aplicada a ele.  Se um usuário visitar `https://org1.test` e o site tentar carregar um recurso, o `https://org1-cdn.test` Microsoft Edge não executará nenhuma ação de imposição em relação a solicitações feitas, `org1-cdn.test` mesmo que não seja uma URL de primeira parte.  Se outra URL que não faz parte da organização do Org1 tentar carregar esse mesmo recurso, no entanto, a solicitação estará sujeita a imposição, pois ela não faz parte da mesma organização.  
> 
> Embora isso reproduza o rastreamento de prevenção de rastreamento para sites que pertençam à mesma organização, é improvável que isso apresente uma grande quantidade de riscos de privacidade, pois essas organizações podem determinar quais sites/recursos você acessou `https://org1.test` e `https://org1-cdn.test` usar dados back-end internos.  

### Atenuação do compromisso da organização  

A atenuação do contrato da organização foi criada para minimizar os riscos de compatibilidade apresentados pela prevenção de rastreamento ao garantir que os sites de propriedade de organizações que os usuários informam com o sistema continuem a funcionar como esperado na Web.  Isso faz com que o uso do [envolvimento de sites][ChromiumDesignDocsSiteEngagement] relaxe seja reforçado sempre que um usuário tiver estabelecido uma relação contínua \ (atualmente definido por uma pontuação do envolvimento no site 4,1 ou maior \) com um determinado site.  Isso novamente é melhor ilustrado por um exemplo:

> **Exemplo:**
> 
> Uma organização chamada organização social possui os domínios `social.example` e `social-videos.example` .
> 
> Os usuários devem ter uma relação com a organização social se tiverem estabelecido uma pontuação de envolvimento no site de 4,1 ou mais com qualquer um dos domínios pertencentes à organização social.
> 
> Se outro site, `https://content-embedder.example` , inclui conteúdo de terceiros \ (por exemplo, um vídeo incorporado de `social-videos.example` \) de qualquer um dos domínios pertencentes à organização social, que normalmente seria restringido por imposição de prevenção de rastreamento, o site está isento de aplicação de prevenção de rastreamento, desde que a Pontuação do envolvimento do usuário com domínios pertencentes à organização social seja mantida acima do limite.
> 
> Se um site não pertence a uma organização, um usuário deve estabelecer uma pontuação do envolvimento do site de 4,1 ou mais com ele diretamente antes que os blocos de carga de acesso/recursos de armazenamento impostos pela prevenção de rastreamento sejam relaxados.

A mitigação do contrato da organização no momento só é aplicada no modo balanceado para que o Microsoft Edge ofereça as melhores proteções possíveis para os usuários que optaram pelo estrito.

### Lista CompatExceptions  

Com base nos comentários recentes do usuário que a Microsoft recebeu, o Microsoft Edge mantém uma pequena lista de sites \ (a maioria delas está na categoria de conteúdo desconectar \) que foi quebrada devido à prevenção de rastreamento, apesar de ter as duas atenuações acima em vigor. Sites nesta lista são isentos de aplicação de prevenção de rastreamento.  A lista pode ser encontrada em disco nos [locais](#determining-whetherhow-a-particular-url-is-classified) descritos abaixo.  Os usuários podem substituir entradas usando a opção **Bloquear** em `edge://settings/content/cookies` .

Para evitar manter esta lista avançando, a Microsoft está trabalhando atualmente na [API de acesso de armazenamento][GitHubMsExplainersStorageAccessApi] na base de código do Chromium.  A [API de acesso de armazenamento][GitHubMsExplainersStorageAccessApi] permite que os desenvolvedores de sites solicitem acesso de armazenamento diretamente dos usuários, fornecendo aos usuários mais transparência em como as configurações de privacidade estão afetando sua experiência de navegação e permitindo que os desenvolvedores de sites desbloqueiem de forma rápida e intuitiva.

Depois que a [API de acesso ao armazenamento][GitHubMsExplainersStorageAccessApi] for implementada, a Microsoft substituirá a lista CompatExceptions e fará o contato com os sites afetados, para que eles fiquem cientes dos problemas e para solicitar que eles usem a API de acesso de [armazenamento][GitHubMsExplainersStorageAccessApi] , movendo-se para frente.  

## Comportamento de prevenção de rastreamento atual  

A tabela a seguir mostra as ações de imposição e as atenuações aplicadas a cada categoria de controlador classificado no Microsoft Edge.  

*   Na parte superior estão as categorias de rastreadores definidas pelas [categorias de lista de proteção contra rastreamento desconectado][GitHubDisconnectTrackingProtectionCategories].  
*   Ao longo do lado esquerdo estão os três níveis de prevenção de rastreamento no Microsoft Edge \ (básico, balanceado e estrito \).  
*   A letra `S` indica que o acesso ao armazenamento está bloqueado.  
*   A letra `B` indica que o acesso ao armazenamento e as cargas de recursos \ (por exemplo, solicitações de rede \) são bloqueados.  
*   Um hífen \ ( `-` \) indica que nenhum bloco é aplicado a um acesso do armazenamento ou carga de recursos.  

| | Anúncios | Análises | Conteúdo | Cryptomining | Impressão digital | Redes sociais | Other | Atenuação da mesma organização | Atenuação do compromisso da organização |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Básico** | - | - | - | B | B | - | - | Habilitado | N/D |  
| **Equilibrada** | S | - | S | B | B | S | S | Habilitada | Habilitada |  
| **Estrito** | B | B | S | B | B | B | B | Habilitado | Desabilitado |  

> [!NOTE]
> A mitigação do contrato da organização não se aplica às categorias de Cryptomining ou impressão digital.  

> [!TIP]
> O modo estrito bloqueia mais cargas de recursos do que o balanceado.  O bloqueio de mais cargas de recursos pode resultar na exibição do modo estrito para bloquear menos solicitações de rastreamento do que o equilibrado, pois os rastreadores que fazem as solicitações nunca são carregados.  

> [!NOTE]
> A coluna impressão digital no [comportamento de prevenção de rastreamento atual](#current-tracking-prevention-behavior) refere-se aos rastreadores que estão na lista de impressão digital, além de outra lista.  Os rastreadores que aparecem em uma lista de impressão digital são considerados impressão digital não maliciosas e não são bloqueados.

### Comportamento InPrivate  

No Microsoft Edge 79, o comportamento padrão era aplicar proteções de modo estrito no InPrivate.  No Microsoft Edge 80, esse comportamento foi substituído por um switch em `edge://settings/privacy` que permite que os usuários decidam se desejam aplicar proteções de modo estrito ou manter suas configurações regulares durante a navegação InPrivate.  

## Determinando se/como uma determinada URL é classificada  

A maneira mais fácil de determinar se uma URL específica é classificada como um controlador conhecido é executar as etapas a seguir.  

1.  Abra o DevTools e navegue até a guia Console.  
1.  Recarregar a página.  
    1.  Você pode querer limpar **cookies e outros dados de site** primeiro para redefinir as pontuações de envolvimento do site e garantir um Tablet completamente limpo.  
1.  Procure mensagens lidas `Tracking Prevention blocked access to storage for <URL>` .  
    1.  Você pode expandir as mensagens para ver as URLs individuais que foram bloqueadas.  
1.  Se você precisar determinar em qual categoria um site bloqueado específico está, a maneira mais fácil de fazer isso é procurá-lo na [lista desconectar services.jsem][GitHubDisconnectTrackingProtectionCategories].  As entradas são em ordem alfabética, portanto, rolar para a parte superior de um bloco de entradas de site permite que você encontre a categoria específica de um site específico.  

> [!TIP]
> Se você precisar acessar as listas de prevenção de rastreamento armazenadas no disco, cada uma pode ser encontrada em um dos dois locais.  
>
> **Atualizações baseadas em componentes** – as listas baixadas do componente "listas de proteção de confiança"  
>
> Windows `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> MacOS `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Diretório de instalação** – as listas que são agrupadas com o instalador do Microsoft Edge.  Se você selecionou um diretório de instalação diferente, seus caminhos exatos podem ser diferentes.  
>
> Windows `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> MacOS `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## Perguntas frequentes  

A seção a seguir contém respostas para perguntas frequentes sobre o recurso de prevenção de rastreamento no Microsoft Edge.  

**Existe uma maneira de bloquear ou permitir rastreadores específicos para fins de depuração?**  

Atualmente, o Microsoft Edge expõe apenas uma opção para desativar o rastreamento de imposição de execução em um site especificado.  Essa opção é acessada por meio do submenu de informações da página ou por meio da `edge://settings/privacy/trackingPreventionExceptions` página.  

Dito isso, as opções **Bloquear** e **permitir** na `edge://settings/content/cookies` página podem ser usadas para permitir ou negar o acesso de domínios específicos ao armazenamento, como cookies e outros mecanismos de armazenamento do navegador.  Isso é útil para depurar problemas de site causados por imposição de prevenção de rastreamento que bloqueia o acesso ao armazenamento para um site específico.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Privacidade-Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Envolvimento no site-projetos do Chromium"  

[DisconnectMain]: https://disconnect.me "Automática"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/desconectar-rastreamento-proteção | GitHub"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.jsdisconnectme/desconectar-rastreamento-proteção | GitHub"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.jsdisconnectme/desconectar-rastreamento-proteção | GitHub"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Explicativo da API do Access Storage-MSEdgeExplainers/StorageAccessAPI | GitHub"
