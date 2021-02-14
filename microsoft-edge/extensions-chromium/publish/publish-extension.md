---
description: Publicar extensões do Microsoft Edge (Chromium) na Loja de complementos do Microsoft Edge
title: Publicar sua extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: b03a74d1faef914298729020e3c9ca4d465e0443
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327671"
---
# Publicar sua extensão  

Depois de desenvolver e testar sua extensão, você estará pronto para distribuir sua extensão. Use o catálogo de complementos do Microsoft Edge para distribuir sua extensão.  Para liberar sua extensão Chromium existente para usuários do Microsoft Edge, navegue para por [a portabilidade da extensão Chromium existente.][PortChromiumExtension]  

Publique sua extensão no catálogo de complementos do Microsoft Edge para aumentar o alcance dela e torná-la disponível para os usuários do Microsoft Edge.  Este artigo fornece o processo para enviar sua extensão ao catálogo de complementos do Microsoft Edge.  

## Antes de começar  

Você deve ter um protótipo de trabalho de sua extensão pronta.  Para obter informações sobre como criar uma extensão, consulte o [tutorial de introdução.][ExtensionsGettingStarted]  

Para publicar sua extensão no catálogo de complementos do Microsoft Edge, use sua conta de desenvolvedor ativa no [Partner Center.][MicrosoftPartnerCenter]  Se você não tiver uma conta de desenvolvedor, crie uma nova conta de desenvolvedor.  Para abrir uma nova conta de desenvolvedor e registrar-se no programa de complementos do Microsoft Edge, navegue até [Registro do desenvolvedor.][DeveloperRegistration]  

Crie um arquivo zip que representa seu pacote de extensão.  Seu pacote de extensão deve incluir os arquivos a seguir.  

*   O manifesto da extensão especificando detalhes como o nome da extensão, descrição curta, permissões e idioma padrão.  
*   Imagens e outros arquivos exigidos pela extensão.  

Os campos a seguir no manifesto são incluídos automaticamente nos detalhes de listagem da loja.  Os campos são somente leitura na página **listagens da** Loja.  A página de listagens da loja é descrita posteriormente neste artigo.  Certifique-se de que os valores do campo corresponderão à sua exibição preferida na página de detalhes da loja antes de carregar o pacote no Partner Center.  Para um exemplo do código necessário para o arquivo de manifesto, revise as noções básicas do arquivo de manifesto.  

*   `Name` no arquivo de manifesto, que é o nome **para exibição** na página de detalhes do armazenamento.  
*   `Description` no arquivo de manifesto, que é a **descrição Curta** na página de detalhes do armazenamento.  Forneça uma descrição curta e captura para exibir na parte superior da listagem da extensão.  Quando incluída, a breve descrição especificada no arquivo de manifesto da extensão é exibida na listagem da loja.  Se uma breve descrição não estiver incluída no arquivo de manifesto, as primeiras linhas de Descrição serão exibidas.  Forneça uma breve descrição para evitar a repetição de conteúdo na página de listagem da Loja.  

## Enviar sua extensão para o armazenamento de complementos do Microsoft Edge  

Para enviar sua extensão para [o Partner Center,][MicrosoftPartnerCenter]use as etapas a seguir.  

#### Etapa 1: Iniciar um novo envio  

Navegue até o [painel do desenvolvedor][MicrosoftPartnerCenter] e escolha Criar nova **extensão** na página **Visão** Geral.  

#### Etapa 2: Carregar o pacote de extensão  

Use a **página Pacotes** para carregar o arquivo zip do pacote de extensão.  Você só pode carregar um pacote de cada vez.  Você não poderá continuar com o envio se o carregamento do pacote não for bem-sucedido na página **Pacotes.**  

Para carregar o pacote, escolha e arraste o pacote para o campo de carregamento. Você também pode escolher **Procurar seus arquivos.**  Depois que o pacote é carregado, seu pacote é validado.  Depois que a validação for bem-sucedida, revise os detalhes da extensão e escolha **Próximo** para continuar.  Se houver erros de validação, resolva os problemas e tente carregar novamente.  

