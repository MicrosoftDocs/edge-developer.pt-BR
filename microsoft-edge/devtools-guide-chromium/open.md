---
title: Abrir o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 06e547d2d413535a6f14d829d30dc4d7b11ac92b
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843990"
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

# Abrir o Microsoft Edge DevTools  

Há muitas maneiras de abrir o Microsoft Edge DevTools, pois diferentes usuários querem acesso rápido a diferentes partes da interface do usuário do DevTools.  

## Abrir o painel de elementos para inspecionar o DOM ou CSS  

Cada uma das seguintes tarefas permite que você inspecione os estilos ou atributos de um nó DOM.

*   Passe o cursor do mouse sobre o elemento, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.  
*   Pressione `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Option` + `C` \ (MacOS \).  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-right-click-inspect.msft.png" alt-text="A opção * * Inspecione * *" lightbox="./media/bing-right-click-inspect.msft.png":::
   A opção **inspecionar**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Abrir o painel de console  

Cada uma das seguintes tarefas permite abrir o painel de [console][DevToolsConsoleIndex] para exibir mensagens registradas ou executar JavaScript.  

*   Use as etapas a seguir para abrir o painel do [console][DevToolsConsoleIndex] .  
    
    1.  [Abra o devtools](#open-microsoft-edge-devtools).  
    1.  Selecione o painel do [console][DevToolsConsoleIndex] .  

*   Para saltar diretamente para o painel do [console][DevToolsConsoleIndex] , pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Abrir o painel anterior  

Para ir para o painel anterior que você abriu, pressione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  

## Abrir o Microsoft Edge DevTools  

Cada uma das seguintes tarefas permite abrir o DevTools.  

*   Use as etapas a seguir para abrir o Microsoft Edge DevTools.  
    
    1.  Selecione o `...` ícone \ (o ícone **configurações e mais** ).  
    1.  Selecione **mais ferramentas**.  
    1.  Selecione **ferramentas de desenvolvedor**.  
    
*   Para abrir o Microsoft Edge devtools, pressione `F12` ou `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  

:::image type="complex" source="./media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abrir o DevTools a partir do menu principal do Microsoft Edge" lightbox="./media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abrir o DevTools a partir do menu principal do Microsoft Edge  
:::image-end:::  

## Abrir automaticamente o DevTools em cada nova guia  

Para abrir automaticamente o DevTools em cada nova guia, abra o Microsoft Edge na linha de comando e passe o `--auto-open-devtools-for-tabs` sinalizador.  

#### [CMD (Windows)](#tab/cmd-windows/)  

<a id="selenium-tools-install"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

#### [PowerShell (Windows)](#tab/powershell-windows/)  

<a id="selenium-tools-install"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

#### [bash (macOS)](#tab/bash-macos/)  

<a id="selenium-tools-install"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

* * *  

<!-- links -->  

[DevToolsConsoleIndex]: ./console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevtoolsShortcuts]: ./shortcuts.md "Atalhos de teclado do Microsoft Edge DevTools-documentos da Microsoft"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/open) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
