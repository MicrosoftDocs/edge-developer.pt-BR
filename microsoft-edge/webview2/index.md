---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Controle WebView2 do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, HTML de borda, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: 4f28ef64bb2936bc6c9a089ea2574070738fc79d
ms.sourcegitcommit: 8f5c9255dadc2a9bb22c3201d15b57d84851fe64
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "10671635"
---
# Introdução ao Microsoft Edge WebView2 (visualização)  

O controle WebView2 do Microsoft Edge permite que você incorpore tecnologias da Web \ (HTML, CSS e JavaScript \) em seus aplicativos nativos.  O controle WebView2 usa o [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com) como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.  Com o WebView2, você pode inserir código da Web em diferentes partes do seu aplicativo nativo ou criar todo o aplicativo nativo em um único WebView.  Para saber mais sobre como começar a criar um aplicativo do WebView2, consulte [introdução](./index.md#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="O que é o WebView":::
   O que é o WebView  
:::image-end:::  

> [!NOTE]
> A visualização do WebView2 foi desenvolvida para o início do protótipo e para coletar comentários e para ajudar a moldar a API.  A equipe do Microsoft Edge WebView não recomenda que você use a visualização em seus aplicativos de produção, pois pode haver [alterações significativas](./releasenotes.md).  

## Abordagem do aplicativo híbrido  

Geralmente, os desenvolvedores precisam escolher entre a criação de um aplicativo Web ou um aplicativo nativo.  As dobradiças de decisão sobre a compensação entre o alcance e a potência.  Os aplicativos da Web permitem um amplo alcance.  Como um desenvolvedor da Web, você pode reutilizar a maioria, se não todo o seu código, em todas as plataformas diferentes.  No entanto, os aplicativos nativos utilizam os recursos de toda a plataforma nativa.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native":::
   Web Native  
:::image-end:::  

Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.  Os desenvolvedores de aplicativos híbridos se beneficiam do Ubiquity e da força da plataforma da Web, e da capacidade e dos recursos completos da plataforma nativa.  

## Benefícios do WebView2   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos da WebView":::
   Motivos da WebView  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Ecossistema da Web \ & conjunto de qualificações**  
      Use toda a plataforma da Web, bibliotecas, ferramentas e talento existentes dentro do ecossistema da Web.  
   :::column-end:::
   :::column span="1":::
      **Inovação rápida**  
      O desenvolvimento na Web permite implantação e iteração mais rápidas.  
   :::column-end:::
   :::column span="1":::
      **Suporte do Windows 7, 8, 10**  
      Suporte para uma experiência de usuário consistente em todo o Windows 7, 8 e 10.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Recursos nativos**  
      Acesse o conjunto completo de APIs nativas.  
   :::column-end:::
   :::column span="1":::
      **Compartilhamento de código**  
      Adicionar código da Web à sua codebase permite maior reutilização em várias plataformas.  
   :::column-end:::
   :::column span="1":::
      **Suporte da Microsoft**  
      A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado como GA.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Distribuição para o meio-verde**  
      Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e correções de segurança.  
   :::column-end:::
   :::column span="1":::
      **Corrigido** \ (em breve \)  
      Escolha para empacotar os bits Chromium em seu aplicativo.  
   :::column-end:::
   :::column span="1":::
      **Adoção incremental**  
      Adicione componentes Web por parte do seu aplicativo.  
   :::column-end:::
:::row-end:::  

## Introdução  

Para compilar e testar seu aplicativo usando o controle WebView2, você precisa ter o [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download) e o [SDK do WebView2](https://aka.ms/webviewnuget) instalado.  Selecione uma das seguintes opções para começar.  

*   [Introdução ao Win32 C/C++](./gettingstarted/win32.md)  
*   [Introdução ao WPF](./gettingstarted/wpf.md)  
*   [Introdução ao WinForms](./gettingstarted/winforms.md)  

O repositório de [exemplos WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contém exemplos que demonstram todos os recursos de SDKs do WebView2 e padrões de uso de APIs. Conforme mais recursos forem adicionados ao SDK do WebView2, os aplicativos de exemplo serão atualizados.   

## Plataformas com suporte  

Uma visualização do desenvolvedor está disponível nos seguintes ambientes de programação:  

*   Win32 C/C++  
*   .NET Framework 4.6.2 ou posterior  
*   .NET Core 3,0 ou posterior  
*   [WinUI 3,0](/uwp/toolkits/winui3/)  

Você deve executar o Windows 10, o Windows 8,1, o Windows 8, o Windows 7, o Windows Server 2016, o Windows Server 2012/2012R2 ou o Windows Server 2008 R2.   

## Próximas etapas  

Para obter informações mais detalhadas sobre como criar e implantar aplicativos WebView2, desfaça checkout da nossa documentação conceitual<!-- and how-to guides-->.  

#### Conceitos  

*   [WebView2 SDK e controle de versão do Microsoft Edge](./concepts/versioning.md)
*   [Distribuir aplicativos do WebView2](./concepts/distribution.md)  
 
#### Guias de instruções  

*   [Depuração de WebView2 com o DevTools e depuração de script do Visual Studio](./howto/debug.md)  
*   [Automatizando e Depurando o WebView2 com o Microsoft EdgeDriver](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## Entrar em contato com a equipe do WebView2  

Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.  Acesse o [repositório de comentários](https://aka.ms/webviewfeedback) da WebView para enviar solicitações de recursos ou relatórios de erros.  Também é um bom lugar para procurar problemas conhecidos.  

> [!NOTE]
> Durante a visualização do desenvolvedor, a equipe do Microsoft Edge WebView também coleta dados para ajudar a criar um WebView melhor.  Os usuários podem desativar a coleta de dados do WebView ao navegar `edge://settings/privacy` no navegador Microsoft Edge e desativar a coleta de dados do navegador.  
