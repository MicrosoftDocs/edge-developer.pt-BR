---
description: Políticas de desenvolvedor de catálogo de Complementos do Microsoft Edge.
title: Políticas de Desenvolvedor de Catálogo de Complementos do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: f71767cc4cd887ce9351202dd06732760299816d
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015706"
---
# Políticas de Desenvolvedor de Catálogo de Complementos do Microsoft Edge  

## Introdução e objetivo deste documento  

Obrigado pelo seu interesse em desenvolver extensões para o catálogo de Complementos do Microsoft Edge.  O Microsoft Edge addon Policies Catalog Policies \ (políticas de desenvolvimento de catálogos de Complementos \) se aplicam às suas extensões, incluindo o envio de extensões por meio do [Partner Center][MicrosoftPartnerCenter] e o fornecimento dessas extensões por meio dos complementos do Microsoft Edge.  

## Básicos  

Alguns princípios para ajudá-lo a começar:  

*   Você deve oferecer um valor exclusivo e distinto em suas extensões para o Microsoft Edge.  Forneça um motivo convincente para baixar suas extensões do catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \).  
*   Você não deve enganar nossos usuários em comum sobre o que sua extensão faz, quem está oferecendo e assim por diante.  
*   Você não deve tentar enganar os usuários, o sistema ou o ecossistema.  Não há nenhum lugar nos Complementos do Microsoft Edge para qualquer tipo de fraude; sejam classificações e manipulação de revisão, fraudes de cartão de crédito ou outra atividade fraudulenta.  

Obedecer a esses Complementos catálogos de catálogos de catálogos devem ajudá-lo a escolher as opções que melhoram o apelo e o público-alvo da extensão.  

Suas extensões são cruciais para a experiência de centenas de milhões de usuários.  Aguardamos que você crie o que você cria e são thrilled para ajudar a fornecer suas extensões para o mundo.  

## 1. políticas de produto  

### 1,1 & valor de função diferente; Representação precisa  

Sua extensão e metadados associados devem refletir com precisão a fonte, a funcionalidade e os recursos que você descrever.  

#### as extensões 1.1.1 devem ter uma finalidade única  

Sua extensão deve ter uma finalidade única com funcionalidade estreita.  

#### 1.1.2 descrever a extensão  

Todos os aspectos da extensão devem descrever precisamente as funções, os recursos e as limitações importantes da extensão, incluindo os dispositivos de entrada necessários ou com suporte.  A proposta de valor da extensão deve ser clara durante a primeira experiência de execução.  Sua extensão pode não usar um nome ou ícone semelhante a de outras extensões e não deve alegar representar uma empresa, corpo governamental ou outra entidade se você não tiver permissão para fazer essa representação.  

#### funcionalidade do 1.1.3  

Sua extensão deve ser totalmente funcional.  

#### pesquisa e descoberta do 1.1.4  

Termos de pesquisa não podem exceder sete termos exclusivos e devem ser relevantes para a extensão.  

#### o 1.1.5 fornece os detalhes apropriados  

Você deve fornecer detalhes distintos e informativos sobre a extensão e a funcionalidade na listagem \ (metadados \) para sua extensão.  Sua extensão deve fornecer uma experiência de usuário valiosa e de qualidade.  Sua extensão também deve ter uma presença ativa em Complementos do Microsoft Edge.  

#### estabilidade e desempenho do 1.1.6  

Sua extensão não deve afetar negativamente o desempenho ou a estabilidade do Microsoft Edge.  

#### ofuscação 1.1.7  

Extensões com código ofuscado não são permitidas.  Isso inclui código dentro do pacote de extensão, bem como qualquer código externo ou recurso externo buscado na Web.  Você pode ser solicitado a refatorar partes do seu código se não for reviewável.  

#### 1.1.8 alterando as configurações do navegador  

Sua extensão **não deve, sem o consentimento do usuário adequado**, alterar ou aparecer como alterar, funcionalidade do navegador ou configurações, incluindo, entre outros: o provedor de pesquisa da barra de endereços e sugestões, a Home Page ou a Home Page, a página da nova guia e adicionar ou remover favorito.  

Qualquer alteração nas configurações do navegador deve ser documentada explicitamente na descrição da extensão.  

