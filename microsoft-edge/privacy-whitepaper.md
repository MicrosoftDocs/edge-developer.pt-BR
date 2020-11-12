---
description: White paper de Privacidade do Microsoft Edge
title: White paper de Privacidade do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, privacidade, white paper, confiança
ms.localizationpriority: high
no-loc:
- Cast
- Google Cast
ms.openlocfilehash: ad65877818e8baf47f2a86be4bc4c3cc03d7b7ed
ms.sourcegitcommit: de29787c02c35084985cc3d4df97a9b12f004971
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163266"
---
# White paper de Privacidade do Microsoft Edge  

A nossa promessa de privacidade do navegador é fornecer a você a proteção, transparência, controle e respeito que merece.  Para manter o compromisso de dar transparência aos produtos Microsoft, a equipe do Microsoft Edge forneceu um white paper sobre privacidade explicando como os recursos e serviços do Microsoft Edge funcionam e como cada um pode afetar sua privacidade.  A meta da equipe do Microsoft Edge é fornecer um entendimento completo de como seus dados são usados, como controlar os diferentes recursos e como gerenciar os dados coletados, para que você tenha as informações necessárias para tomar as devidas decisões de privacidade.  

Em determinadas seções do papel, o Microsoft Team fornece as etapas para acessar as configurações do Microsoft Edge e outras páginas.  Para manter a consistência, a equipe do Microsoft Edge usou um formato reduzido em todo o white paper:  Você deve ver URLs que começam `edge://` como `edge://favorites` ou `edge://settings/privacy`.  Para ir até às páginas, digite o texto em negrito diretamente na barra de endereço do Microsoft Edge.  As páginas só estão visíveis no Microsoft Edge.  

O white paper foca na versão de área de trabalho do Microsoft Edge, e partes do documento podem incluir recursos ou experiências que não estão disponíveis a todos os usuários.  Além disso, o white paper aborda os recursos e serviços existentes no produto hoje, mas que podem estar sujeitos a alterações futuras.  A Microsoft pratica a minimização da coleta de dados, o que significa que seus dados são mantidos pelo período mínimo de tempo, mas o tempo de retenção pode variar dependendo do recurso ou serviço usado, e isso pode mudar com o tempo.  

## Barra de endereços e sugestões  

A barra de endereços permite inserir URLs de site e pesquisar na Web.  Por padrão, a barra de endereços fornece sugestões de pesquisa e de sites usando os caracteres digitados.  Você deve ver sugestões dos seus favoritos, do histórico de navegação, de pesquisas anteriores e do provedor de pesquisa padrão.  

:::image type="complex" source="./media/whitepaper-media/address-bar.png" alt-text="Barra de endereços" lightbox="./media/whitepaper-media/address-bar.png":::
   Barra de endereços  
:::image-end:::  

Para deixar a navegação e a pesquisa mais rápidas, à medida que você digita na barra de endereços, os caracteres digitados são enviados ao provedor de pesquisa padrão para que ele retorne as consultas de pesquisa sugeridas.  A barra de endereços categoriza a entrada como URL, pesquisa ou desconhecida.  As informações, juntamente com as sugestões selecionadas, a posição da seleção e outros dados da barra de endereços, são enviados ao seu provedor de pesquisa padrão.  Se o seu provedor de pesquisa for o Bing, será enviado um identificador redefinível exclusivo com os dados ao seu navegador para ajudar a entender a consulta e a sessão da pesquisa.  Outros identificadores de serviço de sugestão automática são enviados ao mecanismo de pesquisa padrão para concluir as sugestões de pesquisa.  Seu endereço IP e cookies serão enviados ao provedor de pesquisa padrão para aumentar a relevância dos resultados da pesquisa.  Um sinal será enviado ao provedor de pesquisa padrão ao selecionar a barra de endereços para sinalizar ao provedor e se preparar para fornecer sugestões.  Os caracteres digitados e as consultas de pesquisa não serão enviados à Microsoft, a menos que seu provedor de pesquisa seja o Bing.  Para habilitar o envio de dados ao seu provedor de pesquisa padrão, vá para `edge://settings/privacy` e em **Serviços**, selecione **Barra de endereços** e ative a configuração **Mostrar sugestões de pesquisa e de sites usando meus de caracteres digitados**.  Se você desativar a configuração, os caracteres digitados não serão mais enviados ao provedor de pesquisa padrão.  As consultas de pesquisa ainda serão enviadas ao provedor de pesquisa padrão para fornecer resultados de pesquisa.  Se o Microsoft Edge detectar alguma digitação na barra de endereços que possa conter informações confidenciais, como credenciais de autenticação, nomes de arquivos locais ou dados de URL normalmente criptografados, o texto digitado não será enviado..  Se você quiser que o Microsoft Edge colete dados de diagnóstico sobre a barra de endereços, incluindo o número de consultas oferecidas para todos os provedores de pesquisa, vá para `edge://settings/privacy` e, em **Personalizar sua experiência na web**, ative a opção**Melhorar sua experiência na web permitindo que a Microsoft use o histórico de navegação desta conta para personalizar anúncios, pesquisas, notícias e outras configurações de serviços Microsoft**.  

Os pressionamentos de teclas e os sites que você visita são armazenados localmente no dispositivo por perfil.  Para excluir os dados, vá para `edge://settings/clearBrowserData` e, na janela **Limpar dados de navegação**, marque a caixa de seleção **Histórico de navegação** e selecione o botão **Limpar agora**.  Se o Bing for seu provedor de pesquisa padrão e você estiver conectado ao Bing, será possível excluir suas pesquisas no [painel de Privacidade da Microsoft][MicrosoftAccountPrivacy].  Para limpar seu histórico de navegação e excluir a exibição de sites como sugestões na barra de endereços, vá para `edge://history` e selecione **Limpar dados de navegação**.  Para limpar os dados que a Microsoft coleta da barra de endereços e pesquisar os recursos de sugestões no Windows 10, abra **Iniciar** > **Configurações** > **Privacidade** > ** Diagnóstico e comentários** e, em **Excluir dados de diagnóstico**, selecione **Excluir**.  Todos os outros dados serão excluídos após 36 meses.  

Se você estiver conectado ao Microsoft Edge com uma conta corporativa ou de estudante da Microsoft, e a Pesquisa da Microsoft estiver disponível, um token anônimo representando sua conta será enviado com a consulta para fornecer a funcionalidade específica da conta, como os resultados específicos para sua empresa.  

Todos os dados são transmitidos de forma segura por HTTPS.  Se o [Bing][|::ref1::|Main] for seu provedor de busca padrão, as buscas e caracteres digitados são salvos por até seis meses.  

Se você procurar por uma única palavra na caixa de endereços, o Microsoft Edge poderá enviar essa única palavra ao servidor DNS para verificar se ela corresponde a um host da sua rede e tentará se conectar ao host correspondente.  A opção permite que você navegue até o host específico em vez de procurar.  Por exemplo, se o seu roteador usa o nome de host `router` e você digita `router` na barra de endereços, você terá a opção de navegar até `https://router`, bem como pesquisar a palavra `router` com o provedor de pesquisa padrão.  O recurso não é controlado pela configuração **Mostrar sugestões de pesquisa e de sites usando meus caracteres digitados**, já que ele não envolve o envio de dados ao mecanismo de pesquisa padrão.  

Outra maneira de habilitar \(ou desabilitar\) o envio de dados ao provedor de pesquisa padrão, vá para `edge://settings/search` e ative \(ou desative\) a configuração **Mostrar sugestões de pesquisa e de sites usando meus de caracteres digitados**.  Para alterar seu mecanismo de pesquisa padrão, vá para `edge://settings/search` e selecione o menu suspenso **Mecanismo de pesquisa usado na barra de endereços**.  Se você estiver navegando enquanto usa o modo Convidado ou o InPrivate, suas sugestões automáticas serão desativadas.  O InPrivate mostra sugestões da navegação local, como histórico de navegação ou pesquisas anteriores, mas nenhum caractere digitado é enviado ao mecanismo de pesquisa padrão.  O modo Convidado não exibe sugestões ou envia caracteres digitados ao mecanismo de pesquisa padrão.  

Os dados coletados por outros provedores de pesquisa seguem a política de privacidade da empresa.  

## Preenchimento automático  

O preenchimento automático no Microsoft Edge ajuda você a ser mais produtivo, permitindo que você salve senhas, informações de pagamento, endereços e outros dados de entrada de formulários, por exemplo, aniversários.  Quando você visita um site e começa a preencher um formulário, o Microsoft Edge usa as informações de preenchimento de formulário para corresponder os dados de preenchimento automático salvos ao formulário.  O Microsoft Edge oferece dados de entrada de formulário salvos anteriormente quando você encontra formulários semelhantes.  Informações de cartão de crédito e senhas são salvas apenas com sua permissão explícita para cada senha e cartão.  

Endereços e outras entradas de formulário são salvos por padrão.  Para desativar salvar e preencher automaticamente o endereço e outros dados do formulário, vá para `edge://settings/addresses` e desligue a configuração **Salvar e preencher endereços**.  

Para impedir que o Microsoft Edge solicite que você salve as senhas, vá para `edge://settings/passwords` e desative a configuração **Oferecer para salvar senhas**.  Se você não quiser que o Microsoft Edge preencha automaticamente as senhas salvas existentes e quiser apagar suas senhas salvas, vá para `edge://settings/passwords` e selecione **Senhas salvas**.  Para excluir todos os dados de preenchimento automático, vá para `edge://settings/clearBrowserData`, selecione **Dados de formulário de preenchimento automático**, selecione o intervalo de tempo desejado e, em seguida, selecione **Limpar agora**.  

Se você ativou a sincronização para o seu perfil, seus dados de preenchimento automático serão sincronizados em todas as versões do Microsoft Edge em que você estiver conectado com as mesmas credenciais.  Quando a sincronização estiver ativada, todos os dados de preenchimento automático serão armazenados em servidores da Microsoft criptografados.  Os dados de preenchimento automático armazenados nos servidores da Microsoft são usados somente para fins de sincronização.  Para desativar a sincronização dos seus dados de preenchimento automático, vá para `edge://settings/profiles/sync`, e ao lado do seu Perfil, selecione o botão **Desativar sincronização**.  Se você ativou a sincronização para preenchimento automático, a exclusão de dados de preenchimento automático de um dispositivo enquanto você estiver conectado ao Microsoft Edge removerá os dados de preenchimento automático de todos os outros dispositivos que você estiver conectado usando a mesma conta.  

Quando você visita uma página da Web e envia um formulário, o Microsoft Edge envia ao serviço de preenchimento de formulário da Microsoft informações sobre o formulário, como um hash do nome do host e os tipos de entrada de preenchimento automático \(por exemplo, a caixa 1 está procurando um endereço de email, a caixa 2 está procurando uma senha, e assim por diante\).  Nenhuma informação inserida pelo usuário ou identificadores do usuário são enviadas ao serviço.  As informações ajudam o Microsoft Edge a identificar corretamente os formulários em diferentes páginas da Web.  Os dados são usados para ajudar a corresponder os dados de preenchimento automático salvos ao formulário.  

Quando você usa o modo Convidado, o preenchimento automático não fica disponível e as novas entradas de preenchimento automático não são adicionadas.  Quando você navega no InPrivate, o Microsoft Edge oferece entradas de preenchimento automático, mas sem adicionar novas.  

## Cast  

Cast com o Microsoft Edge você pode exibir sua mídia em outra tela usando Google Cast.  Para acessar o recurso Cast, abra **Configurações e mais (...)** > **Mais ferramentas** e selecione **Cast mídia para dispositivo**.  Cast depende da extensão do Media Router que não está inclusa no Microsoft Edge por padrão.  Ao usar pela primeira vez o Cast, o Microsoft Edge solicitará permissão para instalar a extensão do Media Router.  

Selecione **reiniciar** para instalar as extensões do Media Router da Chrome Web Store.  Para manter a extensão do Media Router atualizada, na inicialização do Microsoft Edge e a intervalos regulares, o Microsoft Edge envia solicitações de atualização para a Chrome Web Store com os dados básicos da sua versão do Microsoft Edge.  O Google pode coletar alguns dados associados à extensão do Media Router.  Para desinstalar a extensão do Media Router, vá para `edge://flags` e desabilite o **Edge-On-Demand-Media-Router**.  Isso também interrompe as atualizações da Chrome Web Store.  A extensão ficará oculta e não aparecerá na lista de **extensões instaladas**.  Para a lista de **extensões instaladas**, vá para `edge://extensions`.  

## Coleções  

Você pode coletar sites, textos e imagens na Web, e organizar o conteúdo com Coleções no Microsoft Edge.  Todos os dados de coleções são armazenados localmente no dispositivo e organizados por perfil do Microsoft Edge.  Se a sincronização estiver ativada para Coleções, as coleções criadas, incluindo anotações ou comentários, estarão disponíveis em todas as versões conectadas e sincronizadas do Microsoft Edge.  

A cada 24 horas o Microsoft Edge baixa uma lista de sites suportados para os quais existem modelos de extração de entidades especiais.  Os modelos são específicos para cada site.  Ao criar um novo item em sua coleção, o Microsoft Edge verifica se o site no qual você está criando o novo item de coleção está na lista de sites com suporte.  Se o site estiver na lista, o Microsoft Edge executará ping no serviço de extração de entidade para o modelo do site específico.  Nenhum identificador de usuário está associado à solicitação para o serviço.  O modelo tenta identificar o nome, o preço, as classificações, a imagem principal e outros dados sobre o item que está sendo coletado.  Se o site onde você está criando um novo item de coleção não estiver no site de lista com suporte, o Microsoft Edge não baixará um modelo.  Os modelos permitem a criação de todos os itens da coleção localmente no dispositivo.  Nenhum dado sobre os itens da coleção é enviado ao serviço para criar a coleção.  

