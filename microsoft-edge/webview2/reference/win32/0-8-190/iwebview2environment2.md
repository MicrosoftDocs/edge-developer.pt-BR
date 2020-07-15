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
# 0.8.355-IWebView2Environment2 de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2Environment2
  : public IWebView2Environment
```

Funcionalidades adicionais implementadas pelo objeto Environment.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_BrowserVersionInfo](#get_browserversioninfo) | As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.

Consulte a interface [IWebView2Environment](IWebView2Environment.md) para obter mais detalhes. Você pode QueryInterface para essa interface do objeto que implementa [IWebView2Environment](IWebView2Environment.md).

## Parte

#### get_BrowserVersionInfo 

As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual, incluindo o nome do canal, se não for o canal estável.

> público HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR * versionInfo)

Isso corresponde ao formato da API GetWebView2BrowserVersionInfo. Os nomes dos canais são ' beta ', ' dev ' e ' Canárias '.

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

