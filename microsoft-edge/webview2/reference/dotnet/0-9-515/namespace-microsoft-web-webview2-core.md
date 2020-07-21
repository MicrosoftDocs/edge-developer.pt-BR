---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: def4054fe123cfe8ce5db4905e4e6191162a2cf6
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884453"
---
# namespace 0.9.515-Microsoft. Web. WebView2. Core 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Formato de imagem usado pelo método CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Motivo para mover o foco.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | O tipo de uma solicitação de permissão.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Resposta a uma solicitação de permissão.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Tipo de falha de processo usada na classe CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Tipo de caixa de diálogo JavaScript usada na classe CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Valores de status de erro para navegações na Web.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Enumeração para contextos de solicitação de recurso da Web.
CoreWebView2 | O WebView2 permite que você hospede conteúdo da Web usando a tecnologia de navegador da Web mais recente do Edge.
CoreWebView2AcceleratorKeyPressedEventArgs | Args de evento para o evento AcceleratorKeyPressed.
CoreWebView2ContentLoadingEventArgs | Args de evento para o evento ContentLoading.
CoreWebView2Controller | Essa classe é o proprietário do objeto CoreWebView2 e fornece suporte para redimensionar, mostrar e ocultar, enfocar e outras funcionalidades relacionadas à janela e composição.
CoreWebView2Deferral | Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.
CoreWebView2DevToolsProtocolEventReceivedEventArgs | Args de evento para o evento DevToolsProtocolEventReceived.
CoreWebView2DevToolsProtocolEventReceiver | Um receptor é criado para um determinado evento de protocolo DevTools e permite que você assine e cancele a assinatura desse evento.
CoreWebView2Environment | Isso representa o ambiente WebView2.
CoreWebView2EnvironmentOptions | Opções usadas para criar o ambiente WebView2.
CoreWebView2MoveFocusRequestedEventArgs | Args de evento para o evento MoveFocusRequested.
CoreWebView2NavigationCompletedEventArgs | Args de evento para o evento NavigationCompleted.
CoreWebView2NavigationStartingEventArgs | Args de evento para o evento NavigationStarting.
CoreWebView2NewWindowRequestedEventArgs | Args de evento para o evento NewWindowRequested.
CoreWebView2PermissionRequestedEventArgs | Args de evento para o evento PermissionRequested.
CoreWebView2ProcessFailedEventArgs | Args de evento para o evento ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Args de evento para o evento ScriptDialogOpening.
CoreWebView2Settings | Define propriedades que habilitam, desabilitam ou modificam recursos do WebView.
CoreWebView2SourceChangedEventArgs | Argumentos de evento para o evento SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Args de evento para o evento WebMessageReceived.
CoreWebView2WebResourceRequestedEventArgs | Args de evento para o evento WebResourceRequested.
EdgeNotFoundException | A exceção que é lançada quando uma instalação de borda está ausente.
CoreWebView2PhysicalKeyStatus | Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.

## Parte

#### CoreWebView2CapturePreviewImageFormat 