Sua extensão só poderá revisar as configurações de chave para substituir uma página da Microsoft ou serviço com uma de terceiros (por exemplo, exigir o uso de um mecanismo de pesquisa de terceiros ou definir a Home Page como uma propriedade da Web de terceiros \) se você for empregado ou de outra forma associado a tal terceiros.  

### segurança do 1,2  

Sua extensão não deve prejudicar ou comprometer a segurança do usuário ou a segurança ou a funcionalidade do dispositivo, sistema ou sistemas relacionados.  

#### 1.2.1 políticas de segurança de conteúdo  

> [!NOTE]
> Se você fizer alterações à sua extensão após a funcionalidade descrita, todas as alterações no código deverão ser compatíveis com a [política de segurança de conteúdo do Microsoft Edge][MicrosoftEdgeContentSecurityPolicyRemoteScript].  Exemplo: a extensão não deve baixar um script remoto e, em seguida, executar esse script de uma maneira que não seja consistente com a funcionalidade descrita.  

#### 1.2.2 software indesejado e malicioso  

Sua extensão não deve conter ou habilitar malware conforme definido pelo critério da Microsoft para [software indesejado e mal-intencionado][MicrosoftIdentifiesMalwareUnwantedApplications].  

#### dependência 1.2.3 em outro software  

Sua extensão pode depender de software não integrado \ (por exemplo, outro produto, módulo ou serviço \) para oferecer a funcionalidade principal, contanto que você revele a dependência na descrição  

#### Atualização de extensões do 1.2.4  

A menos que seja permitida de outra forma pela Microsoft, as extensões devem ser atualizadas somente por Complementos do Microsoft Edge.  

### o produto 1,3 está em teste  
A extensão deve ser testada.  Se não for possível testar a extensão por qualquer motivo, incluindo, entre outros, os itens abaixo, a extensão poderá reprovar essa exigência.  

#### Credenciais de usuário do 1.3.1  
Se sua extensão exigir credenciais de logon, forneça uma conta de demonstração em funcionamento usando o campo **anotações para certificação** .  

#### 1.3.2 disponibilidade de serviços  

Se sua extensão requer acesso a um servidor, o servidor deve ser funcional para verificar se ele funciona corretamente.  

### 1,4 usabilidade  

Sua extensão deve atender aos padrões de loja de extensão para usabilidade, incluindo, entre outros, os que estão listados nas subseções abaixo.  

#### 1.4.1 a compatibilidade entre plataformas  

As extensões devem ser compatíveis com o Microsoft Edge em todos os dispositivos e plataformas em que elas podem ser baixadas.  Se for feito o download de uma extensão em um dispositivo com a qual não seja compatível, ele deverá detectar que, em seguida, exibir uma mensagem para o usuário detalhando os requisitos que os dispositivos devem atender para que possam ser compatíveis com a extensão.  

#### 1.4.2 experiência do usuário  

A extensão deve ser imediatamente reiniciada e deve ficar responsiva à entrada do usuário.  As extensões devem continuar sendo executadas e continuar respondendo à entrada do usuário.  As extensões devem desligar normalmente e não fechar inesperadamente.  A extensão deve tratar exceções e continuar respondendo à entrada do usuário após a manipulação da exceção.  

### Informações pessoais do 1,5  

Os seguintes requisitos se aplicam às extensões que acessam informações pessoais.  As informações pessoais incluem todas as informações ou dados que identificam ou podem ser usadas para identificar uma pessoa ou que está associada a tais informações ou dados.  

#### 1.5.1 coletar informações pessoais somente quando necessário  

Sua extensão pode coletar, acessar, usar ou transmitir informações pessoais \ (incluindo atividades de navegação na Web \); somente se exigido por e somente para uso em um recurso divulgado proeminentemente divulgado e voltado para o usuário.  

#### 1.5.2 manter uma política de privacidade  

Não importa se sua extensão acessa, coleta ou transmite informações pessoais; Você deve fornecer avisos proeminentes e obedecer à sua política de privacidade, se exigido por lei.  Sua política de privacidade deve informar os usuários sobre as informações pessoais acessadas, coletadas ou transmitidas pela sua extensão, como essas informações são usadas, armazenadas e protegidas, e indique os tipos de participantes aos quais ele está divulgado.  A política de privacidade deve descrever os controles que os usuários têm sobre o uso e o compartilhamento de suas informações, como eles acessam as informações deles e devem estar em conformidade com as leis e regulamentos aplicáveis.  Sua política de privacidade deve ser mantida atualizada à medida que você adiciona novos recursos e funcionalidades à sua extensão.  

