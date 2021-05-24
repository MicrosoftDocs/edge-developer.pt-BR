---
description: Este artigo fornece documentação sobre as dicas Microsoft Edge cliente do agente de usuário e a cadeia de caracteres de agente do usuário
title: Como detectar o Microsoft Edge em seu site
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user agent string, ua string, ua overrides, user-agent client hints, user agent client hints, ua client hints, ua ch
ms.openlocfilehash: 1957bb5bd33d9d921d8a12e16a4a52a23836027b
ms.sourcegitcommit: e90bbc210b5d510004bbc2145d49e14fe72ed54b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/20/2021
ms.locfileid: "11578773"
---
# <a name="how-to-detect-microsoft-edge-in-your-website"></a>Como detectar o Microsoft Edge em seu site  

Os navegadores fornecem mecanismos para que os sites detectem informações do navegador, como a marca e o número da versão.  Os mecanismos também detectam outras características de dispositivo, como o sistema operacional host.  Dois desses mecanismos suportados no Microsoft Edge são [User-Agent Client Hints](#user-agent-client-hints) e [User-Agent strings](#user-agent-string).  Após décadas de uso, User-Agent cadeias de caracteres estão desatualizadas e têm um histórico longo como causa de problemas de compatibilidade de site.  Em vez disso, Microsoft Edge equipe recomenda que você use um mecanismo aprimorado para recuperar informações do navegador chamadas [User-Agent Client Hints](#user-agent-client-hints).  Este artigo descreve os dois mecanismos que Microsoft Edge suporte para recuperar informações do agente do usuário.  

|  | Lado do servidor | Lado do cliente |  
|:--- |:--- |:--- | 
| **Dicas de cliente de** agente de usuário \(recommended\) | `Sec-CH-UA` Cabeçalho HTTPS | `navigator.userAgentData` Método JavaScript |  
| **Cadeia de caracteres user-agent** \(legacy\) | `User-Agent` Cabeçalho HTTPS | `navigator.userAgent` Método JavaScript |  

A Microsoft recomenda que você use a detecção [de recursos][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] sempre que possível pelos seguintes motivos.  

*   Melhorar a manutenção do código.  
*   Reduza a fragilidade do código.  
*   Reduza a quebra de código das alterações na User-Agent cadeia de caracteres.  
    
Quando [a detecção de][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] recursos não for aplicável e você deve usar a detecção de agente de usuário, use o formato a seguir para detectar Microsoft Edge agente de usuário no Windows e Android.  

## <a name="user-agent-client-hints"></a>User-Agent dicas de cliente  

A partir Microsoft Edge versão 90, acesse as informações do navegador de forma mais limpa e preservando a privacidade.  

### <a name="user-agent-client-hints-https-header"></a>User-Agent cliente dicas de cabeçalho HTTPS  

Por padrão, Chromium navegadores incluindo Microsoft Edge enviar o header de `Accept-CH-UA` resposta no formato a seguir.  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> As Dicas de Cliente são enviadas apenas por conexões seguras usando `HTTPS` .  

As dicas de entropia baixa a seguir são enviadas por padrão.  Se precisar acessar mais informações, envie um dos seguintes headers de solicitação.  

#### <a name="user-agent-request-and-response-headers"></a>User-Agent de solicitação e resposta  

| Cabeçalho da solicitação | Valor de resposta de exemplo |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a>User-Agent Api JavaScript de Dicas de Cliente  

O valor de resposta padrão de `navigator.userAgentData` usa o formato a seguir.  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

Se você precisar acessar informações mais detalhadas, use o [método getHighEntropyValues().][GithubWicgUaClientHintsGethighentropyvalues]  

:::row:::
   :::column span="":::
      O trecho de código a seguir envia uma solicitação.  
   :::column-end:::
   :::column span="":::
      Para receber a seguinte resposta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```javascript
         navigator.userAgentData.getHighEntropyValues(
             ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
             .then(ua => { console.log(ua) });
      ```  
   :::column-end:::
   :::column span="":::
      ```javascript
      {architecture: "x86", 
      model: "", 
      platform: "Windows", 
      platformVersion: "10.0", 
      uaFullVersion: "92.0.866.0"}
      ```  
   :::column-end:::
:::row-end:::  

## <a name="recommended-uses-of-user-agent-client-hints"></a>Usos recomendados User-Agent dicas de cliente  

O conjunto de marcas e a ordem de exibição associada mudam ao longo do tempo, portanto, você nunca deve codificar índices na matriz de marcas retornadas.  Para ajudar a garantir que você localize problemas semelhantes em seu site no início, o navegador inclui um valor de marca que muda ao longo do tempo e é formatado para quebra devido a problemas comuns de análise de `GREASE` cadeia de caracteres.  

Se você for impedido de usar a detecção de [recursos,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]não use uma lista codificada de navegadores Chromium conhecidos para verificação.  Exemplos de nomes de navegadores de código rígido `Microsoft Edge` incluem e `Google Chrome` .  Os motivos pelos [quais a][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] detecção de recursos não é aplicável podem incluir a seguinte situação.  

*   Uma correção para Chromium bug em uma versão posterior deve ser evitada e os navegadores afetados são difíceis de detectar fora de uma verificação da marca e da versão.  
    
Em vez disso, você deve verificar a marca, o que garante que sua detecção se aplique a todos os navegadores Chromium `Chromium` baseados em Chromium afetados.  


```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium") {
            return true;
        }
    }
    return false;
}
```  

## <a name="user-agent-string"></a>Cadeia de caracteres de agente do usuário  

Sempre que possível, a Microsoft recomenda minimizar o uso da Microsoft Edge de detecção do navegador com base na cadeia de caracteres do agente do usuário.  Se você tiver um bom motivo para detectar o agente do usuário, a equipe Microsoft Edge recomenda que você [use](#user-agent-client-hints) As Dicas de Cliente de Agente de Usuário como a lógica de detecção principal.  [As Dicas](#user-agent-client-hints) de Cliente do Agente de Usuário também reduzem o número necessário de cadeias de caracteres analisados.  No entanto, para referência herdado, o formato a seguir é usado para User-Agent cadeia de caracteres.  

:::row:::
   :::column span="":::
      No Windows, o `User-Agent` cabeçalho de solicitação HTTP usa o seguinte formato.  
   :::column-end:::
   :::column span="":::
      No Android, o `User-Agent` cabeçalho de solicitação HTTP usa o seguinte formato.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
:::row-end:::  

O valor de resposta `navigator.userAgent` do método usa o seguinte formato.  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

Os identificadores de plataforma mudam com base no sistema operacional usado, e os números de versão também são incrementados conforme o tempo passa.  O formato é o mesmo que o Chromium do usuário com a adição de um `Edg` novo token no final.  A Microsoft escolheu o token para evitar problemas de compatibilidade causados pela cadeia de caracteres, que foi usada Microsoft Edge `Edg` `Edge` navegador herdado com base no EdgeHTML.  O `Edg` token também é consistente com [tokens existentes][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] usados no iOS e no Android.

## <a name="map-the-user-agent-string-to-browser-name"></a>Mapear a cadeia de caracteres do agente do usuário para o nome do navegador  

Mapeie os tokens de cadeia de caracteres do agente do usuário para um nome de navegador mais acessível para uso no código.  É um padrão comum na Web hoje.  Quando você mapeia o novo token para um nome de navegador, a Microsoft recomenda que você use um nome diferente do usado para o navegador Microsoft Edge herdado para evitar a aplicação acidental de qualquer solução alternativa herdada que não seja aplicável a navegadores baseados em `Edg` Chromium.

## <a name="user-agent-overrides"></a>O Agente de Usuário substitui  

Às vezes, um site não reconhece o novo Microsoft Edge usuário.  Como resultado, um conjunto de recursos do site pode não funcionar corretamente.  Quando a Microsoft é notificada sobre os tipos de problemas, a Microsoft o contata \(um proprietário do site\) e informa sobre o agente de usuário atualizado.  

Talvez você precise de mais tempo para atualizar e testar a lógica de detecção do agente do usuário para seu site para resolver os problemas relatados pela Microsoft.  Para maximizar a compatibilidade com seus usuários, os canais Microsoft Edge Beta e Estável usam uma lista de substituições de agente de usuário.  Use as substituições do agente do usuário enquanto você atualiza seu site.  A lista de substituições de agente de usuário fornecidas pela Microsoft.  

As substituições especificam novos valores de agente de usuário que Microsoft Edge envia em vez do agente de usuário padrão para sites específicos.  Para exibir a lista de substituições de agente de usuário aplicadas no momento, conclua as seguintes ações.  

1.  Abra o Microsoft Edge Beta ou canal Estável.  
1.  Navegue até `edge://compat/useragent`.  
    
Os Microsoft Edge canais Canary e Dev não recebem substituições de agente de usuário no momento.  Os Microsoft Edge canais Canary e Dev fornecem ambientes que usam o agente de usuário padrão Microsoft Edge usuário.  Use os canais Microsoft Edge Canary e Dev para reproduzir facilmente problemas em seu site causados pelo agente de usuário padrão Microsoft Edge usuário.  Para desativar as substituições do agente de usuário nos canais Microsoft Edge Beta ou Estável, conclua as seguintes ações.  

1.  Abra seu aplicativo de linha de comando.  
1.  Copie e colar o seguinte trecho de código.  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  Execute o Microsoft Edge usando o trecho de código.  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge para iOS e Android: o que os desenvolvedores precisam saber | Blogs Windows Microsoft"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. método getHighEntropyValues - User-Agent Dicas de Cliente | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementando a detecção de recursos | MDN"  
