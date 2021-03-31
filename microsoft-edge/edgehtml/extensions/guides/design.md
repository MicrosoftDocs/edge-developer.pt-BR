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
# Diretrizes de design para extensões do Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

A página a seguir contém vários aspectos de design e comportamento da interface do usuário a ser considerado ao criar extensões do Microsoft Edge.  

## Ícones  

Você deve criar os ícones da extensão usando um gráfico vetorial.  Você deve criar alguns tamanhos diferentes de seu ícone para a extensão e três tamanhos adicionais se quiser empacotar a extensão.  As extensões do Microsoft Edge não dão suporte a ícones. svg.  

Antes de criar seus ícones de extensão, você deve revisar o guia de [acessibilidade][ExtensionsGuidesAccessibility] para garantir que seus ícones tenham contraste alto o suficiente e fiquem visíveis nos temas claro e escuro do Microsoft Edge.  

Embora haja suporte para qualquer formato de imagem WebKit, os ícones. png são recomendados para suporte de transparência.  

### Ícones para sua extensão  

Para a sua extensão, você deve criar um tamanho de ícone para a ação do navegador ou a ação da página e um tamanho de ícone para o painel de **extensões** .  Mais de um tamanho para cada um pode ser fornecido para dar suporte a monitores de alta resolução.  

Uma extensão deve ter um ícone de ação de página ou ação do navegador.  Os ícones de ação do navegador e da ação da página podem ser alterados em tempo de execução usando-se o método [BrowserAction. SetIcon][MSDApiBrowseractionSeticon] ou o método [PageAction. SetIcon][MDNApiPageactionSeticon] .  

#### Ação do navegador  

Os tamanhos preferenciais dos ícones de ação de página e de ação do navegador são `20px` ,, `25px` `30px` e `40px` .  Outros tamanhos compatíveis incluem `19px` , `35px` e `38px` .  

Omanifest.jsa seguir [ no trecho de][ExtensionsApisupportManifestkeys] arquivo mostra um ícone de ação de navegador padrão e de alta definição sendo especificado usando a tecla [browser_action][MDNManifestjsonBrowserAction] .  A mesma sintaxe se aplica à chave [page_action][MDNManifestjsonPageAction] .  

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

Se a ação do navegador tiver sido definida pela extensão, ela aparecerá no menu ações após selecionar **mais (...)** ou à direita da barra de endereços se a opção **Mostrar botão ao lado da barra de endereços** for alternada pelo usuário.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Ação do navegador no menu Ação":::
         Ação do navegador no menu Ação :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Ação do navegador":::
         Ação do navegador :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### Ação da página  

A chave [page_action][MDNManifestjsonPageAction] tem a mesma sintaxe de manifesto JSON que a tecla [browser_action][MDNManifestjsonBrowserAction] .  A ação da página também tem os mesmos requisitos de tamanho de ícone da ação do navegador.  

Se a ação da página for especificada no [manifest.jsem][ExtensionsApisupportManifestkeys] arquivo, ela aparecerá na barra de endereços sempre que o método [PageAction. show][MDNApiPageactionShow] for usado.  

:::image type="complex" source="../media/pageaction.png" alt-text="Ação da página":::
   Ação da página
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### Interface do usuário de gerenciamento  

Quando os usuários navegam até o painel extensões indo para o menu **mais (...)** e selecionando **extensões**, um ícone é exibido ao lado do nome da extensão.  

Você deve especificar os tamanhos dos ícones a seguir.  

| Chave | Detalhes |  
|:--- |:--- |  
| `48px` | O ícone de resolução padrão é exibido. |  
| `128px` | Ícone de monitores de alta resolução. |  
| `176px` | Ícone para exibição de resolução ainda melhor. |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Interface do usuário de gerenciamento":::
   Interface do usuário de gerenciamento
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Ícones para empacotamento  

Depois que sua extensão estiver pronta para a embalagem, você deverá ter três tamanhos de ícone adicionais prontos.  

| Size | Detalhes |  
|:--- |:--- |  
| 44px | Usado na interface do usuário do Windows \(**lista de aplicativos**, aplicativos do sistema **configurações**  \>  ****  \>  **& recursos**\). |  
| 50px | Requisito de empacotamento \(não visível em qualquer lugar \). |  
| 150px | Usado como o ícone da Microsoft Store. |  


Consulte o [Guia de empacotamento manual][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] ou o [Guia de empacotamento do ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] para determinar onde esses ícones são colocados.  Isso depende de qual método de empacotamento você escolher.  

#### Ícone da Microsoft Store  

Se o ícone do 150px para a Microsoft Store tiver um plano de fundo transparente, a cor de destaque do dispositivo do usuário será exibida como a cor da tela de fundo do ícone.  

Por exemplo, se um usuário tiver selecionado rosa como a cor de destaque, o plano de fundo transparente do ícone da loja será exibido como rosa.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Cor de destaque do Windows":::
          Cor de destaque do Windows :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Cor da tela de fundo selecionada automaticamente":::
         Cor da tela de fundo selecionada automaticamente :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

Se quiser escolher sua própria cor de plano de fundo para a Microsoft Store, você deve torná-la opaca opaca.  

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.  [Entre em contato conosco][AkaExtensionRequest] com suas solicitações para a Microsoft Store e sua solicitação será considerada para uma atualização futura.  

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
