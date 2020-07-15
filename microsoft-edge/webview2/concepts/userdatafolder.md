---
description: Saiba como gerenciar pastas de dados do usuário em aplicativos do WebView2
title: Gerenciar a pasta dados do usuário em aplicativos do WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge, pasta dados do usuário
ms.openlocfilehash: 870361e5f3edaea776538216c05e4114dc614342
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879148"
---
# Gerenciando a pasta dados do usuário

Os aplicativos do WebView2 interagem com pastas de dados do usuário para armazenar dados do navegador, como cookies, permissões e recursos armazenados em cache. Cada instância de um controle WebView2 é associada a uma pasta de dados do usuário. Cada pasta de dados do usuário é exclusiva para um usuário.

## Práticas recomendadas

As pastas de dados do usuário são criadas automaticamente pelo WebView2. Os desenvolvedores do WebView2 controlam o tempo de vida da pasta de dados do usuário. Se o aplicativo reutilizar dados do usuário de sessões do aplicativo, considere salvar as pastas de dados do usuário, caso contrário, você poderá excluí-las. Considere os seguintes cenários ao decidir como gerenciar suas pastas de dados de usuário:

*   Se o mesmo usuário usar seu aplicativo repetidamente, e o conteúdo da Web do aplicativo depender dos dados do usuário, salve a pasta dados do usuário. Se vários usuários usarem seu aplicativo repetidamente, crie uma nova pasta de dados do usuário para cada novo usuário e salve a pasta dados do usuário de cada usuário.
*   Se seu aplicativo não tiver usuários repetidos, crie uma nova pasta de dados de usuário para cada usuário e exclua a pasta de dados do usuário anterior.

## Criar pastas de dados do usuário

Para especificar o local da pasta de dados do usuário, inclua o `userDataFolder` parâmetro ao chamar [ICoreWebView2Environment](../reference/win32/0-9-538/icorewebview2environment.md) (Win32) ou [CoreWebView2Environment](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md) (.net). Após a criação, os dados do navegador do seu controle WebView2 são armazenados em uma subpasta de `userDataFolder` . Quando `userDataFolder` não é especificado, o WebView2 cria pastas de dados do usuário em locais padrão da seguinte maneira:

* Para aplicativos da Windows Store em pacote, a pasta usuário padrão é a subpasta `ApplicationData\LocalFolder` na pasta do pacote.
* Para aplicativos da área de trabalho existentes, a pasta dados do usuário padrão é o caminho exe do seu aplicativo + `.WebView2` . Em vez de usar o padrão, recomendamos que você especifique uma pasta de dados do usuário e a crie na mesma pasta em que todos os outros dados do aplicativo são armazenados.

## Excluir pastas de dados do usuário

Seu aplicativo pode precisar excluir pastas de dados do usuário:

* Durante a desinstalação do aplicativo. Se você estiver desinstalando aplicativos empacotados da Windows Store, o Windows excluirá pastas de dados do usuário automaticamente. 
* Para limpar todo o histórico de dados de navegação.
* Para recuperar-se da corrupção de dados.
* Para remover dados de sessão anteriores. 


> [!NOTE]
> Os arquivos nas pastas de dados do usuário ainda podem estar em uso após o aplicativo do WebView2 ser fechado. Nessa situação, aguarde o processo do navegador e todos os processos filho serem encerrados antes de excluir a pasta. Você pode recuperar a ID do processo do navegador usando a `BrowserProcessId` Propriedade do WebView2.

## Compartilhar pastas de dados do usuário

Os controles WebView2 podem compartilhar as mesmas pastas de dados de usuário para:

* [Otimize os recursos do sistema](../reference/win32/0-9-538/icorewebview2.md#process-model) executando em um processo do navegador.
* Compartilhe o histórico do navegador e recursos armazenados em cache. 

Considere o seguinte ao compartilhar pastas de dados do usuário: 

1. Ao recriar controles WebView2 para atualizar versões do navegador usando eventos do [add_NewBrowserVersionAvailable](../reference/win32/0-9-538/icorewebview2environment.md#add_newbrowserversionavailable) (Win32) ou do [NewBrowserVersionAvailable](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#newbrowserversionavailable) (.net), garanta que o navegador processe e feche os controles de WebView2 que compartilham a mesma pasta de dados do usuário. Para recuperar a ID do processo do navegador, use a `BrowserProcessId` Propriedade do controle WebView2.

2. Os controles WebView2 que compartilham a mesma pasta de dados do usuário devem usar as mesmas opções para [ICoreWebView2Environment](../reference/win32/0-9-538/icorewebview2environment.md) (Win32) ou [CoreWebView2Environment](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md) (.net). Caso contrário, haverá falha na criação do WebView2 `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` . 

Para isolar partes diferentes do seu aplicativo ou ao compartilhar dados entre os controles do WebView2 não forem necessários, você pode optar por usar pastas de dados de usuário diferentes. Por exemplo, um aplicativo pode consistir em dois controles WebView2, um para exibir um anúncio e o outro para exibir o conteúdo do aplicativo. Nesse cenário, os desenvolvedores podem optar por usar pastas de dados de usuário diferentes para cada controle WebView2. 

> [!NOTE]
> Cada processo de navegador WebView2 consome memória adicional e espaço em disco. Portanto, recomendamos não executar o WebView2s com muitas pastas de dados de usuário diferentes ao mesmo tempo. 
