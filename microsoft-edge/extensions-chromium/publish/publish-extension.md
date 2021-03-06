---
description: Publicar extensões do Microsoft Edge (Chromium) no Armazenamento de Complementos do Microsoft Edge
title: Publicar sua extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 67fdbdb39f3ef0b2b6cef2831520849933ffeeec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399124"
---
# <a name="publish-your-extension"></a>Publicar sua extensão  

Depois de desenvolver e testar sua extensão, você estará pronto para distribuir sua extensão. Use o Armazenamento de Complementos do Microsoft Edge para distribuir sua extensão.  Para liberar sua extensão Chromium existente para usuários do Microsoft Edge, navegue até [por sua extensão Chromium existente.][PortChromiumExtension]  

Publique sua extensão no armazenamento de Complementos do Microsoft Edge para aumentar o alcance dela e torná-la disponível para os usuários do Microsoft Edge.  Este artigo fornece o processo para enviar sua extensão para o armazenamento de Complementos do Microsoft Edge.  

## <a name="before-you-begin"></a>Antes de começar  

Você deve ter um protótipo de trabalho de sua extensão pronto.  Para obter informações sobre como criar uma extensão, consulte o [tutorial Introdução.][ExtensionsGettingStarted]  

Para publicar sua extensão no armazenamento de Complementos do Microsoft Edge, use sua conta de desenvolvedor ativa no [Partner Center][MicrosoftPartnerCenter].  Se você não tiver uma conta de desenvolvedor, crie uma nova conta de desenvolvedor.  Para abrir uma nova conta de desenvolvedor e se registrar no programa de complementos do Microsoft Edge, navegue até [Registro do desenvolvedor][DeveloperRegistration].  

Crie um arquivo zip que representa o pacote de extensão.  Seu pacote de extensão deve incluir os arquivos a seguir.  

*   O manifesto de extensão especificando detalhes como o nome da extensão, descrição curta, permissões e idioma padrão.  
*   Imagens e outros arquivos exigidos pela extensão.  

Os campos a seguir no manifesto são incluídos automaticamente nos detalhes de listagem da loja.  Os campos são somente leitura na **página Listagens da** Loja.  A página listagens da loja é descrita posteriormente neste artigo.  Certifique-se de que os valores de campo corresponderão à exibição preferencial na página de detalhes da loja antes de carregar o pacote no Partner Center.  Para um exemplo do código necessário para o arquivo de manifesto, revise as noções básicas do arquivo de manifesto.  

*   `Name` no arquivo de manifesto, que é o **nome de exibição** na página de detalhes do armazenamento.  
*   `Description` no arquivo de manifesto, que é a **descrição Curta** na página de detalhes do armazenamento.  Forneça uma descrição curta e cntente a ser exibida na parte superior da listagem para sua extensão.  Quando incluído, a breve descrição especificada no arquivo de manifesto de extensão é exibida na listagem da loja.  Se uma descrição curta não estiver incluída no arquivo de manifesto, as primeiras linhas de Descrição serão exibidas.  Forneça uma breve descrição para evitar a repetição de conteúdo na página de listagem da loja.  

## <a name="submit-your-extension-to-microsoft-edge-add-ons-store"></a>Enviar sua extensão para o Armazenamento de Complementos do Microsoft Edge  

Para enviar sua extensão ao [Partner Center,][MicrosoftPartnerCenter]use as etapas a seguir.  

#### <a name="step-1--start-a-new-submission"></a>Etapa 1: Iniciar um novo envio  

Navegue até o [painel do desenvolvedor][MicrosoftPartnerCenter] e escolha Criar nova **extensão** na página **Visão** Geral.  

#### <a name="step-2--upload-the-extension-package"></a>Etapa 2: Carregar o pacote de extensão  

Use a **página Pacotes** para carregar o arquivo zip do pacote de extensão.  Você só pode carregar um pacote por vez.  Você não poderá continuar com o envio se o carregamento do pacote não for bem-sucedido na página **Pacotes.**  

Para carregar o pacote, escolha e arraste o pacote para o campo de carregamento. Você também pode escolher **Procurar seus arquivos**.  Depois que o pacote é carregado, seu pacote é validado.  Depois que a validação for bem-sucedida, revise os detalhes da extensão e escolha **Próximo** para continuar.  Se houver erros de validação, resolva os problemas e tente carregar novamente.  

