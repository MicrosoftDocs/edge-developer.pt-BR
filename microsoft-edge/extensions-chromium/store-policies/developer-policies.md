---
description: Políticas de desenvolvedor da Loja de complementos do Microsoft Edge
title: Políticas de desenvolvedor da Loja de complementos do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: cc34a95e08d01ebee54581222d0eb9fefa3dc458
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343077"
---
# Políticas de desenvolvedor da Loja de complementos do Microsoft Edge  

## Introdução e objetivo deste documento  

Obrigado por seu interesse em desenvolver extensões para a loja de Complementos do Microsoft Edge.  Os Complementos do Microsoft Edge armazenam políticas de desenvolvedor \(Políticas de desenvolvedor da loja de complementos\) se aplicam às suas extensões, incluindo o envio de extensões por meio do [Partner Center][MicrosoftPartnerCenter] e o provisionamento dessas extensões por meio dos Complementos do Microsoft Edge.  

## Princípios  

Alguns princípios para você começar:  

*   Você deve oferecer valor exclusivo e distinto em suas extensões para o Microsoft Edge.  Forneça um motivo atraente para baixar suas extensões da loja de Complementos do Microsoft Edge \(Complementos do Microsoft Edge\).  
*   Você não deve induzir nossos usuários conjuntos sobre o que sua extensão faz, quem a está oferecendo e assim por diante.  
*   Você não deve tentar roubar usuários, o sistema ou o ecossistema.  Não há lugar nos complementos do Microsoft Edge para qualquer tipo de fraude; seja classificações e manipulação de análise, fraude de cartão de crédito ou outras atividades fraudulentas.  
    
A adendo às políticas de desenvolvedor da loja de Complementos do Microsoft Edge deve ajudá-lo a fazer escolhas que aprimoram o atraente e público-alvo de sua extensão.  

Suas extensões são cruciais para a experiência de centenas de milhões de usuários.  Estamos ansiosos para experimentar o que você cria e está ansioso para ajudar a entregar suas extensões ao mundo.  

## 1. Políticas de produto  

### 1.1 Valor & Função Distinct; Representação precisa  

Sua extensão e os metadados associados devem refletir com precisão e clareza a origem, a funcionalidade e os recursos que você descreve.  

#### 1.1.1 As extensões devem ter uma única finalidade  

Sua extensão deve ter uma única finalidade com funcionalidade restrita.  

#### 1.1.2 Descrever sua extensão  

Todos os aspectos da extensão devem descrever com precisão as funções, os recursos e quaisquer limitações importantes da extensão, incluindo dispositivos de entrada necessários ou com suporte.  A proposta de valor da extensão deve ser clara durante a primeira experiência de executar.  Sua extensão pode não usar um nome ou ícone semelhante ao de outras extensões e não deve reivindicar representar uma empresa, corpo do governo ou outra entidade se você não tiver permissão para fazer essa representação.  

#### 1.1.3 Funcionalidade  

Sua extensão deve estar totalmente funcional.  

#### 1.1.4 Pesquisa e Descoberta  

Os termos de pesquisa podem não exceder sete termos exclusivos e devem ser relevantes para sua extensão.  

#### 1.1.5 Fornecer detalhes apropriados  

Você deve fornecer detalhes distintos e informativos sobre sua extensão e a funcionalidade na listagem \(metadados\) para sua extensão.  Sua extensão deve fornecer uma experiência de usuário valiosa e de qualidade.  Sua extensão também deve ter uma presença ativa nos Complementos do Microsoft Edge.  

#### 1.1.6 Estabilidade e desempenho  

Sua extensão não deve afetar negativamente o desempenho ou a estabilidade do Microsoft Edge.  

#### 1.1.7 Ofuscação  

Extensões com código ofuscado não são permitidas.  Isso inclui código no pacote de extensão, bem como qualquer código externo ou recurso buscado na Web.  Você pode ser solicitado a refatorar partes do seu código se ele não for revisível.  

#### 1.1.8 Alterar configurações do navegador  

Sua extensão não deve, sem o consentimento apropriado do usuário, alterar ou parecer alterar a funcionalidade ou as configurações do navegador, incluindo, mas não se limitando a: o provedor de pesquisa da barra de endereços e sugestões, a página inicial ou home page, a página nova guia e adicionar ou remover favoritos.  

Qualquer alteração nas configurações do navegador deve ser explicitamente documentada na descrição da extensão.  

