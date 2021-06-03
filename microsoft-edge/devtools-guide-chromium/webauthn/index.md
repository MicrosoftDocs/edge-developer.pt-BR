---
description: Emular Autenticadores e Depurar WebAuthn no Microsoft Edge DevTools.
title: Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d5eeedfaa98e56bbba81634685a223844803a1ad
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564032"
---
# <a name="emulate-authenticators-and-debug-webauthn-in-microsoft-edge-devtools"></a>Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools  

Em vez de depurar a Autenticação Web em seu site ou aplicativo com autenticadores físicos, use a ferramenta **WebAuthn** no Microsoft Edge DevTools para criar e interagir com autenticadores virtuais baseados em software.  

## <a name="before-you-begin"></a>Antes de começar  

Um ótimo lugar para começar a autenticação da Web é a [especificação da API de Autenticação da Web.][GithubW3cWebauthn]  

## <a name="set-up-the-webauthn-tool"></a>Configurar a ferramenta WebAuthn  

1.  Navegue até uma página da Web que usa WebAuthn, como o seguinte site de demonstração.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Entre no site.  
1.  [Abra DevTools][DevtoolsGuideChromiumOpen].  
1.  Para abrir a **ferramenta WebAuthn,** escolha o ícone Personalizar e controlar **DevTools** \( \) > `...` Mais **ferramentas**  >  **WebAuthn**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Ferramenta WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       **Ferramenta WebAuthn**  
    :::image-end:::  
    
1.  Na ferramenta **WebAuthn,** ative a caixa de seleção Habilitar ambiente **de autenticador virtual.**  
1.  Depois de habilitada, uma nova seção chamada **Novo autenticador** é exibida.  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Habilitar ambiente de autenticador virtual" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Habilitar ambiente de autenticador virtual**  
    :::image-end:::  
    
1.  Na seção **Novo autenticador,** configure as seguintes opções.  
    
    | Opção | Value | Detalhes |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | O protocolo que o autenticador virtual usa para codificação e decodificação |  
    | `Transport` |   `usb`, `nfc` `ble` , ou `internal` | O autenticador virtual simula o transporte selecionado para se comunicar com clientes para obter uma declaração para uma credencial específica.  Para obter mais informações, navegue [até Authenticator Enumeração de Transporte][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Ativar \(ou desativar\) usando a caixa de seleção | A ativar se o aplicativo Web depende de chaves de residente \(também conhecidas como credenciais de descoberta do lado do cliente\).  Para obter mais informações, navegue até [Enumeração de Requisitos de Chave de Residente][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Ativar \(ou desativar\) usando a caixa de seleção | A opção Ativar se seu aplicativo Web depende da autorização local usando modalidades de gesto, como código de toque e pino, entrada de senha ou reconhecimento biométrico.  Para obter mais informações, navegue até [Verificação do Usuário][GithubW3cWebauthnEnumUserverification] |  
    
1.  Escolha o **botão Adicionar.**  
1.  Uma nova seção do autenticador recém-criado é exibida.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
A **Authenticator** inclui uma tabela **Credentials.**  A tabela está vazia até que uma credencial seja registrada no autenticador.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Sem credenciais" lightbox="../media/webauthn-no-cred.msft.png":::
   Sem credenciais  
:::image-end:::  

## <a name="register-a-new-credential"></a>Registrar uma nova credencial  

Para registrar uma nova credencial, conclua as etapas a seguir.  Para obter mais informações sobre o que a API de Autenticação [da Web][GithubW3cWebauthn] está fazendo ao registrar uma nova credencial, navegue até Criar uma [nova credencial.][GithubW3cWebauthnSctnCreatecredential]  

1.  No site de demonstração, escolha **Registrar nova credencial.**  
1.  Uma nova credencial agora é adicionada à tabela **Credenciais** na ferramenta WebAuthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Exibir credenciais" lightbox="../media/webauthn-view-cred.msft.png":::
       Exibir credenciais  
    :::image-end:::  
    
No site de demonstração, escolha o **botão Autenticar.**  Verifique se a [Contagem de][GithubW3cWebauthnSctnSignCounter] Sinais da credencial na tabela **Credenciais** aumentou 1, o que marca uma operação bem-sucedida [do autenticadorGetAssertion.][GithubW3cWebauthnAuthenticatorgetassertion]  

## <a name="export-and-remove-credentials"></a>Exportar e remover credenciais  

Para exportar ou remover uma credencial, escolha o **botão Exportar** ou **Remover.**  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportar ou remover uma credencial" lightbox="../media/webauthn-export-remove.msft.png":::
   Exportar ou remover uma credencial  
:::image-end:::  

## <a name="rename-an-authenticator"></a>Renomear um autenticador  

Para renomear um autenticador, conclua as etapas a seguir.  

1.  Ao lado do nome do autenticador, escolha o **botão Editar.**  
1.  Edite o nome e escolha **Enter** para salvar as alterações.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Renomear um autenticador" lightbox="../media/webauthn-rename.msft.png":::
   Renomear um autenticador  
:::image-end:::  

## <a name="set-the-active-authenticator"></a>Definir o autenticador ativo  

Um autenticador recém-criado é ativado automaticamente.  Para usar outro autenticador virtual, escolha o botão de rádio **Ativo** ao lado do autenticador.  

> [!NOTE]
> O DevTools oferece suporte a apenas um autenticador virtual ativo a qualquer momento.  Se você remover o autenticador ativo, outro autenticador não será ativado automaticamente.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Definir autenticador ativo" lightbox="../media/webauthn-set-active.msft.png":::
   Definir autenticador ativo  
:::image-end:::  

## <a name="remove-a-virtual-authenticator"></a>Remover um autenticador virtual  

Para remover um autenticador virtual, ao lado do autenticador, escolha o **botão Remover.**  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Remover autenticador" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Remover autenticador  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demonstração webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Cliente para Authenticator Protocolo (CTAP) | fido alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Visão geral do Fator 2nd Universal (U2F) | fido alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "A operação authenticatorGetAssertion - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Enumeração de Transporte (enumeração AuthenticatorTransport) - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeração de Requisitos de Chave de Residente (enumeração ResidentKeyRequirement) - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Verificação do usuário - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Criar uma nova credencial - Método [[Create]]](origin, options, sameOriginWithAncestors) - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considerações sobre o contador de assinaturas - Autenticação da Web: uma API para acessar credenciais de chave pública nível 2 | GitHub"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
