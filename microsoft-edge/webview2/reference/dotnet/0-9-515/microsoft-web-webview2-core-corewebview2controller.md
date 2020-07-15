---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 72121ddbc81d2228bf8d185b977e5f3e7ca2deb4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879020"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Controller 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Essa classe é o proprietário do objeto CoreWebView2 e fornece suporte para redimensionar, mostrar e ocultar, enfocar e outras funcionalidades relacionadas à janela e composição.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[AcceleratorKeyPressed](#acceleratorkeypressed) | AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado.
[Limites](#bounds) | Os limites da WebView.
[CoreWebView2](#corewebview2) | Obtém a CoreWebView2 associada a este CoreWebView2Controller.
[GotFocus](#gotfocus) | GotFocus é acionado quando o WebView tem foco.
[IsVisible](#isvisible) | A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.
[LostFocus](#lostfocus) | LostFocus é acionado quando o WebView perdeu o foco.
[MoveFocusRequested](#movefocusrequested) | MoveFocusRequested é acionado quando o usuário tenta Tab no WebView.
[ParentWindow](#parentwindow) | A janela pai fornecida pelo aplicativo que este WebView usa para renderizar o conteúdo.
[ZoomFactor](#zoomfactor) | O fator de zoom para o WebView.
[ZoomFactorChanged](#zoomfactorchanged) | O evento é acionado quando a propriedade ZoomFactor da WebView é alterada.
[Fechar](#close) | Fecha a WebView e limpa a instância do navegador subjacente.
[MoveFocus](#movefocus) | Mover o foco para o WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Esta é uma notificação separada dos limites que dizem ao WebView que o HWND pai (ou qualquer ancestral) moveu.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Atualize as propriedades Bounds e ZoomFactor ao mesmo tempo.

O CoreWebView2Controller é proprietário do CoreWebView2 e, se todas as referências à CoreWebView2Controller ficarem ausentes, o WebView será fechado.

## Parte

#### AcceleratorKeyPressed 

AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado.

> < do evento público EventHandler [CoreWebView2AcceleratorKeyPressedEventArgs](microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)  >  [AcceleratorKeyPressed](#acceleratorkeypressed)

AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado. Uma tecla é considerada um acelerador se:

1. A tecla CTRL ou Alt está sendo mantida no momento ou

1. a tecla pressionada não é mapeada para um caractere. Algumas teclas específicas nunca são consideradas aceleradores, como Shift. A tecla escape é sempre considerada um acelerador.

Os eventos chave repetido com repetição causada pela manutenção da tecla para baixo também acionarão esse evento. Você pode filtrá-los verificando os argumentos do evento KeyEventLParam ou PhysicalKeyStatus.

No modo de janela, esse manipulador de eventos é chamado sincronicamente. Até que você chame Handle () nos argumentos do evento ou o manipulador de eventos seja retornado, o processo do navegador será bloqueado e as chamadas COM saída cruzada de processo não funcionarão com RPC_E_CANTCALLOUT_ININPUTSYNCCALL. No entanto, todos os métodos de API CoreWebView2 funcionarão.

No modo sem janela, o manipulador de eventos é chamado de forma assíncrona. A entrada adicional não entrará em contato com o navegador até que o manipulador de eventos retorne ou manipule () seja chamado, mas o processo do navegador em si não será bloqueado, e as chamadas COM de saída funcionarão normalmente.

É recomendável chamar Handle (TRUE), como o mais cedo possível, se souber que deseja manipular a tecla aceleradora.

#### Limites 

Os limites da WebView.

> [limites](#bounds) do retângulo público

Os limites são relativos ao HWND pai. O aplicativo tem duas maneiras de posicionar um WebView:

1. Crie um HWND filho que seja o HWND pai do WebView. Posicione esta janela onde o WebView deve estar. Nesse caso, use (0, 0) para o canto superior esquerdo Bound's do WebView (o deslocamento).

1. Use a janela mais superior do aplicativo como o HWND pai do WebView. Defina o Bound's canto superior esquerdo da WebView para que o WebView esteja posicionado corretamente no aplicativo. Os valores do limite estão no espaço de coordenadas do host.

#### CoreWebView2 

Obtém a CoreWebView2 associada a este CoreWebView2Controller.

> [CoreWebView2](microsoft-web-webview2-core-corewebview2.md) público [CoreWebView2](#corewebview2)

#### GotFocus 

GotFocus é acionado quando o WebView tem foco.

> objeto< do evento público EventHandler > [GotFocus](#gotfocus)

#### IsVisible 

A propriedade IsVisible Determina se deseja mostrar ou ocultar o WebView.

> bool público [IsVisible](#isvisible)

Se IsVisible estiver definido como false, o WebView será transparente e não será renderizado. No entanto, isso não afetará a janela que contém o WebView (o parâmetro HWND que foi passado para CreateCoreWebView2Controller). Se você quiser que essa janela desapareça também, chame o recurso de janela diretamente, além de modificar a propriedade IsVisible. A WebView como uma janela filho não obterá mensagens de janela quando a janela superior for minimizada ou restaurada. Por motivo de desempenho, o desenvolvedor deve definir a propriedade IsVisible do WebView como false quando a janela do aplicativo é minimizada e retomada como true quando a janela do aplicativo for restaurada. A janela do aplicativo pode fazer isso ao manipular SC_MINIMIZE e SC_RESTORE comando ao receber WM_SYSCOMMAND mensagem.

#### LostFocus 

LostFocus é acionado quando o WebView perdeu o foco.

> objeto<-EventHandler de evento público > [LostFocus](#lostfocus)

No caso em que o evento MoveFocusRequested é acionado, o foco continua no WebView quando o evento MoveFocusRequested é acionado. O foco perdido só será acionado depois que o código do aplicativo ou a ação padrão do conjunto de eventos MoveFocusRequested se concentrar em uma exibição de exibição ausente.

#### MoveFocusRequested 

MoveFocusRequested é acionado quando o usuário tenta Tab no WebView.

> < do evento público EventHandler [CoreWebView2MoveFocusRequestedEventArgs](microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)  >  [MoveFocusRequested](#movefocusrequested)

O foco da WebView não mudou quando esse evento é acionado.

#### ParentWindow 

A janela pai fornecida pelo aplicativo que este WebView usa para renderizar o conteúdo.

> [ParentWindow](#parentwindow) de IntPtr público

Definir a propriedade fará com que o WebView redefina o pai da janela para a janela recém fornecida.

#### ZoomFactor 

O fator de zoom para o WebView.

> [ZoomFactors](#zoomfactor) duplos públicos

Observe que a alteração do fator de zoom pode fazer com que o `window.innerWidth/innerHeight` layout da página seja alterado. Um fator de zoom aplicado pelo host chamando ZoomFactor se torna o novo zoom padrão para o WebView. Esse fator de zoom se aplica a navegações e é o fator de zoom que é retornado quando o usuário pressiona Ctrl + 0. Quando o fator de zoom é alterado pelo usuário (resultante do aplicativo que recebe ZoomFactorChanged), esse zoom se aplica apenas à página atual. O zoom aplicado pelo usuário é somente para a página atual e é redefinido em uma navegação. Não é permitido especificar um zoomFactor menor ou igual a 0. WebView também tem um intervalo de fator de zoom interno com suporte. Quando um fator de zoom especificado estiver fora desse intervalo, ele será normalizado para estar dentro do intervalo, e um evento ZoomFactorChanged será acionado para o fator de zoom aplicado real. Quando essa faixa de normalização acontece, a propriedade ZoomFactor relata o fator de zoom especificado durante a modificação anterior da propriedade ZoomFactor até que o evento ZoomFactorChanged seja recebido após o WebView se aplicar o fator de zoom normalizado.

#### ZoomFactorChanged 

O evento é acionado quando a propriedade ZoomFactor da WebView é alterada.

> objeto<-EventHandler de evento público > [ZoomFactorChanged](#zoomfactorchanged)

O evento pode ser acionado porque o chamador modificou a propriedade ZoomFactor ou porque o usuário modificou manualmente o zoom. Quando ela é modificada pelo chamador por meio da propriedade ZoomFactor, o fator de zoom interno é atualizado imediatamente e não haverá um evento ZoomFactorChanged. O WebView associa o último fator de zoom usado para cada site. Portanto, é possível que o fator de zoom mude ao navegar para uma página diferente. Quando o fator de zoom muda devido a isso, o evento ZoomFactorChanged é acionado logo após o evento ContentLoading.

#### Fechar 

Fecha a WebView e limpa a instância do navegador subjacente.

> public void [Close](#close)()

A limpeza da instância do navegador liberará os recursos que alimentam o WebView. A instância do navegador será encerrada se não houver outros webviews que o usam.

Depois de chamar Close, todas as chamadas de método falharão e os manipuladores de eventos deixarão de ser acionados. Especificamente, a WebView liberará suas referências a seus manipuladores de eventos quando Close for chamado.

Fechar é chamado implicitamente quando o CoreWebView2Controller perde sua referência final e é destruido. Mas é uma prática recomendada chamar o fechamento explicitamente para evitar qualquer ciclo acidental de referências entre o WebView e o código do aplicativo. Especificamente, se você capturar uma referência ao WebView em um manipulador de eventos, criará um ciclo de referência entre o WebView e o manipulador de eventos. Chamar Close irá interromper esse ciclo liberando todos os manipuladores de eventos. Mas para evitar essa situação, é recomendável que a chamada seja fechada explicitamente no WebView e não Capture uma referência para o WebView para garantir que o WebView possa ser limpo corretamente.

#### MoveFocus 

Mover o foco para o WebView.

> public void [MoveFocus](#movefocus)(motivo[CoreWebView2MoveFocusReason](./namespace-microsoft-web-webview2-core.md) )

O WebView receberá o foco e o foco será definido como elemento correspondente na página hospedada na WebView. Para motivo programático, o foco é definido como elemento prefoco anteriormente ou o elemento padrão se não houver nenhum elemento focalizado anteriormente. Para o próximo motivo, o foco é definido como o primeiro elemento. Para o motivo anterior, o foco é definido como o último elemento. A WebView também pode ter o foco por meio da interação do usuário, como clicar em um WebView ou Tab. Para tabulação, o aplicativo pode chamar MoveFocus com o próximo ou o anterior para alinhar-se com Tab e Shift + Tab, respectivamente, quando decide que o WebView é o próximo elemento que pode ser tabulado. Ou, o aplicativo pode chamar IsDialogMessage como parte de seu loop de mensagem para permitir que a plataforma manipule a Tabulação automaticamente. A plataforma irá girar por todas as janelas com WS_TABSTOP. Quando a WebView se concentrar no IsDialogMessage, o foco será inserido internamente no primeiro ou último elemento para Tab e Shift + Tab respectivamente.

#### NotifyParentWindowPositionChanged 

Esta é uma notificação separada dos limites que dizem ao WebView que o HWND pai (ou qualquer ancestral) moveu.

> public void [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Isso é necessário para acessibilidade e determinadas caixas de diálogo no WebView para funcionar corretamente.

#### SetBoundsAndZoomFactor 

Atualize as propriedades Bounds e ZoomFactor ao mesmo tempo.

> public void [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(limites Rect, ZoomFactor duplo)

Esta operação é atômica da perspectiva do host. Após retornar dessa função, as propriedades Bounds e ZoomFactor terão ambos sido atualizadas se a função for bem-sucedida ou nenhuma será atualizada se a função falhar. Se os limites e ZoomFactor forem atualizados com a mesma escala (ou seja, os limites e ZoomFactor forem ambos duplicados), a página não verá uma alteração em Window. innerWidth/innerHeight e o WebView renderizará o conteúdo no novo tamanho e será aplicado sem renderizações intermediárias. Essa função também pode ser usada para atualizar apenas um de ZoomFactor ou limites passando o novo valor para um e o valor atual para o outro.