Se você fornecer a Microsoft com a política de privacidade, concorda em permitir que a Microsoft Compartilhe essa política de privacidade com os usuários da extensão.  

#### 1.5.3 o compartilhamento de dados com terceiros  

Você pode publicar as informações pessoais dos usuários da extensão em um serviço externo ou de terceiros por meio da extensão ou dos metadados associados somente após a obtenção do consentimento consentimento desses usuários.  Consentimento de consentimento significa que os usuários dão permissão expressa na interface do usuário da sua extensão para a atividade solicitada, após:  

*   Descrever para seus usuários como as informações são acessadas, usadas ou compartilhadas e indicar os tipos de participantes aos quais ele está divulgado e  
*   Forneça aos usuários um mecanismo na interface de usuário da extensão por meio da qual eles têm a opção de rescindir a permissão e recusar posteriormente.  

#### 1.5.4 o compartilhamento de informações de não usuários  

Se você publicar as informações pessoais de uma pessoa em um serviço externo ou em terceiros por meio da extensão ou dos metadados, mas a pessoa cujas informações está sendo compartilhada não é um usuário da sua extensão;  

1.  Você deve obter consentimento por escrito expresso para publicar essas informações pessoais.  
1.  Você deve permitir que a pessoa cujas informações seja compartilhada retenham esse consentimento a qualquer momento.  
1.  A política de privacidade deve divulgar claramente que você pode coletar informações pessoais dessa maneira.  
1.  Se exigido pela lei aplicável, você deve excluir as informações pessoais de qualquer solicitação individual, incluindo indivíduos cujas informações você coleta dessa maneira.  
1.  Se a sua extensão fornecer aos usuários acesso às informações pessoais de outras pessoas, essa solicitação também será aplicada.  

#### 1.5.5 transmitir informações com segurança  

Se sua extensão coletar, armazenará ou transmitirá informações pessoais; Ele deve fazer isso com segurança usando métodos de criptografia modernos.  

#### 1.5.6 informações altamente confidenciais  

Sua extensão não deve coletar, armazenar nem transmitir informações pessoais altamente confidenciais, como dados financeiros ou de integridade, a menos que as informações sejam relacionadas à funcionalidade de sua extensão.  Sua extensão também deve obter consentimento do usuário expresso antes de coletar, armazenar ou transmitir essas informações.  

### permissões do 1,6  

Sua extensão só deve solicitar essas permissões necessárias para o funcionamento.  Você deve fornecer uma descrição de como a extensão funciona.  Sua extensão só deve ser executada conforme descrito.  Sua extensão pode não solicitar permissão para recursos que vão além dos recursos necessários para executar e funcionar como declaradas.  

### Localização do 1,7  

Você deve localizar a extensão de todos os idiomas para os quais a extensão alega dar suporte.  O texto da descrição da extensão deve ser localizado em cada idioma que você declarar.  
Se a extensão for traduzida de forma que alguns recursos não estejam disponíveis em uma versão localizada, você deverá declarar claramente ou exibir os limites de localização na descrição da extensão. A experiência fornecida por uma extensão deve ser razoavelmente parecida em todos os idiomas com suporte.  

### 1,8 transações financeiras  

Se o seu produto incluir compras em produtos, assinaturas, moeda virtual, funcionalidade de cobrança ou captura de informações financeiras; os requisitos nas seções a seguir se aplicam.  

#### Recursos pagos do 1.8.1  

Sua extensão pode permitir que os usuários consumam conteúdo digital ou serviços comprados por meio de um mecanismo de compra ou API de terceiros.  

Você deve usar uma API de compra segura de terceiros para compras de bens ou serviços físicos.  Você deve usar uma API de compra segura de terceiros para pagamentos feitos em conexão com qualquer outro serviço, incluindo jogos de azar do mundo real ou contribuições de caridade.  

*   Se a sua extensão for usada para facilitar ou coletar contribuições de caridade ou para conduzir um sorteio ou concurso promocional, você deverá fazer isso em conformidade com a lei aplicável.  
*   Você também deve indicar claramente que a Microsoft não é o beneficente ou patrocinador da promoção.  
*   Ofertas de produtos vendidos na sua extensão não devem ser convertidas em qualquer moeda legal válida \ (como USD, euro e assim por diante \) ou qualquer produto ou serviço físico.  

