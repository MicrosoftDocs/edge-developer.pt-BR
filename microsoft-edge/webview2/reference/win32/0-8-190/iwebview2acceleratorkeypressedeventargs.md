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
ms.openlocfilehash: 5b15d6205306e558d1d8709cceed8b7a68a77bce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652553"
---
# interface IWebView2AcceleratorKeyPressedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

Args de evento para o evento AcceleratorKeyPressed.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_KeyEventType](#get_keyeventtype) | O tipo de evento Key que causou o evento a ser disparado.
[get_VirtualKey](#get_virtualkey) | O código da chave virtual Win32 da chave que foi pressionada ou liberada.
[get_KeyEventLParam](#get_keyeventlparam) | O valor de LPARAM que acompanha a mensagem da janela.
[get_PhysicalKeyStatus](#get_physicalkeystatus) | Uma estrutura que representa as informações passadas no LPARAM da mensagem da janela.
[Cuide](#handle) | Ligar para isso permitirá que o processo do navegador continue.

## Parte

#### get_KeyEventType 

O tipo de evento Key que causou o evento a ser disparado.

> [get_KeyEventType](#get_keyeventtype)público HRESULT (WEBVIEW2_KEY_EVENT_TYPE * keyeventtype)

Esta é uma das WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN ou WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.

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

> público HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS * PhysicalKeyStatus)

#### Cuide 

Ligar para isso permitirá que o processo do navegador continue.

> [identificador](#handle)HRESULT (bool manipulado)

Se você passar verdadeiro, o navegador não impedirá que o navegador execute a ação padrão para essa chave aceleradora. Se o manipulador de eventos retornar sem [identificador de chamada ()](#handle), é equivalente a identificador de chamada (falso). Identificador de chamada [()](#handle) após ele já ter sido chamado ou o manipulador de eventos retornado não fará nada.

