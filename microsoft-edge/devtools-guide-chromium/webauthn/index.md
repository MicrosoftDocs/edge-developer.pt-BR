---
description: Emular autenticadores e depurar webauthn no Microsoft Edge DevTools.
title: Emular autenticadores e depurar webauthn no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3200f22485bfd642a37a7d34ac727b8da4500d06
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231178"
---
# Emular autenticadores e depurar webauthn no Microsoft Edge DevTools  

Em vez de fazer a depuração da autenticação da Web em seu site ou aplicativo com autenticadores físicos, use a ferramenta **Webauthn** no Microsoft Edge devtools para criar e interagir com os autenticadores virtuais baseados em software.  

## Antes de começar  

Um ótimo lugar para começar a autenticação na Web é a [especificação da API de autenticação da Web][GithubW3cWebauthn].  

## Configurar a ferramenta webauthn  

1.  Navegue até uma página da Web que usa webauthn, como o site de demonstração a seguir.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Conecte-se ao website.  
1.  [Abra o devtools][DevtoolsGuideChromiumOpen].  
1.  Para abrir a ferramenta **webauthn** , escolha o ícone **Personalizar e controlar devtools** \ ( `...` \) > **mais ferramentas**  >  **webauthn**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Ferramenta webauthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       Ferramenta **Webauthn**  
    :::image-end:::  
    
1.  Na ferramenta **Webauthn** , ative a caixa de seleção **habilitar ambiente de autenticador virtual** .  
1.  Depois de habilitado, uma nova seção chamada **novo autenticador** será exibida.  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Habilitar o ambiente do autenticador virtual" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Habilitar o ambiente do autenticador virtual**  
    :::image-end:::  
    
1.  Na seção **novo autenticador** , configure as seguintes opções.  
    
    | Opção | Valor | Detalhes |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] ou [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | O protocolo que o autenticador virtual usa para codificar e decodificar |  
    | `Transport` |   `usb`, `nfc` , `ble` , ou `internal` | O autenticador virtual simula o transporte selecionado para comunicação com clientes para obter uma asserção para uma credencial específica.  Para obter mais informações, navegue até [enumeração de transporte do autenticador][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Ative \ (ou desligado \) usando a caixa de seleção | Ative se o seu aplicativo Web depende de chaves residentes \ (também conhecidas como credenciais detectável do lado do cliente \).  Para obter mais informações, navegue até [enumeração de requisitos da chave residente][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Ative \ (ou desligado \) usando a caixa de seleção | Ative se o seu aplicativo Web depende da autorização local usando as modalidades de gesto como toque e código PIN, entrada de senha ou reconhecimento biométrico.  Para obter mais informações, navegue até [verificação do usuário][GithubW3cWebauthnEnumUserverification] |  
    
1.  Escolha o botão **Adicionar** .  
1.  Uma nova seção de seu autenticador recém-criado será exibida.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
A seção do **autenticador** inclui uma tabela de **credenciais** .  A tabela estará vazia até que uma credencial seja registrada no autenticador.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Nenhuma credencial" lightbox="../media/webauthn-no-cred.msft.png":::
   Nenhuma credencial  
:::image-end:::  

## Registrar uma nova credencial  

Para registrar uma nova credencial, conclua as etapas a seguir.  Para obter mais informações sobre o que a [API de autenticação da Web][GithubW3cWebauthn] está fazendo ao registrar uma nova credencial, navegue para [criar uma nova credencial][GithubW3cWebauthnSctnCreatecredential].  

1.  No site de demonstração, escolha **registrar nova credencial**.  
1.  Uma nova credencial agora é adicionada à tabela de **credenciais** na ferramenta webauthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Exibir credenciais" lightbox="../media/webauthn-view-cred.msft.png":::
       Exibir credenciais  
    :::image-end:::  
    
No site de demonstração, escolha o botão **autenticar** .  Verifique se a [contagem de sinal][GithubW3cWebauthnSctnSignCounter] da credencial na tabela de **credenciais** aumentou em 1, que marca uma operação [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] bem-sucedida.  

## Exportar e remover credenciais  

Para exportar ou remover uma credencial, escolha o botão **Exportar** ou **remover** .  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportar ou remover uma credencial" lightbox="../media/webauthn-export-remove.msft.png":::
   Exportar ou remover uma credencial  
:::image-end:::  

## Renomear um autenticador  

Para renomear um autenticador, conclua as etapas a seguir.  

1.  Ao lado do nome do autenticador, escolha o botão **Editar** .  
1.  Edite o nome e escolha **Enter** para salvar as alterações.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Renomear um autenticador" lightbox="../media/webauthn-rename.msft.png":::
   Renomear um autenticador  
:::image-end:::  

## Definir o autenticador ativo  

Um autenticador recém-criado é ativado automaticamente.  Para usar outro autenticador virtual, escolha o botão de opção **ativo** ao lado do autenticador.  

> [!NOTE]
> O DevTools oferece suporte a apenas um autenticador virtual ativo em qualquer point-in-time.  Se você remover o autenticador ativo, outro autenticador não será ativado automaticamente.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Definir autenticador ativo" lightbox="../media/webauthn-set-active.msft.png":::
   Definir autenticador ativo  
:::image-end:::  

## Remover um autenticador virtual  

Para remover um autenticador virtual, ao lado do autenticador, escolha o botão **remover** .  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Remover autenticador" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Remover autenticador  
:::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demonstração webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocolo de cliente para autenticador (CTAP) | Fido Alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Visão geral do 2º fator (U2F) universal | Fido Alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação na Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "A operação authenticatorGetAssertion-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Enumeração de transporte autenticador (Enumeração AuthenticatorTransport)-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeração de requisito de chave residente (Enumeração ResidentKeyRequirement)-autenticação da Web: uma API para acessar o nível 2 das credenciais de chave pública | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Verificação do usuário – autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Criar um novo método Credential-PublicKeyCredential [[Create]] (Origin, Options, sameOriginWithAncestors)-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Considerações do contador de assinatura-autenticação da Web: uma API para acessar as credenciais de chave pública nível 2 | GitHub"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
