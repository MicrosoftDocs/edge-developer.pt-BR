---
description: Todas as maneiras de abrir o Microsoft Edge DevTools.
title: Abra Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a6e83d0651c5611b53735447f6ddc34c90550db1
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643438"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->
# <a name="open-microsoft-edge-devtools"></a>Abra Microsoft Edge DevTools  

Há muitas maneiras de abrir Microsoft Edge DevTools, ajudando você a acessar rapidamente diferentes partes da interface do usuário do DevTools. 

## <a name="open-microsoft-edge-devtools"></a>Abra Microsoft Edge DevTools  

Para abrir o DevTools, use uma das seguintes opções.  

*   Use a interface Microsoft Edge interface do usuário.
    *  Escolha o **Configurações e mais** \( \) ícone > Ferramentas de Desenvolvedor mais `...` ****  >   **Ferramentas.**  
    
*   Use o teclado.  
    *   Selecione `F12` `Control` + `Shift` + `I` ou \(Windows, Linux\) `Command` + `Option` + `I` ou \(macOS\).  

Para obter mais informações, navegue até Microsoft Edge atalhos de teclado [do DevTools.][DevtoolsShortcutsIndex]  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abra DevTools no menu Microsoft Edge principal" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abra DevTools no menu Microsoft Edge principal  
:::image-end:::  

## <a name="open-the-elements-panel-to-inspect-the-dom-or-css"></a>Abra o painel Elementos para inspecionar o DOM ou CSS  

Uma das tarefas a seguir permite inspecionar os estilos ou atributos de um nó Modelo de [Objeto de](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) Documento \(DOM\).

*   Passe o mouse no elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
*   Selecione `Control` + `Shift` + `C` \(Windows, Linux\) `Command` + `Option` + `C` ou \(macOS\). Para obter mais informações, navegue até Microsoft Edge atalhos de teclado [do DevTools.][DevtoolsShortcutsIndex]  

<!-- :::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="The Inspect option" lightbox="../media/bing-right-click-inspect.msft.png":::
   The **Inspect** option  
:::image-end:::  --> 

<!--Navigate to [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <a name="open-the-console-panel"></a>Abra o painel console  

Para abrir o [painel console][DevtoolsConsoleIndex] para exibir mensagens registradas ou executar o JavaScript, selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\). Para obter mais informações, navegue até Microsoft Edge atalhos de teclado [do DevTools.][DevtoolsShortcutsIndex]  

<!--Navigate to [Get Started With The Console][ConsoleGetStarted].  -->

## <a name="open-the-previous-panel"></a>Abra o painel anterior  

Para pular para o painel aberto anteriormente, selecione `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).  Para obter mais informações, navegue até Microsoft Edge atalhos de teclado [do DevTools.][DevtoolsShortcutsIndex]  

## <a name="auto-open-devtools-on-every-new-tab"></a>Abrir automaticamente o DevTools em cada nova guia  

Para abrir automaticamente o DevTools em cada nova guia, abra Microsoft Edge da linha de comando e passe o `--auto-open-devtools-for-tabs` sinalizador.  

### [<a name="cmd-windows"></a>CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [<a name="powershell-windows"></a>PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [<a name="bash-macos"></a>bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [<a name="bash-linux"></a>bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## <a name="toggle-the-f12-keyboard-shortcut-on-or-off"></a>Alternar ou desligar o atalho de teclado F12  

Para alterar a configuração de atalho do `F12` teclado que abre o DevTools, conclua as seguintes ações:  

1.  Navegue até `edge://settings/system`.  
1.  Em `Developer Tools` , escolha Abrir o **DevTools** quando a tecla F12 for pressionada para alternar a configuração para off ou on. Alterne a configuração para off para impedir que o `F12` atalho do teclado abrisse o DevTools.  
1.  Depois de definir a alternância como desligada, verifique se `F12` não abre mais o DevTools.  
    
    > [!NOTE]
    > Depois de desligar **Abrir o DevTools**quando a tecla F12 for pressionada, execute uma das seguintes ações para abrir o DevTools.  
    > 
    > *   Selecione `Ctrl` + `Shift` + `I` .  
    > *   Abra o menu contextual \(botão direito do mouse\) > **Inspecionar**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge Atalhos de teclado do DevTools | Microsoft Docs"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/open) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
