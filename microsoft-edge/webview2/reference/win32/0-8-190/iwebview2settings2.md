---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 4e9f1d7baadcb20774bd4816f043f71a1a8b50b8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878201"
---
# 0.8.355-IWebView2Settings2 de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2Settings2
  : public IWebView2Settings
```

Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Defina a propriedade AreDefaultContextMenusEnabled.

As alterações de configuração feitas após o evento NavigationStarting não serão aplicadas até a próxima navegação de nível superior.

## Parte

#### get_AreDefaultContextMenusEnabled 

A propriedade AreDefaultContextMenusEnabled é usada para impedir que os menus de contexto padrão sejam mostrados para o usuário no WebView.

> [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)público HRESULT (bool * habilitado)

O padrão é TRUE.

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

#### put_AreDefaultContextMenusEnabled 

Defina a propriedade AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)público HRESULT (bool habilitado)

