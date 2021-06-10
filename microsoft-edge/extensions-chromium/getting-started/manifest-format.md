---
description: Saiba mais sobre o formato do arquivo de manifesto em um pacote de extensão.
title: Formato de arquivo de manifesto
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões, mv2, mv3, manifesto
ms.openlocfilehash: ac2358f8927a762dcef98f9e10cc9f343d8a93f1
ms.sourcegitcommit: afeeeea9fccc3c4c096d7d44c401f4fe87ea2cd7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599425"
---
# <a name="manifest-file-format-for-extensions"></a><span data-ttu-id="aafd4-104">Formato de arquivo de manifesto para extensões</span><span class="sxs-lookup"><span data-stu-id="aafd4-104">Manifest file format for extensions</span></span>

<span data-ttu-id="aafd4-105">Cada extensão para Microsoft Edge (Chromium) tem um arquivo de manifesto formatado JSON, chamado `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="aafd4-105">Every extension for Microsoft Edge (Chromium) has a JSON-formatted manifest file, named `manifest.json`.</span></span>  <span data-ttu-id="aafd4-106">O arquivo de manifesto é o plano de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="aafd4-106">The manifest file is the blueprint of your extension.</span></span>  <span data-ttu-id="aafd4-107">O arquivo de manifesto inclui informações como:</span><span class="sxs-lookup"><span data-stu-id="aafd4-107">The manifest file includes information such as:</span></span>

*  <span data-ttu-id="aafd4-108">O número da versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="aafd4-108">The version number of the extension.</span></span>
*  <span data-ttu-id="aafd4-109">O título da extensão.</span><span class="sxs-lookup"><span data-stu-id="aafd4-109">The title of the extension.</span></span>
*  <span data-ttu-id="aafd4-110">As permissões necessárias para a extensão ser executado.</span><span class="sxs-lookup"><span data-stu-id="aafd4-110">The permissions that are needed for the extension to run.</span></span>

<span data-ttu-id="aafd4-111">O formato para `manifest.json` extensões está mudando do Manifesto V2 para o Manifesto V3.</span><span class="sxs-lookup"><span data-stu-id="aafd4-111">The format for `manifest.json` for extensions is moving from Manifest V2 to Manifest V3.</span></span>  <span data-ttu-id="aafd4-112">Ambos os formatos são mostrados aqui.</span><span class="sxs-lookup"><span data-stu-id="aafd4-112">Both formats are shown here.</span></span>  <span data-ttu-id="aafd4-113">Para migrar uma extensão de Manifesto V2 para Manifesto V3, navegue até Preparar para atualizar suas extensões do [Manifesto v2 para v3][MigrateToMV3].</span><span class="sxs-lookup"><span data-stu-id="aafd4-113">To migrate a Manifest V2 extension to Manifest V3, navigate to [Prepare to update your extensions from Manifest v2 to v3][MigrateToMV3].</span></span>


## <a name="format-of-manifestjson-for-extensions-using-manifest-v3"></a><span data-ttu-id="aafd4-114">Formato de manifest\.jspara extensões usando o Manifesto V3</span><span class="sxs-lookup"><span data-stu-id="aafd4-114">Format of manifest\.json for extensions using Manifest V3</span></span>

<span data-ttu-id="aafd4-115">O código a seguir mostra os campos com suporte para `manifest.json` extensões, para um pacote De manifesto V3.</span><span class="sxs-lookup"><span data-stu-id="aafd4-115">The following code shows the fields that are supported in `manifest.json` for extensions, for a Manifest V3 package.</span></span>

<span data-ttu-id="aafd4-116">Para obter informações de referência sobre cada campo, navegue até Manifesto formato de arquivo [(V3)][ChromeDeveloperDocsExtensionsMv3Manifest] e selecione os links nos campos.</span><span class="sxs-lookup"><span data-stu-id="aafd4-116">For reference information about each field, navigate to [Manifest file format (V3)][ChromeDeveloperDocsExtensionsMv3Manifest] and then select the links on the fields.</span></span>

```json
{
  // Required
  "manifest_version": 3,
  "name": "My V3 Extension",
  "version": "versionString",

  // Recommended
  "action": {...},
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `service_ worker` is required
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": [...],
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": "aString",
  "web_accessible_resources": [...]
}
```

## <a name="format-of-manifestjson-for-extensions-using-manifest-v2"></a><span data-ttu-id="aafd4-117">Formato de manifest\.jspara extensões usando Manifesto V2</span><span class="sxs-lookup"><span data-stu-id="aafd4-117">Format of manifest\.json for extensions using Manifest V2</span></span>

<span data-ttu-id="aafd4-118">O código a seguir mostra os campos com suporte para `manifest.json` extensões, para um pacote V2 de manifesto.</span><span class="sxs-lookup"><span data-stu-id="aafd4-118">The following code shows the fields that are supported in `manifest.json` for extensions, for a Manifest V2 package.</span></span>

<span data-ttu-id="aafd4-119">Para obter informações de referência sobre cada campo, navegue até Manifesto formato de arquivo [(V2)][ChromeDeveloperDocsExtensionsMv2Manifest] e selecione os links nos campos.</span><span class="sxs-lookup"><span data-stu-id="aafd4-119">For reference information about each field, navigate to [Manifest file format (V2)][ChromeDeveloperDocsExtensionsMv2Manifest] and then select the links on the fields.</span></span>

```json
{
  // Required
  "manifest_version": 2,
  "name": "My V2 Extension",
  "version": "versionString",

  // Recommended
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Pick one or none
  "browser_action": {...},
  "page_action": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `persistent` is recommended
    "persistent": false,
    // If `background` is included, `service_worker` is optional
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": ...,
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": ...,
  "web_accessible_resources": [...]
}
```

> [!NOTE]
> <span data-ttu-id="aafd4-120">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aafd4-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aafd4-121">A página original é encontrada [aqui](https://developer.chrome.com/docs/extensions/mv3/manifest/).</span><span class="sxs-lookup"><span data-stu-id="aafd4-121">The original page is found [here](https://developer.chrome.com/docs/extensions/mv3/manifest/).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aafd4-123">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aafd4-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies


<!-- links -->
[MigrateToMV3]: ../developer-guide/migrate-your-extension-from-manifest-v2-to-v3.md "Prepare-se para atualizar suas extensões do Manifesto v2 para o v3 | Microsoft Docs"

[ChromeDeveloperDocsExtensionsMv3Manifest]: https://developer.chrome.com/docs/extensions/mv3/manifest "Formato de arquivo de manifesto (V3) | Desenvolvedores do Chrome"
[ChromeDeveloperDocsExtensionsMv2Manifest]: https://developer.chrome.com/docs/extensions/mv2/manifest "Formato de arquivo de manifesto (V2) | Desenvolvedores do Chrome"
