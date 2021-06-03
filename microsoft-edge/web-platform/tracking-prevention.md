---
description: Esta página fornece documentação sobre o recurso Microsoft Edge (Chromium) de prevenção de rastreamento
title: Prevenção de Rastreamento Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web, prevenção de rastreamento, rastreadores, cookies, armazenamento, bloqueio de publicidade, bloqueio de rastreador, proteção de rastreamento
ms.openlocfilehash: 66356ab7ddaa56e46e74560d72b510ba63f7d70a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399285"
---
# <a name="tracking-prevention-in-microsoft-edge-chromium"></a>Prevenção de Rastreamento Microsoft Edge (Chromium)  

O recurso de prevenção de rastreamento no Microsoft Edge protege os usuários contra o controle online restringindo a capacidade dos rastreadores de acessar o armazenamento baseado no navegador, bem como a rede.  Ele foi criado para cumprir [a][MicrosoftEdgeBrowserPrivacyPromise] promessa de privacidade do Microsoft Edge navegador e, ao mesmo tempo, garantir que não haja impacto por padrão para a compatibilidade do site ou para a viabilidade econômica da Web.  

Microsoft Edge atualmente oferece aos usuários três níveis de prevenção de rastreamento, que são selecionados navegando para `edge://settings/privacy` .  

![Três configurações de prevenção de rastreamento][ImageThreeSettingsTrackingPrevention]  

1.  **Básico** - O nível menos restritivo de prevenção de rastreamento projetado para usuários que gostam de anúncios personalizados e que não se importam de serem rastreados na Web.  O Básico protege apenas os usuários contra rastreadores mal-intencionados, como impressões digitais e criptominers.  
1.  **Balanceado (Padrão)** - O nível padrão de prevenção de rastreamento projetado para usuários que querem ver anúncios menos assustadores que os seguem pela Web enquanto navegam.  O objetivo balanceado é bloquear rastreadores de sites com os que os usuários nunca se envolvem enquanto minimizam o risco de problemas de compatibilidade na Web.  
1.  **Estrito** - O nível mais restritivo de prevenção de rastreamento projetado para usuários que estão bem negociando a compatibilidade de site para privacidade máxima.  

O recurso de prevenção de rastreamento no Microsoft Edge é feito de três componentes principais que trabalham juntos para determinar se um recurso específico de um site deve ser classificado como um rastreador e bloqueado.  Os componentes são os seguinte:  

1.  **Classificação** - A maneira Microsoft Edge determina se uma URL pertence a um rastreador.  
1.  **Imposição** - As ações tomadas para proteger Microsoft Edge usuários contra URLs classificadas como rastreadores.  
1.  **Mitigações** - Os mecanismos fornecidos para garantir que os sites favoritos especificados pelo usuário ainda funcionem, oferecendo uma proteção padrão forte.  

Cada um dos componentes é explorado e explicado em detalhes nesta página.  

## <a name="classification"></a>Classificação  

O primeiro componente do recurso de prevenção de rastreamento no Microsoft Edge é a classificação.  Para classificar os rastreadores online e agrupar-os em categorias, Microsoft Edge usa as listas de proteção [de][|::ref1::|Main] rastreamento de código aberto Desconectar. [][GitHubDisconnectMeTrackingProtection]  As listas são entregues por meio do componente "Listas de Proteção de Confiança", que pode ser visualizado em `edge://components` .  Depois de baixadas, as listas são armazenadas no disco onde você pode usá-las para determinar se/como uma URL específica é classificada.  

Para determinar se uma URL é considerada um rastreador pelo sistema de classificação no Microsoft Edge, uma série de nomes de host são verificados, começando com uma combinação exata e, em seguida, continuando a verificar se há parciais de até quatro rótulos além do domínio de nível superior.  

