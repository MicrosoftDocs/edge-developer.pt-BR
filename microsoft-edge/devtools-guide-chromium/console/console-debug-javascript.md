---
description: Erros javaScript são relatados por ferramentas de desenvolvedor e depurar cada uma delas no Console
title: Rastrear erros usando o Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483286"
---
# <a name="debug-errors-reported-in-console"></a>Erros de depuração relatados no Console  

A primeira experiência que você tem com **o Console** provavelmente é um erro em um script.  Para experimentar, navegue até [JavaScript erro relatado na ferramenta Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].  

Se você abrir o DevTools no navegador, um botão na parte superior direita exibirá um erro para a página da Web.  
Escolha o botão para levá-lo ao **Console** e lhe dar mais informações sobre o erro.  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="O DevTools fornece informações detalhadas sobre o erro no Console" lightbox="../media/console-debug-displays-error.msft.png":::
   O DevTools fornece informações detalhadas sobre o erro no **Console**  
:::image-end:::  

A partir das informações, você pode coletar que o erro está na linha 16 do `error.html` arquivo.  Se você escolher o link à direita do Console , ele o leva para a ferramenta Fontes e realça a linha `error.html:16` de código com o erro. **** ****  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="A ferramenta Sources realça a linha de código que causa o erro" lightbox="../media/console-debug-displays-in-sources.msft.png":::
   A **ferramenta Sources** realça a linha de código que causa o erro  
:::image-end:::  

O script tenta obter o primeiro `h2` elemento do documento e pintar uma borda vermelha ao redor dele.  Mas nenhum `h2` elemento existe, portanto, o script falha.  

## <a name="find-and-debug-network-issues"></a>Encontrar e depurar problemas de rede  

