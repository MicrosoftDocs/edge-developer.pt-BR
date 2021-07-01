---
description: Saiba como gerenciar pastas de dados do usuário em aplicativos WebView2
title: Gerenciar a pasta de dados do usuário em aplicativos WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, html de borda, pasta de dados do usuário
ms.openlocfilehash: d3b3e8d81ddffec043f0988385a433eb7c817de7
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627954"
---
# <a name="manage-the-user-data-folder"></a>Gerenciar a pasta de dados do usuário  

Os aplicativos WebView2 interagem com pastas de dados do usuário para armazenar dados do navegador, como cookies, permissões e recursos armazenados em cache.  Cada instância de um controle WebView2 está associada a uma pasta de dados do usuário.  Cada pasta de dados do usuário é exclusiva de um usuário.  

## <a name="best-practices"></a>Práticas recomendadas  

As pastas de dados do usuário são criadas automaticamente pelo WebView2.  Os desenvolvedores do WebView2 controlam o tempo de vida da pasta de dados do usuário.  Se o aplicativo rea usar dados do usuário de sessões de aplicativo, considere salvar as pastas de dados do usuário, caso contrário, você poderá excluí-las.  Considere os seguintes cenários ao decidir como gerenciar suas pastas de dados do usuário:  

*   Se o mesmo usuário usar seu aplicativo repetidamente e o conteúdo da Web do aplicativo se basear nos dados do usuário, salve a pasta de dados do usuário.  Se vários usuários usarem seu aplicativo repetidamente, crie uma nova pasta de dados do usuário para cada novo usuário e salve a pasta de dados do usuário de cada usuário.
*   Se o aplicativo não tiver usuários repetidos, crie uma nova pasta de dados do usuário para cada usuário e exclua a pasta de dados do usuário anterior.  
    
## <a name="create-user-data-folders"></a>Criar pastas de dados do usuário  

Para especificar o local da pasta de dados do usuário, inclua o parâmetro ao chamar `userDataFolder` [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) ou [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).  Após a criação, os dados do navegador do controle WebView2 são armazenados em uma subpasta de `userDataFolder` .  Quando não é especificado, o WebView2 cria pastas de dados do usuário em locais padrão `userDataFolder` da seguinte forma:  

*   Para aplicativos Windows Store empacotados, a pasta de usuário padrão é a `ApplicationData\LocalFolder` subpasta na pasta do pacote.  
*   Para aplicativos de área de trabalho existentes, a pasta de dados do usuário padrão é o caminho exe do seu aplicativo + `.WebView2` .  Em vez de usar o padrão, recomendamos que você especifique uma pasta de dados do usuário e que você a crie na mesma pasta onde todos os outros dados do aplicativo são armazenados.  
    
## <a name="delete-user-data-folders"></a>Excluir pastas de dados do usuário  

Seu aplicativo pode precisar excluir pastas de dados do usuário:  

*   Ao desinstalar seu aplicativo.  Se você estiver desinstalando aplicativos Windows Da Loja, Windows excluir pastas de dados do usuário automaticamente.  
*   Para limpar todo o histórico de dados de navegação.  
*   Para recuperar da corrupção de dados.  
*   Para remover dados da sessão anterior.  
    
> [!NOTE]
> Os arquivos em pastas de dados do usuário ainda podem estar em uso depois que o aplicativo WebView2 for fechado.  Nessa situação, aguarde até que o processo do navegador e todos os processos filho saiam antes de excluir a pasta.  Você pode recuperar a ID do processo do navegador usando a `BrowserProcessId` propriedade do WebView2.  

## <a name="share-user-data-folders"></a>Compartilhar pastas de dados do usuário  

Os controles WebView2 podem compartilhar as mesmas pastas de dados do usuário para:  

*   [Otimize os recursos do](../concepts/process-model.md) sistema executando em um processo de navegador.  
*   Compartilhe o histórico do navegador e os recursos armazenados em cache.  
    
Considere o seguinte ao compartilhar pastas de dados do usuário:  

1.  Ao criar controles WebView2 para atualizar versões do navegador usando eventos add_NewBrowserVersionAvailable \(Win32\) ou [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\), verifique se os processos do navegador saem e fecham controles WebView2 que compartilham a mesma pasta de dados do usuário. [](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable)  Para recuperar a ID do processo do navegador, use a `BrowserProcessId` propriedade do controle WebView2.  
1.  Os controles WebView2 que compartilham a mesma pasta de dados do usuário devem usar as mesmas opções para [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) ou [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).  Caso não seja, a criação de WebView2 falhará com `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .  
    
Para isolar diferentes partes do seu aplicativo ou quando o compartilhamento de dados entre controles WebView2 não for necessário, você pode optar por usar pastas de dados de usuário diferentes.  Por exemplo, um aplicativo pode consistir em dois controles WebView2, um para exibir um anúncio e outro para exibir conteúdo do aplicativo.  Nesse cenário, os desenvolvedores podem optar por usar pastas de dados de usuário diferentes para cada controle WebView2.  

> [!NOTE]
> Cada processo do navegador WebView2 consome memória e espaço em disco adicionais.  Portanto, recomendamos não executar WebView2s com muitas pastas de dados de usuário diferentes ao mesmo tempo.  