Para excluir os modelos armazenados no dispositivo e limpar os dados em cache, vá para `edge://settings/privacy` e em **Limpar dados de navegação** ao lado de **Limpar dados de navegação agora**, selecione o botão **Escolher o que limpar**, selecione o intervalo de tempo e o tipo de dados desejados e, em seguida, selecione o botão **Limpar agora**.  Outra maneira de excluir dados em cache, vá para `edge://settings/clearBrowserData`, selecione o intervalo de tempo e o tipo de dados desejados e, em seguida, selecione o botão **Limpar agora**.  

Para ativar a configuração **Mostrar sugestões do Pinterest em Coleções**, se você quiser ver, Coleções realiza uma busca no Microsoft Bing usando o título de sua coleção para encontrar páginas de Tópicos de Interesse relevantes.  O Microsoft Edge não envia dados sobre suas coleções para a Pinterest.  Para remover as sugestões e interromper as pesquisas nas páginas de Tópicos do Pinterest, vá para `edge://settings/privacy` e desative a configuração **Mostrar sugestões do Pinterest em Coleções**.  

Coleções não está disponível ao usar a navegação InPrivate ou no modo Convidado.  

## Falhas  

Se os dados de diagnóstico opcionais, incluindo relatórios de falhas, estiverem ativados, a Microsoft coletará dados de diagnóstico quando o Microsoft Edge falhar ou encontrar outros problemas de confiabilidade.  Os dados de diagnóstico são usados para diagnosticar e corrigir problemas de confiabilidade do Microsoft Edge e de outros produtos e serviços da Microsoft.  

:::image type="complex" source="./media/whitepaper-media/crashes2.png" alt-text="Falhas" lightbox="./media/whitepaper-media/crashes2.png":::
   Falhas  
:::image-end:::  

Os dados de diagnóstico coletados estão na forma de despejos de memória, que contêm o estado do dispositivo e do software capturado no momento em que o Microsoft Edge encontrou o problema de confiabilidade.  O despejo de memória contém informações sobre o que estava acontecendo no momento do problema de confiabilidade.  Informações como o site que você estava visitando no momento da falha ou o uso da CPU podem ser incluídos nos dados de diagnóstico.  Os dados de diagnóstico de falha são armazenados localmente no dispositivo e enviados à Microsoft usando um link criptografado quando o relatório de falha estiver ativado.  Cada despejo de memória contém um identificador exclusivo para o seu dispositivo, um identificador redefinível exclusivo para o seu navegador e dados de diagnóstico adicionais (como a URL, o uso da CPU e o uso da rede\) para ajudar a identificar o problema.  Os dados adicionais de diagnóstico são anexados ao despejo de memória para ajudar a diagnosticar o problema de confiabilidade, como saber quantos dispositivos estão tendo problemas e a gravidade.  

Os despejos de memória são enviados à Microsoft e armazenados em seus servidores seguros por até 30 dias e, em seguida, excluídos.  Para solicitar que os dados de diagnóstico nos dispositivos Windows 10 seja excluídos, abra **Iniciar** > **Configurações** > **Privacidade** > **Diagnóstico e comentários** e em **Excluir dados de diagnóstico** selecione **Excluir**.  Informações de falha agregadas, como uma contagem dos tipos de falhas ocorrendo, são armazenadas para fins de relatório e de melhoria do produto.  

Para limpar os dados de diagnóstico de falha armazenados localmente no sistema de arquivos do dispositivo, vá para `edge://crashes` e selecione o botão **Limpar tudo**.  

Para desativar a coleta de dados de diagnóstico de falha no Windows 10, abra **Iniciar** > **Configurações** > **Privacidade** e selecione **Diagnóstico e comentários**.  Para versões do Microsoft Edge em todas as outras plataformas, vá para `edge://settings/privacy` e desative a configuração **Ajude a melhorar os produtos da Microsoft enviando dados opcionais sobre como você usa o navegador, websites que visita e relatórios de falha**.  O recurso de coleta de dados de diagnóstico também pode ser desativado para empresas por meio das [políticas de grupo gerenciadas pela sua organização][DeployedgeEnterprisePrivacySettings].  

## Ferramentas de desenvolvedor

As Ferramentas de desenvolvedor do Microsoft Edge fornecem ferramentas para depuração e testes de site. Para acessar as Ferramentas de desenvolvedor, abra **Configurações e mais (...)** > **Mais ferramentas** e selecione **Ferramentas de desenvolvedor**.  Quando você ativa determinados recursos em Ferramentas de Desenvolvimento, o Microsoft Edge solicita módulos dos servidores da Microsoft e os baixa em seu dispositivo.  A solicitação dos módulos enviados é feita por uma conexão HTTPS segura e contém um identificador não exclusivo que representa a versão do Microsoft Edge que está sendo usada.  As experiências específicas que exigem o download remoto incluem a Modo de exibição 3D e o painel Acessibilidade da ferramenta Elementos.  A integração do Webhint requer um módulo remoto que é solicitado automaticamente quando as Ferramentas de desenvolvedor são abertas.  

## Dados de diagnóstico

A Microsoft usa dados de diagnóstico para melhorar nossos produtos e serviços, mantendo nossos produtos seguros, atualizados e executando conforme o esperado. Sempre que coletamos dados, queremos verificar se é a escolha certa para você. A Microsoft acredita e pratica a minimização da coleta de informações. Estamos nos esforçando para coletar somente as informações de que precisamos e armazená-las enquanto são necessárias para fornecer um serviço ou para análise. 

O Microsoft Edge coleta um conjunto de dados de diagnóstico que são necessários para manter o produto seguro, atualizado e funcionando corretamente. Os dados de diagnóstico necessários incluem dados como conectividade do dispositivo, informações de configuração, configuração de software e inventário. A Microsoft usa os dados de diagnóstico necessários para solucionar problemas e manter os produtos e serviços da Microsoft confiáveis, seguros e funcionando normalmente. Para obter mais informações sobre os dados de diagnóstico em dispositivos gerenciados, confira [Configurar os dados de diagnóstico do Windows na sua organização][WindowsPrivacyConfigureDiagnosticDataOrganization] e [Política de grupo de dados de diagnóstico Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-enterprise-privacy-settings). 

:::image type="complex" source="./media/whitepaper-media/diagnostic-data2.png" alt-text="Dados de diagnóstico" lightbox="./media/whitepaper-media/diagnostic-data2.png":::
   Dados de diagnóstico  
:::image-end:::  

Além disso, você pode optar por compartilhar dados de diagnóstico opcionais. À medida que você usa os recursos e serviços do Microsoft Edge e outros aplicativos que usam a plataforma web do Microsoft Edge, os dados de diagnóstico sobre como você usa esses recursos são enviados à Microsoft. Com sua permissão, os dados de diagnóstico opcionais são enviados à Microsoft para melhorar os produtos e serviços Microsoft para todos. Estes dados não são coletados ou armazenados com a sua conta Microsoft.  

Os dados de diagnóstico opcionais incluem informações como o uso de recursos, dados de desempenho, tempos de carga do site, uso de memória e sites que você visita. Por exemplo, se você selecionar um site como favorito, os dados de diagnóstico opcionais incluirão informações de que o botão favorito foi selecionado e um favorito foi adicionado com êxito, mas não qual site foi definido como um favorito.  

O envio de informações sobre sites que você visita no Microsoft Edge ajuda a Microsoft a entender a rapidez com que os sites são carregados, e aumenta a relevância dos resultados da pesquisa. Os dados de diagnóstico incluem informações sobre o website, tais como a URL da página que você visita, métricas do site, título da página, como você acessou a página, informações sobre o conteúdo da página e outras informações relevantes sobre a navegação de página.  

Os dados de diagnóstico são enviados através de HTTPS e armazenados nos servidores da Microsoft. Em dispositivos Windows, os dados de diagnóstico são enviados com um identificador exclusivo para o seu dispositivo. Em outros dispositivos, os dados de diagnóstico são associados a um identificador resettable exclusivo para seu navegador, que é gerado aleatoriamente e não contém suas informações pessoais.  

A equipe do Microsoft Edge respeita a confidencialidade dos dados de diagnóstico, restringindo o acesso aos dados ou removendo informações de identificação pessoal. Para redefinir o identificador exclusivo do seu navegador em dispositivos Windows 10, vá para **Iniciar** > **Configurações** > **Privacidade** > ** Diagnóstico e comentários** e em **Excluir dados de diagnóstico**, selecione **Excluir** ou altere a sua configuração em **Dados de diagnóstico** de **Completo** para **Básico** ou desative **Dados de diagnóstico opcionais**.  

Em outras plataformas, para gerar um novo identificador resettable \(ID\) exclusivo do seu navegador, vá para `edge://settings/privacy` e desative a configuração **Ajude a melhorar os produtos da Microsoft enviando dados de diagnóstico opcionais sobre como você usa o navegador, websites que visita e relatórios de falha**. A funcionalidade redefinir \(ID\) pode ser diferente para dispositivos gerenciados com políticas de grupo definidas pela sua organização. 

Se você estiver usando o Windows 10 versão 1803 (atualização de abril de 2018) ou posterior, para visualizar os dados do produto compartilhados com a Microsoft no Visualizador de Dados de Diagnóstico, vá para **Iniciar** > **Configurações** > **Privacidade** > **Diagnósticos e comentários** e, em **Exibir Dados de Diagnóstico**, selecione **Abrir o Visualizador de Dados de Diagnóstico**. 

Para outras plataformas ou versões do Windows 10 versão 1803 e anteriores, para visualizar os dados de diagnóstico, vá para `edge://data-viewer`. Para visualizar os dados enviados periodicamente à Microsoft desde a última vez em que o visualizador foi aberto, vá para `edge://data-viewer`. Para ver quais dados foram enviados à Microsoft para a sua sessão específica, atualize o visualizador. Os dados usados para preencher `edge://data-viewer` são armazenados localmente no dispositivo. Para apagar os dados no visualizador, feche a guia `edge://data-viewer`. 

Para nos ajudar a melhorar os produtos e serviços Microsoft, os dados de diagnóstico desidentificados e agregados ficam armazenados por até dois anos. Como os dados de diagnóstico não são coletados ou armazenados com a conta Microsoft, os dados de diagnóstico não podem ser exibidos ou excluídos do [painel de privacidade da Microsoft][MicrosoftAccountPrivacy]. Para excluir os dados de diagnóstico no Windows 10, vá para **Iniciar** > **Configurações** > **Privacidade** > **Diagnóstico e comentários** e em **Excluir dados de diagnóstico** selecione **Excluir**. A funcionalidade excluir dados de diagnóstico só tem suporte no Windows 10 versão 1803 ou posterior. Para obter mais informações, confira [Diagnóstico, comentários e privacidade no Windows 10][MicrosoftSupport4468236]. 

Para o Microsoft Edge no Windows 10, a configuração é determinada pela sua configuração de dados de diagnóstico do Windows. A configuração se reflete em `edge://settings/privacy`. Altere as configurações do Windows em **Iniciar** > **Configurações** > **Privacidade** > **Diagnóstico e comentários**. Em todas as outras plataformas, para controlar o conjunto de dados de diagnóstico, vá para `edge://settings/privacy` e ative ou desative **Ajudar a melhorar os produtos Microsoft enviando dados de diagnóstico opcionais sobre como você usa o navegador, os sites que visita e os relatórios de falha**. A configuração é usada para todos os perfis associados à instalação do Microsoft Edge no seu dispositivo.  A configuração não é sincronizada entre dispositivos. A configuração se aplica à navegação InPrivate e ao modo Convidado. As informações sobre sites que você visita nunca são enviadas durante a navegação InPrivate ou no modo Convidado. Se o seu dispositivo for gerenciado com políticas de grupo definidas pela sua organização, isso será refletido em `edge://settings/privacy`.  

## Gerenciamento de Direitos Digitais e Licenças de Mídia  

Quando um site oferece conteúdo de mídia protegido pelo DRM (Gerenciamento de Direitos Digitais), o Microsoft Edge usa um pipeline de reprodução seguro para garantir que o conteúdo não seja copiado ou acessado incorretamente.  Como parte do recurso, o Microsoft Edge pode armazenar dados relacionados ao DRM no seu dispositivo, incluindo um identificador exclusivo e licenças de mídia, e pode transmitir o identificador exclusivo para um servidor de licenciamento de mídia especificado pelo provedor de conteúdo.  Quando você usa o site, o Microsoft Edge recupera as informações do DRM para garantir que você tenha permissão para usar o conteúdo.  Os dados ajudam a validar o acesso ao conteúdo protegido e a garantir uma experiência de mídia perfeita.  

O Microsoft Edge oferece suporte ao DRM usando a API de Extensões de Mídia Criptografada \(EME API\) para sites HTML5.  A EME API permite que os sites se comuniquem com um provedor do DRM chamado de Módulo de Descriptografia de Conteúdo \(CDM\).  Sistemas DRM diferentes, como o Widevine do Google ou o PlayReady da Microsoft, podem ser compatíveis com a implementação do CDM do desenvolvedor.  Os provedores de conteúdo podem optar por oferecer suporte a um ou mais sistemas DRM potenciais, e podem utilizar a funcionalidade da EME API para decidir qual sistema DRM usar para um cliente específico.  Para obter mais informações sobre privacidade da EME, confira [Privacidade de Extensões de Mídia Criptografada][W3cEncryptedMediaPrivacy].  

