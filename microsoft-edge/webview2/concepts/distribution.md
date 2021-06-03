---
description: Opções de distribuição ao liberar um aplicativo usando Microsoft Edge WebView2
title: Distribuição de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 97ede968e066c572bb1b22e10ed7e758e38e3ca4
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535696"
---
# <a name="distribution-of-apps-using-webview2"></a>Distribuição de aplicativos usando WebView2  

Ao distribuir seu aplicativo WebView2, certifique-se de que a plataforma Web de backing, o Tempo de Execução [do WebView2,][Webview2Installer]está presente antes do aplicativo ser iniciado.  Este artigo descreve como você \(o desenvolvedor\) instala o WebView2 Runtime e usa os dois modos de distribuição para seu aplicativo WebView2:  [Evergreen](#evergreen-distribution-mode) e [Fixed Version](#fixed-version-distribution-mode).  

## <a name="evergreen-distribution-mode"></a>Modo de distribuição evergreen  

> [!NOTE]
> O modo de distribuição Evergreen é recomendado para a maioria dos desenvolvedores.  

O modo de distribuição Evergreen garante que seu aplicativo está aproveitando os recursos mais recentes e as atualizações de segurança.  Ele tem as seguintes características.  

*   A plataforma Web subjacente \(WebView2 Runtime\) é atualizada automaticamente sem esforço adicional de você.  
*   Todos os aplicativos que usam o modo de distribuição Evergreen usam uma cópia compartilhada do Evergreen WebView2 Runtime, que economiza espaço em disco.  
    
### <a name="understanding-the-webview2-runtime"></a>Noções básicas sobre o tempo de execução do WebView2  

O WebView2 Runtime é um tempo de execução redistribuível e serve como a plataforma Web de apoio para aplicativos WebView2.  O conceito é semelhante ao Visual C++ ou ao .NET Runtime para aplicativos C++/.NET.  O Runtime contém binários Microsoft Edge \(Chromium\) que são ajustados e testados para aplicativos.  O Tempo de Execução não aparece como um navegador visível pelo usuário durante a instalação.  Por exemplo, um usuário não tem um atalho da área de trabalho do navegador ou entrada do menu iniciar.  

Durante o desenvolvimento e o teste, você pode usar como plataforma Web de backing.  

*   O Tempo de Execução do WebView2  
*   Qualquer canal de navegador do Insider \(non-stable\) Microsoft Edge \(Chromium\)  
    
Em ambientes de produção, você deve garantir que o Tempo de Execução está presente em dispositivos de usuário antes do aplicativo ser iniciado.  O Microsoft Edge canal Estável não está disponível para uso do WebView2.  A decisão impede que os aplicativos se ade baseem no navegador em produção.

Não tome uma dependência no navegador porque:  

*   Microsoft Edge \(Chromium\) não é garantido estar presente em todos os dispositivos de usuário.  Por exemplo, dispositivos desconectados do Windows Update ou não gerenciados diretamente pela Microsoft \(uma grande parte do mercado Enterprise e EDU\) podem não ter o navegador.  Permitir que você distribua o Tempo de Execução do WebView2 evita a dependência do navegador como um pré-requisito para aplicativos.  
*   Navegadores e aplicativos têm casos de uso diferentes e, portanto, tomar uma dependência em um navegador pode ter efeitos colaterais não intencionais em seus aplicativos.  Por exemplo, os administradores de IT podem controlar a versão do navegador para compatibilidade de site interno.  O Tempo de Execução do WebView2 permite que os aplicativos permaneçam sempre agredidos enquanto as atualizações do navegador estão sendo gerenciadas ativamente.  
*   Em vez do navegador, o Tempo de Execução é desenvolvido e testado para cenários de aplicativos e, em alguns casos, pode incluir correções de bugs ainda não disponíveis no navegador.  
    
No futuro, o Evergreen WebView2 Runtime planeja enviar com versões futuras de Windows.  Implante o Tempo de Execução com seu aplicativo de produção até que o Tempo de Execução se torne mais universalmente disponível.  

### <a name="deploying-the-evergreen-webview2-runtime"></a>Implantando o Tempo de Execução do Evergreen WebView2  

Somente uma instalação do Evergreen WebView2 Runtime é necessária para todos os aplicativos Evergreen no dispositivo.  Há várias ferramentas disponíveis na página de download do Tempo de Execução [do WebView2.][Webview2Installer]  As ferramentas a seguir ajudam a implantar o Evergreen Runtime.  

*   WebView2 Runtime Bootstrapper é um instalador minúsculo \(aproximadamente 2 MB\).  WebView2 Runtime Bootstrapper baixa e instala o Evergreen Runtime de servidores Microsoft que corresponde à arquitetura de dispositivo do usuário.  
*   Use um link para baixar programaticamente o bootstrapper.  
*   WebView2 Runtime Instalador Autônomo é um instalador completo que instala o Evergreen WebView2 Runtime em ambientes offline.  
    
Atualmente, tanto o bootstrapper quanto o instalador autônomo suportam apenas as instalações por máquina, o que requer elevação.  Se um instalador for executado sem elevação, o usuário será solicitado a elevar as permissões.  

Use fluxos de trabalho a seguir para garantir que o Tempo de Execução já está instalado antes do seu aplicativo ser lançado.  Você pode ajustar seu fluxo de trabalho dependendo do cenário.  O código de exemplo está disponível no [repo Samples][GitHubMicrosoftedgeWebView2samplesWebview2Deployment].  

#### <a name="online-only-deployment"></a>Implantação somente online  

Se você tiver um cenário de implantação somente online em que os usuários supõem ter acesso à Internet, conclua as etapas a seguir.  

1.  Durante a configuração do aplicativo, verifique se o Tempo de Execução já está instalado.  Para verificar, conclua uma das seguintes ações.  
    *   Inspecione se `pv (REG_SZ)` a regkey existe e não `null` está ou vazia.  Encontre  `pv (REG_SZ)` no local a seguir.  
        
        Em 64 bits Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Em 32 bits Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Execute [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] e verifique se `versionInfo` é `NULL` .  
1.  Se o Tempo de Execução não estiver instalado, use o link para baixar programaticamente o bootstrapper.  
1.  Invoque o bootstrapper de um processo ou prompt de comando elevado com para `MicrosoftEdgeWebview2Setup.exe /silent /install` instalação silenciosa.  
    
O fluxo de trabalho anterior tem os seguintes benefícios.  

*   Instale o Tempo de Execução somente quando necessário ou quando você não for necessário para instalar o pacote.  
*   O bootstrapper detecta automaticamente a arquitetura do dispositivo e instala o Tempo de Execução correspondente.  
*   Instale o Runtime silenciosamente.  
    
Você também pode optar por empacotar o bootstrapper com seu aplicativo em vez de baixá-lo programaticamente sob demanda.  

#### <a name="offline-deployment"></a>Implantação offline  

Se você tiver um cenário de implantação offline em que a implantação do aplicativo precisa funcionar totalmente offline, conclua as etapas a seguir.  

1.  Baixe o [instalador autônomo][Webview2Installer].  
1.  Inclua o instalador no instalador ou no atualizador do aplicativo.  
1.  Durante a configuração do aplicativo, verifique se o Tempo de Execução já está instalado.  Para verificar, conclua uma das seguintes ações.  
    *   Inspecione se `pv (REG_SZ)` a regkey existe e não `null` está ou vazia.  Encontre  `pv (REG_SZ)` no local a seguir.  
        
        Em 64 bits Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        Em 32 bits Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Execute [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] e verifique se `versionInfo` é `NULL` .  
1.  Se o Tempo de Execução não estiver instalado, execute o instalador autônomo.  Se você quiser executar uma instalação silenciosa, execute o instalador de um processo elevado ou copie e execute o seguinte comando.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### <a name="stay-compatible-in-evergreen-mode"></a>Mantenha-se compatível no modo Evergreen  

A Web está em constante evolução.  O Tempo de Execução do Evergreen WebView2 é mantido atualizado para fornecer os recursos mais recentes e as correções de segurança.  Para garantir que seu aplicativo permaneça compatível com a Web, você deve configurar a infraestrutura de teste.  

Canais não estáveis Microsoft Edge \(Beta/Dev/Canary\) fornecem uma visão geral do que está por vir no Tempo de Execução do WebView2.  Assim como desenvolve sites para Microsoft Edge, você deve testar seu aplicativo WebView2 regularmente.  Teste seu aplicativo WebView2 em um dos canais não estáveis e atualize seus problemas de aplicativo ou [relatório][GithubMicrosoftedgeWebviewfeedback] se surgirem problemas. Normalmente, o Dev e o Beta são os canais recomendados.  Para ajudá-lo a decidir qual canal está correto, navegue até [Overview of the Microsoft Edge channels][DeployEdgeMicrosoftEdgeChannels].  Você pode baixar o [canal][DownloadNonstableEdge] de Microsoft Edge não estável em seu ambiente de teste e usar ou variáveis de ambiente para indicar a preferência de canal para seu aplicativo `regkey` de teste.  Para obter mais informações, navegue até [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Você também pode usar [o WebDriver para][HowToWebdriver] automatizar testes webView2.

## <a name="fixed-version-distribution-mode"></a>Modo de distribuição de versão fixa   

Para ambientes restritos com requisitos estritos de compatibilidade, considere usar o modo de distribuição versão fixa.  Escolha e empacote uma versão específica do Tempo de Execução do WebView2 usando o modo de distribuição versão fixa.  Você pode especificar o tempo de atualizações do Tempo de Execução para seu aplicativo.  O modo de distribuição versão fixa não recebe atualizações automáticas. Planeje atualizar seu aplicativo e o Tempo de Execução.  

> [!NOTE] 
> O modo de distribuição versão fixa foi anteriormente chamado de bring-your-own.  

Para usar o modo Versão Fixa, conclua as seguintes ações

1.  [Baixe][Webview2Installer] o pacote Versão Fixa. 
1.  Descompacte o pacote usando linha de `expand {path to the package} -F:* {path to the destination folder}` comando ou com ferramentas como WinRAR. Evite descompactar por meio do Explorador de Arquivos, pois ele pode não gerar a estrutura de pasta correta.  
1.  Inclua os binários de versão fixa descompactados em seu projeto.  
1.  Indique o caminho para os binários de Versão Fixa ao criar o ambiente WebView2.  
    *   Para Win32 C/C++, você pode criar o ambiente usando a [função CreateCoreWebView2EnvironmentWithOptions.][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]  Use o `browserExecutableFolder` parâmetro para indicar o caminho para a pasta que contém `msedgewebview2.exe` .  
    *   Para o .NET, você pode fazer uma das opções a seguir para especificar o ambiente.  
        
        > [!NOTE]
        > Você deve especificar o ambiente antes que a propriedade WebView2 `Source` entre em vigor.  
        
        *   De definir `CreationProperties` a propriedade \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) no elemento WebView2.  Use o `BrowserExecutableFolder` membro na `CoreWebView2CreationProperties` classe \([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\) para indicar o caminho para os binários de Versão Fixa.  
        *   Use `EnsureCoreWebView2Async` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\) para especificar o ambiente.  Use o `browserExecutableFolder` parâmetro em [CoreWebView2Environment.CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] para indicar o caminho para os binários de Versão Fixa.  
1.  Empacote e shipe os binários de Versão Fixa com seu aplicativo.  Atualize os binários conforme apropriado.  
    
### <a name="known-issues-for-fixed-version"></a>Problemas conhecidos para Versão Fixa  

Em comparação com o Evergreen Runtime, a Versão Fixa não tem um processo de instalação, o que faz com que Microsoft PlayReady [não][MicrosoftPlayReady] funcione sem modificação.  Você pode atenuar o problema concluindo as seguintes ações.  

1.  Localize o caminho onde você implanta o pacote Versão Fixa no dispositivo do usuário, como o local a seguir.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Execute os seguintes comandos no dispositivo do usuário.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady deve estar funcionando agora no dispositivo do usuário.  Na guia **Segurança** da pasta **Versão Fixa,** ela deve incluir permissões para `ALL APPLICATION PACKAGES` e `ALL RESTRICTED APPLICATION PACKAGES` .  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Permissão para PlayReady" lightbox="../media/play-ready-permission.png":::
        Permissão para PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Noções básicas sobre versões do navegador e webView2 | Microsoft Docs"  
[HowToWebdriver]: ../how-to/webdriver.md "Automatizar e testar o WebView2 com Microsoft Edge driver | Microsoft Docs"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString - Globals | Microsoft Docs"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos Microsoft Edge canais | Microsoft Docs"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "Classe CreateAsync - Microsoft.WebView2.Core.CoreWebView2Environment | Microsoft Docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Classe EnsureCoreWebView2Async -Microsoft.Web.WebView2.Wpf.WebView2 | Microsoft Docs"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Classe EnsureCoreWebView2Async - Classe Microsoft.Web.WebView2.WinForms.WebView2 | Microsoft Docs"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "Classe CoreWebView2CreationProperties - Classe Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties | Microsoft Docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Classe Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties - Classe Microsoft.Web.WebView2.Wpf.WebView2 | Microsoft Docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Classe Microsoft.Web.WebView2.WinForms.WebView2 | Microsoft Docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer | Desenvolvedor da Microsoft"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "Implantação do WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  
