---
description: Modo IE e o Microsoft Edge (Chromium) DevTools
title: Modo Internet Explorer e o DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, ie11, internet explorer 11, modo ie
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643232"
---
# <a name="internet-explorer-mode-and-the-devtools"></a>Modo Internet Explorer e o DevTools  

Este artigo descreve como o modo do Internet Explorer \(modo IE\) se integra ao Microsoft Edge \(Chromium\) DevTools.  

## <a name="understanding-ie-mode"></a>Noções básicas sobre o modo IE  

O modo IE permite que as empresas especifiquem uma lista de sites que funcionam apenas no Internet Explorer 11.  Quando você navega para esses sites em Microsoft Edge \(Chromium\), uma instância do Internet Explorer 11 é executado e renderiza o site em uma guia.  A funcionalidade permite que as empresas gerenciem a compatibilidade com tecnologias que atualmente não são compatíveis com nenhum navegador moderno da Web.  O suporte para as seguintes tecnologias está incluído no modo IE.  

*   Modos de documento do IE  
*   Controles ActiveX  
*   outros componentes herdados  

No modo IE, o processo de renderização é baseado no Internet Explorer 11.  O Microsoft Edge do processo \(Chromium\) lida com o tempo de vida do processo de renderização.  Ele é restrito ao tempo de vida da guia para um site específico \(ou app\).  Quando uma guia é renderiza no modo IE, um selo aparece na barra de endereços da guia específica.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Selo do modo IE na barra de endereços" lightbox="../media/ie-mode-badge.msft.png":::
   Selo do modo IE na barra de endereços  
:::image-end:::  

O modo IE está disponível no momento no Windows 10 Versão 1903 \(Atualização de maio de 2019\), mas está chegando em breve a todas as plataformas Windows com suporte.  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a>Iniciando o DevTools em uma guia no modo IE  

Se você estiver tentando exibir o modo de documento de um site no modo IE, escolha o selo na barra de endereços.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Exibir o modo de documento usando o selo do modo IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Exibir o modo de documento usando o selo do modo IE  
:::image-end:::  

Se uma guia estiver usando o modo IE, o DevTools não funcionará e as seguintes condições ocorrerão.

*   Se você selecionar ou selecionar , uma instância em branco do `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools será lançada exibirá a seguinte mensagem.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Se você abrir um menu contextual \(clique com o botão direito do mouse\) e escolher **Exibir Fonte**, Bloco de notas será lançado.  
*   Se você abrir um menu contextual \(clique com o botão direito do mouse\), o **Elemento Inspect** não será visível.  

O motivo pelo qual várias ferramentas dentro do DevTools **** \(como as ferramentas de Rede e Desempenho\) não funcionam é que o mecanismo de renderização alterna do Chromium para o Internet Explorer 11 no modo IE. ****  Para fornecer comentários, navegue até Entrar em [contato com a equipe Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools lançado no modo IE" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools lançado no modo IE  
:::image-end:::  

Para testar seu site baseado no Internet Explorer 11 \(ou app\) no modo Internet Explorer 11 e IE, execute as etapas a seguir.  

1.  Abra o Internet Explorer 11.  
    *   No Windows 10, localize o atalho para o Internet Explorer 11.
        1.  **Menu Iniciar**  >  **Windows Acessórios**  >  **Internet Explorer 11**.  
    *   No Windows 7, localize o Internet Explorer 11.
        1.  **Menu Iniciar**  >  **Internet Explorer 11**.  
1.  No Internet Explorer 11, abra a mesma página da Web.  
1.  Iniciar o Internet Explorer DevTools.  
    *   Selecione `F12` .  
    *   Passe o mouse em qualquer lugar, abra um menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar elemento**.  Para obter mais informações sobre como usar essas ferramentas, navegue até [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

Se o Internet Explorer 11 não estiver disponível, como no Windows 11, você poderá usar o IEChooser para iniciar o Internet Explorer DevTools para depurar o conteúdo das guias de modo IE. Para usar o IEChooser, execute as etapas a seguir.

1.  Abra IEChooser.
    1. Abra a caixa de diálogo Executar. Por exemplo, pressione `Windows logo key`  +  `R` o .
    2. Insira `%systemroot%\system32\f12\IEChooser.exe` e selecione **Ok**.
2.  No IEChooser, selecione a entrada para a guia Modo IE.


## <a name="remote-debugging-and-ie-mode"></a>Modo de depuração remota e IE  

Iniciar Microsoft Edge \(Chromium\) com a depuração remota acionda a partir da interface de linha de comando.  Microsoft Visual Studio, Microsoft Visual Studio Código e outras ferramentas de desenvolvimento normalmente executem um comando para iniciar Microsoft Edge.  O comando a seguir inicia Microsoft Edge com a porta de depuração remota definida como `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

Depois de iniciar Microsoft Edge \(Chromium\) usando um argumento de linha de comando, o modo IE fica indisponível.  Você ainda pode navegar para sites \(ou aplicativos\) que são exibidos de outra forma no modo IE.  O conteúdo do site \(ou app\) é render Chromium, não o Internet Explorer 11.  Espere que as partes das páginas da Web que dependem do IE11, como controles ActiveX, não renderizar corretamente.  O selo do modo IE não aparece na barra de endereços.  

O modo IE permanece indisponível até que você feche completamente e reinicie Microsoft Edge \(Chromium\).  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Usando as ferramentas de desenvolvedor F12 | Microsoft Docs"  
