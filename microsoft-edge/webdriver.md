---
ms.assetid: e56172c0-b635-4c02-8e0c-56bf8cb4c164
description: Saiba como começar a usar o WebDriver, um protocolo de conexão que permite que programas e scripts controlem o comportamento do navegador da Web.
title: WebDriver (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, webselenium, teste
ms.openlocfilehash: 0a6ef78103852234a6b52dfe88e60273cc3bd3d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562531"
---
# WebDriver (EdgeHTML)
A API do W3C [WebDriver](https://www.w3.org/TR/webdriver/) é uma plataforma e uma interface neutra em linguagem e um protocolo de conexão, permitindo que programas ou scripts controlem o comportamento de um navegador da Web.

O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário. Isso é diferente dos testes de unidade JavaScript porque o WebDriver tem acesso à funcionalidade e às informações que o JavaScript em execução no navegador não, e ele pode simular de forma mais precisa eventos do usuário ou eventos no nível do sistema operacional. O WebDriver também pode gerenciar o teste em várias janelas, guias e páginas da Web em uma única sessão de teste.

Veja aqui como começar a usar o WebDriver para Microsoft Edge (EdgeHTML).

A implementação do Microsoft Edge (EdgeHTML) do WebDriver permite a especificação do W3C para o [WebDrive](https://www.w3.org/TR/webdriver/) e o [protocolo de transmissão JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol) para compatibilidade com versões anteriores de testes existentes.

## Introdução ao WebDriver para Microsoft Edge (EdgeHTML)
* Instale o Windows 10.
* Baixe o servidor do [Microsoft WebDriver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/) apropriado para sua compilação do Windows e Microsoft Edge (EdgeHTML).
* Baixe a vinculação de linguagem do WebDriver de sua preferência. [Todas as associações de idiomas Selenium dão suporte ao Microsoft Edge (EdgeHTML)](https://docs.seleniumhq.org/download/).

> [!NOTE]
> Você pode encontrar ajuda, relatar problemas e solicitações de recurso de arquivo no [Microsoft Edge (EdgeHTML) comentários & suporte](https://developer.microsoft.com/microsoft-edge/support/).


## Usar o WebDriver
Para começar a usar o WebDriver com o Microsoft Edge (EdgeHTML), confira estes exemplos:

* [Exemplo de código C \ #](https://gist.github.com/InstyleVII/baf25274c55e891076d5#file-webdriver-cs) para abrir uma janela do navegador, navegando para Bing.com e procurando por "WebDriver" (do GitHub do GitHub).

## Sinalizadores de linha de comando do servidor WebDriver
Lista de sinalizadores de linha de comando para o servidor WebDriver.

| Nome    | Descrição                                                                                                      | Lançamento disponível |
|:--------|:-----------------------------------------------------------------------------------------------------------------|:------------------|
| hospedado    | IP do host a ser usado para o servidor WebDriver (padrão: localhost)                                                     | 14393             |
| porta    | Porta para usar para o servidor WebDriver (padrão: 17556)                                                            | 14393             |
| package | ApplicationUserModelId (AUMID) para o aplicativo ser iniciado pelo servidor WebDriver                        | 14393             |
| detalha | Reproduz solicitações recebidas e respostas enviadas pelo servidor WebDriver                                             | 14393             |
| silent  | Não gera nada                                                                                                  | 15063             |
| version | Gera a versão do MicrosoftWebDriver. exe                                                                    | 17763             |
| W3C     | Usar o protocolo W3C do WebDriver (opção padrão)                                                                      | 17763             |
| jwp     | Usar o protocolo de transmissão JSON                                                                                           | 17763             |
| Cleanup | Limpar dados temporários e chaves do registro definidos pelo servidor WebDriver para--Package. Outros parâmetros são ignorados | 17763             |

## W3C WebDriver
O suporte com base em cada comando para a [especificação do W3C do WebDriver](https://www.w3.org/TR/webdriver/).

### Recursos
| Funcionalidade                       | Chave                       | Status                   | Lançamento disponível |
|:---------------------------------|:--------------------------|:-------------------------|:------------------|
| Nome do navegador                     | "browsername"             | Com suporte                | 17763             |
| Versão do navegador                  | "browserVersion"          | Com suporte                | 17763             |
| Nome da plataforma                    | "PlatformName"            | Com suporte                | 17763             |
| Aceitar certificados TLS não seguros | "acceptInsecureCerts"     | Sem &nbsp; suporte       | N/A               |
| Estratégia de carregamento de página               | "pageLoadStrategy"        | Com suporte                | 17763             |
| Configuração de Proxy              | proxy                   | Sem &nbsp; suporte       | N/A               |
| Dimensionamento/posicionamento da janela  | "setWindowRect"           | Com suporte                | 17763             |
| Configuração de tempos limite de sessão   | tempos limite                | Com suporte                | 17763             |
| Comportamento de aviso não manipulado        | "unhandledPromptBehavior" | &nbsp;Suporte parcial | 17763             |
| InPrivate                        | "MS: InPrivate"            | Com suporte                | 17763             |
| Caminhos de extensão                  | "MS: extensionPaths"       | Com suporte                | 17763             |
| Página inicial                       | "MS: startPage"            | Com suporte                | 17763             |

### Estratégias do localizador
| Estratégia do localizador                                                        | Status    | Lançamento disponível |
|:------------------------------------------------------------------------|:----------|:------------------|
| [Seletores de CSS](https://www.w3.org/TR/webdriver/#css-selectors)         | Com suporte | 17763             |
| [Texto do link](https://www.w3.org/TR/webdriver/#link-text)                 | Com suporte | 17763             |
| [Texto do link parcial](https://www.w3.org/TR/webdriver/#partial-link-text) | Com suporte | 17763             |
| [Nome da marca](https://www.w3.org/TR/webdriver/#tag-name)                   | Com suporte | 17763             |
| [XPath](https://www.w3.org/TR/webdriver/#xpath)                         | Com suporte | 17763             |

### Comandos
| Método HTTP | Modelo de URI                                                   | Comando                                                                                   | Status             | Lançamento disponível |
|:------------|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------|:-------------------|:----------------  |
| POST        | /session                                                       | [Nova sessão](https://www.w3.org/TR/webdriver/#new-session)                               | Com suporte          | 17763             |
| DELETE      | ID do/Session/{Session}                                          | [Excluir sessão](https://www.w3.org/TR/webdriver/#delete-session)                         | Com suporte          | 17763             |
| GET         | /status                                                        | [Status](https://www.w3.org/TR/webdriver/#status)                                         | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/timeouts                                 | [Obter tempos limite](https://www.w3.org/TR/webdriver/#get-timeouts)                             | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/timeouts                                 | [Definir tempos limite](https://www.w3.org/TR/webdriver/#set-timeouts)                             | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/URL                                      | [Navegar até](https://www.w3.org/TR/webdriver/#navigate-to)                               | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/URL                                      | [Obter URL atual](https://www.w3.org/TR/webdriver/#get-current-url)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/back                                     | [Voltar](https://www.w3.org/TR/webdriver/#back)                                             | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Forward                                  | [Avançar](https://www.w3.org/TR/webdriver/#forward)                                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Refresh                                  | [Atualizar](https://www.w3.org/TR/webdriver/#refresh)                                       | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/title                                    | [Obter título](https://www.w3.org/TR/webdriver/#get-title)                                   | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Window                                   | [Obter identificador de janela](https://www.w3.org/TR/webdriver/#get-window-handle)                   | Com suporte          | 17763             |
| DELETE      | ID do/Session/{Session}/Window                                   | [Fechar a janela](https://www.w3.org/TR/webdriver/#close-window)                             | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Window                                   | [Alternar para janela](https://www.w3.org/TR/webdriver/#switch-to-window)                     | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Window/Handles                           | [Obter identificadores de janela](https://www.w3.org/TR/webdriver/#get-window-handles)                 | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/frame                                    | [Alternar para quadro](https://www.w3.org/TR/webdriver/#switch-to-frame)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/frame/Parent                             | [Alternar para o quadro pai](https://www.w3.org/TR/webdriver/#switch-to-parent-frame)         | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Window/Rect                              | [Obter janela Rect](https://www.w3.org/TR/webdriver/#get-window-rect)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Window/Rect                              | [Definir o Rect da janela](https://www.w3.org/TR/webdriver/#set-window-rect)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Window/maximize                          | [Maximizar janela](https://www.w3.org/TR/webdriver/#maximize-window)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Window/minimize                          | [Minimizar janela](https://www.w3.org/TR/webdriver/#minimize-window)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Window/fullscreen                        | [Janela de tela inteira](https://www.w3.org/TR/webdriver/#fullscreen-window)                   | Sem &nbsp; suporte | N/A               |
| GET         | ID do/Session/{Session}/Element/active                           | [Obter elemento ativo](https://www.w3.org/TR/webdriver/#get-active-element)                 | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Element                                  | [Localizar elemento](https://www.w3.org/TR/webdriver/#find-element)                             | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Elements                                 | [Localizar elementos](https://www.w3.org/TR/webdriver/#find-elements)                           | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Element/{Element ID}/Element             | [Localizar elemento do elemento](https://www.w3.org/TR/webdriver/#find-element-from-element)   | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Element/{Element ID}/Elements            | [Localizar elementos do elemento](https://www.w3.org/TR/webdriver/#find-elements-from-element) | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Element/{Element ID}/Selected            | [É o elemento selecionado](https://www.w3.org/TR/webdriver/#is-element-selected)               | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Element/{Element ID}/Attribute/{Name}    | [Obter atributo de elemento](https://www.w3.org/TR/webdriver/#get-element-attribute)           | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Element/{Element ID}/property/{name}     | [Obter Propriedade do elemento](https://www.w3.org/TR/webdriver/#get-element-property)             | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Element/{Element ID}/CSS/{Property nome} | [Obter valor CSS do elemento](https://www.w3.org/TR/webdriver/#get-element-css-value)           | Com suporte          | 17763             |
| GET         | ID/Session/{Session}/Element/{Element ID}/Text                | [Obter texto do elemento](https://www.w3.org/TR/webdriver/#get-element-text)                     | Com suporte          | 17763             |
| GET         | ID/Session/{Session}/Element/{Element ID}/Name                | [Obter nome da marca do elemento](https://www.w3.org/TR/webdriver/#get-element-tag-name)             | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Element/{Element ID}/Rect                | [Obter elemento Rect](https://www.w3.org/TR/webdriver/#get-element-rect)                     | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Element/{Element ID}/Enabled             | [O elemento está habilitado](https://www.w3.org/TR/webdriver/#is-element-enabled)                 | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Element/{Element ID}/Click               | [Elemento Click](https://www.w3.org/TR/webdriver/#element-click)                           | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Element/{Element ID}/Clear               | [Elemento limpo](https://www.w3.org/TR/webdriver/#element-clear)                           | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Element/{Element ID}/sendKeys            | [Teclas de envio de elemento](https://www.w3.org/TR/webdriver/#element-send-keys)                   | Com suporte          | 17763             |
| GET         | ID/Session/{Session}/Source                                   | [Obter fonte de página](https://www.w3.org/TR/webdriver/#get-page-source)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/execute/Sync                             | [Executar script](https://www.w3.org/TR/webdriver/#execute-script)                         | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/execute/Async                            | [Executar um script assíncrono](https://www.w3.org/TR/webdriver/#execute-async-script)             | Com suporte          | 17763             |
| GET         | ID do/Session/{session}/cookie                                   | [Obter todos os cookies](https://www.w3.org/TR/webdriver/#get-all-cookies)                       | Com suporte          | 17763             |
| GET         | ID do/Session/{session}/cookie/{Name}                            | [Obter o Cookie nomeado](https://www.w3.org/TR/webdriver/#get-named-cookie)                     | Com suporte          | 17763             |
| POST        | ID do/Session/{session}/cookie                                   | [Adicionar cookie](https://www.w3.org/TR/webdriver/#add-cookie)                                 | Com suporte          | 17763             |
| DELETE      | ID do/Session/{session}/cookie/{Name}                            | [Excluir cookie](https://www.w3.org/TR/webdriver/#delete-cookie)                           | Com suporte          | 17763             |
| DELETE      | ID do/Session/{session}/cookie                                   | [Excluir todos os cookies](https://www.w3.org/TR/webdriver/#delete-all-cookies)                 | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Actions                                  | [Executar ações](https://www.w3.org/TR/webdriver/#perform-actions)                       | Com suporte          | 17763             |
| DELETE      | ID do/Session/{Session}/Actions                                  | [Ações de lançamento](https://www.w3.org/TR/webdriver/#release-actions)                       | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Alert/dismiss                            | [Ignorar alerta](https://www.w3.org/TR/webdriver/#dismiss-alert)                           | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Alert/Accept                             | [Aceitar alerta](https://www.w3.org/TR/webdriver/#accept-alert)                             | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/Alert/Text                               | [Obter texto de alerta](https://www.w3.org/TR/webdriver/#get-alert-text)                         | Com suporte          | 17763             |
| POST        | ID do/Session/{Session}/Alert/Text                               | [Enviar texto de alerta](https://www.w3.org/TR/webdriver/#send-alert-text)                       | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/screenshot                               | [Fazer uma captura de tela](https://www.w3.org/TR/webdriver/#take-screenshot)                       | Com suporte          | 17763             |
| GET         | ID do/Session/{Session}/screenshot/{Element ID}                  | [Captura de tela do elemento](https://www.w3.org/TR/webdriver/#take-element-screenshot)       | Com suporte          | 17763             |

## Protocolo de transmissão JSON
O suporte com base em cada comando para o [protocolo de transmissão de JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol).

### Comandos
| Método HTTP | Caminho                                                                                                                                                         | Status             | Lançamento disponível |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------|
| GET         | [/status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)                                                                               | Com suporte          | 10240             |
| POST        | [/session](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#session-1)                                                                           | Com suporte          | 10240             |
| GET         | [/sessions](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessions)                                                                           | Com suporte          | 10240             |
| GET         | [/Session/: Identificação_da_sessão](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Com suporte          | 10240             |
| DELETE      | [/Session/: Identificação_da_sessão](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/timeouts](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeouts)                                        | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/timeouts/async_script](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsasync_script)               | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/timeouts/implicit_wait](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsimplicit_wait)             | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/window_handle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handle)                              | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/window_handles](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handles)                            | Com suporte          | 10586             |
| GET         | [/Session/: Identificação_da_sessão/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Com suporte          | 10240             |
| POST        | [/Session/: Identificação_da_sessão/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/Forward](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidforward)                                          | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/back](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidback)                                                | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/Refresh](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidrefresh)                                          | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/execute](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute)                                          | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/execute_async](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute_async)                              | Com suporte          | 10586             |
| GET         | [/Session/: Identificação_da_sessão/captura de tela](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidscreenshot)                                    | Com suporte          | 10240             |
| GET         | [/Session/: Id_da_sessão/IME/available_engines](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeavailable_engines)               | Sem &nbsp; suporte | N/A               |
| GET         | [/Session/: Id_da_sessão/IME/active_engine](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactive_engine)                       | Sem &nbsp; suporte | N/A               |
| GET         | [/Session/: Id_da_sessão/IME/Activated](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivated)                               | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Identificação_da_sessão/IME/desativar](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimedeactivate)                             | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/IME/Activate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivate)                                 | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Identificação_da_sessão/frame](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframe)                                              | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/frame/Parent](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframeparent)                                 | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Com suporte          | 10586             |
| DELETE      | [/Session/: Id_da_sessão/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/Window/: windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/Window/: windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/Window/: windowHandle/Position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/Window/: windowHandle/Position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/Window/: windowHandle/Maxim](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlemaximize) | Com suporte          | 10586             |
| GET         | [/Session/: Identificação_da_sessão/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Com suporte          | 10586             |
| POST        | [/Session/: Identificação_da_sessão/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Com suporte          | 10240             |
| DELETE      | [/Session/: Identificação_da_sessão/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Com suporte          | 10586             |
| DELETE      | [/Session/: Id_da_sessão/cookie/: Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookiename)                                  | Com suporte          | 10240             |
| GET         | [/Session/: Identificação_da_sessão/Source](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsource)                                            | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão}/title](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtitle)                                             | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/Element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelement)                                          | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/Elements](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelements)                                        | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/Element/active](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementactive)                             | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementid)                                    | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/element/: ID/elemento](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelement)                     | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/element/: ID/Elements](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelements)                   | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/element/: ID/clique em](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclick)                         | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/element/: ID/Submit](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsubmit)                       | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID/texto](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidtext)                           | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/element/: ID/valor](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidvalue)                         | Com suporte          | 10240             |
| POST        | [/Session/: Identificação_da_sessão/Keys](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidkeys)                                                | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID/nome](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidname)                           | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/element/: ID/Clear](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclear)                         | Com suporte          | 10240             |
| GET         | [/Session/: Id_da_sessão/element/: ID/Selected](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidselected)                   | Com suporte          | 10240             |
| GET         | [/Session/: Id_da_sessão/element/: ID/Enabled](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidenabled)                     | Com suporte          | 10240             |
| GET         | [/Session/: Id_da_sessão/element/: ID/atributo/: Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidattribute/:name)     | Com suporte          | 10240             |
| GET         | [/Session/: Id_da_sessão/element/: ID/Equals/: Other](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidequals/:other)         | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID/exibido](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementiddisplayed)                 | Com suporte          | 10240             |
| GET         | [/Session/: Id_da_sessão/element/: ID/local](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation)                   | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID/location_in_view](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation_in_view)   | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID/tamanho](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsize)                           | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/element/: ID/CSS/:p ropertyName](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidcss/:propertyName) | Com suporte          | 10240             |
| GET         | [/Session/: Identificação_da_sessão/orientação](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Identificação_da_sessão/orientação](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | Sem &nbsp; suporte | N/A               |
| GET         | [/Session/: Id_da_sessão/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/accept_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidaccept_alert)                                | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/dismiss_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddismiss_alert)                              | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/MoveTo](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidmoveto)                                            | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/clique em](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidclick)                                              | Com suporte          | 10240             |
| POST        | [/Session/: Id_da_sessão/BUTTONDOWN](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttondown)                                    | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/BUTTONUP](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttonup)                                        | Com suporte          | 10586             |
| POST        | [/Session/: Identificação_da_sessão/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddoubleclick)                                  | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/Touch/Click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchclick)                                   | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/down](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdown)                                     | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Identificação_da_sessão/Touch/up](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchup)                                         | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/mover](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchmove)                                     | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/Scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll)                                 | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/Scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll-1)                               | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Identificação_da_sessão/Touch/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdoubleclick)                       | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/longclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchlongclick)                           | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/movimento](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick)                                   | Sem &nbsp; suporte | N/A               |
| POST        | [/Session/: Id_da_sessão/Touch/movimento](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick-1)                                 | Sem &nbsp; suporte | N/A               |
| GET         | [/Session/: Identificação_da_sessão/local](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Com suporte          | 10586             |
| POST        | [/Session/: Identificação_da_sessão/local](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Com suporte          | 10586             |
| DELETE      | [/Session/: Id_da_sessão/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Com suporte          | 10586             |
| DELETE      | [/Session/: Id_da_sessão/local_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/local_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagesize)                     | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Com suporte          | 10586             |
| POST        | [/Session/: Id_da_sessão/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Com suporte          | 10586             |
| DELETE      | [/Session/: Id_da_sessão/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Com suporte          | 10586             |
| DELETE      | [/Session/: Id_da_sessão/session_storage/Key/: Key](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Com suporte          | 10586             |
| GET         | [/Session/: Id_da_sessão/session_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagesize)                 | Com suporte          | 10586             |
| GET         | [/Session/: Identificação_da_sessão/log](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlog)                                                  | Sem &nbsp; suporte | N/A               |
| GET         | [/Session/: Identificação_da_sessão/log/tipos](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlogtypes)                                       | Sem &nbsp; suporte | N/A               |
| GET         | [/Session/: Id_da_sessão/application_cache/status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidapplication_cachestatus)         | Com suporte          | 10586             |  
