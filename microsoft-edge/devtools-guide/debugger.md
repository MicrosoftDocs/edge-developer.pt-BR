---
description: Use o depurador para percorrer e solucionar problemas com o seu código.
title: DevTools-depurador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, depurador, depuração, pontos de interrupção, inspeções, trabalhadores do serviço, API do cache, armazenamento na Web, cookies
ms.custom: seodec18
ms.openlocfilehash: f82fbb057a3ad1027309d89db1a15dbcbea31292
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562240"
---
# Depurador

Use o **depurador** para depurar o código, definir inspeções e pontos de interrupção, editar ao vivo seu código e inspecionar os caches. Teste e solucione o problema do seu código:

- [Procurando](#resource-picker) e [procurando](#file-search) código de seus arquivos de origem carregados
- [Controlando o fluxo de execução](#toolbar) enquanto você percorre o código
- [Gerenciamento de recursos de armazenamento de página](./storage.md#cache-manager), incluindo os [funcionários do serviço e o cache](./service-workers.md), [os cookies](./storage.md#cookies-list) e o [armazenamento na Web](./storage.md#local-and-session-storage-managers)  
- [Definir pontos de interrupção e editar ao vivo](#debug-window) seu código durante a execução
- [Rastrear e editar as variáveis locais](#watches) enquanto você depura
- [Ocultar ou mostrar o código assíncrono e o código da biblioteca](#call-stack) da pilha de chamadas conforme necessário
- [Adicionando pontos de interrupção especializados](#breakpoints) para XMLHttpRequests, eventos e [mutações dom](#dom-breakpoints)

![O depurador do Microsoft Edge DevTools](./media/debugger.png)

Há três maneiras de iniciar uma sessão de depuração.

1. **Definir um ponto de interrupção.** Quando a execução do seu código chegar, você entrará no depurador e poderá percorrer o código.
2. **Iniciar uma pausa no código.** Clique no botão da barra de ferramentas de [**quebra**](#toolbar) (ícone de*pausa* ) ou `Ctrl+Shift+B` . O depurador será interrompido na próxima instrução de execução.
3. **Defina o comportamento da exceção.** Use o menu [**alterar comportamento de exceção**](#toolbar) ( `Ctrl+Shift+E` ) para invadir o depurador quando o código gera uma exceção. Por padrão, o depurador é definido para *nunca interromper em exceções*, mas ele é registrado no console.

## Seletor de recursos

Geralmente, a primeira etapa na depuração é definir pontos de interrupção no código que você está procurando para solucionar o problema. Você pode encontrar todos os arquivos de código carregados pela página no painel do *seletor de recursos* , incluindo arquivos *. html,. css* e *. js* .

 Clicar em uma entrada de arquivo abrirá uma guia para esse arquivo na [janela de depuração](#debug-window) e colocará em negrito o texto do nome do arquivo para indicar isso (como o nome de arquivo do *devtools* está na ilustração acima). Em seguida, você pode definir pontos de interrupção nesse arquivo a partir da [janela de depuração](#debug-window).

![Seletor de recursos do depurador](./media/debugger_resource_picker.png)

No menu de contexto do *seletor de recursos* , você também pode marcar um arquivo como **código de biblioteca** ( `Ctrl+L` ), oferecendo a opção de [ignorar o código no depurador](#debug-window) e [ocultá-lo no painel **pilha de chamadas** ](#call-stack). Clicar (ou `Ctrl+L` ) novamente alternará o arquivo de volta para o valor anterior *my code* como código ou *código da biblioteca*.

### Pesquisa de arquivos

Use o comando *Find in Files* ( `Ctrl` + `Shift` + `F` ) quando você tiver uma cadeia de caracteres específica de código que você está tentando encontrar na fonte. A barra de ferramentas fornece opções de pesquisa diferentes, incluindo expressões regulares. Clicar em um resultado de pesquisa focalizará a *janela de depuração* no arquivo e na linha especificados.

![Painel pesquisa de arquivos do depurador](./media/debugger_file_search.png)

## Janela de depuração

A *janela de depuração* é onde você define seus pontos de interrupção, percorre o código e edita o script durante a depuração. Clique à esquerda de qualquer comando de script para adicionar (ou remover) um **ponto de interrupção**. Use o menu de contexto ou o painel de contexto do clique com o botão direito do mouse para *Adicionar uma condição* ao ponto [**de interrupção fornecendo**](#breakpoints) uma expressão lógica que faz com que o depurador seja interrompido se for avaliado como *verdadeiro* nesse local.

![Comandos da janela de depuração](./media/debugger_window.png)

Outros recursos da janela de depuração incluem controles para:

### 1. edição de código

Você pode editar o JavaScript ao vivo durante uma sessão de depuração. Depois de fazer as alterações, clique em <strong> Salvar </strong> ( `Ctrl+S` ) para testar as alterações na próxima vez que a seção do código for executada. Se você tiver alterações de código não salvas, um asterisco (\ *) será exibido antes do nome do arquivo na guia da *janela de depuração* .

Clique no botão **comparar documento com o original** para exibir a comparação do que você alterou.

![Modo de exibição diff do código editado no depurador](./media/debugger_edit_code.png)

Lembre-se das seguintes restrições:

- A edição de script funciona apenas em arquivos *. js* externos (e não inseridos `<script>` em *. html*)
- As edições são salvas na memória e liberadas quando o documento é recarregado, portanto, você não poderá executar edições dentro de um `DOMContentLoaded` manipulador, por exemplo
- No momento, não há nenhuma maneira (como a opção **salvar como** ) para salvar suas edições em disco a partir da devtools

### 2. formatação de código

Use esses controles para formatar o código minified para melhorar a legibilidade durante a depuração:

#### Superimposição ( `Ctrl+Shift+P` ) 
Adiciona quebras de linha e alinhamento de chaves por convenções JavaScript. Até mesmo código compactado que tenha sido tornado mais legível com essa opção pode ter função, seletor e nomes de variáveis muito diferentes dos em seu código-fonte original. Nesses casos, a opção [*alternar mapas de origem*](#source-maps) pode estar disponível.

#### Quebra automática de texto ( `Alt+W` )
Ajusta o código para caber nas margens atuais da janela de depuração (eliminando a necessidade de rolagem horizontal).

### 3. escopo de código

Você pode direcionar o depurador para ignorar certos arquivos com o botão **Marcar como código da biblioteca** ( `Ctrl+L` ). Por padrão, o botão [**depurar apenas meu código**](#toolbar) está ativado, o que significa que o depurador ignorará todos os arquivos que você marca como *código da biblioteca* e eles não aparecerão na [pilha de chamadas](#call-stack)do depurador. Ao pressionar o botão (**Marcar como meu código**), o `Ctrl+L` sinalizador será removido.

Para acompanhar bibliotecas em sessões de depuração, você pode editar esses arquivos para manter uma lista padrão ou adicionar caracteres curinga para um domínio ou tipo de arquivo:

```JavaScript
%APPDATA%\..\LocalLow\Microsoft\F12\header\MyCode.json and %APPDATA%\..\Local\Microsoft\F12\header\MyCode.json
```

#### Mapas de origem

Você verá o botão **alternar mapas de origem** habilitado para o código escrito em uma linguagem que é compilada em JavaScript ou CSS, que fornece um *mapa de origem* (um mapeamento de arquivo intermediário para a fonte original). Essa opção direciona o depurador a apresentar a fonte original para usar para depuração (em vez do arquivo compilado que está *realmente* sendo executado no navegador).

O DevTools verificará se o compilador que gerou o arquivo JavaScript incluía um comentário com o nome do arquivo de mapa. Por exemplo, se um compilador tiver compactado *MyFile. js* em *MyFile. min. min. js*, ele também pode gerar um arquivo de mapa, *MyFile. min. js. map* e incluir um comentário no arquivo compactado como este:

```JavaScript
//# sourceMappingURL=myfile.min.js.map
```

![Menu de contexto da guia Depurar arquivo](./media/debug_file_contextmenu.png)

Se o DevTools não conseguir localizar o mapa automaticamente, você pode escolher um mapa de origem para esse arquivo. Clique com o botão direito do mouse na guia do arquivo para localizar a opção **escolher mapa do código-fonte** . 

## Barra de ferramentas

Use a *barra de ferramentas* do depurador para controlar o modo de depurar o código e o código para percorrer ou ignorar. Aqui você também pode fazer uma pesquisa de texto completo em seus arquivos de código para cadeias de caracteres específicas.

![Barra de ferramentas do depurador](./media/debugger_toolbar.png)

### 1. Continue ( `F5` )/Break ( `Ctrl+Shift+B` )
 **Continue** ( `F5` ) continua a execução do código para o próximo ponto de interrupção. Se `F5` você se soltar, as quebras antigas serão removidas repetidamente até você liberá-la. 

 **Break** ( `Ctrl+Shift+B` ) entrará no depurador após executar a próxima instrução.

### 2. funções de etapa ( `F11` , `Ctrl+F10` , `Shift+F11` )
 **Step Into** ( `F11` ) etapas para a função que está sendo chamada. 

 **Step over** `Ctrl+F10` Etapas de passar sobre a função que estão sendo chamadas. 

 **Step Out** ( `Shift+F11` ) percorre a função atual e para a função de chamadas. 

 O depurador passará para a próxima instrução se não estiver em uma função quando esses comandos forem usados.

### 3. pausa no novo trabalhador ( `Ctrl+Shift+W` )
 Quebras na criação de um novo [trabalhador da Web](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers).

### 4. controle de exceção
**Alterar comportamento de exceção** ( `Ctrl+Shift+E` ) abre opções para alterar a forma como o depurador reage a exceções. Por padrão, exceções são ignoradas pelo depurador e conectadas ao [**console**](./console.md). Você pode optar por *interromper todas as exceções*ou apenas aquelas que não sejam manipuladas por `try...catch` instruções em seu código (*interromper em exceções sem tratamento*).

### 5. exibir resultados da pesquisa
(Atualmente desabilitado.) **Mostrar/ocultar resultados** alterna a exibição dos resultados da pesquisa [*localizar nos arquivos*](#6-find-in-files-ctrlf) .

### 6. localizar nos arquivos ( `Ctrl+F` )
 **Find in Files** ( `Ctrl+F` ) executa uma pesquisa de texto em todos os arquivos carregados dentro do [*seletor de recursos*](#resource-picker). Se o texto for encontrado, ele abrirá o primeiro arquivo correspondente à cadeia de caracteres de pesquisa. Pressionar `Enter` ou `F3` leva você para a próxima correspondência.

### 7. depurar apenas meu código ( `Ctrl+J` )
 **Depurar apenas meu código** ( `Ctrl+J` ) atua como uma alternância para incluir ou excluir todos os arquivos que foram marcados como [código de biblioteca](#3-code-scoping) enquanto você percorre o depurador.

### 8. conexão do depurador
O **depurador de desconexão/conexão** é essencialmente a opção de ativar/desativar para o depurador.

## Watch

Use o painel **inspeções** para procurar um catálogo de todos os objetos e variáveis (**locais**), tanto no escopo local quanto global, disponível para a instrução que é o foco da quebra atual no depurador.

![Painel inspeções](./media/debugger_watches.png)

Você pode acompanhar o valor de variáveis específicas à medida que elas passam e saem do escopo adicionando uma inspeção (**Adicionar inspeção**, `Ctrl+W` ) e modificar os valores editáveis clicando duas vezes nele ou selecionando **Editar valor** no menu de *contexto*. Limpe seus relógios usando os botões **excluir** ( `Ctrl+D` )/ **excluir tudo** ou do menu de contexto. 

## Detalhes

O painel de *detalhes* inclui as guias [**pilha de chamadas**](#call-stack), [**pontos de interrupção**](#breakpoints) e [**pontos de interrupção dom**](#dom-breakpoints) .

### Pilha de chamadas

A guia **pilha de chamadas** mostra a cadeia de funções que levaram ao ponto de execução atual. A função atual aparece na parte superior e as funções de chamada aparecem abaixo dela em ordem inversa.

![Painel de pilha de chamadas](./media/debugger_callstack.png)

O botão **Mostrar/ocultar quadros da biblioteca** ( `Ctrl+Shift+J` ) alterna a saída do [código da biblioteca](#3-code-scoping) da pilha de chamadas. Use a opção de **código de biblioteca** ( `Ctrl+L` ) no menu de *contexto* clique com o botão direito do mouse para marcar (ou desmarcar) a fonte do quadro selecionado como código de biblioteca. 

O botão **Mostrar/ocultar quadros assíncronos** alterna a exibição de raízes para chamadas de função assíncronas.

### Pontos de interrupção

Na guia **pontos de interrupção** , você pode gerenciar pontos de interrupção e tracepoints de evento, incluindo a configuração de condições, a desativação e a exclusão deles.

![Guia pontos de interrupção](./media/debugger_breakpoints.png)

Aqui está um resumo dos diferentes tipos de pontos de interrupção que você pode usar para depuração.

Tipo de ponto de interrupção | Descrição | Como configurá-lo
:------------ | :------------ | :--------
**Interrupção** | Quebra no depurador logo antes da linha especificada do código ser executada. Pontos de interrupção regulares são mais fáceis de definir se você tiver uma instrução por linha. | Na [janela depurar](#debug-window), clique na margem esquerda ao lado de qualquer número de linha no código. Um ponto vermelho é exibido e o ponto de interrupção é definido. Você pode saltar para a fonte de qualquer ponto de interrupção clicando em seu texto azul.
**Ponto de interrupção condicional** | Quebras se a condição especificada for avaliada como *verdadeira*. Isso é essencialmente um `if(condition)` para quebrar o depurador.  | Na guia [pontos de interrupção](#breakpoints) , passe o mouse sobre um ponto de interrupção existente e clique no botão "lápis" (*Adicionar uma condição a esse ponto de interrupção*), clique com o botão direito do mouse em um ponto de interrupção existente e selecione **condição...** no menu de contexto. Especifique a condição "se" a ser avaliada no local do ponto de interrupção. 
**Ponto de interrupção XMLHttpRequest** (w/condição opcional) | Quebras sempre que uma solicitação XMLHttpRequest (XHR) foi cumprida. Você pode inspecionar o `response` objeto XHR no painel [**inspeções**](#watches) . | Na guia [pontos de interrupção](#breakpoints) , clique no botão de *ponto de interrupção XMLHttpRequest* (círculo com setas para cima/para baixo). Você pode transformá-lo em um *ponto de interrupção condicional* , conforme descrito acima.
**Tracepoint de evento** | Chamadas [`console.log()`](./console/console-api.md#logging-custom-messages) com uma cadeia de caracteres especificada em resposta a um evento específico. Use isso para instruções temporárias de log do console que você não deseja salvar diretamente no código do manipulador de eventos. | Na guia [pontos de interrupção](#breakpoints) , clique no botão *tracepoint de evento* (losango com raio). Selecione um tipo de **evento** para o gatilho e uma instrução de **rastreamento** para registro em log.
**Ponto de interrupção de evento** (c/condição opcional) | Quebras sempre que um evento especificado é acionado. | Na guia [pontos de interrupção](#breakpoints) , clique no botão de *ponto de interrupção de evento* (círculo com raio). Selecione um tipo de **evento** para o gatilho e, opcionalmente, especifique uma instrução de **condição** . 
**Ponto de interrupção DOM** | Quebras sempre que um elemento especificado na página é modificado, como quando sua subárvore é modificada, seus atributos mudam ou quando ele é desanexado do DOM. | Na guia [elementos](./elements/dom-breakpoints.md) , clique com o botão direito do mouse em um elemento de origem e selecione uma das opções de *pontos de interrupção do dom* . Use a guia [**pontos de interrupção dom**](#dom-breakpoints) nos painéis de *depurador* ou *elementos* para gerenciar seus pontos de interrupção. 

Os pontos de interrupção condicionais e tracepoints têm acesso a todas as variáveis locais e globais no escopo quando elas falham no depurador.

### Pontos de interrupção DOM

Gerencie seus pontos de interrupção de mutação DOM na guia **pontos de interrupção dom** , incluindo desabilitar, excluir e revinculá-los.  Os [pontos de interrupção dom podem ser definidos](./elements/dom-breakpoints.md) a partir do *modo de exibição de árvore HTML* no painel de **elementos** .

![Guia pontos de interrupção DOM](./media/debugger_dom_breakpoints.png)

A guia *pontos de interrupção dom* no **depurador** fornece funcionalidade equivalente à guia *pontos de interrupção do dom** no painel de **elementos** .

Veja mais sobre os diferentes tipos de [pontos de interrupção dom](./elements/dom-breakpoints.md).

## Teclado

### Atalhos da barra de ferramentas

Ação | Atalho
:------------ | :-------------
Localizar | `Ctrl` + `F`
Continuar (a partir do ponto de interrupção) | `F5` ou `F8`
Continuação rápida | Segure `F5` ou `F8`
Continuar e atualizar | `Ctrl` + `Shift` + `F5`
Condicional | `Ctrl` + `Shift` + `B`
Depuração | `F11`
Depuração de cima | `F10`
Depurar | `Shift` + `F11`
Interromper no novo trabalhador | `Ctrl` + `Shift` + `W`
Alterar comportamento de exceção (menu de abertura) | `Ctrl` + `Shift` + `E`
Depurar apenas meu código | `Ctrl` + `J`

### Atalhos do seletor de recursos

Ação | Atalho
:------------ | :-------------
Marcar como código do meu código/biblioteca | `Ctrl` + `L`
Abrir arquivo | `Ctrl` + `O`, `Ctrl` + `P`
Pesquisar todos os arquivos | `Ctrl` + `Shift` + `F`

### Atalhos da janela depurar

Ação | Atalho
:------------ | :-------------
Remover ponto de interrupção | `F9`
Desabilitar ponto de interrupção | `Ctrl` + `F9`
Ponto de interrupção condicional... | `Alt` + `F9`
Copiar | `Ctrl` + `C`
Salvar | `Ctrl` + `S`
Ir para a linha... | `Ctrl` + `G`
Mostrar próxima instrução | `Alt` + `Num` + `*`
Executar até o cursor | `Ctrl` + `F10`
Definir a próxima instrução | `Ctrl` + `Shift` + `F10`
Mostrar no seletor de arquivos | `Ctrl` + `Alt` + `P`
Vá para definição em arquivo | `Ctrl`+`D`
Localizar referências no arquivo | `Ctrl` + `Shift` + `D`
Impressão bonita | `Ctrl` + `Shift` + `P`
Quebra automática de texto | `Alt` + `W`
Marcar como código do meu código/biblioteca | `Ctrl` + `L`
Desabilitar/habilitar guias no editor. **Observação:** se você estiver usando o teclado para navegar no depurador, não poderá sair do editor até desabilitar a tecla Tab | `Ctrl` + `M`

### Atalhos para o painel inspeções

Ação | Atalho
:------------ | :-------------
Adicionar inspeção | `Ctrl` + `W`
Excluir inspeção | `Ctrl` + `D`

### Atalhos para o painel de detalhes

| Ação                             | Atalho                 |
|:-----------------------------------|:-------------------------|
| Mostrar/ocultar quadros do código da biblioteca | `Ctrl` + `Shift` + `J`   |
| Habilitar todos os pontos de interrupção             | `Ctrl` + `Shift` + `F11` |
