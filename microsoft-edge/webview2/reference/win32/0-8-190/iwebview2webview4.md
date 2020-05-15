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
ms.openlocfilehash: 6ebed9e61bf7eda60e6e16b7a417306baa5d07bf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652351"
---
# <span data-ttu-id="129b2-104">interface IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="129b2-104">interface IWebView2WebView4</span></span> 

> [!NOTE]
> <span data-ttu-id="129b2-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="129b2-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="129b2-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="129b2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

<span data-ttu-id="129b2-107">Funcionalidades adicionais implementadas pelo objeto WebView primário.</span><span class="sxs-lookup"><span data-stu-id="129b2-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="129b2-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="129b2-108">Summary</span></span>

 <span data-ttu-id="129b2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="129b2-109">Members</span></span>                        | <span data-ttu-id="129b2-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="129b2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="129b2-111">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="129b2-111">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="129b2-112">Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="129b2-112">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="129b2-113">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="129b2-113">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="129b2-114">Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.</span><span class="sxs-lookup"><span data-stu-id="129b2-114">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="129b2-115">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="129b2-115">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="129b2-116">Abre a janela do DevTools para o documento atual no WebView.</span><span class="sxs-lookup"><span data-stu-id="129b2-116">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="129b2-117">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="129b2-117">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="129b2-118">Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="129b2-118">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="129b2-119">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="129b2-119">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="129b2-120">Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="129b2-120">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="129b2-121">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="129b2-121">WEBVIEW2_KEY_EVENT_TYPE</span></span>](#webview2_key_event_type) | <span data-ttu-id="129b2-122">O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="129b2-122">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="129b2-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="129b2-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#webview2_physical_key_status) | <span data-ttu-id="129b2-124">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="129b2-124">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="129b2-125">Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="129b2-125">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="129b2-126">Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="129b2-126">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="129b2-127">Parte</span><span class="sxs-lookup"><span data-stu-id="129b2-127">Members</span></span>

#### <span data-ttu-id="129b2-128">Addremoteobject</span><span class="sxs-lookup"><span data-stu-id="129b2-128">AddRemoteObject</span></span> 

