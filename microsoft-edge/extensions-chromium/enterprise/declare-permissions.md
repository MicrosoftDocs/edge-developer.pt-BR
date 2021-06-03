---
description: Saiba como declarar permissões para APIs em seu manifesto
title: Declarar permissões de API em manifestos de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 987279a8072388d3fd47ee8b7cbf5f9bb3c483e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461487"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="declare-api-permissions-in-extension-manifests"></a><span data-ttu-id="8112a-104">Declarar permissões de API em manifestos de extensão</span><span class="sxs-lookup"><span data-stu-id="8112a-104">Declare API permissions in extension manifests</span></span>  

<span data-ttu-id="8112a-105">Para usar a maioria das `chrome.*` APIs, sua extensão deve declarar `permissions` o no manifesto.</span><span class="sxs-lookup"><span data-stu-id="8112a-105">To use most of the `chrome.*` APIs, your extension must declare the `permissions` in the manifest.</span></span>  <span data-ttu-id="8112a-106">Você pode declarar permissões usando uma cadeia de caracteres de permissão da tabela a seguir ou usar um padrão para corresponder a cadeias de caracteres semelhantes.</span><span class="sxs-lookup"><span data-stu-id="8112a-106">You may declare permissions using a permission string from the table that follows, or use a pattern to match similar strings.</span></span>  <span data-ttu-id="8112a-107">As permissões ajudam a restringir sua extensão se ela for comprometida por malware.</span><span class="sxs-lookup"><span data-stu-id="8112a-107">Permissions help to constrain your extension if it gets compromised by malware.</span></span>  <span data-ttu-id="8112a-108">Algumas permissões podem ser exibidas para os usuários antes da instalação da extensão usando Avisos de Permissão.</span><span class="sxs-lookup"><span data-stu-id="8112a-108">Some permissions may display to users before installation of the extension using Permission Warnings.</span></span>  

<span data-ttu-id="8112a-109">Se uma API exigir que você declare permissões no manifesto, revise a documentação dessa API para entender as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="8112a-109">If an API requires you to declare permissions in the manifest, review the documentation for that API to understand the needed permissions.</span></span>  <span data-ttu-id="8112a-110">Por exemplo, Armazenamento página da API de Armazenamento descreve como declarar a `storage` permissão.</span><span class="sxs-lookup"><span data-stu-id="8112a-110">For example, the Storage API page describes how to declare the `storage` permission.</span></span>  

<span data-ttu-id="8112a-111">O trecho de código a seguir descreve como declarar permissões no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="8112a-111">The following code snippet outlines how to declare permissions in the manifest file.</span></span>  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

<span data-ttu-id="8112a-112">A tabela a seguir lista as cadeias de caracteres de permissão disponíveis no momento para usar em seu manifesto e as descrições.</span><span class="sxs-lookup"><span data-stu-id="8112a-112">The following table lists the currently available permission strings to use in your manifest, and the descriptions.</span></span>  