Outros erros que o **Console** relata são erros de rede.  Para exibi-lo em ação, navegue até o [erro de rede relatado no Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="Console exibe um erro Network e JavaScript" lightbox="../media/console-debug-network-error.msft.png":::
   **Console** exibe um erro Network e JavaScript  
:::image-end:::  

A tabela exibe `loading` , mas nada muda na página da Web porque os dados nunca são recuperados.  No **Console**, os dois erros a seguir ocorreram.  

*   Um erro de rede que começa com `GET` o método HTTP seguido por um URI.  
*   Um `Uncaught (in promise) TypeError: data.forEach is not a function` erro.  
    
Se você escolher o `network-error.html:40` link no **Console**, o DevTools o leva para a **ferramenta Fontes.**  A linha problemática do código é realçada e seguida por `error` um `x` botão \(\).  Para exibir a `Failed to load resource: the server responded with a status of 404 ()` mensagem de erro, escolha **o botão** erro \( `x` \) .  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Escolha o link para a página da Web e o código onde ocorre o erro abre a ferramenta Sources" lightbox="../media/console-debug-network-error-code-line.msft.png":::
         Escolha o link para a página da Web e o código onde ocorre o erro abre a **ferramenta Sources**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Para encontrar o erro em JavaScript, use a ferramenta Sources" lightbox="../media/console-debug-network-error-sources.msft.png":::
         Para encontrar o erro em JavaScript, use a **ferramenta Sources**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

No exemplo, o erro informa que a URL solicitada não foi encontrada.  Em seguida, conclua as seguintes ações para abrir a **ferramenta Rede.**  

1.  Abra o **Console**.  
1.  Escolha o URI associado ao erro.  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="Console exibe um código de status HTTP do erro depois que um recurso não é carregado" lightbox="../media/console-debug-network-error-url.msft.png":::
   **Console** exibe um código de status HTTP do erro depois que um recurso não é carregado  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="A ferramenta Rede exibe mais informações sobre a solicitação com falha" lightbox="../media/console-debug-network-error-network.msft.png":::
           A **ferramenta Rede** exibe mais informações sobre a solicitação com falha  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="Inspecionar os headers na ferramenta Rede pode dar mais informações" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           Inspecionar os headers na **ferramenta Rede** pode dar mais informações  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

Qual era o problema?  Dois caracteres de barra \( `//` \) ocorrem no URI solicitado após a palavra `repos` .  Abra a **ferramenta Sources** e inspecione a linha 26.  Um caractere de barra à frente \( \) ocorre `/` no final do URI base.  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="A ferramenta Sources exibe a linha de código com o erro" lightbox="../media/console-debug-network-error-code-error.msft.png":::
   A **ferramenta Sources** exibe a linha de código com o erro  
:::image-end:::  

Para revisar nenhum erro no **Console,** navegue até Erro de rede fixo [relatado no Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="O exemplo sem erros carrega informações de GitHub e as exibe" lightbox="../media/console-debug-network-error-fixed.msft.png":::
   O exemplo sem erros carrega informações de GitHub e as exibe  
:::image-end:::  

Certifique-se de fornecer técnicas de codificação defensiva para evitar as experiências anteriores do usuário.  Além disso, verifique se seu código captura erros e exibe cada um deles no **Console**.  Navegue [até Relatório de erros de rede no Console e na interface do][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] usuário e revise os itens a seguir.  

*   Forneça a interface do usuário ao usuário que algo deu errado.  
*   No **Console**, forneça informações úteis sobre o erro de rede do seu código.  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Um exemplo que captura e relata erros" lightbox="../media/console-debug-network-error-report.msft.png":::
   Um exemplo que captura e relata erros  
:::image-end:::  

O trecho de código a seguir captura e relata erros usando o `handleErrors` método, especificamente a `throw Error` linha.  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a>Criar erros e rastreamentos no Console

Além do exemplo na seção anterior, você também pode criar erros diferentes e `throw Error` rastrear problemas no **Console**.  
Para exibir duas mensagens de erro criadas no **Console,** navegue até Criar relatórios de erro [e declarações no Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Mensagens de erro criadas do Console" lightbox="../media/console-debug-error-assert.msft.png":::
   Mensagens de erro criadas do **Console**  
:::image-end:::  

O trecho de código a seguir foi usado no exemplo anterior.  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

Você tem três funções que solicitam umas às outras em sucessão.  

*   `first()`  
*   `second()`  
*   `third()`  
    
Cada um envia `name` um argumento para o outro.  Na função, você verifica se o argumento existe e, se não, registra um erro que `third()` o nome não está `name` definido.  Se `name` estiver definido, use o método `assert()` para verificar se o argumento tem menos de oito `name` letras.  Você solicita a `first()` função três vezes, com os seguintes parâmetros.  

*   Nenhum argumento que aciona `console.error()` o método na `third()` função.  
*   O termo como um parâmetro para a função não causa um erro porque o argumento existe e é `Console` `first()` menor que oito `name` letras.  
*   A frase como um parâmetro a funcionar faz com que `Microsoft Edge Canary` `first()` o método reporte um erro, pois o parâmetro `console.assert()` tem mais de oito letras.  
    
Use o `console.assert()` método para criar relatórios de erro condicional.  Os dois exemplos a seguir têm o mesmo resultado, mas um precisa de uma `if{}` instrução extra.  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> A segunda e a terceira linhas do código executam o mesmo teste.  Como a afirmação precisa registrar um resultado negativo, teste para no `x < 40` caso e para a `if` `x >= 40` afirmação.  

Se você não tiver certeza de qual função solicita outra função, use o método para rastrear quais funções são solicitadas para chegar `console.trace()` à função atual.  Para exibir o rastreamento no **Console,** navegue até [Criar rastreamentos no Console][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

O resultado é um rastreamento a ser exibido que é `here()` nomeado e, em seguida, e no segundo exemplo chamado `there()` `everywhere()` `everywhere()` .  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Um rastreamento criado a partir do Console" lightbox="../media/console-debug-trace.msft.png":::
   Um rastreamento criado a partir do **Console**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Erro JavaScript relatado na ferramenta console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Criação de relatórios de erro e declarações no Console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Erro de rede relatado no Console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "Erro de rede corrigido relatado no Console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Relatório de erros de rede no Console e na interface do usuário | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Criando rastreamentos no Console | GitHub"  
