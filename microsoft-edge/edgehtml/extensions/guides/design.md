---
description: Saiba mais sobre os vários aspectos de design e o comportamento da interface do usuário a ser considerado ao criar extensões do Microsoft Edge.
title: Extensões-design
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, JavaScript, design, ícones, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a32223f93baf44d2ca523e92cf9d7584ad9a8333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231853"
---
# <span data-ttu-id="3711b-104">Diretrizes de design para extensões do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3711b-104">Design Guidelines For Microsoft Edge Extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="3711b-105">A página a seguir contém vários aspectos de design e comportamento da interface do usuário a ser considerado ao criar extensões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3711b-105">The following page contains various design aspects and UI behavior to consider when creating Microsoft Edge extensions.</span></span>  

## <span data-ttu-id="3711b-106">Ícones</span><span class="sxs-lookup"><span data-stu-id="3711b-106">Icons</span></span>  

<span data-ttu-id="3711b-107">Você deve criar os ícones da extensão usando um gráfico vetorial.</span><span class="sxs-lookup"><span data-stu-id="3711b-107">You should make the icons of your extension using a vector graphic.</span></span>  <span data-ttu-id="3711b-108">Você deve criar alguns tamanhos diferentes de seu ícone para a extensão e três tamanhos adicionais se quiser empacotar a extensão.</span><span class="sxs-lookup"><span data-stu-id="3711b-108">You must create a few different sizes of your icon for your extension, and three additional sizes if you want to package your extension.</span></span>  <span data-ttu-id="3711b-109">As extensões do Microsoft Edge não dão suporte a ícones. svg.</span><span class="sxs-lookup"><span data-stu-id="3711b-109">Microsoft Edge extensions do not support .svg icons.</span></span>  

<span data-ttu-id="3711b-110">Antes de criar seus ícones de extensão, você deve revisar o guia de [acessibilidade][ExtensionsGuidesAccessibility] para garantir que seus ícones tenham contraste alto o suficiente e fiquem visíveis nos temas claro e escuro do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3711b-110">Before you create your extension icons, you should review the [accessibility][ExtensionsGuidesAccessibility] guide to ensure that your icons have high enough contrast and are visible in both the light and dark themes of Microsoft Edge.</span></span>  

<span data-ttu-id="3711b-111">Embora haja suporte para qualquer formato de imagem WebKit, os ícones. png são recomendados para suporte de transparência.</span><span class="sxs-lookup"><span data-stu-id="3711b-111">While any webkit image format is supported, .png icons are recommended for transparency support.</span></span>  

### <span data-ttu-id="3711b-112">Ícones para sua extensão</span><span class="sxs-lookup"><span data-stu-id="3711b-112">Icons for your extension</span></span>  

<span data-ttu-id="3711b-113">Para a sua extensão, você deve criar um tamanho de ícone para a ação do navegador ou a ação da página e um tamanho de ícone para o painel de **extensões** .</span><span class="sxs-lookup"><span data-stu-id="3711b-113">For your extension, you must create one icon size for the browser action or page action, and one icon size for the **Extensions** pane.</span></span>  <span data-ttu-id="3711b-114">Mais de um tamanho para cada um pode ser fornecido para dar suporte a monitores de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="3711b-114">More than one size for each may be provided to support high resolution displays.</span></span>  

<span data-ttu-id="3711b-115">Uma extensão deve ter um ícone de ação de página ou ação do navegador.</span><span class="sxs-lookup"><span data-stu-id="3711b-115">An extension should have a browser action or page action icon.</span></span>  <span data-ttu-id="3711b-116">Os ícones de ação do navegador e da ação da página podem ser alterados em tempo de execução usando-se o método [BrowserAction. SetIcon][MSDApiBrowseractionSeticon] ou o método [PageAction. SetIcon][MDNApiPageactionSeticon] .</span><span class="sxs-lookup"><span data-stu-id="3711b-116">The browser action and page action icons may be changed at runtime using the [browserAction.setIcon][MSDApiBrowseractionSeticon] method or [pageAction.setIcon][MDNApiPageactionSeticon] method.</span></span>  

#### <span data-ttu-id="3711b-117">Ação do navegador</span><span class="sxs-lookup"><span data-stu-id="3711b-117">Browser action</span></span>  

<span data-ttu-id="3711b-118">Os tamanhos preferenciais dos ícones de ação de página e de ação do navegador são `20px` ,, `25px` `30px` e `40px` .</span><span class="sxs-lookup"><span data-stu-id="3711b-118">The preferred sizes for browser action and page action icons are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="3711b-119">Outros tamanhos compatíveis incluem `19px` , `35px` e `38px` .</span><span class="sxs-lookup"><span data-stu-id="3711b-119">Other supported sizes include `19px`, `35px`, and `38px`.</span></span>  

