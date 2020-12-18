---
description: Garantir que o conteúdo de mídia em seu site se destine conforme o esperado
title: Políticas de reprodução automática-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: borda, mídia, vídeo, áudio, reprodução automática
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 85b91a8b87d73d6fccc6eac2aa64513f283d7f21
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231532"
---
# Políticas de reprodução automática  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

O Microsoft Edge fornece aos clientes a capacidade de personalizar suas preferências de navegação em sites que a mídia de reprodução automática com som para minimizar distrações na Web e conservar a largura de banda.  Além disso, o Microsoft Edge automaticamente suprime a reprodução automática de mídia em guias de plano de fundo.  

Os usuários podem personalizar o comportamento de mídia com os controles de reprodução automática [global](#global-media-autoplay-settings) e [por site](#per-site-media-autoplay-settings) , que fornecem as seguintes opções:  

*   `Allow`  O padrão e continuarão a reproduzir vídeos quando uma guia for exibida primeiro em primeiro plano, no caso do site.  

*   `Limit`  Restringe a reprodução automática para funcionar apenas quando os vídeos estiverem em mudo, para que os usuários nunca fiquem surpresos com o som.  Quando o usuário clica em qualquer lugar na página, a reprodução automática é habilitada novamente e continuará a ser permitida dentro desse domínio nessa guia.  

*   `Block`  Evite o sautoplay em todos os sites até que os usuários interajam diretamente com o conteúdo de mídia.  

## Configurações de reprodução automática de mídia global  

Os usuários podem controlar o comportamento de reprodução automática padrão para todos os sites em **Configuração avançada**  >  **reprodução automática de mídia**.  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Configurações de reprodução automática de mídia global" lightbox="../media/autoplay_global.png":::
   Configurações de reprodução automática de mídia global  
:::image-end:::  

## Configurações de reprodução automática de mídia por site  

Os usuários podem controlar o comportamento da reprodução automática em cada site, na seção **permissões do site** do painel de informações do site.  Essa configuração pode ser encontrada clicando no ícone de informações ou no ícone de cadeado no lado esquerdo da barra de endereços e clicando em **configurações de reprodução automática de mídia** para começar.  

As configurações por site substituem a configuração global.  Por exemplo, se um usuário tiver sua configuração global definida como, `Allow` mas alterar uma configuração por site para `Block` , a reprodução automática será bloqueada para esse site.  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Configurações de reprodução automática de mídia por site" lightbox="../media/autoplay_per-site.png":::
   Configurações de reprodução automática de mídia por site  
:::image-end:::  

## Práticas recomendadas para desenvolvedores da Web  

Veja como garantir uma boa experiência do usuário com mídia hospedada em seu site:  

*   Suponha que cada uso de um elemento de mídia ouvirá exija um gesto do usuário para iniciar a reprodução \ (à medida que os usuários podem bloquear a reprodução automática em qualquer point-in-time \) e planeje-se adequadamente.  Políticas de reprodução automática global e por site aplicam-se a todos os `<audio>` `<video>` elementos, independentemente de como eles são usados no seu site  

*   Verifique se os controles de mídia estão sempre presentes na mídia de site e no conteúdo do anúncio.  Isso dará aos usuários a capacidade de reiniciar a reprodução se a reprodução automática estiver bloqueada na página.  

*   Avalie como a reprodução automática pode afetar a experiência dos usuários no seu site e considere o uso da reprodução automática de forma a minimizar a reprodução de mídia indesejada.  Se a reprodução automática for uma parte crucial da sua experiência, considere o uso de conteúdo sem áudio para iniciar e permitir que o usuário o ative.  Para que o conteúdo seja ativado para a reprodução automática, a fonte de áudio deve ser ativada ou desativada explicitamente.  Caso contrário, o elemento não será considerado mudo.  

*   A menos que seja absolutamente necessário fazer o contrário, use os controles nativos do navegador para reprodução de mídia.  Isso irá assegurar uma experiência consistente para os usuários.  Se você estiver criando controles personalizados em vez disso, verifique se os controles de mídia estão sempre presentes e se seus controles reagir corretamente à supressão da reprodução automática.  

### Delegação de iframe  

A reprodução automática em uma `<iframe>` herdará a permissão de reprodução automática da página pai, independentemente da origem do conteúdo.  Em um cenário de playlist em que cada arquivo de mídia é hospedado por um iframe separado, o usuário só precisaria iniciar uma reprodução uma vez para toda a playlist.  

### Detectando quando a reprodução automática é permitida  

Você pode ajustar os controles de reprodução para exibir o estado correto quando a reprodução automática estiver bloqueada examinando a promessa retornada pela `play()` função no elemento de mídia:  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  
