---
title: Informações de versão do JavaScript
description: Comparar o suporte JavaScript no Microsoft Edge, aplicativos da Microsoft Store e Internet Explorer
ms.prod: microsoft-edge
ms.topic: language-reference
author: MSEdgeTeam
ms.author: msedgedevrel
keywords: Edge, IE, Chakra, JScript, WWA, aplicativos da loja
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f420b0546f623b5b1c1d43a7b7237a888f97715
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231590"
---
# Informações de versão do JavaScript  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

O suporte a JavaScript varia de acordo com o Microsoft Edge, os aplicativos da Microsoft Store e os diferentes modos de documento do Internet Explorer \(IE \). Para obter mais informações sobre o controle de versão do código de documento do IE, consulte [definindo a compatibilidade do documento](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).  

A tabela a seguir resume o suporte a JavaScript nos aplicativos Internet Explorer, Microsoft Edge e Microsoft Store.  
  
> [!IMPORTANT]
> Os recursos experimentais \(habilitados de `about:flags` \) são indicados por `Exp` . Em alguns casos, o suporte a repositório de aplicativos varia entre os aplicativos do Windows 8 \(V8 \) e do Windows 10 \(V10 \) e a área de trabalho do Windows \(Win \) e o Windows Phone \(telefone \), conforme indicado.  
  
 | Elemento de linguagem | Peculiaridades, padrões do IE 6, padrões do IE 7 | Padrões do IE 8 | Padrões do IE 9 | Padrões do IE 10 | Padrões do IE 11 | Microsoft Edge | Aplicativos da loja |  
 |:--- |:--- |:--- |:--- |:--- |:--- |:--- |:--- |  