> **Exemplo**:  
> 
> URL: `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Nomes de host testados:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Se algum desses nomes de host corresponder [][|::ref2::|Main] a um nome de host nas listas Desconectar, [][GitHubDisconnectMeTrackingProtection]Microsoft Edge prosseguirá com a avaliação de ações de imposição para impedir que os usuários sejam rastreados.  

## <a name="enforcement"></a>Imposição  

Para fornecer proteção contra ações de controle na Web, Microsoft Edge duas ações de imposição contra rastreadores confidenciais:

*   **Restringir o acesso** ao armazenamento - Se um recurso de rastreamento conhecido tentar acessar qualquer armazenamento da Web em que ele possa tentar persistir dados sobre o usuário, Microsoft Edge bloquear esse acesso.  Isso inclui restringir a capacidade desse rastreador de obter ou definir cookies, bem como acessar APIs de armazenamento, como `IndexedDB` e `localStorage` .  
*   **Bloquear** cargas de recursos - Se um recurso de controle conhecido estiver sendo carregado em um site, o Microsoft Edge poderá bloquear essa carga antes que a solicitação atinja a rede, dependendo do impacto de compatibilidade da carga e da configuração de prevenção de controle que um usuário definiu.  As cargas bloqueadas podem incluir scripts de controle, pixels, iframes e muito mais.  Isso impede que qualquer dado potencialmente seja enviado para o domínio de controle e pode até mesmo melhorar os tempos de carga e o desempenho da página como efeito colateral.  

Um usuário pode escolher o ícone de sobrevoo de informações da página no lado esquerdo da barra de endereços para descobrir quais rastreadores foram bloqueados em uma página específica: 

![Rastreadores bloqueados no flyout de informações da página][ImageBlockedTrackersPageInfoFlyout]  

A forma como as imposições são aplicadas depende do nível de prevenção de rastreamento que o usuário selecionou e das mitigações que podem ser aplicadas.  

## <a name="mitigations"></a>Mitigações  

Para garantir que a compatibilidade com a Web seja preservada o máximo possível, Microsoft Edge tem três mitigações para ajudar a equilibrar as imposições em situações específicas.  Estas são a [mitigação de relações de organização,](#org-relationship-mitigation)a [mitigação de envolvimento](#org-engagement-mitigation)da organização e [a lista CompatExceptions.](#the-compatexceptions-list)  

Antes de mergulhar nas mitigações, vale a pena definir o conceito de "Organização" ou "Org" para resumir.  [A][|::ref3::|Main] desconexão também mantém uma lista chamada [entities.jsem][GitHubDisconnectMeTrackingProtectionEntitiesJson] que define grupos de URLs pertencentes à mesma organização/empresa pai.  O recurso de prevenção de rastreamento no Microsoft Edge usa essa [](#org-engagement-mitigation) lista na [mitigação](#org-relationship-mitigation) de Relações da Organização e na mitigação de Envolvimento da Organização para minimizar a ocorrência de problemas de compatibilidade causados pelo acompanhamento da prevenção que afeta solicitações entre organizações.  

### <a name="org-relationship-mitigation"></a>Mitigação de Relações com a Organização  

Vários sites populares mantêm sites e Redes de Entrega de Conteúdo \(CDNs\) para atender a recursos estáticos e conteúdo a esses sites.  Para garantir que esses tipos de cenários não sejam afetados pelo acompanhamento da prevenção, o Microsoft Edge isenta um site de controlar a prevenção quando o site está fazendo solicitações de terceiros para outros sites pertencentes à mesma organização pai \(conforme definido na lista Desconectar entities.js[na][GitHubDisconnectMeTrackingProtectionEntitiesJson]lista \).  Isso é melhor ilustrado por um exemplo.  

> **Exemplo:**
> 
> Uma organização chamada Org1 é proprietária dos domínios e , conforme definido na lista `org1.test` `org1-cdn.test` [Desconectar][GitHubDisconnectMeTrackingProtectionEntitiesJson]entities.jsna lista .  Imagine que é classificado como um rastreador e normalmente teria as imposições de prevenção de controle `org1-cdn.test` aplicadas a ele.  Se um usuário visitar e o site tentar carregar um recurso de , Microsoft Edge não tomará nenhuma ação de imposição contra solicitações feitas para, mesmo que não seja uma URL de primeira `https://org1.test` `https://org1-cdn.test` `org1-cdn.test` parte.  Se outra URL que não faz parte da organização Org1 tentar carregar esse mesmo recurso, no entanto, a solicitação estará sujeita a imposições porque não faz parte da mesma organização.  
> 
> Mesmo que isso controle as imposições de prevenção para sites que pertencem à mesma organização, é improvável que isso introduza um alto risco de privacidade, pois essas organizações são capazes de determinar em quais sites/recursos você acessou, bem como usando dados `https://org1.test` `https://org1-cdn.test` back-end internos.  

### <a name="org-engagement-mitigation"></a>Mitigação de Envolvimento da Organização  

