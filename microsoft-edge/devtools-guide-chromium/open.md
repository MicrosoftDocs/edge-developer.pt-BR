---
title: Abrir o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601884"
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

Quando você quiser inspecionar os estilos ou atributos de um nó DOM, clique com o botão direito do mouse no elemento e selecione **inspecionar**.  

> ##### Figura 1  
> A opção **inspecionar**  
> ![A opção inspecionar][ImageInspectOption]  

Ou pressione `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Option` + `C` \ (MacOS \).  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## Abrir o painel de console para ver as mensagens registradas ou executar JavaScript   

Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para saltar diretamente para o painel do **console** .  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## Abrir o último painel que você abriu   

Pressione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  

## Abrir o DevTools a partir do menu principal do Microsoft Edge  

Clique em **configurações e mais \ (Alt + F \)** `...` e selecione **mais**ferramentas de  >  **desenvolvedor**ferramentas.  

> ##### Figura 2  
> Abrindo o DevTools a partir do menu principal do Microsoft Edge  
> ![Abrindo o DevTools a partir do menu principal do Microsoft Edge][ImageOpenFromMain]  

## Abrir automaticamente o DevTools em cada nova guia   

Abra o Microsoft Edge na linha de comando e passe o `--auto-open-devtools-for-tabs` sinalizador.  

Windows \ (CMD \):  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

Windows \ (PowerShell \):  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

MacOS  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Figura 1: a opção inspecionar"  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Figura 2: abrindo o DevTools a partir do menu principal do Microsoft Edge"  

<!-- links -->  

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
