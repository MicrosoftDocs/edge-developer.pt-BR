---
description: Publicar extensões do Microsoft Edge (Chromium) no repositório de Complementos do Microsoft Edge.
title: Publicar sua extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 4f8433e74c0fd6dab3278792b94cf3cbaac05d2c
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015748"
---
# Publicar sua extensão  

Depois de concluir o desenvolvimento e o teste da extensão, talvez você esteja pronto para distribuir a extensão usando o catálogo de Complementos do Microsoft Edge.  Como alternativa, se você tiver uma extensão existente do Chromium que você deseja disponibilizar para os usuários do Microsoft Edge, você poderá [portar sua extensão Chromium existente][PortChromiumExtension] para o Microsoft Edge.  

A publicação da extensão no catálogo de Complementos do Microsoft Edge aumenta o alcance da extensão e a disponibiliza para usuários finais.  Este tópico fornece um guia passo a passo do processo para enviar sua extensão ao catálogo de Complementos do Microsoft Edge.  

## Antes de começar  

Nesse ponto, você deve ter um protótipo funcional da sua extensão pronto.  Para obter informações sobre como criar uma extensão, consulte o [tutorial de introdução][ExtensionsGettingStarted].  

Para publicar sua extensão no site de Complementos do Microsoft Edge, você deve ter uma conta de desenvolvedor ativa no [centro de parceiros][MicrosoftPartnerCenter].  Para abrir uma nova conta de desenvolvedor e se registrar no programa Complementos do Microsoft Edge, siga o processo mencionado no guia de [registro do desenvolvedor][DeveloperRegistration] .  

Crie um arquivo zip que represente o pacote de extensão.  O pacote de extensão deve incluir os arquivos a seguir.  

*   O manifesto de extensão especificando detalhes como o nome da extensão, a descrição curta, as permissões e o idioma padrão.  
*   Imagens e outros arquivos exigidos pela extensão.  

Os campos a seguir no manifesto são incluídos automaticamente nos detalhes da listagem da loja e não podem ser modificados na página de listagens da loja, que é descrita posteriormente neste tópico.  Verifique se os campos estão preenchidos para corresponder à exibição preferida na página de detalhes da loja, antes de carregar o pacote para a central de parceiros.  Para obter um exemplo do código necessário para o arquivo de manifesto, examine as noções básicas do arquivo de manifesto.  

*   `Name` no arquivo de manifesto, que é o **nome para exibição** na página de detalhes da loja.  
*   `Description` no arquivo de manifesto, que é a **breve descrição** da página de detalhes da loja.  Forneça uma descrição rápida e curta para ser exibida na parte superior da listagem para a sua extensão.  Quando incluído, a breve descrição especificada no arquivo de manifesto da extensão é exibida na listagem da loja.  Se uma breve descrição não estiver incluída no arquivo de manifesto, as primeiras linhas de descrição serão exibidas.  Você deve fornecer uma breve descrição para evitar a repetição do conteúdo na página de listagem da loja.  

## Enviar sua extensão ao repositório de Complementos do Microsoft Edge  

Para enviar sua extensão ao [Partner Center][MicrosoftPartnerCenter], use as etapas a seguir.  

#### Etapa 1: iniciar um novo envio  

Vá para o [painel do desenvolvedor][MicrosoftPartnerCenter] e selecione **criar nova extensão** na página **visão geral** .  

#### Etapa 2: carregar o pacote de extensão  

Use a página **pacotes** para carregar o arquivo zip do seu pacote de extensão.  Você só pode carregar um pacote de cada vez.  Você não poderá continuar com o envio se o carregamento do pacote não for bem-sucedido na página **pacotes** .  

Carregue o pacote arrastando o pacote para o campo de carregamento ou selecionando **procurar seus arquivos**.  Depois que o pacote for carregado, o pacote será validado.  Uma vez que a validação seja bem-sucedida, examine os detalhes da extensão e selecione **Avançar** para continuar.  Se houver erros de validação, resolva os problemas e tente carregar novamente.  