Os seguintes requisitos se aplicam ao seu uso de uma API de aquisição de terceiros segura:  

*   No momento da transação ou quando você coleta qualquer informação financeira ou de pagamento do usuário; sua extensão deve identificar o provedor de transações comerciais, autenticar o usuário e obter a confirmação do usuário para a transação.  Um provedor de transações comerciais mantém uma plataforma segura para trocas financeiras.  
*   Sua extensão pode oferecer aos usuários a capacidade de salvar essa autenticação, mas os usuários devem ter a capacidade de exigir uma autenticação em todas as transações ou desativar transações no produto.  
*   Se a sua extensão coleta informações de cartão de crédito ou usa um processador de pagamento de terceiros que coleta informações de cartão de crédito, o processamento de pagamento deve atender ao padrão de segurança de dados do PCI (PCI DSS \) atual.  

#### recursos pagos de desfechamento 1.8.2  

Sua extensão e metadados associados devem fornecer informações sobre os tipos de compras no produto oferecidas e o intervalo de preços.  Você não deve induzir usuários e deve estar claro sobre a natureza de suas promoções e ofertas de produtos, incluindo o escopo e os termos de qualquer experiência de avaliação.  Se a sua extensão restringe o acesso ao conteúdo criado pelo usuário durante ou após uma avaliação, você deve notificar os usuários com antecedência.  Além disso, a extensão deve deixá-la clara para os usuários que estão iniciando uma opção de compra na extensão.  

### notificações do 1,9  

Sua extensão deve respeitar as configurações do sistema para notificações.  Isso significa que qualquer apresentação de anúncios e notificações para os usuários deve ser consistente com as preferências do usuário, independentemente de as notificações serem fornecidas pelo serviço de notificação por push da Microsoft \ (MPNS \), serviço de notificação por push do Windows \ (WNS \) ou qualquer outro serviço.  Se o usuário desabilitar as notificações, seja em uma base específica do produto ou do sistema, a extensão deverá permanecer funcional.  

Se o seu produto usa o MPNS ou o WNS para transmitir notificações, ele deve estar em conformidade com os seguintes requisitos:  

#### Orientação geral do 1.9.1  

As notificações fornecidas pelo WNS ou pelo MPNS são consideradas conteúdo do produto e estão sujeitas a todas as políticas de desenvolvedor de catálogos de Complementos.  

#### 1.9.2 de propriedade de notificações  

Você não deve obscurecer nem tentar disfarçar a origem de qualquer notificação iniciada a partir de sua extensão.  

#### 1.9.3 sem informações confidenciais  

Você não deve incluir em uma notificação qualquer informação que os usuários possam considerar razoavelmente confidenciais ou confidenciais.  

#### 1.9.4 propósito de notificações  

As notificações enviadas da extensão devem estar relacionadas a essa extensão ou a outras extensões publicadas no catálogo de Complementos do Microsoft Edge e não devem incluir mensagens promocionais de qualquer tipo que não estejam relacionados a suas extensões.  

### 1,10 condução e conteúdo de publicidade  

Para todas as atividades relacionadas a publicidade, os seguintes requisitos se aplicam:  

#### finalidade do 1.10.1  

O conteúdo principal da extensão não deve ser anunciado, e a publicidade deve ser claramente distinguida de outro conteúdo na extensão.  

#### políticas e contratos do 1.10.2  

Qualquer conteúdo de publicidade que sua extensão exibe deve obedecer à [política de aceitação da Microsoft Creative][MicrosoftAdvertisingCreativeAcceptancePolicies].  
Se a sua extensão exibir anúncios, todo o conteúdo exibido deve estar de acordo com os requisitos de publicidade do [contrato de desenvolvedor de aplicativos][MicrosoftAppDeveloperAgreement] e esta política.  

#### qualidade de publicidade 1.10.3  

*   O objetivo principal da extensão não deve ser fazer com que os usuários cliquem em anúncios.  
*   Sua extensão não deve fazer nada que interfira ou diminua a visibilidade, o valor ou a qualidade de qualquer anúncio exibido.  

#### promoções de 1.10.4  