A mitigação de envolvimento da organização foi criada para minimizar os riscos de compatibilidade introduzidos pelo controle da prevenção, garantindo que os sites pertencentes a organizações que os usuários se envolvam o suficiente continuem a funcionar conforme esperado na Web.  Ele faz uso do envolvimento do [site][ChromiumDesignDocsSiteEngagement] para descontrair as imposições sempre que um usuário estabeleceu uma relação contínua \(atualmente definida por uma pontuação de envolvimento de site de 4,1 ou superior\) com um determinado site.  Isso é mais uma vez ilustrado por um exemplo:

> **Exemplo:**
> 
> Uma organização chamada Social Org é proprietária dos `social.example` domínios e `social-videos.example` .
> 
> Os usuários são considerados ter uma relação com a Organização Social se estabeleceram uma pontuação de envolvimento de site de 4,1 ou superior com qualquer um dos domínios pertencentes à Social Org.
> 
> Se outro site, , incluir conteúdo de terceiros \(digamos um vídeo incorporado de \) de qualquer um dos domínios pertencentes à Social Org que normalmente seriam restritos por meio do controle de imposições de prevenção, o site fica isento de controlar as imposições de prevenção, desde que a pontuação de envolvimento do site do usuário com domínios pertencentes a Social Org seja mantida acima do `https://content-embedder.example` `social-videos.example` limite.
> 
> Se um site não pertence a uma organização, um usuário deve estabelecer uma pontuação de envolvimento de site de 4,1 ou superior diretamente com ele antes que quaisquer blocos de carga de recursos/acesso de armazenamento impostos pela prevenção de controle sejam relaxados.

No momento, a mitigação de envolvimento da organização só é aplicada no modo Balanceado para que Microsoft Edge oferece as proteções mais altas possíveis para os usuários que optaram por Estrito.

### <a name="the-compatexceptions-list"></a>A lista CompatExceptions  