<span data-ttu-id="129b2-129">Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="129b2-129">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="129b2-130">Public HRESULT [Addremoteobject](#addremoteobject)(nome do LPCWSTR, objeto Variant \*)</span><span class="sxs-lookup"><span data-stu-id="129b2-130">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="129b2-131">Os objetos de host são expostos como proxies de objeto remoto via `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="129b2-131">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="129b2-132">Proxies de objeto remoto são promessas e serão resolvidos para um objeto que representa o objeto host.</span><span class="sxs-lookup"><span data-stu-id="129b2-132">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="129b2-133">A promessa será recusada se o aplicativo não adicionar um objeto com o nome.</span><span class="sxs-lookup"><span data-stu-id="129b2-133">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="129b2-134">Quando o código JavaScript acessa uma propriedade ou método do objeto, uma promessa é retornada, que será resolvida para o valor retornado do host para a propriedade ou método, ou recusada em caso de erro, pois não há tal propriedade ou método no objeto ou parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="129b2-134">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="129b2-135">Por exemplo, quando o código do aplicativo faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="129b2-135">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="129b2-136">O código JavaScript na WebView poderá acessar o appObject da seguinte forma e, em seguida, acessar atributos e métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="129b2-136">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="129b2-137">Observe que, enquanto tipos simples, IDispatch e matriz são compatíveis, IUnknown Generic, VT_DECIMAL ou Variant VT_RECORD não é suportada.</span><span class="sxs-lookup"><span data-stu-id="129b2-137">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="129b2-138">Objetos JavaScript remotos como funções de retorno de chamada são representados como uma variante VT_DISPATCH com o objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="129b2-138">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="129b2-139">O método de retorno de chamada JavaScript pode ser invocado usando DISPID_VALUE para o DISPID.</span><span class="sxs-lookup"><span data-stu-id="129b2-139">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="129b2-140">Há suporte para matrizes aninhadas até uma profundidade de 3.</span><span class="sxs-lookup"><span data-stu-id="129b2-140">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="129b2-141">Matrizes de tipos de referência não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="129b2-141">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="129b2-142">VT_EMPTY e VT_NULL são mapeados para JavaScript como nulo.</span><span class="sxs-lookup"><span data-stu-id="129b2-142">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="129b2-143">Em JavaScript nulo e indefinido são mapeados para VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="129b2-143">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="129b2-144">Além disso, todos os objetos remotos são expostos como `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="129b2-144">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="129b2-145">Aqui, os objetos do host são expostos como proxies síncronos de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-145">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="129b2-146">Elas não são promessas e chamadas para funções ou acesso à propriedade o bloqueio síncrono de script em execução, aguardando a comunicação de processo cruzado para o código do host ser executado.</span><span class="sxs-lookup"><span data-stu-id="129b2-146">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="129b2-147">Portanto, isso pode resultar em problemas de confiabilidade e é recomendável que você use a API assíncrona baseada em promessa `window.chrome.webview.remoteObjects.<name>` descrita acima.</span><span class="sxs-lookup"><span data-stu-id="129b2-147">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="129b2-148">Proxies de objetos remotos síncronos e proxies de objeto remoto assíncrono podem proxy para o mesmo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-148">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="129b2-149">As alterações remotas feitas por um proxy serão refletidas em qualquer outro proxy do mesmo objeto remoto, seja os outros proxies e síncronos ou assíncronos.</span><span class="sxs-lookup"><span data-stu-id="129b2-149">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="129b2-150">Embora o JavaScript seja bloqueado em uma chamada síncrona para o código nativo, esse código nativo não pode retornar a chamada para JavaScript.</span><span class="sxs-lookup"><span data-stu-id="129b2-150">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="129b2-151">As tentativas de fazer isso falharão com o HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="129b2-151">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="129b2-152">Proxies de objeto remoto são objetos de proxy JavaScript que interceptam todas as invocações de propriedade, conjunto de propriedades e invocação de propriedade.</span><span class="sxs-lookup"><span data-stu-id="129b2-152">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="129b2-153">Propriedades ou métodos que fazem parte da função ou do protótipo do objeto são executados localmente.</span><span class="sxs-lookup"><span data-stu-id="129b2-153">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="129b2-154">Além disso, qualquer propriedade ou método na matriz `chrome.webview.remoteObjects.options.forceLocalProperties` também será executado localmente.</span><span class="sxs-lookup"><span data-stu-id="129b2-154">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="129b2-155">Isso assume como padrão os métodos opcionais que têm significado em JavaScript como `toJSON` e `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="129b2-155">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="129b2-156">Você pode adicionar mais à matriz, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="129b2-156">You can add more to this array as required.</span></span>

<span data-ttu-id="129b2-157">Há um método `chrome.webview.remoteObjects.cleanupSome` que melhor esforço coletará os proxies de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="129b2-157">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="129b2-158">Os proxies de objetos remotos também têm os seguintes métodos que são executados localmente:</span><span class="sxs-lookup"><span data-stu-id="129b2-158">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="129b2-159">applyRemote, getRemote, SetRemote: execute uma invocação de método, uma propriedade get ou uma propriedade definida no objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-159">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="129b2-160">Você pode usá-los para forçar explicitamente um método ou uma propriedade para execução remota se houver um método ou uma propriedade local conflitante.</span><span class="sxs-lookup"><span data-stu-id="129b2-160">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="129b2-161">Por exemplo, ele `proxy.toString()` executará o método ToString local no objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="129b2-161">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="129b2-162">Mas `proxy.applyRemote('toString')` é executado `toString` no objeto em proxy remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-162">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="129b2-163">getLocal, setlocal: executar propriedade get ou Property definido localmente.</span><span class="sxs-lookup"><span data-stu-id="129b2-163">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="129b2-164">Você pode usar esses métodos para forçar a obtenção ou configuração de uma propriedade no próprio proxy de objeto remoto, em vez de no objeto remoto que ele representa.</span><span class="sxs-lookup"><span data-stu-id="129b2-164">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="129b2-165">Por exemplo, receberá `proxy.unknownProperty` a propriedade nomeada `unknownProperty` do objeto com proxy remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-165">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="129b2-166">Mas receberá `proxy.getLocal('unknownProperty')` o valor da propriedade `unknownProperty` no próprio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="129b2-166">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="129b2-167">sincronização: proxies de objetos remotos assíncronos expõem um método de sincronização que retorna uma promessa para um proxy síncrono de objeto remoto para o mesmo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-167">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="129b2-168">Por exemplo, `chrome.webview.remoteObjects.sample.methodCall()` retorna um proxy de objeto remoto assíncrono.</span><span class="sxs-lookup"><span data-stu-id="129b2-168">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="129b2-169">Você pode usar o `sync` método para obter um proxy de objeto remoto síncrono em vez disso:</span><span class="sxs-lookup"><span data-stu-id="129b2-169">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="129b2-170">Async: proxies de objetos remotos síncronos expõem um método Async que bloqueia e retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-170">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="129b2-171">Por exemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` retorna um proxy síncrono de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-171">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="129b2-172">Chamar o `async` método nesse bloco e, em seguida, retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto:</span><span class="sxs-lookup"><span data-stu-id="129b2-172">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="129b2-173">em seguida: proxies de objetos remotos assíncronos têm um método Where.</span><span class="sxs-lookup"><span data-stu-id="129b2-173">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="129b2-174">Isso permite que eles sejam awaitable.</span><span class="sxs-lookup"><span data-stu-id="129b2-174">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="129b2-175">retornará uma promessa que será resolvida com uma representação do objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-175">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="129b2-176">Se o proxy representar um literal JavaScript, uma cópia dele será retornada localmente.</span><span class="sxs-lookup"><span data-stu-id="129b2-176">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="129b2-177">Se o proxy representar uma função, um proxy não awaitable será retornado.</span><span class="sxs-lookup"><span data-stu-id="129b2-177">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="129b2-178">Se o proxy representar um objeto JavaScript com uma mistura de propriedades literais e propriedades de função, a cópia do objeto será retornada com algumas propriedades como proxies de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="129b2-178">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="129b2-179">Todas as outras invocações de método e Propriedade (além dos métodos de proxy de objeto remoto acima, lista de forceLocalProperties e propriedades em protótipos de objeto e função) são executadas remotamente.</span><span class="sxs-lookup"><span data-stu-id="129b2-179">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="129b2-180">Proxies assíncronos de objetos remotos retornam uma promessa que representa a conclusão assíncrona da invocação remota do método ou a obtenção da propriedade.</span><span class="sxs-lookup"><span data-stu-id="129b2-180">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="129b2-181">A promessa é resolvida após a conclusão das operações remotas e as promessas são resolvidas para o valor resultante da operação.</span><span class="sxs-lookup"><span data-stu-id="129b2-181">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="129b2-182">Os proxies de objetos remotos síncronos funcionam da mesma forma, mas bloqueiam a execução de JavaScript e aguardam a conclusão da operação remota.</span><span class="sxs-lookup"><span data-stu-id="129b2-182">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="129b2-183">A configuração de uma propriedade em um proxy de objeto remoto assíncrono funciona de forma ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="129b2-183">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="129b2-184">O conjunto retorna imediatamente e o valor de retorno é o valor que será definido.</span><span class="sxs-lookup"><span data-stu-id="129b2-184">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="129b2-185">Isso é uma exigência do objeto proxy JavaScript.</span><span class="sxs-lookup"><span data-stu-id="129b2-185">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="129b2-186">Se você precisar esperar assincronamente o conjunto de propriedades para concluir, use o método SetRemote que retorna uma promessa conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="129b2-186">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="129b2-187">Propriedade de conjunto de propriedades de objeto síncrono bloqueia sincronamente, até que a propriedade seja definida.</span><span class="sxs-lookup"><span data-stu-id="129b2-187">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="129b2-188">Por exemplo, suponha que você tenha um objeto COM com a seguinte interface</span><span class="sxs-lookup"><span data-stu-id="129b2-188">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="129b2-189">Poderemos adicionar uma instância dessa interface ao nosso JavaScript com `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="129b2-189">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="129b2-190">Nesse caso, podemos nomeá-lo `sample` :</span><span class="sxs-lookup"><span data-stu-id="129b2-190">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="129b2-191">Em seguida, no documento HTML, podemos usar esse objeto COM via `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="129b2-191">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="129b2-192">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="129b2-192">RemoveRemoteObject</span></span> 

<span data-ttu-id="129b2-193">Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.</span><span class="sxs-lookup"><span data-stu-id="129b2-193">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="129b2-194">Public HRESULT [RemoveRemoteObject](#removeremoteobject)(nome LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="129b2-194">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="129b2-195">Embora novas tentativas de acesso sejam negadas, se o objeto já for obtido por código JavaScript na WebView, o código JavaScript continuará a ter acesso a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="129b2-195">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="129b2-196">Chamar este método para um nome que já foi removido ou nunca adicionado falhará.</span><span class="sxs-lookup"><span data-stu-id="129b2-196">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="129b2-197">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="129b2-197">OpenDevToolsWindow</span></span> 

<span data-ttu-id="129b2-198">Abre a janela do DevTools para o documento atual no WebView.</span><span class="sxs-lookup"><span data-stu-id="129b2-198">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="129b2-199">Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="129b2-199">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="129b2-200">Não faz nada se for chamado quando a janela do DevTools já estiver aberta</span><span class="sxs-lookup"><span data-stu-id="129b2-200">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="129b2-201">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="129b2-201">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="129b2-202">Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="129b2-202">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="129b2-203">Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="129b2-203">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="129b2-204">AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado.</span><span class="sxs-lookup"><span data-stu-id="129b2-204">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="129b2-205">Uma tecla é considerada um acelerador se:</span><span class="sxs-lookup"><span data-stu-id="129b2-205">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="129b2-206">A tecla CTRL ou Alt está sendo mantida no momento ou</span><span class="sxs-lookup"><span data-stu-id="129b2-206">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="129b2-207">a tecla pressionada não é mapeada para um caractere.</span><span class="sxs-lookup"><span data-stu-id="129b2-207">the pressed key does not map to a character.</span></span> <span data-ttu-id="129b2-208">Algumas teclas específicas nunca são consideradas aceleradores, como Shift.</span><span class="sxs-lookup"><span data-stu-id="129b2-208">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="129b2-209">A tecla escape é sempre considerada um acelerador.</span><span class="sxs-lookup"><span data-stu-id="129b2-209">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="129b2-210">Os eventos chave repetido com repetição causada pela manutenção da tecla para baixo também acionarão esse evento.</span><span class="sxs-lookup"><span data-stu-id="129b2-210">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="129b2-211">Você pode filtrá-los verificando os argumentos do evento KeyEventLParam ou PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="129b2-211">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="129b2-212">No modo de janela, esse manipulador de eventos é chamado sincronicamente.</span><span class="sxs-lookup"><span data-stu-id="129b2-212">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="129b2-213">Até que você chame Handle () nos argumentos do evento ou o manipulador de eventos seja retornado, o processo do navegador será bloqueado e as chamadas COM saída cruzada de processo não funcionarão com RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="129b2-213">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="129b2-214">No entanto, todos os métodos de API WebView2 funcionarão.</span><span class="sxs-lookup"><span data-stu-id="129b2-214">All WebView2 API methods will work, however.</span></span>

<span data-ttu-id="129b2-215">No modo sem janela, o manipulador de eventos é chamado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="129b2-215">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="129b2-216">A entrada adicional não entrará em contato com o navegador até que o manipulador de eventos retorne ou manipule () seja chamado, mas o processo do navegador em si não será bloqueado, e as chamadas COM de saída funcionarão normalmente.</span><span class="sxs-lookup"><span data-stu-id="129b2-216">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="129b2-217">É recomendável chamar Handle (TRUE), como o mais cedo possível, se souber que deseja manipular a tecla aceleradora.</span><span class="sxs-lookup"><span data-stu-id="129b2-217">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_webView->add_AcceleratorKeyPressed(
        Callback<IWebView2AcceleratorKeyPressedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2AcceleratorKeyPressedEventArgs* args)
                -> HRESULT {
                WEBVIEW2_KEY_EVENT_TYPE type;
                CHECK_FAILURE(args->get_KeyEventType(&type));
                // We only care about key down events.
                if (type == WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN ||
                    type == WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->Handle(TRUE));

                        // Filter out autorepeated keys.
                        WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="129b2-218">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="129b2-218">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="129b2-219">Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="129b2-219">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="129b2-220">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)público HRESULT (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="129b2-220">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="129b2-221">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="129b2-221">WEBVIEW2_KEY_EVENT_TYPE</span></span> 

<span data-ttu-id="129b2-222">O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="129b2-222">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="129b2-223">Enumeração [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span><span class="sxs-lookup"><span data-stu-id="129b2-223">enum [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span></span>

 <span data-ttu-id="129b2-224">Valores</span><span class="sxs-lookup"><span data-stu-id="129b2-224">Values</span></span>                         | <span data-ttu-id="129b2-225">Descrições</span><span class="sxs-lookup"><span data-stu-id="129b2-225">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="129b2-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="129b2-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span></span>            | <span data-ttu-id="129b2-227">Corresponde à mensagem do Window WM_KEYDOWN.</span><span class="sxs-lookup"><span data-stu-id="129b2-227">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="129b2-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="129b2-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span></span>            | <span data-ttu-id="129b2-229">Corresponde à mensagem do Window WM_KEYUP.</span><span class="sxs-lookup"><span data-stu-id="129b2-229">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="129b2-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="129b2-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="129b2-231">Corresponde à mensagem do Window WM_SYSKEYDOWN.</span><span class="sxs-lookup"><span data-stu-id="129b2-231">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="129b2-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="129b2-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="129b2-233">Corresponde à mensagem do Window WM_SYSKEYUP.</span><span class="sxs-lookup"><span data-stu-id="129b2-233">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="129b2-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="129b2-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="129b2-235">Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.</span><span class="sxs-lookup"><span data-stu-id="129b2-235">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="129b2-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="129b2-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span></span>

<span data-ttu-id="129b2-237">Consulte a documentação do WM_KEYDOWN para obter detalhes em[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="129b2-237">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

