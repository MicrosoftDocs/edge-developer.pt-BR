---
description: Usar o painel de emulação para testar perfis de navegador diferentes, tamanhos de tela e resoluções e coordenadas de localização do GPS
title: DevTools-emulação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, emulação de dispositivo, design responsivo, geolocalização, resolução
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561436"
---
# Emulação

O painel *emulação* ajuda você a:
 - Simular vários [perfis de dispositivo](#device), [navegadores](#browser-profile), [tamanhos de tela e resoluções](#display)
 - Testar diferentes [configurações de localização geográfica e coordenadas](#geolocation)

![O painel de emulação do Microsoft Edge DevTools](./media/emulation.png)

1. O botão de **configurações de emulação de persistência** salvará todas as alterações feitas nas configurações de emulação de área de trabalho padrão, mesmo quando você fechar e reabrir o devtools. 

2. O botão **Redefinir configurações de emulação** redefinirá as configurações de emulação para o perfil do navegador *da área de trabalho* padrão e a cadeia de caracteres do agente de usuário do Microsoft Edge com GPS desativado.

3. Quando qualquer uma dessas opções for alterada do padrão, a guia **emulação** mostrará um alerta informativo para indicar que algum aspecto do comportamento do seu navegador está sendo emulado.

## Dispositivo

Escolha em uma lista predefinida de perfis de dispositivo do Windows que configuram automaticamente as outras opções de emulação ou especifiquem seus próprios configuation *personalizados* . Volte para o *padrão* para redefinir todas as ferramentas de emulação.

## Modo

### Perfil do navegador
Uma maneira rápida de simular a página em execução em um dispositivo Windows Phone é alterar a configuração do **perfil do navegador** para *Windows Phone*.

#### Cadeia de caracteres do agente do usuário

Modificar sua cadeia de caracteres de agente do usuário para imitar outro navegador é uma boa primeira etapa em erros de depuração que ocorrem somente no Microsoft Edge. 

Os scripts de front-end e/ou back-end às vezes usam a cadeia de caracteres do agente do usuário para detectar qual navegador você está usando. E mesmo quando você não estiver usando a detecção do navegador em seu próprio código, talvez esteja usando uma biblioteca JavaScript ou um script do lado do servidor de terceiros.

O problema com a detecção do navegador é que ele é usado com frequência para redimensionar ou alterar os recursos em uma página da Web com base no que o desenvolvedor que escreve o script pensa que o seu navegador pode fazer, em vez de detectar o que o seu navegador pode realmente usar para a detecção de recursos. Isso pode causar um comportamento inesperado, porque o código direcionado para Windows Internet Explorer 8 pode ser executado de forma muito diferente no Microsoft Edge; ou um recurso que pode ser perfeitamente compatível com o seu navegador pode ser desabilitado por causa de uma pressuposição feita pelo desenvolvedor.

Se a alteração da cadeia de caracteres do agente do usuário apagar o problema, é provável que a detecção do navegador seja culpado.

## Vídeo

A emulação de exibição permite que você visualize seu site em diferentes tamanhos de tela e resoluções: de monitores convencionais de área de trabalho para telas de dispositivos móveis menores ou monitores de alta resolução mais recentes.

Emulações são adaptadas para experimentar e corresponderem às dimensões físicas das telas que estão sendo emuladas. Os pixels emulados podem parecer compactados ou expandidos, e a emulação não é recomendada se você precisar testar o posicionamento de pixels perfeitos dos elementos HTML. No entanto, a emulação é boa para testar designs responsivos e identificar problemas maiores de posicionamento de elementos.

### Orientação

Escolha em modo *paisagem* ou *retrato* .

### Resolução

Escolha uma lista predefinida de resoluções de dispositivos populares ou especifique sua configuração *personalizada* . Há suporte para resoluções de até 80 polegadas e 3820 x 2160.

## Geolocalização

Se o seu site usa a [API de geolocalização](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) para fornecer serviços baseados em localização, você pode testar facilmente diferentes coordenadas de GPS e Estados de sensor da conveniência da área de trabalho. Essas configurações substituirão todas as coordenadas reais do GPS e o estado do sensor nas máquinas que dão suporte à localização geográfica. 

Assim como qualquer uso de dados pessoais na Web, os usuários precisam primeiro conceder permissão a seu site para usar o local. Você pode testar como o seu site se comporta com e sem permissões de localização no painel *configurações* do Microsoft Edge:

**...** >  **Configurações**  >  de **Exibir configurações avançadas**  >  **Permissões**  >  de site **Gerenciar**

![Gerenciar permissões de site no painel configurações do Microsoft Edge](./media/settings_manage_permissions.png)

## Teclado

| Ação                   | Atalho               |
|:-------------------------|:-----------------------|
| Redefinir configurações de emulação | `CTRL` + `SHIFT` + `L` |
