---
description: Entre em contato com o mundo dos clientes do Windows 10 distribuindo o seu PWA por meio da Microsoft Store
title: Aplicativos Web progressivos na Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, Microsoft Store, índice do Bing PWA
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dae25bcdf37a2496e181ab915d1686fe5d3a4985
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231566"
---
# Aplicativos Web progressivos na Microsoft Store

Quando você publica seu aplicativo Web progressivo (PWA) na [Microsoft Store](https://developer.microsoft.com/store), seu possível público de aplicativos se expande para toda a base de instalação do Windows 10 de quase 700 milhões usuários do mês ativo. 

PWAs na Microsoft Store, desfrute de várias vantagens:

-   **Capacidade de descoberta** – os aplicativos na Microsoft Store são mostrados por categorias diferentes, coleções organizadas e filtros de pesquisa, oferecendo uma fácil navegação e experiência de compras para clientes em potencial do seu aplicativo. Você pode até mesmo [aprimorar a listagem da loja](/windows/uwp/publish/app-screenshots-and-images) com capturas de tela, uma imagem do herói e trailers de vídeo.
-   **Confiabilidade** – os clientes do Windows sabem que podem confiar nas compras e downloads da Microsoft Store, pois eles aderem aos padrões rigorosos de [qualidade e segurança](/legal/windows/agreements/store-policies)da Microsoft.
-   **Instalação fácil** – a Microsoft Store oferece uma experiência de instalação consistente e de usuário em [todos os aplicativos do Windows 10](https://www.microsoft.com/store/apps/windows?icid=CNavAppsWindowsApps), tornando mais fácil para todos os clientes instalarem o PWA, independentemente do nível de conforto técnico.
-   **Informações comerciais** – o painel do [centro de desenvolvimento do Windows](/windows/uwp/publish/using-the-windows-dev-center-dashboard) para a Microsoft Store oferece uma [análise detalhada](/windows/uwp/publish/analytics) sobre tudo que a quantidade de clientes do Windows que o seu PWA alcançou para a forma como estão usando e o que eles têm a dizer. Você também pode encontrar métricas e dados de telemetria sobre a integridade do aplicativo, o uso do anúncio e muito mais.
    
Há duas opções para colocar seu PWA na Microsoft Store:

1.  Você pode [enviá-lo manualmente](#submitting-your-pwa-manually)ou
2.  Se o seu PWA atender a [certos critérios](#criteria-for-automatic-submission), ele poderá ser [automaticamente indexado](#automatic-pwa-importing-with-bing) pelo rastreador da Web do Bing. (Você também tem a opção de [recusar](#opting-out-of-automatic-microsoft-store-import) o envio automático.)
    
Independentemente do método de envio, uma vez que o PWA seja aceito para a Microsoft Store, você obterá acesso a todos os benefícios descritos acima.

## Enviando seu PWA manualmente

Para distribuir e promover um aplicativo por meio da Microsoft Store, você precisará enviá-lo como um pacote de aplicativo do Windows (arquivo *. Appx* ).  Para aplicativos Web hospedados no servidor, como o PWAs, este pacote simplesmente contém metadados do aplicativo e ícones da tela inicial (e nenhum dos códigos do aplicativo real). Com isso, seu aplicativo Web pode ser instalado e iniciado a partir da tela inicial ao lado de outros [aplicativos do Windows 10](/windows/uwp/get-started/whats-a-uwp) executando em um invólucro de aplicativo nativo leve (*WWAHost.exe* processo), independente da janela do navegador Microsoft Edge.  

> [!IMPORTANT]
> O mecanismo de plataforma da Web EdgeHTML é usado pelo wrapper do aplicativo WWAHost que pode introduzir diferenças de compatibilidade para o seu PWA baseado no Microsoft Edge (Chromium).  Certifique-se de fazer um teste de teste completo em seu aplicativo usando o Microsoft Edge (EdgeHTML) antes de enviar seu aplicativo para a Microsoft Store, pois o mecanismo de EdgeHTML não está mais sendo atualizado com padrões da Web mais recentes.  

Veja aqui como fazer isso.

### Pré-requisitos

-   **Um PWA existente**. Confira aqui como [converter seu aplicativo Web em um PWA](./get-started.md) se ainda não houver um. 
-   **Uma ferramenta de empacotamento do Windows Appx para PWAs**. Veja aqui como [Compilar e executar o PWA no Windows usando o](./windows-features.md) Visual Studio. Você também pode usar o [compilador do PWA](https://www.pwabuilder.com/) para compilar um pacote do Windows.
-   [**Conta de desenvolvedor do aplicativo da Microsoft Store**](/windows/uwp/publish/opening-a-developer-account). Há uma [taxa única](/windows/uwp/publish/account-types-locations-and-fees) , dependendo do tipo e local de conta escolhido, e o registro requer uma [conta da Microsoft](https://account.microsoft.com/)válida.
    
### Envio da loja pelo *Visual Studio* 

Siga estas etapas para [criar um arquivo de carregamento de pacote do aplicativo](/windows/uwp/packaging/packaging-uwp-apps#create-an-app-package-upload-file) para o seu PWA no Visual Studio. Consulte [*empacotar um aplicativo UWP com o Visual Studio*](/windows/uwp/packaging/packaging-uwp-apps) para obter uma visão geral mais geral desse processo.

As instruções também o orientarão na execução do [**Kit de certificação de aplicativos Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit) para testar seu aplicativo quanto à conformidade com os requisitos da Microsoft Store. Isso é opcional, mas altamente recomendado.

### Envio da loja por meio do *centro de desenvolvimento do Windows*

Veja como usar o *construtor do PWA* para gerar um pacote do aplicativo para carregar no centro de desenvolvimento do Windows.

1.  Gere seu aplicativo do Windows 10. Veja aqui como executar o [PWA como um aplicativo do Windows com o Visual Studio](./windows-features.md). Você também pode usar o [construtor do PWA](https://www.pwabuilder.com/) para gerar seu aplicativo do Windows 10.
2.  Reserve o nome do seu aplicativo para a Microsoft Store ao fazer logon no [painel do centro de desenvolvimento do Windows](https://developer.microsoft.com/dashboard/windows/overview) com as informações da sua conta e seguindo as etapas para [criar seu aplicativo reservando um nome](/windows/uwp/publish/create-your-app-by-reserving-a-name). Cada nome reservado deve ser exclusivo em toda a Microsoft Store.
3.  Quando você carrega pacotes do aplicativo, os valores *DisplayName*, *Name*, *Publisher*e *PublisherDisplayName* em seu arquivo *. appxmanifest* devem coincidir com os valores atribuídos ao seu aplicativo no painel do centro de desenvolvimento do Windows, ao reservar o nome. 
    
    Faça logon no [painel do centro de desenvolvimento do Windows](https://developer.microsoft.com/dashboard/windows/overview)e localize os valores de identidade do aplicativo na identidade do aplicativo de **Gerenciamento do aplicativo**  >  ****:
    
    ![Painel do centro de desenvolvimento do Windows, configurações de identidade do aplicativo](./media/dashboard-app-identity.png)
    
    Em seguida, localize o `appxmanifest.xml` arquivo e substitua os seguintes valores por aqueles atribuídos no painel do centro de desenvolvimento do Windows:
    
    -   **<Identity Name = "** *pacote/identidade/nome*
    -   **<Identity Publisher = "** *pacote/identidade/editor*
    -   **<DisplayName** **>** *Nome reservado para seu aplicativo* 
    -   **<PublisherDisplayName** **>** *Package/Properties/PublisherDisplayName***</PublisherDisplayName>**
        
4.  Agora, você está pronto para compilar todos os seus recursos do PWA em um único `.appx` arquivo que você pode carregar na Microsoft Store. Em um prompt de comando, navegue até o diretório do seu manifesto da Web e crie um pacote do Windows 10 (especificado abaixo de w/log de depuração opcional):
    
    ```shell
    pwabuilder package -p windows10 -l debug
    ```  
    
    Seu arquivo. Appx será gerado para este local: `PWA\Store packages\windows10\package\windows.appx` .
    
5.  Antes de carregar seu aplicativo para o submisison na Microsoft Store, é uma boa ideia testar seu aplicativo em busca de conformidade com as políticas da Microsoft Store. Você pode fazer isso baixando o [**Kit de certificação de aplicativos Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit), iniciando-o e selecionando o arquivo *. Appx* do aplicativo para teste. Você receberá um relatório de áreas que serão abordadas quando todos os testes estiverem concluídos.
6.  Carregue o pacote e conclua o envio registrando novamente no [painel do centro de desenvolvimento do Windows](https://developer.microsoft.com/dashboard/windows/overview) e expandindo o painel **envios**  >  **Submisison 1** . Siga a lista de verificação para concluir as [informações da listagem da loja necessárias](/windows/uwp/publish/app-submissions) e [carregar o pacote do aplicativo](/windows/uwp/publish/upload-app-packages).
    
Para saber mais sobre todos os recursos e serviços disponíveis para os desenvolvedores de aplicativos da Microsoft Store, consulte [*publicar aplicativos do Windows*](https://developer.microsoft.com/store/publish-apps) no [centro de desenvolvimento do Windows](https://developer.microsoft.com/windows).

## Importação automática do PWA com o Bing

Assim como o manifesto do [aplicativo Web](https://developer.mozilla.org/docs/Web/Manifest) do PWA é um sinal para dar suporte a plataformas que seu aplicativo está habilitado para offline e pronto para ser apresentado como uma experiência de aplicativo totalmente integrada, também é uma dica ao rastreador da Web do Bing que o seu PWA deve ser considerado para a inclusão automática na Microsoft Store. 

Se o seu PWA atender aos requisitos abaixo, o serviço de indexação do Bing empacotará automaticamente o PWA no formato [*. Appx*](#submitting-your-pwa-manually) necessário para instalação no Windows 10 e montará a página de produto da loja do aplicativo com base nos metadados do manifesto do aplicativo Web. Depois de reivindicar o seu PWA, você poderá personalizar ainda mais a página da loja e obter acesso ao Analytics do usuário e outras ferramentas de gerenciamento de aplicativos por meio do painel do centro de desenvolvimento do Windows.

### Critérios para envio automático

Para ser empacotado automaticamente e listado para a Microsoft Store, o PWA precisará de:

-   Um arquivo de manifesto do aplicativo Web não vazio, com pelo menos:
    
    -   Nome
    -   Descrição
    -   Ícone do aplicativo com pelo menos 512 x 512 pixels
        
-   Lógica do núcleo exclusivo (não um código modificado minimamente de um modelo [clichê do aplicativo](https://en.wikipedia.org/wiki/Boilerplate_code) )
-   Para ser servido por meio de uma conexão segura (HTTPS)
-   Script de trabalhador de serviço (s)
-   Para não violar as leis ou [políticas da Microsoft Store](/legal/windows/agreements/store-policies).
    
Não informaremos todos os aplicativos que atendem a esses critérios, mas o incluirá em nossas considerações para os candidatos, pois expandimos gradualmente nosso programa.

### Optando pela importação automática da Microsoft Store

O PWA pode recusar a importação automática para a Microsoft Store, servindo um `robots.txt` arquivo contendo o seguinte:

```text
User-agent: bingbot
Disallow: /manifest.json
```  

Isso direciona o Bing Web crawler (Bingbot) para desconsiderar o arquivo de manifesto da Web para fins de indexação do PWA. Isso não afetará a classificação de pesquisa do seu site no processo regular de [indexação da Web](https://www.bing.com/webmaster/help/help-center-661b2d18)do Bing.
