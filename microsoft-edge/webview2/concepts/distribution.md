---
description: Opções de distribuição ao liberar um aplicativo usando o Microsoft Edge WebView2
title: Distribuição do aplicativo Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: ec623da0181a4f21c3192652b0d098f922225b0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697921"
---
# Distribuição de aplicativos usando o WebView2 

O controle WebView2 utiliza o navegador Microsoft Edge \ (Chromium \). Ao distribuir seu aplicativo, verifique se o navegador de borda está instalado em todas as máquinas de usuário em que seu aplicativo é executado. O controle WebView2 usa a versão mais estável do navegador que está instalada em um computador. Por exemplo, você pode ter estáveis, beta, dev e Canárias instalados ao mesmo tempo e, nesta situação, os controles WebView2 são executados no canal estável. Verifique se você revisar as notas de versão para garantir que a versão do navegador instalada em suas máquinas que executam os controles de WebView2 atenda aos requisitos mínimos de versão.

## Mapa

Reconhecemos que o navegador Edge pode não estar disponível em todas as máquinas de usuário em que seu aplicativo será executado ou que a instalação do navegador do Edge em toda a organização possa ser difícil. Para garantir que seu aplicativo seja executado em todas as máquinas, independentemente do navegador Microsoft Edge instalado, liberaremos o tempo de execução do Microsoft Edge WebView2. Além disso, atualizaremos o WebView2 para pesquisar a versão estável do tempo de execução antes de Pesquisar versões de pré-lançamento do navegador instalado.

Haverá suporte para duas opções de distribuição usando o tempo de execução do WebView2: a versão do baixo e a correção.

O verde será o modelo de distribuição recomendado para a maioria dos desenvolvedores. Nesse modo, as atualizações são enviadas automaticamente para o tempo de execução do WebView2 sem esforço adicional do seu aplicativo. O modelo verde garante que seu aplicativo aproveite os recursos e atualizações de segurança mais recentes para conteúdo da Web hospedado.

Para ambientes restritos, haverá suporte para um modelo de distribuição de versão fixa. Nesse modelo, seu aplicativo seleciona e empacota uma versão específica do WebView2. As atualizações para a versão do WebView não ocorrem automaticamente e serão de responsabilidade do aplicativo. O modelo de versão fixa é benéfico quando você precisa controlar a versão do navegador e quando o aplicativo é atualizado. 

### Microsoft Edge WebView2 Runtime

O tempo de execução do Microsoft Edge WebView2 compacta os binários do navegador otimizados para uso por aplicativos do WebView2. Ele funcionará de forma autônoma ou lado a lado com um navegador cliente Edge instalado. Instalar o Runtime uma vez dará suporte a muitos aplicativos do WebView2 em execução no computador cliente. A instalação do tempo de execução não aparecerá como um navegador para usuários finais e não terá atalhos da área de trabalho, ponto de entrada do menu iniciar ou registro de protocolo.

Os aplicativos que usam o tempo de execução WebView2 precisarão garantir que a instalação do tempo de execução seja concluída. Para garantir que seu aplicativo instale o tempo de execução como uma dependência, você poderá adicionar o tempo de execução ao seu fluxo de instalação. 
