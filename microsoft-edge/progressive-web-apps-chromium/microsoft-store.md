---
description: Tornar seu PWA mais descoberto publicando na Microsoft Store
title: Publicar seu Aplicativo Web Progressivo na Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 5e78e909187408566219ffe80779bb9221b585fa
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "11527049"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Publicar seu Aplicativo Web Progressivo na Microsoft Store  

Publicar seu Aplicativo Web Progressivo \(PWA\) para a [Microsoft Store][WindowsUwpPublishIndex] traz as seguintes vantagens.  

:::row:::
   :::column span="1":::
      **Detectabilidade**  
   :::column-end:::
   :::column span="2":::
      Os usuários procurarão naturalmente aplicativos na loja de aplicativos.  Quando você publica na Microsoft Store, milhões de usuários do Windows podem descobrir seu PWA junto com outros aplicativos do Windows.  A Loja mostra aplicativos por meio de categorias, coleções com curadoria e muito mais.  Os portais de descoberta de aplicativos oferecem uma experiência fácil de navegação e compras para os possíveis usuários do seu aplicativo.  Você pode até [aprimorar sua listagem da Loja][WindowsUwpPublishAppScreenshotsImages] com capturas de tela, uma imagem de herói e trailers de vídeo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Confiabilidade**  
   :::column-end:::
   :::column span="2":::
      Os clientes do Windows sabem que podem confiar em suas compras e downloads da Microsoft Store, porque eles aderem aos rigorosos padrões de segurança e qualidade [da][LegalWindowsAgreementsStorePolicies]Microsoft.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Instalação fácil**  
   :::column-end:::
   :::column span="2":::
      A Microsoft Store fornece uma experiência de instalação consistente e fácil de usar em todos [os aplicativos do Windows 10.][MicrosoftStoreAppsWindows]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Análise de aplicativos**  
   :::column-end:::
   :::column span="2":::
      O [painel do Windows Partner Center][WindowsUwpPublishIndex] fornece análises [detalhadas][WindowsUwpPublishAnalytics] sobre a saúde, o uso e muito mais do aplicativo.  
   :::column-end:::
:::row-end:::  

Para publicar seu PWA na Microsoft Store, nenhuma alteração de código é necessária.  Em vez disso, crie uma reserva de aplicativo, empacote seu PWA e envie seu pacote para a Loja.  As seções a seguir explicam as etapas.   

## <a name="create-an-app-reservation"></a>Criar uma reserva de aplicativo  

[O Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] é o hub para você enviar seu aplicativo para a Microsoft Store.  

Para criar uma reserva de aplicativo, conclua as seguintes ações.  

1.  Para exibir seus programas inscritos, conclua as seguintes ações.  
    1.  Entre no Windows Partner Center com sua conta da Microsoft e navegue até o [Painel do Partner Center][MicrosoftPartnerDashboardHome].  
    1.  Navegue **até Windows & Xbox**  
        *   Se **o Windows & Xbox** for exibido, seu aplicativo já está inscrito.  
        *   Se **o Windows & Xbox** não for exibido, escolha Adicionar **programa**.  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Adicionar um programa no painel do Windows Partner Center" lightbox="./media/windows-partner-center-add-program.msft.png":::
       Adicionar um programa no painel do Windows Partner Center
    :::image-end:::  
    
1.  Para se inscrever no programa de desenvolvedor, conclua as seguintes ações.  
    1.  Navegue **até Windows & Xbox**.  
    1.  Escolha **Começar.**  
    1.  Siga os avisos.  
1.  Agora, sua conta está inscrita no programa de desenvolvedor de aplicativos. Para criar uma reserva de aplicativo, conclua as seguintes ações.  
    1.  Navegue **até Windows & Xbox**.  
    1.  Escolha **Visão geral**Criar um novo  >  **aplicativo.**  
    1.  Digite o nome do aplicativo no prompt.  
    1.  Escolha `Reserve product name` .  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Criar uma reserva de aplicativo no Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Criar uma reserva de aplicativo no Windows Partner Center  
    :::image-end:::  
    
