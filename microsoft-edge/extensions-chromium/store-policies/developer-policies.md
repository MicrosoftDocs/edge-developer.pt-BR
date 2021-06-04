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

##  <a name="introduction-and-objective-of-this-document"></a>Introdução e objetivo deste documento  

Obrigado por seu interesse em desenvolver extensões para o Microsoft Edge de complementos.  As políticas de desenvolvedor do armazenamento de complementos do Microsoft Edge \(Políticas de desenvolvedor do armazenamento de complementos\) se aplicam às suas extensões, incluindo o envio de extensões por meio do [Partner Center][MicrosoftPartnerCenter] e a provisão dessas extensões por meio dos complementos do Microsoft Edge.  

##  <a name="principles--"></a>Princípios  

Alguns princípios para começar:  

*   Você deve oferecer um valor exclusivo e distinto em suas extensões para Microsoft Edge.  Forneça um motivo atraente para baixar suas extensões do Microsoft Edge de complementos \(Microsoft Edge complementos\).  
*   Você não deve enganar nossos usuários conjuntos sobre o que sua extensão faz, quem a está oferecendo e assim por diante.  
*   Você não deve tentar enganar usuários, o sistema ou o ecossistema.  Não há lugar em nossas Microsoft Edge complementos para qualquer tipo de fraude; seja classificações e manipulação de revisão, fraude de cartão de crédito ou outra atividade fraudulenta.  
    
A adesão às Microsoft Edge de desenvolvedor do armazenamento de complementos deve ajudá-lo a fazer escolhas que aprimoram o recurso e a audiência de sua extensão.  

Suas extensões são cruciais para a experiência de centenas de milhões de usuários.  Estamos ansiosos para experimentar o que você cria e está animado para ajudar a entregar suas extensões para o mundo.  

##  <a name="1.-product-policies"></a>1. Políticas de produto  

###  <a name="1.1-distinct-function-&-value;-accurate-representation"></a>1.1 Função Distinta & Valor; Representação precisa  

Sua extensão e metadados associados devem refletir com precisão e clareza a origem, a funcionalidade e os recursos descritos.  

#### 1.1.1 Extensões devem ter uma única finalidade  

Sua extensão deve ter uma única finalidade com funcionalidade estreita.  

#### 1.1.2 Descrever sua extensão  

Todos os aspectos de sua extensão devem descrever com precisão as funções, recursos e quaisquer limitações importantes de sua extensão, incluindo dispositivos de entrada necessários ou suportados.  A proposta de valor da extensão deve ser clara durante a primeira experiência de executar.  Sua extensão pode não usar um nome ou ícone semelhante ao de outras extensões e não deve reivindicar representar uma empresa, um corpo governamental ou outra entidade se você não tiver permissão para fazer essa representação.  

#### Funcionalidade 1.1.3  

Sua extensão deve estar totalmente funcional.  

#### 1.1.4 Pesquisa e Descoberta  

Os termos de pesquisa podem não exceder sete termos exclusivos e devem ser relevantes para sua extensão.  

#### 1.1.5 Fornecer detalhes apropriados  

Você deve fornecer detalhes distintos e informativos sobre sua extensão e a funcionalidade na listagem \(metadados\) para sua extensão.  Sua extensão deve fornecer uma experiência de usuário valiosa e de qualidade.  Sua extensão também deve ter uma presença ativa Microsoft Edge complementos.  

#### 1.1.6 Estabilidade e desempenho  

Sua extensão não deve afetar negativamente o desempenho ou a estabilidade de Microsoft Edge.  

#### 1.1.7 Ofuscação  

Extensões com código ofuscado não são permitidas.  Isso inclui código no pacote de extensão, bem como qualquer código externo ou recurso buscado na Web.  Você pode ser solicitado a refactor partes do seu código se ele não for revisível.  

#### 1.1.8 Altering Browser Configurações  

Sua extensão não deve, sem o consentimento do usuário apropriado, alterar ou parecer alterar, a funcionalidade do navegador ou as configurações, incluindo, mas não se limitando a: o provedor de pesquisa da barra de endereços e sugestões, a página inicial ou inicial, a nova página de tabulação e a adição ou remoção do favorito.  

