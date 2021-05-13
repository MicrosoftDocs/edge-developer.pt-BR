---
description: Saiba mais sobre as práticas recomendadas de desenvolvimento a ser usadas ao desenvolver seu aplicativo WebView2.
title: Práticas recomendadas de desenvolvimento do WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, edge, práticas recomendadas
ms.openlocfilehash: 5a11f01ec07aea12599c8bdb8428d451ad7bd013
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564746"
---
# <a name="webview2-development-best-practices"></a>Práticas recomendadas de desenvolvimento do WebView2  

Cada equipe de desenvolvimento segue práticas diferentes ao criar seu aplicativo. Quando você cria aplicativos WebView2, há práticas que recomendamos seguir. Este artigo descreve essas recomendações e práticas recomendadas para você ao criar aplicativos WebView2 baseados em produção.

## <a name="use-evergreen-webview2-runtime-recommended"></a>Usar o Tempo de Execução do Evergreen WebView2 (recomendado)  

Embora a Versão Fixa tenha seus casos de uso para aplicativos com requisitos estritos de compatibilidade, geralmente recomendamos usar o Evergreen WebView2 Runtime.  O Evergreen WebView2 Runtime é atualizado automaticamente e inclui os recursos mais recentes e patches de segurança disponíveis para seu aplicativo WebView2. O Evergreen WebView2 Runtime também requer menos espaço de armazenamento no disco.

Verifique se o Tempo de Execução do WebView2 evergreen está instalado antes de usar seu aplicativo WebView2.  Para obter mais informações, navegue até [Deploying the Evergreen WebView2 Runtime][Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime].  

## <a name="run-compatibility-tests-regularly-when-using-the-evergreen-webview2-runtime"></a>Executar testes de compatibilidade regularmente ao usar o Evergreen WebView2 Runtime

Ao usar o Evergreen WebView2 Runtime, certifique-se de executar testes de compatibilidade regulares. Como o tempo de execução é atualizado automaticamente, teste o conteúdo da Web no controle WebView2 em relação às versões não estáveis do Microsoft Edge para garantir que seu aplicativo WebView2 seja executado conforme o esperado. Essa orientação é semelhante às orientações que damos aos desenvolvedores da Web. Para obter mais informações, navegue até [Permanecer compatível no modo Evergreen][Webview2ConceptsDistributionStayCompatibleEvergreenMode].

## <a name="ensure-apis-are-supported-by-the-installed-webview2-runtime"></a>Verifique se as APIs são suportadas pelo Tempo de Execução do WebView2 instalado

Os aplicativos WebView2 precisam de um SDK Webview2 e um WebView2 Runtime instalado no computador para execução. O SDK e o tempo de execução são versionados. Como as APIs estão continuamente sendo adicionadas ao WebView2, novas versões do tempo de execução também são lançadas para dar suporte às novas APIs. Você precisará garantir que as APIs usadas pelo aplicativo WebView2 sejam suportadas pelo Tempo de Execução webView2 instalado no computador. 

Se você usar o Evergreen WebView2 Runtime, há alguns cenários em que o tempo de execução pode não ser atualizado para usar a versão mais recente. Por exemplo, quando os usuários não têm acesso à Internet, o tempo de execução não é atualizado automaticamente nesse ambiente. Além disso, o uso de algumas políticas de grupo pausa as atualizações do WebView2. Quando você pressiona uma atualização para seu aplicativo WebView2, o aplicativo pode quebrar porque ele usa APIs mais novas que não estão disponíveis no tempo de execução instalado.   
 
Para resolver essa situação, você pode testar a disponibilidade das APIs no tempo de execução instalado, antes que seu código chama a API. Esse teste para funcionalidade mais nova é semelhante a outras práticas recomendadas de desenvolvimento da Web que detectam recursos com suporte antes de usar novas APIs da Web. Para testar a disponibilidade da API no tempo de execução instalado, use:  

*   O `queryinterface` em C/C++. 
*   Um bloco try/catch em .NET ou WinUI. 
    
Para obter mais informações, navegue [até Determine WebView2 Runtime requirement][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement].  

## <a name="update-the-fixed-version-runtime"></a>Atualizar o Tempo de Execução de Versão Fixa  

