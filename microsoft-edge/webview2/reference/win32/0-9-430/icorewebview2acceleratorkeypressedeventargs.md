---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 1168749b27488831d914a4f64c0830f39d53415f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652760"
---
# interface ICoreWebView2AcceleratorKeyPressedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Args de evento para o evento AcceleratorKeyPressed.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_KeyEventKind](#get_keyeventkind) | O tipo de evento Key que causou o evento a ser disparado.
[get_VirtualKey](#get_virtualkey) | O código da chave virtual Win32 da chave que foi pressionada ou liberada.
[get_KeyEventLParam](#get_keyeventlparam) | O valor de LPARAM que acompanha a mensagem da janela.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.
[get_Handled](#get_handled) | Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.
[put_Handled](#put_handled) | Define a propriedade Handled.

## Parte

#### get_KeyEventKind 

O tipo de evento Key que causou o evento a ser disparado.

> público HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND * KeyEventKind)

#### get_VirtualKey 

O código da chave virtual Win32 da chave que foi pressionada ou liberada.

> público HRESULT [get_VirtualKey](#get_virtualkey)(UINT * VirtualKey)

Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '. Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).

#### get_KeyEventLParam 

O valor de LPARAM que acompanha a mensagem da janela.

> público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * lParam)

Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.

#### get_PhysicalKeyStatus 

Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.

> público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### get_Handled 

Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.

> [get_Handled](#get_handled)público HRESULT (bool * manipulado)

Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora. Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.

#### put_Handled 

Define a propriedade Handled.

> [put_Handled](#put_handled)público HRESULT (bool manipulado)

