---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: ba91056fa6d2e6cf9e7da18202fb3c74d7deb827
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010240"
---
# 0.9.579-ICoreWebView2ExperimentalEnvironmentOptions de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

Opções experimentais usadas para criar o ambiente WebView2.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled) | A propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.
[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled) | Defina a propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled.

Uma implementação padrão é fornecida em WebView2ExperimentalEnvironmentOptions. h.

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2ExperimentalEnvironmentOptions>();
    CHECK_FAILURE(options->put_IsSingleSignOnUsingOSPrimaryAccountEnabled(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## Parte

#### get_IsSingleSignOnUsingOSPrimaryAccountEnabled 

A propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.

> [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)público HRESULT (bool * habilitado)

O padrão é desabilitado. Os aplicativos da plataforma universal do Windows também devem declarar o [recurso restrito](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO para que o logon único funcione.

#### put_IsSingleSignOnUsingOSPrimaryAccountEnabled 

Defina a propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled.

> [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)público HRESULT (bool habilitado)

