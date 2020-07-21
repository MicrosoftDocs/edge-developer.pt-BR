---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 4ba0299f3afbc6fc2846481f52c1000cd338ecd8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885778"
---
# <span data-ttu-id="304f2-104">0.8.355-IWebView2Settings2 de interface</span><span class="sxs-lookup"><span data-stu-id="304f2-104">0.8.355 - interface IWebView2Settings2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="304f2-105">Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.</span><span class="sxs-lookup"><span data-stu-id="304f2-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="304f2-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="304f2-106">Summary</span></span>

 <span data-ttu-id="304f2-107">Parte</span><span class="sxs-lookup"><span data-stu-id="304f2-107">Members</span></span>                        | <span data-ttu-id="304f2-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="304f2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="304f2-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="304f2-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="304f2-110">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="304f2-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="304f2-111">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="304f2-111">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="304f2-112">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="304f2-112">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="304f2-113">As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="304f2-113">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="304f2-114">Parte</span><span class="sxs-lookup"><span data-stu-id="304f2-114">Members</span></span>

#### <span data-ttu-id="304f2-115">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="304f2-115">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="304f2-116">A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.</span><span class="sxs-lookup"><span data-stu-id="304f2-116">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="304f2-117">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="304f2-117">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="304f2-118">O padrão é TRUE.</span><span class="sxs-lookup"><span data-stu-id="304f2-118">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="304f2-119">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="304f2-119">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="304f2-120">Defina a propriedade AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="304f2-120">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="304f2-121">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="304f2-121">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

