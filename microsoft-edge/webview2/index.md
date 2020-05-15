---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b1ec0c43b57fb107490ddb34b330bb6ec378ac41
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652451"
---
# Microsoft Edge WebView2 (prévia do desenvolvedor)

O controle WebView2 do Microsoft Edge permite que você hospede conteúdo da Web em seu aplicativo usando o [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/) como mecanismo de renderização.

O controle WebView2 está atualmente na visualização do desenvolvedor, durante o qual você pode compartilhar suas soluções e compartilhar comentários conosco para moldar a próxima API estável. Provavelmente haverá algumas alterações significativas ao desenvolvermos a API durante a visualização e, quando isso acontecer, você precisará ter o SDK do WebView2 e o navegador do Microsoft Edge (Chromium) atualizados. As alterações significativas serão observadas nas [notas de versão](./releasenotes.md) do SDK. Isso travará como WebView2 abordagens beta e estável.

## Plataformas com suporte

Uma visualização do desenvolvedor está disponível para Win32 C/C++ e Windows Forms e WPF no .NET Framework 4.6.2 ou posterior e .NET Core 3,0 ou posterior no Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 e Windows Server 2008 R2. Uma versão Alpha para WinUI 3,0 está disponível [aqui](https://docs.microsoft.com/uwp/toolkits/winui3/).

## Introdução

Para compilar e testar seu aplicativo usando o controle WebView2, você precisa ter o [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) e o [SDK do WebView2](https://aka.ms/webviewnuget) instalado. Selecione uma das opções abaixo para começar!

* [Introdução ao Win32 C/C++](./gettingstarted/win32.md)
* [Introdução ao WPF](./gettingstarted/wpf.md)
* [Introdução ao Windows Forms](./gettingstarted/winforms.md)

Envie-nos comentários em nosso repositório de [comentários WebView2](https://aka.ms/webviewfeedback) .

## Exemplos de WebView2

O repositório de [exemplos WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contém exemplos que demonstram todos os recursos do SDK do WebView2 e seus padrões de uso da API. À medida que adicionamos mais recursos ao SDK do WebView2, atualizaremos regularmente nossos aplicativos de exemplo.

## Distribuição de aplicativos

O controle WebView2 utiliza o navegador Microsoft Edge (Chromium). Ao distribuir seu aplicativo, é importante garantir que o navegador do Edge seja instalado em todas as máquinas do usuário onde o aplicativo será executado. Você também deve estar ciente de qual versão e canal está instalado, por exemplo, estável, beta, dev ou Canárias. O controlador WebView2 usará a versão mais estável do navegador quando instalado em um computador.

### Alterações planejadas futuras

Reconhecemos que o navegador Edge pode não estar disponível em todas as máquinas de usuário que o aplicativo pretende executar ou que o controle de instalação do navegador Edge pode ser difícil. Para garantir que seu aplicativo será executado em todos os computadores, independentemente do status de instalação do navegador cliente Microsoft Edge, liberaremos o tempo de execução do Microsoft Edge WebView2. Atualizaremos ainda mais o WebView2 para pesquisar a versão estável do tempo de execução antes de Pesquisar versões de pré-lançamento do navegador instalado.

Reconhecemos também que alguns desenvolvedores de aplicativos operam em ambientes restritos e, portanto, pretendem dar suporte a duas opções de distribuição, a versão verde e fixa.

O sempre é o modelo de distribuição recomendado para a maioria dos desenvolvedores. Nesse modo, as atualizações do tempo de execução do WebView2 serão totalmente gerenciadas pela Microsoft, o que o manterá atualizado automaticamente, sem esforço adicional do seu aplicativo. Com este modelo de autoatualização, você pode ter certeza de que seu aplicativo está aproveitando os recursos e atualizações de segurança mais recentes para conteúdo da Web hospedado.

Para ambientes restritos, também vamos dar suporte a um modelo de distribuição de versão fixa. Nesse modelo, seu aplicativo selecionará e empacotará uma versão específica do WebView2. As atualizações para a versão do WebView serão a responsabilidade do aplicativo e serão independentes de qualquer mecanismo gerenciado do Microsoft Update. Você deve escolher esse modelo se for crucial poder ter controle absoluto sobre a versão do navegador e atualizar o tempo de aproveitamento do aplicativo.

## Microsoft Edge WebView2 Runtime

O tempo de execução do Microsoft Edge WebView2 é uma embalagem dos binários do navegador otimizados para uso por aplicativos do WebView2. Ele funcionará de forma autônoma ou lado a lado com uma instalação do navegador de borda do cliente. Uma única instalação do tempo de execução aceitará qualquer número de aplicativos WebView2. A instalação do tempo de execução não aparecerá como uma instalação do navegador para o usuário final, isto é, nenhum atalho da área de trabalho, entrada do menu iniciar ou registro de protocolo.

Um aplicativo que usa o WebView2 deve garantir que a instalação do Microsoft Edge WebView2 o tempo de execução ocorreu. No momento da instalação do aplicativo, você deve verificar o status de instalação atual, que pode ser determinado usando [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring). Se o tempo de execução do WebView2 não estiver disponível, você deve encadear o instalador do Microsoft Edge WebView2 Runtime para o fluxo de instalação.

## SDK do Microsoft Edge WebView2

Para usar o WebView2 em seu aplicativo, você precisará instalar e referenciar o [SDK do WebView2](https://aka.ms/webviewnuget) em seu aplicativo. Nossas versões do NuGet conterá uma versão de pré-lançamento e de pré-lançamento. A versão de lançamento contém as APIs públicas que atualmente pretendem liberar para a disponibilidade geral.

A versão de pré-lançamento conterá [APIs experimentais](./reference/win32/0-9-488-reference-webview2.md#experimental)adicionais. Estes são APIs e funcionalidades que estamos avaliando e gostaria de fazer [comentários](https://aka.ms/webviewfeedback) antes de promovê-los para a versão de lançamento.

## Desenvolvimento em versões futuras

Para o desenvolvimento, talvez você queira direcionar a versão beta, dev ou Canárias para garantir que seu aplicativo funcione com versões futuras ou aproveite os recursos futuros. Todos os canais já liberados são fornecidos pelo navegador cliente instalado da Microsoft Edge. Para direcionar um desses canais, certifique-se de que o navegador de borda instalado em seu computador de desenvolvimento seja o canal que você deseja. Os desenvolvedores podem usar uma chave do registro ou uma variável de ambiente para alterar o WebView2 da versão mais estável encontrada para o menos estável encontrado. Veja mais detalhes no [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).

## Depurando WebView2

### DevTools

Você pode usar as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) para depurar o conteúdo da Web exibido no WebView, da mesma forma que faria no navegador. Enquanto estiver com o foco na janela do WebView, pressione `F12` ou pressione ou `Ctrl`  +  `Shift`  +  `I` clique com o botão direito do mouse + escolha `Inspect` para abrir as ferramentas de desenvolvedor.

:::image type="complex" source="./media/f12.png" alt-text="F12":::
   F12
:::image-end:::  

<!--![F12](./media/f12.png)  -->  

**Observação Quando a depuração de aplicativo no Visual Studio com o depurador nativo anexado, `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor. Use `Ctrl`  +  `Shift`  +  `I` ou clique com o botão direito do mouse em + `Inspect` para evitar possível conflito de teclas de atalho.**

### Visual Studio

Você pode usar o depurador de script no Visual Studio 2019 (versão mínima 16,4 Preview 2) para depurar o script no WebView2 diretamente do IDE. Certifique-se de que o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.

:::image type="complex" source="./media/vs-js-diagnostics.jpg" alt-text="Diagnóstico do JavaScript do Visual Studio":::
   Diagnóstico do JavaScript do Visual Studio
:::image-end:::  

<!--![vs-js-diagnostics](./media/vs-js-diagnostics.jpg)  -->  

Clique com o botão direito do mouse no projeto e selecione **Propriedades**. Em **Propriedades de configuração**  >  **Debugging**  >  **tipo de depurador**de depuração, escolha a opção **JavaScript (WebView2)** para habilitar a depuração de script WebView2. Mais detalhes para acompanhar em breve.

:::image type="complex" source="./media/vs-script-debugger.jpg" alt-text="Depurador de scripts do Visual Studio":::
   Depurador de scripts do Visual Studio
:::image-end:::  

<!--![vs-script-debugger](./media/vs-script-debugger.jpg)  -->  

### Visual Studio Code

Você também pode usar o código do Visual Studio para depurar o script no WebView2 diretamente do IDE. Para obter mais detalhes, clique [aqui](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).

## Entrar em contato com a equipe do WebView2  

Ajude-nos a criar uma experiência WebView2 mais rica compartilhando seus comentários! Acesse nosso [repositório de comentários](https://aka.ms/webviewfeedback) para enviar solicitações de recursos ou relatórios de erros.

Também é um bom lugar para procurar problemas conhecidos.
Durante a visualização do desenvolvedor, também coletaremos dados de telemetria para nos ajudar a construir um WebView melhor. Os usuários podem desativar a coleta de dados do WebView navegando para edge://settings/privacy no navegador e desativando a coleta de dados do navegador.
