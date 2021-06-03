---
description: Lista de APIs com suporte a ser usada ao criar Microsoft Edge extensões.
title: APIs com suporte para Microsoft Edge extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, api de extensão, desenvolvedor, desenvolvimento da Web
ms.openlocfilehash: 20e924b5c973b9ecd433feeb3a772c6d17746369
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398102"
---
# <a name="supported-apis-for-microsoft-edge-extensions"></a>APIs com suporte para Microsoft Edge extensões

A tabela a seguir fornece uma lista de APIs que você pode usar ao criar extensões para o navegador Microsoft Edge \(Chromium\).

| API                                   | Descrição                                            
|---------------------------------------|----------------------------------------------------------|
| [alarmes](https://developer.chrome.com/extensions/alarms) | Agende o código para ser executado periodicamente ou em um horário especificado no futuro. |
| [indicadores](https://developer.chrome.com/extensions/bookmarks) | Criar, organizar e manipular indicadores. |
| [browserAction](https://developer.chrome.com/extensions/browserAction) | Use ações do navegador para colocar ícones na barra de ferramentas Microsoft Edge. Você também pode usar ações do navegador para adicionar uma dica de ferramenta, selo ou pop-up. |
| [browsingData](https://developer.chrome.com/extensions/browsingData) | Remova os dados de navegação do perfil local de um usuário. |
| [comandos](https://developer.chrome.com/extensions/commands) | Adicione atalhos de teclado que disparam ações em sua extensão. Por exemplo, uma ação para abrir o navegador ou enviar um comando para a extensão. |
| [contentSettings](https://developer.chrome.com/extensions/contentSettings) | Em geral, as configurações de conteúdo permitem personalizar o comportamento da Microsoft Edge em cada site, em vez de globalmente. Altere as configurações que controlam se os sites podem usar recursos como cookies, JavaScript e plug-ins. |
| [contextMenus](https://developer.chrome.com/extensions/contextMenus) | Adicione itens ao menu de contexto no Microsoft Edge. Os itens de menu podem ser aplicados a objetos diferentes, como imagens, hiperlinks e páginas. |
| [cookies](https://developer.chrome.com/extensions/cookies) | Consultar e modificar cookies e receber notificações quando eles mudarem. |
| [depurador](https://developer.chrome.com/extensions/debugger) | Anexe a uma ou mais guias à interação de rede de instrumentos, depure JavaScript, altere o DOM, altere CSS e assim por diante. Use a guia depurador TabId para direcionar guias com sendCommand e roteie eventos por tabId de retornos de chamada onEvent. |
| [declarativeContent](https://developer.chrome.com/extensions/declarativeContent) | Tome ações dependendo do conteúdo de uma página, sem exigir permissão para ler o conteúdo da página. |
| [declarativeNetRequest](https://developer.chrome.com/extensions/declarativeNetRequest) | Fornece mais privacidade bloqueando ou modificando solicitações de rede especificando regras declarativas. Permitir extensões para modificar solicitações de rede sem interceptar a solicitação e exibir o conteúdo. |
| [desktopCapture](https://developer.chrome.com/extensions/desktopCapture) | Capture o conteúdo de uma tela, janelas individuais ou guias. |
| [devtools.inspectedWindow](https://developer.chrome.com/extensions/devtools_inspectedWindow) | Interaja com a janela inspecionada.  Por exemplo, obtenha a ID da guia de páginas, avalie o código, atualize páginas ou obtenha recursos em uma página. |
| [devtools.network](https://developer.chrome.com/extensions/devtools_network) | Recupere informações sobre solicitações de rede exibidas pelas Ferramentas de Desenvolvedor no painel Rede. |
| [devtools.panels](https://developer.chrome.com/extensions/devtools.panels) | Integre sua extensão à interface do usuário da janela Ferramentas do Desenvolvedor criando seus próprios painéis, acessando painéis existentes ou adicionando barras laterais. |
| [downloads](https://developer.chrome.com/extensions/downloads) | Inicie, monitore, manipule e pesquise programaticamente os downloads. |
| [enterprise.hardwarePlatform](https://developer.chrome.com/extensions/enterprise.hardwarePlatform) | Obter o fabricante e o modelo da plataforma de hardware em que o navegador é executado. Essa API só está disponível para extensões instaladas pela política empresarial. |
| [events](https://developer.chrome.com/extensions/events) | Tipos comuns usados por APIs que levantam eventos para notificar você quando ocorre um evento interessante. |
| [extension](https://developer.chrome.com/extensions/extension) | Qualquer página de extensão pode usar os utilitários desta API. Ele inclui suporte para trocar mensagens entre extensões e scripts de conteúdo, que é descrito em Passagem de Mensagens. |
| [extensionTypes](https://developer.chrome.com/extensions/extensionTypes) | Contém declarações de tipo para Microsoft Edge extensões. |
| [fontSettings](https://developer.chrome.com/extensions/fontSettings) | Gerenciar configurações de fonte em Microsoft Edge. |
| [histórico](https://developer.chrome.com/extensions/history) | Interaja com o registro do navegador de páginas visitadas. Você pode adicionar, remover ou consultar URLs no histórico do navegador. Para substituir a página de histórico pela sua própria versão, navegue até Substituir Páginas. |
| [i18n](https://developer.chrome.com/extensions/i18n) | Implemente a internacionalização em todo o aplicativo ou extensão. |
| [idle](https://developer.chrome.com/extensions/idle) | Detectar quando o estado ocioso do computador muda. |
| [management](https://developer.chrome.com/extensions/management) | Gerencie a lista de extensões instaladas ou em execução. É útil para extensões que substituem a página Nova Guia. |
| [notificações](https://developer.chrome.com/extensions/notifications) | Crie notificações ricas usando modelos e as exibe na bandeja do sistema. |
| [omnibox](https://developer.chrome.com/extensions/omnibox) | Registre palavras-chave na barra Microsoft Edge endereço, também conhecida como omnibox. |
| [pageAction](https://developer.chrome.com/extensions/pageAction) | Adicione ícones à Microsoft Edge de ferramentas, à direita da barra de endereços. As ações de página são ações que podem ser tomadas na página atual e não são aplicáveis a todas as páginas. As ações de página aparecem acinzenadas quando inativas. |
| [pageCapture](https://developer.chrome.com/extensions/pageCapture) | Salvar guias como arquivos MHTML.|
| [permissions](https://developer.chrome.com/extensions/permissions) | Recupere permissões declaradas e opcionais no tempo de execução, em vez de no momento da instalação. Você pode usar essa API para exibir permissões necessárias e aprovadas para seus usuários. |
| [Ligar/Desligar](https://developer.chrome.com/extensions/power) | Substitua os recursos de gerenciamento de energia do sistema. |
| [printerProvider](https://developer.chrome.com/extensions/printerProvider) | Use eventos para consultar impressoras, seus recursos e enviar trabalhos de impressão. |
| [privacidade](https://developer.chrome.com/extensions/privacy) | Recursos de controle Microsoft Edge que afetam a privacidade de um usuário. Essa API depende do `EdgeSetting` protótipo de obter e definir a `types` configuração de Microsoft Edge. |
| [proxy](https://developer.chrome.com/extensions/proxy) | Gerenciar configurações de proxy para Microsoft Edge. Essa API depende do protótipo da API para obter e definir a `EdgeSetting` `types` configuração de proxy de Microsoft Edge. |
| [tempo de execução](https://developer.chrome.com/extensions/runtime) | Recupere a página em segundo plano, retorne detalhes sobre o manifesto e ouça e responda a eventos no ciclo de vida do aplicativo ou extensão. Você também pode converter o caminho relativo das URLs em URLs totalmente qualificadas. |
| [sessões](https://developer.chrome.com/extensions/sessions) | Consultar e restaurar guias e janelas de uma sessão de navegação. |
| [armazenamento](https://developer.chrome.com/extensions/storage) | Armazene, recupere e acompanhe as alterações nos dados do usuário. |
| [system.memory](https://developer.chrome.com/extensions/system_memory) | A `system.memory` API. |
| [system.storage](https://developer.chrome.com/extensions/system_storage) | Informações de consulta sobre dispositivos de armazenamento. Você também pode receber notificações quando os dispositivos de armazenamento são anexados ou desconectados. |
| [tabCapture](https://developer.chrome.com/extensions/tabCapture) | Interaja com fluxos de mídia de tabulação. |
| [guias](https://developer.chrome.com/extensions/tabs) | Interaja com o sistema de guias do navegador para criar, modificar e reorganizar guias. |
| [topSites](https://developer.chrome.com/extensions/topSites) | Acesse os sites principais, também chamados de sites mais visitados, exibidos na nova página de guia. Esses sites não incluem atalhos personalizados pelo usuário. |
| [tts](https://developer.chrome.com/extensions/tts) | Reproduza texto sintetizado em fala (TTS). |
| [ttsEngine](https://developer.chrome.com/extensions/ttsEngine) | Implemente um mecanismo de texto para fala (TTS) usando uma extensão. Extensões que se registram para usar essa API recebem eventos que contêm expressões a serem faladas e outros parâmetros. As extensões podem então usar qualquer tecnologia web disponível para sintetizar e enviar eventos de volta à função de chamada para relatar o status. |
| [types](https://developer.chrome.com/extensions/types) | Digite declarações para Microsoft Edge. |
| [webNavigation](https://developer.chrome.com/extensions/webNavigation) | Receber notificações sobre o status das solicitações de navegação. |
| [webRequest](https://developer.chrome.com/extensions/webRequest) | Observe e analise o tráfego. Intercepte, bloqueie ou modifique solicitações. |
| [windows](https://developer.chrome.com/extensions/windows) | Interaja com janelas do navegador para criar, modificar e reorganizar janelas no navegador. |



## <a name="unsupported-extension-apis"></a>APIs de extensão sem suporte

Microsoft Edge oferece suporte às seguintes APIs de Extensão:

* `chrome.gcm`.
* `chrome.identity.getAccounts`.
* `chrome.identity.getAuthToken` - Como alternativa, você pode usar para `launchWebAuthFlow` buscar um token OAuth2 para autenticar usuários.
* `chrome.instanceID`.


## <a name="additional-considerations-for-supported-apis"></a>Considerações adicionais para APIs com suporte

* O usuário deve estar Microsoft Edge usando uma conta MSA ou Azure Active Directory para usar `chrome.identity.getProfileUserInfo` . Se o usuário estiver Microsoft Edge usando uma conta local do Active Directory, a API retornará para os valores `null` de email e ID.

* Microsoft Edge não dá suporte a extensões que usam Chrome Web Store pagamentos porque ele usa para solicitar tokens para usuários `identity.getAuthtoken` assinados. Esses tokens são enviados para a API de licenciamento baseada em REST. 


<!-- links -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/apps/external_extensions).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