#### Etapa 3: fornecer detalhes de disponibilidade  

Na página **disponibilidade** , insira as informações a seguir sobre a disponibilidade de sua extensão.  

##### Visibilidade  

Escolha uma das opções de visibilidade a seguir para definir se a extensão é detectável no catálogo de Complementos do Microsoft Edge.  

*   `Public` \ (padrão \)  
    Público permite que as extensões sejam detectáveis para todos por meio de pesquisa, navegação no catálogo de Complementos do Microsoft Edge ou uso da URL de listagem para a sua extensão no repositório Complementos do Microsoft Edge.  A URL de listagem está disponível no painel do centro de parceiros na página de **visão geral** da extensão.  

*   `Hidden`  
    Oculto remove as extensões dos resultados da pesquisa ou navega no catálogo Complementos do Microsoft Edge.  Para distribuir extensões ocultas no repositório de Complementos do Microsoft Edge, você deve compartilhar a URL de listagem para a extensão com seus clientes.  

> [!NOTE]
> Você pode alterar a visibilidade de sua extensão de **Public** para **Hidden**.  Os usuários que instalaram sua extensão enquanto a visibilidade foram definidas como Public retenham o acesso à sua extensão e recebem todas as atualizações disponibilizadas por meio do site de Complementos do Microsoft Edge.  

##### Mercados  

Defina os mercados específicos nos quais você planeja oferecer a extensão.  Por padrão, todos os mercados foram selecionados, incluindo todos os futuros mercados que forem adicionados mais tarde.  Se preferir, escolha mercados específicos selecionando **alterar mercados**.  Desmarque mercados individuais para excluí-los ou selecione **desmarcar tudo** e adicione mercados individuais à sua escolha.  

> [!NOTE]
> Você pode alterar os mercados nos quais a extensão é oferecida.  Os usuários que instalaram sua extensão enquanto estiverem disponíveis no mercado reterão acesso à sua extensão.  No entanto, os usuários não têm mais acesso a futuras atualizações enviadas ao catálogo de Complementos do Microsoft Edge.  

Selecione **salvar** para continuar na seção **Propriedades** .  

#### Etapa 4: selecionar propriedades para a extensão  

Na **página Propriedades**, insira as informações a seguir para especificar as propriedades de sua extensão.  As propriedades são exibidas para os usuários no catálogo de Complementos do Microsoft Edge.  