Se você usar o Tempo de Execução de Versão Fixa, certifique-se de atualizar o tempo de execução regularmente para reduzir qualquer risco potencial de segurança. Ao usar conteúdo de terceiros em aplicativos Webview2, sempre considere o conteúdo não falso.  Para obter mais informações, navegue até [Modo de distribuição de Versão Fixa][Webview2ConceptsDistributionFixedVersionDistributionMode].  

## <a name="manage-new-versions-of-the-runtime"></a>Gerenciar novas versões do tempo de execução  

Sempre que uma nova versão do Evergreen WebView2 Runtime é baixada para o dispositivo, os aplicativos WebView2 em execução continuam usando o tempo de execução anterior até que o processo do navegador seja lançado. Esse comportamento permite que os aplicativos executem continuamente e impede que o tempo de execução anterior seja excluído. Para usar a nova versão do tempo de execução, você precisará liberar todas as referências aos objetos de ambiente WebView2 anteriores ou reiniciar seu aplicativo. Na próxima vez que você criar um novo ambiente WebView2, ele usará a nova versão.

Para tomar medidas quando uma nova versão estiver disponível, como notificar o usuário para reiniciar o aplicativo, você pode usar o [evento add_NewBrowserVersionAvailable(Win32)][Webview2ReferenceaddNewBrowserVersionAvailable] ou [CoreWebView2Environment.NewBrowserVersionAvailable(.NET)][Webview2ReferenceNewBrowserVersionAvailable] em seu código. Se o código manipular a reinicialização do aplicativo, considere salvar o estado do usuário antes que o aplicativo WebView2 saia.  

## <a name="manage-the-lifetime-of-the-user-data-folder"></a>Gerenciar o tempo de vida da pasta de dados do usuário 
Os aplicativos WebView2 criam uma pasta de dados do usuário para armazenar dados como cookies, credenciais, permissões e assim por diante. Depois de criar a pasta, seu aplicativo é responsável pelo gerenciamento do tempo de vida da pasta de dados do usuário, incluindo a limpeza quando o aplicativo é desinstalado.  Para obter mais informações, navegue até [Gerenciando a Pasta de Dados do Usuário.][Webview2ConceptsUserDataFolder]  

## <a name="follow-recommended-webview2-security-best-practices"></a>Siga as práticas recomendadas de segurança do WebView2 
Para qualquer aplicativo WebView2, certifique-se de seguir nossas práticas recomendadas de segurança webView2.  Para obter mais informações, navegue até [Práticas recomendadas para desenvolver aplicativos WebView2 seguros.][Webview2ConceptsSecurity]  

<!-- links -->  

[Webview2ConceptsDistributionDeployingEvergreenWebview2Runtime]: ../concepts/distribution.md#deploying-the-evergreen-webview2-runtime "Implantando o Tempo de Execução do Evergreen WebView2 - Distribuição de aplicativos usando o webView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ../concepts/distribution.md#fixed-version-distribution-mode "Modo de distribuição de versão fixa - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsDistributionStayCompatibleEvergreenMode]: ../concepts/distribution.md#stay-compatible-in-evergreen-mode "Mantenha-se compatível no modo Evergreen - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ../concepts/security.md "Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ../concepts/user-data-folder.md "Gerenciar a pasta de dados do usuário | Microsoft Docs"  
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#determine-webview2-runtime-requirement "Determinar o requisito de Tempo de Execução do WebView2 - Entenda as versões do SDK webView2 | Microsoft Docs"  
[Webview2GetStartedWin32]: ../get-started/win32.md "Começar com WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ../get-started/winforms.md "Começar com WebView2 no Windows Forms | Microsoft Docs"  
[Webview2GetStartedWinui]: ../get-started/winui.md "Começar com WebView2 no WinUI 3 (Visualização) | Microsoft Docs"  
[Webview2GetStartedWpf]: ../get-started/wpf.md "Começar com WebView2 no WPF | Microsoft Docs"  

[Webview2ReferenceaddNewBrowserVersionAvailable]: /microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable "add_NewBrowserVersionAvailable | Microsoft Docs"  

[Webview2ReferenceNewBrowserVersionAvailable]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable "Evento CoreWebView2Environment.NewBrowserVersionAvailable | Microsoft Docs"  