#### <a name="step-3--provide-availability-details"></a>Etapa 3: Fornecer detalhes de disponibilidade  

Na página **Disponibilidade,** insira as informações a seguir sobre a disponibilidade de sua extensão.  

##### <a name="visibility"></a>Visibilidade  

Escolha uma das seguintes opções de visibilidade para definir se sua extensão pode ser descoberta no armazenamento de Complementos do Microsoft Edge.  

*   `Public` \(default\)  
    O público permite que todos descubram sua extensão por meio de pesquisa, navegando no armazenamento de Complementos do Microsoft Edge ou usando a URL de listagem para sua extensão no armazenamento de Complementos do Microsoft Edge.  A URL de listagem está disponível no painel do Partner Center na página Visão geral **da** extensão.  
    
*   `Hidden`  
    Oculto remove extensões dos resultados da pesquisa ou da navegação no armazenamento de Complementos do Microsoft Edge.  Para distribuir extensões ocultas no armazenamento de Complementos do Microsoft Edge, você deve compartilhar a URL de listagem para a extensão com seus clientes.  
    
> [!NOTE]
> Você pode alterar a visibilidade da extensão de **Public** para **Hidden**.  Os usuários que instalaram sua extensão enquanto a visibilidade foi definida como público retêm o acesso à sua extensão e recebem todas as atualizações disponibilizadas por meio do site de complementos do Microsoft Edge.  

##### <a name="markets"></a>Mercados  

Defina os mercados específicos nos quais você planeja oferecer sua extensão.  A configuração padrão para mercados é todos os mercados e isso inclui todos os mercados futuros adicionados posteriormente.  Para escolher mercados específicos, escolha **Alterar mercados**.  Alterne mercados individuais para excluir cada um ou escolha **Desmarcar todos** e, em seguida, adicionar mercados individuais de sua escolha.  

> [!NOTE]
> Você pode alterar os mercados em que sua extensão é oferecida.  Um usuário que instala sua extensão enquanto ela está disponível no mercado do usuário retém o acesso à extensão.  No entanto, o usuário não tem acesso a atualizações futuras enviadas ao armazenamento de Complementos do Microsoft Edge.  

Selecione **Salvar** para continuar na **seção Propriedades.**  

#### <a name="step-4-select-properties-for-your-extension"></a>Etapa 4: Selecionar Propriedades para sua extensão  

Na página **Propriedades,** insira as informações a seguir para especificar propriedades da extensão.  As propriedades são exibidas para os usuários no armazenamento de Complementos do Microsoft Edge.  

