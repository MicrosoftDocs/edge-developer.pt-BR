---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Referência a códigos de console comuns e correções sugeridas
title: DevTools-códigos de erro e status do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, códigos de console
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: aa667941f619dcc0eac2411a087dbdfcf2fda613
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562243"
---
# Erros de console e códigos de status  

Essa referência ajuda a interpretar mensagens de erro e de status no [console](../console.md)do devtools.  Use a tabela a seguir para pesquisar códigos pelo prefixo \ (em que "x" representa um número&ndash;de 0 9 dígitos):

| Prefixo do código | Área | Descrição |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Política de segurança de conteúdo | Recursos bloqueados pelo uso de um `Content-Security-Policy` cabeçalho http.  |  
| [CSS31xx](#css-codes) | Folhas de estilos | Erros relacionados ao formato de fonte de fonte *aberta da Web* \ (WOFF \) e à fonte de fonte OpenType \ (EOT \) *incorporada* problemas de servidor host.  |  
| [HTML1112-1300](#html-codes) | HTML | A maioria desses são códigos herdados específicos dos conceitos do Microsoft Internet Explorer, como o *modo de documento* e o modo de *exibição de compatibilidade*.  |  
| [HTML1400-1532](#html5-parser-warnings) | Análise de HTML5 | Avisos de validação lançados pelo analisador HTML5.  |  
| [HTTP](#http-codes) | Erros e status do servidor | Códigos retornados de servidores remotos em resposta a solicitações HTTP.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | Erros de sintaxe JavaScript | Ocorre quando a estrutura de uma de suas instruções JavaScript viola uma ou mais das regras sintáticas.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | Erros de tempo de execução JavaScript | Ocorre quando o seu script tenta executar uma ação que o sistema não pode executar.  |  
| [SEC71xx](#security-codes) | Segurança | Reflete as condições de segurança que o Microsoft Edge aplica, como *proteção de rastreamento*e *conteúdo misto* .  |  
| [SVG560x](#svg-codes) | Elementos gráficos vetoriais escaláveis |  Não há suporte para a depuração SVG extensiva no momento, mas algumas mensagens de console são fornecidas para fins de depuração.  |  
| WebGL11_xxx | WebGL | Mensagens de erro do contexto WebGL.  Consulte também [erros de GLSL](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Erros na análise e na validação XML.  |  

## Códigos de CSP  

Os recursos bloqueados pelo uso de `Content-Security-Policy` um cabeçalho HTTP são relatados pelo console devtools e, opcionalmente, como um relatório de volta para o servidor.

| Código | Mensagem | Descrição | Correção sugerida |
|:--- |:--- |:--- |:--- |
| CSP14301 | "Falha ao analisar o \ [tipo de política \] porque \ <o motivo para cancelar a operação \ >--a política será ignorada." | O tipo de política de segurança especificado \ (por exemplo, script-src, base-URI \) falhou pelo motivo identificado e será ignorado.  | Verifique se você listou todos os recursos necessários de um tipo específico em uma única diretiva.  Por exemplo, in `script-src https://host1.com; script-src https://host2.com`, a segunda diretiva será ignorada.  O seguinte procedimento especifica corretamente ambas as origens como `script-src https://host1.com https://host2.com`válidas:.  |
| CSP14302 | "Falha ao analisar o código-fonte em \ [tipo de política \] para diretiva \ [tipo de Diretiva \] at \ [URL fonte \]--a origem será ignorada."                                                         | A maioria das diretivas de CSP exige uma ou mais fontes de conteúdo \ (indicando uma URL em que o conteúdo pode ser carregado \).  Esse erro indica uma política com uma diretiva que contém uma URL de origem que falhou quando a análise foi tentada.  | Verifique a fonte de conteúdo \ (geralmente uma URL \) que é definida na diretiva especificada, que você pode encontrar no tipo de política especificado.  Corrija ou substitua a URL de origem ou remova a política.  <br /> *\ * Sua política deve incluir uma diretiva de política src padrão, que é um fallback para outros tipos de recurso quando eles não têm políticas próprias.* |
| CSP14303 | A política "[tipo de política] estava vazia." | O tipo de política \ (por exemplo, conteúdo-segurança-política no cabeçalho HTTP \) está vazio.  | Uma referência rápida para configurar uma política de segurança de conteúdo pode ser encontrada [http://content-security-policy.com](http://content-security-policy.com)em.  |
| CSP14304 | "Fonte desconhecida \ [URL-fonte \] para diretiva \ [tipo de Diretiva \] in \ [tipo de política \] a origem será ignorada." | As fontes do conteúdo aprovado \ (seguro \) na diretiva identificada são desconhecidas e serão ignoradas.  | Verifique a fonte de conteúdo identificada \ (geralmente, é uma URL \) para verificar se ela está correta.  |
| CSP14305 | "Fonte sem suporte \ [URL da fonte \] para a diretiva [tipo de diretiva] em \ [tipo de política \] a origem será ignorada." | A fonte \ (URL, palavra-chave ou dados) listada nessa política não tem suporte e será ignorada.  | O endereço do site de origem pode incluir um caractere curinga inicial opcional \ (o caractere `*`de asterisco, \).  Por exemplo, http://`*`. foo.com ou mail.foo.com: *.  Os hosts são delimitados por espaço.  As fontes também podem ser palavras-chave \ (None, Self, UNSAFE, unsafe e unsafe-eval são all supported \) ou dados \ (dados: URIs, MediaStream: URIs \).  |
| CSP14306 | "Nenhuma fonte fornecida para a diretiva \ [tipo de Diretiva \] para \ [tipo de política \]--equivale a usar ' none ' e evitará o download de todos os recursos desse tipo." | Fazer uma diretiva e não listar qualquer fonte para conteúdo seguro para acessar é o mesmo que não permitir que todos os recursos do tipo especificado na diretiva sejam baixados.  | Uma fonte pode ser um ou mais nomes de host da Internet ou endereços IP, bem como um esquema de URL opcional e/ou número de porta.  |
| CSP14307 | "Source [URL de origem] já era fornecida para a diretiva \ [tipo de Diretiva \] para \ [tipo de política \]." | Uma origem duplicada \ (URL, palavra-chave ou dados \) foi listada nessa política e será ignorada.  | Remover a fonte duplicada identificada.  |
| CSP14308 | "Política de falha na análise em \ [tipo de política \] at [nome da diretiva]." | Falha na diretiva identificada.  Para obter orientação sobre como escrever diretivas com suporte, [http://content-security-policy.com](http://content-security-policy.com/)consulte.  | As diretivas devem ser separadas por ponto-e-vírgula.  Por exemplo, se você tiver um aplicativo que carrega todos os seus recursos a partir de uma rede de distribuição de conteúdo \ `https://cdn.example.net`(por exemplo, \) e souber que não precisa de conteúdo em enquadramento ou de qualquer plug-in, `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` a política poderá ter uma aparência semelhante a *um espaço apenas com ponto e vírgula, as fontes dentro de uma diretiva só deverão ser separadas por um espaço.* |
| CSP14309 | "Diretiva desconhecida em \ [nome da Diretiva \] em \ [tipo de política \]--a diretiva será ignorada." | A diretiva definida na política de CSP é desconhecida e será ignorada.  | Para obter uma lista de diretivas com suporte [http://content-security-policy.com](http://content-security-policy.com/), consulte.  |
| CSP14310 | "Diretriz sem suporte [nome da diretiva] em \ [tipo de política]--a diretiva será ignorada." | Foi encontrada uma política durante a análise no tipo de política \ (por exemplo, o `Content-Security-policy-Report-Only` campo de cabeçalho \) que não é suportado e será ignorada.  Para obter as diretivas com [http://content-security-policy.com](http://content-security-policy.com/)suporte, consulte.  | Remova a política sem suporte.  **Observação**: algumas diretivas não são compatíveis com o elemento \ <meta \ > ou no campo `Content-Security-policy-Report-Only` header.  |
| CSP14311 | "Diretiva \ [nome da Diretiva \] já foi fornecida em \ [tipo de política \]--a diretiva duplicada será ignorada." | Uma diretiva duplicada foi encontrada durante A análise, a segunda diretiva e suas expressões-fonte serão ignoradas.  | Remova o script duplicado.  |
| CSP14312 | Diretiva "recurso violated [nome da diretiva] no [tipo de política]: [URI de destino].  O recurso será bloqueado. " | Neste exemplo: o script "recurso violated Policy"-src MS-Appx: Data: ' unsafe-eval ' na política definida pelo host: script embutido.  O recurso será bloqueado. " | Um script embutido \ (URI de destino \) foi bloqueado devido à `'script-src ms-appx: data: 'unsafe-eval'` diretiva na política ' host defined '.  <br /> Os autores precisam mover todo o script embutido e o estilo fora da linha porque o agente do usuário não pode determinar se um script embutido foi injetado por um invasor.  Remova o script embutido e coloque-o em um arquivo externo.  |
| CSP14313 | Diretiva "recurso violated [nome da diretiva] no [tipo de política]: [URI de destino].  O recurso não será bloqueado porque a política está sendo somente para relatórios. " | Foi identificado um recurso que viola a diretiva especificada no campo de `Content-Security-policy-Report-Only` cabeçalho.  Como ele está em um `Report-Only` tipo de política, o recurso não será bloqueado.  | Mova a diretiva para um campo Content-Security-Security-Policy header se esse recurso deve ser bloqueado para proteger seu site.  |
| CSP14314 | "Falha ao enviar o relatório de violação de política para [URI de destino de destino] porque [razão para cancelar a operação]." | Houve um problema ao relatar uma violação de política, o destino de destino onde o relatório foi designado para ser enviado e o motivo pelo qual não o enviar deve ser identificado.  | A `report-uri` diretiva especifica uma URL na qual um navegador enviará relatórios quando uma política de segurança de conteúdo for violada.  *\ * Ele não pode ser usado nas marcas <meta \ >.* |
| CSP14315 | "Falha ao impor a diretiva de área restrita em [tipo de política] porque [razão para cancelar a operação]." | A política de área restrita falhou pelos motivos especificados.  Essa diretiva impõe restrições às ações que a página pode executar em vez de recursos que a página pode carregar.  Se a diretiva de área restrita estiver presente, a página será tratada como se tivesse sido carregada dentro de um iframe.  Ele pode evitar pop-ups e plug-ins e bloquear a execução do script.  | Mantenha o valor de área restrita vazio para manter todas as restrições no local ou adicione `allow-forms`valores `allow-same-origin`: `allow-scripts`,, `allow-top-navigation`e.  *\ * A diretiva de área restrita não é compatível com o elemento \ <meta \ > ou `Content-Security-policy-Report-Only` no campo header.* |
| CSP14316 | "Avaliação de script permitida devido à substituição do host." | Quando a diretiva `script-src` or `default-src` estiver incluída, o script `eval()` embutido será desabilitado, a `unsafe-inline` menos `unsafe-eval`que você especifique e, respectivamente.  | `'unsafe-eval'` permite o uso de `eval()` métodos semelhantes e semelhantes para a criação de código de cadeias de caracteres.  Você deve incluir as aspas simples.  ***Observação**: não é seguro e pode abrir seu site em vulnerabilidades de script entre sites. * |
| CSP14317 | "Frame [nome da fonte] permitido devido à substituição do host." | O quadro de origem identificado foi permitido devido a um conjunto de substituições na política de CSP do host.  | Uma política pode conter uma expressão de fonte nonce, o que significa que a origem pode ser usada apenas em uma ocasião, e o servidor deve gerar um valor novo para a diretiva toda vez que transmite uma política.  Os nonces substituem as restrições na diretiva em que estão presentes.  |

> [!NOTE]
> Para sites em uma zona de segurança confiável de um usuário, o Microsoft Edge não verifica o tipo MIME de uma folha de estilos.  

## Códigos CSS  

Esses erros estão no formato CSS31xx e estão relacionados ao formato de fonte de fonte *aberta* \ (WOFF \) e à fonte de fonte OpenType \ (EOT \) *inserida* e os problemas do servidor host.  

| Código | Mensagem | Descrição | Correção sugerida |
|:--- |:--- |:--- |:--- |
| CSS3111 | "@font-rosto encontrou o erro desconhecido" | Foi encontrado um problema desconhecido com o "formato de fonte aberta da Web \ (WOFF \)" e "fonte OpenType inserida \ (EOT \)" da fonte folhas de estilos em cascata \ (CSS \).  | Verifique a fonte das fontes do WOFF.  Experimente fonte ou face de fonte alternativa para ver se você pode reproduzir o problema.  |
| CSS3112 | "@font-face falha na verificação de integridade do WOFF" | A fonte do formato de fonte aberta da Web \ (WOFF \) pode estar corrompida, incompleta ou não no formato correto.  | Verifique a fonte das fontes.  Experimente um bom estilo de fonte ou fonte conhecida para ver se você pode reproduzir o problema.  |
| CSS3113 | "@font-face incompatível entre a origem do documento e a cadeia de caracteres raiz EOT" | A fonte não pode ser usada porque a URL \ (rootstring \) na fonte OpenType \ (EOT \) inserida não corresponde ao domínio do documento usando a fonte.  | A soma de verificação de URL na raiz EOT pode estar incorreta, indicando uma URL corrompida ou alterada para a fonte.  Verifique se a fonte está licenciada ou tem permissões para o site onde ele está sendo usado.  |
| CSS3114 | "@font-face falhou na verificação de permissão de inserção de OpenType.  A permissão deve ser instalada. " | A fonte-face não tem permissões para instalar com a página da Web atual.  | Obtenha a permissão ou as licenças corretas para inserir a fonte.  |
| CSS3115 | "@font-face não pode carregar fonte OpenType inválida". | O tipo de fonte não é válido para este uso.  | Obtenha a permissão ou as licenças para o rosto de fonte atual e válido.  |
| CSS3116 | "@font-face com falha na solicitação entre origens.  Sem cabeçalho Access-Control-Allow-Origin. " | A fonte pode não estar configurada para acesso de domínio cruzado.  | A fonte não é fornecida da mesma origem do documento.  Certifique-se de que o host que serve a fonte permite o uso dessa fonte usando o cabeçalho HTTP "Access-Control-Allow-Origin".                        |
| CSS3117 | "@font-face com falha na solicitação entre origens.  O acesso ao recurso é restrito. " | O cabeçalho "Access-Control-Allow-Origin" pode não ter sido configurado corretamente ou o host de fonte pode não permitir que essa fonte seja usada pela página.  | Verifique se o recurso tem as permissões corretas e um cabeçalho de resposta HTTP corretamente configurado que tenha origem de acesso de domínio cruzado no host servindo as fontes.  |
| CSS3118 | "Falha ao criar nova folha de estilos.  Há mais de \ [máximo \] folhas de estilos no documento. " | O Microsoft Edge criou mais de 4095 objetos de folha de estilos durante o processo de renderização da página.  | Pode ser um processo de JavaScript fora do controle ou um erro de sistema de compilação.  Reduza o número de objetos de folha de estilos sendo gerados.  |
| CSS3119 | "A consulta de mídia-MS-View-State foi preterida.  -as consultas de mídia do estado MS-View podem ser alteradas ou indisponíveis para lançamentos após o Windows 8,1.  Em vez disso, use consultas de largura máx e de largura mínima. " | Seu CSS contém uma `-ms-view-state` consulta de mídia.  | Use largura máx e largura mínima.  |

## Códigos HTML

Esses códigos estão no formato HTML1xxx, como HTML1115.  Muitos desses são códigos herdados específicos para conceitos do Internet Explorer, como *modo de documento* e modo de exibição de *compatibilidade*  

| Código | Mensagem | Descrição | Correção sugerida |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "Página inicial em reinicialização de \ [codificação \] para \ [codificação \]" | Foi especificado um CodePage diferente do CodePage do servidor.  | Use o mesmo código de página que o servidor para evitar esse erro.  |  
| HTML1113 | "Modo de documento reiniciar de \ [Mode \] para \ [Mode \]" | A página da Web requer um modo de documento diferente do qual o navegador está atualmente definido.  | Essa mensagem pode ocorrer quando o usuário navega de outra página, tornando-a do controle do desenvolvedor.  |  
| HTML1114 | "CodePage \ [Encoding \] from \ [Domain \] substitui a página de código de página conflitante \ [Encoding \] from \ [Domain \]" | As páginas de código especificadas nos cabeçalhos HTTP \ (de servidor \) e HTML \ (na página \) são diferentes umas das outras.  | Altere uma para que correspondam.  |  
| HTML1115 | Marca META compatível com X-UA \ (`[META tag]`\) ignorada porque o modo de documento já está finalizado " | Geralmente, a marca META foi colocada após uma declaração de "script" ou "Style", que corrigia o modo de documento para a página.  | Mova a marca META compatível com X-UA para o mais cedo possível no cabeçalho.  É uma prática recomendada colocá-lo logo após o título \ <title \ > e o valor charset.  |  
| HTML1116 | "Marca META compatível com x-UA \ (`[META tag]`\) ignorada devido à marca meta compatível anterior X-UA (`[META tag]`\)" | Há mais de uma marca "META" de "X-UA-Compatible" na seção \ <Head \ > do código-fonte.  | Remova tudo, exceto uma marca "META compatível com X-UA", e verifique se ela é o mais cedo possível no cabeçalho.  Uma prática recomendada é colocá-lo logo após o título \ <title \ > e o valor charset.  |  
| HTML1121 | "CodePage \ [Encoding \] não é permitido, somente a página de código \ [Encoding \] é permitida." | O conteúdo na página da Web chamou uma codificação de caracteres que não é permitida neste contexto.  | Verifique se todo o conteúdo usa a codificação permitida especificada na mensagem.  |  
| HTML1122 | "O Internet Explorer está em execução em modo empresarial emulando o IE8" | No momento, a página está sendo renderizada no modo empresarial, que é uma emulação do Windows Internet Explorer 8.  | Esse modo é configurado pelo gerenciamento de ti para sites específicos.  Se um usuário individual precisar desativá-lo em uma página da Web, desmarque a opção modo empresarial no menu ferramentas.  Para saber mais sobre o gerenciamento do modo empresarial, consulte a [documentação da ti](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | "`[domain]` é um site que você adicionou ao modo de exibição de compatibilidade." | O usuário selecionou o botão do **modo de exibição de compatibilidade** para o site atual ou o adicionou por meio das configurações do modo de exibição de **compatibilidade**.  | Iniciados pelo usuário.  |  
| HTML1202 | "`[domain]` está em execução no modo de exibição de compatibilidade porque" exibir sites da intranet no modo de exibição de compatibilidade "está marcada." | O usuário marcou a caixa de seleção **Exibir sites da intranet no modo de exibição de compatibilidade** nas **configurações do modo de exibição de compatibilidade**.  | O usuário precisa pressionar ALT + T, selecionar **as configurações do modo de exibição de compatibilidade**e desmarcar a caixa de seleção **Exibir sites da intranet no modo de exibição de compatibilidade** .  |  
| HTML1203 | "`[domain]` foi configurado para ser executado no modo de exibição de compatibilidade por meio da política de grupo." | O administrador de rede especificou que a página da Web foi executada no modo de exibição de compatibilidade.  | Você precisa entrar em contato com o administrador da rede.  |  
| HTML1204 | "`[domain]` está em execução no modo de exibição de compatibilidade porque" exibir todos os sites no modo de exibição de compatibilidade "está marcada." | O usuário marcou a caixa de seleção **Exibir todos os sites no modo de exibição de compatibilidade** nas **configurações do modo de exibição de compatibilidade**.  | O usuário precisa pressionar ALT + T, selecionar **as configurações do modo de exibição de compatibilidade**e desmarcar a caixa de seleção **Exibir todos os sites no modo de exibição de compatibilidade** .  |  
| HTML1300 | "Navegação ocorrida" | Uma nova página foi navegada ou a página atual foi atualizada.  | Esta é uma mensagem informativa, não um erro.  |  

## Avisos do analisador HTML5  

Os seguintes avisos podem ocorrer como parte da validação executada durante a análise de HTML.  Esses avisos não significam necessariamente que uma página seja quebrada, mas que o HTML fornecido seja inválido por meio do padrão HTML5.  O conteúdo criado em conformidade com versões anteriores das especificações HTML ou XHTML pode não ser válido em HTML5, principalmente em relação ao uso de DOCTYPEs.

Esses avisos geralmente indicam caracteres ausentes ou adicionais e marcas não coincidentes.  Quando você soluciona esses avisos, a compatibilidade com navegadores mais antigos e a conformidade de uma página da Web com o padrão HTML5 deve melhorar.  Para ajudar a identificar a origem de um aviso, ele inclui informações de deslocamento de linha e caractere, juntamente com um link apontando para o local onde o problema foi encontrado.

| Código     | Mensagem |  
| :--- |:--- |  
| HTML1400 | "Caractere inesperado no início da referência de caractere numérico.  Era esperado [0-9]. " |  
| HTML1401 | "Caractere inesperado na inicialização de referência de caractere numérico hexadecimal.  Espere o (a) Ed [0-9], [a-f] ou [A-F]. " |  
| HTML1402 | "A referência de caractere não tem um ponto-e-vírgula final"; "." |  
| HTML1403 | "A referência de caractere numérico não é resolvida para um caractere válido." |  
| HTML1404 | "Referência de caractere nomeado não reconhecido". |  
| HTML1405 | "Caractere inválido: U + 0000 NULL.  Caracteres nulos não devem ser usados. " |  
| HTML1406 | "Início de marca inválido: \ < \?.  Os pontos de interrogação não devem iniciar marcas. " |  
| HTML1407 | "Nome da marca inválido.  O primeiro caractere deve corresponder a [a-zA-Z]. " |  
| HTML1408 | "Marca de fim inválida \ </\ >.  As marcas de fim não devem estar vazias. " |  
| HTML1409 | "Caractere de nome de atributo inválido.  Os nomes de atributo não devem conter \ (\ "\), \ (\ ' \), \ (\ < \) ou \ (= \)". |  
| HTML1410 | "Valor de atributo sem aspas inválido.  Os valores de atributo sem aspas não devem conter \ (\ "\" \), \ (\ ' \), \ (\ < \), \ (= \) ou \ (\ ' \) ". |  
| HTML1411 | "Fim de arquivo inesperado". |  
| HTML1412 | "Comentário malformado.  Os comentários devem começar com \ < \!--\ >. " |  
| HTML1413 | "Caractere inesperado: U + 003E maior que" sinal \ (\ > \) " |  
| HTML1414 | "Caractere inesperado: 0021 de EXCLAMAção U (\! \)" |  
| HTML1415 | "Caractere inesperado: U + 002D hífen-sinal de subtração \ (-\)" |  
| HTML1416 | "Caractere inesperado no final do comentário.  Esperado "--\ >". " |  
| HTML1417 | "DOCTYPE vazio.  O DOCTYPE mais curto válido é \ < \! DOCTYPE HTML \ >. " |  
| HTML1418 | "Caractere inesperado em DOCTYPE." |  
| HTML1419 | "Palavra-chave inesperada em DOCTYPE.  "Público" ou "sistema" esperado. " |  
| HTML1420 | "Citação inesperada após a palavra-chave" PUBLIC "ou" SYSTEM ".  Espaço em branco esperado. " |  
| HTML1421 | "Marca final malformada.  As marcas de fim não devem conter atributos. " |  
| HTML1422 | "Marca de início malformada.  Uma barra de autofechamento deve ser seguida por um sinal de maior que U + 003E \ (\ > \). " |  
| HTML1423 | "Marca de início malformada.  Atributos devem ser separados por espaço em branco. " |  
| HTML1424 | "Caractere inválido" |  
| HTML1500 | "A marcação não pode ser autofechada.  Use uma marca de fechamento explícita. " |  
| HTML1501 | "Fim de arquivo inesperado". |  
| HTML1502 | "DOCTYPE inesperado.  Somente um DOCTYPE é permitido e ele deve ocorrer antes de qualquer elemento. " |  
| HTML1503 | "Marca de início inesperada". |  
| HTML1504 | "Marca de fim inesperada". |  
| HTML1505 | "Token de caractere inesperado". |  
| HTML1506 | "Token inesperado". |  
| HTML1507 | "Caractere inesperado: U + 0000 NULL.  Caracteres nulos não devem ser usados. " |  
| HTML1508 | "Marca de fim sem correspondência". |  
| HTML1509 | "Marca de fim sem correspondência". |  
| HTML1510 | "Nós obrigatórios fora do escopo". |  
| HTML1511 | "Elemento de nível de título inesperado encontrado fora do \ <Head \ >". |  
| HTML1512 | "Marca de fim sem correspondência". |  
| HTML1513 | "Extra \ <HTML \ > marca Fond.  Apenas um \ <marca HTML \ > deve existir por documento. " |  
| HTML1514 | Marca "extra \ <corpo \ > encontrada.  Só deve existir uma marca \ <corpo \ > por documento. " |  
| HTML1515 | "Encontrado \ <conjunto de quadros \ > muito longe do documento.  Essa marca deve ocorrer antes que um \ <corpo \ > seja criado. " |  
| HTML1516 | "Aninhamento inválido.  Uma marca de cabeçalho como \ <H1 \ > ou \ <H2 \ > não deve ser colocada dentro de outra marca de cabeçalho. " |  
| HTML1517 | "Aninhamento inválido.  Uma marca \ <forma \ > não deve ser colocada dentro de outro formulário \ <\ >. " |  
| HTML1518 | "Aninhamento inválido.  A marca A \ <do botão \ > não deve ser colocada dentro de outro \ <botão \ >. " |  
| HTML1519 | "Aninhamento inválido.  Uma marca \ <a \ > não deve ser colocada dentro de outro \ <a \ >. " |  
| HTML1520 | "Marca de início inesperada: o elemento \ <isindex \ > foi preterido e não deve ser usado." |  
| HTML1521 | "Inesperado \ </body\ > ou fim do arquivo.  Todos os elementos abertos devem ser fechados antes do fim do documento. " |  
| HTML1522 | "Marca de fim inválida: \ </br\ >.  Use \ <br \ > ou \ <br/\ > em vez disso. " |  
| HTML1523 | "Marca de fim da sobreposição.  Marcas devem ser estruturadas como \ <b \ > \ <i \ > \ </i\ > \ </b\ > em vez de \ <b \ > \ <i \ > \ </b\ > \ </i\ >. " |  
| HTML1524 | "DOCTYPE inválido.  O DOCTYPE mais curto válido é \ < \! DOCTYPE HTML \ >. " |  
| HTML1525 | "Marca HTML inesperada encontrada dentro do conteúdo estrangeiro \ (MathML/SVG \)." |  
| HTML1526 | "Aninhamento inválido.  Uma marca \ <nobr \ > não deve ser colocada dentro de outro \ <nobr \ >. " |  
| HTML1527 | "DOCTYPE esperado.  O DOCTYPE mais curto válido é \ < \! DOCTYPE HTML \ >. " |  
| HTML1528 | "Inesperada \ <imagem \ > em conteúdo HTML.  Use \ <img \ > em vez disso. " |  
| HTML1529 | "Valor do atributo xmlns: xlink inválido.  O valor deve ser "\ <https://w3.org/1999/xlink\>". " |  
| HTML1530 | "Texto encontrado dentro de um elemento de tabela estrutural.  O texto da tabela só pode ser colocado dentro de \ <legenda \ >, \ <TD \ > ou \ <th \ > elementos ". |  
| HTML1531 | "Valor do atributo xmlns inválido.  Para elementos SVG, o valor deve ser "\ https://w3.org/2000/svg/\><". " |  
| HTML1532 | "Valor do atributo xmlns inválido.  Para elementos MathML, o valor deve ser "\ https://w3.org/1998/Math/MathML/\><".  |  

## Códigos HTTP  

Os códigos de erro HTTP são retornados de servidores remotos em resposta a solicitações.  Provavelmente o mais familiar é o HTTP404, que é retornado sempre que o servidor não consegue encontrar a página ou o documento especificado no identificador de recursos uniforme \ (URI \).

| Código | Mensagem | Descrição |  
| :--- |:--- |:--- |  
| HTTP400 | SOLICITAÇÃO INCORRETA | Não foi possível processar a solicitação pelo servidor devido a sintaxe inválida.  |  
| HTTP401 | RECUSOU | O recurso solicitado requer autenticação do usuário.  |  
| HTTP402 | PAGAMENTO OBRIGATÓRIO | Não implementado no momento no protocolo HTTP.  |  
| HTTP403 | PROIBIDO | O servidor compreendeu a solicitação, mas está se recusando a atendê-la.  |  
| HTTP404 | NÃO ENCONTRADO | O servidor não encontrou nada que corresponda ao URI solicitado.  |  
| HTTP405 | MÉTODO INCORRETO | O verbo HTTP usado não é permitido.  |  
| HTTP406 | NENHUM ACEITÁVEL | Não foram encontradas respostas aceitáveis para o cliente.  |  
| HTTP407 | AUTENTICAÇÃO DE PROXY OBRIGATÓRIA | Autenticação de proxy obrigatória.  |  
| HTTP408 | TEMPO LIMITE DA SOLICITAÇÃO | O servidor expirou enquanto aguardava a solicitação.  |  
| HTTP409 | CONFLITOS | Não foi possível concluir a solicitação devido a um conflito com o estado atual do recurso.  |  
| HTTP410 | FORA | O recurso solicitado não está mais disponível no servidor, e nenhum endereço de encaminhamento é conhecido.  |  
| HTTP411 | COMPRIMENTO OBRIGATÓRIO | O servidor recusa-se a aceitar a solicitação sem um comprimento de conteúdo definido.  |  
| HTTP412 | FALHA NA PRECONDIÇÃO | A pré-condição fornecida em um ou mais campos de cabeçalho de solicitação avaliados como falso quando ele foi testado no servidor.  |  
| HTTP413 | CARGA MUITO GRANDE | O servidor está se recusando a processar uma solicitação porque a entidade de solicitação é maior do que o servidor está disposto ou pode processar.  |  
| HTTP414 | URI MUITO LONGO | O servidor está se recusando a atender a solicitação porque o URI da solicitação é maior do que o servidor está disposto a interpretar.  |  
| HTTP415 | TIPO DE MÍDIA SEM SUPORTE | O servidor está se recusando a atender a solicitação porque a entidade da solicitação está em um formato sem suporte pelo recurso solicitado para o método solicitado.  |  
| HTTP416 | INTERVALO SOLICITADO NÃO SATISFATÓRIO | O servidor não pode fornecer a parte do arquivo que o cliente solicitou.  A parte pode se estender além do fim do arquivo.  |  
| HTTP417 | FALHA NA EXPECTATIVA | O servidor não pode atender aos requisitos do campo de cabeçalho da solicitação esperada.  |  
| HTTP418 | ENVIAR UMA MENSAGEM DE CHAT A TEAPOT | O servidor é um teapot; Ele não pode brew café.  |  
| HTTP419 | TEMPO LIMITE DE AUTENTICAÇÃO | A autenticação válida anteriormente venceu.  |  
| HTTP422 | ENTIDADE NÃO PROCESSÁVEL | A solicitação foi bem formada, mas não foi possível processá-la devido a erros semânticos.  |  
| HTTP423 | TRANCA | O recurso que está sendo acessado está bloqueado.  |  
| HTTP424 | DEPENDÊNCIA COM FALHA | Falha na solicitação devido à falha de uma solicitação anterior.  |  
| HTTP426 | ATUALIZAÇÃO NECESSÁRIA | O cliente deve alternar para um protocolo diferente.  |  
| HTTP428 | PRÉ-CONDIÇÃO NECESSÁRIA | O servidor de origem requer que a solicitação seja condicional.  |  
| HTTP429 | MUITAS SOLICITAÇÕES | O servidor está se recusando a atender a solicitação porque muitas solicitações foram enviadas pelo cliente.  |  
| HTTP431 | CAMPOS DE CABEÇALHO DA SOLICITAÇÃO MUITO GRANDES | O servidor está se recusando a atender a solicitação porque um campo de cabeçalho ou todos os campos de cabeçalho coletivamente é maior do que o servidor está disposto ou pode processar.  |  
| HTTP449 | TENTE NOVAMENTE COM | A solicitação deve ser repetida depois de realizar a ação adequada.  |  
| HTTP500 | ERRO DO SERVIDOR | O servidor encontrou uma condição inesperada que o impedia de atender à solicitação.  |  
| HTTP501 | SEM SUPORTE | O servidor não é compatível com a funcionalidade necessária para atender à solicitação.  |  
| HTTP502 | GATEWAY INCORRETO | O servidor, ao atuar como gateway ou proxy, recebeu uma resposta inválida do servidor upstream que ele acessou ao tentar atender à solicitação.  |  
| HTTP503 | SERVIÇO INDISPONÍVEL | O serviço está temporariamente sobrecarregado.  |  
| HTTP504 | TEMPO LIMITE DO GATEWAY | A solicitação expirou enquanto aguardava um gateway.  |  
| HTTP505 | VERSÃO SEM SUPORTE | O servidor não dá suporte ou recusa-se a oferecer suporte, a versão do protocolo HTTP que foi usada na mensagem de solicitação.  |  
| HTTP506 | A VARIANTE TAMBÉM NEGOCIA | A negociação de conteúdo transparente para a solicitação resultou em referências circulares.  |  
| HTTP507 | ARMAZENAMENTO INSUFICIENTE | O servidor não pode armazenar a representação necessária para concluir a solicitação.  |  
| HTTP508 | LOOP DETECTADO | O servidor detectou um loop infinito durante a manutenção da solicitação.  |  
| HTTP510 | NÃO ESTENDIDO | Extensões adicionais à solicitação são necessárias para que o servidor a atenda.  |  
| HTTP511 | AUTENTICAÇÃO DE REDE NECESSÁRIA | O cliente deve autenticar para obter acesso à rede.  |  

## Erros de sintaxe JavaScript  

Erros de sintaxe JavaScript ocorrem quando a estrutura de uma de suas instruções viola uma ou mais das regras sintáticas.  

| Número do erro | Descrição |  
| --- | --- |  
| 1019 | [Não pode ter ' break ' fora do loop](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | [Não é possível ter ' continue ' fora do loop](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [A compilação condicional está desativada](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | ["default" só pode aparecer uma vez em uma instrução "switch"](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [Esperado ' \ ('](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [Esperado ' \) '](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | [Esperado '/'](/scripting/javascript/misc/expected-minus) |  
| 1003 | [Esperado ': '](/scripting/javascript/misc/expected-colon) |  
| 1004 | [Esperado '; '](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | [Esperado ' @ '](/scripting/javascript/misc/expected-at) |  
| 1029 | [Esperado ' @end '](/scripting/javascript/misc/expected-at-end) |  
| 1007 | [Esperado ' \] '](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | [Esperado ' {'](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | [Esperado '} '](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [Esperado ' = '](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | [' Catch ' esperado](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Constante esperada](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Dígito hexadecimal esperado](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Identificador esperado](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Identificador, cadeia ou número esperado](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | [Esperado ' While '](/scripting/javascript/misc/expected-while) |  
| 1014 | [Caractere inválido](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Rótulo não encontrado](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Rótulo redefinido](/scripting/javascript/misc/label-redefined) |  
| 1018 | [instrução ' Return ' fora da função](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Erro de sintaxe](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | [Throw deve ser seguido por uma expressão na mesma linha de origem](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Comentário não finalizado](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Constante de cadeia de caracteres não terminada](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Erros de host de script  

Os erros a seguir referem-se ao host de script, mas você pode vê-los ocasionalmente:  
  
| Erro | HRESULT | Descrição |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Um erro foi gravado e aprovado entre o mecanismo de script e o host.  O host precisa passar o código de erro para o chamador.  |  
| SCRIPT_E_REPORTED | 0x80020101 | O mecanismo de script relatou uma exceção não tratada para o host por meio de IActiveScriptSite:: OnScriptError.  O host pode ignorar esse erro.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Um erro de script que está sendo propagado para o chamador pode estar em um thread diferente.  O host deve passar o código de erro para o chamador.  |  

## Erros em tempo de execução JavaScript

Erros em tempo de execução JavaScript ocorrem quando o seu script tenta executar uma ação que o sistema não pode executar.  Você poderá ver erros de tempo de execução quando expressões variáveis estiverem sendo avaliadas ou quando a memória estiver sendo atribuída.

| Número do erro | Descrição |  
| --- | --- |  
| 5 | [Acesso negado](/scripting/javascript/misc/access-is-denied) |  
| 438 | [O objeto não dá suporte a essa propriedade ou método](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Memória insuficiente |  

### Erros do Windows Runtime  

 Se você estiver usando APIs do Windows Runtime \ (WinRT \), talvez veja erros de JavaScript que foram convertidos do tempo de execução do Windows HRESULTs.  O tempo de execução do Windows HRESULTs no intervalo de mais de 0x80070000 são convertidos em erros de JavaScript ao tirar o valor hexadecimal dos bits baixos e convertê-lo em um decimal.  Por exemplo, o HRESULT 0x80070032 é convertido no valor decimal 50, e o erro JavaScript é SCRIPT50.  O HRESULT 0x80074005 é convertido no valor decimal 16389, e o erro JavaScript é SCRIPT16389.

| Número do erro | Descrição |  
| --- | --- |  
| 5029 | [O comprimento da matriz deve ser um inteiro positivo finito](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [O comprimento da matriz deve ser atribuído a um número positivo finito](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Objeto Array ou Arguments esperado](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Booliano esperado](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [Não é possível atribuir ao resultado de uma função](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [Não é possível atribuir a "This"](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Não há suporte para a referência circular no argumento de valor](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Objeto Date esperado](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Objeto Enumerator esperado](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Exceção acionada e não detectada](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Esperado ') ' em expressão regular](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [Esperado ' &#93; ' em expressão regular](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [A função não tem um objeto prototype válido](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Função esperada](/scripting/javascript/misc/function-expected) |  
| 5008 | [Atribuição ilegal](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Intervalo inválido no conjunto de caracteres](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Argumento do substituidor inválido](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [Objeto JavaScript esperado](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Número esperado](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objeto esperado](/scripting/javascript/misc/object-expected) |  
| 5012 | [Membro do objeto esperado](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Objeto de expressão regular esperado](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Cadeia de caracteres esperada](/scripting/javascript/misc/string-expected) |  
| 5017 | [Erro de sintaxe em expressão regular](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [O número de dígitos fracionários está fora do intervalo](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [A precisão está fora do intervalo](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [O URI a ser decodificado não é uma codificação válida](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [O URI a ser codificado contém um caractere inválido](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Identificador não definido](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Quantificador inesperado](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [VBArray esperado](/scripting/javascript/misc/vbarray-expected) |  

## Códigos de segurança

Os `SEC7xxx` códigos de erro de segurança estão no formato, `SEC7113`como.  Esses erros refletem as condições de segurança que o Microsoft Edge aplica, como proteção de rastreamento e conteúdo misto.

| Código | Mensagem | Descrição | Correção sugerida |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "A segurança HTTPS está comprometida por [nome do recurso]" | Uma página Secure Hypertext Transfer Protocol \ (HTTPS \) tem conteúdo de uma fonte não segura.  | Certifique-se de que todo o conteúdo na página, incluindo scripts, objetos de folha de estilo e imagens, seja de fontes HTTPS.  |  
| SEC7112 | "Script from [URL] foi bloqueado devido à incompatibilidade de tipos MIME" | O cabeçalho de resposta HTTP para o arquivo JavaScript especificado pela URL tem um cabeçalho "X-Content-Type – opções: nofarejador" e não tem uma declaração de tipo de conteúdo reconhecido.  | Atualize o servidor para enviar o tipo de conteúdo correto para o arquivo JavaScript \ (como texto/JavaScript, aplicativo/JavaScript ", por exemplo \) no cabeçalho de resposta HTTP.  Para obter mais informações e uma lista completa de tipos de conteúdo, consulte [alterações de manipulação de MIME no Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | "CSS foi ignorada devido à incompatibilidade de tipos MIME" | Uma folha de estilos importada não foi usada porque o tipo MIME errado estava no cabeçalho HTTP.  | Verifique se o arquivo de folha de estilos é fornecido com o cabeçalho de resposta HTTP correto, que inclui um tipo de conteúdo de texto/CSS.  Para obter mais informações, consulte [alterações de manipulação de MIME no Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | "Um download nesta página foi bloqueado por proteção contra rastreamento. [URL fornecida aqui] " | O usuário bloqueou o script ou o conteúdo usando a proteção contra rastreamento.  | Nenhum-iniciado pelo usuário.  |  
| SEC7115 | ": visitado e: os estilos de link só podem ser diferentes por cor.  Alguns estilos não foram aplicados a: visitado. " | Mais de um atributo, como fonte ou tamanho, foram alterados usando os estilos de link visitado e de link.  | Alterar somente o atributo Color.  |  
| SEC7116 | "Acesso negado.  Falha ao revogar a URL entre origens: [URL]. " | Um script que tem um site de origem diferente do qual o blob tentou revogar uma URL de BLOB.  Devido a políticas de origem de BLOB, a tentativa falhou.  | Certifique-se de que todas as URLs de blob sejam revogadas usando scripts do mesmo site de origem que o documento que criou a URL de BLOB.  |  
| SEC7120 | "Origin [domain] not found in Access-Control-Allow-Origin header." | Na resposta a seu XMLHttpRequest, o cabeçalho Access-Control-Allow-Origin foi retornado com um valor que não contém ou corresponde ao valor de Origin do seu site.  | O recurso está retornando o tipo correto de códigos de cabeçalho, mas não está permitindo o seu site.  Entre em contato com o desenvolvedor responsável pelo recurso e solicite a atualização do cabeçalho Access-Control-Allow-Origin para que o seu site seja permitido.  Você pode apontá-los para [CORS para XHR no IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) para obter mais informações sobre o CORS em cabeçalhos de resposta.  |  
| SEC7121 | "Caractere curinga em Access-Control-Allow-Origin não permitido quando o sinalizador de credenciais está definido como true." | O servidor está retornando "Access-Control-Allow-Origin: *" nos cabeçalhos, mas isso não é permitido quando o `withCredentials` sinalizador está definido como **true** no XMLHttpRequest.  | O manipulador do lado do servidor deve ser modificado para retornar um cabeçalho Access-Control-Allow-Origin que permite especificamente o ponto de origem nesse tipo de solicitação.  Se não controlar o manipulador do lado do servidor, você precisará falar com o desenvolvedor que faz isso.  |  
| SEC7122 | "O sinalizador de credenciais foi definido como true, mas Access-Control-Allow-Credentials não estava presente ou não foi definido como" true ". | Uma XMLHttpRequest foi feita usando- `withCredentials` se o sinalizador.  O cabeçalho Access-Control-Allow-Credentials não era retornado ou foi retornado com um valor diferente de **true**.  | Pode haver um problema com suas credenciais ou com a resposta do servidor.  Consulte a [especificação XMLHttpRequest nível 2](https://w3.org/TR/XMLHttpRequest2/) para obter informações sobre solicitações credenciadas.  |  
| SEC7123 | "Cabeçalho de solicitação [Header] não está presente na lista Access-Control-Allow-Headers." | Um tipo de cabeçalho personalizado foi incluído na solicitação, mas a lista de acesso-controle-permissão-cabeçalhos da resposta não a incluiu.  | Verifique se o servidor permite cabeçalhos personalizados e permite que o mesmo seja enviado na solicitação.  |  
| SEC7124 | "Método de solicitação [método] não está presente na lista Access-Control-Allow-Methods." | Um método de solicitação, como POST, foi usado no XMLHttpRequest, mas a resposta retornou um cabeçalho Access-Control-Allow-Methods que não o incluiu.  | Verifique se o servidor permite esse tipo de método de solicitação e se você está usando `withCredentials` corretamente se esse método tiver acesso restrito.  |  
| SEC7125 | "XMLHttpRequest para [URL] causou uma falha na análise dos cabeçalhos de resposta." | Os cabeçalhos de resposta do servidor não puderam ser analisados; portanto, a solicitação falhou.  | Use a [ferramenta de rede](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspecionar os cabeçalhos de resposta para garantir que eles correspondam às [especificações CORS](https://w3.org/TR/cors/).  |  
| SEC7126 | "Redirecionamentos não são permitidos nas solicitações de pré-lançamento do CORS." | Um redirecionamento foi detectado no cabeçalho de origem, e o agente de usuário não seguirá redirecionamentos durante uma comprovação.  | Use a [ferramenta de rede](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspecionar os cabeçalhos de solicitação e verificar se há uma única origem direta.  |  
| SEC7127 | "O redirecionamento foi bloqueado para a solicitação CORS." | O caminho para o recurso CORS continha um redirecionamento que violou as regras de segurança.  | Verifique se você tem o caminho mais direto para o recurso CORS em seu XMLHttpRequest.  |  
| SEC7128 | "Vários cabeçalhos Access-Control-Allow-Origin não são permitidos para a resposta CORS". | O cabeçalho de resposta continha vários cabeçalhos Access-Control-Allow-Origin.  | Esse é um erro do lado do servidor.  O servidor deve retornar um cabeçalho Access-Control-Allow-Origin único.  Denuncie esse erro ao desenvolvedor responsável pelo recurso do lado do servidor.
| SEC7129 | "Vários cabeçalhos Access-Control-Allow-Credentials não são permitidos para a resposta CORS". | O cabeçalho de resposta continha vários cabeçalhos Access-Control-Allow-Credentials.  | Esse é um erro do lado do servidor.  O servidor deve retornar um único cabeçalho Access-Control-Allow-Credentials.  Denuncie esse erro ao desenvolvedor responsável pelo recurso do lado do servidor.  |  
| SEC7130 | "Possível script entre sites detectados em [URL].  O conteúdo foi modificado pelo filtro XSS. " | O [Filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx) detectou conteúdo potencialmente mal-intencionado na resposta do recurso e removeu o conteúdo ofensivo.  | Saiba mais sobre o [Filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx).  |  
| SEC7131 | "A segurança de um iframe em área restrita está potencialmente comprometida, permitindo que o script e o mesmo acesso à origem" sejam comprometidos. " | Se o conteúdo em um iframe em área restrita vier de uma fonte não confiável ou desprotegida, ele pode escapar da área restrita quando o script e o mesmo acesso à origem forem ambos permitidos.  | Esta é uma mensagem de aviso informativa e não deve afetar a funcionalidade.  Recomendamos que você evite combinar essas permissões, a menos que tenha certeza do que será executado no iframe.  |  
| SEC7132 | "O certificado que protege este site da Web usa criptografia fraca" | O certificado de segurança TLS usado por este site usa criptografia de baixa segurança | Atualize o certificado TLS do servidor |  

> [!NOTE]
> Para sites em uma zona de segurança confiável de um usuário, o Microsoft Edge não verifica o tipo MIME de uma folha de estilos.

## Códigos SVG  

DevTools atualmente, no momento, não oferece suporte a depuração de elementos gráficos vetoriais escaláveis extensos \ (SVG \), mas algumas mensagens de console são fornecidas para ajudar na depuração.

| Código | Mensagem | Descrição | Correção sugerida |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | "Os dados do caminho SVG têm formato incorreto e não foi possível analisá-los completamente." | A cadeia de caracteres de [caminho](https://msdn.microsoft.com/library/ff972086.aspx) SVG não está formatada corretamente ou contém comandos não reconhecidos.  | Verifique o formato dos comandos.  |  
| SVG5602 | "A lista de pontos SVG tem um formato incorreto e não foi possível analisá-la completamente." | A lista de pontos usados para um elemento, como uma [polilinha](https://msdn.microsoft.com/library/ff972113.aspx), é formatada incorretamente.  | Verifique se os pontos estão completos e formatados corretamente para o sistema de coordenadas usuários.  |  

## Códigos XML  

Os códigos XML estão na forma de XML5xxx, como XML5603.  

| Código | Mensagem |  
|:--- |:--- |  
| XML5001 | "Aplicando manipulação XSLT integrada." |  
| XML5601 | "MX_E_MX" |  
| XML5602 | "Fim inesperado da entrada". |  
| XML5603 | "Codificação não reconhecida". |  
| XML5604 | "Não é possível mudar a codificação". |  
| XML5605 | "Assinatura de codificação de entrada não reconhecida". |  
| XML5606 | "WC_E_WC" |  
| XML5607 | "Espaço em branco esperado". |  
| XML5608 | "Ponto-e-vírgula esperado." |  
| XML5609 | "Esperado" > "." |  
| XML5610 | "Caractere de aspas esperado." |  
| XML5611 | "Esperado" = "." |  
| XML5612 | "O caractere < não é permitido em valores de atributos." |  
| XML5613 | "Dígito hexadecimal esperado." |  
| XML5614 | "Dígito decimal esperado." |  
| XML5615 | "Esperada" ["." |  
| XML5616 | "Esperado" ("". " |  
| XML5617 | "Caractere XML ilegal". |  
| XML5618 | "Caractere de nome ilegal". |  
| XML5619 | "Sintaxe de documento incorreta". |  
| XML5620 | "Sintaxe da seção CDATA incorreta". |  
| XML5621 | "Sintaxe do comentário incorreto". |  
| XML5622 | "Sintaxe da seção condicional incorreta". |  
| XML5623 | "Sintaxe da declaração ATTLIST incorreta." |  
| XML5624 | "Sintaxe da declaração DOCTYPE incorreta." |  
| XML5625 | "Sintaxe da declaração de elemento incorreta". |  
| XML5626 | "Sintaxe da declaração de entidade incorreta". |  
| XML5627 | "Sintaxe da declaração NOTATION incorreta." |  
| XML5628 | "Era esperado" NDATA "." |  
| XML5629 | "Público" esperado "." |  
| XML5630 | "Sistema" esperado "." |  
| XML5631 | "Nome inválido". |  
| XML5632 | "Apenas um elemento raiz é permitido." |  
| XML5633 | "O nome da marca de fim não corresponde ao nome de marca inicial correspondente." |  
| XML5634 | "Já existe um atributo com o mesmo nome neste elemento." |  
| XML5635 | "Uma declaração XML só é permitida no início do arquivo." |  
| XML5636 | "Entrelinha" XML "." |  
| XML5637 | "Sintaxe da declaração de texto incorreta". |  
| XML5638 | "Sintaxe da declaração XML incorreta." |  
| XML5639 | "Sintaxe do nome da codificação incorreta". |  
| XML5640 | "Sintaxe do identificador público incorreto". |  
| XML5641 | "Referências de entidade de parâmetro não são permitidas em declarações de marcação em um subconjunto de DTD interno." |  
| XML5642 | "O texto de substituição para referências de entidade de parâmetro usado entre declarações de marcação deve conter uma série de declarações de marcação completas." |  
| XML5643 | "Uma entidade analisada não deve conter uma referência direta ou indireta a si mesma." |  
| XML5644 | "O conteúdo da entidade especificada não é bem-formado." |  
| XML5645 | "A entidade especificada não foi declarada". |  
| XML5646 | "A referência de entidade não pode conter o nome de uma entidade não analisada". |  
| XML5647 | "Os valores de atributo não devem conter referências diretas ou indiretas a entidades externas." |  
| XML5648 | "Sintaxe da instrução de processamento incorreta". |  
| XML5649 | "Sintaxe do identificador de sistema incorreto". |  
| XML5650 | "Um ponto de interrogação era esperado \ (\? \)". |  
| XML5651 | "O delimitador de CDATA de fechamento de seção"]] > "não deve ser usado no conteúdo de elemento." |  
| XML5652 | "Nem todos os blocos de dados foram lidos." |  
| XML5653 | "O DTD foi encontrado, mas está proibido." |  
| XML5654 | Atributo XML: Space encontrado com valor inválido.  Os valores válidos são "preserve" ou "default". " |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Caractere de nome qualificado ilegal". |  
| XML5657 | "Vários dois-pontos": "não devem ocorrer em um nome qualificado." |  
| XML5658 | "Dois-pontos": "não deve ocorrer em um nome." |  
| XML5659 | "Prefixo declarado". |  
| XML5660 | "O prefixo especificado não foi declarado." |  
| XML5661 | "Declarações de namespace não padrão não devem ter um URI vazio." |  
| XML5662 | "O prefixo" XML "é reservado e deve ter o URI"<https://w3.org/XML/1998/namespace/>"." |  
| XML5663 | "O prefixo" xmlns "é reservado para uso por XML." |  
| XML5664 | "O URI do namespace XML \ (\ https://w3.org/XML/1998/namespace/\>\) <só deve ser atribuído ao prefixo" XML "." |  
| XML5665 | "O URI do namespace xmlns \ (\ https://w3.org/2000/xmlns/\>\) <é reservado e não deve ser usado." |  
| XML5666 | "SC_E_SC" |  
| XML5667 | "A profundidade máxima de elementos aninhados foi excedida". |  
| XML5668 | "Número máximo de expansões de entidade excedido." |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: Writer: a cadeia de caracteres especificada não é espaço em branco." |  
| XML5671 | "WR_E_NSPREFIXDECLARED: Writer: o prefixo de namespace já está declarado com um namespace diferente." |  
| XML5672 | "WR_E_NSPREFIXWITHEMPTYNSURI: Writer: não é possível usar prefixo com URI de namespace vazio." |  
| XML5673 | "WR_E_DUPLICATEATTRIBUTE: Writer: atributo duplicado." |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: Writer: não é possível redefinir o prefixo xmlns." |  
| XML5675 | "WR_E_XMLPREFIXDECLARATION: Writer: o prefixo XML deve ter o URI https://w3.org/XML/1998/namespace/\> \ <". |  
| XML5676 | "WR_E_XMLURIDECLARATION: Writer: o URI do namespace XML \ ( https://w3.org/XML/1998/namespace/\>\) \ <deve ser atribuído somente ao prefixo" XML "." |  
| XML5677 | "WR_E_XMLNSURIDECLARATION: Writer: o URI do namespace xmlns \ ( https://w3.org/2000/xmlns/\>\) \ <está reservado e não deve ser usado." |  
| XML5678 | "WR_E_NAMESPACEUNDECLARED: Writer: o namespace não está declarado." |  
| XML5679 | "WR_E_INVALIDXMLSPACE: Writer: valor inválido do atributo XML: Space \ (os valores permitidos são" default "e" preserve "\)." |  
| XML5680 | "WR_E_INVALIDACTION: Writer: executar a ação solicitada resultaria em um documento XML inválido." |  
| XML5681 | "WR_E_INVALIDSURROGATEPAIR: Writer: a entrada contém um par substituto inválido ou incompleto." |  
| XML5682 | "Caractere inesperado na entidade de caracteres.  Era esperado um dígito decimal. " |  
| XML5683 | "Caractere inesperado na entidade de caracteres.  Era esperado um dígito hexadecimal. " |  
| XML5684 | "O valor Unicode da entidade do caractere especificado é inválido." |  
| XML5685 | "Codificação inválida". |  
| XML5686 | "Erro XML não especificado." |  
