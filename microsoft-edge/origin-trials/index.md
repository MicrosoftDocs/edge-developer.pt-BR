---
ms.assetid: ''
description: Experimente com segurança um período de tempo fixo e forneça comentários sobre novos recursos da plataforma.
title: Avaliações de Origem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, tentativas de origem, desenvolvedor
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846522"
---
# Usar testes de origem no Microsoft Edge  

Os desenvolvedores podem usar avaliações de origem para experimentar APIs experimentais em sites ativos por um período limitado de tempo.  Ao usar avaliações de origem, os usuários do Microsoft Edge que acessam o site podem executar um código que usa APIs experimentais.  Para acessar as APIs experimentais em cada computador de usuário, você não precisa ir para `edge://flags` e ativar os sinalizadores de recursos.  Para obter mais informações, consulte [APIs experimentales][DeveloperMicrsoftEdgeOriginTrials].  Além disso, você pode fornecer comentários sobre o design da API, seus casos de uso ou sua experiência ao usar as APIs para engenheiros de navegador e a Comunidade padrão da Web.  

## Comece a usar os testes de origem  

Para obter mais informações sobre as APIs experimentais disponíveis no Microsoft Edge, consulte [console de desenvolvedor de tentativas de origem do Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials].  Certifique-se de que você revisar os requisitos mínimos de versão do Microsoft Edge e a data de término da avaliação para avaliar a adequação do uso das APIs experimentais em seu site.  

> [!NOTE]
> Um experimento poderá terminar antes do planejado se qualquer uma das seguintes situações ocorrer.  
> *   Um incidente de segurança importante.  
> *   Se forem coletados comentários suficientes que indicam que é preciso fazer um novo design para atender às necessidades dos desenvolvedores da Web.  
> Em ambos os casos, um e-mail de notificação é enviado a todos os desenvolvedores atualmente registrados no experimento.  

### Registre-se para obter uma avaliação de uma API experimental  

Use as etapas a seguir para se registrar para uma avaliação experimental de uma API experimental.  

1.  Acesse a página do [console do desenvolvedor de Microsoft Edge originies][DeveloperMicrsoftEdgeOriginTrials] .  
1.  Escolha o botão registrar em qualquer um dos experimentos disponíveis.  
1.  Conecte-se ao console do desenvolvedor usando seu nome de usuário e senha do GitHub.  
1.  Escolha **autorizar MicrosoftEdge**.  
1.  Preencha o formulário.  
    
    > [!NOTE]
    > Para registrar um único ou todos os subdomínios, escolha definir a `Do you need to match all subdomains for the provided origin?` configuração como `Yes` .  Por exemplo, `https://dev.contoso.com` é um único domínio e `https://*.contoso.com` usa um curinga para representar todos os subdomínios.  
    
    > [!IMPORTANT]
    > Os seguintes formatos de origem não são permitidos.  
    > *   Especificando uma subpasta na origem.  Por exemplo, `https://contoso.com/path/subfolder`  
    > 
    > *   Usar uma origem com parâmetros de cadeia de caracteres de consulta.  Por exemplo, `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Escolha **aceitar e registrar**.  

### Aplicar seu token  

Um token é gerado instantaneamente e exibido na página do [console de desenvolvedor de origem do Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .  Para começar a usar a avaliação no seu site, use um dos seguintes métodos para aplicar o token à sua página.  

*   Adicione o `origin-trial` valor do atributo e seu token à `meta` marca em cada página que usa a API experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Adicione `Origin-Trial` ao cabeçalho de resposta http do seu servidor.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Seu token é válido por 6 semanas.  Antes do término do período de teste, os e-mails dos lembretes são enviados para você, que solicitam seus comentários e pedem que você considere a renovação de sua avaliação antes de o token expirar.  

### Recusar um experimento  

Para cancelar um experimento, use um dos seguintes métodos para remover o token.  

*   Remova a `meta` marca de cada página que usou a API experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Remover `Origin-Trial` do cabeçalho de resposta http do seu servidor.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### Detectar recursos experimentais e fornecer um fallback  

Ao usar APIs experimentais, certifique-se de fornecer uma experiência de trabalho para todos os visitantes do seu site.  Os visitantes podem usar navegadores que não dão suporte a APIs experimentadas que você adicionou ao seu código.  Além disso, se o token expirar antes de ser renovado, a API experimental não estará mais disponível, o que pode resultar em erros.  Para evitar essa situação, verifique se você detecta recursos disponíveis no seu navegador.  Para obter mais informações, consulte [implementando a detecção de recursos][MDNImplementingFeatureDetection].

### Mapa de origens permitidas  

O portal de avaliações de origem do Microsoft Edge hoje só oferece suporte a origens habilitadas para SSL, o que significa que os sites devem ter HTTPS devidamente implementados para se registrarem para um experimento.  No futuro, as seguintes origens seguras são planejadas.  

*   Registre-se `http://localhost` como a origem de seus experimentos.  Para usar `http://localhost` o hoje, vá para `edge://flags` e defina o experimento como **habilitado**.  
*   Use extensões com `extensions://` origens prefixadas para se cadastrar em experimentos.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Console de desenvolvedor de tentativas de origem do Microsoft Edge | Documentos da Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementando a detecção de recursos | MDN"  
