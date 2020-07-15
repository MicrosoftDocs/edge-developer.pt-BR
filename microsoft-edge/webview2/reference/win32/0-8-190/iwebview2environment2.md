---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878544"
---
# <span data-ttu-id="748c2-104">0.8.355-IWebView2Environment2 de interface</span><span class="sxs-lookup"><span data-stu-id="748c2-104">0.8.355 - interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="748c2-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="748c2-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="748c2-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="748c2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="748c2-107">Funcionalidades adicionais implementadas pelo objeto Environment.</span><span class="sxs-lookup"><span data-stu-id="748c2-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="748c2-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="748c2-108">Summary</span></span>

 <span data-ttu-id="748c2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="748c2-109">Members</span></span>                        | <span data-ttu-id="748c2-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="748c2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="748c2-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="748c2-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="748c2-112">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="748c2-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="748c2-113">Consulte a interface [IWebView2Environment](IWebView2Environment.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="748c2-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="748c2-114">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="748c2-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="748c2-115">Parte</span><span class="sxs-lookup"><span data-stu-id="748c2-115">Members</span></span>

#### <span data-ttu-id="748c2-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="748c2-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="748c2-117">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="748c2-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="748c2-118">público HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="748c2-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="748c2-119">Isso corresponde ao formato da API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="748c2-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="748c2-120">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="748c2-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

