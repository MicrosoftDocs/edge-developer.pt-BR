---
description: Opções de distribuição ao liberar um aplicativo usando o Microsoft Edge WebView2
title: Distribuição de aplicativos do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 7db610ff1133b1b5b380372422f1f2f10981e583
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11052183"
---
# Distribuição de aplicativos usando o WebView2  

Ao distribuir seu aplicativo do WebView2, certifique-se de que a plataforma da Web de backup – o [tempo de execução do WebView2](#understanding-the-webview2-runtime) está presente antes do início do aplicativo.  Este artigo descreve como os desenvolvedores podem instalar o tempo de execução do WebView2 e usar os dois modos de distribuição para o seu aplicativo do WebView2: a versão do mais  [verde](#evergreen-distribution-mode) e [fixo](#fixed-version-distribution-mode).  

## Modo de distribuição do verde  

> [!NOTE]
> O modo de distribuição de verde é recomendado para a maioria dos desenvolvedores.  

O modo de distribuição do verde garante que seu aplicativo Tire proveito dos recursos e das atualizações de segurança mais recentes.  Ele tem as características a seguir.  

*   A plataforma da Web subjacente \ (tempo de execução WebView2 \) é atualizada automaticamente sem esforço adicional dos desenvolvedores.  
*   Todos os aplicativos que usam o modo de distribuição para o verde usam uma cópia compartilhada do tempo de execução do WebView2, que poupa espaço em disco.  

### Compreendendo o tempo de execução do WebView2  

O tempo de execução do WebView2 é um tempo de execução redistribuível e funciona como a plataforma de backup para aplicativos do WebView2.  Esse conceito é semelhante ao VC + + ou ao .NET Runtime para aplicativos C++/.NET.  Nos bastidores, o tempo de execução é modificado para binários do Microsoft Edge \ (Chromium \) que são ajustados e testados para aplicativos.  O tempo de execução não aparecerá como um navegador visível ao usuário durante a instalação, por exemplo, os usuários não terão um atalho para a área de trabalho do navegador ou uma entrada do menu iniciar.  

Para desenvolvimento e testes, os desenvolvedores podem usar o tempo de execução ou qualquer canal de navegador não estável do Microsoft Edge \ (Chromium \) para a plataforma de backup da Web.  Em ambientes de produção, os desenvolvedores devem garantir que o tempo de execução esteja presente em dispositivos de usuário antes de o aplicativo iniciar.  O canal estável do Microsoft Edge não está disponível para uso do WebView2 para impedir que os aplicativos tirem uma dependência do navegador na produção.  

Os desenvolvedores não devem ter dependência do navegador porque:  

*   O Microsoft Edge \ (Chromium \) não está garantido para estar presente em todos os dispositivos do usuário.  Por exemplo, dispositivos desconectados do Windows Update ou não são gerenciados pela Microsoft diretamente \ (uma grande parte do mercado corporativo/EDU) pode não ter o navegador.  Permitir que os desenvolvedores distribuam o tempo de execução do WebView2 evita assumir uma dependência do navegador como pré-requisito para aplicativos.
*   Navegadores e aplicativos têm casos de uso diferentes e, portanto, assumir uma dependência em um navegador pode ter efeitos colaterais indesejados nos seus aplicativos.  Por exemplo, os administradores de ti podem controlar a versão do navegador para compatibilidade de site interno.  O tempo de execução do WebView2 permite que os aplicativos permaneçam à frente enquanto as atualizações do navegador são gerenciadas ativamente.  
*   Ao contrário do navegador, o tempo de execução é desenvolvido e testado para cenários de aplicativo e, em alguns casos, pode incluir correções de bugs ainda não disponíveis no navegador.  

O tempo de execução do WebView2 está planejado para enviar a caixa de entrada em versões futuras do Windows.  Antes que o tempo de execução se torne mais universalmente disponível, recomendamos aos desenvolvedores implantar o tempo de execução juntamente com o aplicativo de produção.  

### Implantando o tempo de execução do WebView2 verde  

Apenas uma instalação do WebView2 do tempo de execução do verde é necessária para todos os aplicativos no dispositivo.  Há várias ferramentas disponíveis na página de download do [tempo de execução do WebView2][Webview2Installer] para ajudar os desenvolvedores a implantar o tempo de execução de verde, como:  

*   WebView2 de tempo de execução de tempo de execução \ (a ser lançado em breve \) é um instalador pequeno \ (aproximadamente 2 MB \).  Este instalador baixa e instala o tempo de execução de verde dos servidores da Microsoft que corresponde à arquitetura de dispositivo do usuário.  
*   Link para baixar o bootstrapper \ (a ser lançado em breve \) é um link para os desenvolvedores baixarem programaticamente o bootstrapper.
*   O instalador autônomo do WebView2 Runtime é um instalador completo que pode instalar o tempo de execução do WebView2 verde em ambientes offline.  

Atualmente, tanto o bootstrapper quanto o instalador autônomo dão suporte apenas à instalação por computador, o que requer elevação.  Quando executado sem elevação, um prompt de controle de conta de usuário do Windows é exibido para perguntar aos usuários sobre a elevação de permissões.  

Recomendamos os seguintes fluxos de trabalho para garantir que o tempo de execução já esteja instalado antes do aplicativo ser iniciado.  Você pode ajustar o fluxo de trabalho dependendo do cenário.  Também forneceremos um código de exemplo no futuro.  

#### Implantação somente online  

Se você tiver um cenário de implantação somente online em que os usuários finais presumiram ter acesso à Internet, execute as seguintes etapas:  

*   Durante a configuração do seu aplicativo, verifique se o tempo de execução já está instalado por uma destas opções:  
    *   Inspecionando se a regkey `pv (REG_SZ)` existe em `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` ou  
    *   Chamando WebView2 API [GetAvailableCoreWebView2BrowserVersionString](../reference/win32/0-9-622/webview2-idl.md#getavailablecorewebview2browserversionstring) e verifique se o VERSIONINFO é nulo.  
*   Se o tempo de execução não estiver instalado, use o link para baixar programaticamente o bootstrapper.  
*   Invoque o bootstrapper de um processo elevado ou prompt de comando com `MicrosoftEdgeWebview2Setup.exe /silent /install` para a instalação silenciosa.  

Esse fluxo de trabalho garante a instalação do tempo de execução somente quando for necessário, você não é obrigado a empacotar instaladores nem detectar a arquitetura de dispositivos do usuário e pode instalar o tempo de execução silenciosamente.  Você também pode optar por empacotar o bootstrapper com seu aplicativo em vez de baixá-lo programaticamente sob demanda.  

#### Implantação offline  

Se você tiver um cenário de implantação offline em que a implantação do aplicativo tem que funcionar completamente offline, execute as seguintes etapas:  

*   Baixe o [instalador autônomo][Webview2Installer].  
*   Inclua o instalador no instalador do aplicativo ou no atualizador.  
*   Durante a configuração do seu aplicativo, verifique se o tempo de execução já está instalado por uma destas opções:  
    *   Inspecionando se a regkey `pv (REG_SZ)` existe em `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` ou  
    *   Chamando WebView2 API [GetAvailableCoreWebView2BrowserVersionString](../reference/win32/0-9-622/webview2-idl.md#getavailablecorewebview2browserversionstring) e verifique se o VERSIONINFO é nulo.  
*   Se o tempo de execução não estiver instalado, chame o instalador autônomo de um processo elevado ou prompt de comando com `MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install` para a instalação silenciosa.  

## Modo de distribuição de versão corrigido  

> [!NOTE]
> O modo de distribuição de versão fixa ainda não está disponível.  

Para ambientes restritos, há planos para dar suporte a uma versão fixa, que anteriormente tinha o seu próprio modo de distribuição, que tinha sido chamado.  O modo de distribuição de versão fixa permite que os desenvolvedores selecionem e Empacotem uma versão específica do tempo de execução do WebView2.  O modo de distribuição de versão fixa permite que você controle qual versão do tempo de execução do WebView2 é usada pelo seu aplicativo e quando as máquinas do usuário são atualizadas.  O modo de distribuição de versão fixa não recebe atualizações automáticas, e os desenvolvedores devem planejar a aplicação de atualizações.  


<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Noções básicas sobre versões do navegador e WebView2 | Documentos da Microsoft"  
[ReferenceWin3209622WebviewIdl]: ../reference/win32/0-9-622/webview2-idl.md  "Globais | Documentos da Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador do WebView2"  
