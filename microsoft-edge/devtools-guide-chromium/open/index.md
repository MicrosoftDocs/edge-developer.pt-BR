---
description: Todas as maneiras de abrir o Microsoft Edge DevTools.
title: Abrir o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d21ebbf0b84be757c1b7a69d36b3bd3cc8403c6d
ms.sourcegitcommit: 77c8f42cc84600c2b853b15aaaecf0749b74bb01
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/22/2020
ms.locfileid: "11238214"
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

*   Passe o cursor do mouse sobre o elemento, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
*   Selecione `Control` + `Shift` + `C` \ (Windows, Linux \) ou `Command` + `Option` + `C` \ (MacOS \).  Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-right-click-inspect.msft.png" alt-text="A opção inspecionar" lightbox="../media/bing-right-click-inspect.msft.png":::
   A opção **inspecionar**  
:::image-end:::  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Abrir o painel de console  

Cada uma das seguintes tarefas permite abrir o painel de [console][DevtoolsConsoleIndex] para exibir mensagens registradas ou executar JavaScript.  

*   Use as etapas a seguir para abrir o painel do [console][DevtoolsConsoleIndex] .  
    
    1.  [Abra o devtools](#open-microsoft-edge-devtools).  
    1.  Selecione o painel do [console][DevtoolsConsoleIndex] .  

*   Para saltar diretamente para o painel do [console][DevtoolsConsoleIndex] , selecione `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \).  Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevtoolsShortcutsIndex].  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Abrir o painel anterior  

Para ir para o painel anterior que você abriu, selecione `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).  Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevtoolsShortcutsIndex].  

## Abrir o Microsoft Edge DevTools  

Para abrir o DevTools, use uma das opções a seguir.  

*   Use a interface do usuário do Microsoft Edge.  
    
    1.  Selecione o ícone **configurações e mais** \ ( `...` \).  
    1.  Escolha **mais ferramentas**.  
    1.  Escolha **ferramentas de desenvolvedor**.  
    
*   Use o teclado.  
    *   Selecione `F12` ou `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).  

Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevtoolsShortcutsIndex].  

:::image type="complex" source="../media/bing-customize-more-tools-developer-tools-transparent.msft.png" alt-text="Abrir o DevTools a partir do menu principal do Microsoft Edge" lightbox="../media/bing-customize-more-tools-developer-tools-transparent.msft.png":::
   Abrir o DevTools a partir do menu principal do Microsoft Edge  
:::image-end:::  

## Abrir automaticamente o DevTools em cada nova guia  

Para abrir automaticamente o DevTools em cada nova guia, abra o Microsoft Edge na linha de comando e passe o `--auto-open-devtools-for-tabs` sinalizador.  

### [CMD (Windows)](#tab/cmd-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

### [PowerShell (Windows)](#tab/powershell-Windows/)  

<a id="auto-open-devtools-command-line"></a>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

### [bash (macOS)](#tab/bash-macos/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

### [bash (Linux)](#tab/bash-linux/)  

<a id="auto-open-devtools-command-line"></a>  

```bash
microsoft-edge-dev --auto-open-devtools-for-tabs
```  

* * *  

## Ativar ou desativar o atalho do teclado F12  

Para alterar a `F12` configuração do atalho de teclado que abre o devtools, complete as seguintes ações.  

1.  Escolha o ícone **configurações e mais** \ ( `...` \) ícone > **configurações**.  
1.  Em **configurações de pesquisa**, digite `Developer Tools` .  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-on.msft.png" alt-text="A configuração abrir o DevTools quando a tecla F12 estiver pressionada" lightbox="../media/settings-developer-tools-f12-on.msft.png":::
       A configuração **abrir o devtools quando a tecla F12 estiver pressionada**  
    :::image-end:::  
    
1.  Escolha **abrir o devtools quando a tecla F12 estiver pressionada** para alternar a configuração para desativado \ (ou em \).  Alterne a configuração para desativar para impedir que o `F12` atalho de teclado Abra o devtools.  
    
    :::image type="complex" source="../media/settings-developer-tools-f12-off.msft.png" alt-text="A configuração abrir o DevTools quando a tecla F12 está pressionada está desativada" lightbox="../media/settings-developer-tools-f12-off.msft.png":::
       A configuração **abrir o devtools quando a tecla F12 está pressionada** está desativada  
    :::image-end:::  
    
1.  Depois de definir o botão de alternância como desativado, selecione `F12` para confirmar que o devtools não está mais aberto.  
    
    > [!NOTE]
    > Depois de desativar a configuração **abrir o devtools quando a tecla F12 estiver pressionada** , para abrir o devtools, execute uma das seguintes ações.  
    > 
    > *   Selecione `Ctrl` + `Shift` + `I` .  
    > *   Abra o menu contextual \ (clique com o botão direito do mouse \) > **Inspecione**.  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/open) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
