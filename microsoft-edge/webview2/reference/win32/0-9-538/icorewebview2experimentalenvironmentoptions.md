---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalEnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalEnvironmentOptions
ms.openlocfilehash: 3e18c15e23338404720dae917cb6d009c41c3c04
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886509"
---
# <span data-ttu-id="f6366-104">interface ICoreWebView2ExperimentalEnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="f6366-104">interface ICoreWebView2ExperimentalEnvironmentOptions</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalEnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="f6366-105">Opções experimentais usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="f6366-105">Experimental options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="f6366-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f6366-106">Summary</span></span>

 <span data-ttu-id="f6366-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f6366-107">Members</span></span>                        | <span data-ttu-id="f6366-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f6366-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f6366-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="f6366-109">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#get_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="f6366-110">A propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.</span><span class="sxs-lookup"><span data-stu-id="f6366-110">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="f6366-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="f6366-111">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span>](#put_issinglesignonusingosprimaryaccountenabled) | <span data-ttu-id="f6366-112">Defina a propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="f6366-112">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

<span data-ttu-id="f6366-113">Uma implementação padrão é fornecida em WebView2ExperimentalEnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="f6366-113">A default implementation is provided in WebView2ExperimentalEnvironmentOptions.h.</span></span>

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

## <span data-ttu-id="f6366-114">Parte</span><span class="sxs-lookup"><span data-stu-id="f6366-114">Members</span></span>

#### <span data-ttu-id="f6366-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="f6366-115">get_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="f6366-116">A propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.</span><span class="sxs-lookup"><span data-stu-id="f6366-116">The IsSingleSignOnUsingOSPrimaryAccountEnabled property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="f6366-117">[get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)público HRESULT (bool \* habilitado)</span><span class="sxs-lookup"><span data-stu-id="f6366-117">public HRESULT [get_IsSingleSignOnUsingOSPrimaryAccountEnabled](#get_issinglesignonusingosprimaryaccountenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="f6366-118">O padrão é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6366-118">Default is disabled.</span></span> <span data-ttu-id="f6366-119">Os aplicativos da plataforma universal do Windows também devem declarar o [recurso restrito](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO para que o logon único funcione.</span><span class="sxs-lookup"><span data-stu-id="f6366-119">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="f6366-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span><span class="sxs-lookup"><span data-stu-id="f6366-120">put_IsSingleSignOnUsingOSPrimaryAccountEnabled</span></span> 

<span data-ttu-id="f6366-121">Defina a propriedade IsSingleSignOnUsingOSPrimaryAccountEnabled.</span><span class="sxs-lookup"><span data-stu-id="f6366-121">Set the IsSingleSignOnUsingOSPrimaryAccountEnabled property.</span></span>

> <span data-ttu-id="f6366-122">[put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)público HRESULT (bool habilitado)</span><span class="sxs-lookup"><span data-stu-id="f6366-122">public HRESULT [put_IsSingleSignOnUsingOSPrimaryAccountEnabled](#put_issinglesignonusingosprimaryaccountenabled)(BOOL enabled)</span></span>