| [Propriedade __proto \ _ \ _ (objeto)](/scripting/javascript/reference/proto-property-object-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (telefone): Y |  
| [$1... $9 Propriedades (RegExp)](/scripting/javascript/reference/dollar-1-dot-dot-dot-dollar-9-properties-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade 0N](/scripting/javascript/reference/0-dot-dot-dot-n-properties-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ABS](/scripting/javascript/reference/math-abs-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função acos](/scripting/javascript/reference/math-acos-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ACOSH](/scripting/javascript/reference/math-acosh-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Objeto ActiveXobject](/scripting/javascript/reference/activexobject-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Operador de atribuição de adição (+ =)](/scripting/javascript/reference/addition-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de adição (+)](/scripting/javascript/reference/addition-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Apply](/scripting/javascript/reference/apply-method-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Arguments](/scripting/javascript/reference/arguments-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Arguments](/scripting/javascript/reference/arguments-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto array](/scripting/javascript/reference/array-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função array. from (matriz)](/scripting/javascript/reference/array-from-function-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Função array. IsArray](/scripting/javascript/reference/array-isarray-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Matriz. de função (matriz)](/scripting/javascript/reference/array-of-function-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Objeto ArrayBuffer](/scripting/javascript/reference/arraybuffer-object) | N | N | N | Y | Y | Y | Y |  
| [Funções](/scripting/javascript/functions-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Função Asen](/scripting/javascript/reference/math-asin-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Object. Assign function (objeto)](/scripting/javascript/reference/object-assign-function-object-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Operador de atribuição (=)](/scripting/javascript/reference/assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ATAN](/scripting/javascript/reference/math-atan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ATAN2](/scripting/javascript/reference/math-atan2-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método atEnd](/scripting/javascript/reference/atend-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Método BIND](/scripting/javascript/reference/bind-method-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Operadora bit a bit e de atribuição (&=)](/scripting/javascript/reference/bitwise-and-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operadora e bit a bit (&)](/scripting/javascript/reference/bitwise-and-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador SHIFT esquerdo de bit (< \ <)](/scripting/javascript/reference/bitwise-left-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de não-bit a bit (~)](/scripting/javascript/reference/bitwise-not-operator-decrement-tilde-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operadora bit a bit ou de atribuição (&#124;=)](/scripting/javascript/reference/bitwise-or-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operadora ou bit a bit (&#124;)](/scripting/javascript/reference/bitwise-or-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de deslocamento à direita não-bit a lado (>>)](/scripting/javascript/reference/bitwise-right-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição do bit a bit (^ =)](/scripting/javascript/reference/bitwise-xor-assignment-operator-decrement-hat-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador do bit a bit (^)](/scripting/javascript/reference/bitwise-xor-operator-decrement-hat-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método de intermitência](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Bold](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto booliano](/scripting/javascript/reference/boolean-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução break](/scripting/javascript/reference/break-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método de chamada](/scripting/javascript/reference/call-method-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Callee](/scripting/javascript/reference/callee-property-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Caller](/scripting/javascript/reference/caller-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução Catch](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ceil](/scripting/javascript/reference/math-ceil-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método charAt](/scripting/javascript/reference/charat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método charCodeAt](/scripting/javascript/reference/charcodeat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução de classe](/scripting/javascript/reference/class-statement-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: exp. |  
| [Método codePointAt (cadeia de caracteres)](/scripting/javascript/reference/codepointat-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador vírgula (,)](/scripting/javascript/reference/comma-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [(Instrução de comentário de linha única)](/scripting/javascript/reference/comment-statements-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [/*.. \ */(Demonstrativo de comentário multilinha)](/scripting/javascript/reference/comment-statements-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operadores de comparação](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Compile](/scripting/javascript/reference/compile-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Concat (matriz)](/scripting/javascript/reference/concat-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Concat (cadeia de caracteres)](/scripting/javascript/reference/concat-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Compilação condicional](/scripting/javascript/advanced/conditional-compilation-javascript) | Y | Y | Y | Y | N | N | N |  
| [Variáveis de compilação condicional](/scripting/javascript/advanced/conditional-compilation-variables-javascript) | Y | Y | Y | Y | N | N | N |  
| [Operador condicional (Ternário) (?:)](/scripting/javascript/reference/conditional-ternary-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade do Construtor](/scripting/javascript/reference/constructor-property-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução const](/scripting/javascript/reference/const-statement-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (telefone): Y |  
| [Instrução Continue](/scripting/javascript/reference/continue-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função cos](/scripting/javascript/reference/math-cos-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função criar](/scripting/javascript/reference/object-create-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto DataView](/scripting/javascript/reference/dataview-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Date](/scripting/javascript/reference/date-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto de depuração](/scripting/javascript/reference/debug-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Debug. setNonUserCodeExceptions](/scripting/javascript/reference/debug-setnonusercodeexceptions-property) | N | N | N | Y | Y | Y | Y |  
| [Propriedade Debug. setNonUserCodeExceptions](/scripting/javascript/reference/debug-setnonusercodeexceptions-property) | N | N | N | Y | Y | Y | Y |  
| [Instrução do depurador](/scripting/javascript/reference/debugger-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função decodeURI](/scripting/javascript/reference/decodeuri-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função DecodeURIComponent](/scripting/javascript/reference/decodeuricomponent-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador decréscimo (--)](/scripting/javascript/reference/increment-and-decrement-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Funções](/scripting/javascript/functions-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: exp. |  
| [Função definoproperties](/scripting/javascript/reference/object-defineproperties-function-javascript) | N | I | Y | Y | Y | Y | Y |  
| [Função DefineProperty](/scripting/javascript/reference/object-defineproperty-function-javascript) | N | I | Y | Y | Y | Y | Y |  
| [Excluir operador](/scripting/javascript/reference/delete-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Description](/scripting/javascript/reference/description-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Dimensions](/scripting/javascript/reference/dimensions-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição de divisão (/=)](/scripting/javascript/reference/division-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de divisão (/)](/scripting/javascript/reference/division-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [do... Instrução while](/scripting/javascript/reference/do-dot-dot-dot-while-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função encodeURI](/scripting/javascript/reference/encodeuri-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função de componente encodeURI](/scripting/javascript/reference/encodeuricomponent-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Entries (matriz)](/scripting/javascript/reference/entries-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Objeto Enumerator](/scripting/javascript/reference/enumerator-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Constantes de número](/scripting/javascript/reference/number-constants-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Operador de igualdade (= =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto de erro](/scripting/javascript/reference/error-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Stack (erro)](/scripting/javascript/reference/stack-property-error-javascript) | N | N | N | Y | Y | Y | Y |  
| [Propriedade stackTraceLimit (erro)](/scripting/javascript/reference/stacktracelimit-property-error-javascript) | N | N | N | Y | Y | Y | Y |  
| [Função escape](/scripting/javascript/reference/escape-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função eval](/scripting/javascript/reference/eval-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Exec](/scripting/javascript/reference/exec-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [cada método](/scripting/javascript/reference/every-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Função exp](/scripting/javascript/reference/math-exp-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Fill (matriz)](/scripting/javascript/reference/fill-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Método Filter](/scripting/javascript/reference/filter-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Instrução Finally](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método findIndex (matriz)](/scripting/javascript/reference/findindex-method-array-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Método fixo](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Float32Array](/scripting/javascript/reference/float32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Float64Array](/scripting/javascript/reference/float64array-object) | N | N | N | Y | Y | Y | Y |  
| [Função Floor](/scripting/javascript/reference/math-floor-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método fontcolor](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método TamanhoDaFonte](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução for](/scripting/javascript/reference/for-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método forEach](/scripting/javascript/reference/foreach-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [para... na instrução](/scripting/javascript/reference/for-dot-dot-dot-in-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [para... da instrução](/scripting/javascript/reference/for-dot-dot-dot-of-statement-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Função congelar](/scripting/javascript/reference/object-freeze-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Função fromCharCode](/scripting/javascript/reference/string-fromcharcode-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função fromCodePoint](/scripting/javascript/reference/string-fromcodepoint-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Objeto function](/scripting/javascript/reference/function-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução function](/scripting/javascript/reference/function-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Geradores](/scripting/javascript/advanced/iterators-and-generators-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: exp. |  
| [Método getDate](/scripting/javascript/reference/getdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getDay](/scripting/javascript/reference/getday-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getFullYear](/scripting/javascript/reference/getfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getHours](/scripting/javascript/reference/gethours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getItem](/scripting/javascript/reference/getitem-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getmilisegundos](/scripting/javascript/reference/getmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getMinutes](/scripting/javascript/reference/getminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getMonth](/scripting/javascript/reference/getmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função GetObject](/scripting/javascript/reference/getobject-function-javascript) | Y | Y | N | N | N | N | N |  
| [Função getOwnPropertyDescriptor](/scripting/javascript/reference/object-getownpropertydescriptor-function-javascript) | N | I | Y | Y | Y | Y | Y |  
| [Função getOwnPropertyNames](/scripting/javascript/reference/object-getownpropertynames-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Função getPrototypeOf](/scripting/javascript/reference/object-getprototypeof-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método getSeconds](/scripting/javascript/reference/getseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getTime](/scripting/javascript/reference/gettime-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getTimezoneOffset](/scripting/javascript/reference/gettimezoneoffset-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCDate](/scripting/javascript/reference/getutcdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCDay](/scripting/javascript/reference/getutcday-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCFullYear](/scripting/javascript/reference/getutcfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCHours](/scripting/javascript/reference/getutchours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCMilliseconds](/scripting/javascript/reference/getutcmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCMinutes](/scripting/javascript/reference/getutcminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCMonth](/scripting/javascript/reference/getutcmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getUTCSeconds](/scripting/javascript/reference/getutcseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método getVarDate](/scripting/javascript/reference/getvardate-method-date-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Método getYear](/scripting/javascript/reference/getyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto global](/scripting/javascript/reference/global-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade global](/scripting/javascript/reference/global-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador maior que (>)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador maior do que ou igual a (>=)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método hasOwnProperty](/scripting/javascript/reference/hasownproperty-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Métodos de marca HTML](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função hypot](/scripting/javascript/reference/math-hypot-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador de identidade (= = =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [se... Instrução else](/scripting/javascript/reference/if-dot-dot-dot-else-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade ignoreCase](/scripting/javascript/reference/ignorecase-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função imul](/scripting/javascript/reference/math-imul-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador in](/scripting/javascript/reference/in-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [inclui método (cadeia)](/scripting/javascript/reference/includes-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Operador de incremento (+ +)](/scripting/javascript/reference/increment-and-decrement-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade index](/scripting/javascript/reference/index-property-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método indexOf (matriz)](/scripting/javascript/reference/indexof-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método indexOf (cadeia de caracteres)](/scripting/javascript/reference/indexof-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de desigualdade (! =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante infinito](/scripting/javascript/reference/infinity-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Input ($ _)](/scripting/javascript/reference/input-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador instanceof](/scripting/javascript/reference/instanceof-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Int8Array](/scripting/javascript/reference/int8array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Int16Array](/scripting/javascript/reference/int16array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Int32Array](/scripting/javascript/reference/int32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto intl. COLLATE](/scripting/javascript/reference/intl-collator-object-javascript) | N | N | N | N | Y | Y | V8 (Win): N <br /> v 8.1 (Win): Y <br /> v 8.1 (telefone): Y |  
| [Objeto intl. DateTimeFormat](/scripting/javascript/reference/intl-datetimeformat-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Objeto intl. NumberFormat](/scripting/javascript/reference/intl-numberformat-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Função isfinita](/scripting/javascript/reference/isfinite-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função IsArray](/scripting/javascript/reference/array-isarray-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Função extensível](/scripting/javascript/reference/object-isextensible-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Função iscongelado](/scripting/javascript/reference/object-isfrozen-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Função IsInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Função isNaN](/scripting/javascript/reference/isnan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função isNaN (número)](/scripting/javascript/reference/number-isnan-function-number-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Formato de data ISO](/scripting/javascript/date-and-time-strings-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método IsPrototypeOf](/scripting/javascript/reference/isprototypeof-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função IsSealed](/scripting/javascript/reference/object-issealed-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método de itálico](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Iteradores](/scripting/javascript/advanced/iterators-and-generators-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método item](/scripting/javascript/reference/item-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Join](/scripting/javascript/reference/join-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto JSON](/scripting/javascript/reference/json-object-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Função Keys](/scripting/javascript/reference/object-keys-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método Keys (matriz)](/scripting/javascript/reference/keys-method-array-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Instrução rotulada](/scripting/javascript/reference/labeled-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade lastIndex](/scripting/javascript/reference/lastindex-property-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método lastIndexOf (matriz)](/scripting/javascript/reference/lastindexof-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método lastIndexOf (cadeia de caracteres)](/scripting/javascript/reference/lastindexof-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade lastMatch ($&)](/scripting/javascript/reference/lastmatch-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade lastParen ($ +)](/scripting/javascript/reference/lastparen-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método LBound](/scripting/javascript/reference/lbound-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade leftContext ($ ')](/scripting/javascript/reference/leftcontext-property-dollar-grave-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição de deslocamento à esquerda (<<=)](/scripting/javascript/reference/left-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Length (argumentos)](/scripting/javascript/reference/length-property-arguments-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Length (matriz)](/scripting/javascript/reference/length-property-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Length (função)](/scripting/javascript/reference/length-property-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Length (cadeia)](/scripting/javascript/reference/length-property-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador menor que (<)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador menor ou igual a (<=)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução Let](/scripting/javascript/reference/let-statement-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Método de link](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LN2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LN10](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método localeCompare](/scripting/javascript/reference/localecompare-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função log](/scripting/javascript/reference/math-log-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LOG2E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante LOG10E](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador lógico e operador (&&)](/scripting/javascript/reference/logical-and-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador lógico NOT (!)](/scripting/javascript/reference/logical-not-operator-decrement-exclpt-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador lógico ou (&#124;&#124;)](/scripting/javascript/reference/logical-or-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método MAP](/scripting/javascript/reference/map-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto MAP](/scripting/javascript/reference/map-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Método Match](/scripting/javascript/reference/match-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto matemático](/scripting/javascript/reference/math-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função máximo](/scripting/javascript/reference/math-max-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante MAX_VALUE](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade da mensagem](/scripting/javascript/reference/message-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função mín](/scripting/javascript/reference/math-min-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante MIN_VALUE](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição restante (% =)](/scripting/javascript/reference/modulus-assignment-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador restante (%)](/scripting/javascript/reference/modulus-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método moveFirst](/scripting/javascript/reference/movefirst-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método moveNext](/scripting/javascript/reference/movenext-method-enumerator-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Multiline](/scripting/javascript/reference/multiline-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição de multiplicação (* =)](/scripting/javascript/reference/multiplication-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de multiplicação (*)](/scripting/javascript/reference/multiplication-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Name](/scripting/javascript/reference/name-property-error-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NaN (global)](/scripting/javascript/reference/nan-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NaN (número)](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante NEGATIVE_INFINITY](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [novo operador](/scripting/javascript/reference/new-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador nonidentity (! = =)](/scripting/javascript/reference/comparison-operators-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função Now](/scripting/javascript/reference/date-now-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto Number](/scripting/javascript/reference/number-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade Number](https://developer.mozilla.org/docs/Web/JavaScript/Microsoft_Extensions/Error.number) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Object](/scripting/javascript/reference/object-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Precedência de operadores](/scripting/javascript/operator-subtractprecedence-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função Date. Parse](/scripting/javascript/reference/date-parse-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função JSON. Parse](/scripting/javascript/reference/json-parse-function-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Função parseFloat](/scripting/javascript/reference/parsefloat-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função parseInt](/scripting/javascript/reference/parseint-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante PI](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método pop](/scripting/javascript/reference/pop-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante POSITIVE_INFINITY](/scripting/javascript/reference/number-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função pow](/scripting/javascript/reference/math-pow-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função preventExtensions](/scripting/javascript/reference/object-preventextensions-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto Promise](/scripting/javascript/reference/promise-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Propriedade Prototype](/scripting/javascript/reference/prototype-property-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método propertyIsEnumerable](/scripting/javascript/reference/propertyisenumerable-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto proxy](/scripting/javascript/reference/proxy-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método push](/scripting/javascript/reference/push-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função Random](/scripting/javascript/reference/math-random-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função RAW](/scripting/javascript/reference/string-raw-function-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método de redução](/scripting/javascript/reference/reduce-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método reduceRight](/scripting/javascript/reference/reduceright-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Objeto RegExp](/scripting/javascript/reference/regexp-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto de expressão regular](/scripting/javascript/reference/regular-expression-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Sintaxe de expressões regulares](https://msdn.microsoft.com/ab0766e1-7037-45ed-aa23-706f58358c0e) | Y | Y | Y | Y | Y | Y | Y |  
| [Sinalizador de expressão regular/y](/scripting/javascript/reference/regular-expression-object-javascript) | N | N | N | N | N | Exp. | v 8.1: N <br /> V10: exp. |  
| [Método REPEAT (cadeia de caracteres)](/scripting/javascript/reference/repeat-method-string-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método Replace](/scripting/javascript/reference/replace-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Funções](/scripting/javascript/functions-javascript) | N | N | N | N | N | N | v 8.1: N <br /> V10: Y |  
| [Instrução return](/scripting/javascript/reference/return-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método reverso](/scripting/javascript/reference/reverse-method-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade rightContext ($ ')](/scripting/javascript/reference/rightcontext-property-dollar-regexp-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição de deslocamento à direita (>>=)](/scripting/javascript/reference/right-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ARRED](/scripting/javascript/reference/math-round-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ScriptEngine](/scripting/javascript/reference/scriptengine-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ScriptEngineBuildVersion](/scripting/javascript/reference/scriptenginebuildversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ScriptEngineMajorVersion](/scripting/javascript/reference/scriptenginemajorversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função ScriptEngineMinorVersion](/scripting/javascript/reference/scriptengineminorversion-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função lacre](/scripting/javascript/reference/object-seal-function-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método de pesquisa](/scripting/javascript/reference/search-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Definir objeto](/scripting/javascript/reference/set-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Método setDate](/scripting/javascript/reference/setdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setFullYear](/scripting/javascript/reference/setfullyear-method-date-javascript) |  | Y | Y | Y | Y | Y | Y |  
| [Método setHours](/scripting/javascript/reference/sethours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setmilisegundos](/scripting/javascript/reference/setmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setMinutes](/scripting/javascript/reference/setminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setMonth](/scripting/javascript/reference/setmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setSeconds](/scripting/javascript/reference/setseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setTime](/scripting/javascript/reference/settime-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCDate](/scripting/javascript/reference/setutcdate-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCFullYear](/scripting/javascript/reference/setutcfullyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCHours](/scripting/javascript/reference/setutchours-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCMilliseconds](/scripting/javascript/reference/setutcmilliseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCMinutes](/scripting/javascript/reference/setutcminutes-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCMonth](/scripting/javascript/reference/setutcmonth-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setUTCSeconds](/scripting/javascript/reference/setutcseconds-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método setYear](/scripting/javascript/reference/setyear-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Shift](/scripting/javascript/reference/shift-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função Sen](/scripting/javascript/reference/math-sin-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Slice (matriz)](/scripting/javascript/reference/slice-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método de fatia (cadeia de caracteres)](/scripting/javascript/reference/slice-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método pequeno](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [algum método](/scripting/javascript/reference/some-method-array-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método de classificação](/scripting/javascript/reference/sort-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Propriedade de origem](/scripting/javascript/reference/source-property-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Splice](/scripting/javascript/reference/splice-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Split](/scripting/javascript/reference/split-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Funções](/scripting/javascript/functions-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Função sqrt](/scripting/javascript/reference/math-sqrt-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante SQRT1_2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante SQRT2](/scripting/javascript/reference/math-constants-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [usar a diretiva estrita](/scripting/javascript/reference/use-strict-directive) | N | N | N | Y | Y | Y | Y |  
| [Método Strike](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto String](/scripting/javascript/reference/string-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função JSON. stringify](/scripting/javascript/reference/json-stringify-function-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Método sub](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método subst](/scripting/javascript/reference/substr-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método substring](/scripting/javascript/reference/substring-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição de subtração (-=)](/scripting/javascript/reference/subtraction-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de subtração (-)](/scripting/javascript/reference/subtraction-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método sup](/scripting/javascript/reference/html-tag-methods-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução switch](/scripting/javascript/reference/switch-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Symbol](/scripting/javascript/reference/symbol-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Função Tan](/scripting/javascript/reference/math-tan-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Cadeias de caracteres de modelo](/scripting/javascript/advanced/template-strings-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método de teste](/scripting/javascript/reference/test-method-regular-expression-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Esta instrução](/scripting/javascript/reference/this-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Instrução Throw](/scripting/javascript/reference/throw-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toArray](/scripting/javascript/reference/toarray-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toDateString](/scripting/javascript/reference/todatestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toexponencial](/scripting/javascript/reference/toexponential-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toFixed](/scripting/javascript/reference/tofixed-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toGMTString](/scripting/javascript/reference/togmtstring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toISOString](/scripting/javascript/reference/toisostring-method-date-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Método toJSON](/scripting/javascript/reference/tojson-method-date-javascript) | N | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleDateString](/scripting/javascript/reference/tolocaledatestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleLowercase](/scripting/javascript/reference/tolocalelowercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleString](/scripting/javascript/reference/tolocalestring-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleTimeString](/scripting/javascript/reference/tolocaletimestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toLocaleUppercase](/scripting/javascript/reference/tolocaleuppercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método tominúscula](/scripting/javascript/reference/tolowercase-method-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toPrecision](/scripting/javascript/reference/toprecision-method-number-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toString](/scripting/javascript/reference/tostring-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toTimeString](/scripting/javascript/reference/totimestring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método topercase](/scripting/javascript/reference/touppercase-method-string-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método toUTCString](/scripting/javascript/reference/toutcstring-method-date-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Trim](/scripting/javascript/reference/trim-method-string-javascript) | N | N | Y | Y | Y | Y | Y |  
| [Instrução try](/scripting/javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador typeof](/scripting/javascript/reference/typeof-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método UBound](/scripting/javascript/reference/ubound-method-vbarray-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto Uint8Array](/scripting/javascript/reference/uint8array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Uint16Array](/scripting/javascript/reference/uint16array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Uint32Array](/scripting/javascript/reference/uint32array-object) | N | N | N | Y | Y | Y | Y |  
| [Objeto Uint8ClampedArray](/scripting/javascript/reference/uint8clampedarray-object-javascript) | N | N | N | N | Y | Y | V8: não <br /> v 8.1 (Win): Sim <br /> v 8.1 (telefone): não <br /> V10: Y |  
| [Operador de negação unário (-)](/scripting/javascript/reference/subtraction-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Constante indefinida](/scripting/javascript/reference/undefined-constant-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função não escapar](/scripting/javascript/reference/unescape-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Caracteres de escape de ponto de código Unicode](/scripting/javascript/advanced/special-characters-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Método unshift](/scripting/javascript/reference/unshift-method-array-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de atribuição de deslocamento à direita não assinado (>>>=)](/scripting/javascript/reference/unsigned-right-shift-assignment-operator-decrement-equal-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Operador de deslocamento à direita não assinado (>>>)](/scripting/javascript/reference/unsigned-right-shift-operator-decrement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [usar a diretiva estrita](/scripting/javascript/reference/use-strict-directive) | N | N | N | Y | Y | Y | Y |  
| [Função UTC](/scripting/javascript/reference/date-utc-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método valueOf](/scripting/javascript/reference/valueof-method-object-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Método Value (array)](/scripting/javascript/reference/values-method-array-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Instrução var](/scripting/javascript/reference/var-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto VBArray](/scripting/javascript/reference/vbarray-object-javascript) | Y | Y | Y | Y | Y | Y | N |  
| [Operador void](/scripting/javascript/reference/void-operator-decrementjavascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto WeakMap](/scripting/javascript/reference/weakmap-object-javascript) | N | N | N | N | Y | Y | V8: N <br /> v 8.1: Y |  
| [Objeto fracoset](/scripting/javascript/reference/weakset-object-javascript) | N | N | N | N | N | Y | v 8.1: N <br /> V10: Y |  
| [Instrução while](/scripting/javascript/reference/while-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Objeto WinRTError](/scripting/javascript/reference/winrterror-object-javascript) | N | N | N | Y | Y | Y | Y |  
| [Instrução with](/scripting/javascript/reference/with-statement-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função escrever](/scripting/javascript/reference/debug-write-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
| [Função writeln](/scripting/javascript/reference/debug-writeln-function-javascript) | Y | Y | Y | Y | Y | Y | Y |  
  
 \ * Oferece suporte a objetos DOM, mas não a objetos definidos pelo usuário.  Os `enumerable` `configurable` atributos e podem ser especificados, mas não são usados.  
