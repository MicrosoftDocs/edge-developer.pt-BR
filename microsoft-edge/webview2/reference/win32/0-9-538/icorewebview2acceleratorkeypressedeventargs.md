---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2AcceleratorKeyPressedEventArgs
ms.openlocfilehash: b646846c85c0e36fbcf7a55cd98f7495c252f8f9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010611"
---
# 0.9.579-ICoreWebView2AcceleratorKeyPressedEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Args de evento para o evento AcceleratorKeyPressed.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.
[get_KeyEventKind](#get_keyeventkind) | O tipo de evento Key que causou o evento a ser disparado.
[get_KeyEventLParam](#get_keyeventlparam) | O valor de LPARAM que acompanha a mensagem da janela.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.
[get_VirtualKey](#get_virtualkey) | O código da chave virtual Win32 da chave que foi pressionada ou liberada.
[put_Handled](#put_handled) | Define a propriedade Handled.

## Parte

#### get_Handled 

Durante a invocação do manipulador AcceleratorKeyPressedEvent, o WebView está bloqueado aguardando a decisão de se o acelerador será manipulado pelo host ou não.

> [get_Handled](#get_handled)público HRESULT (bool * manipulado)

Se a propriedade Handled estiver definida como TRUE, isso impedirá que o WebView execute a ação padrão para essa chave aceleradora. Caso contrário, o WebView executará a ação padrão para a tecla aceleradora.

#### get_KeyEventKind 

O tipo de evento Key que causou o evento a ser disparado.

> público HRESULT [get_KeyEventKind](#get_keyeventkind)(COREWEBVIEW2_KEY_EVENT_KIND * KeyEventKind)

#### get_KeyEventLParam 

O valor de LPARAM que acompanha a mensagem da janela.

> público HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int * lParam)

Consulte a documentação para as mensagens de WM_KEYDOWN e WM_KEYUP.

#### get_PhysicalKeyStatus 

Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.

> público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(COREWEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### get_VirtualKey 

O código da chave virtual Win32 da chave que foi pressionada ou liberada.

> público HRESULT [get_VirtualKey](#get_virtualkey)(UINT * VirtualKey)

Isso será uma das constantes de chave virtual do Win32, como VK_RETURN ou um valor ASCII (maiúsculo) como ' A '. Você pode verificar se a tecla CTRL ou Alt está pressionada chamando GetKeyState (VK_CONTROL) ou GetKeyState (VK_MENU).

#### put_Handled 

Define a propriedade Handled.

> [put_Handled](#put_handled)público HRESULT (bool manipulado)