Qualquer alteração nas configurações do navegador deve ser documentada explicitamente na descrição da extensão.  

Sua extensão só pode revisar as configurações de chave para substituir uma página da Web da Microsoft ou um serviço por um \(como exigir o uso de um mecanismo de pesquisa de terceiros ou definir a home page como uma propriedade da Web de terceiros\) se você estiver empregado ou associado a esse terceiro.  

###  <a name="1.2-security"></a>1.2 Segurança  

Sua extensão não deve comprometer ou comprometer a segurança do usuário ou a segurança ou a funcionalidade do dispositivo, sistema ou sistemas relacionados.  

#### 1.2.1 Políticas de Segurança de Conteúdo  

> [!NOTE]
> Se você fizer alterações na extensão além da funcionalidade descrita, quaisquer alterações no código devem estar em conformidade com a política de segurança de Microsoft Edge [de conteúdo.][MicrosoftEdgeContentSecurityPolicyRemoteScript]  Por exemplo, sua extensão não deve baixar um script remoto e, posteriormente, executar esse script de maneira que não seja consistente com a funcionalidade descrita.  

#### 1.2.2 Software indesejado e mal-intencionado  

Sua extensão não deve conter ou habilitar malware conforme definido pelos critérios da Microsoft para Software Indesejado [e Mal-Intencionado.][MicrosoftIdentifiesMalwareUnwantedApplications]  

#### 1.2.3 Dependência de outro software  

Sua extensão pode depender de software não integrado \(como outro produto, módulo ou serviço\) para fornecer a funcionalidade principal, desde que você revele a dependência na descrição  

#### Atualização de Extensões 1.2.4  

A menos que seja permitido de outra forma pela Microsoft, suas extensões devem ser atualizadas somente Microsoft Edge complementos.  

###  <a name="1.3-product-is-testable"></a>1.3 O produto é testável  

Sua extensão deve ser testável.  Se não for possível testar sua extensão por qualquer motivo, incluindo, mas não se limitando a, os itens abaixo, sua extensão pode falhar nesse requisito.  

#### 1.3.1 Credenciais de Usuário  

Se a extensão exigir credenciais de logon, forneça uma conta de demonstração funcionando usando o `Notes for certification` campo.  

#### 1.3.2 Disponibilidade de serviços  

Se a extensão exigir acesso a um servidor, o servidor deverá estar funcional para verificar se ele funciona corretamente.  

###  <a name="1.4-usability"></a>1.4 Usabilidade  

Sua extensão deve atender Microsoft Edge padrões de armazenamento de complementos para usabilidade, incluindo, mas não se limitando aos listados nas subseções abaixo.  

#### 1.4.1 Compatibilidade entre plataformas  

Sua extensão deve ser compatível com Microsoft Edge em todos os dispositivos e plataformas em que eles podem ser baixados.  Se uma extensão for baixada em um dispositivo com o qual não seja compatível, ela deverá detectar isso no início e exibir uma mensagem para o usuário detalhando os requisitos que os dispositivos devem atender para serem compatíveis com sua extensão.  

#### 1.4.2 Experiência do Usuário  

Sua extensão deve ser inativa e ser responsiva à entrada do usuário.  Sua extensão deve continuar a ser executado e permanecer respondendo à entrada do usuário.  Sua extensão deve ser fechada normalmente e não fechar inesperadamente.  Sua extensão deve manipular exceções e permanecer responsiva à entrada do usuário depois que a exceção for manipulada.  

###  <a name="1.5-personal-information"></a>1.5 Informações Pessoais  

Os requisitos a seguir se aplicam a extensões que acessam Informações Pessoais.  As Informações Pessoais incluem todas as informações ou dados que identificam ou podem ser usados para identificar uma pessoa ou que estão associadas a essas informações ou dados.  

#### 1.5.1 Coletar Informações Pessoais somente quando necessário  

