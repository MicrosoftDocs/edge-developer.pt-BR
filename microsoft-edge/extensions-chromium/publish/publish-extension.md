---
description: Processo passo a passo para publicar extensões Edge (Chromium) na Microsoft Store.
title: Publicar uma extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607374"
---
# Publicar uma extensão  

Publicar sua extensão no catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \).  Primeiro, você deve criar um envio no [centro de parcerias][MicrosoftPartnerCenter] e enviá-lo.  Este documento lista todos os detalhes que você deve fornecer para criar um envio de extensão.  

## Antes de começar  

*   Você deve ter uma conta de desenvolvedor ativa no [centro de parceiros][MicrosoftPartnerCenter] para enviar sua extensão em Complementos do Microsoft Edge.  Se você não tiver um, [crie uma nova conta de desenvolvedor][MicrosoftPartnerCenter].  
*   Crie um arquivo zip do seu pacote de extensão e verifique se ele contém estes arquivos:  
    *   O arquivo de manifesto e deve definir o nome e a versão de sua extensão.  
    *   As imagens e outros arquivos necessários para a extensão.  


Se você não iniciou a criação de uma extensão, talvez se refira ao tutorial de [introdução][ExtensionsGettingStarted] para a criação de uma extensão Chromium do Microsoft Edge.  

Para criar um envio de extensão no [Partner Center][MicrosoftPartnerCenter], siga estas etapas.  

## Etapa 1: iniciar um novo envio  

Acesse o [painel do desenvolvedor][MicrosoftPartnerCenter].  Na página Visão geral, clique em **criar nova extensão**.  

## Etapa 2: carregar o arquivo zip da extensão  

A página do **pacote** é onde você carrega o arquivo zip para o envio da extensão.  Você só pode carregar um pacote por vez, portanto, se sua extensão não estiver completa, você pode carregar um pacote do trabalho em andamento e atualizar a qualquer momento antes de publicá-lo.  Certifique-se de que seu pacote contém o `manifest.json` arquivo e está funcionando bem no Microsoft Edge antes de carregá-lo.  
Carregue o pacote arrastando-o para o campo de carregamento ou selecionando **procurar seus arquivos**.  A página pacote valida o arquivo zip Extensions e exibe o **status de êxito ou falha do seu carregamento**.  Se o pacote passar na validação; Ele foi carregado com êxito e você vê uma mensagem de êxito.  Se o pacote falhar na validação; o pacote não é aceito e você vê uma mensagem de erro.  Se houver erros no pacote, resolva os problemas e tente carregá-lo novamente.  

Após o upload bem-sucedido, examine os detalhes da extensão e clique em **Avançar** para continuar.  

## Etapa 3: fornecer detalhes de disponibilidade  

### Definir visibilidade  

Selecione uma opção de **visibilidade** para definir a audiência que pode descobrir e adquirir a extensão.  Isso lhe dá a opção de especificar se os usuários devem encontrar a extensão nos Complementos do Microsoft Edge ou ver a listagem.  Atualmente, você tem duas opções em visibilidade:  

*   `Public`  
    Essa é a opção padrão.  
    Se você selecionar `Public` , sua extensão estará disponível e detectável para todos os complementos do Microsoft Edge.  Deixe essa opção selecionada se desejar que a extensão seja listada nos Complementos do Microsoft Edge para os usuários encontrarem através de pesquisa, navegação e o link direto da extensão.  

*   `Hidden`  
    Se você selecionar `Hidden` , a extensão ficará oculta nos Complementos do Microsoft Edge dos usuários que estão procurando ou navegando; você deve compartilhar a URL da sua listagem para distribuir a extensão.  Os usuários que têm o link direto para a listagem podem baixá-lo no Microsoft Edge \ (talvez você encontre a URL da sua listagem na página **visão geral de extensão** do envio de extensão \).  

> [!NOTE]
> Se você enviar uma extensão como **pública** e posteriormente alterá-la para **particular**, os usuários que instalaram a extensão quando ele foi público continuarão a ter acesso e receber atualizações futuras.  

### Definir mercados  

