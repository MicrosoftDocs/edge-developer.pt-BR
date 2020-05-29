---
description: 'Saiba como direcionar os diferentes mecanismos JavaScript do Windows 10. '
title: Direcionando mecanismos do Microsoft Edge versus Legacy em APIs do JsRT | Documentos da Microsoft
ms.custom: ''
ms.date: 03/05/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ed0dc8c67b8189a7433d52185aa995997edb70a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560984"
---
# <span data-ttu-id="5d277-103">Direcionando mecanismos do Microsoft Edge versus Legacy em APIs do JsRT</span><span class="sxs-lookup"><span data-stu-id="5d277-103">Targeting Microsoft Edge vs. Legacy Engines in JsRT APIs</span></span>

<span data-ttu-id="5d277-104">O Windows 10 dá suporte a dois mecanismos JavaScript diferentes:</span><span class="sxs-lookup"><span data-stu-id="5d277-104">Windows 10 supports two different JavaScript engines:</span></span>

-   <span data-ttu-id="5d277-105">O antigo mecanismo de Chakra (também chamado de *mecanismo herdado* ou jscript9. dll abaixo) que acompanha e suporta o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="5d277-105">The old Chakra engine (also called the *legacy engine* or jscript9.dll below) that ships with and supports Internet Explorer 11.</span></span> <span data-ttu-id="5d277-106">Esse mecanismo está congelado no tempo e permanecerá fundamentalmente inalterado do lançamento do Win 8.1/IE11.</span><span class="sxs-lookup"><span data-stu-id="5d277-106">This engine is frozen in time and will remain fundamentally unchanged from Win8.1/IE11 release.</span></span>  
  
-   <span data-ttu-id="5d277-107">O novo mecanismo Chakra (também chamado de *Edge Engine* ou Chakra. dll abaixo) que acompanha e dá suporte ao novo navegador no Windows 10, Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d277-107">The new Chakra engine (also called the *Edge engine* or chakra.dll below) that ships with and supports the new browser in Windows 10, Microsoft Edge.</span></span> <span data-ttu-id="5d277-108">Este mecanismo será atualizado continuamente e dará suporte a um mecanismo de [borda](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) "vivo".</span><span class="sxs-lookup"><span data-stu-id="5d277-108">This engine will be continually updated and will support a "living" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) engine.</span></span> <span data-ttu-id="5d277-109">Um mecanismo dinâmico da Microsoft Edge sugere que, ao contrário do mecanismo herdado, o mecanismo Microsoft Edge não transportasse qualquer tipo de funcionalidade de script de controle de versão para aceitar.</span><span class="sxs-lookup"><span data-stu-id="5d277-109">A living Microsoft Edge engine implies that unlike the legacy engine, the Microsoft Edge engine would not carry forward any form of versioning script functionality to opt into.</span></span>  
  
 <span data-ttu-id="5d277-110">Ao criar um aplicativo usando a API de Hospedagem de tempo de execução (JsRT) do JavaScript, você pode optar por direcionar o mecanismo herdado ou o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d277-110">When creating an app using the JavaScript Runtime Hosting (JsRT) API, you can choose to target either the legacy or the Microsoft Edge engine.</span></span>  
  
-   <span data-ttu-id="5d277-111">Se você precisar enfatizar a compatibilidade com versões anteriores de seus aplicativos existentes, destinar-se ao mecanismo herdado.</span><span class="sxs-lookup"><span data-stu-id="5d277-111">If you need to emphasize backward compatibility of your existing applications, target the legacy engine.</span></span>  
  
-   <span data-ttu-id="5d277-112">Se você quiser que seu aplicativo seja encaminhado procurando e dê suporte a novos recursos JavaScript conforme eles são lançados (por exemplo, ECMAScript 6), destinam-se ao mecanismo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d277-112">If you want your app to be forward looking and support new JavaScript features as they are released (for example, ECMAScript 6), target the Microsoft Edge engine.</span></span>  
  
 <span data-ttu-id="5d277-113">Este tópico inclui detalhes que descrevem como direcionar os diferentes mecanismos.</span><span class="sxs-lookup"><span data-stu-id="5d277-113">This topic includes details that describe how to target the different engines.</span></span>  
  