Sua extensão só pode revisar as configurações de chave para substituir uma página da Web ou serviço da Microsoft por um \(por exemplo, exigir o uso de um mecanismo de pesquisa de terceiros ou definir a home page para uma propriedade da Web de terceiros\) se você for empregado ou associado a esses terceiros.  

### 1.2 Segurança  

Sua extensão não deve comprometer ou comprometer a segurança do usuário ou a segurança ou a funcionalidade do dispositivo, sistema ou sistemas relacionados.  

#### 1.2.1 Políticas de Segurança de Conteúdo  

> [!NOTE]
> Se você fizer alterações em sua extensão além da funcionalidade descrita, todas as alterações no código deverão ser compatíveis com a política de segurança de conteúdo [do Microsoft Edge.][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Por exemplo, sua extensão não deve baixar um script remoto e, subsequentemente, executar esse script de maneira que não seja consistente com a funcionalidade descrita.  

#### 1.2.2 Software indesejado e mal-intencionado  

Sua extensão não deve conter ou habilitar malware conforme definido pelos critérios da Microsoft para [Software Indesejado e Mal-intencionado.][MicrosoftIdentifiesMalwareUnwantedApplications]  

#### 1.2.3 Dependência de outro software  

Sua extensão pode depender de software não integrado \(como outro produto, módulo ou serviço\) para fornecer a funcionalidade principal, desde que você divulgar a dependência na descrição  

#### 1.2.4 Atualização de Extensões  

A menos que seja permitido de outra forma pela Microsoft, suas extensões devem ser atualizadas somente por meio de Complementos do Microsoft Edge.  

### 1.3 O produto é testável  

Sua extensão deve ser testável.  Se não for possível testar sua extensão por qualquer motivo, incluindo, mas não se limitando a, os itens abaixo, sua extensão pode falhar nesse requisito.  

#### 1.3.1 Credenciais de Usuário  

Se sua extensão exigir credenciais de logon, forneça uma conta de demonstração de trabalho usando o `Notes for certification` campo.  

#### 1.3.2 Disponibilidade de serviços  

Se a extensão exigir acesso a um servidor, o servidor deverá estar funcional para verificar se ele funciona corretamente.  

### 1.4 Usabilidade  

Sua extensão deve atender aos padrões de armazenamento dos Complementos do Microsoft Edge para usabilidade, incluindo, mas não se limitando a, aqueles listados nas subseções abaixo.  

#### 1.4.1 Compatibilidade entre plataformas  

Sua extensão deve ser compatível com o Microsoft Edge em todos os dispositivos e plataformas em que eles podem ser baixados.  Se uma extensão for baixada em um dispositivo com o qual não seja compatível, ela deverá detectar isso na tela de início e exibir uma mensagem para o usuário detalhando os requisitos que os dispositivos devem atender para serem compatíveis com sua extensão.  

#### 1.4.2 Experiência do Usuário  

Sua extensão deve iniciar imediatamente e deve permanecer responsiva à entrada do usuário.  Sua extensão deve continuar a ser executado e permanecer responsiva à entrada do usuário.  Sua extensão deve ser desligado normalmente e não ser fechada inesperadamente.  Sua extensão deve lidar com exceções e permanecer responsiva à entrada do usuário depois que a exceção for manipulada.  

### 1.5 Informações pessoais  

Os requisitos a seguir se aplicam às extensões que acessam Informações Pessoais.  As Informações Pessoais incluem todas as informações ou dados que identificam ou podem ser usados para identificar uma pessoa ou que estão associados a essas informações ou dados.  

#### 1.5.1 Coletar Informações Pessoais somente quando necessário  

Sua extensão pode coletar, acessar, usar ou transmitir Informações Pessoais \(incluindo a atividade de navegação na Web\); somente se exigido por e somente para uso em um recurso com destaque voltado para o usuário.  

#### 1.5.2 Manter uma política de privacidade  

Independentemente de sua extensão acessar, coletar ou transmitir Informações Pessoais; você deve fornecer um aviso de destaque e estar em conformidade com sua política de privacidade, se exigido por lei.  Sua política de privacidade deve informar os usuários sobre as Informações Pessoais acessadas, coletadas ou transmitidas por sua extensão, como essas informações são usadas, armazenadas e protegidas e indicar os tipos de partes para quem são divulgadas.  Sua política de privacidade deve descrever os controles que os usuários têm sobre o uso e o compartilhamento de suas informações, como eles acessam suas informações e devem estar em conformidade com as leis e regulamentos aplicáveis.  Sua política de privacidade deve ser mantida atualizada à medida que você adiciona novos recursos e funcionalidades à sua extensão.  

Se você fornecer à Microsoft sua política de privacidade, você concorda em permitir que a Microsoft compartilhe essa política de privacidade com os usuários da sua extensão.  

#### 1.5.3 Compartilhar dados com terceiros  

Você pode publicar as Informações Pessoais dos usuários da sua extensão para um serviço externo ou de terceiros por meio de sua extensão ou metadados associados somente depois de obter o consentimento de aceitação desses usuários.  Consentimento de aceitação significa que os usuários dão permissão expressa na interface do usuário da extensão para a atividade solicitada, depois de você:  

*   Descreva aos usuários como as informações são acessadas, usadas ou compartilhadas e indique os tipos de partes para quem são divulgadas e  
*   Forneça aos usuários um mecanismo na interface do usuário da extensão por meio do qual eles têm a opção de cancelar a permissão posteriormente e re optá-la.  
    
#### 1.5.4 Informações de compartilhamento de não usuários  

Se você publicar informações pessoais de uma pessoa em um serviço externo ou de terceiros por meio de sua extensão ou dos metadados, mas a pessoa cujas informações estão sendo compartilhadas não é um usuário de sua extensão;  

1.  Você deve obter o consentimento expresso por escrito para publicar essas Informações Pessoais.  
1.  Você deve permitir que a pessoa cujas informações são compartilhadas retire esse consentimento a qualquer momento.  
1.  Sua política de privacidade deve divulgar claramente que você pode coletar informações pessoais dessa maneira.  
1.  Se exigido por lei aplicável, você deve excluir as Informações Pessoais de qualquer pessoa mediante solicitação, incluindo indivíduos cujas informações você coleta dessa maneira.  
1.  Se sua extensão fornece aos usuários acesso às Informações Pessoais de outra pessoa, esse requisito também se aplica.  
    
#### 1.5.5 Transmitir informações com segurança  

Se sua extensão coletar, armazenar ou transmitir Informações Pessoais; ele deve fazer isso com segurança usando métodos de criptografia modernos.  

#### 1.5.6 Informações altamente confidenciais  

Sua extensão não deve coletar, armazenar ou transmitir informações pessoais altamente confidenciais, como dados de saúde ou financeiros, a menos que as informações estão relacionadas à funcionalidade da extensão.  Sua extensão também deve obter o consentimento expresso do usuário antes de coletar, armazenar ou transmitir essas informações.  

### 1.6 Permissões  

Sua extensão só deve solicitar as permissões necessárias para o funcionamento.  Você deve fornecer uma descrição de como sua extensão funciona.  Sua extensão só deve ter o desempenho descrito.  Sua extensão pode não solicitar permissão para recursos que vão além dos recursos necessários para executar e funcionar conforme declarado.  

### 1.7 Localização  

Você deve localizado sua extensão para todos os idiomas com suporte de sua extensão.  O texto da descrição da extensão deve ser localizado em cada idioma declarado.  
Se sua extensão estiver localizada de forma que alguns recursos não estão disponíveis em uma versão localizada, você deverá mostrar claramente ou exibir os limites de localização na descrição da extensão. A experiência fornecida por uma Extensão deve ser razoavelmente semelhante em todos os idiomas compatíveis.  

### 1.8 Transações Financeiras  

Se o produto incluir compra no produto, assinaturas, moeda virtual, funcionalidade de cobrança ou captura informações financeiras; os requisitos nas seções a seguir se aplicam.  

#### 1.8.1 Recursos pagos  

Sua extensão pode permitir que os usuários consumam conteúdo digital ou serviços comprados por meio de um mecanismo de compra de terceiros ou API.  

Você deve usar uma API de compra de terceiros segura para compras de bens ou serviços físicos.  Você deve usar uma API de compra de terceiros segura para pagamentos feitos em conexão com qualquer outro serviço, incluindo jogos de jogos de verdade ou contribuições de líderes.  

*   Se sua extensão for usada para facilitar ou coletar contribuições sociais ou para realizar uma promoção ou um prêmio promocional, você deverá fazê-lo em conformidade com a lei aplicável.  
*   Você também deve dizer claramente que a Microsoft não é a patrocinadora da promoção.  
*   As ofertas no produto vendidas em sua extensão não devem ser convertidas em qualquer moeda legalmente válida \(como USD, Euro e assim por diante\) ou quaisquer bens ou serviços físicos.  
    
Os seguintes requisitos se aplicam ao uso de uma API de compra segura de terceiros:  

*   No momento da transação ou quando você coleta qualquer informação de pagamento ou financeiro do usuário; sua extensão deve identificar o provedor de transações de comércio, autenticar o usuário e obter confirmação do usuário para a transação.  Um provedor de transações comerciais mantém uma plataforma segura para trocas financeiras.  
*   Sua extensão pode oferecer aos usuários a capacidade de salvar essa autenticação, mas os usuários devem ter a capacidade de exigir uma autenticação em cada transação ou desativar transações no produto.  
*   Se o ramal coletar informações de cartão de crédito ou usar um processador de pagamento de terceiros que colete informações de cartão de crédito, o processamento de pagamento deverá atender ao Padrão de Segurança de Dados PCI \(PCI DSS\).  
    
#### 1.8.2 Divulgação de recursos pagos  

Sua extensão e metadados associados devem fornecer informações sobre os tipos de compras no produto oferecidas e a faixa de preços.  Você não deve induzir os usuários e deve ser claro sobre a natureza de suas promoções e ofertas no produto, incluindo o escopo e os termos de qualquer experiência de avaliação.  Se sua extensão restringe o acesso ao conteúdo criado pelo usuário durante ou após uma avaliação, você deve notificar os usuários com antecedência.  Além disso, sua extensão deve deixar claro para os usuários que eles estão iniciando uma opção de compra em sua extensão.  

### 1.9 Notificações  

Sua extensão deve respeitar as configurações do sistema para notificações.  Isso significa que qualquer apresentação de anúncios e notificações aos usuários deve ser consistente com as preferências do usuário, independentemente de as notificações serem fornecidas pelo Microsoft Push Notification Service \(MPNS\), Windows Push Notification Service \(WNS\) ou qualquer outro serviço.  Se o usuário desabilitar as notificações, seja em um produto específico ou em todo o sistema, sua extensão deverá permanecer funcional.  

Se seu produto usa MPNS ou WNS para transmitir notificações, ele deve estar em conformidade com os seguintes requisitos:  

#### 1.9.1 Diretrizes gerais  

As notificações fornecidas por meio do WNS ou MPNS são consideradas conteúdo do produto e estão sujeitas a todas as Políticas de Desenvolvedor do Catálogo de Complementos.  

#### 1.9.2 Propriedade das notificações  

Você não deve ocultar ou tentar disfarçar a origem de qualquer notificação iniciada na extensão.  

#### 1.9.3 Nenhuma informação confidencial ou confidencial  

Você não deve incluir em uma notificação quaisquer informações que os usuários possam considerar razoavelmente confidenciais ou confidenciais.  

#### 1.9.4 Finalidade das notificações  

As notificações enviadas de sua extensão devem estar relacionadas a essa extensão ou a outras extensões que você publica na loja de Complementos do Microsoft Edge e não devem incluir mensagens promocionais de qualquer tipo que não estão relacionadas às suas extensões.  

### 1.10 Conteúdo e Conduta de Publicidade  

Para todas as atividades relacionadas à publicidade, os seguintes requisitos se aplicam:  

#### 1.10.1 Finalidade  

O conteúdo principal da extensão não deve ser de publicidade, e a publicidade deve ser claramente distinguível com outros conteúdos da extensão.  

#### 1.10.2 Políticas e Contratos  

Qualquer conteúdo de publicidade que sua extensão exibe deve aderir à [Política de Aceitação de Criatividade da Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Se sua extensão exibir anúncios, todo o conteúdo exibido deverá estar em conformidade com os requisitos de publicidade do Contrato de Desenvolvedor de Aplicativos [e][MicrosoftAppDeveloperAgreement] desta Política.  

#### 1.10.3 Qualidade da publicidade  

*   A principal finalidade da extensão não deve ser fazer com que os usuários cliquem em anúncios.  
*   Sua extensão não deve fazer nada que interfira ou diminua a visibilidade, o valor ou a qualidade de quaisquer anúncios que ela exibe.  

#### 1.10.4 Promoções  

Se você comprar ou criar campanhas publicitárias promocionais para promover suas extensões por meio da funcionalidade da campanha publicitária no [Partner Center][MicrosoftPartnerCenter], todos os materiais de publicidade que você fornece à Microsoft, incluindo qualquer página de aterrissagem associada, devem estar em conformidade com a Política de Especificações de [Criativos][MicrosoftAdvertisingCreativeSpecifications] da Microsoft e a Política de Aceitação de Criatividade da [Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  

#### 1.10.5 Notificando os usuários sobre Opt-Out para Interest-Based Publicidade  

Sua política de privacidade ou termos de uso deve permitir que os usuários saibam que você planeja enviar Informações Pessoais para o provedor de serviços de anúncios e devem dizer aos usuários como eles podem optar por não fazer publicidade baseada em interesse.  

#### 1.10.6 Outras diretrizes  

Se sua extensão for direcionada a crianças com menos de 13 anos, conforme definido na [Children's Online Privacy Protection Act][FTCChildrensPrivacy]; você deve notificar a Microsoft sobre esse fato no [Partner Center][MicrosoftPartnerCenter] e garantir que todo o conteúdo de publicação exibido em sua extensão seja apropriado para crianças com menos de 13 anos.  

## 2 Políticas de Conteúdo  

As políticas a seguir se aplicam ao conteúdo e aos metadados \(incluindo nome do editor, nome da extensão, ícone de extensão, descrição da extensão, capturas de tela de extensão, trailers de extensão e miniaturas de trailer e quaisquer outros metadados de extensão\) oferecidos para distribuição nos Complementos do Microsoft Edge.  Conteúdo significa as imagens, sons, vídeos e texto contidos em sua extensão, os blocos, notificações, mensagens de erro ou anúncios expostos por meio de sua extensão e qualquer coisa entregue de um servidor ou ao qual sua extensão se conecta.  Como as extensões e os Complementos do Microsoft Edge são usados em todo o mundo, esses requisitos são interpretados e aplicados no contexto das normas regionais e culturais.  

### 2.1 Requisitos de conteúdo para listagem do Catálogo de Complementos do Microsoft Edge  

Os metadados e outros conteúdos que você envia para acompanhar sua extensão podem não conter conteúdo adulto.  
Os envios que não atendem aos requisitos de listagens da loja de Complementos do Microsoft Edge são rejeitados ou removidos imediatamente.  

### 2.2 Conteúdo incluindo nomes, logotipos, originais e de terceiros  

Todo o conteúdo em sua extensão e metadados associados deve ser criado originalmente por você ou licenciado adequadamente de um titular de direitos de terceiros e deve ser usado somente conforme permitido pelo titular dos direitos ou conforme permitido por lei.  

### 2.3 Risco de danos  

#### 2.3.1 Requisitos  

Sua extensão não deve conter nenhum conteúdo que facilite ou fazer reflexos das seguintes atividades do mundo real: \(a\) violência gratuita ou extrema; \(b\) violações de direitos humanos; \(c\) a criação de armas ilegais; ou \(d\) o uso de armas contra uma pessoa, sua propriedade real ou pessoal.  

#### 2.3.2 Responsabilidade  

Sua extensão não deve: \(a\) representar um risco de segurança para, nem resultar em reação, dano ou qualquer outro dano aos usuários finais ou a qualquer outra pessoa ou filho; ou \(b\) representa um risco ou resultar em danos a propriedades reais ou pessoais.  Você é o único responsável por todos os testes de segurança de extensão, aquisição de certificados e implementação de quaisquer proteções de recurso apropriadas.  Você não deve desabilitar nenhum recurso de segurança ou conforto da plataforma e deve incluir todos os avisos, avisos e avisos de isenção aplicáveis legalmente e padrão do setor em sua extensão.  

### 2.4 Defamatory, Libelous, Sousous e  

Sua extensão não deve conter qualquer conteúdo que seja defamatório, libeloso, sálogo ou ameaçador.  

### 2.5 Conteúdo ofensivo  

Sua extensão e metadados associados não devem conter conteúdo potencialmente sensível ou ofensivo.  O conteúdo pode ser considerado sensível ou ofensivo em determinados países/regiões devido a leis locais ou normas culturais.  Além disso, sua extensão e os metadados associados não devem conter conteúdo que defender a violência, violência ou violência com base em considerações de corrida, diversidade, origem nacional, idioma, sexo, idade, deficiência, física, orientação sexual, status como membro de qualquer outro grupo social.  

### 2,6 Abusos, Abusos e Armas  

Sua extensão não deve conter qualquer conteúdo que facilite ou esvaça o uso excessivo ou excessivo de produtos de petróleo ou petróleo.  

### 2.7 Conteúdo adulto  

Sua extensão não deve conter ou exibir conteúdo que uma pessoa razoável consideraria explícita ouicic.  

### 2.8 Conteúdo, Serviços e Atividades Proibidos  

Sua extensão deve cumprir as seguintes condições.  

*   Sua extensão não deve conter conteúdo ou fornecer serviços que facilitem jogos online.  Jogos online incluem, mas não se limitando a volantes online, esportes, esportes ou jogos de habilidades que oferecem jogadores de dinheiro ou outro valor.  
*   Sua extensão não deve fornecer acesso não autorizado ao conteúdo do site, por exemplo, contornando as restrições de pagamento ou de logon.  
*   Sua extensão não deve fornecer, incentivar ou habilitar o acesso não autorizado, download ou streaming de conteúdo ou mídia protegido por direitos autorais.  
*   Sua extensão não deve minerar a criptografia.  
    
### 2.9 Atividade ilegal  

Sua extensão não deve conter conteúdo ou funcionalidade que incentiva, facilita ou reflete a atividade ilegal no mundo real.  

### 2.10 Linguagem excessiva e conteúdo inadequado  

*   Sua extensão não deve conter profanação excessiva ou gratuita.  
*   Sua extensão não deve conter ou exibir conteúdo que uma pessoa razoável considere obscena.  
    
### 2.11 Requisitos específicos do país/região  

O conteúdo ofensivo em qualquer país/região para o qual sua extensão está direcionada não é permitido.  O conteúdo pode ser considerado ofensivo em determinados países/regiões devido a leis locais ou normas culturais.  Exemplos de conteúdo potencialmente ofensivo em determinados países/regiões incluem o seguinte:  

**China**  

*   Conteúdo sexual proibido  
*   Referências de território ou região em disputa  
*   Fornecendo ou habilitando o acesso a conteúdo ou serviços que são ilegais sob a lei local aplicável  
    
### 2,12 Classificações Etárias  

#### 2.12.1 Conteúdo de vencimento  

Ao enviar sua extensão para o [Partner Center,][MicrosoftPartnerCenter]você deve indicar se sua extensão exibe o conteúdo que deve ser marcado como "Adulto".  Ao determinar a classificação para sua extensão, considere todo o conteúdo em seu aplicativo, incluindo conteúdo gerado pelo usuário e anúncios e o conteúdo que sua extensão vincula.  Se você indicar que sua extensão não contém conteúdo "Adulto", será responsável por manter a precisão dessa classificação.  Independentemente da classificação dada à sua extensão, ela ainda deve cumprir todos os requisitos de conteúdo das políticas de Desenvolvedor de Complementos do Microsoft Edge  

#### 2.12.2 Alteração de Classificações  

Se sua extensão fornece conteúdo \(como gerado pelo usuário, varejo ou outro conteúdo baseado na Web\) que pode ser apropriado para uma classificação etária maior do que a atribuída, você deve exigir que os usuários optem por receber esse conteúdo usando um filtro de conteúdo ou entrando com uma conta pré-existente.  

### 2.13 Vídeos  

Se você enviar um vídeo promocional na listagem, ele deverá seguir todas as diretrizes de conteúdo mencionadas nesta política.  Se você optar por fornecer um link do YouTube, deverá garantir que os anúncios sejam desabilitados para os vídeos específicos que você deseja inserir.  Para obter mais informações sobre como os anúncios são habilitados e desabilitados no YouTube, [consulte support.google.com/youtube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] e [support.google.com/youtube/answer/132596][GoogleYoutubeAnswer132596].  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Como desabilizar a política padrão - Política de Segurança de Conteúdo \(CSP\) | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de Desenvolvedor de Aplicativos | Microsoft Docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Como a Microsoft identifica malware e aplicativos potencialmente indesejados | Microsoft Docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Definir os formatos de vídeo padrão - Ajuda do YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anúncios em vídeos incorporados - Ajuda do YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privacidade das Crianças - Comissão Federal de Comércio"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Políticas de aceitação criativas - Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Especificações Criativas - Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
