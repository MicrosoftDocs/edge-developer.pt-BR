---
description: Usar o painel de emulação para testar perfis de navegador diferentes, tamanhos de tela e resoluções e coordenadas de localização do GPS
title: DevTools-emulação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, emulação de dispositivo, design responsivo, geolocalização, resolução
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231483"
---
# Emulação  

> [!NOTE]
> O novo Microsoft Edge é criado usando o Chromium e começa na versão 75.  Para obter mais informações, [Baixe o novo Microsoft Edge][MicrosoftNewEdge]e experimente as novas [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromium].  
> 
> Para emular diferentes dispositivos, navegadores, tamanhos de tela e resoluções no novo DevTools, navegue para [emular dispositivos móveis no Microsoft Edge \ (Chromium \) devtools][DevtoolsGuideChromiumDeviceMode].  

O painel **emulação** ajuda nas seguintes atividades.    

*   Simular vários [perfis de dispositivo](#device), [navegadores](#browser-profile)e [tamanhos de tela e resoluções](#display)  
*   Testar diferentes [configurações de localização geográfica e coordenadas](#geolocation)  

:::image type="complex" source="./media/emulation.png" alt-text="O painel de emulação do Microsoft Edge DevTools" lightbox="./media/emulation.png":::
   O painel de **emulação** do Microsoft Edge devtools  
:::image-end:::  

1.  O botão de **configurações de emulação de persistência** salva todas as alterações feitas nas configurações de emulação de área de trabalho padrão, mesmo quando você fecha e reabre o devtools.  

1.  O botão **Redefinir configurações de emulação** redefine as configurações de emulação de volta para o perfil do navegador da área de trabalho padrão e a cadeia de caracteres do agente de usuário do Microsoft Edge com GPS desativado.  

1.  Quando qualquer uma dessas opções for alterada do padrão, a guia **emulação** exibirá um alerta informativo para indicar que algum aspecto do comportamento do seu navegador está sendo emulado.  

## Dispositivo  

Escolha uma lista predefinida de perfis de dispositivo do Windows que configuram automaticamente as outras opções de emulação ou especifiquem sua própria configuração **personalizada** .  Volte para o **padrão** para redefinir todas as ferramentas de emulação.  

## Modo  

### Perfil do navegador  

Uma maneira rápida de simular a página em execução em um dispositivo Windows Phone é alterar a configuração do **perfil do navegador** para **Windows Phone**.  

#### Cadeia de caracteres do agente do usuário  

Modificar sua cadeia de caracteres de agente do usuário para imitar outro navegador é uma boa primeira etapa em erros de depuração que ocorrem somente no Microsoft Edge.  

Os scripts usam a cadeia de caracteres do agente do usuário para detectar qual navegador é usado.  O script pode ser front-end, back-end ou front-end e back-end.  Embora o código não use a detecção do navegador, o código pode herdar de uma biblioteca JavaScript ou script do lado do servidor de terceiros.  

O problema com a detecção do navegador é que você pode redimensionar \ (ou alterar \) recursos em sua página da Web usando pressuposições sobre recursos do navegador. Em vez disso, você deve considerar o uso da detecção de recursos para detectar os recursos do seu navegador.  Um comportamento inesperado pode ocorrer devido a uma das seguintes situações.  

*   O código direcionado para Windows Internet Explorer 8 pode funcionar de forma diferente no Microsoft Edge.  
*   Um recurso ao qual o seu navegador deve oferecer suporte está desabilitado, devido a uma pressuposição feita pelo desenvolvedor.  

Se a alteração da cadeia de caracteres do agente do usuário apagar o problema, é provável que a detecção do navegador seja culpado.  

## Vídeo  

Emulação de exibição para visualizar o site em diferentes tamanhos de tela e resoluções.  

*   monitores convencionais para área de trabalho  
*   telas móveis menores  
*   monitores de alta resolução mais recentes  

Emulações são adaptadas para tentar corresponderem às dimensões físicas das telas que estão sendo emuladas.  Os pixels emulados podem aparecer compactados ou expandidos. A emulação não será recomendada se você precisar testar o posicionamento perfeito de pixels dos elementos HTML.  No entanto, a emulação é boa para testar designs responsivos e identificar problemas maiores de posicionamento de elementos.  

### Orientação  

Escolha em modo **paisagem** ou **retrato** .  

### Resolução  

Escolha uma lista predefinida de resoluções de dispositivos populares ou especifique sua configuração **personalizada** .  Há suporte para resoluções de até 80 polegadas e 3820 x 2160.  

## Geolocalização  

Se o seu site usa a [API geolocalização][MdnGeolocationUsing] para fornecer serviços baseados em localização, as seguintes atividades estão disponíveis na conveniência da área de trabalho.  

*   testar facilmente diferentes coordenadas do GPS  
*   testar facilmente diferentes Estados do sensor  

As configurações substituem todas as coordenadas reais do GPS e o estado do sensor em dispositivos que dão suporte a geolocalização.  

Seu site deve solicitar e receber permissão de um usuário antes de usar o local do dispositivo.  Teste como o seu site se comporta com e sem permissões de localização no painel **configurações** do Microsoft Edge.  

**...** >  **Configurações**  >  de **Exibir configurações avançadas**  >  **Permissões**  >  de site **Gerenciar**  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Gerenciar permissões de site no painel configurações do Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   Gerenciar permissões de site no painel **configurações** do Microsoft Edge  
:::image-end:::  

## Atalhos

| Ação  | Atalho  |  
|:--- |:--- |  
| Redefinir configurações de emulação | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Baixar novo navegador Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API de geolocalização | MDN"  