| Nome da propriedade Extension | Descrição |  
|:--- |:--- |  
| Categoria \(obrigatório\) | A categoria que melhor descreve sua extensão.  Listar sua extensão na categoria certa ajuda os usuários a encontrar sua extensão facilmente e entender mais sobre ela.  |  
| Requisitos de política de privacidade \(obrigatório\) | Indique se sua extensão acessa, coleta ou transmite qualquer informação pessoal.  Sua extensão pode falhar na etapa de certificação se você escolher **Sim** e não fornecer `Privacy policy URL` um .  |  
| URL da política de privacidade | Uma URL de política de privacidade válida para comunicar como sua extensão segue as leis e regulamentos de privacidade.  Você é responsável por garantir que sua extensão siga as leis e regulamentos de privacidade.  Você também é responsável por fornecer uma URL de política de privacidade se qualquer informação pessoal estiver sendo acessada, transmitida ou coletada pela extensão.  Para determinar se sua extensão requer uma política de privacidade, navegue até o Contrato de Desenvolvedor do Microsoft Edge e as políticas de desenvolvedor de armazenamento de [complementos][MicrosoftEdgeAddonsCatalogDeveloperPolicies]do Microsoft [Edge.][MicrosoftAppDeveloperAgreement]  |  
| URL do site | Uma página da Web que fornece informações adicionais sobre sua extensão.  O deve apontar para uma página em seu próprio site, não a listagem da Web para sua extensão no armazenamento `Website URL` de complementos do Microsoft Edge.  O `Website URL` ajuda os usuários a saber mais sobre sua extensão, seus recursos e quaisquer outras informações relevantes.  |  
| Dar suporte aos detalhes do contato | A URL para sua página da Web de suporte ou o endereço de email para entrar em contato com sua equipe de suporte.  |  
| Conteúdo maduro | Caixa de seleção para especificar se sua extensão inclui conteúdo maduro.  A classificação de extensão ajuda a determinar a faixa etária apropriada do público-alvo da extensão.  Para ajudar a determinar se sua extensão tem conteúdo maduro, navegue até [Microsoft Edge Add-ons store developer policies][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Escolha **Salvar** para continuar na **seção Listagens da** Loja.  

> [!Important]
> O nome do desenvolvedor/organização, a URL do site e os detalhes de contato de suporte que você enviou durante o registro são exibidos para os usuários no armazenamento de Complementos do Microsoft Edge.  

#### <a name="step-5-add-store-listing-details-for-your-extension"></a>Etapa 5: Adicionar detalhes de listagem da Loja para sua extensão  

As informações fornecidas na seção a seguir são exibidas para os usuários que revisam sua listagem no armazenamento de complementos do Microsoft Edge.  Mesmo que alguns campos sejam opcionais, você deve fornecer o máximo de informações possível.  Para listar sua extensão na loja, os detalhes a seguir são necessários.  

*   **Descrição** de cada idioma no pacote de extensão.  
*   **Logotipo da Loja de Extensão** para cada idioma no pacote de extensão.  
    
> [!NOTE]
> Os detalhes mínimos de listagem de armazenamento necessários devem ser preenchidos para pelo menos um dos idiomas mencionados no pacote zip de extensão.  Para adicionar ou remover idiomas na listagem da loja no armazenamento de Complementos do Microsoft Edge, use **a** lista suspenso Adicionar um idioma na página **Listagens da** Loja.  Além disso, você pode optar por duplicar seus ativos de um idioma entre outros usando o botão de funcionalidade duplicada na página detalhes do idioma.  

| Nome da propriedade De detalhes do idioma | Descrição |  
|:--- |:--- |  
| Nome de exibição \(obrigatório\) | A `name` da extensão especificada no arquivo de manifesto da extensão.  Para alterar o nome de exibição da loja após o envio, você pode atualizar o nome no arquivo de manifesto, criar um novo pacote de extensão e, em seguida, recarregá-lo.  |  
| Descrição \(obrigatório\) | O campo se concentra em explicar o que sua extensão faz, por que os usuários devem instalá-la ou outras informações relevantes que os `description` usuários precisam saber.  Deve ter menos de 10.000 caracteres.  |  
| Logotipo da Loja de Extensões \(obrigatório\) | Uma imagem que representa sua empresa ou com uma taxa de proporção de 1 e tamanho recomendado `extension logo` de 300 x 300 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado seguindo o campo depois que você carrega seu logotipo para o idioma.  |  
| Pequeno azulejo promocional \(opcional\) | A `Small promotional tile` imagem é usada para exibir sua extensão junto com outras extensões na loja.  O tamanho da imagem deve ser de 440 x 280 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado seguindo o campo após carregar um pacote promocional para o idioma.  |  
| Capturas de tela \(opcional\) | Você pode enviar no máximo 10 descrevendo a `screenshots` funcionalidade de sua extensão em detalhes.  O tamanho das capturas de tela deve ser de 640 x 480 pixels ou 1280 x 800 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado seguindo o campo após carregar pelo menos um para o idioma.|  
| Grande azulejo promocional \(opcional\) | `Large promotion tiles` são usados na loja para extensões de recursos com mais destaque no site de complementos do Microsoft Edge.  As imagens, se enviadas, ficam visíveis para os usuários.  O tamanho dos arquivos PNG deve ser de 1400 x 560 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado seguindo o campo após carregar um pacote promocional para o idioma.  |  
| URL de vídeo do YouTube \(opcional\) | Você pode incluir um vídeo promocional do YouTube da extensão.  O vídeo é exibido na página de listagem da loja `YouTube video URL` da extensão.  |  
| Descrição curta \(obrigatório\) | Para editar o , você deve atualizar o campo de descrição no arquivo de manifesto do pacote de extensão e `short description` recarregá-lo.  |  
| Termos de pesquisa \(opcional\) | `Search terms` são palavras ou frases simples que ajudam os usuários a descobrir sua extensão ao pesquisar no armazenamento de Complementos do Microsoft Edge.  Os termos de pesquisa não são exibidos para os usuários.  |  

##### <a name="youtube-video-url-requirements"></a>Requisitos de URL de vídeo do YouTube  

Verifique se o vídeo atende aos seguintes requisitos.  

*   Verifique se o conteúdo do vídeo do YouTube segue as Políticas de Desenvolvedor do Armazenamento de Complementos do [Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Desativar anúncios em seu vídeo.  Para obter mais informações, navegue até [Definir seus formatos de anúncio padrão][GoogleYoutubeAnswer2531367Topic7072227] e Anúncios em vídeos [incorporados.][GoogleYoutubeAnswer132596]  
*   Ativar a incorporação para seus vídeos.  Para obter mais informações, navegue até [Incorporar vídeos & playlists][GoogleYoutubeAnswer171780].  
    
Para enviar a URL de vídeo do YouTube do seu vídeo, conclua as etapas a seguir.  

1.  No YouTube, localize o vídeo que você deseja adicionar à página de listagem da loja.  
1.  No vídeo, escolha **Compartilhar**  >  **Incorporar**.  
1.  Copie o código HTML exibido.  
1.  Na página de detalhes de listagem da loja, colar o código HTML no `YouTube video URL` campo.  
    
##### <a name="search-terms-requirements"></a>Requisitos de termos de pesquisa  

Os termos de pesquisa devem atender aos seguintes requisitos.  

*   Você pode inserir termos de pesquisa para usar até um máximo de 21 palavras.  Se for usado como palavras simples, frases ou uma combinação de ambas, você só tem permissão para um máximo de 21 palavras.  
*   Até um máximo de sete termos de pesquisa: palavras ou frases simples.  Cada termo de pesquisa tem um limite de caracteres de 30 caracteres.  
    
#### <a name="step-6-complete-your-submission"></a>Etapa 6: Concluir seu envio  

Na página **Enviar sua extensão,** adicione anotações para certificação para ajudar a testar sua extensão.  

##### <a name="notes-for-certification-optional"></a>Notas para certificação (Opcional)  

Ao enviar sua extensão, use a página **Notas para** certificação para fornecer informações adicionais aos testadores de certificação.  As informações adicionais ajudam a garantir que sua extensão seja testada corretamente.  Se a extensão não for totalmente testada, ela poderá falhar na certificação.  

Certifique-se de incluir as informações a seguir, conforme necessário.  

*   Nomes de usuário e senhas para contas de teste.  
*   Etapas para acessar recursos ocultos ou bloqueados.  
*   Diferenças esperadas na funcionalidade com base na região ou em outras configurações do usuário.  
*   Se o envio for uma atualização para uma extensão existente, inclua informações sobre as alterações feitas na extensão.  
*   Qualquer informação adicional que os testadores devem entender sobre seu envio.  

Depois de fornecer as informações, escolha **Publicar** para enviar sua extensão para o armazenamento de Complementos do Microsoft Edge.  Seu envio segue para a etapa de certificação.  O processo de certificação pode levar até sete dias úteis após o envio.  

Quando seu envio passa na certificação, sua extensão é publicada no armazenamento de Complementos do Microsoft Edge.  O status da extensão no painel do Partner Center muda para `In the Store` .  

> [!NOTE]
> Se você encontrar algum problema no processo de envio ou registro, envie um tíquete de suporte em [Extensões][ExtensionsSupportForm] Nova Solicitação de Suporte ou envie um email para ext_dev_support@microsoft.com [.][MailtoExtDevSupportMicrosoftCom]  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Iniciando com extensões do Microsoft Edge (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registre-se como desenvolvedor de extensões do Microsoft Edge | Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Port your Chromium extension to Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Os Complementos do Microsoft Edge armazenam políticas de desenvolvedor | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de Desenvolvedor de Aplicativos | Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensões Nova Solicitação de Suporte | Suporte da Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Definir seus formatos de | Ajuda do YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anúncios em vídeos incorporados | Ajuda do YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Incorporar vídeos & listas de reprodução | Ajuda do YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Enviar email para ext_dev_support@microsoft.com" 