## <span data-ttu-id="5d277-114">Destinar-se à sua versão preferida</span><span class="sxs-lookup"><span data-stu-id="5d277-114">Target your preferred version</span></span>  
 <span data-ttu-id="5d277-115">Ao criar um aplicativo, você pode selecionar a versão do JsRT que suporta o mecanismo Microsoft Edge ou o mecanismo herdado.</span><span class="sxs-lookup"><span data-stu-id="5d277-115">When creating an app, you can select the version of the JsRT that supports either the Microsoft Edge engine or the legacy engine.</span></span> <span data-ttu-id="5d277-116">Você pode escolher a versão do JsRT com base nas diretrizes acima.</span><span class="sxs-lookup"><span data-stu-id="5d277-116">You can choose the JsRT version based on the guidelines above.</span></span> <span data-ttu-id="5d277-117">Para acomodar essas distinções, as seguintes alterações foram feitas em `JsCreateRuntime` , `JsCreateContext` e `JsStartDebugging` .</span><span class="sxs-lookup"><span data-stu-id="5d277-117">To accommodate these distinctions, the following changes have been made to `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging`.</span></span>  
  
 <span data-ttu-id="5d277-118">Para `JsCreateRuntime` :</span><span class="sxs-lookup"><span data-stu-id="5d277-118">For `JsCreateRuntime`:</span></span>  
  
-   <span data-ttu-id="5d277-119">Ao direcionar o mecanismo herdado, o `JsRuntimeVersionEdge` valor de enumeração é preterido, e uma mensagem vai sugerir usar o `JsRuntimeVersionInternetExplorer11` valor em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5d277-119">When targeting the legacy engine, the `JsRuntimeVersionEdge` enumeration value is deprecated, and a message will suggest using the `JsRuntimeVersionInternetExplorer11` value instead.</span></span>  
  
-   <span data-ttu-id="5d277-120">Ao direcionar o mecanismo do Microsoft Edge, o parâmetro version é omitido da `JsCreateRuntime` função.</span><span class="sxs-lookup"><span data-stu-id="5d277-120">When targeting the Microsoft Edge engine, the version parameter is omitted from the `JsCreateRuntime` function.</span></span>  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 <span data-ttu-id="5d277-121">Para `JsCreateContext` e `JsStartDebugging` :</span><span class="sxs-lookup"><span data-stu-id="5d277-121">For `JsCreateContext` and `JsStartDebugging`:</span></span>  
  
-   <span data-ttu-id="5d277-122">Ao direcionar o mecanismo herdado, a `IDebugApplication` interface é usada para fornecer seus próprios métodos de depuração não remotos.</span><span class="sxs-lookup"><span data-stu-id="5d277-122">When targeting the legacy engine, the `IDebugApplication` interface is used to supply your own non-remote debugging methods.</span></span> <span data-ttu-id="5d277-123">Para fins de depuração, `JsCreateContext` e `JsStartDebugging` as funções são executadas `IDebugApplication` como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5d277-123">For debugging purposes, `JsCreateContext` and `JsStartDebugging` functions take `IDebugApplication` as parameter.</span></span>  
  