O Microsoft Edge é compatível com o DRM do PlayReady somente no Windows 10.  O PlayReady é uma implementação de DRM que oferece experiências de mídia, como vídeo 4K e áudio Dolby Atmos.  O Microsoft Edge usa as APIs do Windows Platform Media Foundation para dar suporte ao PlayReady.  Para validar o acesso ao conteúdo protegido, o Microsoft Edge usa o sistema operacional Windows 10, que usa um identificador exclusivo \(ID\) e comunica a ID com o serviço do PlayReady.  Todos os dados de EME, CDM e navegador do PlayReady que persistem no dispositivo são armazenados e mantidos no Microsoft Edge.  Para mais informações sobre o PlayReady, confira [Sistema Simples de Ponta a Ponta][PlayreadyOverviewSimpleEndSystem].  

O Microsoft Edge oferece suporte ao Widevine do DRM do Google e a opção está ativada por padrão.  O Microsoft Edge busca periodicamente atualizações para o Widevine nos servidores do Google.  O uso do Widevine pode incluir comunicações com o Google.  Para optar por não usar o Widevine no Microsoft Edge, vá para `edge://flags/#edge-widevine-drm` e desative a configuração do DRM do Widevine.  O Widevine tem a capacidade de criar um identificador de dispositivo exclusivo e transmiti-lo ao Google.  Para obter informações mais específicas sobre o Widevine e privacidade, confira a política de privacidade do Google.  

O Microsoft Edge é compatível com o DRM do Flash Access do Adobe, usado por alguns sites em vez do HTML5.  Você deve conceder permissão de uso do Adobe Flash quando um site solicitar.  Quando um site usa o DRM do Flash Access do Adobe, o Microsoft Edge concede ao Adobe acesso a um identificador de dispositivo exclusivo.  Para limpar e redefinir todas as instâncias armazenadas localmente do identificador, vá para `edge://settings/privacy` e em **Limpar dados de navegação**, selecione **Escolher o que limpar**, marque a caixa de seleção **Cookies e outros dados do site** e selecione **Limpar agora** para remover todos os identificadores armazenados.  Para interromper o uso do DRM do Adobe Flash, vá para `edge://settings/content/flash`.  

Quando você solicita acesso à mídia HTML5 criptografada como um filme online, o Microsoft Edge cria uma solicitação de licença para descriptografar a mídia.  O CDM que está sendo usado cria a solicitação de licença que contém uma ID da solicitação.  A solicitação é enviada ao servidor de licença.  Nenhuma parte da solicitação de licença contém informações de identificação pessoal, e a solicitação de licença não é armazenada no dispositivo.  

Quando a licença de mídia é retornada, um identificador de mídia exclusivo é criado para o usuário e o site.  A ID não é compartilhada entre sites e é diferente para cada site.  Uma ID da sessão, usada para identificar uma sessão de reprodução, é enviada com o identificador de mídia para descriptografar mídia.  O identificador de mídia é armazenado localmente no dispositivo e pode ser armazenado com o provedor de conteúdo.  

Para desabilitar todas as proteções de DRM e de conteúdo, vá para `edge://settings/content/protectedContent` e desative as configurações **Permitir que sites reproduzam conteúdo protegido (recomendado)** e **Permitir identificadores de conteúdo protegido (pode ser necessário reiniciar o computador)**.  

*   Desativar a configuração **Permitir que sites reproduzam conteúdo protegido** desabilita a reprodução de sistemas de DRM baseados em CDM, como o PlayReady e o Widevine, mas não para sistemas não baseados em CDM, como o DRM do Flash Access.  Para gerenciar as permissões de site do Flash, vá para `edge://settings/content/flash`.  Desativar a configuração faz com que a funcionalidade da mídia pare de funcionar corretamente.  
*   Desativar a configuração **Permitir identificadores para conteúdo protegido** impede a criação de identificadores para o DRM do Flash Access e impede que o Widevine busque atualizações no Google periodicamente.  Desativar a configuração pode fazer com que algumas funcionalidades de mídia parem de funcionar corretamente em alguns sites.  

## Não Rastrear  

Para habilitar o recurso **Não Rastrear** no Microsoft Edge, vá para `edge://settings/privacy` e ative a configuração **Enviar solicitações de "Não Rastrear"**.  Se você habilitar o recurso **Não Rastrear**, o Microsoft Edge enviará um cabeçalho DNT:1 HTTP com as solicitações de tráfego de navegação HTTP, HTTPS e SPDY de saída para os sites que você visita, solicitando que não usem rastreadores.  No entanto, ao habilitar a configuração **Enviar solicitações de "Não Rastrear"** não garante que os sites não consigam rastrear você.  Alguns sites podem atender à solicitação, mostrando anúncios que não se baseiam em nenhuma navegação anterior.  O Microsoft Edge não controla se a solicitação será atendida ou não.  Para ajudar a impedir que os sites o rastreiem, vá para `edge://settings/privacy` e altere a configuração **Prevenção de rastreamento** para **Equilibrado** ou **Estrito**.  

Quando você usa o modo Convidado, o Microsoft Edge não envia solicitações de **Não Rastrear**.  Quando você usa a navegação InPrivate, o Microsoft Edge envia apenas solicitações de **Não Rastrear** se a configuração **Enviar solicitações de "Não Rastrear"** estiver ativada no perfil que você está usando.  

## Downloads  