#### Etapa 3: Fornecer detalhes de disponibilidade  

Na página **Disponibilidade,** insira as seguintes informações sobre a disponibilidade da extensão.  

##### Visibilidade  

Escolha uma das seguintes opções de visibilidade para definir se sua extensão pode ser descoberta no catálogo de complementos do Microsoft Edge.  

*   `Public` \(padrão\)  
    O público permite que todos descubram sua extensão por meio de pesquisa, navegação no catálogo de complementos do Microsoft Edge ou uso da URL de listagem para sua extensão no armazenamento de complementos do Microsoft Edge.  A URL de listagem está disponível no painel do Partner Center na página Visão Geral **da Extensão.**  
    
*   `Hidden`  
    Oculto remove extensões dos resultados da pesquisa ou navegação no catálogo de complementos do Microsoft Edge.  Para distribuir extensões ocultas no armazenamento de complementos do Microsoft Edge, você deve compartilhar a URL de listagem para a extensão com seus clientes.  
    
> [!NOTE]
> Você pode alterar a visibilidade de sua extensão de **Público** para **Oculto.**  Os usuários que instalaram sua extensão enquanto a visibilidade estava definida como pública retêm o acesso à extensão e recebem as atualizações disponibilizadas por meio do site de complementos do Microsoft Edge.  

##### Mercados  

Defina os mercados específicos nos quais você planeja oferecer sua extensão.  A configuração padrão para mercados é todos os mercados e que inclui quaisquer mercados futuros adicionados posteriormente.  Para escolher mercados específicos, escolha **Alterar mercados.**  Alterne os mercados individuais para excluir cada um deles ou escolha Desmarcar **tudo** e, em seguida, adicionar mercados individuais de sua escolha.  

> [!NOTE]
> Você pode alterar os mercados em que sua extensão é oferecida.  Um usuário que instala sua extensão enquanto ela está disponível no mercado do usuário retém o acesso à extensão.  No entanto, o usuário não tem acesso a atualizações futuras enviadas ao catálogo de complementos do Microsoft Edge.  

Selecione **Salvar** para continuar na **seção** Propriedades.  

#### Etapa 4: Selecionar propriedades para sua extensão  

Na página **Propriedades,** insira as informações a seguir para especificar as propriedades da extensão.  As propriedades são exibidas para os usuários no catálogo de complementos do Microsoft Edge.  