1.  Para exibir os detalhes do editor para uso na seção [Pacote do PWA,](#package-your-pwa-for-the-store) escolha **Product management**  >  **Product Identity**.  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copie as informações do editor do Windows Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Copie as informações do editor do Windows Partner Center  
    :::image-end:::  
    
1.  Copie e salve os seguintes valores.  
    *   **ID do pacote**  
    *   **Publisher ID**  
    *   **Nome de Exibição do Publisher**  
        
## <a name="package-your-pwa-for-the-store"></a>Empacote seu PWA para a Loja 

Agora que você tem as informações de publicação do aplicativo, gere um pacote de aplicativos do Windows para o PWA.

Para gerar um pacote de aplicativos, conclua as seguintes ações.  

1.  Navegue até [Construtor do PWA][PwabuilderMain].  
1.  Digite a URL do seu PWA.  
1.  Escolha **Iniciar**  >  **a com build minhas opções do Windows do PWA.**  >  ****  >  ****  
1.  Colar os seguintes valores que você salvou na seção [Criar uma reserva de](#create-an-app-reservation) aplicativo.  
    *   **ID do pacote**  
    *   **Publisher ID**  
    *   **Nome de Exibição do Publisher**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Colar informações do editor no PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       Colar informações do editor no PWABuilder  
    :::image-end:::  
    
1.  Escolha **Feito**.  
1.  Para baixar seu pacote de aplicativos do Windows, escolha **Baixar**.

Seu download é um `.zip` arquivo morto que contém um arquivo e um `.msixbundle` `.classic.appxbundle` arquivo.  Os dois pacotes de aplicativos permitem que o PWA seja executado em uma ampla variedade de versões do Windows.  Para obter mais informações, navegue até [O que é um pacote clássico?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].  

### <a name="submit-your-app-package-to-the-store"></a>Enviar seu pacote de aplicativos para a Loja  

Para enviar seu aplicativo para a Loja, conclua as seguintes ações.  

1.  Navegue até [o Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] 
1.  Escolha seu aplicativo.  
1.  Escolha **Iniciar seu Envio**.  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Iniciar um novo envio de aplicativo no Windows Partner Center" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       Iniciar um novo envio de aplicativo no Windows Partner Center  
    :::image-end:::  
    
1.  Preencha os prompts a seguir para obter informações sobre seu aplicativo.
    *   pricing  
    *   classificação etária  
    *   e mais  
        
1.  No prompt **Pacotes,** escolha os `.msixbundle` arquivos e os `.classic.appxbundle` gerados na seção Pacote do [PWA.](#package-your-pwa-for-the-store)  
    
Depois que você concluir seu envio, seu aplicativo será revisado, normalmente entre 24 e 48 horas.  Depois de receber aprovação, o PWA estará disponível na Microsoft Store.  

## <a name="see-also"></a>Ver também  

O PWABuilder fornece mais documentação para ajudá-lo a obter seu PWA na Microsoft Store.  

*   [Testar e enviar seu pacote de aplicativos PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [Publicar um novo PWA na Loja][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [Atualizar um aplicativo da Loja existente para um PWA][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [Recomendações de imagem para PWAs na Loja][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [Explicador de empacotamento de aplicativos][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Políticas da Microsoft Store | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analisar o desempenho do aplicativo | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de tela, imagens e trailers do aplicativo | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar aplicativos e jogos do Windows | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Home | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para parceiros | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Aplicativos do Windows | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modelo de aplicativo hospedado | Blog do Desenvolvedor do Windows"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "O que é um pacote clássico? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recomendações de imagem para pacotes PWA do Windows | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Próximas etapas para obter seu PWA no microsoft store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publicar um novo aplicativo na loja | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Atualizar um aplicativo existente na loja | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