O Microsoft Edge permite que você baixe arquivos com segurança.  Para escolher onde os arquivos são baixados no seu dispositivo, vá para `edge://settings/downloads`.  Se o SmartScreen estiver habilitado, as informações sobre o arquivo, como o nome e a URL do arquivo, serão enviadas ao SmartScreen para verificar a reputação do arquivo.  A verificação de reputação ajuda a evitar que você baixe acidentalmente algum malware conhecido por causar dano à dispositivos.  Para ligar \(ou desligar) o SmartScreen, vá para `edge://settings/privacy` e ligue \(ou desligue\) o SmartScreen.  Para mais informações sobre o SmartScreen, confira a seção [SmartScreen](#smartscreen).  

Para ver o histórico de seus downloads anteriores, vá para `edge://downloads`.  Para apagar seus dados de navegação e apagar seu histórico de downloads, vá para `edge://settings/clearBrowserData`.  A eliminação do histórico de downloads no Microsoft Edge não remove os arquivos do seu dispositivo.  Excluir os arquivos baixados do dispositivo não os remove do histórico de downloads.  Quando você usa a navegação InPrivate ou o modo Convidado, o histórico de downloads da sessão é limpo ao fechar as janelas InPrivate ou de Convidado, mas os arquivos ficam salvos no dispositivo.  

## Extensões e Complementos do Microsoft Edge  

Você pode instalar extensões no Microsoft Edge para adicionar funcionalidades ao navegador.  Ao instalar uma extensão do site de Complementos do Microsoft Edge ou de outro armazenamento de extensões, a Microsoft coleta informações sobre a extensão para ajudar os desenvolvedores e a Microsoft a entender como a extensão é usada.  O Microsoft Edge coleta dados agregados, incluindo o número de vezes que uma extensão foi baixada e informações sobre o seu desempenho, por exemplo, dados de falhas.  A Microsoft compartilha os dados agregados com os desenvolvedores da extensão.  Os comentários e as avaliações dos usuários são públicos no site de Complementos e também são compartilhados com os desenvolvedores. Se você estiver conectado ao Microsoft Edge, as extensões instaladas no site de Complementos do Microsoft Edge serão associadas à sua conta para fornecer recomendações de extensão.  Os dados são usados agregados para ajudar a entender a popularidade das extensões.   

Se você quiser que suas extensões e preferências sejam sincronizadas em todas as versões sincronizadas do Microsoft Edge conectadas, vá para `edge://settings/profiles/sync` e selecione o botão **ativar sincronização**.   

A instalação de extensões é opcional e, para desinstalar as extensões a qualquer momento, vá para `edge://extensions`.  Quando uma extensão é instalada, ela especifica quais dados de usuário ela precisa ter acesso, e o Microsoft Edge solicita permissão antes de instalar a extensão.  Sempre verifique se uma extensão é confiável e segura antes de instalá-la, e analise a política de privacidade do desenvolvedor para a extensão específica.  

As extensões são atualizadas através do serviço de atualização do Microsoft Edge.  O Microsoft Edge envia uma lista de extensões instaladas ao serviço de atualização para verificar se há atualizações disponíveis.  Se você instalar uma extensão da Chrome Web Store, as solicitações serão enviadas à Chrome Web Store em intervalos regulares para verificar se há atualizações de extensão.  O identificador da extensão, a versão da extensão e as informações sobre o Microsoft Edge estão incluídos na solicitação para procurar atualizações.  Para interromper as solicitações da Chrome Web Store, vá para `edge://extensions` e em **De outras fontes**, desinstale as extensões.  

Ao importar extensões de outros navegadores como o Google Chrome, se uma extensão estiver disponível no site de Complementos do Microsoft Edge, o Microsoft Edge instalará automaticamente a extensão do site de Complementos do Microsoft Edge e a ativará se você já tiver a extensão ativada.  Se a extensão não estiver disponível no site de Complementos do Microsoft Edge, o Microsoft Edge copiará e instalará localmente a extensão do Google Chrome sem ativá-la, ou se conectará à Chrome Web Store.  O Microsoft Edge solicitará sua permissão para ativar a extensão e para permitir extensões de outras lojas.  Caso tenha concedido permissão, o Microsoft Edge permitirá a instalação de extensões de outras lojas e de atualizações para suas extensões usando a Chrome Web Store.  Para habilitar \(ou desabilitar\) a opção, vá para `edge://extensions` e ative \(ou desative\) a configuração **Permitir extensões de outras lojas**.

## Proteção para a família  

A Microsoft oferece várias ferramentas para ajudar as famílias a se conectarem e manterem as crianças mais seguras em dispositivos Windows 10, Xbox e Android executando o Microsoft Launcher.  

Dentro de um grupo de família, há controles de conteúdo que devem ser habilitados para crianças que usam o Microsoft Edge.  O organizador do grupo de família deve habilitar as configurações aos usuários do grupo.  Os três principais recursos oferecidos a um grupo de família são: filtragem da Web, relatórios de atividades e pesquisa segura.  

A filtragem da Web protege as crianças do grupo de família de acessar sites adultos ou sites especificamente bloqueados pelo organizador da família.  

O relatório de atividades registra informações sobre os sites visitados pelas crianças, bem como pesquisas, tempo de tela, dispositivos usados e tentativas de visitar sites bloqueados.  O organizador do grupo de família pode ver as informações em [family.microsoft.com][MicrosoftAccountFamilyMain].  Os dados são coletados, criptografados em trânsito, enviados à Microsoft e armazenados em servidores de armazenamento seguros da Microsoft.  Os dados são coletados com a conta Microsoft da criança, para que sejam gerenciados corretamente.  Os relatórios de atividades são armazenados em [family.microsoft.com][MicrosoftAccountFamilyMain] por até 30 dias e depois excluídos.  

A pesquisa segura adiciona uma palavra-chave segura à solicitação de cabeçalho dos mecanismos de pesquisa.  O Bing lê a palavra-chave segura e filtra os resultados da pesquisa retornados para a criança.  Outros mecanismos de pesquisa podem retornar resultados filtrados devido também à palavra-chave.  Todas as pesquisas da criança são coletadas e disponibilizadas para visualização pelo organizador da família nos relatórios de atividades ou em [family.microsoft.com][MicrosoftAccountFamilyMain].  Os dados são coletados com a conta Microsoft da criança, para que sejam gerenciados corretamente.  

Os dados de navegação da criança são armazenados em servidores seguros da Microsoft e disponibilizados aos pais por até 30 dias e, em seguida, são excluídos imediatamente.  Os dados podem ser excluídos a qualquer momento no [painel de privacidade da Microsoft][MicrosoftAccountPrivacy].  Para limpar os dados de navegação armazenados localmente em um dispositivo, vá para `edge://settings/clearBrowserData`.  

A criança deve estar conectada ao Windows 10 com uma conta Microsoft, e a configuração do relatório de atividades deve ser ativada pelo organizador da família, para permitir a coleta dos dados e o compartilhamento com o organizador do grupo da família.  A criança não precisa estar conectada ao Microsoft Edge para que haja coleta de dados.  Se os recursos de segurança da família não estiverem disponíveis na sua versão do Windows 10, você poderá atualizar para a versão mais recente do Windows para obtê-los.  

O modo Convidado e a navegação InPrivate serão desabilitados se a filtragem da Web ou os relatórios de atividades estiverem ativados.  

O organizador do grupo da família pode interromper a coleta de dados no portal de segurança da família.  Para obter mais informações sobre os recursos de segurança da família da Microsoft, confira [O que é um grupo de família da Microsoft?][MicrosoftSupport12413]  

## Geolocalização  

O Microsoft Edge é compatível com a [API de geolocalização][W3cGeolocationApiMain], que permite que os sites acessem suas informações de localização com a sua permissão.  Os sites podem solicitar sua localização, por exemplo, ao tentar encontrar a cafeteria mais próxima de você.  O Microsoft Edge sempre pede sua permissão antes de conceder a sites acesso à sua localização.  Para gerenciar a permissão ou para sempre impedir que sites acessem sua localização, vá para `edge://settings/content/location`.  

No lado direito da barra de endereços, o Microsoft Edge indica quando a sua localização está ou não sendo compartilhada.  

:::image type="complex" source="./media/whitepaper-media/geolocation2.png" alt-text="Location" lightbox="./media/whitepaper-media/geolocation2.png":::
   Location  
:::image-end:::  

Se você permitir o compartilhamento da sua localização com um site, o Microsoft Edge enviará informações da rede local, como seu endereço IP e pontos de acesso Wi-Fi próximos ao serviço de localização da Microsoft.  O serviço da Microsoft usa as informações para estimar suas coordenadas de geolocalização.  A estimativa de geolocalização é compartilhada com o site com o qual você concordou de compartilhar sua localização.  Para especificar que o Microsoft Edge forneça ao site solicitante uma localização mais precisa no Windows 10, abra **Configurações** > **Privacidade** > **Localização** e ative as configurações **Permitir acesso à localização neste dispositivo** e **Permitir que os aplicativos acessem suas configurações de localização**.  Se você desativar as configurações **Permitir acesso à localização neste dispositivo** e **Permitir que os aplicativos acessem suas configurações de localização**, o Microsoft Edge fornecerá uma localização aproximada ao site solicitante.  As informações só são compartilhadas com um site solicitante, caso você tenha permitido anteriormente ver sua localização.  Para obter mais informações sobre as configurações de localização do Windows, confira [Privacidade e serviço de localização do Windows 10][MicrosoftSupport4468240].  

Uma nova ID gerada aleatoriamente é usada ao fazer solicitações ao serviço de localização do Microsoft Edge.  O serviço de localização do Microsoft Edge não armazena suas coordenadas de geolocalização por nenhum período de tempo.  

A navegação InPrivate usa a configuração de permissão de localização do perfil do qual a sessão InPrivate foi iniciada.  O modo Convidado sempre solicita sua permissão antes de conceder ao site sua localização.  

## Importar dados do navegador  

O Microsoft Edge oferece uma experiência interativa e perfeita ao iniciar o navegador pela primeira vez.  Como parte da experiência, você tem a opção de importar de outro navegador seus dados de navegação ao Microsoft Edge.  Durante a experiência de importação, você pode manter os dados importados ou excluí-los e começar do zero.  Os dados incluem seus favoritos, histórico de navegação, dados de preenchimento automático, extensões, configurações e outros dados de navegação.  Seus dados de navegação de versões mais antigas do Microsoft Edge são importados automaticamente ao atualizar para o novo Microsoft Edge.  Com a sua confirmação, o Microsoft Edge importa dados de navegação de outros navegadores, como o Google Chrome, o Mozilla Firefox ou o Internet Explorer, e o navegador importado é determinado com base no navegador mais usado, conforme definido pelo seu sistema operacional.  A importação de dados é concluída localmente no seu dispositivo, armazenada localmente e não é enviada à Microsoft, a menos que você concorde em sincronizar seus dados de navegação.  

:::image type="complex" source="./media/whitepaper-media/migration.png" alt-text="Import" lightbox="./media/whitepaper-media/migration.png":::
   Import  
:::image-end:::  

Ao importar suas extensões de um navegador diferente, como o Google Chrome, o Microsoft Edge importa uma cópia local e pede permissão antes de ativá-la, se a extensão não estiver disponível no site de Complementos do Microsoft Edge.  As permissões para algumas das extensões podem ter sido alteradas.  Para revisar as permissões de extensão, vá para `edge://extensions`.  

Para importar dados de outro navegador a qualquer momento, vá para `edge://settings/importData`.  

## Instalar e atualizar  

Você pode baixar e instalar o Microsoft Edge em plataformas como o Windows e o macOS.  O Microsoft Edge usa o serviço atualizador para manter sua versão do Microsoft Edge atualizada e segura.  

Quando você baixa e instala o Microsoft Edge, as informações sobre o seu dispositivo, como o canal de versão, as informações básicas de hardware, os identificadores de atualização, um identificador exclusivo para o seu dispositivo e um identificador redefinível exclusivo para o seu navegador são enviados para a Microsoft durante o processo de instalação.  O endereço IP do dispositivo é enviado para o serviço atualizador, mas o último decimal é limpo para obter proteções de privacidade adicionais.  Durante cada sessão de navegação, um novo token gerado aleatoriamente será criado para instalar versões atualizadas do Microsoft Edge.  O token não está associado a nenhuma informação pessoal e é usado somente no processo de instalação e atualização, e para melhorar o serviço atualizador.  

O Microsoft Edge efetua ping no serviço atualizador do Microsoft Edge sobre o andamento da instalação e atualização.  Se uma instalação ou atualização falhar e o relatório de falhas estiver ativado, um log será criado e enviado para a Microsoft.  Para mais informações sobre o envio de relatórios de falhas para a Microsoft, consulte a seção [Falhas](#crashes).  A Microsoft coleta informações sobre como você baixou o Microsoft Edge, o sucesso da instalação e quaisquer desinstalações para entender melhor o sucesso dos downloads do Microsoft Edge.  

As atualizações automáticas são ativadas por padrão para todos os usuários do Microsoft Edge.  Em todas as plataformas, o Microsoft Edge verifica atualizações sobre a inicialização e periodicamente durante a execução.  Nos dispositivos MacOS, o Microsoft AutoUpdate também verifica periodicamente se há atualizações para os produtos Microsoft.  Controles e configurações adicionais estão disponíveis para as organizações.  Para obter mais informações sobre controles e configurações adicionais, confira [Atualizar][DeployedgeUpdatePoliciesUpdate].  

## Modo Internet Explorer  

O Microsoft Edge oferece uma experiência simplificada com a integração do Internet Explorer \(IE\).  O Microsoft Edge é compatível apenas com o IE 11, e o modo do IE está disponível apenas no Windows.  O recurso modo IE está disponível para organizações através de políticas de grupo.  O administrador opta por abrir certos sites no modo IE no Microsoft Edge.  

:::image type="complex" source="./media/whitepaper-media/ie-mode.png" alt-text="Modo IE" lightbox="./media/whitepaper-media/ie-mode.png":::
   Modo do IE  
:::image-end:::  

O Microsoft Edge baixa a lista de sites de um local definido pelo administrador por meio de uma política e armazena em cache o arquivo que determina quais sites devem ser abertos no modo do IE.  Dependendo das configurações do Windows ou do IE 11, o Microsoft Edge coleta dados de diagnóstico sobre o uso do modo do IE, como quais sites os usuários acessam, dados de desempenho, dados de confiabilidade e dados de uso de recursos.  No Windows 10, os dados de diagnóstico são coletados de acordo com a configuração de dados de diagnóstico do Windows.  No Windows 8.1, as informações do site são coletadas se o usuário tiver optado pelo recurso de Virar a Página ou o de Sites Sugeridos no IE.  O modo do IE pode não seguir as mesmas configurações de coleta de dados nas configurações de privacidade do Microsoft Edge.  

Se o seu administrador ativou o Enterprise Site Discovery, os dados do histórico de navegação serão coletados periodicamente para ajudar os administradores a revisar os sites que os usuários visitam e garantir que todas as atualizações do sistema continuem a oferecer suporte a esses sites.  Para obter mais informações sobre o Enterprise Site Discovery no IE11, confira [Coletar dados usando o Enterprise Site Discovery][InternetExplorer11DeployGuideCollectDataEnterpriseSiteDiscovery].  

Usuários não corporativos em dispositivos Windows também podem acessar o modo IE.  Para ligar o modo IE, vá para `edge://settings/defaultBrowser` e selecione a configuração **Permitir que os sites sejam recarregados no modo Internet Explorer**.  Para abrir guias no modo IE, abra **Configurações e mais (...)** > **Mais ferramentas** e selecione **Recarregar no modo Internet Explorer**.  Depois de ligar o modo IE, o Microsoft Edge solicita periodicamente uma lista de sites sem suporte de um serviço da Microsoft.  A solicitação é enviada por HTTPS e não contém identificadores.  

Os dados de navegação do Internet Explorer são armazenados localmente no Microsoft Edge e no Internet Explorer.  Para excluir os dados de navegação enquanto navega no modo IE, vá para `edge://settings/privacy` e limpe os dados em **Limpar dados de navegação** e **Limpar dados de navegação no Internet Explorer**.  


## Anúncios intrusivos  

Para fornecer uma melhor experiência de navegação, o Microsoft Edge oferece o bloqueio do carregamento de anúncios em sites que mostram anúncios intrusivos ou enganosos.  Quando o Ads Blocking está ativado, o Microsoft Edge baixa periodicamente dos servidores da Microsoft a lista mais recente de sites que mostram anúncios intrusivos ou enganosos e os armazena localmente no seu dispositivo.  Nenhum identificador de usuário está incluso na solicitação de download.  Se você visitar um site que está na lista, o Microsoft Edge bloqueará todos os anúncios no site e você deverá ver a mensagem `Ads blocked`.  Para permitir anúncios para o site, vá para `edge://settings/content/ads` e altere as configurações.  Além de baixar a lista de sites com anúncios intrusivos, o recurso Ads Blocking não envia informações adicionais à Microsoft ou solicita informações adicionais da Microsoft enquanto você navega na Web.  

## Lista de atalhos  

A lista de atalhos no Microsoft Edge permite encontrar facilmente os sites fechados mais recentemente, passando o mouse sobre o ícone do Microsoft Edge na barra de tarefas e abrindo um menu contextual \(clique com o botão direito do mouse\).  As três últimas guias fechadas são armazenadas localmente para cada perfil.  Para excluir sites da lista de atalhos no Windows 10, passe o mouse em cada site e abra um menu contextual \(clique com o botão direito do mouse\).  Para desmarcar ou alterar a tela das suas guias recentemente fechadas na lista de atalhos, vá para `edge://settings/privacy` e selecione a configuração **Escolher o que você quer limpar sempre que fechar o navegador**.  Ao usar uma janela InPrivate, o Microsoft Edge não adiciona informações da guia fechada à lista de atalhos.  A lista de atalhos não fica disponível ao usar o modo Convidado.  Para obter mais informações sobre como limpar seus dados de navegação, confira [Exibir e excluir o histórico do navegador no Microsoft Edge][MicrosoftSupport10607].  

## Horário de rede  

O Microsoft Edge usa um serviço de horário de rede da Microsoft para rastrear o horário de uma fonte externa, como um servidor de horário.  Em intervalos aleatórios ou quando o Microsoft Edge encontra um certificado SSL expirado, o Microsoft Edge pode enviar solicitações à Microsoft para obter o horário de uma fonte confiável.  As solicitações ocorrem com mais frequência se o Microsoft Edge detectar que o relógio do sistema está impreciso.  Uma imprecisão do relógio do sistema acontece se o usuário alterar a hora no sistema operacional e isso causar um conflito com o fuso horário correto.  O serviço de horário de rede da Microsoft é usado para obter o Tempo Universal Coordenado \(UTC\).  As solicitações não contêm cookies ou identificadores de usuário, e nenhum dado é registrado.  

## Página de nova guia  

O Microsoft Edge proporciona uma experiência envolvente e centrada no usuário para a página de nova guia com a caixa de pesquisa da plataforma [Bing][|::ref2::|Main], com os blocos de links rápidos para os sites que você visita com mais frequência, além de conteúdo relevante do Microsoft News ou do Office 365.  Personalize a aparência da página de nova guia, selecionando o botão Personalizar.  Suas preferências para a página de nova guia são definidas para cada perfil e armazenadas localmente no seu dispositivo, e as preferências não são sincronizadas entre os dispositivos.

Para melhorar os tempos de carregamento da página da nova guia, a página da nova guia da Microsoft pode ser carregada em segundo plano para acelerar o processo. O conteúdo carregado pode incluir cookies, caso você permita cookies. Para desabilitar o carregamento da página nova guia da Microsoft em segundo plano, vá para `edge://settings/newTabPage` e desabilite a configuração **Pré-carregar a nova guia para obter uma experiência mais rápida**. 

:::image type="complex" source="./media/whitepaper-media/n-t-p1.png" alt-text="Página de nova guia" lightbox="./media/whitepaper-media/n-t-p1.png":::
   Página de nova guia  
:::image-end:::  

### Microsoft News  

Para adaptar o conteúdo às suas interações e preferências, a página de nova guia no Microsoft Edge armazena cookies com identificadores gerados aleatoriamente no dispositivo.  Uma versão limpa do seu endereço IP também é usada para adaptar o conteúdo para sua região geral.  Para desmarcar os cookies que persistem no seu dispositivo, vá para `edge://settings/siteData`.  

Para impedir que anúncios sejam personalizados, vá para [Configurações de anúncios][MicrosoftAccountPrivacyAdSettings] no [painel de privacidade da Microsoft][MicrosoftAccountPrivacy] e desative a configuração **Ver anúncios personalizados em seu navegador**.  Para desligar os blocos de links rápidos, abra **botão Personalizar** > **Personalizado** e desative a configuração **Mostrar links rápidos**.  O Microsoft Edge usa o histórico de navegação local para personalizar os blocos de links rápidos e você pode excluir ou criar novos blocos.  Os dados são armazenados apenas localmente no dispositivo, por perfil.  

A caixa de pesquisa na página de nova guia executa uma pesquisa do Bing com base na consulta de pesquisa digitada.  Para fornecer sugestões e resultados de pesquisa automaticamente, o Microsoft Edge compartilha com o Bing os caracteres digitados, a consulta de pesquisa, o endereço IP e o identificador de pesquisa.  A caixa de pesquisa pode ser configurada com políticas de grupo para fornecer resultados da Pesquisa da Microsoft, retornando informações da sua organização, como documentos e conteúdo da intranet.  Para fornecer uma experiência de pesquisa integrada, o Microsoft Edge armazena cookies localmente no dispositivo.  

Se você estiver conectado ao Microsoft Edge com sua conta Microsoft, poderá gerenciar suas atividades de navegação associadas à página de nova guia no [painel de privacidade da Microsoft][MicrosoftAccountPrivacyAdSettings].  

O Microsoft Edge coleta dados de diagnóstico sobre como você usa a nova guia, como interações com a caixa de pesquisa e seleções em blocos de link rápido.  Para habilitar o conjunto de dados de diagnóstico sobre como você usa a página nova guia, vá para `edge://settings/privacy` e ative a configuração **Ajudar a melhorar os produtos da Microsoft enviando dados de diagnóstico opcionais sobre como você usa o navegador, os sites que visita e os relatórios de falha**.  O navegador envia dados de diagnóstico sobre como você usa a página do Microsoft News para a Microsoft, para ajudar a entender as interações do usuário com o conteúdo de notícias e melhorar os produtos da Microsoft.  Você pode desativar o conteúdo do Microsoft News selecionando o botão Personalizar na página de nova guia.  Os dados de notícias são enviados à Microsoft através de HTTPS e armazenados por até 13 meses, após os quais são agregados e tornados anônimos.  

A página de nova guia também permite definir uma imagem personalizada como plano de fundo.  A imagem é armazenada localmente no dispositivo e pode ser excluída removendo a imagem ou carregando uma nova.  As informações sobre a imagem são enviadas à Microsoft.  

### Office 365  

Se você estiver conectado ao Microsoft Edge com uma conta corporativa ou de estudante, sua organização poderá ativar o Office 365 como uma opção para o conteúdo da página na página de nova guia.  No momento, o recurso está disponível apenas para clientes comerciais e é regido pelos [OST (Termos do Microsoft Online Services)][MicrosoftLicensingProductProducts].  Para obter mais informações sobre privacidade do Office 365, confira [Visão geral dos controles de privacidade do Microsoft 365 Apps para Grandes Empresas][DeployedgePrivacyOverviewControls].  

A navegação InPrivate e o modo Convidado oferecem experiências alternativas na página de nova guia.  

## Na inicialização  

O Microsoft Edge permite que você continue sua navegação de onde parou, abrindo suas últimas guias abertas da sessão de navegação anterior incluindo os cookies da sessão. Ele permanece disponível na inicialização para restaurar as guias da sessão anterior e manter você conectado aos sites visitados.  Para habilitar a abertura das últimas guias abertas da sessão de navegação anterior, vá para `edge://settings/onStartup` e ative a configuração **Continuar de onde você parou**.  Se você selecionar a configuração **Continuar de onde você parou** e limpar os dados de navegação sempre que fechar o navegador, os dados especificados serão excluídos, mas a URL persistirá na próxima sessão.  

Você também pode configurar o Microsoft Edge para abrir páginas específicas na inicialização.  As páginas que você especifica são armazenadas localmente em seu dispositivo e são específicas para seu perfil.  Se você ligar a sincronização para Configurações, as páginas especificadas serão sincronizadas em todas as versões do Microsoft Edge, onde você estiver conectado.  Para habilitar a sincronização das suas configurações, vá para `edge://settings/profiles/sync` e ative **Configurações**.  

As guias InPrivate e no modo Convidado não são restauradas na inicialização.  

## Monitor de Senhas
O Microsoft Edge tem o compromisso de manter você seguro na Web.  Para ajudar a manter suas informações pessoais privadas e seguras, se você estiver conectado ao Microsoft Edge, o Monitor de Senhas alertará você se suas credenciais forem expostas a uma violação de dados de terceiros.  Se o Monitor de Senhas estiver ativado, suas credenciais são salvas com hash e criptografadas localmente no dispositivo, enviadas aos servidores da Microsoft por HTTPS e comparadas com uma lista criptografada de credenciais violadas conhecidas.  Seu identificador de conta conectado é enviado com segurança, juntamente com suas credenciais com hash e criptografadas, para o serviço Monitor de Senhas.  Se uma credencial for encontrada na lista de credenciais violadas conhecidas, a Microsoft enviará uma resposta criptografada de volta à sua versão do Microsoft Edge para avisar você de que sua credencial foi detectada como parte de um ataque ou violação.  Nenhum dado é armazenado nos servidores da Microsoft após a conclusão da verificação.   

O recurso está disponível apenas para os usuários conectados ao Microsoft Edge.  O Microsoft Edge solicita permissão para ativar o Monitor de Senhas.  Para ativar ou \(desativar\) o Monitor de Senhas, vá para `edge://passwords`.

## Pagamentos  

O Microsoft Edge ajuda você a ser mais produtivo, permitindo salvar suas informações de pagamento em seu perfil do navegador e se oferecendo para preencher automaticamente as informações dos formulários de pagamento enquanto você navega.  Quando você encontra um formulário de pagamento semelhante, o Microsoft Edge oferece o preenchimento do formulário com as informações salvas.  Os cartões de crédito e outras informações de pagamento só são salvos com sua permissão explícita.  

O Microsoft Edge pergunta se você deseja armazenar suas informações de pagamento se o preenchimento automático de pagamento for ativado.  As informações são criptografadas localmente no seu dispositivo.  Para excluir informações de pagamento salvas, vá para `edge://settings/payments`.  Quando você exclui as informações de pagamento salvas, elas não são mais exibidas como uma sugestão de preenchimento automático.  Para não salvar nenhuma informação de pagamento, vá para `edge://settings/payments` e ligue o recurso.  

O Microsoft Edge oferece suporte à API PaymentRequest, permitindo que você pague por compras usando as informações de pagamento salvas anteriormente através do preenchimento automático.  A API PaymentRequest permite que o estabelecimento solicite as seguintes informações: número do cartão de crédito, vencimento do cartão de crédito, nome completo, endereço de cobrança, endereço de email, número de telefone e endereço de entrega.  A API informa ao estabelecimento que o usuário tem as informações do cartão de crédito salvas, mas não compartilha nenhuma informação até que você concorde.  Para ligar o recurso Pagamentos, vá para `edge://settings/privacy`.  

Caso tenha salvo anteriormente as informações de pagamento em sua conta Microsoft, elas também estarão disponíveis para preenchimento automático no navegador.  As informações de pagamento armazenadas na sua conta Microsoft são sincronizadas entre dispositivos.  Se você já fez compras no Xbox ou na Microsoft Store, talvez já tenha as informações de pagamento salvas na sua conta Microsoft.  Durante o preenchimento automático de pagamento, um cartão da sua conta Microsoft é mascarado e só é totalmente revelado após a autenticação de dois fatores.  A máscara oferece segurança adicional enquanto recupera suas informações de pagamento.  

## A personalização de publicidade, pesquisa, notícias e outros serviços Microsoft  

Se você permitir a personalização, a equipe do Microsoft Edge coletará e usará o histórico de navegação do Microsoft Edge para personalizar experiências e anúncios no [Bing][|::ref3::|Main], no Microsoft News e em outros serviços da Microsoft.  A personalização fornece resultados de pesquisa, anúncios e conteúdos de notícias mais relevantes e úteis.  Por exemplo, se a equipe do Microsoft Edge deduzir, com base na sua navegação, que você prefere comprar em uma determinada loja, os anúncios que você vê podem ser adaptados aos produtos dessa loja.  Da mesma forma, se você costuma ver blogs de viagens e ler artigos sobre esse mesmo tema, seu feed de notícias pode incluir conteúdos de notícias mais relevantes sobre viagens.  
 
O recurso está disponível apenas para usuários com conta Microsoft que não seja de criança.  O recurso não está disponível para usuários conectados ao Microsoft Edge com uma conta corporativa ou de estudante.  

O histórico de navegação será coletado e usado para personalização somente se todas as quatro condições forem atendidas:  

*   O usuário está conectado com uma conta Microsoft que não é de criança. 
*   O usuário concedeu permissão para a coleta e o uso dos dados para personalização.  
*   As políticas de grupo do usuário gerenciadas pela organização \(empregador, escola e assim por diante\) permitem personalização.  
*   O usuário não está usando o navegador no modo Convidado ou InPrivate.  

Seu histórico de navegação e outros dados relevantes são transferidos por HTTPS e anexados às suas informações da conta Microsoft.  Seu histórico de navegação é armazenado em servidores Microsoft seguros.  Você pode visualizar e excluir o histórico de navegação compartilhado anteriormente acessando o [painel de privacidade da Microsoft][MicrosoftAccountPrivacy].  Seu histórico de navegação é armazenado em servidores da Microsoft seguros por até 45 dias.  Após 45 dias, os dados são excluídos e não são usados para personalização.  

Você pode modificar seus interesses ou recusar anúncios personalizados das [Configurações de anúncios][MicrosoftAccountPrivacyAdSettings] no [painel de privacidade da Microsoft][MicrosoftAccountPrivacy].  

> [!NOTE]
> A recusa de anúncios personalizados no [painel de privacidade da Microsoft][MicrosoftAccountPrivacy], não desativará a coleta e o uso do seu histórico de navegação para personalização dos resultados de pesquisa e dos conteúdos no seu feed de notícias.  Para desabilitar a coleta e o uso do seu histórico de navegação do Microsoft Edge para obter notícias e resultados de pesquisa personalizados, vá para `edge://settings/privacy` e em **Personalizar sua experiência na web**, desative a configuração **Melhorar sua experiência na Web, permitindo que a Microsoft use seu histórico de navegação na conta para personalizar anúncios, pesquisas, notícias e outros serviços Microsoft**.  Se você parar de compartilhar os dados, a Microsoft não mais coletará e usará seu histórico de navegação para personalizar anúncios, resultados de pesquisa e notícias. Para obter mais informações sobre personalização no Microsoft Edge, confira [Histórico de navegação do Microsoft Edge para obter experiências e anúncios personalizados][MicrosoftSupport4532583].  

## Print  

O Microsoft Edge permite imprimir páginas da Web, arquivos PDF ou qualquer outro conteúdo usando uma variedade de dispositivos e aplicativos.  Quando você imprime em uma impressora, aplicativo ou PDF, o Microsoft Edge envia os comandos e as informações do arquivo para o sistema operacional do seu dispositivo.  A informação não é enviada à Microsoft, e todos os dados enviados ao sistema operacional do seu dispositivo para impressão são imediatamente apagados após a impressão ser concluída ou cancelada.  Para mudar o destino da sua impressão, vá para `edge://settings/printing`.  

Você também pode imprimir páginas da Web e arquivos em um PDF usando a Impressão da Microsoft em PDF, que não envia dados sobre o arquivo para a Microsoft.  As anotações feitas no arquivo PDF serão salvas localmente no arquivo.  

## Perfis  

Os perfis no Microsoft Edge permitem separar os dados de navegação em perfis independentes.  Os dados associados a um perfil são separados dos dados associados a outros perfis.  Seu histórico e favoritos pessoais, por exemplo, não serão sincronizados com sua conta corporativa se você os configurar em perfis diferentes.  

No entanto, os usuários podem alternar facilmente entre os perfis existentes no Microsoft Edge sem a necessidade de senhas.  Se os usuários tiverem acesso ao mesmo dispositivo, eles poderão criar outro perfil na mesma versão do Microsoft Edge sem a permissão do proprietário do perfil atual.  A remoção do perfil das configurações do Microsoft Edge exclui permanentemente os dados de navegação do perfil específico armazenado no dispositivo, como histórico de navegação, favoritos, dados de preenchimento de formulário e senhas.  Os dados sincronizados com a sua conta ainda podem ser armazenados na nuvem da Microsoft, e poderão ser removidos no [painel de privacidade da Microsoft][MicrosoftAccountPrivacy].  

O modo Convidado é uma instância temporária de um novo perfil.  Ele permite que você navegue no dispositivo de outro usuário sem modificar o perfil conectado.  Os dados de navegação do modo Convidado, como favoritos, histórico de navegação, senhas e dados de preenchimento do formulário, não permanecem depois que você fecha todas as janelas do modo Convidado.  Os arquivos baixados são armazenados no dispositivo, mas o histórico dos downloads é excluído.  O modo Convidado permite que você navegue na Web sem estar conectado a outros sites automaticamente.  O Microsoft Edge não envia nenhuma informação que indique aos sites que o usuário está navegando no modo Convidado.  Quando você usa o modo Convidado, a permissão para coletar dados de diagnóstico sobre como você usa o navegador e os sites visitados é obtida do perfil do Microsoft Edge no qual a sessão do modo Convidado foi iniciada.  Todos os dados de navegação de uma específica sessão de modo Convidado são limpos depois que todas as janelas de Convidado são fechadas.  

A navegação InPrivate é um modo de navegação privado no qual nenhum histórico de navegação, histórico de downloads, cookies, dados do site e dados de preenchimento de formulário são lembrados.  O Microsoft Edge salva os arquivos baixados, bem como todos os novos favoritos criados durante a navegação InPrivate.  Por padrão, ao navegar InPrivate, a Microsoft não coleta nenhuma informação sobre sites visitados para fins de melhorias de produto.  A sua escola, seu local de trabalho ou o provedor de serviços de Internet ainda poderão ver a atividade de navegação.  Os dados de navegação de uma específica sessão InPrivate são limpos depois que todas as janelas de InPrivate são fechadas.  Ao usar o teclado IME (Windows Input Method Editor) para digitar e escrever à tinta, os dados podem ser coletados para melhorar os recursos de sugestão e de reconhecimento de idiomas.  Para impedir que os dados de digitação e de escrita à tinta sejam coletados pela Microsoft ao usar o teclado IME do Windows em janelas de navegação InPrivate e normal, abra **Iniciar** > **Configurações** > ** Privacidade** e selecione **Personalização de escrita à tinta e de digitação**.  Para obter mais informações sobre a navegação InPrivate, confira [Navegação InPrivate no Microsoft Edge][MicrosoftSupport4533513].  
  

## Ler em voz alta  

O Microsoft Edge oferece o recurso Ler em voz alta, que lê o conteúdo de uma página da Web para o usuário.  Para começar a Ler em voz alta, passe o cursor em qualquer lugar da página e abra o menu contextual \(clique com o botão direito do mouse\) ou abra **Configurações e mais (...)**  e selecione  **Ler em voz alta**.  Ler em voz alta oferece várias vozes que podem ser usadas para ler o conteúdo da página da Web.  Se você estiver usando vozes [instaladas no Windows 10][OfficeSupport4c83a8d8748642f78e462b0fdf753130] na seção **Hora e Idioma** em Configurações do Windows 10 e quiser limpar o cache local de todas as vozes usadas anteriormente, vá para `edge://settings/clearBrowserData`.  

Quando você começa a Ler em voz alta, o Microsoft Edge utiliza a [API Web Speech][GithubW3cIncubatorCommunityGroupSpeechApi].  Dependendo da voz selecionada, o conteúdo da página é convertido de texto para fala usando uma biblioteca do lado do cliente fornecida pela plataforma \(por exemplo, uma específica para o seu sistema operacional\) ou uma biblioteca do lado do servidor alimentada pelos Serviços Cognitivos do Azure.  Se seu conteúdo for convertido em fala usando uma biblioteca do lado do cliente, nenhuma informação será enviada aos servidores da Microsoft.  Se seu conteúdo for convertido para fala usando os Serviços Cognitivos do Azure (como indicado pela palavra "Online" em qualquer um dos nomes de voz), o texto, juntamente com uma ficha gerada aleatoriamente, será enviado à Microsoft.  Uma vez concluída a conversão, o serviço devolve o texto falado em um arquivo de áudio ao seu dispositivo.  Todos os dados são criptografados durante a transferência do seu dispositivo para a Microsoft e vice-versa.  O texto enviado à Microsoft e o arquivo de áudio gerado são excluídos imediatamente após a conversão. Nenhum outro dado sobre o seu conteúdo da Web é armazenado por qualquer período de tempo.  

## Liberando novas funcionalidades  

Para melhorar o Microsoft Edge, a equipe do Microsoft Edge está sempre aprendendo com os usuários.  Como parte do aprendizado, alguns usuários podem experimentar novas funcionalidades antes que ela sejam disponibilizadas para todo mundo.  Para habilitar novas funcionalidades para usuários selecionados aleatoriamente, o Microsoft Edge envia regularmente as informações necessárias sobre o sistema operacional, canal, versão, país ou região, e outros dados de configuração do dispositivo ao serviço de configuração do Microsoft Edge.  Os dados são enviados com um identificador redefinível exclusivo do seu navegador.  Os dados são transmitidos ao serviço por HTTPS.  Os dados são usados ao receber atualizações para habilitar novas funcionalidades, manter o Microsoft Edge atualizado e com desempenho adequado, e melhorar os produtos e serviços da Microsoft.  Controles e configurações adicionais estão disponíveis para as organizações.  Para obter mais informações sobre controles e configurações adicionais das organizações, confira [Configurações e experimentação do Microsoft Edge][DeployedgeConfigurationExperiments].  

Como usuário, não é possível desativar as atualizações do navegador controladas ou configuradas pela sua organização, mas para controlar se os dados de uso do produto são enviados à Microsoft, vá para `edge://settings/privacy` e altere as configurações em **Dados de diagnóstico opcionais**.  

Para saber como a nova funcionalidade afeta o Microsoft Edge e os serviços da Microsoft, o Microsoft Edge envia um identificador redefinível exclusivo para o seu navegador e uma marca de funcionalidade que codifica qual nova funcionalidade foi habilitada nos serviços Microsoft e no Microsoft Edge.  As novas funcionalidades ajudam a criar as melhores experiências e o melhor navegador para todo mundo.  A marca de funcionalidade não é exclusiva para a sua instalação do Microsoft Edge e é compartilhada em todas as instalações do Microsoft Edge que compartilham o mesmo conjunto de funcionalidades habilitadas.  O Microsoft Edge envia as informações em HTTPS para os serviços Microsoft.  O navegador não envia as informações ao navegar InPrivate ou no modo Convidado.  Para evitar que os dados sejam enviados, vá para `edge://settings/privacy` e desative a configuração **Ajudar a melhorar os produtos Microsoft enviando dados de diagnóstico opcionais sobre como você usa o navegador, os sites que visita e os relatórios de falha**.  Para obter mais informações sobre como redefinir o identificador exclusivo para o seu navegador, confira a seção [Dados de diagnóstico sobre como você usa o navegador](#diagnostic-data).  

## Resolver erros de navegação  

Se o Microsoft Edge detectar tempos limite de conexão SSL, erros de certificado ou outros problemas de rede que possam ser causados por um portal cativo \(por exemplo, uma rede Wi-Fi em um hotel ou aeroporto\), o Microsoft Edge enviará um pedido para `http://edge.microsoft.com/captiveportal/generate_204` e verificará o código de resposta.  Se a solicitação for redirecionada para outra URL, o Microsoft Edge abrirá a URL em uma nova guia, supondo que ela seja uma página de entrada.  As solicitações para a página de detecção de portal cativo são um serviço sem monitoração de estado, as solicitações não são registradas e os cookies não são enviados ou salvos.  Nas plataformas Windows, o Microsoft Edge usa um serviço de portal cativo do Windows.  Caso contrário, será utilizado o serviço de portal cativo do Microsoft Edge.  Para desativar o serviço, vá para `edge://settings/privacy` e desative a configuração **Utilizar um serviço web para ajudar a resolver erros de navegação**.  

## DNS seguro

Para navegar até um site, o navegador deve pesquisar o endereço de rede (por exemplo, 93.184.216.34) para o nome do host (por exemplo, example.com) que é usado na URL do site. O DNS seguro realiza esta pesquisa usando um serviço sobre uma conexão HTTPS ao provedor de serviços DNS, protegendo assim as pesquisas contra modificações ou escutas por invasores na rede.  

Por padrão, seu provedor de serviços DNS atual é usado para evitar interrupções na sua navegação. Nem todos os prestadores de serviços oferecem DNS seguro. Para evitar qualquer interrupção na navegação, se a conexão DNS segura falhar, o Microsoft Edge será retornado e executará uma pesquisa de DNS não criptografada com seu provedor de serviços de DNS atual. O Microsoft Edge permite que você use um provedor de DNS seguro específico. Se um provedor de DNS seguro for escolhido, o Microsoft Edge não voltará à busca regular do DNS se a procuração segura falhar. Você pode escolher suas configurações seguras de DNS em `edge://setting/privacy`.  

O DNS seguro fica desativado por padrão para computadores gerenciados que fazem parte de uma organização, mas podem ser configurados usando políticas administrativas. A navegação InPrivate usa a configuração de permissão de localização do perfil do qual a sessão InPrivate foi iniciada. O modo convidado sempre usará seu provedor de serviços atual.

## Compras

O Microsoft Edge ajuda você a encontrar cupons e preços melhores enquanto faz compras online.  Para ajudá-lo a encontrar cupons enquanto faz compras online, o Microsoft Edge baixa uma lista de domínios de compras localmente para o cliente a partir do serviço de compras da Microsoft.  Quando você visita um site, o Microsoft Edge determina localmente se o site em que você está é um domínio de compras.  Se for determinado que o site é um domínio de compras, o Microsoft Edge enviará o URL com informações de identificação pessoal removidas para o serviço de compras da Microsoft.  O serviço de compras retornará todos os cupons disponíveis para esse site.  

Quando você estiver aplicando cupons, os cookies serão armazenados em seu dispositivo para atribuir corretamente o fornecedor do cupom.  Os cookies só serão salvos por nossos fornecedores de cupons de confiança depois que um cupom for aplicado com sucesso no carrinho.  Após a aplicação dos cupons, as informações sobre o sucesso dos cupons serão enviadas de volta ao serviço de compras da Microsoft para nos ajudar a entender quais cupons foram bem-sucedidos e quais fracassaram.  Os dados enviados ao serviço de compras da Microsoft são enviados por HTTPS com um identificador gerado aleatoriamente que muda por busca de cupom.  

:::image type="complex" source="./media/whitepaper-media/shopping.png" alt-text="Compras e cupons" lightbox="./media/whitepaper-media/shopping.png":::
   Compras e cupons  
:::image-end:::  

Para ajudá-lo a encontrar o melhor preço enquanto estiver comprando online e usando Coleções, o Microsoft Edge determina localmente se a página ou item de coleção que você está visualizando é uma página de detalhes do produto.  Se você estiver olhando para uma página de detalhes do produto, o Microsoft Edge envia os detalhes do produto para o serviço de compras, incluindo o URL com as informações de identificação pessoal removidas. Também enviamos o preço do produto, a imagem do produto, o nome do produto, as classificações e as opiniões, juntamente com informações sobre o Microsoft Edge e sua versão do sistema operacional para o serviço.  Estes dados são enviados sobre HTTPS com um identificador gerado aleatoriamente.  O serviço de compras da Microsoft retornará os preços de outros varejistas para o mesmo produto.  

O serviço de compras está ativado por padrão para todos os usuários.  Para alterar a configuração de compras no Microsoft Edge, navegue até `edge://settings/privacy`, e depois desative **Economize tempo e dinheiro com Compras no Microsoft Edge**.  A navegação InPrivate usa a configuração de compras do perfil que iniciou a sessão InPrivate.  

## Logon e Identidade  

Conectar-se ao Microsoft Edge proporciona acesso a recursos adicionais que tornam o navegador mais produtivo para você.  Para conectá-lo sem problemas, ao iniciar o Microsoft Edge pela primeira vez, o programa tentará detectar a identidade do sistema operacional.  Se o Microsoft Edge detectar a sua identidade no sistema operacional, mas você não quiser permanecer conectado ao Microsoft Edge, vá para `edge://settings/profiles`, e saia ou remova seu perfil.  Para entrar no Microsoft Edge, sua identidade não é detectada no sistema operacional, vá para `edge://settings/profiles`.  

Se uma nova identidade for adicionada ao sistema operacional e, no momento, seu perfil do Microsoft Edge não tiver uma identidade, o Microsoft Edge adicionará a identidade específica ao seu perfil.  Se você se conectar ao Microsoft Edge com uma conta Microsoft, uma conta corporativa ou uma de estudante, e não tiver uma identidade no seu perfil do Windows 10, a conta específica será adicionada ao seu perfil do Windows 10, a menos que você escolha especificamente não adicioná-la ao Windows 10 ao se conectar.  

Seu perfil conectado não começa a sincronizar seus dados sem a sua permissão explícita ao iniciar o Microsoft Edge pela primeira vez ou ao se conectar ao navegador.  

Estar conectado ao Microsoft Edge permite o logon único \(você entra automaticamente em determinados sites como o Bing\) e outras experiências de identidade, como a sincronização. Caso queira se conectar apenas ao Microsoft Edge e não em outros sites da Microsoft, como o [Bing][|::ref4::|Main], poderá sair do site específico.  O Microsoft Edge cria um cookie de saída que informa ao Microsoft Edge para não se conectar ao site específico em visitas futuras.  Para entrar em sites específicos novamente usando seu nome de usuário e senha ou limpar seus cookies, vá para `edge://settings/privacy`.  Para obter mais informações sobre como limpar dados de navegação, confira [Exibir e excluir o histórico de navegação do Microsoft Edge][MicrosoftSupport10607].  

Para impedir que qualquer identidade seja associada ao Microsoft Edge, remova seu perfil do Microsoft Edge ou se desconecte dele.  Para excluir todos os dados associados ao seu perfil do Microsoft Edge do dispositivo, você deve remover o seu perfil dele.  Excluir todos os dados não exclui os dados sincronizados anteriormente associados à identidade.  

Sua identidade no Microsoft Edge no macOS é compartilhada entre os aplicativos da Microsoft.  Uma identidade compartilhada permite que você entre em um aplicativo da Microsoft sem precisar inserir suas credenciais separadamente, caso esteja conectado a outro aplicativo da Microsoft no dispositivo.  No macOS, você não entra automaticamente no Microsoft Edge com base no estado de autenticação em outro aplicativo da Microsoft.  Quando você tenta entrar no Microsoft Edge, ele oferece as credenciais de outro aplicativo da Microsoft no dispositivo para que entre nele sem problemas.  Da mesma forma, quando você está conectado a uma conta do Microsoft Edge, se tentar entrar em outros aplicativos da Microsoft, as credenciais do Microsoft Edge podem ser usadas para ajudá-lo a entrar no outro aplicativo da Microsoft no dispositivo sem solicitar que você insira suas credenciais novamente.  

Não é possível se conectar ao Microsoft Edge no modo Convidado ou no InPrivate.  

## SmartScreen  

O SmartScreen foi projetado para ajudar você a navegar na Web com segurança.  Quando você acessa sites ou baixa arquivos, o SmartScreen verifica a reputação da URL ou do arquivo.  Se o SmartScreen determinar que o site ou o arquivo é mal-intencionado, ele impedirá que você acesse o site ou baixe o arquivo.  

:::image type="complex" source="./media/whitepaper-media/smart-screen.png" alt-text="SmartScreen" lightbox="./media/whitepaper-media/smart-screen.png":::
   SmartScreen  
:::image-end:::  

Enquanto você navega na Web, o SmartScreen categoriza sites e downloads como tráfego principal, perigoso ou desconhecido.  Fazem parte do tráfego principal sites populares que o SmartScreen tenha determinado como confiáveis.  Se você for a um site marcado como perigoso, o SmartScreen imediatamente o impedirá de acessar o site.  Ao acessar um site desconhecido, o SmartScreen verifica a reputação para determinar se você deve acessar o site.  

O SmartScreen usa três tipos de verificações de reputação.  Primeiro, o SmartScreen verifica a URL dos sites visitados em uma lista local para determinar se o site faz parte do tráfego principal ou se é um site perigoso conhecido.  Ao visitar um site de tráfego principal, o SmartScreen não envia a URL ao serviço SmartScreen.  Se a URL estiver na lista local de sites perigosos, o SmartScreen o bloqueará, impedindo o carregamento de qualquer parte do conteúdo da Web mal-intencionado.  O Microsoft Edge baixa periodicamente uma lista atualizada de tráfegos principais e de sites perigosos para o dispositivo.  O segundo tipo de verificação de URL é uma verificação de reputação assíncrona do serviço SmartScreen.  O SmartScreen realiza a verificação em todas as URLs que não são classificadas como tráfego principal.  Para determinar a segurança do site, o Microsoft Edge passa ao serviço SmartScreen a URL, informações relevantes sobre o site, um identificador exclusivo para o seu dispositivo e informações gerais de localização.  As informações fornecidas pelo Microsoft Edge permitem que o serviço identifique novos sites perigosos e mantenha-se atualizado com as ameaças de segurança mais recentes.  Os resultados das verificações de URL são armazenados localmente no dispositivo e apagados automaticamente no final da sessão do navegador.  Todas as solicitações para o serviço SmartScreen são feitas com criptografia HTTPS.  

Terceiro, o SmartScreen verifica os arquivos baixados para ajudar a evitar danos ao dispositivo.  O SmartScreen executa uma verificação de reputação do arquivo binário de forma síncrona, conforme o download é concluído.  Para executar a verificação de reputação, o Microsoft Edge envia ao SmartScreen informações sobre o arquivo, como o hash do arquivo, o nome do arquivo, o URI de download e um identificador exclusivo do dispositivo.   Todas as solicitações do SmartScreen são feitas com criptografia HTTPS.  O serviço SmartScreen retorna o resultado da verificação, o que permite que o arquivo seja baixado integralmente ou não.  Os resultados são armazenados localmente no dispositivo.  

O serviço SmartScreen armazena dados sobre as verificações de reputação e cria um banco de dados de arquivos e URLs maliciosos conhecidos.  Os dados são armazenados em servidores seguros da Microsoft e são usados apenas para serviços de segurança da Microsoft.  Os dados nunca são usados para identificar ou marcar você de qualquer forma.  A limpeza do cache de navegação limpa todos os dados da URL do SmartScreen armazenados localmente.  A limpeza do histórico de downloads remove todos os dados do SmartScreen armazenados localmente relacionados a downloads de arquivos.  

O SmartScreen está ativado por padrão no Microsoft Edge.  Para desativar o SmartScreen, vá para `edge://settings/privacy` e, em **Segurança**, desative a configuração do **Microsoft Defender SmartScreen**.  A configuração é a mesma para todos os perfis associados à instalação do Microsoft Edge no seu dispositivo.  A configuração não é sincronizada entre dispositivos.  A configuração se aplica à navegação InPrivate e ao modo Convidado.  Se o seu dispositivo for gerenciado com políticas de grupo definidas pela sua organização, a configuração será refletida no Microsoft Edge.  Para exibir a configuração, vá para `edge://settings/privacy`.  Para mais informações sobre o SmartScreen, confira [SmartScreen: perguntas frequentes][MicrosoftSupport17443].  

Opcionalmente, o SmartScreen verifica as URLs dos arquivos baixados para ver se algum deles está classificado como aplicativos potencialmente indesejados.  O bloqueio de aplicativos potencialmente indesejados ajuda a proporcionar experiências mais produtivas, avançadas e agradáveis do Windows.  A configuração está desativada por padrão e disponível apenas em dispositivos Windows 10.  Para habilitar o recurso, vá para `edge://settings/privacy` e ative a configuração **Bloquear aplicativos potencialmente indesejados**.  Para obter mais informações sobre como os aplicativos potencialmente indesejados são categorizados, confira [PUA (Aplicativo Potencialmente Indesejado)][WindowsSecurityThreatProtectionIntelligenceCriteriaPotentiallyUnwanted].  Para obter mais informações sobre como definir a configuração, confira [Detectar e bloquear aplicativos potencialmente indesejados][WindowsSecurityThreatProtectionWindowsDefender].  

## Reconhecimento de fala

Para converter sua fala em texto, o Microsoft Edge tem suporte da [Web Speech API][GithubW3cIncubatorCommunityGroupSpeechApi].  Se um site incluir um recurso da Web que exija captura e tradução do seu discurso em texto e solicitar acesso ao seu microfone, o Microsoft Edge enviará o áudio capturado para um serviço da Microsoft, onde será traduzido em texto.  O áudio gravado é enviado com um token gerado aleatoriamente por uma conexão HTTPS segura com os Serviços Cognitivos do Microsoft Azure.  O conteúdo de áudio gravado não é armazenado para nenhuma finalidade.  O texto é enviado de volta ao seu dispositivo e, em seguida, enviado ao site.  

Para desativar a fala traduzida em texto, você pode negar o acesso ao microfone de qualquer site que solicite permissão.  Para desligar a permissão de microfone para todos os sites, vá para `edge://settings/content/microphone`.  

## Verificação Ortográfica  

O Microsoft Edge verifica a ortografia à medida que você digita no navegador.  O serviço de verificação ortográfica é concluído localmente no dispositivo. O Microsoft Edge não envia informações sobre sua digitação à Microsoft para verificação ortográfica.  Para desativar o recurso, vá para `edge://settings/languages` e em **Verificar ortografia**, desative a configuração de cada idioma.  

Ao adicionar um novo idioma ao Microsoft Edge, o navegador baixa o dicionário do novo idioma no dispositivo usando HTTPS.  O dicionário é usado para o serviço de verificação ortográfica interno.  Ao excluir o idioma das configurações do Microsoft Edge, o dicionário é excluído do dispositivo.  O modo Convidado não usa o dicionário personalizado do perfil ou de qualquer idioma adicionado.  Para adicionar ou remover palavras no dicionário local, vá para `edge://settings/languages` e em **Verificar ortografia**, selecione **Adicionar ou excluir palavras**.  

## Sugerir sites semelhantes  

Para ajudar a resolver erros de digitação de URL na barra de endereços que resultam em um erro de site, o Microsoft Edge pode recomendar uma URL corrigida.  Quando ocorre um erro de navegação no site, o Microsoft Edge envia o domínio do endereço da Web ao serviço da Microsoft para sugerir uma URL corrigida.  O Microsoft Edge não inclui identificadores ou tokens com o domínio.  Se o serviço encontrar uma sugestão, ele retornará a URL sugerida.  A Microsoft armazena o domínio incorreto e o domínio sugerido para ajudar a melhorar o serviço.  Para ajudar você a navegar até os sites corretos, o recurso está ativado por padrão.  Para desativar o recurso, vá para `edge://settings/privacy` e, em **Serviços**, desative a configuração **Sugerir sites semelhantes quando não for possível encontrar um site**.  

## Sync  

Fazer o logon no Microsoft Edge com uma conta Microsoft permite que você sincronize seus dados de navegação em todas as suas versões conectadas do Microsoft Edge.  Você pode sincronizar seu histórico de navegação, favoritos, configurações, dados de preenchimento de formulário (endereços e mais), senhas, extensões e coleções.  Você deve permitir a ativação da sincronização no Microsoft Edge e cada tipo de dado sincronizado poderá ser ativado ou desativado individualmente.  Os favoritos incluem as guias reservadas anteriormente na versão herdada do Microsoft Edge, que são sincronizadas com os demais favoritos.  Os favoritos excluídos ou modificados, ou outros dados de uma versão conectada do Microsoft Edge, são sincronizados com todas as outras versões conectadas do Microsoft Edge em que a sincronização está ativada.  Para gerenciar as configurações de sincronização, vá para `edge://settings/profiles/sync`.  As configurações de sincronização podem ser gerenciadas pela sua organização.

:::image type="complex" source="./media/whitepaper-media/sync.png" alt-text="Imagem da configuração de sincronização sendo definida como ativado" lightbox="./media/whitepaper-media/sync.png":::
   A configuração de sincronização está ativada
:::image-end:::  

Para que a sincronização funcione, são enviados dados adicionais de conectividade e configuração do dispositivo necessários para fornecer a experiência de sincronização, como o nome do seu dispositivo, marca e modelo.  Os dados podem ser excluídos no [painel de dispositivos Microsoft][MicrosoftAccountDevices].  Para gerenciar seus favoritos sincronizados, vá para `edge://favorites`.  Para gerenciar todos os outros tipos de dados, vá para `edge://settings/profiles`.  

Todos os dados sincronizados são criptografados em trânsito por HTTPS quando transferidos entre o navegador e os servidores da Microsoft.  Os dados sincronizados também são armazenados em um estado criptografado nos servidores da Microsoft.  Os tipos de dados confidenciais, como endereços e senhas, são criptografados no dispositivo antes de serem sincronizados.  Se você estiver usando uma conta corporativa ou de estudante, todos os tipos de dados serão criptografados antes mesmo de serem sincronizados usando a Proteção de Informações da Microsoft.  Todos os outros tipos de dados sincronizados serão armazenados até você excluir os dados, a conta ser excluída ou a conta ficar inativa.  Uma ID da conta é anexada a todos os dados sincronizados, pois a ID é necessária para executar a sincronização em vários dispositivos. 

Os dados de navegação InPrivate e no modo Convidado não são sincronizados com sua conta Microsoft.  No entanto, os favoritos criados durante as sessões InPrivate são sincronizados nas versões conectadas do Microsoft Edge, onde a sincronização está ativada.  

## Dicas e recomendações

O Microsoft Edge pretende fornecer a você dicas e recomendações relevantes para obter a melhor experiência com o navegador.  O Microsoft Edge usa os dados disponíveis de conectividade e configuração do dispositivo para fornecer dicas e recomendações relevantes.  Esses dados consistirão em seu sistema operacional, localização, configurações do navegador e outros dados de conectividade e configuração do dispositivo.  Estes dados são enviados através de uma conexão HTTPS segura com um identificador reinicializável exclusivo para seu navegador.  Para dispositivos Windows 10, enquanto o Microsoft Edge está sendo configurado, honramos experiências personalizadas no Windows.  [Saiba mais sobre experiências personalizadas no Windows](https://support.microsoft.com/help/4468236/diagnostics-feedback-and-privacy-in-windows-10-microsoft-privacy).  

Esses dados não são enviados durante a navegação InPrivate ou no Modo convidado.  

## Prevenção contra rastreamento  

O Microsoft Edge foi projetado para detectar e bloquear rastreadores conhecidos.  Os usuários podem escolher entre três níveis de prevenção contra rastreamento: Básico, Equilibrado e Estrito.  Para proteger a privacidade do usuário, a opção Equilibrado é selecionada por padrão.  O Microsoft Edge detecta os rastreadores antes que qualquer um seja carregado na página, utilizando uma lista de rastreadores conhecidos de código aberto.  A lista é baixada periodicamente para o dispositivo à medida que a lista é atualizada.  O número e o nome dos rastreadores bloqueados são armazenados localmente no dispositivo para fins estatísticos.  Para limpar os dados, vá para `edge://settings/privacy/blockedTrackers`.  A detecção e o bloqueio dos rastreadores ocorrem localmente no dispositivo.  Para desabilitar a prevenção contra rastreamento, vá para `edge://settings/privacy`.  Para obter mais informações sobre a Prevenção contra rastreamento, confira [Saiba mais sobre a prevenção contra rastreamento no Microsoft Edge][MicrosoftAccount4533959].  

Você pode desativar as atualizações da lista usando a seguinte política de grupo, [Habilitar atualizações de componentes no Microsoft Edge][DeployedgePoliciesComponentupdatesenabled].  

:::image type="complex" source="./media/whitepaper-media/tracking-prevention.png" alt-text="Prevenção contra rastreamento" lightbox="./media/whitepaper-media/tracking-prevention.png":::
   Prevenção contra rastreamento  
:::image-end:::  

## Traduzir  

No Microsoft Edge, você pode navegar na Web e traduzir páginas da Web em um idioma de sua escolha.  O recurso de tradução interno usa um serviço no seu dispositivo que mostra partes aleatórias de uma página da Web para detectar o idioma original.  Se o idioma detectado não for um dos idiomas padrão, o Microsoft Edge oferecerá a tradução da página da Web para o seu idioma ou para outro idioma que você escolher.  O Microsoft Edge não traduz uma página da Web sem sua permissão.  Você também pode traduzir uma página da Web clicando com o botão direito do mouse na página e selecionando **Traduzir**.  Para traduzir a página da Web, o Microsoft Edge envia o conteúdo da página e um token gerado aleatoriamente ao serviço de tradução do Microsoft Azure através de uma conexão HTTPS segura.  O conteúdo da página não é armazenado para nenhuma finalidade.  Para impedir que o Microsoft Edge se ofereça para traduzir páginas da Web, vá para `edge://settings/languages` e desative a configuração **Oferecer para traduzir páginas que não estão em um idioma que você lê**.  

## Aplicativos da Web e sites fixos  

O Microsoft Edge permite instalar aplicativos da Web criados por desenvolvedores de site e fixar seus sites favoritos.  

Quando você fixa um site, ele é adicionado à sua barra de tarefas ou plataforma.  Os dados são armazenados localmente no seu dispositivo.  Para alguns sites, as informações sobre se o site foi fixado são compartilhadas com o site, para que ele não solicite a fixação.  Você pode gerenciar seus sites fixados na barra de tarefas ou na plataforma.  Os sites fixados são abertos em janelas do Microsoft Edge e usam as mesmas permissões de site e configurações de dados de diagnóstico da versão específica do Microsoft Edge.  

## WebView

O Microsoft Edge WebViews permite que os desenvolvedores de aplicativos hospedem conteúdo da Web em aplicativos nativos no Windows 10 e no Windows 7.  Os aplicativos que hospedam o Microsoft Edge WebView podem enviar para a Microsoft dados de diagnóstico, como a forma que você usa a plataforma da Web do Microsoft Edge, e os sites que você visita no aplicativo.  Para habilitar a coleta de dados de diagnóstico, vá para `edge://settings/privacy` e ative a configuração em **Dados de diagnóstico opcionais**.  Para desligar a coleta de dados de diagnóstico do Microsoft Edge no Windows 10,abra **Iniciar** > ** Configurações** > **Privacidade** e selecione **Diagnóstico e comentários**.  Para desativar a coleta de dados de diagnóstico de todas as outras plataformas, vá para `edge://settings/privacy` em uma sessão de navegação normal e desative a configuração **Ajudar a melhorar os produtos Microsoft enviando dados de diagnóstico opcionais sobre como você usa o navegador, os sites que visita e os relatórios de falha**.  Os aplicativos que hospedam o Microsoft Edge WebView podem coletar outros dados controlados pelo gerenciamento de coleta de dados do desenvolvedor e pelas políticas de privacidade relevantes.  

## Windows Defender Application Guard  

O Windows Defender Application Guard \(WDAG\) é um recurso disponível para organizações.  Quando o Windows Defender Application Guard está ativado, o Microsoft Edge abre sites não confiáveis dentro de um contêiner isolado para proteger os recursos em sua organização contra sites mal-intencionados ou ataques de phishing.  O recurso é ativado apenas com políticas de grupo gerenciadas pela sua organização e está disponível apenas nas versões recentes do Windows 10.  O WDAG coleta dados de diagnóstico de melhoria de produtos sobre a abertura de sites não confiáveis no contêiner isolado, como quanto tempo leva para abrir uma nova janela do Application Guard.  

Com sua permissão, o WDAG também coletará informações sobre como você usa o navegador e informações sobre sites que você visita.  Para desligar a coleta de dados de diagnóstico do Microsoft Edge no Windows 10,abra **Iniciar** > ** Configurações** > **Privacidade** e selecione **Diagnóstico e comentários**.  Para desativar a coleta de dados de diagnóstico para todas as outras plataformas, vá para `edge://settings/privacy` em uma sessão de navegação normal e desative a configuração **Ajudar a melhorar os produtos Microsoft enviando dados de diagnóstico opcionais sobre como você usa o navegador, os sites que visita e os relatórios de falha**.  

## Proteção de Informações do Windows  

A Proteção de Informações do Windows \(WIP\) ajuda a impedir o vazamento acidental de informações corporativas.  Ele está disponível apenas para organizações por meio de políticas de grupo gerenciadas pela sua organização.  O WIP é habilitado para os sites identificados como ativos corporativos.  Identifique quais sites são ativos corporativos no ícone de gerenciamento na barra de endereços.  O WIP impõe recursos como a prevenção contra copiar e colar do navegador, ou carregar determinados arquivos em sites fora da organização.  

:::image type="complex" source="./media/whitepaper-media/w-i-p.png" alt-text="Proteção de Informações do Windows" lightbox="./media/whitepaper-media/w-i-p.png":::
   Proteção de Informações do Windows  
:::image-end:::  

Se a WIP estiver habilitada em sua versão do Microsoft Edge, o navegador coletará os logs de eventos e os enviará à sua organização.  Se o WIP estiver ativado, não será possível desativar a coleta de dados.  O WIP só está disponível em versões do Windows 10 de agosto de 2016 ou posterior.  Para obter mais informações sobre os logs de eventos capturados pelo WIP, confira [Como coletar os logs de eventos de auditoria da Proteção de Informações do Windows (WIP)][WindowsSecurityInformationProtectionCollectAuditEventLogs].  

## Obrigado!  

O Microsoft Edge é possível graças ao projeto [Chromium][ChromiumMain] de código aberto e outros softwares de código aberto.  Para ver todos os créditos do software, vá para `edge://credits`.  O [White paper de Privacidade do Google Chrome][GoogleChromePrivacyWhitepaper] foi usado como fonte para coletar informações relacionadas sobre o projeto de código aberto Chromium.  

<!--Microsoft Edge is committed to protecting and respecting your privacy while giving you the transparency and control you deserve.  Reach out to [@MSEdgeDev][TwitterMsedgedev] on Twitter or submit feedback by opening **Settings and more (...)** > **Help and feedback** and selecting **Send feedback** with questions or comments.  -->  

## Entrar em contato com a equipe do Microsoft Edge  

A equipe do Microsoft Edge está sempre ouvindo os clientes e valoriza os seus comentários.  Para fornecer comentários no Microsoft Edge, abra **Configurações e mais** > **Ajuda e comentários** e selecione **Enviar comentários**.  Para os Aplicativos Web Progressivos \(PWAs\), abra **Configurações e mais (...)** e selecione **Enviar comentários à Microsoft**.  Você deve fornecer detalhes sobre os comentários, mas todas as outras informações são opcionais.  Se for detectado que um email é do seu perfil do Microsoft Edge, ele será preenchido previamente, junto com a URL atual do site em que você está e os dados de diagnóstico relevantes.  Os dados de diagnóstico podem incluir dados sobre os recursos do Microsoft Edge ativados e o uso do navegador.  Uma captura de tela, arquivos do seu dispositivo e gravações do seu navegador também podem ser incluídos opcionalmente.  A captura de tela, os arquivos ou as gravações opcionais fornecidos por você podem incluir informações de identificação pessoal.  Os dados serão usados somente para fins de diagnóstico e melhoria do produto.  

Os comentários dos usuários são enviados com segurança à Microsoft usando HTTPS e armazenados em servidores seguros da Microsoft.  Se você incluir seu endereço de email e a configuração **Melhorar os produtos Microsoft enviando relatórios de falha e dados sobre como você usa o navegador** estiver ativada nas configurações de privacidade do Microsoft Edge, um identificador exclusivo para a instalação do navegador no dispositivo será associado aos seus comentários.  Todos os dados de diagnóstico, incluindo logs de diagnóstico, registros, gravações e anexos, são armazenados por até 30 dias.  Os dados de comentários restantes, incluindo uma captura de tela opcional, são armazenados por até 15 meses.  Faça uma [solicitação][MicrosoftConcernPrivacy] para excluir seus comentários, caso tenha fornecido um email com o item de comentários.  

<!-- links -->  

[DeployedgeConfigurationExperiments]: /deployedge/edge-configuration-and-experiments "Configurações e experimentação do Microsoft Edge — Microsoft Docs"  
[DeployedgePoliciesComponentupdatesenabled]: /deployedge/microsoft-edge-policies#componentupdatesenabled "ComponentUpdatesEnabled - Microsoft Edge - Políticas — Microsoft Docs"  
[DeployedgeUpdatePoliciesUpdate]: /deployedge/microsoft-edge-update-policies#update "Atualização - Microsoft Edge - Políticas de atualização — Microsoft Docs"  
[DeployedgeEnterprisePrivacySettings]: /deployedge/microsoft-edge-enterprise-privacy-settings "Configurar as políticas do Microsoft Edge para oferecer suporte à privacidade da empresa — Microsoft Docs"  
[DeployedgePrivacyOverviewControls]: /deployoffice/privacy/overview-privacy-controls "Visão geral dos controles de privacidade do Microsoft 365 Apps para Grandes Empresas — Microsoft Docs"  

[InternetExplorer11DeployGuideCollectDataEnterpriseSiteDiscovery]: /internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery "Coletar dados usando o Enterprise Site Discovery — Microsoft Docs"  

[PlayreadyOverviewSimpleEndSystem]: /playready/overview/simple-end-to-end-system "Sistema de Ponta a Ponta Simples — Microsoft Docs"  

[WindowsPrivacyConfigureDiagnosticDataOrganization]: /windows/privacy/configure-windows-diagnostic-data-in-your-organization "Configurar os dados de diagnóstico do Windows em sua organização — Microsoft Docs"  

[WindowsSecurityInformationProtectionCollectAuditEventLogs]: /windows/security/information-protection/windows-information-protection/collect-wip-audit-event-logs "Como coletar logs de eventos de auditoria da Proteção de Informações do Windows (WIP) — Microsoft Docs"  
[WindowsSecurityThreatProtectionIntelligenceCriteriaPotentiallyUnwanted]: /windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua "Aplicativo potencialmente indesejado (PUA) - Como a Microsoft identifica malware e aplicativos potencialmente indesejados — Microsoft Docs"  
[WindowsSecurityThreatProtectionWindowsDefender]: /windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus "Detectar e bloquear aplicativos potencialmente indesejados — Microsoft Docs"  

[BingMain]: https://bing.com "Bing"  

[ChromiumMain]: https://www.chromium.org "The Chromium Projects"  

[GithubW3cIncubatorCommunityGroupSpeechApi]: https://wicg.github.io/speech-api "Web Speech API Draft Report — W3C Incubator Community Group" 

[GoogleChromePrivacyWhitepaper]: https://www.google.com/chrome/privacy/whitepaper.html "White paper de privacidade do Google Chrome"  

[MicrosoftAccountDevices]: https://account.microsoft.com/devices "Dispositivos — Conta Microsoft"  
[MicrosoftAccountFamilyMain]: https://account.microsoft.com/family "Família — Conta Microsoft"  
[MicrosoftAccountPrivacy]:  https://account.microsoft.com/privacy/ "Privacidade — Conta Microsoft"  
[MicrosoftAccountPrivacyAdSettings]: https://account.microsoft.com/privacy/ad-settings "Adicionar configurações – Privacidade — Conta Microsoft"  

[MicrosoftConcernPrivacy]: https://www.microsoft.com/concern/privacy "Relatar uma Preocupação com Privacidade — Microsoft"  
[MicrosoftLicensingProductProducts]: https://www.microsoft.com/licensing/product-licensing/products "Termos de licenciamento — Licenciamento por Volume da Microsoft"  

[MicrosoftSupport10607]: https://support.microsoft.com/help/10607 "Exibir e excluir o histórico do navegador no Microsoft Edge — Suporte do Microsoft Edge"  
[MicrosoftSupport12413]: https://support.microsoft.com/help/12413 "O que é um grupo de família da Microsoft ? — Suporte à conta da Microsoft"  
[MicrosoftSupport17443]: https://support.microsoft.com/help/17443 "SmartScreen: perguntas frequentes — Suporte do Microsoft Edge"  
[MicrosoftSupport4468236]: https://support.microsoft.com/help/4468236 "Diagnóstico, comentários e privacidade no Windows 10 — Suporte de privacidade da Microsoft"  
[MicrosoftSupport4468240]: https://support.microsoft.com/help/4468240 "Serviço de localização e privacidade do Windows 10 — Suporte de privacidade da Microsoft"  
[MicrosoftSupport4532583]: https://support.microsoft.com/help/4532583 "Histórico de navegação do Microsoft Edge para experiências e publicidade personalizadas — Suporte de privacidade da Microsoft"  
[MicrosoftSupport4533513]: https://support.microsoft.com/help/4533513 "Navegar InPrivate no Microsoft Edge — Suporte do Microsoft Edge"  
[MicrosoftAccount4533959]: https://support.microsoft.com/help/4533959 "Saiba mais sobre controle de prevenção no Microsoft Edge — Suporte à privacidade da Microsoft"  

[OfficeSupport4c83a8d8748642f78e462b0fdf753130]: https://support.office.com/article/4c83a8d8-7486-42f7-8e46-2b0fdf753130 "Baixar vozes para os recursos de Leitura Avançada, Modo de Leitura e Ler em Voz Alta — Suporte do Office"  

[W3cEncryptedMediaPrivacy]: https://w3.org/TR/encrypted-media#privacy "11. Privacidade – Extensões de Mídia Criptografada — W3C"  
[W3cGeolocationApiMain]: https://w3.org/TR/geolocation-api "Especificação da API de Geolocalização 2ª Edição — W3C"  

[TwitterMsedgedev]: https://www.twitter.com/MSEdgeDev "Canal Microsoft Edge Dev — Twitter"  