| Nome da propriedade extension | Descrição |  
|:--- |:--- |  
| Category \(required\) | A categoria que melhor descreve sua extensão.  Listar sua extensão na categoria certa ajuda os usuários a encontrar sua extensão facilmente e a entender mais sobre ela.  |  
| Requisitos de política de privacidade \(obrigatório\) | Indica se sua extensão acessa, coleta ou transmite qualquer informação pessoal.  Sua extensão poderá falhar na etapa de certificação se você escolher **Sim** e não fornecer um `Privacy policy URL` .  |  
| URL da política de privacidade | Uma URL de política de privacidade válida para comunicar como sua extensão segue as leis e regulamentos de privacidade.  Você é responsável por garantir que sua extensão siga as leis e regulamentos de privacidade.  Você também é responsável por fornecer uma URL de política de privacidade se qualquer informação pessoal estiver sendo acessada, transmitida ou coletada por sua extensão.  Para determinar se sua extensão requer uma política de privacidade, navegue até o Contrato de Desenvolvedor do [Microsoft Edge][MicrosoftAppDeveloperAgreement] e as políticas de desenvolvedor do catálogo de [complementos do Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  
| URL do site | Uma página da Web que fornece informações adicionais sobre sua extensão.  Deve apontar para uma página em seu próprio site, não para a listagem da Web para sua extensão no catálogo de `Website URL` complementos do Microsoft Edge.  Ajuda `Website URL` os usuários a saber mais sobre sua extensão, seus recursos e outras informações relevantes.  |  
| Detalhes do contato de suporte | A URL da página da Web de suporte ou o endereço de email para entrar em contato com a equipe de suporte.  |  
| Conteúdo mais adulto | Caixa de seleção para especificar se sua extensão inclui conteúdo adulto.  A classificação de extensão ajuda a determinar a faixa etária apropriada do público-alvo de sua extensão.  Para ajudar a determinar se sua extensão tem conteúdo adulto, navegue até as políticas de desenvolvedor do catálogo de [complementos do Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  

Selecione **Salvar** para continuar na seção **listagens da** Loja.  

> [!Important]
> O nome do desenvolvedor/organização, a URL do site e os detalhes de contato de suporte enviados durante o registro são exibidos aos usuários na loja de complementos do Microsoft Edge.  

#### Etapa 5: Adicionar detalhes de listagem da Loja para sua extensão  

As informações fornecidas na seção a seguir são exibidas aos usuários que revisam sua listagem no catálogo de complementos do Microsoft Edge.  Embora alguns campos sejam opcionais, você deve fornecer o máximo de informações possível.  Para listar sua extensão na loja, os seguintes detalhes são necessários.  

*   **Descrição** de cada idioma no pacote de extensão.  
*   **Logotipo da Loja de** Extensões para cada idioma no pacote de extensão.  
    
> [!NOTE]
> Os detalhes mínimos necessários de listagem da loja devem ser preenchidos para pelo menos um dos idiomas mencionados no pacote zip de extensão.  Para adicionar ou remover idiomas na listagem da Loja no catálogo de complementos do Microsoft Edge, use **o** menu suspenso Adicionar um idioma na página **listagens da** Loja.  Além disso, você pode optar por duplicar seus ativos de um idioma em outros usando o botão de funcionalidade duplicada na página de detalhes do idioma.  

| Nome da propriedade de detalhes do idioma | Descrição |  
|:--- |:--- |  
| Nome de exibição \(obrigatório\) | A `name` extensão especificada no arquivo de manifesto da extensão.  Para alterar o nome de exibição da loja após o envio, você pode atualizar o nome no arquivo de manifesto, criar um novo pacote de extensão e, em seguida, recarregá-lo.  |  
| Descrição \(obrigatório\) | O campo se concentra em explicar o que sua extensão faz, por que os usuários devem instalá-la ou outras informações relevantes `description` que os usuários precisam saber.  Deve ter menos de 10.000 caracteres.  |  
| Logotipo do Extension Store \(required\) | Uma imagem que representa sua empresa ou com uma taxa de proporção de 1 e tamanho recomendado de `extension logo` 300 x 300 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado após o campo depois que você carrega seu logotipo para o idioma.  |  
| Small promotional tile \(optional\) | A `Small promotional tile` imagem é usada para exibir sua extensão junto com outras extensões na loja.  O tamanho da imagem deve ser 440 x 280 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado após o campo depois que você carrega um pacote promocional para o idioma.  |  
| Capturas de tela \(opcional\) | Você pode enviar no máximo 10 descrevendo a `screenshots` funcionalidade de sua extensão em detalhes.  O tamanho das capturas de tela deve ser 640 x 480 pixels ou 1280 x 800 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado após o carregamento de pelo menos um para o idioma.|  
| Large promotional tile \(optional\) | `Large promotion tiles` são usadas na loja para apresentar extensões com mais destaque no site de complementos do Microsoft Edge.  As imagens, se enviadas, ficam visíveis para os usuários.  O tamanho dos arquivos PNG deve ser de 1400 x 560 pixels.  Além disso, você pode optar por copiar o ativo de um idioma para todos os outros idiomas usando o botão duplicado.  O botão é encontrado após o campo depois que você carrega um pacote promocional para o idioma.  |  
| URL de vídeo do YouTube \(opcional\) | Você pode incluir um vídeo promocional do YouTube de sua extensão.  O `YouTube video URL` vídeo é exibido na página de listagem da loja da extensão.  |  
| Descrição curta \(obrigatório\) | Para editar o `short description` campo , você deve atualizar o campo de descrição no arquivo de manifesto do pacote de extensão e recarregá-lo.  |  
| Termos de pesquisa \(opcional\) | `Search terms` são palavras ou frases individuais que ajudam os usuários a descobrir sua extensão ao pesquisar no Catálogo de Complementos do Microsoft Edge.  Os termos de pesquisa não são exibidos aos usuários.  |  

##### Requisitos de URL de vídeo do YouTube  

Verifique se o vídeo atende aos requisitos a seguir.  

*   Verifique se o conteúdo do vídeo do YouTube segue as Políticas de Desenvolvedor do Catálogo de Complementos do [Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Desativar anúncios em seu vídeo.  Para obter mais informações, navegue [até Definir os formatos de anúncio padrão][GoogleYoutubeAnswer2531367Topic7072227] e anúncios em vídeos [incorporados.][GoogleYoutubeAnswer132596]  
*   Ativar a incorporação de seus vídeos.  Para obter mais informações, navegue [até Inserir vídeos & playlists][GoogleYoutubeAnswer171780].  
    
Para enviar a URL de vídeo do YouTube do seu vídeo, conclua as etapas a seguir.  

1.  No YouTube, localize o vídeo que você deseja adicionar à página de listagem da Loja.  
1.  Under the video, choose **Share**  >  **Embed**.  
1.  Copie o código HTML exibido.  
1.  Na página de detalhes de listagem da loja, colar o código HTML no `YouTube video URL` campo.  
    
##### Requisitos de termos de pesquisa  

Os termos de pesquisa devem atender aos seguintes requisitos.  

*   Você pode inserir termos de pesquisa para usar no máximo 21 palavras.  Seja usado como palavras únicas, frases ou uma combinação de ambos, você só tem permissão para no máximo 21 palavras.  
*   Até um máximo de sete termos de pesquisa: palavras ou frases individuais.  Cada termo de pesquisa tem um limite de caracteres de 30 caracteres.  
    
#### Etapa 6: Concluir seu envio  

Na página **Enviar sua extensão,** adicione notas de certificação para ajudar a testar sua extensão.  

##### Notas para certificação (opcional)  

Ao enviar sua extensão, use a página **Notas para certificação** para fornecer informações adicionais aos testadores de certificação.  As informações adicionais ajudam a garantir que sua extensão seja testada corretamente.  Se a extensão não for totalmente testada, ela poderá falhar na certificação.  

Certifique-se de incluir as informações a seguir, conforme necessário.  

*   Nomes de usuário e senhas para contas de teste.  
*   Etapas para acessar recursos ocultos ou bloqueados.  
*   Diferenças esperadas na funcionalidade com base na região ou em outras configurações do usuário.  
*   Se o envio for uma atualização para uma extensão existente, inclua informações sobre as alterações feitas na extensão.  
*   Qualquer informação adicional que os testadores devem entender sobre seu envio.  

Depois de fornecer as informações, escolha **Publicar** para enviar sua extensão ao catálogo de complementos do Microsoft Edge.  Seu envio prosseguirá para a etapa de certificação.  O processo de certificação pode levar até sete dias úteis após o envio.  

Quando seu envio for aprovado na certificação, sua extensão será publicada no catálogo de complementos do Microsoft Edge.  O status da extensão no painel do Partner Center muda para `In the Store` .  

> [!NOTE]
> Se você encontrar algum problema no processo de envio [][ExtensionsSupportForm] ou registro, envie um tíquete de suporte na Solicitação de Suporte de Novas Extensões ou envie um email para [ext_dev_support@microsoft.com.][MailtoExtDevSupportMicrosoftCom]  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Como começar a trabalhar com extensões do Microsoft Edge (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registre-se como um desenvolvedor de extensões do Microsoft Edge | Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Fazer a portabilidade da extensão Chromium para o Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Políticas de Desenvolvedor do Catálogo de Complementos do Microsoft Edge | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de Desenvolvedor de Aplicativos | Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Solicitação de Novo Suporte de Extensões | Suporte da Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Definir os formatos de | Ajuda do YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anúncios em vídeos incorporados | Ajuda do YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Incorporar vídeos & playlists | Ajuda do YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Enviar email para ext_dev_support@microsoft.com" 
