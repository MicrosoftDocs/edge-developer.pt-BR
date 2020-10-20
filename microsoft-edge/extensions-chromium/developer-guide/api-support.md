---
description: Lista de APIs com suporte a serem usadas ao criar extensões do Microsoft Edge.
title: APIs com suporte para extensões do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, API de extensão, desenvolvedor, desenvolvimento da Web
ms.openlocfilehash: 868473393da6cefbf146fb7acd6c9816903bd253
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120386"
---
# APIs com suporte para extensões do Microsoft Edge

A tabela a seguir fornece uma lista de APIs que você pode usar ao criar extensões para o navegador Microsoft Edge \ (Chromium \).

| API                                   | Descrição                                            
|---------------------------------------|----------------------------------------------------------|
| [alarmes](https://developer.chrome.com/extensions/alarms) | Agende o código para executar periodicamente ou em um horário especificado no futuro. |
| [indicadores](https://developer.chrome.com/extensions/bookmarks) | Criar, organizar e manipular indicadores. |
| [BrowserAction](https://developer.chrome.com/extensions/browserAction) | Use ações do navegador para colocar ícones na barra de ferramentas do Microsoft Edge. Você também pode usar ações do navegador para adicionar uma dica de ferramenta, um emblema ou um pop-up. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Remover dados de navegação do perfil local de um usuário. |
| [comandos](https://developer.chrome.com/extensions/commands) | Adicione atalhos de teclado que acionem ações na extensão. Por exemplo, uma ação para abrir o navegador ou enviar um comando para a extensão. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | Em geral, as configurações de conteúdo permitem que você personalize o comportamento do Microsoft Edge em cada site, em vez de globalmente. Altere as configurações que controlam se os sites podem usar recursos como cookies, JavaScript e plugins. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Adicionar itens ao menu de contexto no Microsoft Edge. Itens de menu podem ser aplicados a objetos diferentes, como imagens, hiperlinks e páginas. |
| [cookies](https://developer.chrome.com/extensions/cookies) | Consultar e modificar cookies e receber notificações quando forem alterados. |
| [depurador](https://developer.chrome.com/extensions/debugger) | Anexe a uma ou mais guias para instrumentar a interação de rede, Depurar JavaScript, alterar o DOM, alterar CSS e assim por diante. Use o depurador tabId para direcionar as guias com sendCommand e encaminhar eventos por tabId de retornos de chamada OnEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Tome medidas dependendo do conteúdo de uma página, sem precisar de permissão para ler o conteúdo da página. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Fornece mais privacidade bloqueando ou modificando solicitações de rede especificando regras declarativas. Permita que as extensões modifiquem solicitações de rede sem interceptar a solicitação e exibir o conteúdo. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Capture o conteúdo de uma tela, janelas individuais ou guias. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interagir com a janela inspecionada. Por exemplo, obtenha a ID da guia de páginas, avalie o código, recarregue páginas ou obtenha recursos em uma página. |
| [rede devtools.](https://developer.chrome.com/extensions/devtools_network) | Recuperar informações sobre as solicitações de rede exibidas pelas ferramentas de desenvolvedor no painel rede. |
| [devtools. panels](https://developer.chrome.com/extensions/devtools.panels) | Integre a extensão à interface do usuário da janela ferramentas de desenvolvedor criando seus próprios painéis, acessando painéis existentes ou adicionando barras laterais. |
| [downloads](https://developer.chrome.com/extensions/downloads) | Iniciar, monitorar, manipular e Pesquisar downloads por programação. |
| [Enterprise. hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Obtenha o fabricante e o modelo da plataforma de hardware onde o navegador é executado. Esta API só está disponível para extensões instaladas pela política empresarial. |
| [MouseUp](https://developer.chrome.com/extensions/events) | Tipos comuns usados por APIs que geram eventos para notificá-lo quando ocorre um evento interessante. |
| [prorroga](https://developer.chrome.com/extensions/extension) | Qualquer página de extensão pode usar os utilitários desta API. Ele inclui suporte para troca de mensagens entre extensões e scripts de conteúdo, que é descrita em transmissão de mensagens. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Contém declarações de tipo para extensões do Microsoft Edge. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Gerenciar configurações de fonte no Microsoft Edge. |
| [histórico](https://developer.chrome.com/extensions/history) | Interagir com o registro de páginas visitadas do navegador. Você pode adicionar, remover ou consultar URLs no histórico do navegador. Para substituir a página de histórico pela sua própria versão, consulte substituir páginas. |
| [nacional](https://developer.chrome.com/extensions/i18n) | Implementar a internacionalização em todo o aplicativo ou ramal. |
| [ociosidade](https://developer.chrome.com/extensions/idle) | Detectar quando o estado ocioso da máquina muda. |
| [gerencia](https://developer.chrome.com/extensions/management) | Gerenciar a lista de extensões instaladas ou em execução. Isso é útil para extensões que substituem a página da nova guia interna. |
| [notificações](https://developer.chrome.com/extensions/notifications) | Criar notificações avançadas usando modelos e exibi-los na bandeja do sistema. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Registre palavras-chave na barra de endereços do Microsoft Edge, também conhecido como Omnibox. |
| [página de anotações](https://developer.chrome.com/extensions/pageAction) | Adicione ícones à barra de ferramentas do Microsoft Edge à direita da barra de endereços. Ações de página são ações que podem ser executadas na página atual e não são aplicáveis a todas as páginas. As ações da página aparecem esmaecidas quando inativas. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Salvar guias como arquivos MHTML.|
| [Elas](https://developer.chrome.com/extensions/permissions) | Recuperar permissões declaradas e opcionais em tempo de execução, em vez de no momento da instalação. Você pode usar essa API para exibir as permissões necessárias e aprovadas para os usuários. |
| [Ligar/Desligar](https://developer.chrome.com/extensions/power) | Substituir os recursos de gerenciamento de energia do sistema. |
| [printerprovider](https://developer.chrome.com/extensions/printerProvider) | Use eventos para consultar impressoras, suas funcionalidades e enviar trabalhos de impressão. |
| [privacidade](https://developer.chrome.com/extensions/privacy) | Recursos de controle no Microsoft Edge que afetam a privacidade de um usuário. Essa API depende do `EdgeSetting` protótipo de `types` para obter e definir a configuração do Microsoft Edge. |
| [proxy](https://developer.chrome.com/extensions/proxy) | Gerenciar configurações de proxy para o Microsoft Edge. Essa API depende do `EdgeSetting` protótipo da `types` API para obter e definir a configuração de proxy do Microsoft Edge. |
| [classpath](https://developer.chrome.com/extensions/runtime) | Recupere a página de plano de fundo, retorne os detalhes sobre o manifesto e ouça e responda a eventos no aplicativo ou na extensão do ciclo de vida. Você também pode converter o caminho relativo de URLs para URLs totalmente qualificadas. |
| [sessões](https://developer.chrome.com/extensions/sessions) | Consultar e restaurar guias e janelas de uma sessão de navegação. |
| [armazenamento](https://developer.chrome.com/extensions/storage) | Armazene, recupere e controle as alterações dos dados do usuário. |
| [System. Memory](https://developer.chrome.com/extensions/system_memory) | A `system.memory` API. |
| [System. Storage](https://developer.chrome.com/extensions/system_storage) | Consultar informações sobre dispositivos de armazenamento. Você também pode receber notificações quando dispositivos de armazenamento são anexados ou desconectados. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interagir com fluxos de mídia de guia. |
| [efetua](https://developer.chrome.com/extensions/tabs) | Interaja com o sistema de guia do navegador para criar, modificar e reorganizar guias. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Acesse os sites principais, também chamados de sites mais visitados, que são exibidos na página da nova guia. Esses sites não incluem atalhos personalizados pelo usuário. |
| [TTS](https://developer.chrome.com/extensions/tts) | Executar conversão de texto em fala sintetizada (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implemente um mecanismo de conversão de texto em fala (TTS) usando uma extensão. As extensões que se registram para usar essa API recebem eventos que contêm expressões a serem falados e outros parâmetros. As extensões podem então usar qualquer tecnologia da Web disponível para resumir e produzir voz e enviar eventos de volta para a função de chamada para relatar o status. |
| [tipos](https://developer.chrome.com/extensions/types) | Declarações de tipo para Microsoft Edge. |
| [webnavigation](https://developer.chrome.com/extensions/webNavigation) | Receber notificações sobre o status das solicitações de navegação. |
| [webRequest](https://developer.chrome.com/extensions/webRequest) | Observar e analisar o tráfego. Interceptar, bloquear ou modificar solicitações. |
| [windows](https://developer.chrome.com/extensions/windows) | Interaja com janelas do navegador para criar, modificar e reorganizar janelas no navegador. |



## APIs de extensão sem suporte

O Microsoft Edge não oferece suporte às seguintes APIs de extensão:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` -Como alternativa, você pode usar `launchWebAuthFlow` para buscar um token OAuth2 para autenticar usuários.
* `chrome.instanceID`.


## Considerações adicionais para APIs com suporte

* O usuário deve estar conectado ao Microsoft Edge usando um MSA ou uma conta do Azure Active Directory para usar `chrome.identity.getProfileUserInfo` . Se o usuário estiver conectado ao Microsoft Edge usando uma conta local do Active Directory, a API retornará `null` para os valores de email e ID.

* O Microsoft Edge não oferece suporte a extensões que usam pagamentos do Chrome Web Store porque ele usa `identity.getAuthtoken` para solicitar tokens para os usuários conectados. Esses tokens são enviados para a API de licenciamento baseado em REST. 


<!-- links -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/apps/external_extensions).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