> Enumeração [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
Formato            | Formato de imagem PNG.
Formato            | Formato de imagem JPEG.

Formato de imagem usado pelo método CoreWebView2CapturePreview.

#### CoreWebView2KeyEventKind 

> Enumeração [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
KeyDown            | Corresponde à mensagem do Window WM_KEYDOWN.
KeyUp            | Corresponde à mensagem do Window WM_KEYUP.
SystemKeyDown            | Corresponde à mensagem do Window WM_SYSKEYDOWN.
SystemKeyUp            | Corresponde à mensagem do Window WM_SYSKEYUP.

O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.

#### CoreWebView2MoveFocusReason 

> Enumeração [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
Maneira            | Configuração de código focalizada no WebView.
Próxima            | Movendo o foco devido à guia passagem para frente.
Anterior            | Movendo o foco devido a Tabulação de passagem para trás.

Motivo para mover o foco.

#### CoreWebView2PermissionKind 

> Enumeração [CoreWebView2PermissionKind](#corewebview2permissionkind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
UnknownPermission            | Permissões desconhecidas.
Microfone            | Permissão para capturar o áudio.
Câmera            | Permissão para capturar vídeo.
Geolocalização            | Permissão para acessar a localização geográfica.
Notificações            | Permissão para enviar notificações da Web.
OtherSensors            | Permissão para acessar o sensor genérico.
ClipboardRead            | Permissão para ler a área de transferência do sistema sem um gesto do usuário.

O tipo de uma solicitação de permissão.

#### CoreWebView2PermissionState 

> Enumeração [CoreWebView2PermissionState](#corewebview2permissionstate)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
Padrão            | Use o comportamento padrão do navegador, que normalmente solicita aos usuários a decisão.
Permitido            | Conceder a solicitação de permissão.
Negado            | Negue a solicitação de permissão.

Resposta a uma solicitação de permissão.

#### CoreWebView2ProcessFailedKind 

> Enumeração [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
BrowserProcessExited            | Indicou que o processo do navegador foi encerrado inesperadamente.
RenderProcessExited            | Indicou que o processo de renderização terminou inesperadamente.
RenderProcessUnresponsive            | Indicou que o processo de renderização se torna não responsivo.

Tipo de falha de processo usada na classe CoreWebView2ProcessFailedEventHandler.

#### CoreWebView2ScriptDialogKind 

> Enumeração [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
Alerta            | Uma caixa de diálogo chamada por meio da função JavaScript Window. Alert.
Confirmar            | Uma caixa de diálogo invocada pela janela. confirmar a função JavaScript.
Imediata            | Uma caixa de diálogo chamada por meio da função de JavaScript Window. prompt.
Beforeunload            | Uma caixa de diálogo chamada por meio da função JavaScript Window. beforeunload.

Tipo de caixa de diálogo JavaScript usada na classe CoreWebView2ScriptDialogOpeningEventHandler.

#### CoreWebView2WebErrorStatus 

> Enumeração [CoreWebView2WebErrorStatus](#corewebview2weberrorstatus)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
Desconhecido            | Ocorreu um erro desconhecido.
CertificateCommonNameIsIncorrect            | O nome comum do certificado SSL não corresponde ao endereço Web.
CertificateExpired            | O certificado SSL venceu.
ClientCertificateContainsErrors            | O certificado do cliente SSL contém erros.
CertificateRevoked            | A revogação do certificado SSL foi cancelada.
CertificateIsInvalid            | O certificado SSL é inválido &ndash; isso significa que o certificado não correspondia aos pins da chave pública para o nome do host, o certificado é assinado por uma autoridade não confiável ou por meio de um algoritmo de sinal fraco, o certificado declarado pelos nomes DNS viola restrições de nome, o certificado contém uma chave fraca, o período de validade do certificado é muito longo, falta de informações sobre a revogação ou o mecanismo de revogação, o nome do host não exclusivo, a falta de informações [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)de transparência do certificado
ServerUnreachable            | Não é possível acessar o host.
Tempo limite            | A conexão expirou.
ErrorHttpInvalidServerResponse            | O servidor retornou uma resposta inválida ou não reconhecida.
ConnectionAborted            | A conexão foi anulada.
ConnectionReset            | A conexão foi redefinida.
Desconectado            | A conexão à Internet foi perdida.
CannotConnect            | Não é possível se conectar ao destino.
HostNameNotResolved            | Não foi possível resolver o nome de host fornecido.
OperationCanceled            | A operação foi cancelada.
RedirectFailed            | Falha no redirecionamento de solicitação.
UnexpectedError            | Ocorreu um erro inesperado.

Valores de status de erro para navegações na Web.

#### CoreWebView2WebResourceContext 

> Enumeração [CoreWebView2WebResourceContext](#corewebview2webresourcecontext)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
Todas            | Todos os recursos.
Documento            | Recursos de documento.
Xsl            | Recursos CSS.
Imagem            | Recursos de imagem.
Mídia            | Outros recursos de mídia, como vídeos.
Fonte            | Recursos de fonte.
Script            | Recursos de script.
XMLHttpRequest            | Solicitações HTTP XML.
Retornar            | Busque a comunicação da API.
Texttrack            | Recursos do texttrack.
EventSource            | Comunicação de API de EventSource.
Websocket            | Comunicação de API WebSocket.
Manifesto            | Manifestos do aplicativo Web.
SignedExchange            | Trocas HTTP assinadas.
Disparo            | Solicitações de ping.
CspViolationReport            | Relatórios de violação de CSP.
Other            | Outros recursos.

Enumeração para contextos de solicitação de recurso da Web.

