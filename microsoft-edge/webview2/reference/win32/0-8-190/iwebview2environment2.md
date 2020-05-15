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
ms.openlocfilehash: 00b19d1174a5d5ac643a04038ecdd60c82211194
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652604"
---
# <span data-ttu-id="69c29-104">interface IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="69c29-104">interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="69c29-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="69c29-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="69c29-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="69c29-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="69c29-107">Funcionalidades adicionais implementadas pelo objeto Environment.</span><span class="sxs-lookup"><span data-stu-id="69c29-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="69c29-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="69c29-108">Summary</span></span>

 <span data-ttu-id="69c29-109">Parte</span><span class="sxs-lookup"><span data-stu-id="69c29-109">Members</span></span>                        | <span data-ttu-id="69c29-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="69c29-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="69c29-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="69c29-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="69c29-112">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="69c29-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="69c29-113">Consulte a interface [IWebView2Environment](IWebView2Environment.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="69c29-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="69c29-114">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="69c29-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="69c29-115">Parte</span><span class="sxs-lookup"><span data-stu-id="69c29-115">Members</span></span>

#### <span data-ttu-id="69c29-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="69c29-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="69c29-117">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="69c29-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="69c29-118">público HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="69c29-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="69c29-119">Isso corresponde ao formato da API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="69c29-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="69c29-120">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="69c29-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