Sua extensão pode coletar, acessar, usar ou transmitir Informações Pessoais \(incluindo atividade de navegação na Web\); somente se necessário e somente para uso em um recurso proeminentemente divulgado, voltado para o usuário.  

#### 1.5.2 Manter uma política de privacidade  

Independentemente de sua extensão acessar, coletar ou transmitir Informações Pessoais; você deve fornecer aviso de destaque e estar em conformidade com sua política de privacidade, se necessário por lei.  Sua política de privacidade deve informar aos usuários sobre as Informações Pessoais acessadas, coletadas ou transmitidas por sua extensão, como essas informações são usadas, armazenadas e protegidas e indicam os tipos de partes às quais são divulgadas.  Sua política de privacidade deve descrever os controles que os usuários têm sobre o uso e o compartilhamento de suas informações, como eles acessam suas informações e devem estar em conformidade com as leis e regulamentos aplicáveis.  Sua política de privacidade deve ser mantida atualizada à medida que você adiciona novos recursos e funcionalidade à sua extensão.  

Se você fornecer à Microsoft sua política de privacidade, você concorda em permitir que a Microsoft compartilhe essa política de privacidade com os usuários de sua extensão.  

#### 1.5.3 Compartilhamento de dados com terceiros  

Você pode publicar as Informações Pessoais dos usuários de sua extensão para um serviço externo ou de terceiros por meio de sua extensão ou metadados associados somente depois de obter o consentimento de aceitação desses usuários.  Consentimento de aceitação significa que os usuários dão permissão expressa na interface do usuário da extensão da atividade solicitada, depois de você:  

*   Descreva aos usuários como as informações são acessadas, usadas ou compartilhadas e indicam os tipos de partes às quais são divulgadas e  
*   Forneça aos usuários um mecanismo em sua interface do usuário de extensão por meio do qual eles têm a opção de rescindir posteriormente a permissão e a aceitação.  
    
#### 1.5.4 Informações de compartilhamento de não usuários  

Se você publicar as Informações Pessoais de uma pessoa a um serviço externo ou a terceiros por meio da extensão ou dos metadados, mas a pessoa cujas informações estão sendo compartilhadas não é um usuário de sua extensão;  

1.  Você deve obter consentimento expresso por escrito para publicar essas Informações Pessoais.  
1.  Você deve permitir que a pessoa cujas informações são compartilhadas retire esse consentimento a qualquer momento.  
1.  Sua política de privacidade deve divulgar claramente que você pode coletar informações pessoais dessa maneira.  
1.  Se necessário pela lei aplicável, exclua as Informações Pessoais de qualquer indivíduo mediante solicitação, incluindo indivíduos cujas informações você coletar dessa maneira.  
1.  Se sua extensão fornece aos usuários acesso às Informações Pessoais de outra pessoa, esse requisito também se aplica.  
    
#### 1.5.5 Transmitir informações com segurança  

Se sua extensão coletar, armazenar ou transmitir Informações Pessoais; ele deve fazer isso com segurança usando métodos modernos de criptografia.  

#### 1.5.6 Informações altamente confidenciais  

Sua extensão não deve coletar, armazenar ou transmitir informações pessoais altamente confidenciais, como dados de saúde ou financeiros, a menos que as informações estão relacionadas à funcionalidade de sua extensão.  Sua extensão também deve obter o consentimento expresso do usuário antes de coletar, armazenar ou transmitir essas informações.  

###  <a name="1.6-permissions"></a>1.6 Permissões  

Sua extensão só deve solicitar as permissões necessárias para o funcionamento.  Você deve fornecer uma descrição de como sua extensão funciona.  Sua extensão só deve ter o desempenho conforme descrito.  Sua extensão pode não solicitar permissão para recursos que vão além dos recursos necessários para executar e funcionar conforme declarado.  

###  <a name="1.7-localization"></a>1.7 Localização  

Você deve localizar sua extensão para todos os idiomas que sua extensão diz ter suporte.  O texto da descrição de sua extensão deve ser localizado em cada idioma que você declarar.  
Se sua extensão for localizada de forma que alguns recursos não estão disponíveis em uma versão localizada, você deve dizer claramente ou exibir os limites de localização em sua descrição de extensão. A experiência fornecida por um Extension deve ser razoavelmente semelhante em todos os idiomas compatíveis.  

