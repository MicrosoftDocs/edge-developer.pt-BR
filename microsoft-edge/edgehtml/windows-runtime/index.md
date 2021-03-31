---
description: Use o Windows Runtime (WinRT) para chamar APIs nativas do Windows a partir do seu aplicativo JavaScript.
title: Tempo de execução do Windows (WinRT) para JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Tempo de execução do Windows, WinRT, PWA, JavaScript
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bd67f052d0a836c754f7b58d0625e09ae8781cd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231969"
---
# Tempo de execução do Windows (WinRT) para JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

O [tempo de execução do Windows](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \(ou simplesmente WinRT \) é a coleção de APIs nativas que reforçam os aplicativos da [plataforma universal do Windows](/windows/uwp/get-started/universal-application-platform-guide) \(UWP \) que são executados em todas as famílias de dispositivos do [Windows 10](/uwp/extension-sdks/device-families-overview).  As APIs do WinRT são projetadas em vários idiomas diferentes, incluindo C#, C++, Visual Basic e JavaScript.  

Como um desenvolvedor da Web, você pode solicitar essas APIs nativas do Windows em JavaScript quando seu aplicativo Web estiver [sendo executado como um aplicativo do Windows 10 instalado](../progressive-web-apps/windows-features.md#set-up-and-run-your-universal-windows-app) \(iniciado do `wwahost.exe` processo, em vez do navegador \).  Além disso, seu site executando como um aplicativo do Windows 10 também pode usar o controle [WebView da Microsoft Edge](#webview) para exibir conteúdo da Web remoto e local e APIs [MSApp](#msapp) para BLOB e manipulação de fluxo, entre outras coisas.  

Aqui estão as áreas de namespace do WinRT de nível superior disponíveis para todos os aplicativos do Windows 10:  

| Namespace do WinRT | Descrição |  
|:--- |:--- |  
| [Ai](/uwp/api/windows.AI.MachineLearning.Preview) \(visualização \) | Contém classes que permitem que os aplicativos carreguem modelos de aprendizagem de máquina, associem dados como entradas e avaliem os resultados.  |  
| [ApplicationModel](/uwp/api/windows.applicationmodel) | Fornece um aplicativo com acesso a funcionalidades principais do sistema e informações em tempo de execução sobre o pacote do aplicativo e manipula operações de suspensão.  |  
| [Dados](/uwp/api/windows.data.html) | Fornece classes de utilitário para trabalhar com vários formatos de dados, incluindo HTML, JSON, PDF, texto e XML.  |  
| [Devices](/uwp/api/windows.devices) | Esse namespace fornece acesso aos provedores de dispositivos de nível inferior, incluindo ADC, GPIO, I2 C, PWM e SPI.  |  
| [Foundation](/uwp/api/windows.foundation) | Habilita a funcionalidade básica do Windows Runtime, incluindo o gerenciamento de operações assíncronas e o acesso a repositórios de propriedades  Esse namespace também define tipos de valor comuns que representam identificador de recursos uniforme \(URI \), datas e horas, medidas 2D e outros valores básicos.  |  
| [Jogos](/uwp/api/windows.gaming.input) |Fornece acesso à entrada do controlador de jogo, à barra de jogos, ao monitoramento de jogos e ao chat do jogo.  |  
| [Globalização](/uwp/api/windows.globalization) | Fornece suporte à globalização para perfis de idioma, regiões geográficas e calendários internacionais.  |  
| [Elementos gráficos](/uwp/api/windows.graphics) | Fornece tipos de dados básicos que contêm informações sobre como desenhar elementos gráficos.  Essas estruturas de dados geralmente são usadas para definir como superfícies grandes são desenhadas ao usar a classe CompositionVirtualDrawingSurface.  |  
| [Management](/uwp/api/windows.management) | Fornece recursos para forçar uma sincronização de um dispositivo de gerenciamento de dispositivo móvel (MDM \) para o servidor.  Este protocolo de sincronização de MDM é baseado no padrão de gerenciamento de dispositivo móvel de aliança móvel.  |  
| [Media](/uwp/api/windows.media) | Fornece classes para criar e trabalhar com mídia, como fotos, gravações de áudio e vídeos.  |  
| [Rede](/uwp/api/windows.networking) | Fornece acesso a nomes de host e pontos de extremidade usados por aplicativos de rede.  |  
| [Percepção](/uwp/api/windows.perception) | Contém classes para a movimentação dos arredores do usuário, permitindo que os aplicativos localizem e motivom sobre o dispositivo relativo às superfícies e hologramas ao redor do usuário.  |  
| [Segurança](/uwp/api/windows.security.authentication.identity) | Fornece classes para autenticação de usuário, gerenciamento de credenciais, operações criptográficas e recursos de proteção de dados corporativos.  |  
| [Serviços](/uwp/api/windows.services.cortana) | Fornece acesso aos serviços da Microsoft para a Cortana, mapas, à Microsoft Store e direcionado o conteúdo de \(assinatura \).  |  
| [Armazenamento](/uwp/api/windows.storage) | Fornece classes para gerenciar arquivos, pastas e configurações de aplicativo.  |  
| [Sistema](/uwp/api/windows.system) | Habilita a funcionalidade do sistema, como iniciar aplicativos, obter informações sobre um usuário e a criação de perfil de memória.  |  
| [Interface do Usuário](/uwp/api/windows.ui) | Fornece um aplicativo com acesso a funcionalidades principais do sistema e informações em tempo de execução sobre a interface do usuário.  **Observação**: as APIs no `Windows.UI.Xaml` namespace não estão disponíveis para aplicativos JavaScript \(que podem usar as tecnologias baseadas em padrões da Web equivalentes \).  |  
| [Web](/uwp/api/windows.web) | Fornece informações sobre erros resultantes de operações de serviço Web.  |  

Para obter mais detalhes sobre o uso, confira [usando o tempo de execução do Windows em JavaScript](./using-the-windows-runtime-in-javascript.md).  Para saber como executar seu site como um aplicativo do Windows, tente personalizar o tutorial do [seu PWA para Windows](../progressive-web-apps/windows-features.md) .  

## WebView  

O controle [WebView da Microsoft Edge](../hosting/webview/index.md) permite que você hospede conteúdo da Web em seu aplicativo do Windows 10.  Isso é semelhante a usar um `<iframe>` , mas oferece muito [mais recursos e controle](../hosting/webview/index.md#webview-versus-iframe) sobre a experiência.  

## MSApp  

O objeto global [MSApp](./reference/msapp.md) \( `window.MSApp` \) fornece funções auxiliares ordenadas para aplicativos do Windows 10 baseados em JavaScript, como utilitários para conversão entre tipos de objetos do WinRT baseados em padrões da Web e equivalentes.  