-   <span data-ttu-id="5d277-124">Ao direcionar o mecanismo do Microsoft Edge, a `IDebugApplication` interface é preterida.</span><span class="sxs-lookup"><span data-stu-id="5d277-124">When targeting the Microsoft Edge engine, the `IDebugApplication` interface is deprecated.</span></span> <span data-ttu-id="5d277-125">O mecanismo Chakra permite a funcionalidade de depuração nativa e de script com depurador do Visual Studio sem exigir uma implementação de `IDebugApplication` do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d277-125">The Chakra engine enables native and script debugging capability with Visual Studio debugger without requiring an implementation of `IDebugApplication` from user.</span></span> <span data-ttu-id="5d277-126">A interface não é mais um parâmetro para `JsCreateContext` e `JsStartDebugging` como resultado.</span><span class="sxs-lookup"><span data-stu-id="5d277-126">The interface is no longer a parameter for `JsCreateContext` and `JsStartDebugging` as a result.</span></span>  
  
 <span data-ttu-id="5d277-127">As assinaturas para as APIs anteriores no mecanismo herdado são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="5d277-127">The signatures for the preceding APIs in the legacy engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 <span data-ttu-id="5d277-128">As assinaturas para as APIs anteriores no mecanismo Microsoft Edge são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="5d277-128">The signatures for the preceding APIs in the Microsoft Edge engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## <span data-ttu-id="5d277-129">Compilar para a sua versão preferida usando o Visual C++</span><span class="sxs-lookup"><span data-stu-id="5d277-129">Compile for your preferred version using Visual C++</span></span>  
 <span data-ttu-id="5d277-130">Ao usar o Visual C++, importe a API JsRT incluindo o cabeçalho JsRT. h e certifique-se de que JsRT. lib esteja incluído na sua lista de arquivos de entrada do vinculador:</span><span class="sxs-lookup"><span data-stu-id="5d277-130">When using Visual C++, import the JsRT API by including the jsrt.h header, and ensure that jsrt.lib is included in your linker input files list:</span></span>  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Adicionando jsrt. lib como um arquivo de entrada do vinculador](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 <span data-ttu-id="5d277-132">Se quiser direcionar os binários do mecanismo Microsoft Edge, você precisa definir a macro `USE_EDGEMODE_JSRT` antes de incluir jsrt. h e, em vez de vincular a jsrt. lib, você deve vincular o chakrart. lib:</span><span class="sxs-lookup"><span data-stu-id="5d277-132">If you want to target the Microsoft Edge engine binaries, you need to define the macro `USE_EDGEMODE_JSRT` before including jsrt.h, and instead of linking against jsrt.lib, you should link against chakrart.lib:</span></span>  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Adicionando chakrart. lib como um arquivo de entrada do vinculador](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 <span data-ttu-id="5d277-134">Se você estiver começando com um novo aplicativo, agora você está pronto para começar a escrever código com a API JsRT.</span><span class="sxs-lookup"><span data-stu-id="5d277-134">If you're starting with a new application, you are now ready to start writing code against the JsRT API.</span></span>  
  
## <span data-ttu-id="5d277-135">Compilar para a sua versão preferida usando o .NET</span><span class="sxs-lookup"><span data-stu-id="5d277-135">Compile for your preferred version using .NET</span></span>  
 <span data-ttu-id="5d277-136">Se você estiver usando .NET e P/Invoke, será necessário alterar suas declarações API de JsRT [DllImport] para importar Chakra. dll em vez de jscript9. dll.</span><span class="sxs-lookup"><span data-stu-id="5d277-136">If you're using .NET and P/Invoke, you must change your JsRT API [DllImport] declarations to import chakra.dll instead of jscript9.dll.</span></span> <span data-ttu-id="5d277-137">Além disso, altere a definição de `JsCreateRuntime` para remover o `JsRuntimeVersion` parâmetro e a definição de `JsCreateContext` e `JsStartDebugging` para remover o `IDebugApplication` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5d277-137">In addition, change the definition of `JsCreateRuntime` to remove the `JsRuntimeVersion` parameter and the definition of `JsCreateContext` and `JsStartDebugging` to remove the `IDebugApplication` parameter.</span></span>  
  
 <span data-ttu-id="5d277-138">Para o mecanismo herdado, use o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d277-138">For the legacy engine, use the following code.</span></span>  
  
```c#  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsRuntimeVersion version,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    IDebugApplication debugApplication,  
    out JsContextRef newContext  
);   
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsStartDebugging(  
    IDebugApplication debugApplication,  
);  
```  
  
 <span data-ttu-id="5d277-139">Para o mecanismo Microsoft Edge, use o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d277-139">For the Microsoft Edge engine, use the following code.</span></span>  
  
```c#  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    out JsContextRef newContext  
);   
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsStartDebugging();  
```  
  
> [!CAUTION]
>  <span data-ttu-id="5d277-140">Se você estiver fazendo o marshaling manual do ponteiro da função (como via LoadLibrary/GetProcAddress), é fundamental que você não misture as declarações do método ou desbalanceia a pilha, o que resultará em um comportamento imprevisível, como causar falha no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d277-140">If you are manually marshaling the function pointer (such as via LoadLibrary/GetProcAddress), it is critical that you do not mix the declarations of the method, or else you will unbalance the stack, which will result in unpredictable behavior such as causing your app to crash.</span></span> <span data-ttu-id="5d277-141">O mesmo problema ocorrerá se você executar uma pesquisa global e substituir de instâncias de jscript9. dll no código de importação, porque perderá o `version` parâmetro sendo eliminado.</span><span class="sxs-lookup"><span data-stu-id="5d277-141">The same problem will occur if you perform a global search-and-replace of instances of jscript9.dll in your import code, because you'll miss the `version` parameter being dropped.</span></span>  
  
## <span data-ttu-id="5d277-142">Resumo</span><span class="sxs-lookup"><span data-stu-id="5d277-142">Summary</span></span>  
 <span data-ttu-id="5d277-143">No Windows 10, as APIs de hospedagem do tempo de execução do JavaScript estão sendo divididas em duas.</span><span class="sxs-lookup"><span data-stu-id="5d277-143">In Windows 10, the JavaScript Runtime Hosting APIs are splitting into two.</span></span> <span data-ttu-id="5d277-144">Essas APIs agora dão suporte a um mecanismo "vivo" do Microsoft Edge, cujos recursos de idioma serão alinhados com o mecanismo "vivo" do Microsoft Edge no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5d277-144">These APIs now support a "living" Microsoft Edge engine, whose language capabilities will be aligned with the "living" Microsoft Edge engine in the Microsoft Edge.</span></span> <span data-ttu-id="5d277-145">Você pode aproveitar esses recursos da área de trabalho ou aplicativos da loja para criar maneiras novas e incríveis de estender o aplicativo e aproveitar habilidades modernas da Web em sua base de códigos existente.</span><span class="sxs-lookup"><span data-stu-id="5d277-145">You can leverage these capabilities from your desktop or Store apps to create new and exciting ways to extend your application and to leverage modern Web skills in your existing code base.</span></span> <span data-ttu-id="5d277-146">No entanto, como há diferenças sutis entre as versões anteriores, você deve estar ciente dos seguintes pontos ao direcionar a borda ou o mecanismo herdado.</span><span class="sxs-lookup"><span data-stu-id="5d277-146">However, because there are subtle differences between previous versions, you must be aware of the following points when targeting the Edge or legacy engine.</span></span>  
  
-   <span data-ttu-id="5d277-147">Seu aplicativo pode dar suporte a apenas uma versão do JsRT por processo.</span><span class="sxs-lookup"><span data-stu-id="5d277-147">Your app can support only one version of JsRT per process.</span></span>  
  
     <span data-ttu-id="5d277-148">Por exemplo, você não pode criar um tempo de execução do Microsoft Edge Engine e, em seguida, um tempo de execução do mecanismo herdado e esperar que eles sejam executados corretamente no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="5d277-148">For example, you can't create a Microsoft Edge engine runtime and then a legacy engine runtime and expect them to run correctly in the same process.</span></span> <span data-ttu-id="5d277-149">Isso não tem suporte e pode resultar em um comportamento não documentado, como falha ao carregar a segunda DLL.</span><span class="sxs-lookup"><span data-stu-id="5d277-149">This is unsupported and may result in undocumented behavior, such as failure to load the second DLL.</span></span>  
  
-   <span data-ttu-id="5d277-150">Ao direcionar o mecanismo do Microsoft Edge, seu aplicativo pode adquirir inesperadamente novos recursos quando a plataforma subjacente é atualizada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5d277-150">When targeting the Microsoft Edge engine, your app may unexpectedly acquire new features when the underlying platform is automatically updated.</span></span>  
  
     <span data-ttu-id="5d277-151">Por exemplo, o modo do Internet Explorer 11 do tempo de execução herdado dá suporte a declarações de variáveis de escopo de bloco, como `let` e `const` .</span><span class="sxs-lookup"><span data-stu-id="5d277-151">For example, the Internet Explorer 11 mode of the legacy runtime supports block-scoping variable declarations such as `let` and `const`.</span></span> <span data-ttu-id="5d277-152">Se o comportamento de controle automático do mecanismo de borda da Microsoft Edge era o padrão anteriormente, o código que funcionou no modo do Internet Explorer 10, que não tinha regras de escopo de bloco, pode ter começado a falhar quando a plataforma tiver sido atualizada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5d277-152">If the Microsoft Edge engine automatic versioning behavior had been the standard previously, code that had worked in Internet Explorer 10 mode, which did not have block-scoping rules, may have started failing when the platform had automatically upgraded.</span></span> <span data-ttu-id="5d277-153">Isso deve ser uma consideração ao escolher qual modelo de tempo de execução usar.</span><span class="sxs-lookup"><span data-stu-id="5d277-153">This must be a consideration when choosing which runtime model to use.</span></span> <span data-ttu-id="5d277-154">Enquanto acreditamos que você deve direcionar o mecanismo Microsoft Edge sempre que possível, você deve ter cuidado em usar estruturas de código JavaScript que podem se tornar inválidas no futuro.</span><span class="sxs-lookup"><span data-stu-id="5d277-154">While we believe you should target the Microsoft Edge engine whenever possible, you must be careful about using JavaScript code structures that may become invalid in the future.</span></span>  
  
-   <span data-ttu-id="5d277-155">O JsRT para a Windows Store só oferece suporte ao mecanismo Microsoft Edge (Chakra. dll).</span><span class="sxs-lookup"><span data-stu-id="5d277-155">JsRT for the Windows Store only supports the Microsoft Edge engine (chakra.dll).</span></span> <span data-ttu-id="5d277-156">Os aplicativos que tentam se vincular a qualquer API do JsRT no jscript9. dll falham na certificação.</span><span class="sxs-lookup"><span data-stu-id="5d277-156">Apps attempting to link against any JsRT API in jscript9.dll will fail certification.</span></span>  
  
-   <span data-ttu-id="5d277-157">É essencial que você não confunda a declaração de `JsCreateRuntime` , `JsCreateContext` e `JsStartDebugging` entre jscript9. dll e Chakra. dll, pois isso resultará em imbalancear a pilha.</span><span class="sxs-lookup"><span data-stu-id="5d277-157">It is critical that you do not confuse the declaration of `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging` between jscript9.dll and chakra.dll, because it will result in imbalancing the stack.</span></span>  
  
     <span data-ttu-id="5d277-158">Ao usar C e C++, você receberá um erro de vinculador se tentar usar a declaração errada, desde que não esteja fazendo algo como fazer chamadas `LoadLibrary` e, em seguida, `GetProcAddress` .</span><span class="sxs-lookup"><span data-stu-id="5d277-158">When using C and C++, you will receive a linker error if you try to use the wrong declaration, as long as you're not doing something like calling `LoadLibrary` and then `GetProcAddress`.</span></span> <span data-ttu-id="5d277-159">Os desenvolvedores do .NET podem não encontrar esse problema com facilidade, portanto, clique duas vezes no seu código ao usar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5d277-159">.NET developers may not find this problem as easily, so double-check your code when using this feature.</span></span>  
  
## <span data-ttu-id="5d277-160">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5d277-160">See Also</span></span>  
 [<span data-ttu-id="5d277-161">Hospedagem do tempo de execução JavaScript</span><span class="sxs-lookup"><span data-stu-id="5d277-161">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)
 