###  <a name="1.8-financial-transactions"></a>1.8 Transações Financeiras  

Se o produto incluir compra no produto, assinaturas, moeda virtual, funcionalidade de cobrança ou captura informações financeiras; os requisitos nas seções a seguir se aplicam.  

#### 1.8.1 Recursos pagos  

Sua extensão pode permitir que os usuários consumam conteúdo digital ou serviços adquiridos por meio de um mecanismo de compra ou API de terceiros.  

Você deve usar uma API de compra de terceiros segura para compras de bens físicos ou serviços.  Você deve usar uma API de compra segura de terceiros para pagamentos feitos em conexão com qualquer outro serviço, incluindo apostas no mundo real ou contribuições de caridade.  

*   Se sua extensão for usada para facilitar ou coletar contribuições de caridade ou para conduzir um concurso ou um sorteio promocional, você deve fazê-lo em conformidade com a lei aplicável.  
*   Você também deve dizer claramente que a Microsoft não é a patrocinadora da promoção.  
*   As ofertas no produto vendidas em sua extensão não devem ser convertidas em qualquer moeda legalmente válida \(como USD, Euro e assim por diante\) ou quaisquer bens ou serviços físicos.  
    
Os seguintes requisitos se aplicam ao uso de uma API de compra de terceiros segura:  

*   No momento da transação ou quando você coleta qualquer pagamento ou informações financeiras do usuário; sua extensão deve identificar o provedor de transações de comércio, autenticar o usuário e obter a confirmação do usuário para a transação.  Um provedor de transações de comércio mantém uma plataforma segura para trocas financeiras.  
*   Sua extensão pode oferecer aos usuários a capacidade de salvar essa autenticação, mas os usuários devem ter a capacidade de exigir uma autenticação em cada transação ou desativar transações no produto.  
*   Se sua extensão coletar informações de cartão de crédito ou usar um processador de pagamento de terceiros que colete informações de cartão de crédito, o processamento de pagamento deverá atender ao padrão atual de segurança de dados pci \(PCI DSS\).  
    
#### 1.8.2 Divulgar recursos pagos  

Sua extensão e metadados associados devem fornecer informações sobre os tipos de compras no produto oferecidas e o intervalo de preços.  Você não deve enganar os usuários e deve ser claro sobre a natureza de suas promoções e ofertas no produto, incluindo o escopo e os termos de qualquer experiência de avaliação.  Se a extensão restringir o acesso ao conteúdo criado pelo usuário durante ou após uma avaliação, você deve notificar os usuários com antecedência.  Além disso, sua extensão deve deixar claro para os usuários que eles estão iniciando uma opção de compra em sua extensão.  

###  <a name="1.9-notifications"></a>1.9 Notificações  

Sua extensão deve respeitar as configurações do sistema para notificações.  Isso significa que qualquer apresentação de anúncios e notificações aos usuários deve ser consistente com as preferências do usuário, independentemente de as notificações serem fornecidas pelo Serviço de Notificação por Push da Microsoft \(MPNS\), Windows Serviço de Notificação por Push \(WNS\) ou qualquer outro serviço.  Se o usuário desabilitar as notificações, seja em um produto específico ou em todo o sistema, sua extensão deve permanecer funcional.  

Se o produto usa MPNS ou WNS para transmitir notificações, ele deve estar em conformidade com os seguintes requisitos:  

#### 1.9.1 Diretrizes Gerais  

As notificações fornecidas por meio do WNS ou MPNS são consideradas conteúdo do produto e estão sujeitas a todas as Políticas de Desenvolvedores de Catálogo de Complementos.  

#### 1.9.2 Propriedade de notificações  

Você não deve obscurecer ou tentar disfarçar a origem de qualquer notificação iniciada de sua extensão.  

#### 1.9.3 Nenhuma informação confidencial ou confidencial  

