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
# <a name="debug-errors-reported-in-console"></a><span data-ttu-id="79213-104">Erros de depuração relatados no Console</span><span class="sxs-lookup"><span data-stu-id="79213-104">Debug errors reported in Console</span></span>  

<span data-ttu-id="79213-105">A primeira experiência que você tem com **o Console** provavelmente é um erro em um script.</span><span class="sxs-lookup"><span data-stu-id="79213-105">The first experience you have with the **Console** is probably an error in a script.</span></span>  <span data-ttu-id="79213-106">Para experimentar, navegue até [JavaScript erro relatado na ferramenta Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].</span><span class="sxs-lookup"><span data-stu-id="79213-106">To try it, navigate to [JavaScript error reported in the Console tool][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].</span></span>  

<span data-ttu-id="79213-107">Se você abrir o DevTools no navegador, um botão na parte superior direita exibirá um erro para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="79213-107">If you open DevTools in the browser, a button on the top right displays an error for the webpage.</span></span>  
<span data-ttu-id="79213-108">Escolha o botão para levá-lo ao **Console** e lhe dar mais informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="79213-108">Choose the button to take you to the **Console** and give you more information about the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="O DevTools fornece informações detalhadas sobre o erro no Console" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="79213-110">O DevTools fornece informações detalhadas sobre o erro no **Console**</span><span class="sxs-lookup"><span data-stu-id="79213-110">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="79213-111">A partir das informações, você pode coletar que o erro está na linha 16 do `error.html` arquivo.</span><span class="sxs-lookup"><span data-stu-id="79213-111">From the information, you may gather that the error is on line 16 of the `error.html` file.</span></span>  <span data-ttu-id="79213-112">Se você escolher o link à direita do Console , ele o leva para a ferramenta Fontes e realça a linha `error.html:16` de código com o erro. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="79213-112">If you choose the `error.html:16` link on the right of the **Console**, it takes you to the **Sources** tool and highlights the line of code with the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="A ferramenta Sources realça a linha de código que causa o erro" lightbox="../media/console-debug-displays-in-sources.msft.png":::
   <span data-ttu-id="79213-114">A **ferramenta Sources** realça a linha de código que causa o erro</span><span class="sxs-lookup"><span data-stu-id="79213-114">The **Sources** tool highlights the line of code that causes the error</span></span>  
:::image-end:::  

<span data-ttu-id="79213-115">O script tenta obter o primeiro `h2` elemento do documento e pintar uma borda vermelha ao redor dele.</span><span class="sxs-lookup"><span data-stu-id="79213-115">The script tries to get the first `h2` element in the document and paint a red border around it.</span></span>  <span data-ttu-id="79213-116">Mas nenhum `h2` elemento existe, portanto, o script falha.</span><span class="sxs-lookup"><span data-stu-id="79213-116">But no `h2` element exists, so the script fails.</span></span>  

## <a name="find-and-debug-network-issues"></a><span data-ttu-id="79213-117">Encontrar e depurar problemas de rede</span><span class="sxs-lookup"><span data-stu-id="79213-117">Find and debug network issues</span></span>  

