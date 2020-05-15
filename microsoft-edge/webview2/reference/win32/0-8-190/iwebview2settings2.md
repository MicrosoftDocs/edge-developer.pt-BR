---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: cb317e9078e48ed14091eb2eda6ff9d59a19c6ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652491"
---
# <span data-ttu-id="44c5a-104">interface IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="44c5a-104">interface IWebView2Settings2</span></span> 

> [!NOTE]
> <span data-ttu-id="44c5a-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="44c5a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="44c5a-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="44c5a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="44c5a-107">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="44c5a-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="44c5a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="44c5a-108">Summary</span></span>

 <span data-ttu-id="44c5a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="44c5a-109">Members</span></span>                        | <span data-ttu-id="44c5a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="44c5a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44c5a-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="44c5a-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="44c5a-112">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="44c5a-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="44c5a-113">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="44c5a-113">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="44c5a-114">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="44c5a-114">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="44c5a-115">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="44c5a-115">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="44c5a-116">Parte</span><span class="sxs-lookup"><span data-stu-id="44c5a-116">Members</span></span>

#### <span data-ttu-id="44c5a-117">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="44c5a-117">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="44c5a-118">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="44c5a-118">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="44c5a-119">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="44c5a-119">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="44c5a-120">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="44c5a-120">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="44c5a-121">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="44c5a-121">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="44c5a-122">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="44c5a-122">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="44c5a-123">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="44c5a-123">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