<span data-ttu-id="3711b-120">Omanifest.jsa seguir [ no trecho de][ExtensionsApisupportManifestkeys] arquivo mostra um ícone de ação de navegador padrão e de alta definição sendo especificado usando a tecla [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="3711b-120">The following [manifest.json][ExtensionsApisupportManifestkeys] file snippet shows a standard and high definition browser action icon being specified using the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="3711b-121">A mesma sintaxe se aplica à chave [page_action][MDNManifestjsonPageAction] .</span><span class="sxs-lookup"><span data-stu-id="3711b-121">The same syntax applies for the [page_action][MDNManifestjsonPageAction] key.</span></span>  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

<span data-ttu-id="3711b-122">Se a ação do navegador tiver sido definida pela extensão, ela aparecerá no menu ações após selecionar **mais (...)** ou à direita da barra de endereços se a opção **Mostrar botão ao lado da barra de endereços** for alternada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3711b-122">If the browser action has been set by the extension, it appears either in the Actions menu after selecting **More(...)**,  or to the right of the address bar if **Show button next to the address bar** has been toggled on by the user.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Ação do navegador no menu Ação":::
         <span data-ttu-id="3711b-124">Ação do navegador no menu Ação</span><span class="sxs-lookup"><span data-stu-id="3711b-124">Browser action in action menu</span></span> :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Ação do navegador":::
         <span data-ttu-id="3711b-126">Ação do navegador</span><span class="sxs-lookup"><span data-stu-id="3711b-126">Browser action</span></span> :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="3711b-127">Ação da página</span><span class="sxs-lookup"><span data-stu-id="3711b-127">Page action</span></span>  

<span data-ttu-id="3711b-128">A chave [page_action][MDNManifestjsonPageAction] tem a mesma sintaxe de manifesto JSON que a tecla [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="3711b-128">The [page_action][MDNManifestjsonPageAction] key has the same JSON manifest syntax as the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="3711b-129">A ação da página também tem os mesmos requisitos de tamanho de ícone da ação do navegador.</span><span class="sxs-lookup"><span data-stu-id="3711b-129">Page action also has the same icon size requirements as browser action.</span></span>  

<span data-ttu-id="3711b-130">Se a ação da página for especificada no [manifest.jsem][ExtensionsApisupportManifestkeys] arquivo, ela aparecerá na barra de endereços sempre que o método [PageAction. show][MDNApiPageactionShow] for usado.</span><span class="sxs-lookup"><span data-stu-id="3711b-130">If page action is specified in the [manifest.json][ExtensionsApisupportManifestkeys] file, it appears within the address bar whenever the [pageAction.show][MDNApiPageactionShow] method is used.</span></span>  

:::image type="complex" source="../media/pageaction.png" alt-text="Ação da página":::
   <span data-ttu-id="3711b-132">Ação da página</span><span class="sxs-lookup"><span data-stu-id="3711b-132">Page action</span></span>
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### <span data-ttu-id="3711b-133">Interface do usuário de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3711b-133">Management UI</span></span>  

<span data-ttu-id="3711b-134">Quando os usuários navegam até o painel extensões indo para o menu **mais (...)** e selecionando **extensões**, um ícone é exibido ao lado do nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="3711b-134">When users navigate to the extensions pane by going to the **More(...)** menu and selecting **Extensions**, an icon is displayed next to the name of the extension.</span></span>  

<span data-ttu-id="3711b-135">Você deve especificar os tamanhos dos ícones a seguir.</span><span class="sxs-lookup"><span data-stu-id="3711b-135">You should specify the following icon sizes.</span></span>  

| <span data-ttu-id="3711b-136">Chave</span><span class="sxs-lookup"><span data-stu-id="3711b-136">Key</span></span> | <span data-ttu-id="3711b-137">Detalhes</span><span class="sxs-lookup"><span data-stu-id="3711b-137">Details</span></span> |  
|:--- |:--- |  
| `48px` | <span data-ttu-id="3711b-138">O ícone de resolução padrão é exibido.</span><span class="sxs-lookup"><span data-stu-id="3711b-138">Icon for standard resolution displays.</span></span> |  
| `128px` | <span data-ttu-id="3711b-139">Ícone de monitores de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="3711b-139">Icon for high resolution displays.</span></span> |  
| `176px` | <span data-ttu-id="3711b-140">Ícone para exibição de resolução ainda melhor.</span><span class="sxs-lookup"><span data-stu-id="3711b-140">Icon for even higher resolution displays.</span></span> |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Interface do usuário de gerenciamento":::
   <span data-ttu-id="3711b-142">Interface do usuário de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3711b-142">Management UI</span></span>
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### <span data-ttu-id="3711b-143">Ícones para empacotamento</span><span class="sxs-lookup"><span data-stu-id="3711b-143">Icons for packaging</span></span>  

<span data-ttu-id="3711b-144">Depois que sua extensão estiver pronta para a embalagem, você deverá ter três tamanhos de ícone adicionais prontos.</span><span class="sxs-lookup"><span data-stu-id="3711b-144">Once your extension is ready for packaging, you must have three additional icon sizes ready.</span></span>  

| <span data-ttu-id="3711b-145">Size</span><span class="sxs-lookup"><span data-stu-id="3711b-145">Size</span></span> | <span data-ttu-id="3711b-146">Detalhes</span><span class="sxs-lookup"><span data-stu-id="3711b-146">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="3711b-147">44px</span><span class="sxs-lookup"><span data-stu-id="3711b-147">44px</span></span> | <span data-ttu-id="3711b-148">Usado na interface do usuário do Windows \(**lista de aplicativos**, aplicativos do sistema **configurações**  \>    \>  **& recursos**\).</span><span class="sxs-lookup"><span data-stu-id="3711b-148">Used in the Windows UI \(**App List**, **Settings** \> **System** \> **Apps & features**\).</span></span> |  
| <span data-ttu-id="3711b-149">50px</span><span class="sxs-lookup"><span data-stu-id="3711b-149">50px</span></span> | <span data-ttu-id="3711b-150">Requisito de empacotamento \(não visível em qualquer lugar \).</span><span class="sxs-lookup"><span data-stu-id="3711b-150">Packaging requirement \(not visible anywhere\).</span></span> |  
| <span data-ttu-id="3711b-151">150px</span><span class="sxs-lookup"><span data-stu-id="3711b-151">150px</span></span> | <span data-ttu-id="3711b-152">Usado como o ícone da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="3711b-152">Used as the icon for the Microsoft Store.</span></span> |  


<span data-ttu-id="3711b-153">Consulte o [Guia de empacotamento manual][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] ou o [Guia de empacotamento do ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] para determinar onde esses ícones são colocados.</span><span class="sxs-lookup"><span data-stu-id="3711b-153">See either the [manual packaging guide][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] or the [ManifoldJS packaging guide][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] to determine where these icons is placed.</span></span>  <span data-ttu-id="3711b-154">Isso depende de qual método de empacotamento você escolher.</span><span class="sxs-lookup"><span data-stu-id="3711b-154">This depends upon which packaging method you choose.</span></span>  

#### <span data-ttu-id="3711b-155">Ícone da Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="3711b-155">Microsoft Store icon</span></span>  

<span data-ttu-id="3711b-156">Se o ícone do 150px para a Microsoft Store tiver um plano de fundo transparente, a cor de destaque do dispositivo do usuário será exibida como a cor da tela de fundo do ícone.</span><span class="sxs-lookup"><span data-stu-id="3711b-156">If the 150px icon for the Microsoft Store has a transparent background, the accent color of the user's device appears as the background color of the icon.</span></span>  

<span data-ttu-id="3711b-157">Por exemplo, se um usuário tiver selecionado rosa como a cor de destaque, o plano de fundo transparente do ícone da loja será exibido como rosa.</span><span class="sxs-lookup"><span data-stu-id="3711b-157">For example, if a user has selected pink as the accent color, the transparent background of your store icon is displayed as pink.</span></span>  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Cor de destaque do Windows":::
          <span data-ttu-id="3711b-159">Cor de destaque do Windows</span><span class="sxs-lookup"><span data-stu-id="3711b-159">Windows accent color</span></span> :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Cor da tela de fundo selecionada automaticamente":::
         <span data-ttu-id="3711b-161">Cor da tela de fundo selecionada automaticamente</span><span class="sxs-lookup"><span data-stu-id="3711b-161">Background color auto selected</span></span> :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

<span data-ttu-id="3711b-162">Se quiser escolher sua própria cor de plano de fundo para a Microsoft Store, você deve torná-la opaca opaca.</span><span class="sxs-lookup"><span data-stu-id="3711b-162">If you want to pick your own background color for your Microsoft Store, you must make the background opaque.</span></span>  

> [!NOTE]
> <span data-ttu-id="3711b-163">No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="3711b-163">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="3711b-164">[Entre em contato conosco][AkaExtensionRequest] com suas solicitações para a Microsoft Store e sua solicitação será considerada para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="3711b-164">[Contact us][AkaExtensionRequest] with your requests for the Microsoft Store, and your request is considered for a future update.</span></span>  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Acessibilidade | Documentos da Microsoft"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Pasta ativos-criando e testando um pacote AppX de extensão do Microsoft Edge | Documentos da Microsoft"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Empacotamento com ManifoldJS-usando ManifoldJS para criar pacotes AppX de extensão | Documentos da Microsoft"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Chaves de manifesto com suporte | Documentos da Microsoft"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Entrar em contato conosco"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "BrowserAction. SetIcon ()-API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "PageAction. SetIcon ()-API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "PageAction. show ()-API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action manifest.jsem | MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action manifest.jsem | MDN"  