Com base nos comentários recentes recebidos pela Microsoft, o Microsoft Edge mantém uma pequena lista de sites \(a maioria dos quais estão na categoria Desconectar conteúdo\) que estavam quebrando devido à prevenção de controle, apesar de ter as duas mitigações acima no local. Os sites nesta lista estão isentos de controlar as imposições de prevenção.  A lista pode ser encontrada no disco nos [locais](#determining-whetherhow-a-particular-url-is-classified) descritos abaixo.  Os usuários podem substituir entradas nele usando a **opção Bloquear** em `edge://settings/content/cookies` .

Para evitar manter essa lista seguindo em frente, a Microsoft está trabalhando atualmente na API Armazenamento [Access][GitHubMsExplainersStorageAccessApi] no Chromium codebase.  A API do [Armazenamento Access][GitHubMsExplainersStorageAccessApi] oferece aos desenvolvedores de sites uma maneira de solicitar acesso de armazenamento diretamente dos usuários, fornecendo aos usuários mais transparência sobre como suas configurações de privacidade estão afetando sua experiência de navegação e dando aos desenvolvedores de sites controles para desbloquear a si mesmos de forma rápida e intuitiva.

Após a implementação da API do [Armazenamento Access, a][GitHubMsExplainersStorageAccessApi] Microsoft depredará a lista CompatExceptions e alcançará os sites afetados para torná-los cientes dos problemas e solicitar que eles usem a API do Armazenamento [Access][GitHubMsExplainersStorageAccessApi] seguindo em frente.  

## <a name="current-tracking-prevention-behavior"></a>Comportamento de prevenção de rastreamento atual  

A tabela a seguir mostra as ações de imposição e mitigações que são aplicadas a cada categoria de rastreador classificado em Microsoft Edge.  

*   Ao longo da parte superior estão as categorias de rastreadores conforme definido pelas categorias de lista de proteção de rastreamento [de desconectar.][GitHubDisconnectTrackingProtectionCategories]  
*   No lado esquerdo estão os três níveis de prevenção de rastreamento em Microsoft Edge \(Basic, Balanced e Strict\).  
*   A carta `S` indica que o acesso ao armazenamento está bloqueado.  
*   A carta indica que o acesso ao armazenamento e as cargas de recursos `B` \(como solicitações de rede\) estão bloqueadas.  
*   Um hífen \( \) indica que nenhum bloco é aplicado ao acesso `-` de armazenamento ou às cargas de recursos.  

| | Anúncios | Análises | Conteúdo | Cryptomining | Impressão digital | Redes sociais | Other | Mitigação da Mesma Organização | Mitigação de Envolvimento da Organização |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **Básico** | - | - | - | B | B | - | - | Habilitada | N/A |  
| **Balanced** | S | - | S | B | B | S | S | Habilitada | Habilitada |  
| **Estrito** | B | B | S | B | B | B | B | Habilitada | Desabilitado |  

> [!NOTE]
> A mitigação de envolvimento da organização não se aplica às categorias Cryptomining ou Fingerprinting.  

> [!TIP]
> O modo estrito bloqueia mais cargas de recursos do que Balanceada.  O bloqueio de mais cargas de recursos pode fazer com que o modo Estrito apareça para bloquear menos solicitações de controle do que Balanceado, pois os rastreadores que fazem as solicitações nunca são carregados.  

> [!NOTE]
> A coluna Impressão Digital no [comportamento de](#current-tracking-prevention-behavior) prevenção de rastreamento atual refere-se a rastreadores que estão na lista Impressão Digital, além de outra lista.  Os rastreadores que aparecem somente na lista Impressão Digital são considerados não mal-intencionados e não são bloqueados.

### <a name="inprivate-behavior"></a>Comportamento InPrivate  

No Microsoft Edge 79, o comportamento padrão era aplicar proteções de modo estrito em InPrivate.  No Microsoft Edge 80, esse comportamento foi substituído por uma opção que permite que os usuários decidam se aplicarão proteções de modo estrito ou se manterão suas configurações regulares enquanto navegam no `edge://settings/privacy` InPrivate.  

## <a name="determining-whetherhow-a-particular-url-is-classified"></a>Determinando se/como uma URL específica é classificada  

A maneira mais fácil de determinar se uma URL específica é classificada como um rastreador conhecido é executar as etapas a seguir.  

1.  Abra DevTools e navegue até a guia Console.  
1.  Atualize a página da Web.  
    1.  Você pode querer limpar Cookies e outros dados **de site** primeiro para redefinir as pontuações de envolvimento do site e garantir uma ardósia completamente limpa.  
1.  Procure qualquer mensagem que leia `Tracking Prevention blocked access to storage for <URL>` .  
    1.  Você pode expandir as mensagens para ver as URLs individuais que foram bloqueadas.  
1.  Se você precisar determinar em qual categoria um site bloqueado específico está, a maneira mais fácil de fazer isso é pesquisá-lo na lista Desconectar services.js[na lista][GitHubDisconnectTrackingProtectionCategories].  As entradas são alfabéticas, portanto, rolar até a parte superior de um bloco de entradas de site permite que você encontre a categoria específica para um site específico.  

> [!TIP]
> Se você precisar acessar as listas de prevenção de rastreamento armazenadas no disco, cada uma delas poderá ser encontrada em um dos dois locais.  
>
> **Atualizações baseadas em componentes** - As listas baixadas do componente "Listas de Proteção de Confiança"  
>
> Windows: `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> macOS: `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Diretório de** instalação - As listas que são agrupadas com o Microsoft Edge Instalador.  Se você selecionou um diretório de instalação diferente, seus caminhos exatos podem ser diferentes.  
>
> Windows: `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> macOS: `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## <a name="frequently-asked-questions"></a>Perguntas frequentes  

A seção a seguir contém respostas para perguntas frequentes sobre o recurso de prevenção de rastreamento Microsoft Edge.  

**Há uma maneira de bloquear ou permitir rastreadores específicos para fins de depuração?**  

Atualmente, Microsoft Edge expõe apenas uma opção para desabilitar o controle de imposições de prevenção de execução em um site especificado.  Essa opção é acessada por meio do sobrevoo de informações da página ou por meio da `edge://settings/privacy/trackingPreventionExceptions` página.  

Dito isso, as **** opções **Bloquear** e Permitir na página podem ser usadas para permitir ou negar acesso a domínios específicos ao armazenamento, como cookies e outros mecanismos de armazenamento `edge://settings/content/cookies` do navegador.  Isso é útil para depurar problemas de site causados pelo controle de imposições de prevenção bloqueando o acesso ao armazenamento de um site específico.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Privacidade - Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Envolvimento do site - Os Chromium projetos"  

[DisconnectMain]: https://disconnect.me "Desconectar"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.json - disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.json - disconnectme/disconnect-tracking-protection | Github"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Armazenamento Explicador de API do Access - MSEdgeExplainers/StorageAccessAPI | GitHub"
