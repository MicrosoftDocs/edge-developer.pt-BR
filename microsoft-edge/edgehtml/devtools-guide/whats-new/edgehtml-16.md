---
description: Recursos adicionados ao Microsoft Edge DevTools na atualização do Windows 10 para criadores de outono (EdgeHTML 16)
title: DevTools no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, edgehtml 16
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2d24b6851e843f491e470b18ccc18d559ed5533d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231326"
---
# <span data-ttu-id="877de-104">DevTools na atualização do Windows 10 para criadores de outono (EdgeHTML 16)</span><span class="sxs-lookup"><span data-stu-id="877de-104">DevTools in the Windows 10 Fall Creators Update (EdgeHTML 16)</span></span>

<span data-ttu-id="877de-105">Com este lançamento, começamos um grande esforço de refatoração de DevTools para melhorar a robustez e o desempenho, além de adicionar um monte de novos recursos que você pode começar a usar hoje mesmo!</span><span class="sxs-lookup"><span data-stu-id="877de-105">With this release we started a major DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today!</span></span> 

<span data-ttu-id="877de-106">Estes são os recursos do Microsoft Edge DevTools fornecidos com a [atualização do Windows 10 para criadores de outono](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span><span class="sxs-lookup"><span data-stu-id="877de-106">Here are the Microsoft Edge DevTools features that shipped with the [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span></span>

## <span data-ttu-id="877de-107">Ouvintes de eventos ancestrais</span><span class="sxs-lookup"><span data-stu-id="877de-107">Ancestor event listeners</span></span> 

<span data-ttu-id="877de-108">O painel **eventos** agora adiciona a opção para exibir ouvintes de eventos registrados em qualquer ancestral do elemento atualmente selecionado (no painel **elementos** ), além daqueles do elemento em si.</span><span class="sxs-lookup"><span data-stu-id="877de-108">The **Events** pane now adds the option to view event listeners registered on any ancestor of the currently selected element (in the **Elements** panel), in addition to those on the element itself.</span></span> <span data-ttu-id="877de-109">Além disso, você agora pode agrupar a exibição ouvinte de eventos por *evento* ou *elemento*.</span><span class="sxs-lookup"><span data-stu-id="877de-109">Additionally, you can now group the event listener display by either *Event* or *Element*.</span></span> 

![Painel de inspeção do ouvinte de eventos](../media/elements_ancestor_events.png)

## <span data-ttu-id="877de-111">Pontos de interrupção de mutação DOM</span><span class="sxs-lookup"><span data-stu-id="877de-111">DOM mutation breakpoints</span></span>

<span data-ttu-id="877de-112">Agora você pode definir pontos de interrupção de mutação DOM para invadir o depurador sempre que um nó de elemento selecionado é alterado.</span><span class="sxs-lookup"><span data-stu-id="877de-112">You can now set DOM mutation breakpoints to break into the Debugger whenever a selected element node changes.</span></span> <span data-ttu-id="877de-113">No painel **elementos** , clique com o botão RT em qualquer elemento na exibição de árvore DOM e selecione um ou mais dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="877de-113">From the **Elements** panel, rt-click on any element in the DOM tree view and select one or more of the following:</span></span>

 - <span data-ttu-id="877de-114">Quebra no nó removida</span><span class="sxs-lookup"><span data-stu-id="877de-114">Break on Node removed</span></span>
 - <span data-ttu-id="877de-115">Quebra na subárvore modificada</span><span class="sxs-lookup"><span data-stu-id="877de-115">Break on Subtree modified</span></span>
 - <span data-ttu-id="877de-116">Quebra no atributo modificado</span><span class="sxs-lookup"><span data-stu-id="877de-116">Break on Attribute modified</span></span>

<span data-ttu-id="877de-117">Você pode gerenciar seus pontos de interrupção de mutação do painel **pontos de interrupção do dom** nos painéis **elementos** ou **depurador** .</span><span class="sxs-lookup"><span data-stu-id="877de-117">You can manage your mutation breakpoints from the **DOM breakpoints** pane in the **Elements** or **Debugger** panels.</span></span>

![Painel pontos de interrupção DOM](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="877de-119">Suporte a CSS at-Rule</span><span class="sxs-lookup"><span data-stu-id="877de-119">CSS at-rule support</span></span>

<span data-ttu-id="877de-120">As regras CSS "at" (@) agora são representadas entre outras declarações de regra CSS no painel **estilos** , incluindo regras de animação `@keyframes` (atualmente limitadas a somente leitura), `@supports` consultas de recursos e `@media` consultas.</span><span class="sxs-lookup"><span data-stu-id="877de-120">CSS "at" (@) rules are now represented among other CSS rule declarations on the **Styles** pane, including animation `@keyframes` rules (currently limited to read-only), `@supports` feature queries, and `@media` queries.</span></span>

![Inspeção em regras CSS no painel estilo DevTools](../media/elements_at_rules.png)

## <span data-ttu-id="877de-122">Painel fontes CSS</span><span class="sxs-lookup"><span data-stu-id="877de-122">CSS fonts pane</span></span>

<span data-ttu-id="877de-123">`@font-face`Agora, as regras CSS têm o próprio painel **fontes** dedicadas que exibe onde a fonte é carregada (*local* ou *rede*) e quantos caracteres estão usando.</span><span class="sxs-lookup"><span data-stu-id="877de-123">CSS `@font-face` rules now have their own dedicated **Fonts** pane that displays where the font is loaded from (*Local* or *Network*) and how many characters are using it.</span></span> <span data-ttu-id="877de-124">Se uma fonte for carregada da rede, o DevTools exibirá a regra que a importada juntamente com o seu alias e tipo de fonte.</span><span class="sxs-lookup"><span data-stu-id="877de-124">If a font is loaded from the network,  DevTools will display the rule that imported it along with its alias and font type.</span></span>

![Informações de fonte CSS](../media/elements_fonts.png)

## <span data-ttu-id="877de-126">Suporte a polielemento CSS</span><span class="sxs-lookup"><span data-stu-id="877de-126">CSS pseudo-element support</span></span>

<span data-ttu-id="877de-127">Agora, o painel **estilos** agrupa os pseudoelementos em seus próprios títulos e não exibe mais o conteúdo deles como riscado.</span><span class="sxs-lookup"><span data-stu-id="877de-127">The **Styles** pane now groups pseudo-elements under their own headings and no longer displays their content as crossed out.</span></span>

**<span data-ttu-id="877de-128">Antes:</span><span class="sxs-lookup"><span data-stu-id="877de-128">Before:</span></span>**
<br>
![O conteúdo gerado foi anteriormente riscado](../media/gc_before.png)

**<span data-ttu-id="877de-130">Depois:</span><span class="sxs-lookup"><span data-stu-id="877de-130">After:</span></span>**
<br>
![O conteúdo gerado não é mais exibido com um tachado](../media/gc_after.png)

## <span data-ttu-id="877de-132">Melhorias no console</span><span class="sxs-lookup"><span data-stu-id="877de-132">Console improvements</span></span>

<span data-ttu-id="877de-133">O painel de **console** tem uma revisão de UX para melhor usabilidade e uma experiência de IntelliSense mais rápida e mais rica.</span><span class="sxs-lookup"><span data-stu-id="877de-133">The **Console** panel got a UX overhaul for improved usability and a faster, richer Intellisense experience.</span></span>

<span data-ttu-id="877de-134">**Antes:** 
![ Console anterior</span><span class="sxs-lookup"><span data-stu-id="877de-134">**Before:**
![Previous console</span></span>](../media/console_old.png)

<span data-ttu-id="877de-135">**Após:** 
![ Novo console</span><span class="sxs-lookup"><span data-stu-id="877de-135">**After:**
![New console</span></span>](../media/console_new.png)

<span data-ttu-id="877de-136">Também adicionamos estes aprimoramentos:</span><span class="sxs-lookup"><span data-stu-id="877de-136">We also added these improvements:</span></span>

 -  <span data-ttu-id="877de-137">Use `Shift + Enter` para adicionar uma linha adicional a um comando antes de executá-lo `Enter` .</span><span class="sxs-lookup"><span data-stu-id="877de-137">Use `Shift + Enter` to add an additional line to a command before executing it with `Enter`.</span></span> <span data-ttu-id="877de-138">(Antigamente, houve uma *mudança para o botão de alternância de várias linhas/modo de linha única* .)</span><span class="sxs-lookup"><span data-stu-id="877de-138">(Formerly there was a *Switch to multiline/single-line mode* toggle button.)</span></span>

 - <span data-ttu-id="877de-139">Há suporte para as seguintes novas APIs:</span><span class="sxs-lookup"><span data-stu-id="877de-139">The following new APIs are supported:</span></span>
    - <span data-ttu-id="877de-140">método [ **console. Table (**_objeto_*_)_* ](../console/console-api.md#organizing-log-output)</span><span class="sxs-lookup"><span data-stu-id="877de-140">[**console.table(**_object_*_)_*](../console/console-api.md#organizing-log-output) method</span></span>
    - <span data-ttu-id="877de-141">comando [ **getEventListeners (**_objeto_*_)_* ](../console/command-line.md#event-listeners)</span><span class="sxs-lookup"><span data-stu-id="877de-141">[**getEventListeners(**_object_*_)_*](../console/command-line.md#event-listeners) command</span></span>
    - <span data-ttu-id="877de-142">comando [ **Keys (**_objeto_*_)_* ](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="877de-142">[**keys(**_object_*_)_*](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="877de-143">comando [ **valores (**_objeto_*_)_* ](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="877de-143">[**values(**_object_*_)_*](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="877de-144">seletor [ **de $x (**_expressão XPath_*_)_* ](../console/command-line.md#dom-selectors)</span><span class="sxs-lookup"><span data-stu-id="877de-144">[**$x(**_xpath expression_*_)_*](../console/command-line.md#dom-selectors) selector</span></span>

 - <span data-ttu-id="877de-145">Agora há suporte para o parâmetro de formatação [**% c ()**](../console/console-api.md#logging-custom-messages)</span><span class="sxs-lookup"><span data-stu-id="877de-145">The [**%c()**](../console/console-api.md#logging-custom-messages) formatting parameter is now supported</span></span>

## <span data-ttu-id="877de-146">Aprimoramentos de depuração</span><span class="sxs-lookup"><span data-stu-id="877de-146">Debugging improvements</span></span>

<span data-ttu-id="877de-147">Além de um conjunto de novos recursos para a depuração dos [funcionários e do cache do serviço PWA](#progressive-web-app-debugging), o depurador adicionou estes recursos:</span><span class="sxs-lookup"><span data-stu-id="877de-147">In addition to a suite of new features for debugging your [PWA service workers and cache](#progressive-web-app-debugging), the Debugger added these features:</span></span>

### <span data-ttu-id="877de-148">Depuração consolidada para recursos compartilhados</span><span class="sxs-lookup"><span data-stu-id="877de-148">Consolidated debugging for shared resources</span></span>

<span data-ttu-id="877de-149">Mesmo quando um recurso, como um arquivo carregado da CDN, é referenciado várias vezes em todo o seu código, o DevTools agora fornecerá uma única instância de depuração para esse arquivo em que você pode, em seguida, definir pontos de interrupção comuns que serão atingidos independentemente de onde o arquivo for referenciado.</span><span class="sxs-lookup"><span data-stu-id="877de-149">Even when a resource, such as a file loaded from CDN, is referenced multiple times throughout your code,  DevTools will now provide a single debugging instance for that file where you can then set common breakpoints which will be hit regardless of where that file is referenced.</span></span> <span data-ttu-id="877de-150">(Anteriormente, cada referência de script foi considerada um recurso exclusivo que seria mapeado para um conjunto separado de pontos de interrupção.)</span><span class="sxs-lookup"><span data-stu-id="877de-150">(Previously each script reference was considered a unique resource would map to a separate set of breakpoints.)</span></span>

### <span data-ttu-id="877de-151">Editar em tempo real JavaScript com o *Editing-on-Idle*</span><span class="sxs-lookup"><span data-stu-id="877de-151">Live edit JavaScript with *Edit-on-idle*</span></span>

<span data-ttu-id="877de-152">Agora você pode editar o JavaScript ao vivo durante uma sessão de depuração.</span><span class="sxs-lookup"><span data-stu-id="877de-152">You can now edit your JavaScript live during a debugging session.</span></span> <span data-ttu-id="877de-153">Este recurso estava experimentomente disponível (atrás de um sinalizador) na versão [anterior](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) e agora é um recurso permanente.</span><span class="sxs-lookup"><span data-stu-id="877de-153">This feature was experimentally available (behind a flag) in the [previous](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) release and now its a permanent feature.</span></span> <span data-ttu-id="877de-154">Basta selecionar qualquer arquivo de script no painel **depurador** , editar e, em seguida, clicar em **salvar** (ou `Ctrl+S` ) para testar suas alterações na próxima vez que a seção de código for executada.</span><span class="sxs-lookup"><span data-stu-id="877de-154">Simply select any script file from the **Debugger** panel, edit, then click **Save** (or `Ctrl+S`) to test your changes next time that section of code runs.</span></span> 

![O depurador permite editar script ao vivo e comparar as alterações](../media/debugger_edit_buttons.png) 

<span data-ttu-id="877de-156">Clique no botão **comparar documento com o original** para exibir a comparação do que você alterou.</span><span class="sxs-lookup"><span data-stu-id="877de-156">Click the **Compare document to original** button to view the diff of what you changed.</span></span>

![Modo de exibição diff do código editado no depurador](../media/debugger_edit_code.png) 

<span data-ttu-id="877de-158">Lembre-se das seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="877de-158">Please be aware of the following constraints:</span></span>

- <span data-ttu-id="877de-159">A edição de script funciona apenas em arquivos *. js* externos (e não inseridos `<script>` em *. html*)</span><span class="sxs-lookup"><span data-stu-id="877de-159">Script editing only works in external *.js* files (and not embedded `<script>` within *.html*)</span></span>
- <span data-ttu-id="877de-160">As edições são salvas na memória e liberadas quando o documento é recarregado, portanto, você não poderá executar edições dentro de um `DOMContentLoaded` manipulador, por exemplo</span><span class="sxs-lookup"><span data-stu-id="877de-160">Edits are saved in memory and flushed when the document is reloaded, thus you won’t be able to run edits inside a `DOMContentLoaded` handler, for example</span></span>
- <span data-ttu-id="877de-161">No momento, não há nenhuma maneira (como a opção **salvar como** ) para salvar suas edições em disco a partir do devtools</span><span class="sxs-lookup"><span data-stu-id="877de-161">Currently there’s no way (such as a **Save As** option) to save your edits to disk from  DevTools</span></span>

## <span data-ttu-id="877de-162">Atalhos</span><span class="sxs-lookup"><span data-stu-id="877de-162">Shortcuts</span></span>

<span data-ttu-id="877de-163">Agora você pode iniciar o DevTools no último painel exibido ( `Ctrl+Shift+I` ) ou diretamente ao console ( `Ctrl+Shift+J` ) da mesma forma que faria em outros principais navegadores.</span><span class="sxs-lookup"><span data-stu-id="877de-163">You can now launch DevTools to the last viewed panel (`Ctrl+Shift+I`) or directly to the Console (`Ctrl+Shift+J`) just like you would on other major browsers.</span></span>

## <span data-ttu-id="877de-164">Depuração de aplicativo Web progressivo</span><span class="sxs-lookup"><span data-stu-id="877de-164">Progressive Web App debugging</span></span>

<span data-ttu-id="877de-165">Teste o suporte experimental para aplicativos Web progressivos (PWAs) no Microsoft Edge e no DevTools selecionando a opção **habilitar trabalhos de serviço** a partir de `about:flags` (e reiniciar o Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="877de-165">Test out the experimental support for Progressive Web Apps (PWAs) in Microsoft Edge and  DevTools by selecting the **Enable service workers** option from `about:flags` (and restarting Microsoft Edge).</span></span> <span data-ttu-id="877de-166">Se um site usa funcionários de **serviço** e/ou a API de **cache** , as entradas no painel do **depurador** serão preenchidas para cada origem, de forma semelhante à forma como o armazenamento da Web e a inspeção de cookies funcionam.</span><span class="sxs-lookup"><span data-stu-id="877de-166">If a site makes use of **Service Workers** and/or the **Cache** API,  will populate entries in the **Debugger** panel for each origin, similar to how web storage and cookie inspection work.</span></span>

<span data-ttu-id="877de-167">Clicar em uma entrada de trabalho específica do serviço abrirá a **visão geral do trabalho do serviço**, onde você pode gerenciar o registro de trabalho do serviço para o escopo fornecido e forçar uma notificação por push de teste.</span><span class="sxs-lookup"><span data-stu-id="877de-167">Clicking on a specific service worker entry will open up the **Service Worker Overview**, where you can manage the service worker registration for the given scope and force a test push notification.</span></span> <span data-ttu-id="877de-168">Você também pode **parar** / de**Iniciar** trabalhadores individuais do serviço e **inspecioná** -los em uma janela separada do depurador:</span><span class="sxs-lookup"><span data-stu-id="877de-168">You can also **Stop**/**Start** individual service workers and **Inspect** them from a separate debugger window:</span></span>

![Painel Visão geral do trabalhador do serviço](../media/debugger_sw_overview.png)

<span data-ttu-id="877de-170">Observe o seguinte sobre a depuração de trabalho do serviço:</span><span class="sxs-lookup"><span data-stu-id="877de-170">Please note the following about service worker debugging:</span></span>

 - <span data-ttu-id="877de-171">A depuração de um trabalhador de serviço iniciará uma nova instância do DevTools separada das ferramentas da página, pois os trabalhadores do serviço podem ser compartilhados entre várias guias.</span><span class="sxs-lookup"><span data-stu-id="877de-171">Debugging a service worker will launch a new instance of the DevTools separate from the page's tools because service workers can be shared across multiple tabs.</span></span> 
 - <span data-ttu-id="877de-172">Os painéis de [elementos](../elements.md) e [emulação](../emulation.md) estão ausentes do depurador de trabalho do serviço, pois os trabalhadores do serviço são executados em segundo plano e não controlam diretamente o front-end do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="877de-172">The [Elements](../elements.md) and [Emulation](../emulation.md) panels are absent from the service worker debugger, given that service workers run in the background and do not directly control the front-end of your app.</span></span>
 - <span data-ttu-id="877de-173">Atualmente, o tráfego de rede para um trabalhador de serviço é reportado apenas da instância de depuração DevTools para esse trabalhador, e não da instância central da própria página.</span><span class="sxs-lookup"><span data-stu-id="877de-173">Currently network traffic for a service worker is only reported from the DevTools debugging instance for that worker, and not from the central instance for the page itself.</span></span>

<span data-ttu-id="877de-174">Clicar em uma entrada de cache específica abrirá o Gerenciador de **cache** , onde você pode inspecionar e, opcionalmente, excluir entradas de cache (pares de*solicitação* e *resposta* de chave/valor).</span><span class="sxs-lookup"><span data-stu-id="877de-174">Clicking on a specific cache entry will open up the **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs).</span></span>
