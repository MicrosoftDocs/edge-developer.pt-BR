---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d2c3b3ee179dec217418241031142549d170e440
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652341"
---
# Classe Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties 

Namespace: Microsoft. Web. WebView2. WPF \
Assembly: Microsoft. Web. WebView2. WPF. dll

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

Essa classe é um pacote dos parâmetros mais comuns usados para criar um CoreWebView2Environment.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[BrowserExecutableFolder](#browserexecutablefolder) | Obtém ou define o valor a ser passado como o parâmetro browserExecutableFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.
[Idioma](#language) | Obtém ou define o valor a ser usado para a propriedade Language do parâmetro CoreWebView2EnvironmentOptions passado para CoreWebView2Environment. createasync ao criar um ambiente com essa instância.
[UserDataFolder](#userdatafolder) | Obtém ou define o valor a ser passado como o parâmetro userDataFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.
[CoreWebView2CreationProperties](#corewebview2creationproperties) | Cria uma nova instância de CoreWebView2CreationProperties com dados padrão para todas as propriedades.

Sua principal finalidade é definir como [WebView2. creationproperties](microsoft-web-webview2-wpf-webview2.md) para personalizar o ambiente usado por um [WebView2](microsoft-web-webview2-wpf-webview2.md) durante a inicialização implícita. Também é um excelente utilitário de integração do WPF que permite que os parâmetros de ambiente comumente usados sejam Propriedades de dependência e sejam criados e usados na marcação.

Essa classe não deve conter todas as opções de personalização de ambiente possíveis. Se precisar de controle total sobre o ambiente usado por um controle WebView2, você precisará inicializar o controle explicitamente criando seu próprio ambiente com CoreWebView2Environment. createasync e transmitindo-o para [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de definir a propriedade [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) para qualquer coisa. Consulte a documentação da classe [WebView2](microsoft-web-webview2-wpf-webview2.md) para obter uma visão geral de inicialização.

## Parte

#### BrowserExecutableFolder 

Obtém ou define o valor a ser passado como o parâmetro browserExecutableFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.

> Cadeia de caracteres pública [BrowserExecutableFolder](#browserexecutablefolder)

#### Idioma 

Obtém ou define o valor a ser usado para a propriedade Language do parâmetro CoreWebView2EnvironmentOptions passado para CoreWebView2Environment. createasync ao criar um ambiente com essa instância.

> [linguagem](#language) de cadeia de caracteres pública

#### UserDataFolder 

Obtém ou define o valor a ser passado como o parâmetro userDataFolder de CoreWebView2Environment. createasync ao criar um ambiente com essa instância.

> Cadeia de caracteres pública [UserDataFolder](#userdatafolder)

#### CoreWebView2CreationProperties 

Cria uma nova instância de CoreWebView2CreationProperties com dados padrão para todas as propriedades.

> [CoreWebView2CreationProperties](#corewebview2creationproperties)público ()