| <span data-ttu-id="8112a-113">Cadeia de caracteres de permissão</span><span class="sxs-lookup"><span data-stu-id="8112a-113">Permission string</span></span> | <span data-ttu-id="8112a-114">Detalhes</span><span class="sxs-lookup"><span data-stu-id="8112a-114">Details</span></span> |  
|:--- |:--- |  
| `activeTab` | <span data-ttu-id="8112a-115">Solicita que a extensão seja concedida permissões de acordo com a `activeTab` especificação.</span><span class="sxs-lookup"><span data-stu-id="8112a-115">Requests that the extension is granted permissions according to the `activeTab` specification.</span></span> |  
| `alarms` | <span data-ttu-id="8112a-116">Fornece acesso de extensão à `chrome.alarms` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-116">Gives your extension access to the `chrome.alarms` API.</span></span> |  
| `background` | <span data-ttu-id="8112a-117">Faz Microsoft Edge iniciar cedo e desligar tarde, para que as extensões possam ter uma vida mais longa.</span><span class="sxs-lookup"><span data-stu-id="8112a-117">Makes Microsoft Edge start up early and shut down late, so that extensions may have a longer life.</span></span>  <span data-ttu-id="8112a-118">Quando qualquer extensão instalada tem permissão, Microsoft Edge é executado de forma invisivelmente assim que o usuário faz logons no computador do usuário e antes que o usuário `background` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8112a-118">When any installed extension has `background` permission, Microsoft Edge runs invisibly as soon as the user logs into the user's computer, and before the user launches Microsoft Edge.</span></span>  <span data-ttu-id="8112a-119">A permissão também faz Microsoft Edge continuar em execução, mesmo após o fechamento da última janela, até que o usuário saia explicitamente `background` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8112a-119">The `background` permission also makes Microsoft Edge continue running, even after its last window is closed, until the user explicitly quits Microsoft Edge.</span></span>  <span data-ttu-id="8112a-120">Essa permissão não afeta extensões que estão desligadas no navegador.</span><span class="sxs-lookup"><span data-stu-id="8112a-120">This permission does not affect extensions that are turned off in the browser.</span></span>  <span data-ttu-id="8112a-121">A `background` permissão normalmente é usada em uma página em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8112a-121">The `background` permission is normally used on a background page.</span></span> |  
| `bookmarks` | <span data-ttu-id="8112a-122">Fornece acesso de extensão à `chrome.bookmarks` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-122">Gives your extension access to the `chrome.bookmarks` API.</span></span> |  
| `browsingData` | <span data-ttu-id="8112a-123">Fornece acesso de extensão à `chrome.browsingData` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-123">Gives your extension access to the `chrome.browsingData` API.</span></span> |  
| `certificateProvider` | <span data-ttu-id="8112a-124">Fornece acesso de extensão à `chrome.certificateProvider` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-124">Gives your extension access to the `chrome.certificateProvider` API.</span></span> |  
| `clipboardRead` | <span data-ttu-id="8112a-125">Obrigatório se a extensão usar `document.execCommand('paste')` .</span><span class="sxs-lookup"><span data-stu-id="8112a-125">Required if the extension uses `document.execCommand('paste')`.</span></span> |  
| `clipboardWrite` | <span data-ttu-id="8112a-126">Indica que a extensão usa `document.execCommand('copy')` ou `document.execCommand('cut')` .</span><span class="sxs-lookup"><span data-stu-id="8112a-126">Indicates the extension uses `document.execCommand('copy')` or `document.execCommand('cut')`.</span></span> |  
| `contentSettings` | <span data-ttu-id="8112a-127">Fornece acesso de extensão à `chrome.contentSettings` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-127">Gives your extension access to the `chrome.contentSettings` API.</span></span> |  
| `contextMenus` | <span data-ttu-id="8112a-128">Fornece acesso de extensão à `chrome.contextMenus` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-128">Gives your extension access to the `chrome.contextMenus` API.</span></span> |  
| `cookies` | <span data-ttu-id="8112a-129">Fornece acesso de extensão à `chrome.cookies` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-129">Gives your extension access to the `chrome.cookies` API.</span></span> |  
| `debugger` | <span data-ttu-id="8112a-130">Fornece acesso de extensão à `chrome.debugger` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-130">Gives your extension access to the `chrome.debugger` API.</span></span> |  
| `declarativeContent` | <span data-ttu-id="8112a-131">Fornece acesso de extensão à `chrome.declarativeContent` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-131">Gives your extension access to the `chrome.declarativeContent` API.</span></span> |  
| `declarativeNetRequest` | <span data-ttu-id="8112a-132">Fornece acesso de extensão à `chrome.declarativeNetRequest` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-132">Gives your extension access to the `chrome.declarativeNetRequest` API.</span></span> |  
| `declarativeNetRequestFeedback` | <span data-ttu-id="8112a-133">Concede o acesso de extensão a eventos e métodos dentro da API, que `chrome.declarativeNetRequest` retorna informações sobre regras declarativas que corresponderam.</span><span class="sxs-lookup"><span data-stu-id="8112a-133">Grants the extension access to events and methods within the `chrome.declarativeNetRequest` API, which returns information on declarative rules matched.</span></span> |  
| `declarativeWebRequest` | <span data-ttu-id="8112a-134">Fornece acesso de extensão à `chrome.declarativeWebRequest` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-134">Gives your extension access to the `chrome.declarativeWebRequest` API.</span></span> |  
| `desktopCapture` | <span data-ttu-id="8112a-135">Fornece acesso de extensão à `chrome.desktopCapture` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-135">Gives your extension access to the `chrome.desktopCapture` API.</span></span> |  
| `documentScan` | <span data-ttu-id="8112a-136">Fornece acesso de extensão à `chrome.documentScan` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-136">Gives your extension access to the `chrome.documentScan` API.</span></span> |  
| `downloads` | <span data-ttu-id="8112a-137">Fornece acesso de extensão à `chrome.downloads` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-137">Gives your extension access to the `chrome.downloads` API.</span></span> |  
| `enterprise.deviceAttributes` | <span data-ttu-id="8112a-138">Fornece acesso de extensão à `chrome.enterprise.deviceAttributes` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-138">Gives your extension access to the `chrome.enterprise.deviceAttributes` API.</span></span> |  
| `enterprise.hardwarePlatform` | <span data-ttu-id="8112a-139">Fornece acesso de extensão à `chrome.enterprise.hardwarePlatform` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-139">Gives your extension access to the `chrome.enterprise.hardwarePlatform` API.</span></span> |  
| `enterprise.networkingAttributes` | <span data-ttu-id="8112a-140">Fornece acesso de extensão à `chrome.enterprise.networkingAttributes` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-140">Gives your extension access to the `chrome.enterprise.networkingAttributes` API.</span></span> |  
| `enterprise.platformKeys` | <span data-ttu-id="8112a-141">Fornece acesso de extensão à `chrome.enterprise.platformKeys` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-141">Gives your extension access to the `chrome.enterprise.platformKeys` API.</span></span> |  
| `experimental` | <span data-ttu-id="8112a-142">Obrigatório se a extensão usar qualquer `chrome.experimental.*` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-142">Required if the extension uses any `chrome.experimental.*` API.</span></span> |  
| `fileBrowserHandler` | <span data-ttu-id="8112a-143">Fornece acesso de extensão à `chrome.fileBrowserHandler` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-143">Gives your extension access to the `chrome.fileBrowserHandler` API.</span></span> |  
| `fileSystemProvider` | <span data-ttu-id="8112a-144">Fornece acesso de extensão à `chrome.fileSystemProvider` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-144">Gives your extension access to the `chrome.fileSystemProvider` API.</span></span> |  
| `fontSettings` | <span data-ttu-id="8112a-145">Fornece acesso de extensão à `chrome.fontSettings` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-145">Gives your extension access to the `chrome.fontSettings` API.</span></span> |  
| `geolocation` | <span data-ttu-id="8112a-146">Permite que a extensão use a API de localização geográfica sem solicitar permissão ao usuário.</span><span class="sxs-lookup"><span data-stu-id="8112a-146">Allows the extension to use the geolocation API without prompting the user for permission.</span></span> |  
| `history` | <span data-ttu-id="8112a-147">Fornece acesso de extensão à `chrome.history` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-147">Gives your extension access to the `chrome.history` API.</span></span> |  
| `identity` | <span data-ttu-id="8112a-148">Fornece acesso de extensão à `chrome.identity` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-148">Gives your extension access to the `chrome.identity` API.</span></span> |  
| `idle` | <span data-ttu-id="8112a-149">Fornece acesso de extensão à `chrome.idle` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-149">Gives your extension access to the `chrome.idle` API.</span></span> |  
| `loginState` | <span data-ttu-id="8112a-150">Fornece acesso de extensão à `chrome.loginState` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-150">Gives your extension access to the `chrome.loginState` API.</span></span> |  
| `management` | <span data-ttu-id="8112a-151">Fornece acesso de extensão à `chrome.management` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-151">Gives your extension access to the `chrome.management` API.</span></span> |  
| `nativeMessaging` | <span data-ttu-id="8112a-152">Fornece acesso de extensão à API de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="8112a-152">Gives your extension access to the native messaging API.</span></span> |  
| `notifications` | <span data-ttu-id="8112a-153">Fornece acesso de extensão à `chrome.notifications` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-153">Gives your extension access to the `chrome.notifications` API.</span></span> |  
| `pageCapture` | <span data-ttu-id="8112a-154">Fornece acesso de extensão à `chrome.pageCapture` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-154">Gives your extension access to the `chrome.pageCapture` API.</span></span> |  
| `platformKeys` | <span data-ttu-id="8112a-155">Fornece acesso de extensão à `chrome.platformKeys` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-155">Gives your extension access to the `chrome.platformKeys` API.</span></span> |  
| `power` | <span data-ttu-id="8112a-156">Fornece acesso de extensão à `chrome.power` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-156">Gives your extension access to the `chrome.power` API.</span></span> |  
| `printerProvider` | <span data-ttu-id="8112a-157">Fornece acesso de extensão à `chrome.printerProvider` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-157">Gives your extension access to the `chrome.printerProvider` API.</span></span> |  
| `printing` | <span data-ttu-id="8112a-158">Fornece acesso de extensão à `chrome.printing` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-158">Gives your extension access to the `chrome.printing` API.</span></span> |  
| `printingMetrics` | <span data-ttu-id="8112a-159">Fornece acesso de extensão à `chrome.printingMetrics` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-159">Gives your extension access to the `chrome.printingMetrics` API.</span></span> |  
| `privacy` | <span data-ttu-id="8112a-160">Fornece acesso de extensão à `chrome.privacy` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-160">Gives your extension access to the `chrome.privacy` API.</span></span> |  
| `processes` | <span data-ttu-id="8112a-161">Fornece acesso de extensão à `chrome.processes` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-161">Gives your extension access to the `chrome.processes` API.</span></span> |  
| `proxy` | <span data-ttu-id="8112a-162">Fornece acesso de extensão à `chrome.proxy` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-162">Gives your extension access to the `chrome.proxy` API.</span></span> |  
| `scripting` | <span data-ttu-id="8112a-163">Fornece acesso de extensão à `chrome.scripting` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-163">Gives your extension access to the `chrome.scripting` API.</span></span> |  
| `search` | <span data-ttu-id="8112a-164">Fornece acesso de extensão à `chrome.search` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-164">Gives your extension access to the `chrome.search` API.</span></span> |  
| `sessions` | <span data-ttu-id="8112a-165">Fornece acesso de extensão à `chrome.sessions` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-165">Gives your extension access to the `chrome.sessions` API.</span></span> |  
| `signedInDevices` | <span data-ttu-id="8112a-166">Fornece acesso de extensão à `chrome.signedInDevices` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-166">Gives your extension access to the `chrome.signedInDevices` API.</span></span> |  
| `storage` | <span data-ttu-id="8112a-167">Fornece acesso de extensão à `chrome.storage` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-167">Gives your extension access to the `chrome.storage` API.</span></span> |  
| `system.cpu` | <span data-ttu-id="8112a-168">Fornece acesso de extensão à `chrome.system.cpu` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-168">Gives your extension access to the `chrome.system.cpu` API.</span></span> |  
| `system.display` | <span data-ttu-id="8112a-169">Fornece acesso de extensão à `chrome.system.display` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-169">Gives your extension access to the `chrome.system.display` API.</span></span> |  
| `system.memory` | <span data-ttu-id="8112a-170">Fornece acesso de extensão à `chrome.system.memory` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-170">Gives your extension access to the `chrome.system.memory` API.</span></span> |  
| `system.storage` | <span data-ttu-id="8112a-171">Fornece acesso de extensão à `chrome.system.storage` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-171">Gives your extension access to the `chrome.system.storage` API.</span></span> |  
| `tabCapture` | <span data-ttu-id="8112a-172">Fornece acesso de extensão à `chrome.tabCapture` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-172">Gives your extension access to the `chrome.tabCapture` API.</span></span> |  
| `tabGroups` | <span data-ttu-id="8112a-173">Fornece acesso de extensão à `chrome.tabGroups` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-173">Gives your extension access to the `chrome.tabGroups` API.</span></span> |  
| `tabs` | <span data-ttu-id="8112a-174">Fornece acesso de extensão a campos privilegiados dos objetos que podem ser usados por `Tab` várias APIs, incluindo `chrome.tabs` e `chrome.windows` .</span><span class="sxs-lookup"><span data-stu-id="8112a-174">Gives your extension access to privileged fields of the `Tab` objects that may be used by several APIs including `chrome.tabs` and `chrome.windows`.</span></span>  <span data-ttu-id="8112a-175">Em muitas circunstâncias, sua extensão não precisa declarar a `tabs` permissão para usar essas APIs.</span><span class="sxs-lookup"><span data-stu-id="8112a-175">In many circumstances, your extension does not need to declare the `tabs` permission to make use of these APIs.</span></span> |  
| `topSites` | <span data-ttu-id="8112a-176">Fornece acesso de extensão à `chrome.topSites` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-176">Gives your extension access to the `chrome.topSites` API.</span></span> |  
| `tts` | <span data-ttu-id="8112a-177">Fornece acesso de extensão à `chrome.tts` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-177">Gives your extension access to the `chrome.tts` API.</span></span> |  
| `ttsEngine` | <span data-ttu-id="8112a-178">Fornece acesso de extensão à `chrome.ttsEngine` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-178">Gives your extension access to the `chrome.ttsEngine` API.</span></span> |  
| `unlimitedStorage` | <span data-ttu-id="8112a-179">Fornece uma cota ilimitada para armazenar dados do lado do cliente, como bancos de dados e arquivos de armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="8112a-179">Provides an unlimited quota for storing client-side data, such as databases and local storage files.</span></span>  <span data-ttu-id="8112a-180">Sem essa permissão, a extensão é limitada a 5 MB de armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="8112a-180">Without this permission, the extension is limited to 5 MB of local storage.</span></span> |  
| `vpnProvider` | <span data-ttu-id="8112a-181">Fornece acesso de extensão à `chrome.vpnProvider` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-181">Gives your extension access to the `chrome.vpnProvider` API.</span></span> |  
| `wallpaper` | <span data-ttu-id="8112a-182">Fornece acesso de extensão à `chrome.wallpaper` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-182">Gives your extension access to the `chrome.wallpaper` API.</span></span> |  
| `webNavigation` | <span data-ttu-id="8112a-183">Fornece acesso de extensão à `chrome.webNavigation` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-183">Gives your extension access to the `chrome.webNavigation` API.</span></span> |  
| `webRequest` | <span data-ttu-id="8112a-184">Fornece acesso de extensão à `chrome.webRequest` API.</span><span class="sxs-lookup"><span data-stu-id="8112a-184">Gives your extension access to the `chrome.webRequest` API.</span></span> |  
| `webRequestBlocking` | <span data-ttu-id="8112a-185">Obrigatório se a extensão usar a `chrome.webRequest` API para bloquear solicitações.</span><span class="sxs-lookup"><span data-stu-id="8112a-185">Required if the extension uses the `chrome.webRequest` API to block requests.</span></span> |  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="8112a-186">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8112a-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8112a-187">A página original é encontrada [aqui](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/).</span><span class="sxs-lookup"><span data-stu-id="8112a-187">The original page is found [here](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8112a-189">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8112a-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