| Nome da propriedade da extensão | Descrição |  
|:--- |:--- |  
| Categoria \ (obrigatório \) | A categoria que melhor descreve sua extensão.  Listar a extensão na categoria certa ajuda os usuários a encontrar sua extensão facilmente e a entender mais sobre isso.  |  
| Requisitos da política de privacidade \ (obrigatório \) | Indique se sua extensão acessa, coleta ou transmite qualquer informação pessoal.  Sua extensão poderá falhar na etapa de certificação se você escolher **Sim** e não fornecer uma `Privacy policy URL` .  |  
| URL da política de privacidade | Uma URL de política de privacidade válida para comunicar como a extensão está em conformidade com as leis e regulamentos de privacidade.  Você é responsável por assegurar que sua extensão esteja em conformidade com as leis e regulamentos de privacidade, e para fornecer uma URL de política de privacidade válida, se necessário.  Forneça uma URL de política de privacidade se qualquer informação pessoal estiver sendo acessada, transmitida ou coletada pela extensão.  Para determinar se sua extensão requer uma política de privacidade, acesse [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] e [Microsoft Edge Add-Policies Catalog][MicrosoftEdgeAddonsCatalogDeveloperPolicies]Policy.  |  
| URL do site | Uma página da Web que fornece informações adicionais sobre a extensão.  O `Website URL` deve apontar para uma página em seu próprio site, não para a listagem da Web para sua extensão no catálogo de Complementos do Microsoft Edge.  O `Website URL` ajuda os usuários a saber mais sobre sua extensão, seus recursos e outras informações relevantes.  |  
| Detalhes de contato de suporte | A URL da sua página da Web de suporte ou o endereço de email para entrar em contato com a equipe de suporte.  |  
| Conteúdo maduro | Caixa de seleção para especificar se sua extensão inclui conteúdo maduro.  A classificação da extensão ajuda a determinar a faixa etária apropriada do público-alvo de sua extensão.  Para ajudar a determinar se sua extensão tem conteúdo maduro, vá para [Microsoft Edge Add-Complementos Catalog políticas de desenvolvedor][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Selecione **salvar** para continuar na seção **listagens da loja** .  

#### Etapa 5: adicionar detalhes da listagem da loja para sua extensão  

As informações fornecidas na seção a seguir são exibidas para os usuários que acessam sua lista no catálogo de Complementos do Microsoft Edge.  Embora alguns campos sejam opcionais, você deve fornecer o máximo de informações possível.  Os detalhes mínimos necessários para a sua extensão para a listagem na loja, para cada idioma mencionado em seu pacote de extensão, são **Descrição** e **logotipo da loja da extensão**.  

> [!NOTE]
> Os detalhes da listagem mínima da loja necessária devem ser preenchidos para cada idioma mencionado em seu pacote zip de extensão.  Para adicionar ou remover idiomas na lista da loja no catálogo de Complementos do Microsoft Edge, você deve modificar a lista de idiomas com suporte na sua extensão no pacote de extensão, criar um novo pacote de extensão e carregá-lo novamente.  

| Nome da propriedade da listagem da loja | Descrição |  
|:--- |:--- |  
| Idiomas de listagem da loja \ (obrigatório \) | Selecione um idioma na lista suspensa de **idiomas** e insira os detalhes da listagem da loja para esse idioma.  Extensões que dão suporte a vários idiomas devem fornecer uma página de listagem da loja para cada idioma com suporte.  |  
| Nome para exibição \ (obrigatório \) | O nome da extensão especificada no arquivo de manifesto da extensão.  Para alterar o nome de exibição da loja após o envio, você pode atualizar o nome no arquivo de manifesto, criar um novo pacote de extensão e, em seguida, carregá-lo novamente.  |  
| Descrição \ (obrigatório \) | O campo Descrição se concentra em explicar o que a extensão faz, por que os usuários devem instalá-la ou outras informações relevantes que os usuários precisam saber.  Deve ter menos de 10.000 caracteres.  |  
| Logotipo da loja de Extensões \ (obrigatório \) | Uma imagem que representa o logotipo da sua empresa ou extensão com uma taxa de proporção de 1 e o tamanho recomendado de 300 x 300 pixels.  |  
| Bloco promocional pequeno \ (opcional \) | A `Small promotional tile` imagem é usada para exibir a extensão junto a outras extensões na loja.  O tamanho da imagem deve ser 440 x 280 pixels.  |  
| Capturas de tela \ (opcional \) | Você pode enviar um máximo de 10 capturas de tela descrevendo a funcionalidade de sua extensão em detalhes.  O tamanho das capturas de tela deve ser 640 x 480 pixels ou 1280 x 800 pixels.  |  
| Bloco promocional grande \ (opcional \) | Blocos de promoção grandes são usados na loja para extensões de recursos com mais destaque no site Complementos do Microsoft Edge.  As imagens, se enviadas, são visíveis para os usuários.  O tamanho dos arquivos PNG deve ser 1400 x 560 pixels.  |  
| URL de vídeo do YouTube \ (opcional \) | Você pode incluir um vídeo do YouTube promocional da extensão.  O `YouTube video URL` vídeo é exibido na página listagem da loja da extensão.  |  
| Descrição curta \ (obrigatório \) | Para editar a descrição resumida, você deve atualizar o campo Descrição em seu arquivo de manifesto do seu pacote de extensão e carregá-lo novamente.  |  
| Termos da pesquisa \ (opcional \) | Termos de pesquisa são palavras únicas ou frases que ajudam os usuários a descobrir a extensão ao pesquisar no catálogo de Complementos do Microsoft Edge.  Os termos da pesquisa não são exibidos para os usuários.  |  

##### Requisitos de URL de vídeo do YouTube  

Certifique-se de que seu vídeo atenda aos seguintes requisitos.  

*   Verifique se o conteúdo do vídeo do YouTube está em conformidade com o tópico de [políticas de desenvolvedor de catálogo do Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies] .  
*   Desative anúncios no vídeo.  Para obter mais informações, vá para [definir seus formatos de anúncio padrão][GoogleYoutubeAnswer2531367Topic7072227] e [anúncios em vídeos inseridos][GoogleYoutubeAnswer132596].  
*   Ative a inserção para seus vídeos.  Para obter mais informações, vá para [inserir vídeos & playlists][GoogleYoutubeAnswer171780].  

Execute as etapas a seguir para enviar a URL de vídeo do YouTube do seu vídeo.  

1.  No YouTube, localize o vídeo que você deseja adicionar à sua página de listagem da loja.  
1.  Em vídeo, escolha **compartilhar**  >  **incorporar**.  
1.  Copie o código HTML que é exibido.  
1.  Na página detalhes da listagem da loja, Cole o código HTML no `YouTube video URL` campo.  

##### Requisitos de termos de pesquisa  

Os termos de pesquisa devem atender aos seguintes requisitos.  

*   Você pode inserir termos de pesquisa para usar até no máximo 21 palavras.  Seja usado como palavras únicas, frases ou uma combinação de ambas, você só pode ter no máximo 21 palavras.  
*   Até um máximo de sete termos de pesquisa: palavras ou frases individuais.  Cada termo de pesquisa tem um limite de caracteres de 30 caracteres.  

#### Etapa 6: concluir o envio  

Na página **enviar sua extensão** , adicione anotações para certificação para ajudar a testar a extensão.  

##### Notas para certificação (opcional)  

Ao enviar sua extensão, use a página **anotações para certificação** para fornecer informações adicionais aos testadores de certificação.  As informações adicionais ajudam a garantir que sua extensão seja testada corretamente.  Se a extensão não for totalmente testada, poderá falhar a certificação.  

Certifique-se de incluir as informações a seguir, conforme necessário.  

*   Nomes de usuário e senhas para contas de teste.  
*   Etapas para acessar recursos ocultos ou bloqueados.  
*   Diferenças esperadas na funcionalidade com base na região ou em outras configurações de usuário.  
*   Se o envio for uma atualização para uma extensão existente, inclua informações sobre as alterações feitas na extensão.  
*   Qualquer informação adicional que os testadores devem entender sobre o seu envio.  

Após fornecer as informações, selecione **publicar** para enviar sua extensão ao catálogo de Complementos do Microsoft Edge.  Seu envio continua até a etapa de certificação.  O processo de certificação pode levar até sete dias úteis após o envio.  

Quando o envio for aprovado na certificação, a extensão será publicada no catálogo Complementos do Microsoft Edge.  O status da sua extensão no painel do centro de parcerias muda para `In the Store` .  

> [!NOTE]
> Se você estiver enfrentando problemas no envio ou no processo de registro, envie um tíquete de suporte [aqui][ExtensionsSupportForm] ou envie um email para [ext_dev_support@microsoft.com](mailto:ext_dev_support@microsoft.com).  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introdução às extensões do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DeveloperRegistration]: ./create-dev-account.md "Cadastre-se como desenvolvedor de extensões do Microsoft Edge | Documentos da Microsoft"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Portar sua extensão do Chromium para o Microsoft Edge | Documentos da Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Políticas de desenvolvedor de catálogo de Complementos do Microsoft Edge | Documentos da Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de desenvolvedor de aplicativos | Documentos da Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Central de parceiros"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Ramais nova solicitação de suporte | Suporte da Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Definir seus formatos de anúncio padrão-ajuda do YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anúncios em vídeos inseridos-ajuda do YouTube"
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Inserir vídeos & playlists-ajuda do YouTube"  
