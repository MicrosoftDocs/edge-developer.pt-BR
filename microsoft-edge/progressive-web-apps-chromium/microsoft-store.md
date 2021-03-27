---
description: Tornar seu PWA mais descoberto publicando na Microsoft Store
title: Publicar seu Aplicativo Web Progressivo na Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 68471535446a2270a23b32205717da225fd9e4bf
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461476"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a>Publicar seu Aplicativo Web Progressivo na Microsoft Store  

Publicar seu Aplicativo Web Progressivo \(PWA\) para a [Microsoft Store][WindowsUwpPublishIndex] traz as seguintes vantagens.  

:::row:::
   :::column span="1":::
      **Detectabilidade**  
   :::column-end:::
   :::column span="2":::
      Os usuários procurarão naturalmente aplicativos na loja de aplicativos.  Ao publicar na Microsoft Store, milhões de usuários do Windows podem descobrir seu PWA juntamente com outros aplicativos do Windows.  A Loja mostra aplicativos por meio de categorias, coleções com curadoria e muito mais.  Os portais de descoberta de aplicativos oferecem uma experiência fácil de navegação e compras para os possíveis usuários do seu aplicativo.  Você pode até [aprimorar sua listagem da Loja][WindowsUwpPublishAppScreenshotsImages] com capturas de tela, uma imagem de herói e trailers de vídeo.  
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
1.  Agora, seu aplicativo está inscrito no programa de desenvolvedor de aplicativos. Para criar uma reserva de aplicativo, conclua as seguintes ações.  
    1.  Navegue **até Windows & Xbox**.  
    1.  Escolha **Visão geral**Criar um novo  >  **aplicativo.**  
    1.  Digite seu nome PWA no prompt.  
    1.  Escolha `Reserve product name` .  
    
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Criar uma reserva de aplicativo no Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       Criar uma reserva de aplicativo no Windows Partner Center  
    :::image-end:::  

1.  Para exibir os detalhes do editor para uso na seção [Pacote do PWA,](#package-your-pwa) escolha **Product management**  >  **Product Identity**.  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copie as informações do editor do Windows Partner Center" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       Copie as informações do editor do Windows Partner Center  
    :::image-end:::  

1.  Copie e salve os seguintes valores.  
    *   **ID do pacote**  
    *   **Publisher ID**  
    *   **Nome de Exibição do Publisher**  
        
## <a name="package-your-pwa"></a>Empacote seu PWA  

Gere um pacote de aplicativos do Windows para o PWA.  

Seu pacote de aplicativos é um arquivo que contém os metadados do seu aplicativo, incluindo o `.msixbundle` nome, a descrição, os ícones e assim por diante.  Ele usa o [Modelo de Aplicativo Hospedado][WindowsBlogWindowsdeveloperHostedAppModel], com o Microsoft Edge powering your PWA.  Nesse modelo, o PWA usa recursos modernos da Web enquanto funciona como um aplicativo do Windows.  Os recursos modernos da Web incluem trabalho de serviço, offline, notificações por push, badging e muito mais.  

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
1.  Para baixar seu pacote de aplicativos do Windows, escolha **Baixar**.  Seu download é um `.zip` arquivo morto que contém um `.msixbundle` arquivo.  Use o `.msixbundle` arquivo na seção Enviar seu pacote de [aplicativos para a](#submit-your-app-package-to-the-store) Loja.  

### <a name="submit-your-app-package-to-the-store"></a>Enviar seu pacote de aplicativos para a Loja  

Agora, você tem seu `.msixbundle` pacote de aplicativos.  Para enviar seu pacote de aplicativos para a Loja, conclua as seguintes ações.  

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
        
1.  No prompt **Pacotes,** escolha o `.msixbundle` arquivo gerado na seção Pacote do [PWA.](#package-your-pwa)  

Depois que você concluir seu envio, seu aplicativo será revisado, normalmente entre 24 e 48 horas.  Depois de receber aprovação, o PWA estará disponível na Microsoft Store.  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Políticas da Microsoft Store | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analisar o desempenho do aplicativo | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de tela, imagens e trailers do aplicativo | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar aplicativos e jogos do Windows | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Home | Microsoft Partner Center"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para parceiros | Microsoft Partner Center"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Aplicativos do Windows | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Modelo de aplicativo hospedado | Blog do Desenvolvedor do Windows"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  

