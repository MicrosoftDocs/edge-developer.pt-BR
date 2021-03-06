---
description: Use o painel De armazenamento para inspecionar o armazenamento da Web, IndexedDB, cookies e caches de solicitação/resposta
title: Armazenamento | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, armazenamento da Web, armazenamento local, armazenamento de sessão, indexadodb, cookies, serviço de trabalho, cache
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398893"
---
# <a name="storage"></a>Storage

Use o **painel De** armazenamento para inspecionar e gerenciar vários dados armazenados em cache localmente, incluindo:  

*   [Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs  
*   [Dados estruturados de DB](#indexeddb-manager) indexados  
*   [Cookies](#cookies-list) para o domínio  
*   [Cache](#cache-manager) \(pares de solicitação/resposta\) para depuração de funcionários de serviço  

Expanda qualquer uma dessas categorias e clique em uma entrada filha para abrir sua guia gerenciador de recursos.  

## <a name="local-and-session-storage-managers"></a>Gerentes de armazenamento local e de sessão  

Use o Gerenciador de Armazenamento Local e o Gerenciador de Armazenamento de Sessão para inspecionar e gerenciar o armazenamento da Web para sua página.  

As **pastas Armazenamento Local** e Armazenamento de **Sessão** dentro do Se [picker](./debugger.md#resource-picker) de Recursos do painel de armazenamento exibem uma lista de origens para a página.  Selecionar um desses quadros abre uma tabela editável dos pares de chave/valor atuais definidos por meio de [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente \(and/or set directly from the DevTools [Storage list](#storage-list)\).  

![Gerente de Armazenamento do DevTools](./media/storage_web_storage.png)  

Nas guias Armazenamento Local e Armazenamento de Sessão, você pode:  

*   **Atualize** \( \) a lista de armazenamento para ver o conjunto atual de pares de `Ctrl+F5` chave/valores para o domínio determinado. [](#cookies-list)  \(A lista não atualiza automaticamente após atualizações de script.\)  
*   **Simular atingir o limite de armazenamento**  para o armazenamento web do Microsoft Edge.  Cada domínio e subdomínio tem sua própria área de armazenamento, no entanto, há um limite combinado:  
    *   **Subdomas**: até 5 MBs de espaço  
    *   **Domínios**: até 10 MBs de espaço  
    *   **Total para todos os domínios**: até 50 MBs de espaço  

   O armazenamento de sessão é limpo assim que a última guia do navegador fazendo referência à sua origem é fechada.  As entradas de armazenamento local persistem indefinidamente até serem desempuradas programaticamente pela página ou manualmente pelo usuário:  

   **Configurações**  >  **Limpar dados de navegação**  >  **Cookies e dados de site salvos**  

![Limpar dados de navegação do painel Configurações do Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a>Lista de armazenamento  

Na tabela De armazenamento, você pode:  

*   **Inspecione** e `key/value` classificar seus pares clicando em qualquer nome de coluna na tabela.  
*   **Edite** `Key` e de uma entrada existente `Value` clicando na célula.  
*   **Excluir** \( \) uma entrada da opção de menu de contexto de clique com o botão direito `Del` do mouse, **Excluir item**.  
*   **Adicione** um novo `key/value` par clicando na linha vazia na parte inferior da tabela.  

### <a name="shortcuts"></a>Atalhos

| Ação | Atalho |  
|:--- |:--- |  
| Atualizar | `Ctrl`+`F5` |  
| Excluir item | `Del` |  
| Copiar itens selecionados | `Ctrl`+`C` |  
| Selecionar tudo | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a>Gerente indexedDB  

Use a **guia IndexedDB** para inspecionar e gerenciar os dados estruturados armazenados localmente em uma máquina cliente.  Especificamente, você pode inspecionar/classificar e atualizar seus índices e armazenamentos de objetos e também excluir entradas de valor de chave individuais.  

> [!TIP]
> Você pode usar nossa [demonstração do Mixador](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) de Áudio para testar o *gerenciador IndexedDB* no Microsoft Edge DevTools.  

Para excluir todos os dados IndexedDB armazenados para o usuário atual no Microsoft Edge, use o menu Configurações **do** Microsoft Edge:  

**...** >  **Configurações**  >  **Limpar dados de navegação**  >  **Cookies e dados de site salvos**  

A pasta dentro do Seletor de Recursos do Depurador exibe uma lista de origens dos recursos `IndexedDB` carregados pela [](./debugger.md#resource-picker) página.  Todos os bancos de dados IndexedDB \(IDB\) serão listados na origem, juntamente com seus armazenamentos de objetos.  

![Gerente IndexedDB do DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a>Barra de ferramentas IndexedDB  

Na barra de ferramentas IndexedDB, você pode:  

*   **Atualize** \( \) para ver as entradas atuais no armazenamento de objetos `Ctrl` + `F5` ou no índice do banco de dados.  O gerente IndexedDB não atualize automaticamente quando as alterações são feitas no banco de dados.  

### <a name="object-store-entries-list"></a>Lista de entradas do armazenamento de objetos  

No armazenamento de objetos ou na tabela Índice, você pode:  

*   **Inspecione** e classificar seus pares de valores-chave clicando em qualquer nome de coluna na tabela.  
*   **Atualizar** \( `Ctrl` + `F5` \)  
*   **Excluir item** \( `Del` \) para remover a entrada selecionada no seu armazenamento de objetos ou índice.  Você também pode fazer isso na opção menu de contexto com o botão direito [do](#context-menu) mouse, **Excluir item**.  
*   **Copie itens selecionados** \( `Ctrl` + `C` \) para copiar o item selecionado para sua área de transferência.  Você também pode fazer isso na opção menu de contexto com o botão direito [do](#context-menu) **mouse, Copiar item selecionado**.  
*   **Selecione todos** \( `Ctrl` + `A` \) para selecionar todas as entradas no seu armazenamento de objetos ou índice.  Você também pode fazer isso na opção menu de contexto com o botão [direito](#context-menu) do mouse, **Selecione tudo**.  

As colunas do armazenamento de objetos ou da tabela Index podem ser classificação:  

| Coluna | Descrição |  
|:--- |:--- |  
| Chave | Nome do par de valores-chave \(mesmo que **Chave Primária**\) ao iterar sobre um armazenamento de objetos; Nome da chave de índice \(chave atual do cursor\) ao iterar sobre um índice |  
| Chave Primária | Nome do par de valores-chave \(consulte **Documentos da Web MDN** para obter mais informações sobre chaves [do](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)BID \) |  
| Value | Valor do par de valores-chave |  

Confira documentos *da Web MDN para* saber mais sobre conceitos e uso [indexadosDB.](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)  

### <a name="context-menu"></a>Menu de contexto  

Além da barra de ferramentas [ *IndexedDB,* ](#indexeddb-toolbar)você também pode gerenciar seus dados em armazenamentos de objetos ou índices no **menu** Contexto com o botão direito do mouse e/ou [atalhos de teclado.](#shortcuts)  

### <a name="shortcuts"></a>Atalhos

| Ação | Atalho |  
|:--- |:--- |  
| Atualizar | `Ctrl`+`F5` |  
| Excluir par de valores-chave | `Del` |  
| Copiar itens selecionados | `Ctrl`+`C` |  
| Selecionar tudo | `Ctrl +`A' |  

## <a name="cookies-manager"></a>Gerenciador de cookies  

Use o Gerenciador de Cookies para inspecionar e gerenciar os cookies para o domínio determinado.  

A pasta dentro do Seletor de Recursos do Depurador exibe uma lista de origens dos recursos `Cookies` carregados pela [](./debugger.md#resource-picker) página.  Selecionar um desses quadros abre uma tabela que representa os cookies atuais definidos pelo cabeçalho [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou por script com [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).  

![Gerenciador de Cookies do DevTools](./media/storage_cookies.png)  

Na barra de ferramentas da guia Cookies, você pode:  

*   **Atualize** \( `Ctrl` + `F5` \) a [lista Cookies](#cookies-list) para ver o conjunto atual de cookies para o domínio determinado.  \(A lista não atualize automaticamente.\)  
*   **Exclua** todos os cookies `Ctrl` + `Shift` + `Del` \( \) \(session e permanent\) para o caminho da página atual.  
*   **Exclua todos os cookies** `Ctrl` + `Del` de sessão \( \) para o caminho da página atual.  

Para limpar completamente sua lista de Cookies, talvez seja necessário limpar todos **os cookies** para o domínio na barra de ferramentas [do](./network.md#toolbar) painel de rede.  

### <a name="cookies-list"></a>Lista de cookies  

Na tabela de lista Cookies, você pode:  

*   **Inspecionar e classificar** seus cookies clicando em qualquer nome de coluna na tabela.  
*   **Edite** `Name` e de um cookie existente `Value` clicando na célula.  
*   **Exclua** \( \) um cookie da opção de menu de contexto com o botão `Del` direito do mouse, [](#context-menu) `Delete cookie` .  
*   **Adicione** um novo cookie de sessão para o dado clicando na linha `Domain/Path` vazia na parte inferior da tabela.  Isso só funciona para cookies de sessão; cookies permanentes \(com datas de expiração específicas\) devem ser definidos com métodos tradicionais.  Os `Domain` valores e são `Path` preenchidos automaticamente de acordo com o local da página.  

As colunas da lista Cookies são sortíveis:

| Coluna | Descrição |  
| :--- | :--- |  
| Name | Nome do cookie |  
| Value | Valor do cookie |  
| Domínio | Nome do host do cookie \(pode estar vazio\) |  
| Caminho | Caminho da URL para o cookie \(pode estar vazio\) |  
| Expira | Duração máxima do cookie como um data/hora HTTP.  Se não `Expires` tiver `Max-Age` sido definido, a entrada será considerada um cookie de sessão.  |  
| Somente HTTP | Indica se o cookie foi definido com `HttpOnly` diretiva, indicando que ele está inacessível do JavaScript |  
| Proteja | Indica se o cookie foi definido com a diretiva, indicando que ele só será enviado para o servidor a partir de uma solicitação usando `Secure` SSL e o protocolo HTTPS.  |  

Consulte a referência [set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) de documentos da **Web MDN** para obter mais detalhes sobre propriedades de cookie.  

### <a name="context-menu"></a>Menu de contexto  

Além da barra de ferramentas da guia [Cookies,](#cookies-manager)você também pode gerenciar seus cookies no **menu** Contexto com o botão direito do mouse e/ou os [atalhos de teclado.](#shortcuts)  

### <a name="shortcuts"></a>Atalhos  

| Ação | Atalho |  
|:--- |:--- |  
| Atualizar | `Ctrl`+`F5` |  
| Excluir cookie | `Del` |  
| Excluir todos os cookies | `Ctrl`+`Shift`+`Del` |  
| Excluir todos os cookies de sessão | `Ctrl`+`Del` |  
| Copiar itens selecionados | `Ctrl`+`C` |  
| Selecionar tudo | `Ctrl`+`A` |  

### <a name="cache-manager"></a>Gerenciador de cache  

Clicar em uma entrada de cache específica abrirá o Gerenciador de **Cache** de funcionários do serviço, onde você pode inspecionar e, opcionalmente, excluir entradas de cache \( e pares de `Request` `Response` chave/valor\):  

![Gerenciador de cache](./media/storage_cache.png)  

### <a name="shortcuts"></a>Atalhos  

#### <a name="cache-manager"></a>Gerenciador de cache  

| Ação | Atalho |  
|:--- |:--- |  
| Atualizar | `Ctrl`+`F5` |  
| Excluir item | `Del` |  
| Copiar itens selecionados | `Ctrl`+`C` |  
| Selecionar tudo | `Ctrl`+`A` |  