<span data-ttu-id="79213-118">Outros erros que o **Console** relata são erros de rede.</span><span class="sxs-lookup"><span data-stu-id="79213-118">Other errors that the **Console** reports are network errors.</span></span>  <span data-ttu-id="79213-119">Para exibi-lo em ação, navegue até o [erro de rede relatado no Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].</span><span class="sxs-lookup"><span data-stu-id="79213-119">To display it in action, navigate to the [Network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="Console exibe um erro Network e JavaScript" lightbox="../media/console-debug-network-error.msft.png":::
   <span data-ttu-id="79213-121">**Console** exibe um erro Network e JavaScript</span><span class="sxs-lookup"><span data-stu-id="79213-121">**Console** displays a Network and a JavaScript error</span></span>  
:::image-end:::  

<span data-ttu-id="79213-122">A tabela exibe `loading` , mas nada muda na página da Web porque os dados nunca são recuperados.</span><span class="sxs-lookup"><span data-stu-id="79213-122">The table displays `loading`, but nothing changes on the webpage because the data is never retrieved.</span></span>  <span data-ttu-id="79213-123">No **Console**, os dois erros a seguir ocorreram.</span><span class="sxs-lookup"><span data-stu-id="79213-123">In the **Console**, the following two errors occurred.</span></span>  

*   <span data-ttu-id="79213-124">Um erro de rede que começa com `GET` o método HTTP seguido por um URI.</span><span class="sxs-lookup"><span data-stu-id="79213-124">A network error that starts with `GET` HTTP method followed by a URI.</span></span>  
*   <span data-ttu-id="79213-125">Um `Uncaught (in promise) TypeError: data.forEach is not a function` erro.</span><span class="sxs-lookup"><span data-stu-id="79213-125">An `Uncaught (in promise) TypeError: data.forEach is not a function` error.</span></span>  
    
<span data-ttu-id="79213-126">Se você escolher o `network-error.html:40` link no **Console**, o DevTools o leva para a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="79213-126">If you choose the `network-error.html:40` link in the **Console**, DevTools takes you to the **Sources** tool.</span></span>  <span data-ttu-id="79213-127">A linha problemática do código é realçada e seguida por `error` um `x` botão \(\).</span><span class="sxs-lookup"><span data-stu-id="79213-127">The problematic line of code is highlighted and followed by an `error` \(`x`\) button.</span></span>  <span data-ttu-id="79213-128">Para exibir a `Failed to load resource: the server responded with a status of 404 ()` mensagem de erro, escolha **o botão** erro \( `x` \) .</span><span class="sxs-lookup"><span data-stu-id="79213-128">To display the `Failed to load resource: the server responded with a status of 404 ()` error message, choose the **error** \(`x`\) button.</span></span>  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Escolha o link para a página da Web e o código onde ocorre o erro abre a ferramenta Sources" lightbox="../media/console-debug-network-error-code-line.msft.png":::
         <span data-ttu-id="79213-130">Escolha o link para a página da Web e o código onde ocorre o erro abre a **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="79213-130">Choose the link to the webpage and code where the error occurs line opens the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Para encontrar o erro em JavaScript, use a ferramenta Sources" lightbox="../media/console-debug-network-error-sources.msft.png":::
         <span data-ttu-id="79213-132">Para encontrar o erro em JavaScript, use a **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="79213-132">To find the error in JavaScript, use the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="79213-133">No exemplo, o erro informa que a URL solicitada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="79213-133">In the example, the error informs you that the requested URL isn't found.</span></span>  <span data-ttu-id="79213-134">Em seguida, conclua as seguintes ações para abrir a **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="79213-134">Next, complete the following actions to open the **Network** tool.</span></span>  

1.  <span data-ttu-id="79213-135">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="79213-135">Open the **Console**.</span></span>  
1.  <span data-ttu-id="79213-136">Escolha o URI associado ao erro.</span><span class="sxs-lookup"><span data-stu-id="79213-136">Choose the URI associated with the error.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="Console exibe um código de status HTTP do erro depois que um recurso não é carregado" lightbox="../media/console-debug-network-error-url.msft.png":::
   <span data-ttu-id="79213-138">**Console** exibe um código de status HTTP do erro depois que um recurso não é carregado</span><span class="sxs-lookup"><span data-stu-id="79213-138">**Console** displays an HTTP status code of the error after a resource isn't loaded</span></span>  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="A ferramenta Rede exibe mais informações sobre a solicitação com falha" lightbox="../media/console-debug-network-error-network.msft.png":::
           <span data-ttu-id="79213-140">A **ferramenta Rede** exibe mais informações sobre a solicitação com falha</span><span class="sxs-lookup"><span data-stu-id="79213-140">The **Network** tool displays more information about the failed request</span></span>  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="Inspecionar os headers na ferramenta Rede pode dar mais informações" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           <span data-ttu-id="79213-142">Inspecionar os headers na **ferramenta Rede** pode dar mais informações</span><span class="sxs-lookup"><span data-stu-id="79213-142">Inspect the headers in the **Network** tool may give more insight</span></span>  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="79213-143">Qual era o problema?</span><span class="sxs-lookup"><span data-stu-id="79213-143">What was the problem?</span></span>  <span data-ttu-id="79213-144">Dois caracteres de barra \( `//` \) ocorrem no URI solicitado após a palavra `repos` .</span><span class="sxs-lookup"><span data-stu-id="79213-144">Two slash characters \(`//`\) occur in the requested URI after the word `repos`.</span></span>  <span data-ttu-id="79213-145">Abra a **ferramenta Sources** e inspecione a linha 26.</span><span class="sxs-lookup"><span data-stu-id="79213-145">Open the **Sources** tool and inspect line 26.</span></span>  <span data-ttu-id="79213-146">Um caractere de barra à frente \( \) ocorre `/` no final do URI base.</span><span class="sxs-lookup"><span data-stu-id="79213-146">A trailing slash character \(`/`\) occurs at the end of the base URI.</span></span>  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="A ferramenta Sources exibe a linha de código com o erro" lightbox="../media/console-debug-network-error-code-error.msft.png":::
   <span data-ttu-id="79213-148">A **ferramenta Sources** exibe a linha de código com o erro</span><span class="sxs-lookup"><span data-stu-id="79213-148">The **Sources** tool displays the line of code with the error</span></span>  
:::image-end:::  

<span data-ttu-id="79213-149">Para revisar nenhum erro no **Console,** navegue até Erro de rede fixo [relatado no Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span><span class="sxs-lookup"><span data-stu-id="79213-149">To review no errors in the **Console**, navigate to [Fixed network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="O exemplo sem erros carrega informações do GitHub e as exibe" lightbox="../media/console-debug-network-error-fixed.msft.png":::
   <span data-ttu-id="79213-151">O exemplo sem erros carrega informações do GitHub e as exibe</span><span class="sxs-lookup"><span data-stu-id="79213-151">The example without any errors loads information from GitHub and displays it</span></span>  
:::image-end:::  

<span data-ttu-id="79213-152">Certifique-se de fornecer técnicas de codificação defensiva para evitar as experiências anteriores do usuário.</span><span class="sxs-lookup"><span data-stu-id="79213-152">Ensure you provide defensive coding techniques to avoid the previous user experiences.</span></span>  <span data-ttu-id="79213-153">Além disso, verifique se seu código captura erros e exibe cada um deles no **Console**.</span><span class="sxs-lookup"><span data-stu-id="79213-153">Also, ensure your code catches errors and display each in the **Console**.</span></span>  <span data-ttu-id="79213-154">Navegue [até Relatório de erros de rede no Console e na interface do][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] usuário e revise os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="79213-154">Navigate to [Network error reporting in Console and UI][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] and review the following items.</span></span>  

*   <span data-ttu-id="79213-155">Forneça a interface do usuário ao usuário que algo deu errado.</span><span class="sxs-lookup"><span data-stu-id="79213-155">Provide UI to the user that something went wrong.</span></span>  
*   <span data-ttu-id="79213-156">No **Console**, forneça informações úteis sobre o erro de rede do seu código.</span><span class="sxs-lookup"><span data-stu-id="79213-156">In the **Console**, provide helpful information about the Network error from your code.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Um exemplo que captura e relata erros" lightbox="../media/console-debug-network-error-report.msft.png":::
   <span data-ttu-id="79213-158">Um exemplo que captura e relata erros</span><span class="sxs-lookup"><span data-stu-id="79213-158">An example that catches and reports errors</span></span>  
:::image-end:::  

<span data-ttu-id="79213-159">O trecho de código a seguir captura e relata erros usando o `handleErrors` método, especificamente a `throw Error` linha.</span><span class="sxs-lookup"><span data-stu-id="79213-159">The following code snippet catches and reports errors using the `handleErrors` method, specifically the `throw Error` line.</span></span>  

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

## <a name="create-errors-and-traces-in-the-console"></a><span data-ttu-id="79213-160">Criar erros e rastreamentos no Console</span><span class="sxs-lookup"><span data-stu-id="79213-160">Create errors and traces in the Console</span></span>

<span data-ttu-id="79213-161">Além do exemplo na seção anterior, você também pode criar erros diferentes e `throw Error` rastrear problemas no **Console**.</span><span class="sxs-lookup"><span data-stu-id="79213-161">Besides the `throw Error` example in the previous section, you may also create different errors and trace problems in the **Console**.</span></span>  
<span data-ttu-id="79213-162">Para exibir duas mensagens de erro criadas no **Console,** navegue até Criar relatórios de erro [e declarações no Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].</span><span class="sxs-lookup"><span data-stu-id="79213-162">To display two created error messages in the **Console**, navigate to [Creating error reports and assertions in Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].</span></span>  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Mensagens de erro criadas do Console" lightbox="../media/console-debug-error-assert.msft.png":::
   <span data-ttu-id="79213-164">Mensagens de erro criadas do **Console**</span><span class="sxs-lookup"><span data-stu-id="79213-164">Error messages created from **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="79213-165">O trecho de código a seguir foi usado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="79213-165">The following code snippet was used in the previous example.</span></span>  

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

<span data-ttu-id="79213-166">Você tem três funções que solicitam umas às outras em sucessão.</span><span class="sxs-lookup"><span data-stu-id="79213-166">You have three functions that request each other in succession.</span></span>  

*   `first()`  
*   `second()`  
*   `third()`  
    
<span data-ttu-id="79213-167">Cada um envia `name` um argumento para o outro.</span><span class="sxs-lookup"><span data-stu-id="79213-167">Each sends a `name` argument to the other.</span></span>  <span data-ttu-id="79213-168">Na função, você verifica se o argumento existe e, se não, registra um erro que `third()` o nome não está `name` definido.</span><span class="sxs-lookup"><span data-stu-id="79213-168">In the `third()` function, you check if the `name` argument exists and if it doesn't, you log an error that name isn't defined.</span></span>  <span data-ttu-id="79213-169">Se `name` estiver definido, use o método `assert()` para verificar se o argumento tem menos de oito `name` letras.</span><span class="sxs-lookup"><span data-stu-id="79213-169">If `name` is defined, you use the `assert()` method to check if the `name` argument is fewer than eight letters long.</span></span>  <span data-ttu-id="79213-170">Você solicita a `first()` função três vezes, com os seguintes parâmetros.</span><span class="sxs-lookup"><span data-stu-id="79213-170">You request the `first()` function three times, with the following parameters.</span></span>  

*   <span data-ttu-id="79213-171">Nenhum argumento que aciona `console.error()` o método na `third()` função.</span><span class="sxs-lookup"><span data-stu-id="79213-171">No argument that triggers the `console.error()` method in the `third()` function.</span></span>  
*   <span data-ttu-id="79213-172">O termo como um parâmetro para a função não causa um erro porque o argumento existe e é `Console` `first()` menor que oito `name` letras.</span><span class="sxs-lookup"><span data-stu-id="79213-172">The term `Console` as a parameter to the `first()` function doesn't cause an error because `name` argument exists and is shorter than eight letters.</span></span>  
*   <span data-ttu-id="79213-173">A frase como um parâmetro a funcionar faz com que `Microsoft Edge Canary` `first()` o método reporte um erro, pois o parâmetro `console.assert()` tem mais de oito letras.</span><span class="sxs-lookup"><span data-stu-id="79213-173">The phrase `Microsoft Edge Canary` as a parameter to `first()` function causes the `console.assert()` method to report an error, because the parameter is longer than eight letters.</span></span>  
    
<span data-ttu-id="79213-174">Use o `console.assert()` método para criar relatórios de erro condicional.</span><span class="sxs-lookup"><span data-stu-id="79213-174">Use the `console.assert()` method to create conditional error reports.</span></span>  <span data-ttu-id="79213-175">Os dois exemplos a seguir têm o mesmo resultado, mas um precisa de uma `if{}` instrução extra.</span><span class="sxs-lookup"><span data-stu-id="79213-175">The following two examples have the same result, but one needs an extra `if{}` statement.</span></span>  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> <span data-ttu-id="79213-176">A segunda e a terceira linhas do código executam o mesmo teste.</span><span class="sxs-lookup"><span data-stu-id="79213-176">The second and third lines of the code perform the same test.</span></span>  <span data-ttu-id="79213-177">Como a afirmação precisa registrar um resultado negativo, teste para no `x < 40` caso e para a `if` `x >= 40` afirmação.</span><span class="sxs-lookup"><span data-stu-id="79213-177">Because the assertion needs to record a negative result, you test for `x < 40` in the `if` case and `x >= 40` for the assertion.</span></span>  

<span data-ttu-id="79213-178">Se você não tiver certeza de qual função solicita outra função, use o método para rastrear quais funções são solicitadas para chegar `console.trace()` à função atual.</span><span class="sxs-lookup"><span data-stu-id="79213-178">If you aren't sure which function requests another function, use the `console.trace()` method to track which functions are requested to get to the current one.</span></span>  <span data-ttu-id="79213-179">Para exibir o rastreamento no **Console,** navegue até [Criar rastreamentos no Console][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].</span><span class="sxs-lookup"><span data-stu-id="79213-179">To display the trace in the **Console**, navigate to [Creating traces in Console][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].</span></span>  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

<span data-ttu-id="79213-180">O resultado é um rastreamento a ser exibido que é `here()` nomeado e, em seguida, e no segundo exemplo chamado `there()` `everywhere()` `everywhere()` .</span><span class="sxs-lookup"><span data-stu-id="79213-180">The result is a trace to display that `here()` is named `there()` and then `everywhere()` and in the second example that it's named `everywhere()`.</span></span>  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Um rastreamento criado a partir do Console" lightbox="../media/console-debug-trace.msft.png":::
   <span data-ttu-id="79213-182">Um rastreamento criado a partir do **Console**</span><span class="sxs-lookup"><span data-stu-id="79213-182">A trace created from **Console**</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="79213-183">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="79213-183">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Erro JavaScript relatado na ferramenta console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Criação de relatórios de erro e declarações no Console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Erro de rede relatado no Console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "Erro de rede corrigido relatado no Console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Relatório de erros de rede no Console e na interface do usuário | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Criando rastreamentos no Console | GitHub"  