Você deve definir os mercados específicos em que está oferecendo a extensão, selecione **Mostrar opções** na seção **mercados** na página **disponibilidade** .  A janela pop-up seleção de mercado é exibida, onde você deve escolher os mercados.  Por padrão, todos os mercados são selecionados, incluindo quaisquer **mercados futuros** que possam ser adicionados mais tarde.  Você pode cancelar a seleção de mercados individuais para excluí-los, ou pode clicar em **desmarcar tudo** e adicionar mercados individuais à sua escolha.  

> [!NOTE]
> Se os usuários já tiverem a extensão em um determinado mercado e você remover esse mercado posteriormente, os usuários que já tiverem a extensão nesse mercado poderão continuar a usá-lo, mas não receberão as atualizações posteriores que você enviar.  

Clique em **salvar** para ir para a seção **Propriedades** .  

## Etapa 4: selecionar propriedades para a extensão  

### Propriedades de extensão  

*   [Categoria](#category)  
*   [Requisitos da política de privacidade](#privacy-policy-requirements)  
*   [URL da política de privacidade](#privacy-policy-url)  
*   [URL do site](#website-url)  
*   [URL de suporte/endereço de email](#support-urlemail-address)  
*   [Classificação de extensão](#extension-rating)  

#### Categoria  

Listar a extensão na categoria certa ajuda os usuários a encontrar sua extensão facilmente e a entender mais sobre isso.  Selecione uma categoria que melhor descreva a extensão.  

**Valores possíveis**:  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### Requisitos da política de privacidade  

Indique se sua extensão acessa, coleta ou transmite qualquer informação pessoal.  

> [!NOTE]
> Se a sua extensão exigir uma política de privacidade e você não tiver fornecido uma, seu envio poderá falhar na certificação.  

**Valores possíveis**:  

*   `No`: Uma URL de política de privacidade é opcional.  
*   `Yes`: É preciso uma URL de política de privacidade.  

#### URL da política de privacidade  

Você é responsável por assegurar que sua extensão esteja em conformidade com as leis e regulamentos de privacidade, e para fornecer uma URL de política de privacidade válida, se necessário.  Você deve fornecer uma URL de política de privacidade se qualquer informação pessoal estiver sendo acessada, transmitida ou coletada pela extensão.  
Para determinar se sua extensão requer uma política de privacidade, examine o [contrato de desenvolvedor do Microsoft Edge][MicrosoftAppDeveloperAgreement] e o [documento de políticas de desenvolvimento de catálogos de Complementos do Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valores possíveis**:  

*   `{url}`  

#### URL do site  

Essa propriedade é opcional.  
A URL da página da Web para sua extensão.  Esta URL deve apontar para uma página em seu próprio site, não para a listagem da Web para sua extensão nos Complementos do Microsoft Edge.  

**Valores possíveis**:  

*   `{url}`  

#### URL de suporte/endereço de email  

Essa propriedade é opcional.  
A URL da página da Web em que os usuários vão para dar suporte à sua extensão ou a um endereço de email para o contatarem para obter suporte.  Você inclui informações de suporte para todos os envios, para que seus usuários saibam como obter suporte de você.  

**Valores possíveis**:  

*   `{email_address}`  
*   `{url}`  

#### Classificação de extensão  

A classificação da extensão nos ajuda a determinar a idade do público-alvo da sua extensão.  
Para ajudá-lo a determinar se suas extensões têm um conteúdo maduro, examine o [documento de políticas de desenvolvimento de catálogos de Complementos do Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valores possíveis**:  

*   Adulto \ (caixa de seleção \): Marque esta caixa se sua extensão contiver qualquer conteúdo maduro.  Se você selecionar adulto para a sua extensão, sua listagem estará disponível com uma marca separada para indicar que a extensão contém conteúdo maduro.  

Clique em **salvar** para passar para a seção de listagem.  

## Etapa 5: adicionar informações de listagens para a extensão  

Estas são as informações que os usuários visualizam ao exibir sua listagem em Complementos do Microsoft Edge.  Muitos dos campos em uma listagem são opcionais, mas sugerimos fornecer o máximo de informações possível para destacar a sua listagem.  O mínimo necessário para sua listagem nos Complementos do Microsoft Edge ser considerado concluído é a [Descrição do texto](#description), o [logotipo da extensão](#store-logo)e o [bloco promocional pequeno](#small-promotional-tile) em cada idioma mencionado em seu pacote de extensão.  

### Campos de listagem da loja  

*   [Idiomas da listagem da Loja](#store-listing-languages)  
*   [Nome de exibição da loja](#store-display-name)  
*   [Descrição](#description)  
*   [Logotipo da loja](#store-logo)  
*   [Bloco promocional pequeno](#small-promotional-tile)  
*   [Mídia](#media)  
*   [Descrição breve](#short-description)  
*   [Termos de pesquisa](#search-terms)  

#### Idiomas da listagem da Loja  

Se o pacote de extensão oferecer suporte a vários idiomas, a extensão deverá ter uma página de listagem para cada um deles.  
Você deve preencher detalhes da lista \ (descrição de texto, imagens e assim por diante \) para cada idioma separadamente, mesmo se estiver usando o mesmo conteúdo para cada idioma.  Se a extensão for localizada em mais de um idioma, esses idiomas serão exibidos na parte superior da página de listagem.  

1.  Selecione um nome de idioma na lista suspensa **idiomas** .  
1.  Preencha os detalhes da listagem.  
1.  Clique em **Salvar**.  
1.  Repita o procedimento para todos os seus idiomas suportados.  

> [!NOTE]
> Para adicionar ou remover idiomas para sua listagem nos Complementos do Microsoft Edge, você deve modificar a lista de idiomas com suporte no seu pacote de extensão e carregá-lo novamente.  

**Valores possíveis**:  

*   `English (United States)`: Esse é o valor padrão.  Se você não mencionar qualquer idioma em seu pacote, definimos seu idioma padrão para inglês \ (Estados Unidos \) e você deve fornecer uma listagem em inglês \ (Estados Unidos \).  
*   `{language}` \(`{Country}`\)  

#### Nome de exibição da loja  

O nome da extensão conforme mencionado no manifesto do pacote de extensão.  

> [!NOTE]
> Para editar o nome, você deve atualizar o manifesto em seu pacote de extensão e carregá-lo novamente.  

#### Descrição  

Este campo é obrigatório.  
A descrição para seus usuários do que sua extensão faz.  

**Valores possíveis**:  

*   {plain_text}: menos de 10.000 caracteres.  

#### Logotipo da loja  

Este campo é obrigatório.  
Uma imagem do 1:1 para o seu logotipo de extensão.  

**Valores possíveis**:  

*   128px x 128px, PNG \ (. png \)  
*   150px x 140px, PNG \ (. png \)  
*   300px x 300px, PNG \ (. png \): o tamanho recomendado.  

#### Bloco promocional pequeno  

Este campo é obrigatório.  
Um bloco promocional de tamanho pequeno.  Sua listagem será exibida neste bloco.  

**Valores possíveis**:  

*   440px x 280X, PNG \ (. png \)  

#### Mídia  

Este campo é opcional.  
Você deve fornecer esses ativos para ajudar a exibir seu produto com mais eficiência.  

*   Capturas de tela  
    As imagens da extensão que descrevem o que a extensão faz.  
    
*   Blocos de promoção grandes  
    Um bloco promocional grande para apresentar a extensão mais proeminente em Complementos do Microsoft Edge.  
    
*   URL de vídeo do YouTube  
    Uma [URL de vídeo do YouTube válida para a extensão][MicrosoftEdgeAddonsUploadYouTubeVideo].  Seu vídeo deve ter uma boa qualidade e comprimento mínimo.  Seu vídeo do YouTube deve passar certificação antes de publicar sua extensão nos Complementos do Microsoft Edge.  Verifique se o seu vídeo do YouTube está de acordo com o [documento de políticas de desenvolvimento de catálogos de Complementos do Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valores possíveis**:  

*   10 capturas de tela no máximo.  
    *   640 PX x 480px, PNG \ (. png \): capturas de tela.  
    *   1280px x 800px, PNG \ (. png \): capturas de tela.  
*   1400px x 560px, PNG \ (. png \): blocos grandes de promoção.  
*   60 segundos ou mais curto e 2 GB ou menor, URL de vídeo do YouTube.  

#### Descrição breve  

Uma descrição curta e curta que pode ser usada na parte superior da listagem do seu produto.  Se não for fornecido, as primeiras linhas da descrição mais longa serão usadas em vez disso.  Como a descrição também aparece abaixo desse texto, você deve fornecer uma breve descrição com texto diferente para que sua listagem seja menos repetitiva.  A breve descrição da extensão é separada diretamente do arquivo de manifesto do pacote.  

> [!NOTE]
> Para editar a descrição resumida, você deve atualizar o manifesto em seu pacote de extensão e carregá-lo novamente.  

#### Termos de pesquisa  

Termos de pesquisa são palavras únicas ou frases curtas que não são exibidas para os usuários, mas ajudam a torná-la detectável nos Complementos do Microsoft Edge quando os usuários pesquisam usando esses termos.  

**Requisitos**:  

*   7 ou menos termos de pesquisa  
*   30 ou menos caracteres por termo de pesquisa  
*   21 ou menos palavras para termos de pesquisa combinados  

Clique em **salvar** para continuar para salvar a seção de listagem.  Clique em **publicar** para fornecer detalhes de envio.  

## Etapa 6: concluir o envio e clicar em publicar  

A página opções de envio do processo de envio de extensão é onde você fornece mais informações para nos ajudar a testar o produto corretamente.  Essa é uma etapa opcional, mas é recomendável para muitos envios.  

### Opções de suspensão de publicação  

Por padrão, o envio é publicado assim que ele passa a certificação.  Você pode optar por colocar uma espera na publicação do envio até uma data específica.  As opções desta seção são descritas a seguir.  

*   **Publicar o envio assim que ele passar na certificação**  

    Esta é a seleção padrão.  Isso significa que seu envio começa o processo de publicação assim que passa a certificação  

*   **Iniciar a publicação de seu envio em uma data específica**  

    Escolha **iniciar a publicação do envio em uma determinada data** para garantir que o envio não seja publicado até uma data específica.  Com essa opção, seu envio é lançado o mais rápido possível em ou após a data que você especificar.  A data deve ser pelo menos 24 horas no futuro.  Juntamente com a data, você pode especificar a hora em que o envio deve começar a ser publicado.  

### Notas para certificação  

À medida que você envia a extensão, tem a opção de usar a página anotações para certificação para fornecer informações adicionais aos testadores de certificação.  Essas informações ajudam a garantir que sua extensão seja testada corretamente.  Se não pudermos testar completamente o envio, pode haver falha na certificação.  

Certifique-se de incluir o seguinte \ (se aplicável à sua extensão \):  

*   Nomes de usuário e senhas para contas de teste.  
*   Etapas para acessar recursos ocultos ou bloqueados.  
*   Diferenças esperadas no comportamento com base na região ou em outras configurações do usuário.  
*   Informações sobre o que mudou em uma atualização de aplicativo.  
*   Qualquer outra coisa que você acha que os testadores devem entender sobre o seu envio.  

Depois de concluir os detalhes acima, clique em **publicar** para enviar sua extensão nos Complementos do Microsoft Edge.  

Quando terminar de criar o envio para a extensão e clicar em **publicar**, o envio entrará na etapa de certificação.  Geralmente, esse processo é concluído dentro de alguns dias, mas em alguns casos pode levar até sete dias úteis.  Depois que seu envio for aprovado na certificação, sua extensão será publicada nos Complementos do Microsoft Edge, a menos que você tenha selecionado as opções de retenção de publicação para especificar que ele não deve ser liberado até uma determinada data.  Você será notificado quando o envio for publicado, e o status da extensão no painel mudará para `In the Store` .  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introdução ao Microsoft Edge \ (Chromium \) extensões | Documentos da Microsoft"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Carregar um vídeo do YouTube | Documentos da Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Políticas de desenvolvedor de catálogo de Complementos do Microsoft Edge | Documentos da Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Contrato de desenvolvedor de aplicativos | Documentos da Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Central de parceiros"  