Se você comprar ou criar campanhas publicitárias promocionais para promover suas extensões por meio da funcionalidade de campanha publicitária no [centro de parceiros][MicrosoftPartnerCenter], todos os materiais de anúncios fornecidos à Microsoft, incluindo todas as páginas iniciais associadas, devem estar em conformidade com a [política de especificações do Microsoft Creative][MicrosoftAdvertisingCreativeSpecifications] e com a [política de aceitação do Microsoft Creative][MicrosoftAdvertisingCreativeAcceptancePolicies].  

#### 1.10.5 notificando os usuários sobre o cancelamento de publicidade baseada em juros  

Sua declaração de privacidade ou termos de uso devem permitir que os usuários saibam que você planeja enviar informações pessoais para o provedor de serviços de anúncios e deve informar aos usuários como elas podem recusar anúncios baseados em juros.  

#### 1.10.6 outras diretrizes  

Se a extensão for direcionada para crianças com menos de 13 anos, conforme definido na [lei de proteção de privacidade online da criança][FTCChildrensPrivacy]; Você deve notificar a Microsoft sobre esse fato ao [centro de parceria][MicrosoftPartnerCenter] e garantir que todo o conteúdo do anúncio exibido na extensão seja apropriado para crianças com menos de 13 anos.  

## 2 políticas de conteúdo  

As políticas a seguir se aplicam ao conteúdo e aos metadados \ (incluindo o nome do editor, o nome da extensão, o ícone de extensão, a descrição da extensão, as capturas de tela, os trailers de extensão e as miniaturas do trailer e qualquer outro metadado de extensão \) oferecido para distribuição em Complementos do Microsoft Edge.  Conteúdo significa imagens, sons, vídeos e texto contidos na extensão, os blocos, notificações, mensagens de erro ou anúncios expostos por meio da extensão e qualquer coisa entregue de um servidor ou para o qual a extensão se conecta.  Como as extensões e Complementos do Microsoft Edge são usados em todo o mundo, esses requisitos são interpretados e aplicados no contexto de normas regionais e culturais.  

### 2,1 requisitos de conteúdo para a listagem de catálogo addon do Microsoft Edge  

Os metadados e outros conteúdos que você envia para acompanhar sua extensão podem não conter conteúdo maduro.  
Os envios que não atendem aos requisitos de listagens da loja de extensão são rejeitados ou removidos com aviso.  

### 2,2 conteúdo, incluindo nomes, logotipos, originais e terceiros  

Todo o conteúdo na extensão e os metadados associados devem ser criados originalmente por você ou licenciada apropriadamente de um detentor de direitos de terceiros e deve ser usado somente conforme permitido pelo titular dos direitos ou da mesma forma permitida por lei.  

### 2,3 risco de dano  

#### 2.3.1 requisitos  

Sua extensão não deve conter qualquer conteúdo que facilite ou glamorizes as seguintes atividades do mundo real: \ (a \) Extreme ou violência gratuita; \ (b \) violações de direitos humanos; \ (c \) a criação de armas ilegais; ou \ (d \) o uso de armas em relação a uma pessoa, um animal ou uma propriedade real ou pessoal.  

#### responsabilidade do 2.3.2  

Sua extensão não deve: \ (a \) gerar um risco de segurança, nem resultar em desconforto, ferimentos ou qualquer outro dano a usuários finais ou a qualquer outra pessoa ou animal; ou \ (b \) representam um risco ou resulta em danos à propriedade real ou pessoal.  Você é o único responsável por todos os testes de segurança de extensão, aquisição de certificados e implementação de qualquer proteção de recurso adequada.  Você não deve desabilitar qualquer recurso de segurança ou conforto da plataforma e deve incluir todos os avisos legalmente obrigatórios e de avisos padrão do setor e avisos de isenção de responsabilidade aplicáveis em sua extensão.  

### 2,4 difamatório, caluniadoras, Slanderous e ameaça  

Sua extensão não deve conter conteúdo que seja difamatório, caluniadoras, Slanderous ou ameaça.  

### 2,5 conteúdo ofensivo  

Sua extensão e metadados associados não devem conter conteúdo potencialmente confidencial ou ofensivo.  O conteúdo pode ser considerado confidencial ou ofensivo em determinados países/regiões, devido a leis locais ou a normas culturais.  Além disso, a extensão e os metadados associados não devem conter conteúdo que defende o discriminação, a hatred ou a violência com base em considerações de corrida, étnicas, origens nacionais, linguagem, sexo, idade, deficiência, religião, orientação sexual, status como veterano ou associação em qualquer outro grupo social.  