Você não deve incluir em uma notificação qualquer informação que os usuários possam considerar razoavelmente confidenciais ou confidenciais.  

#### 1.9.4 Finalidade das notificações  

As notificações enviadas de sua extensão devem estar relacionadas a essa extensão ou a outras extensões que você publica no armazenamento de complementos do Microsoft Edge e não devem incluir mensagens promocionais de qualquer tipo que não sejam relacionadas às suas extensões.  

###  <a name="1.10-advertising-conduct-and-content"></a>1.10 Comportamento e conteúdo de publicidade  

Para todas as atividades relacionadas à publicidade, os seguintes requisitos se aplicam:  

#### 1.10.1 Finalidade  

O conteúdo principal da extensão não deve ser publicidade, e a publicidade deve ser claramente distinguível de outro conteúdo em sua extensão.  

#### 1.10.2 Políticas e Acordos  

Qualquer conteúdo de publicidade que sua extensão exibe deve aderir à Política de Aceitação Criativa [da Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  
Se sua extensão exibir anúncios, todo o conteúdo exibido deverá estar em conformidade com os requisitos de publicidade do Contrato de Desenvolvedor de Aplicativos [e][MicrosoftAppDeveloperAgreement] desta Política.  

#### 1.10.3 Qualidade da publicidade  

*   O principal objetivo da extensão não deve ser fazer com que os usuários cliquem em anúncios.  
*   Sua extensão não deve fazer nada que interfira ou diminua a visibilidade, o valor ou a qualidade de todos os anúncios que ele exibe.  

#### 1.10.4 Promoções  

Se você comprar ou criar campanhas publicitárias promocionais para promover suas extensões por meio da funcionalidade de campanha publicitária no [Partner Center][MicrosoftPartnerCenter], todos os materiais de publicidade que você fornece à Microsoft, incluindo quaisquer páginas de aterrissagem [associadas,][MicrosoftAdvertisingCreativeSpecifications] devem estar em conformidade com a Política de Especificações Criativas da Microsoft e a Política de Aceitação Criativa da [Microsoft.][MicrosoftAdvertisingCreativeAcceptancePolicies]  

#### 1.10.5 Notificando usuários do Opt-Out para Interest-Based Publicidade  

Sua instrução de privacidade ou termos de uso deve permitir que os usuários saibam que você planeja enviar Informações Pessoais para o provedor de serviços de anúncios e deve dizer aos usuários como eles podem optar por não fazer publicidade baseada em juros.  

#### 1.10.6 Outras diretrizes  

Se sua extensão for direcionada a crianças menores de 13 anos, conforme definido na Lei de Proteção de Privacidade Online para [Crianças;][FTCChildrensPrivacy] você deve notificar a Microsoft sobre esse fato no [Partner Center][MicrosoftPartnerCenter] e garantir que todo o conteúdo do comercial exibido em sua extensão seja apropriado para crianças menores de 13 anos.  

##  <a name="2-content-policies"></a>2 Políticas de Conteúdo  

As políticas a seguir se aplicam a conteúdo e metadados \(incluindo nome do editor, nome da extensão, ícone de extensão, descrição de extensão, capturas de tela de extensão, trailers de extensão e miniaturas de trailer e quaisquer outros metadados de extensão\) oferecidos para distribuição em complementos Microsoft Edge.  O conteúdo significa as imagens, sons, vídeos e texto contidos em sua extensão, os blocos, notificações, mensagens de erro ou anúncios expostos por meio de sua extensão e qualquer coisa entregue de um servidor ou ao qual sua extensão se conecta.  Como extensões e Microsoft Edge complementos são usados em todo o mundo, esses requisitos são interpretados e aplicados no contexto de normas regionais e culturais.  

###  <a name="2.1-content-requirements-for-microsoft-edge-addon-catalog-listing"></a>2.1 Requisitos de conteúdo para Microsoft Edge lista de catálogos de complementos  

Os metadados e outros conteúdos que você envia para acompanhar sua extensão podem não conter conteúdo maduro.  
Os envios que não atendem Microsoft Edge requisitos de listagem do armazenamento de complementos são rejeitados ou removidos prontamente.  

###  <a name="2.2-content-including-names,-logos,-original,-and-third-party"></a>2.2 Conteúdo incluindo nomes, logotipos, originais e terceiros  

Todo o conteúdo em sua extensão e metadados associados deve ser originalmente criado pelo usuário ou licenciado adequadamente de um titular de direitos de terceiros e deve ser usado apenas conforme permitido pelo titular dos direitos ou conforme permitido por lei.  

###  <a name="2.3-risk-of-harm"></a>2.3 Risco de danos  

#### 2.3.1 Requisitos  

Sua extensão não deve conter qualquer conteúdo que facilite ou envidraça as seguintes atividades do mundo real: \(a\) violência extrema ou gratuita; \(b\) violações de direitos humanos; \(c\) a criação de armas ilegais; ou \(d\) o uso de armas contra uma pessoa, um animal ou uma propriedade real ou pessoal.  

#### Responsabilidade 2.3.2  

Sua extensão não deve: \(a\) representar um risco de segurança, nem resultar em desconforto, danos ou qualquer outro dano aos usuários finais ou a qualquer outra pessoa ou animal; ou \(b\) representam um risco ou resultam em danos a propriedades reais ou pessoais.  Você é o único responsável por todos os testes de segurança de extensão, aquisição de certificados e implementação de quaisquer proteções de recursos apropriadas.  Você não deve desabilitar nenhum recurso de segurança ou conforto da plataforma e deve incluir todos os avisos, avisos e avisos, avisos e avisos de isenção de responsabilidade legais aplicáveis em sua extensão.  

###  <a name="2.4-defamatory,-libelous,-slanderous,-and-threatening"></a>2.4 Defamatory, Libelous, Slanderous e Threatening  

Sua extensão não deve conter qualquer conteúdo que seja difamatório, caluniador, caluniador ou ameaçador.  

###  <a name="2.5-offensive-content"></a>2.5 Conteúdo ofensivo  

Sua extensão e metadados associados não devem conter conteúdo potencialmente sensível ou ofensivo.  O conteúdo pode ser considerado sensível ou ofensivo em determinados países/regiões devido a leis locais ou normas culturais.  Além disso, sua extensão e metadados associados não devem conter conteúdo que defenda a discriminação, o desdém ou a violência com base em considerações de raça, etnidade, origem nacional, idioma, sexo, idade, deficiência, religião, orientação sexual, status como um veterano ou associação em qualquer outro grupo social.  

###  <a name="2.6-alcohol,-tobacco,-and-drugs"></a>2.6 Álcool, Tabaco e Drogas  

Sua extensão não deve conter qualquer conteúdo que facilite ou envidraça o uso excessivo ou irresponsável de álcool ou produtos de tabaco ou drogas.  

###  <a name="2.7-adult-content"></a>2.7 Conteúdo Adulto  

Sua extensão não deve conter ou exibir conteúdo que uma pessoa razoável consideraria sexualmente ou sexualmente explícita.  

###  <a name="2.8-prohibited-content,-services,-and-activity"></a>2.8 Conteúdo, Serviços e Atividades Proibidos  

Sua extensão deve seguir as seguintes condições.  

*   Sua extensão não deve conter conteúdo ou fornecer serviços que facilitem o jogo online.  O jogo online inclui, mas não se limita a casinos online, apostas de esportes, lotéricas ou jogos de habilidade que oferecem prêmios de dinheiro ou outro valor.  
*   Sua extensão não deve fornecer acesso não autorizado ao conteúdo do site, por exemplo, contornando as restrições de pagamento ou logon.  
*   Sua extensão não deve fornecer, incentivar ou habilitar o acesso não autorizado, download ou streaming de conteúdo ou mídia protegido por direitos autorais.  
*   Sua extensão não deve minar a criptografia.  
    
###  <a name="2.9-illegal-activity"></a>Atividade ilegal 2.9  

Sua extensão não deve conter conteúdo ou funcionalidade que incentive, facilite ou envidraça atividades ilegais no mundo real.  

###  <a name="2.10-excessive-profanity-and-inappropriate-content"></a>2.10 Excesso de profanidade e conteúdo inadequado  

*   Sua extensão não deve conter profanidade excessiva ou gratuita.  
*   Sua extensão não deve conter ou exibir conteúdo que uma pessoa razoável considere obscena.  
    
###  <a name="2.11-country/region-specific-requirements"></a>2.11 Requisitos específicos de país/região  

O conteúdo ofensivo em qualquer país/região ao qual sua extensão é direcionada não é permitido.  O conteúdo pode ser considerado ofensivo em determinados países/regiões devido a leis locais ou normas culturais.  Exemplos de conteúdo potencialmente ofensivo em determinados países/regiões incluem o seguinte:  

**China**  

*   Conteúdo sexual proibido  
*   Referências de território ou região disputadas  
*   Fornecendo ou habilitando o acesso a conteúdo ou serviços ilegais sob a lei local aplicável  
    
###  <a name="2.12-age-ratings"></a>Classificações etárias de 2,12  

#### 2.12.1 Conteúdo maduro  

Ao enviar sua extensão para [o Partner Center,][MicrosoftPartnerCenter]você deve indicar se sua extensão exibe conteúdo que deve ser marcado como "Maduro".  Ao determinar a classificação para sua extensão, considere todo o conteúdo em seu aplicativo, incluindo conteúdo gerado pelo usuário e anúncios e o conteúdo que sua extensão vincula.  Se você indicar que sua extensão não contém conteúdo "Maduro", será responsável por manter a precisão dessa classificação.  Independentemente da classificação dada à sua extensão, ela ainda deve seguir todos os requisitos de conteúdo das políticas de desenvolvedor de complementos Microsoft Edge complementos  

#### 2.12.2 Alteração de classificações  

Se sua extensão fornece conteúdo \(como gerado pelo usuário, varejo ou outro conteúdo baseado na Web\) que pode ser apropriado para uma classificação etária maior do que a classificação atribuída, você deve exigir que os usuários optem por receber esse conteúdo usando um filtro de conteúdo ou entrando com uma conta pré-existente.  

###  <a name="2.13-videos"></a>2.13 Vídeos  

Se você enviar um vídeo promocional na listagem, ele deverá seguir todas as diretrizes de conteúdo mencionadas nesta política.  Se você optar por fornecer um link do YouTube, verifique se os anúncios estão desabilitados para os vídeos específicos que você deseja inserir.  Para obter mais informações sobre como os anúncios são habilitados e desabilitados no YouTube, consulte [support.google.com/youtube/answer/2531367?ref_topic=7072227][GoogleYoutubeAnswer2531367Topic7072227] e [support.google.com/youtube/answer/132596][GoogleYoutubeAnswer132596].  

<!-- links -->  

[MicrosoftEdgeContentSecurityPolicyRemoteScript]: ./csp.md#relaxing-the-default-policy "Descontrair a política padrão - Política de Segurança de Conteúdo \(CSP\) | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de Desenvolvedor de Aplicativos | Microsoft Docs"  
[MicrosoftIdentifiesMalwareUnwantedApplications]: /windows/security/threat-protection/intelligence/criteria "Como a Microsoft identifica malware e aplicativos potencialmente indesejados | Microsoft Docs"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Definir seus formatos de ad padrão - Ajuda do YouTube"  
[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anúncios em vídeos incorporados - Ajuda do YouTube"  
[FTCChildrensPrivacy]: https://www.ftc.gov/tips-advice/business-center/privacy-and-security/children%27s-privacy "Privacidade de Crianças - Comissão Federal do Comércio"  

[MicrosoftAdvertisingCreativeAcceptancePolicies]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-acceptance-policies "Políticas de aceitação criativas - Microsoft Advertising"  
[MicrosoftAdvertisingCreativeSpecifications]: https://about.ads.microsoft.com/solutions/ad-products/display-advertising/creative-specs "Especificações Criativas - Microsoft Advertising"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
