---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886084"
---
# <span data-ttu-id="6efca-104">0.8.355-IWebView2Environment2 de interface</span><span class="sxs-lookup"><span data-stu-id="6efca-104">0.8.355 - interface IWebView2Environment2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="6efca-105">Funcionalidades adicionais implementadas pelo objeto Environment.</span><span class="sxs-lookup"><span data-stu-id="6efca-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="6efca-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6efca-106">Summary</span></span>

 <span data-ttu-id="6efca-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6efca-107">Members</span></span>                        | <span data-ttu-id="6efca-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6efca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6efca-109">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6efca-109">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="6efca-110">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="6efca-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="6efca-111">Consulte a interface [IWebView2Environment](IWebView2Environment.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="6efca-111">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="6efca-112">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="6efca-112">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="6efca-113">Parte</span><span class="sxs-lookup"><span data-stu-id="6efca-113">Members</span></span>

#### <span data-ttu-id="6efca-114">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6efca-114">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="6efca-115">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.</span><span class="sxs-lookup"><span data-stu-id="6efca-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="6efca-116">público HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="6efca-116">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="6efca-117">Isso corresponde ao formato da API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="6efca-117">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="6efca-118">Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.</span><span class="sxs-lookup"><span data-stu-id="6efca-118">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

