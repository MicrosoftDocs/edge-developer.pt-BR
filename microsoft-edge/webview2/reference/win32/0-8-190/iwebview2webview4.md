---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 8b029202843dd006be4d9ecdadc63161bebb6b39
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878054"
---
# 0.8.355-IWebView2WebView4 de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

Funcionalidades adicionais implementadas pelo objeto WebView primário.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Addremoteobject](#addremoteobject) | Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.
[RemoveRemoteObject](#removeremoteobject) | Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.
[OpenDevToolsWindow](#opendevtoolswindow) | Abre a janela do DevTools para o documento atual no WebView.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.
[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) | O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.
[WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) | Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.

Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md). Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.

## Parte

#### Addremoteobject 

Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.

> Public HRESULT [Addremoteobject](#addremoteobject)(nome do LPCWSTR, objeto Variant *)

Os objetos de host são expostos como proxies de objeto remoto via `window.chrome.webview.remoteObjects.<name>` . Proxies de objeto remoto são promessas e serão resolvidos para um objeto que representa o objeto host. A promessa será recusada se o aplicativo não adicionar um objeto com o nome. Quando o código JavaScript acessa uma propriedade ou método do objeto, uma promessa é retornada, que será resolvida para o valor retornado do host para a propriedade ou método, ou recusada em caso de erro, pois não há tal propriedade ou método no objeto ou parâmetros são inválidos. Por exemplo, quando o código do aplicativo faz o seguinte: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 O código JavaScript na WebView poderá acessar o appObject da seguinte forma e, em seguida, acessar atributos e métodos de appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Observe que, enquanto tipos simples, IDispatch e matriz são compatíveis, IUnknown Generic, VT_DECIMAL ou Variant VT_RECORD não é suportada. Objetos JavaScript remotos como funções de retorno de chamada são representados como uma variante VT_DISPATCH com o objeto que implementa IDispatch. O método de retorno de chamada JavaScript pode ser invocado usando DISPID_VALUE para o DISPID. Há suporte para matrizes aninhadas até uma profundidade de 3. Matrizes de tipos de referência não são suportadas. VT_EMPTY e VT_NULL são mapeados para JavaScript como nulo. Em JavaScript nulo e indefinido são mapeados para VT_EMPTY.

Além disso, todos os objetos remotos são expostos como `window.chrome.webview.remoteObjects.sync.<name>` . Aqui, os objetos do host são expostos como proxies síncronos de objeto remoto. Elas não são promessas e chamadas para funções ou acesso à propriedade o bloqueio síncrono de script em execução, aguardando a comunicação de processo cruzado para o código do host ser executado. Portanto, isso pode resultar em problemas de confiabilidade e é recomendável que você use a API assíncrona baseada em promessa `window.chrome.webview.remoteObjects.<name>` descrita acima.

Proxies de objetos remotos síncronos e proxies de objeto remoto assíncrono podem proxy para o mesmo objeto remoto. As alterações remotas feitas por um proxy serão refletidas em qualquer outro proxy do mesmo objeto remoto, seja os outros proxies e síncronos ou assíncronos.

Embora o JavaScript seja bloqueado em uma chamada síncrona para o código nativo, esse código nativo não pode retornar a chamada para JavaScript. As tentativas de fazer isso falharão com o HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Proxies de objeto remoto são objetos de proxy JavaScript que interceptam todas as invocações de propriedade, conjunto de propriedades e invocação de propriedade. Propriedades ou métodos que fazem parte da função ou do protótipo do objeto são executados localmente. Além disso, qualquer propriedade ou método na matriz `chrome.webview.remoteObjects.options.forceLocalProperties` também será executado localmente. Isso assume como padrão os métodos opcionais que têm significado em JavaScript como `toJSON` e `Symbol.toPrimitive` . Você pode adicionar mais à matriz, conforme necessário.

Há um método `chrome.webview.remoteObjects.cleanupSome` que melhor esforço coletará os proxies de objetos remotos.

Os proxies de objetos remotos também têm os seguintes métodos que são executados localmente:

* applyRemote, getRemote, SetRemote: execute uma invocação de método, uma propriedade get ou uma propriedade definida no objeto remoto. Você pode usá-los para forçar explicitamente um método ou uma propriedade para execução remota se houver um método ou uma propriedade local conflitante. Por exemplo, ele `proxy.toString()` executará o método ToString local no objeto proxy. Mas `proxy.applyRemote('toString')` é executado `toString` no objeto em proxy remoto.

* getLocal, setlocal: executar propriedade get ou Property definido localmente. Você pode usar esses métodos para forçar a obtenção ou configuração de uma propriedade no próprio proxy de objeto remoto, em vez de no objeto remoto que ele representa. Por exemplo, receberá `proxy.unknownProperty` a propriedade nomeada `unknownProperty` do objeto com proxy remoto. Mas receberá `proxy.getLocal('unknownProperty')` o valor da propriedade `unknownProperty` no próprio objeto proxy.

* sincronização: proxies de objetos remotos assíncronos expõem um método de sincronização que retorna uma promessa para um proxy síncrono de objeto remoto para o mesmo objeto remoto. Por exemplo, `chrome.webview.remoteObjects.sample.methodCall()` retorna um proxy de objeto remoto assíncrono. Você pode usar o `sync` método para obter um proxy de objeto remoto síncrono em vez disso: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: proxies de objetos remotos síncronos expõem um método Async que bloqueia e retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto. Por exemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` retorna um proxy síncrono de objeto remoto. Chamar o `async` método nesse bloco e, em seguida, retorna um proxy de objeto remoto assíncrono para o mesmo objeto remoto: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* em seguida: proxies de objetos remotos assíncronos têm um método Where. Isso permite que eles sejam awaitable. `then` retornará uma promessa que será resolvida com uma representação do objeto remoto. Se o proxy representar um literal JavaScript, uma cópia dele será retornada localmente. Se o proxy representar uma função, um proxy não awaitable será retornado. Se o proxy representar um objeto JavaScript com uma mistura de propriedades literais e propriedades de função, a cópia do objeto será retornada com algumas propriedades como proxies de objeto remoto.

Todas as outras invocações de método e Propriedade (além dos métodos de proxy de objeto remoto acima, lista de forceLocalProperties e propriedades em protótipos de objeto e função) são executadas remotamente. Proxies assíncronos de objetos remotos retornam uma promessa que representa a conclusão assíncrona da invocação remota do método ou a obtenção da propriedade. A promessa é resolvida após a conclusão das operações remotas e as promessas são resolvidas para o valor resultante da operação. Os proxies de objetos remotos síncronos funcionam da mesma forma, mas bloqueiam a execução de JavaScript e aguardam a conclusão da operação remota.

A configuração de uma propriedade em um proxy de objeto remoto assíncrono funciona de forma ligeiramente diferente. O conjunto retorna imediatamente e o valor de retorno é o valor que será definido. Isso é uma exigência do objeto proxy JavaScript. Se você precisar esperar assincronamente o conjunto de propriedades para concluir, use o método SetRemote que retorna uma promessa conforme descrito acima. Propriedade de conjunto de propriedades de objeto síncrono bloqueia sincronamente, até que a propriedade seja definida.

Por exemplo, suponha que você tenha um objeto COM com a seguinte interface

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

 Poderemos adicionar uma instância dessa interface ao nosso JavaScript com `AddRemoteObject` . Nesse caso, podemos nomeá-lo `sample` :

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

 Em seguida, no documento HTML, podemos usar esse objeto COM via `chrome.webview.remoteObjects.sample` :

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

#### RemoveRemoteObject 

Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.

> Public HRESULT [RemoveRemoteObject](#removeremoteobject)(nome LPCWSTR)

Embora novas tentativas de acesso sejam negadas, se o objeto já for obtido por código JavaScript na WebView, o código JavaScript continuará a ter acesso a esse objeto. Chamar este método para um nome que já foi removido ou nunca adicionado falhará.

#### OpenDevToolsWindow 

Abre a janela do DevTools para o documento atual no WebView.

> Public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Não faz nada se for chamado quando a janela do DevTools já estiver aberta

#### add_AcceleratorKeyPressed 

Adicione um manipulador de eventos para o evento AcceleratorKeyPressed.

> Public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) * EventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed é acionado quando uma tecla de aceleração ou combinação de teclas é pressionada ou lançada enquanto o WebView está focalizado. Uma tecla é considerada um acelerador se:

1. A tecla CTRL ou Alt está sendo mantida no momento ou

1. a tecla pressionada não é mapeada para um caractere. Algumas teclas específicas nunca são consideradas aceleradores, como Shift. A tecla escape é sempre considerada um acelerador.

Os eventos chave repetido com repetição causada pela manutenção da tecla para baixo também acionarão esse evento. Você pode filtrá-los verificando os argumentos do evento KeyEventLParam ou PhysicalKeyStatus.

No modo de janela, esse manipulador de eventos é chamado sincronicamente. Até que você chame Handle () nos argumentos do evento ou o manipulador de eventos seja retornado, o processo do navegador será bloqueado e as chamadas COM saída cruzada de processo não funcionarão com RPC_E_CANTCALLOUT_ININPUTSYNCCALL. No entanto, todos os métodos de API WebView2 funcionarão.

No modo sem janela, o manipulador de eventos é chamado de forma assíncrona. A entrada adicional não entrará em contato com o navegador até que o manipulador de eventos retorne ou manipule () seja chamado, mas o processo do navegador em si não será bloqueado, e as chamadas COM de saída funcionarão normalmente.

É recomendável chamar Handle (TRUE), como o mais cedo possível, se souber que deseja manipular a tecla aceleradora.

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

#### remove_AcceleratorKeyPressed 

Remover um manipulador de eventos adicionado anteriormente com add_AcceleratorKeyPressed.

> [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)público HRESULT (token EventRegistrationToken)

#### WEBVIEW2_KEY_EVENT_TYPE 

O tipo de evento de chave que disparou um evento AcceleratorKeyPressed.

> Enumeração [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)

 Valores                         | Descrições
--------------------------------|---------------------------------------------
WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN            | Corresponde à mensagem do Window WM_KEYDOWN.
WEBVIEW2_KEY_EVENT_TYPE_KEY_UP            | Corresponde à mensagem do Window WM_KEYUP.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN            | Corresponde à mensagem do Window WM_SYSKEYDOWN.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP            | Corresponde à mensagem do Window WM_SYSKEYUP.

#### WEBVIEW2_PHYSICAL_KEY_STATUS 

Uma estrutura que representa as informações empacotadas no LPARAM fornecido a um evento de chave do Win32.

> typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)

Consulte a documentação do WM_KEYDOWN para obter detalhes em[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

