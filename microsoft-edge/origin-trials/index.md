---
ms.assetid: ''
description: Experimente com segurança por um período de tempo fixo e forneça comentários sobre os novos recursos da plataforma.
title: Avaliações de Origem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, css, avaliação de origem, desenvolvedor
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397542"
---
# <a name="use-origin-trials-in-microsoft-edge"></a>Usar testes de origem no Microsoft Edge  

Os desenvolvedores podem usar testes de origem para experimentar APIs experimentais em sites ao vivo por um período limitado de tempo.  Ao usar as avaliação de origem, os usuários do Microsoft Edge que visitam seu site podem executar um código que usa APIs experimentais.  Para acessar as APIs experimentais em cada máquina de usuário, você não precisa ir e `edge://flags` ativar sinalizadores de recursos.  Para obter mais informações, navegue até [APIs experimentais.][DeveloperMicrsoftEdgeOriginTrials]  Além disso, você pode fornecer comentários sobre o design da API, seus casos de uso ou sua experiência usando as APIs para engenheiros de navegador e a comunidade padrão da Web.  

## <a name="get-started-using-origin-trials"></a>Começar a usar as avaliação de origem  

Para obter mais informações sobre as APIs experimentais disponíveis no Microsoft Edge, navegue até [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].  Verifique os requisitos mínimos de versão para o Microsoft Edge e a data de término da avaliação para avaliar a adequação do uso das APIs experimentais em seu site.  

> [!NOTE]
> Um experimento pode terminar antes do planejado se qualquer uma das seguintes situações ocorrer.  
> *   Um incidente de segurança grave.  
> *   Se os comentários suficientes são coletados que indicam que um grande redesenho é necessário para atender às necessidades dos desenvolvedores da Web.  
> Em ambos os casos, um email de notificação é enviado para todos os desenvolvedores atualmente inscritos no experimento.  

### <a name="register-for-a-trial-of-an-experimental-api"></a>Registrar-se para uma avaliação de uma API experimental  

Use as etapas a seguir para registrar uma avaliação de uma API experimental.  

1.  Visite a [página Console do Desenvolvedor de Avaliação de Origem do Microsoft Edge.][DeveloperMicrsoftEdgeOriginTrials]  
1.  Escolha o botão Registrar em qualquer um dos experimentos disponíveis.  
1.  Entre no Console do Desenvolvedor usando seu nome de usuário e senha do GitHub.  
1.  Escolha **Autorizar o MicrosoftEdge**.  
1.  Preencha o formulário.  
    
    > [!NOTE]
    > Para registrar um único ou todos os subdomas, escolha definir a `Do you need to match all subdomains for the provided origin?` configuração como `Yes` .  Por exemplo, `https://dev.contoso.com` é um único domínio e usa um `https://*.contoso.com` curinga para representar todos os subdomas.  
    
    > [!IMPORTANT]
    > Os seguintes formatos de origem não são permitidos.  
    > *   Especificando uma subpasta na origem.  Por exemplo, `https://contoso.com/path/subfolder`  
    > 
    > *   Usando uma origem com parâmetros de cadeia de caracteres de consulta.  Por exemplo, `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Escolha **ACEITAR e REGISTRAR**.  
    
### <a name="apply-your-token"></a>Aplicar seu token  

Um token é gerado instantaneamente e exibido na página Console do Desenvolvedor de Avaliação de Origem do [Microsoft Edge.][DeveloperMicrsoftEdgeOriginTrials]  Para começar a usar a avaliação em seu site, use um dos métodos a seguir para aplicar o token à sua página.  

*   Adicione o `origin-trial` valor do atributo e seu token à marca em cada página que usa a API `meta` experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Adicione `Origin-Trial` ao cabeçalho de resposta HTTP do seu servidor.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Seu token é válido por 6 semanas.  Antes do final da avaliação, os emails de lembrete são enviados para você que solicitam seus comentários e solicitam que você considere a renovação da avaliação antes que seu token expire.  

### <a name="opt-out-of-an-experiment"></a>Não participar de um experimento  

Para não participar de um experimento, use um dos métodos a seguir para remover seu token.  

*   Remova a `meta` marca de cada página que usou a API experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Remova `Origin-Trial` do cabeçalho de resposta HTTP do seu servidor.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a>Detectar recursos experimentais e fornecer um fallback  

Ao usar APIs experimentais, certifique-se de fornecer uma experiência de trabalho para todos os visitantes do seu site.  Os visitantes podem usar navegadores que não suportam as APIs experimentais que você adicionou ao código.  Além disso, se o token expirar antes de renová-lo, a API experimental não estará mais disponível, o que pode resultar em erros.  Para evitar essa situação, certifique-se de detectar recursos disponíveis no navegador.  Para obter mais informações, navegue até [Implementando a detecção de recursos][MDNImplementingFeatureDetection].

### <a name="roadmap-for-allowed-origins"></a>Roteiro para Origens Permitidas  

O portal de Avaliação de Origem do Microsoft Edge atualmente só dá suporte a Origens Habilitadas para SSL, o que significa que os sites devem ter HTTPS implementado corretamente para registrar um experimento.  No futuro, as seguintes origens seguras são planejadas.  

*   `http://localhost`Registre-se como a origem de seus experimentos.  Para usar `http://localhost` hoje, navegue até `edge://flags` e de definir o experimento como **Habilitado**.  
*   Use extensões com `extensions://` origens prefixadas para se registrar em experimentos.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementando a detecção de recursos | MDN"  