### 2,6 de álcool, tabaco e drogas  

Sua extensão não deve conter qualquer conteúdo que facilite ou glamorizes o uso excessivo ou Irresponsible de produtos de álcool ou tabaco ou drogas.  

### 2,7 conteúdo adulto  

Sua extensão não deve conter ou exibir conteúdo que uma pessoa razoável consideraria pornográfico ou sexual Explicit.  

### 2,8 conteúdo, serviços e atividades proibidos  

Sua extensão deve obedecer às seguintes condições.  

*   Sua extensão não deve conter conteúdo ou fornecer serviços que facilitem jogos online.  Jogos Online incluem, mas não se limitam a casinos online, aposta esportiva, loterias ou jogos de habilidade que oferecem prêmios de dinheiro ou outro valor.  
*   Sua extensão não deve fornecer acesso não autorizado ao conteúdo do site, por exemplo, burlando paywalls ou restrições de login.  
*   Sua extensão não deve fornecer, incentivar ou habilitar o acesso não autorizado, o download ou o fluxo de conteúdo ou mídias de direitos autorais.  
*   Sua extensão não deve ser o meu cryptocurrency.  

### 2,9 atividade ilegal  

Sua extensão não deve conter conteúdo ou funcionalidade que incentiva, facilita ou glamorizes atividades ilegais no mundo real.  

### 2,10 de profanação excessiva e conteúdo impróprio  

*   Sua extensão não deve conter profana excessiva ou gratuita.  
*   Sua extensão não deve conter ou exibir conteúdo que uma pessoa razoável considera obscena.  

### 2,11 requisitos específicos de país/região  

O conteúdo ofensivo em qualquer país/região ao qual a extensão é destinada não é permitido.  O conteúdo pode ser considerado ofensivo em determinados países/regiões devido a leis locais ou normas culturais.  Exemplos de conteúdo potencialmente ofensivo em determinados países/regiões incluem o seguinte:  

**China**  

*   Conteúdo sexual proibido  
*   Referências de território ou região contestada  
*   Fornecendo ou habilitando o acesso a conteúdo ou serviços que sejam ilegais em leis locais aplicáveis  

### Classificações etárias de 2,12  

#### Conteúdo maduro 2.12.1  

Ao enviar sua extensão para o [Partner Center][MicrosoftPartnerCenter], você deve indicar se a extensão exibe conteúdo que deve ser marcado como "maduro".  Ao determinar a classificação de sua extensão, considere todo o conteúdo em seu aplicativo, incluindo conteúdo gerado pelo usuário e anúncios, e para o conteúdo que sua extensão conecta.  Se você indicar que sua extensão não contém nenhum conteúdo "maduro", você é responsável por manter a precisão dessa classificação.  Independentemente da classificação fornecida à sua extensão, ela ainda deve obedecer a todos os requisitos de conteúdo das políticas de desenvolvedor dos complementos do Microsoft Edge  

#### Alterações de classificação do 2.12.2  

Se a extensão fornecer conteúdo \ (como gerado pelo usuário, varejo ou outro conteúdo baseado na Web \) que possa ser apropriado para uma classificação de idade mais alta do que a classificação atribuída, você deve exigir que os usuários optem por receber tal conteúdo usando um filtro de conteúdo ou entrando com uma conta pré-existente.  

### vídeos do 2,13  

Se você enviar um vídeo promocional na listagem, ele deverá seguir todas as diretrizes de conteúdo mencionadas nesta política.  Se optar por fornecer um link do YouTube, você deve garantir que os anúncios sejam desabilitados para vídeos específicos que você deseja inserir.  Para obter mais informações sobre como os anúncios são habilitados e desabilitados no YouTube, consulte [support.google.com/YouTube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] e [support.google.com/YouTube/answer/132596][GoogleYoutubeAnswer132596].  

<!-- image links -->  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Relaxar a política padrão-política de segurança de conteúdo \ (CSP \) | Documentos da Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de desenvolvedor de aplicativos | Documentos da Microsoft"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Como a Microsoft identifica malware e aplicativos potencialmente indesejados | Documentos da Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Definir seus formatos de anúncio padrão-ajuda do YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anúncios em vídeos inseridos-ajuda do YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privacidade dos filhos-Comissão Federal para comércio"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Políticas de aceitação criativa-Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Especificações criativas-Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Central de parceiros"  
