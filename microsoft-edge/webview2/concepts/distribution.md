---
description: Opções de distribuição ao liberar um aplicativo usando o Microsoft Edge WebView2
title: Distribuição do aplicativo Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 1b7ebf9dde594b7cdac3b41915fa9d9187d09da1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879174"
---
# Distribuição de aplicativos usando o WebView2  

O controle WebView2 utiliza a plataforma Microsoft Edge \ (Chromium \).  Ao empacotar e distribuir seu aplicativo, certifique-se de que uma cópia da plataforma ou do tempo de execução do WebView2 está presente antes do início do aplicativo.  A página a seguir descreve como você \ (o desenvolvedor \) pode garantir que o tempo de execução do WebView2 está instalado e usar os dois modos de distribuição para seu aplicativo do [WebView2:](#evergreen-distribution-mode) versão do meio e [fixo](#fixed-version-distribution-mode).  

## Modo de distribuição do verde  

O modo de distribuição do verde garante que seu aplicativo Tire proveito dos recursos e das atualizações de segurança mais recentes.  O modo de distribuição do verde tem as características a seguir.  

*   A plataforma da Web é atualizada automaticamente sem esforço adicional.  
*   Todos os aplicativos que aproveitam o modo de distribuição verde usam uma cópia compartilhada dos binários da plataforma, o que poupa espaço em disco.  

Há vários canais WebView2 que os aplicativos podem usar como a plataforma da Web.  Por padrão, o WebView2 direciona o canal mais estável disponível no dispositivo que atende ao requisito mínimo de versão do SDK do WebView2.  Os canais a seguir estão listados em ordem do canal mais para o menos estável.  

1.  Tempo de execução do WebView2 \ (visualização \)  
1.  Canal Microsoft Edge Beta  
1.  Canal Microsoft Edge Dev  
1.  Canal Microsoft Edge Canary    

> [!NOTE]
> O modelo de distribuição verde é recomendado para a maioria dos desenvolvedores.  

> [!IMPORTANT]
> O canal estável do Microsoft Edge não é um destino válido para WebView2, e os motivos são descritos mais tarde.  

Para obter mais informações sobre controle de versão, consulte [versionamento][ConceptsVersioning] e [globais][ReferenceWin3209538WebviewIdl].  

### Entender o tempo de execução do WebView2 e o instalador (visualização)  

O canal estável do Microsoft Edge pode não ser instalado em todas as máquinas de usuário em que seu aplicativo é executado.  Em vez de exigir que os usuários instalem o Microsoft Edge, seu aplicativo pode usar o tempo de execução do WebView2 e o instalador do verde \ (Preview \).  O tempo de execução do WebView2 é uma cópia personalizada dos binários do Microsoft Edge que é usada para executar seus aplicativos do WebView2.  Quando o tempo de execução do WebView2 estiver instalado, os usuários não poderão usá-lo como um navegador normal.  Por exemplo, não há um atalho da área de trabalho, entrada do menu Iniciar, os usuários não podem abrir uma janela do navegador usando os binários do tempo de execução e assim por diante.  Todos os aplicativos de WebView2 em verde no dispositivo podem usar uma única instalação de tempo de execução do WebView2 verde.  

Hoje durante a visualização, o ambiente de tempo de execução do Microsoft Edge e o tempo de execução do Microsoft Edge WebView2 são atualizados ao mesmo tempo e têm a mesma compilação.  No futuro, durante a visualização, a equipe do WebView2 planeja atualizar o tempo de execução do WebView2 e corresponder à mesma compilação que o canal do Microsoft Edge beta.  No futuro, quando o WebView2 atingir a disponibilidade geral \ (GA \), a equipe do WebView2 planeja atualizar o tempo de execução do WebView2 e corresponder à mesma compilação que o canal estável do Microsoft Edge.  Após o GA, os aplicativos devem usar o tempo de execução do WebView2 em produção.  

> [!IMPORTANT]
> Não envie aplicativos WebView2 em produção durante a visualização.  

Os desenvolvedores são recomendados para garantir que o tempo de execução do WebView2 do verde seja instalado antes de iniciar o aplicativo. Veja a seguir um exemplo de fluxo de trabalho.  

1.  Baixe o instalador mais recente do [WebView2 tempo de execução do verde][Webview2Installer].  
1.  Inclua o instalador no instalador do aplicativo ou no atualizador.  
1.  Durante a instalação ou atualização do aplicativo, verifique se o tempo de execução do WebView2 está instalado no computador do usuário usando a API [GetAvailableCoreWebView2BrowserVersionString](../reference/win32/0-9-538/webview2-idl.md#getavailablecorewebview2browserversionstring) e verificando se o VERSIONINFO é nulo. Se não estiver instalado, o instalador do aplicativo/atualizador pode invocar silenciosamente o instalador do tempo de execução de um processo elevado ou prompt de comando com `MicrosoftEdgeWebView2RuntimeInstallerX64.exe /silent /install` . 

Dependendo do cenário, talvez seja necessário alterar o fluxo de trabalho acima.  Por exemplo, o instalador do aplicativo pode baixar o instalador do tempo de execução do WebView2 em vez de incluí-lo em seu pacote de aplicativo.  

> [!NOTE]
> O instalador de tempo de execução do WebView2 e do WebView2 está em visualização.  A visualização tem um escopo inicial limitado e só está disponível como uma instalação autônoma para cada computador no Windows 10 em x64.  No futuro, o suporte para Windows 7, x86 e ARM64 é planejado.  

### Práticas recomendadas para usar o tempo de execução do WebView2 e canais não estáveis do Microsoft Edge  

Considere as seguintes recomendações durante a visualização.  

*   Certifique-se de usar o [tempo de execução do WebView2 e o instalador do verde][Webview2Installer] para desenvolver ou testar o seu pipeline de distribuição e empacotamento.  No futuro, o aplicativo de produção deve incluir o instalador.  
*   Para desenvolver seu aplicativo, você pode usar o tempo de execução do WebView2 em verde.  No entanto, como o tempo de execução muda do canal de desenvolvimento para o canal beta ou canal estável, o número da compilação do tempo de execução pode não atender aos requisitos de versão mínima do SDK do SDK da visualização mais recentes.  Se você quiser usar o SDK mais recente, instale o Microsoft Edge Canárias Channel para garantir que uma compilação compatível esteja disponível no dispositivo.  Para obter mais informações sobre controle de versão, consulte [controle de versão][ConceptsVersioning].  
*   Para testar o conteúdo da Web quanto à compatibilidade com as alterações na plataforma não disponíveis no canal estável, use o canal não estável adequado, conforme necessário.  

## Modo de distribuição de versão corrigido  

> [!NOTE]
> O modelo de distribuição de versão fixa não está disponível no momento.  

Para ambientes restritos, há planos para dar suporte a um modo de distribuição \ versão corrigida \ (anteriormente denominado trazer anteriormente chamado \).  O modo de distribuição de versão fixa permite que você selecione e empacote uma versão específica do tempo de execução do WebView2.  O modo de distribuição de versão fixa permite que você controle qual versão do tempo de execução do WebView2 é usada pelo seu aplicativo e quando as máquinas do usuário são atualizadas.  O modo de distribuição de versão fixa não recebe atualizações automáticas e você deve planejar a aplicação manual de atualizações.  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Noções básicas sobre versões do navegador e WebView2 | Documentos da Microsoft"  
[ReferenceWin3209538WebviewIdl]: ../reference/win32/0-9-538/webview2-idl.md  "Globais | Documentos da Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador do WebView2"  
