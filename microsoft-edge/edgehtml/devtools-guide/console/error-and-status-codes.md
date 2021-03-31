---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Referência a códigos comuns de Console e correções sugeridas
title: DevTools - códigos de erro e status do Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools, códigos de console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da9facaa65b2bd2403d454c2041e2ad30dfcd112
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231962"
---
# Códigos de erro e status do console  

Esta referência ajuda você a interpretar as mensagens de erro e de status do [Console](../console.md) da DevTools.  Use a tabela a seguir para pesquisar códigos por seu prefixo \(em que "x" representa um número de 0&ndash;9 dígitos\):

| Prefixo do código | Área | Descrição |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Política de Segurança de Conteúdo | Recursos bloqueados pelo uso de um cabeçalho HTTP `Content-Security-Policy`.  |  
| [CSS31xx](#css-codes) | Folhas de estilo | Erros relacionados ao Formato de Fonte Aberta da Web \(WOFF\) e problemas do código fonte *Tipo Aberto Incorporado* \(EOT\) e de servidor host.  |  
| [HTML1112-1300](#html-codes) | HTML | A maioria delas são códigos herdados específicos para conceitos do Microsoft Internet Explorer, como *Modo de Documento* e *Modo de Exibição de Compatibilidade*.  |  
| [HTML1400-1532](#html5-parser-warnings) | Análise HTML5 | Avisos de validação lançados pelo analisador HTML5.  |  
| [HTTP](#http-codes) | Status e erros do servidor | Códigos retornados de servidores remotos em resposta a solicitações HTTP.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | Erros de sintaxe de JavaScript | Ocorre quando a estrutura de uma das instruções de JavaScript viola uma ou mais das regras sintáticas.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | Erros de tempo de execução no JavaScript | Ocorre quando o seu script tenta executar uma ação que o sistema não consegue executar.  |  
| [SEC71xx](#security-codes) | Segurança | Reflete as condições de segurança que o Microsoft Edge impõe, como *Conteúdo Misto* e *Proteção de Rastreamento*.  |  
| [SVG560x](#svg-codes) | Elementos Gráficos Vetoriais Escalonáveis |  Não há suporte para a depuração extensa de SVG no momento, mas algumas mensagens de console são fornecidas para fins de depuração.  |  
| WebGL11_xxx | WebGL | Mensagens de erro do contexto WebGL.  Confira também [Erros GLSL](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Erros na análise e validação de XML.  |  

## Códigos de CSP  

Os recursos bloqueados pelo uso de um cabeçalho HTTP `Content-Security-Policy` são relatados pelo console DevTools e opcionalmente como um relatório de volta para o servidor.

| Código | Mensagem | Descrição | Correção sugerida |
|:--- |:--- |:--- |:--- |
| CSP14301 | "Falha ao analisar o \[tipo de política\] porque \<the reason for canceling the operation\>-- a política será ignorada." | O tipo de política de segurança especificado \(por exemplo, script-src, base-uri\) falhou para o motivo identificado e será ignorado.  | Verifique se você listou todos os recursos necessários de um tipo específico em uma única diretiva.  Por exemplo, em `script-src https://host1.com; script-src https://host2.com`, a segunda diretiva será ignorada.  O que vem a seguir especifica corretamente ambas as origens como válidas: `script-src https://host1.com https://host2.com`.  |
| CSP14302 | "Falha na análise de fonte em \[tipo de política\] para diretiva \[tipo de diretiva\] em \[URL da origem\] -- a fonte será ignorada".                                                         | A maioria das diretrizes de CSP exige uma ou mais fontes de conteúdo \(indicando uma URL cujo conteúdo pode ser carregado a partir dela\).  Esse erro indica uma política com uma diretriz que contém uma URL de origem que falhou quando houve tentativa de análise.  | Verifique a fonte de conteúdo \(geralmente, uma URL\) definida na diretriz especificada, que você pode encontrar no tipo de política especificado.  Corrija ou substitua a URL de origem ou remova a diretriz.  <br /> *\*Sua política deve incluir uma política de política src padrão, que é um retorno para outros tipos de recurso quando não têm políticas próprias.* |
| CSP14303 | "A política [tipo de política] estava vazia". | O tipo de política \(por exemplo, conteúdo-segurança-política no cabeçalho HTTP \) está vazio.  | Uma referência rápida para configurar uma Política de Segurança de Conteúdo pode ser encontrada em [](http://content-security-policy.com).  |
| CSP14304 | "Fonte desconhecida \[URL de origem\] para diretiva \[tipo de diretiva\] em \[tipo de política\] -- a fonte será ignorada". | As fontes para conteúdo aprovado \(seguro\) na política identificada são desconhecidas e serão ignoradas.  | Verifique a fonte de conteúdo identificada \(geralmente, esta é uma URL\) para verificar se está correta.  |
| CSP14305 | "Fonte não suportada \[URL de origem\] para diretiva \[tipo de diretiva\] em \[tipo de política\] -- a fonte será ignorada". | A fonte listada \(URL, palavra-chave ou dados) nessa diretriz não tem suporte e será ignorada.  | O endereço do site de origem pode incluir um curinga opcional inicial \(o caractere de asterisco, `*`\).  Por exemplo, http://`*`.foo.com ou mail.foo.com: *.  Os hosts são delimitados por espaço.  As fontes também podem ser palavras-chave \(nenhum, self, unsafe-inline e unsafe-eval têm suporte\) ou dados \(dados:URIs, mediastream: URIs\).  |
| CSP14306 | "Sem fontes fornecidas para diretiva \[tipo de diretiva \] para \[tipo de política\]--equivale a usar "nenhum" e impedirá o download de todos os recursos desse tipo". | Dar a uma diretiva e não listar as fontes de conteúdo seguro para acessar é o mesmo que não permitir que todos os recursos do tipo especificado na diretiva sejam baixados.  | Uma fonte pode ser um ou mais nomes de host da Internet ou endereços IP, bem como um esquema de URL opcional e/ou número de porta.  |
| CSP14307 | "Fonte [URL de origem] já foi fornecida para diretiva \[tipo de diretiva\] para \[tipo de política\]." | Uma fonte duplicada \(URL, palavra-chave ou dados) foi listada nessa diretiva e será ignorada.  | Remover a fonte duplicada identificada.  |
| CSP14308 | "Política de falha na análise em \[tipo de política\] em [nome da diretriz]." | Falha na diretiva identificada.  Para obter instruções sobre como escrever diretrizes com suporte, consulte [http://content-security-policy.com](http://content-security-policy.com/).  | As diretivas devem ser separadas por ponto e vírgula.  Por exemplo, se você tiver um aplicativo que carregue todos os seus recursos a partir de uma rede de distribuição de conteúdo \(por exemplo, `https://cdn.example.net`\) e souber que não precisa de conteúdo com um frame ou de qualquer plug-in, sua política poderá ser semelhante: `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` *\*Enquanto as políticas estiverem separadas por ponto-e-vírgulas, as fontes dentro de uma diretiva só deverão estar separadas com um espaço.* |
| CSP14309 | "Diretiva desconhecida em \[nome da diretiva\] em \[tipo de política\] -- a política será ignorada". | A diretiva definida na política de CSP é desconhecida e será ignorada.  | Para obter uma lista de diretivas com suporte, consulte [http://content-security-policy.com](http://content-security-policy.com/).  |
| CSP14310 | "Diretiva não suportada em \[nome da diretiva\] em \[tipo de política\] -- a política será ignorada". | Foi encontrada uma diretiva durante a análise do tipo de política \(por exemplo, o campo de cabeçalho `Content-Security-policy-Report-Only`\) sem suporte e será ignorado.  Para diretivas com suporte, consulte [http://content-security-policy.com](http://content-security-policy.com/).  | Remova a política sem suporte.  **OBSERVAÇÃO**: algumas diretivas não têm suporte no elemento \<meta\> ou no campo de cabeçalho `Content-Security-policy-Report-Only`.  |
| CSP14311 | "A diretiva \[nome da diretiva\] já foi fornecida em \[tipo de política\] -- a diretiva duplicada será ignorada". | Encontrada uma diretiva duplicada durante a análise, a segunda diretiva e suas expressões de fonte serão ignoradas.  | Remova o script duplicado.  |
| CSP14312 | "Recurso violou a diretiva [nome da diretiva] em [tipo de política]: [URI de destino].  O recurso será bloqueado.” | Nesse exemplo: "Recurso violou diretiva 'script-src ms-appx: dados: 'unsafe-eval' em Política definida do Host: inline script.  O recurso será bloqueado.” | Um script embutido \(URI de destino\) foi bloqueado devido à diretiva `'script-src ms-appx: data: 'unsafe-eval'` na política 'host definido'.  <br /> Os autores devem mover todos os scripts embutidos e o estilo de saída porque o agente do usuário não consegue determinar se um script embutido foi injetado por um invasor.  Remova o script embutido e coloque-o em um arquivo externo.  |
| CSP14313 | "Recurso violou a diretiva [nome da diretiva] em [tipo de política]: [URI de destino].  O recurso não será bloqueado devido à política ser somente reportada. " | Foi identificado um recurso que viola a diretiva especificada no campo de cabeçalho `Content-Security-policy-Report-Only`.  Como ele se encontra em um tipo de política `Report-Only`, o recurso não será bloqueado.  | Mova a diretiva para um campo de cabeçalho de política de segurança de conteúdo se esse recurso deve ser bloqueado para proteger seu site.  |
| CSP14314 | "Falha ao enviar o relatório de violação de política para [URI de destino] porque [razão para cancelar a operação]." | Ocorreu um problema com o relato de uma violação de política, o destino para o qual o relatório deve ser enviado e o motivo pelo qual não foi enviado deve ser identificado.  | A diretiva `report-uri` especifica uma URL onde um navegador enviará relatórios quando uma política de segurança de conteúdo for violada.  *\*Não pode ser usado em marcas \<meta\>.* |
| CSP14315 | "Falha na imposição da diretiva de área restrita no [tipo de política] porque [razão para cancelar a operação]". | A diretiva de área restrita falhou devido aos motivos especificados.  Essa diretiva impõe restrições nas ações que a página pode executar em vez de em recursos que a página pode carregar.  Se a diretiva de área restrita estiver presente, a página será tratada como se tivesse sido carregada dentro de um iframe.  Ele pode evitar pop-ups e plug-ins e bloquear a execução de scripts.  | Mantenha o valor da área restrita vazio para manter todas as restrições no local ou adicione valores: `allow-forms`, `allow-same-origin`, `allow-scripts`e `allow-top-navigation`.  *\*A diretiva de área restrita não tem suporte no elemento \<meta\> ou no campo de cabeçalho `Content-Security-policy-Report-Only`.* |
| CSP14316 | "Script eval sendo permitido devido à substituição do host". | Quando a diretriz `script-src` ou `default-src` estiver incluída, os scripts embutidos e os `eval()` serão desabilitados, a menos que você especifique `unsafe-inline` e `unsafe-eval`, respectivamente.  | `'unsafe-eval'` permite o uso de `eval()` e métodos similares para a criação de códigos de cadeias de caracteres.  Você deve incluir as aspas simples.  ***OBSERVAÇÃO**: isso não é seguro e pode abrir o seu site para vulnerabilidades de script entre sites.* |
| CSP14317 | "Quadro [nome da origem] permitido devido à substituição do host". | O quadro de origem identificado foi permitido devido a um conjunto de substituições na política de CSP do host.  | Uma política pode conter uma expressão de fonte nonce, o que significa que a origem pode ser usada apenas em uma ocasião, e o servidor deve gerar um novo valor para a diretiva toda vez que transmitir uma política.  Os nonces substituem as restrições na diretiva em que estão presentes.  |

> [!NOTE]
> Para os sites da zona de segurança confiável de um usuário, o Microsoft Edge não verifica o tipo de MIME de uma folha de estilos.  

## Códigos CSS  

Esses erros estão no formato CSS31xx e estão relacionados ao *Formato de Fonte Aberta da Web* \(WOFF\) e problemas de código fonte *Tipo Aberto Incorporado* \(EOT\) e de servidor host.  

| Código | Mensagem | Descrição | Correção sugerida |
|:--- |:--- |:--- |:--- |
| CSS3111 | "@font-face encontrou um erro desconhecido" | Ocorreu um problema desconhecido com o "Formato de Fonte Aberta da Web \(WOFF \)" e "Fonte Tipo Aberta Incorporada \(EOT\)" da fonte das folhas de estilos em cascata \(CSS\).  | Verifique a origem das fontes WOFF.  Tente alternar a face de fonte ou origem para ver se você consegue reproduzir o problema.  |
| CSS3112 | "@font-face falhou na verificação de integridade WOFF" | A fonte de Formato de Fonte Aberta da Web \(WOFF\) pode estar corrompida, incompleta ou não ter o formato correto.  | Verifique a origem das fontes.  Experimente um bom tipo de fonte ou origem conhecida para ver se você consegue reproduzir o problema.  |
| CSS3113 | "@font-face incompatibilidade entre a origem do documento e a cadeia de caracteres raiz EOT" | Não é possível usar a fonte porque a URL \(raizstring\) na fonte Tipo Aberta Incorporada \(EOT\) não corresponde ao domínio do documento usando a fonte.  | A soma de verificação de URL na raizstring EOT pode estar incorreta, indicando uma URL corrompida ou alterada para a fonte.  Verifique se a fonte está licenciada ou se tem permissões para o site onde está sendo usada.  |
| CSS3114 | "@font-face falhou na verificação de permissão de incorporação de OpenType.  A permissão deve ser instalável." | O tipo de fonte não tem permissões para instalar com a página da Web atual.  | Obtenha a permissão ou licenças corretas para incorporar a fonte.  |
| CSS3115 | "@font-face não consegue carregar uma fonte OpenType inválida." | O tipo de fonte não é válido para esse uso.  | Obtenha a permissão ou licenças para o tipo de fonte atual e válida.  |
| CSS3116 | "@font-face falhou na solicitação entre origens.  Sem o cabeçalho Access-Control-Allow-Origin.” | A fonte pode não estar configurada para acesso entre domínios.  | A fonte não tem a mesma origem do documento.  Verifique se o host servindo a fonte permite o uso dessa fonte usando o cabeçalho HTTP "Access-Control-Allow-Origin".                        |
| CSS3117 | "@font-face falhou na solicitação entre origens.  O acesso ao recurso é restrito. " | O cabeçalho "Access-Control-Allow-Origin" pode não estar configurado corretamente ou o host de fonte pode não permitir que essa fonte seja usada pela sua página.  | Certifique-se de que o recurso tenha as permissões corretas e um cabeçalho de resposta HTTP corretamente configurado com origem de acesso entre domínios no host servindo as fontes.  |
| CSS3118 | "Falha ao criar nova folha de estilo.  Há mais de \[máximo\] folhas de estilo no documento. " | O Microsoft Edge criou mais de 4095 objetos de folha de estilo durante o processo de renderização da página.  | Pode ser um processo de JavaScript sem controle ou um erro de sistema de compilação.  Reduza o número de objetos de folha de estilo sendo gerados.  |
| CSS3119 | "A consulta de mídia – ms-view-state foi substituída.  As consultas de mídia ms-view-state podem ser alteradas ou estar indisponíveis para versões posteriores ao Windows 8.1.  Em vez disso, use as consultas max-width e min-width." | Sua CSS contém uma consulta de mídia `-ms-view-state`.  | Use max-width e min-width.  |

## Códigos HTML

Esses códigos estão no formato HTML1xxx, como HTML1115.  A maioria deles são códigos herdados específicos para conceitos do Microsoft Internet Explorer, como *Modo de Documento* e *Modo de Exibição de Compatibilidade*.  

| Código | Mensagem | Descrição | Correção sugerida |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "Página de código reiniciar de \[encoding\] para \[encoding \]" | Foi especificada uma página de código diferente da página de código do servidor.  | Use a mesma página de código que o servidor para evitar esse erro.  |  
| HTML1113 | "Modo de documento reiniciar de \[modo\] para \[modo\]" | A página da Web exige um modo de documento diferente do configurado para o navegador no momento.  | Esta mensagem pode ocorrer quando o usuário navega a partir de outra página, deixando-a fora do controle do desenvolvedor.  |  
| HTML1114 | "Página de código \[encoding\] de \[domínio\] substitui a página de código conflitante \[encoding\] de \[domínio\]" | As páginas de códigos especificadas nos cabeçalhos HTTP \(de servidor\) e HTML \(na página\) diferem entre si.  | Alterar uma para que correspondam.  |  
| HTML1115 | "Marca META compatível com X-UA \(`[META tag]`\) ignorada porque o modo de documento já está finalizado" | Geralmente, a marca META foi colocada após uma declaração de "script" ou "estilo", que corrigiu o modo de documento para a página.  | Mova a marca META compatível com X-UA para o mais cedo possível no cabeçalho.  É uma boa prática colocá-la logo após o \<title\> e o valor do conjunto de caracteres.  |  
| HTML1116 | "Marca META compatível com X-UA (`[META tag]`\) ignorada devido a uma marca META compatível com X-UA anterior \(`[META tag]`\)" | Há mais de uma marca "META" “compatível com de X-UA" na seção \<head\> do código-fonte.  | Remova todas, exceto uma marca "META compatível com X-UA", e verifique se ela está o mais cedo possível no cabeçalho.  Uma boa prática é colocá-la logo após o \<title\> e o valor do conjunto de caracteres.  |  
| HTML1121 | "Página de código \[encoding\] não é permitida. Somente a página de código \[encoding\] é permitida". | O conteúdo na página da Web invocou uma codificação de caracteres que não é permitida neste contexto.  | Verifique se todo o conteúdo usa a codificação permitida especificada na mensagem.  |  
| HTML1122 | "O Internet Explorer está em execução no Modo de Empresarial emulando o IE8" | A página está sendo processada no Modo Empresarial, que é uma emulação do Windows Internet Explorer 8.  | Esse modo é configurado pelo gerenciamento de TI para sites específicos.  Se um usuário individual precisar desativá-lo em uma página da Web, desmarque a opção Modo Empresarial no menu Ferramentas.  Para saber mais sobre o gerenciamento de Modo Empresarial, confira a [documentação de TI](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | "`[domain]` é um site que você adicionou ao Modo de Exibição de Compatibilidade." | O usuário escolheu o botão **Modo de Exibição de Compatibilidade** para o site atual ou o adicionou por meio das **Configurações do Modo de Exibição de Compatibilidade**.  | Iniciado pelo usuário.  |  
| HTML1202 | "`[domain]` está em execução no Modo de Exibição de Compatibilidade porque" Exibir sites da intranet no Modo de Exibição de Compatibilidade" está marcado.” | O usuário marcou a caixa de seleção Exibir sites da intranet no Modo de Exibição de Compatibilidade nas **configurações do Modo de Exibição de Compatibilidade**.  | O usuário precisa pressionar ALT+T, selecionar **configurações do Modo de Exibição de Compatibilidade**e desmarcar a caixa de seleção Exibir sites da intranet no Modo de Exibição de Compatibilidade.  |  
| HTML1203 | "`[domain]` foi configurado para ser executado no Modo de Exibição de Compatibilidade por meio da Política de Grupo." | O administrador de rede especificou que a página da Web deve ser executada no Modo de Exibição de Compatibilidade.  | Entre em contato com o administrador da rede.  |  
| HTML1204 | "`[domain]` está em execução no Modo de Exibição de Compatibilidade porque "Exibir todos os sites da intranet no Modo de Exibição de Compatibilidade" está marcado.” | O usuário marcou a caixa de seleção **Exibir todos os sites da intranet no Modo de Exibição de Compatibilidade** nas **configurações do Modo de Exibição de Compatibilidade**.  | O usuário precisa pressionar ALT+T, selecionar **configurações do Modo de Exibição de Compatibilidade**e desmarcar a caixa de seleção **Exibir todos os sites da intranet no Modo de Exibição de Compatibilidade**.  |  
| HTML1300 | "A navegação ocorreu" | Uma nova página foi navegada, ou a página atual foi atualizada.  | Essa é uma mensagem informativa, não de erro.  |  

## Avisos do analisador HTML5  

Os seguintes avisos podem ocorrer como parte da validação realizada durante a análise de HTML.  Esses avisos não significam necessariamente que uma página está quebrada, mas que a HTML fornecida é inválida pelo padrão HTML5.  O conteúdo criado em conformidade com versões anteriores das especificações HTML ou XHTML pode não ser válido no HTML5, particularmente no caso de usar DOCTYPEs.

Esses avisos costumam indicar caracteres ausentes ou adicionais e marcas incompatíveis.  Ao resolver esses avisos, a compatibilidade com navegadores mais antigos e a conformidade de uma página da Web com o padrão HTML5 deve melhorar.  Para ajudar a identificar a origem de um aviso, ele inclui informações de deslocamento de linha e caractere, juntamente com um link que aponta para o local onde o problema foi encontrado.

| Código     | Mensagem |  
| :--- |:--- |  
| HTML1400 | "Caractere inesperado no início de referência de caractere numérico.  Esperado [0-9]. " |  
| HTML1401 | "Caractere inesperado no início de referência de caractere numérico hexadecimal.  Esperado [0-9], [a-f] ou [A-F] ". |  
| HTML1402 | "O caractere de referência não tem um ponto e vírgula no final ";"." |  
| HTML1403 | "A referência de caractere numérico não é resolvida como um caractere válido". |  
| HTML1404 | "Referência de caractere nomeado não reconhecido". |  
| HTML1405 | "Caractere inválido: U+0000 NULL.  Caracteres Null não devem ser usados. " |  
| HTML1406 | "Início da marca inválido: \<\?.  Pontos de interrogação não devem iniciar marcas." |  
| HTML1407 | "Nome da marca inválido.  Primeiro caractere deve corresponder a [a-zA-Z]." |  
| HTML1408 | "Marca de fim inválida \</\>.  As marcas de fim não devem estar vazias. " |  
| HTML1409 | "Caractere nome do atributo inválido.  Nomes de atributo não devem conter \(\"\), \(\'\), \(\<\) ou \(=\)." |  
| HTML1410 | "Valor de atributo sem aspas inválido.  Valores de atributo sem aspas não devem conter \(\"\), \(\'\), \(\<\), \(=\) ou \(\`\)." |  
| HTML1411 | "Fim inesperado do arquivo." |  
| HTML1412 | "Comentário malformado.  Os comentários devem começar com \<\!-- \>." |  
| HTML1413 | "Caractere inesperado: U+003E SINAL MAIOR QUE \(\>\)" |  
| HTML1414 | "Caractere inesperado: U+0021 PONTO DE EXCLAMAÇÃO \(\!\) |  
| HTML1415 | "Caractere inesperado: U+002D HÍFEN-SINAL DE SUBTRAÇÃO \(-\)" |  
| HTML1416 | "Caractere inesperado no fim do comentário.  Esperado "--\>"." |  
| HTML1417 | "DOCTYPE vazio.  O menor doctype válido é \<\!DOCTYPE html\>." |  
| HTML1418 | "Caractere inesperado em DOCTYPE.” |  
| HTML1419 | "Palavra-chave inesperada em DOCTYPE.  Esperado "PUBLIC" ou "SYSTEM"." |  
| HTML1420 | "Aspas inesperadas após" "PUBLIC" ou "SYSTEM".  Espaço em branco esperado ". |  
| HTML1421 | "Marca de fim malformada.  Marcas de fim não devem conter atributos." |  
| HTML1422 | "Marca de início malformada.  Uma barra de fechamento duplo deve ser seguida por um SINAL MAIOR QUE U+003E (\>\). " |  
| HTML1423 | "Marca de início malformada.  Atributos devem ser separados por espaço em branco. " |  
| HTML1424 | "Caractere inválido   “ |  
| HTML1500 | "A marca não pode ser de autofechamento.  Use uma marca de fechamento explícita. " |  
| HTML1501 | "Fim inesperado do arquivo." |  
| HTML1502 | "DOCTYPE inesperado.  Somente um DOCTYPE é permitido e deve ocorrer antes de qualquer elemento. " |  
| HTML1503 | "Marca de início inesperada". |  
| HTML1504 | "Marca de fim inesperada.” |  
| HTML1505 | "Token de caractere inesperado.” |  
| HTML1506 | “Token inesperado.” |  
| HTML1507 | "Caractere inesperado: U+0000 NULL.  Caracteres Null não devem ser usados. " |  
| HTML1508 | "Marca de fim sem correspondência". |  
| HTML1509 | "Marca de fim sem correspondência". |  
| HTML1510 | "Nós necessários não estão no escopo". |  
| HTML1511 | "Elemento de nível de cabeçalho inesperado encontrado fora de \<head\>". |  
| HTML1512 | "Marca de fim sem correspondência". |  
| HTML1513 | "Encontrada marca \<html\> extra.  Apenas uma marca \<html\> deve existir por documento. " |  
| HTML1514 | "Encontrada marca \<body\> extra.  Apenas uma marca \<body\> deve existir por documento. " |  
| HTML1515 | "Encontrada \<frameset\> muito distante no documento.  Essa marca deve ocorrer antes que um \<body\> seja criado. " |  
| HTML1516 | "Aninhamento inválido.  Uma marca de cabeçalho como \<h1\> ou \<h2\> não deve ser colocada dentro de outra marca de cabeçalho." |  
| HTML1517 | "Aninhamento inválido.  Uma marca de \<form\> não deve ser colocada dentro de outra \<form\>". |  
| HTML1518 | "Aninhamento inválido.  Uma marca de \<button\> não deve ser colocada dentro de outra \<button\>". |  
| HTML1519 | "Aninhamento inválido.  Uma marca de \<a\> não deve ser colocada dentro de outra \<a\>". |  
| HTML1520 | "Marca de início inesperada: o elemento \<isindex\> foi substituído e não deve ser usado." |  
| HTML1521 | "\</body\> inesperado ou fim do arquivo.  Todos os elementos abertos devem ser fechados antes do fim do documento. " |  
| HTML1522 | "Marca de fim inválida: \</br\>.  Use \<br\> ou \<br /\> em vez disso. " |  
| HTML1523 | "Marca de fim sobreposta.  As marcas devem ser estruturadas como \<b\>\<i\>\</i\>\</b\> em vez de \<b\>\<i\>\</b\>\</i\>." |  
| HTML1524 | "DOCTYPE inválido.  O menor doctype válido é \<\!DOCTYPE html\>." |  
| HTML1525 | "Marca HTML inesperada encontrada em conteúdo estrangeiro \(MathML/SVG\)". |  
| HTML1526 | "Aninhamento inválido.  Uma marca de \<nobr\> não deve ser colocada dentro de outra \<nobr\>". |  
| HTML1527 | "DOCTYPE esperado.  O menor doctype válido é \<\!DOCTYPE html\>." |  
| HTML1528 | "\<image\> inesperado em conteúdo HTML.  Use \<img\> em vez disso.” |  
| HTML1529 | "Valor do atributo xmlns:xlink inválido.  O valor deve ser “\<https://w3.org/1999/xlink\>”.” |  
| HTML1530 | "Texto encontrado em um elemento de tabela estrutural.  O texto da tabela só pode ser colocado dentro dos elementos \<caption\>, \<td\>ou \<th\>." |  
| HTML1531 | "Valor do atributo xmlns inválido.  Para elementos SVG, o valor deve ser "\<https://w3.org/2000/svg/\>"." |  
| HTML1532 | "Valor do atributo xmlns inválido.  Para elementos MathML, o valor deve ser "\<https://w3.org/1998/Math/MathML/\>".  |  

## Códigos HTTP  

Códigos de erro são retornados de servidores remotos em resposta a solicitações.  Provavelmente o mais familiar é HTTP404, que é retornado quando o servidor não consegue encontrar a página ou o documento especificado no Identificador de Recursos Uniforme \(URI\).

| Código | Mensagem | Descrição |  
| :--- |:--- |:--- |  
| HTTP400 | SOLICITAÇÃO INVÁLIDA | A solicitação não pôde ser processada pelo servidor devido a uma sintaxe inválida.  |  
| HTTP401 | NEGADO. | O recurso solicitado requer a autenticação do usuário.  |  
| HTTP402 | PAGAMENTO OBRIGATÓRIO | Atualmente, não implementado no protocolo HTTP.  |  
| HTTP403 | PROIBIDO | O servidor compreendeu a solicitação, mas se recusou a atendê-la.  |  
| HTTP404 | NÃO ENCONTRADO | O servidor não encontrou nada que corresponda ao URI solicitado.  |  
| HTTP405 | MÉTODO INCORRETO | O verbo HTTP usado não é permitido.  |  
| HTTP406 | NENHUM ACEITÁVEL | Não foram encontradas respostas aceitáveis para o cliente.  |  
| HTTP407 | AUTENTICAÇÃO DE PROXY NECESSÁRIA | A autenticação de proxy é necessária.  |  
| HTTP408 | TEMPO LIMITE DA SOLICITAÇÃO | O servidor atingiu o tempo limite ao aguardar a solicitação.  |  
| HTTP409 | CONFLITO | A solicitação não foi concluída por causa de um conflito com o estado atual do recurso.  |  
| HTTP410 | DESAPARECIDO | O recurso solicitado não está mais disponível no servidor e nenhum endereço de encaminhamento é conhecido.  |  
| HTTP411 | COMPRIMENTO OBRIGATÓRIO | O servidor se recusa a aceitar a solicitação sem um comprimento de conteúdo definido.  |  
| HTTP412 | FALHA NA PRÉ-CONDIÇÃO | A pré-condição fornecida em um ou mais campos do cabeçalho de solicitação foi avaliada como falsa quando testada no servidor.  |  
| HTTP413 | CONTEÚDO MUITO GRANDE | O servidor se recusa a processar uma solicitação porque a entidade de solicitação é maior do que o servidor está disposto ou é capaz de processar.  |  
| HTTP414 | URI MUITO LONGO | O servidor se recusa a processar a solicitação porque a URI da solicitação é mais longa do que o servidor está disposto a interpretar.  |  
| HTTP415 | TIPO DE MÍDIA SEM SUPORTE | O servidor está se recusando a atender à solicitação porque a entidade da solicitação está em um formato sem suporte pelo recurso solicitado para o método solicitado.  |  
| HTTP416 | INTERVALO SOLICITADO NÃO SATISFATÓRIO | O servidor não pode fornecer a parte do arquivo solicitada pelo cliente.  A parte pode se estender além do fim do arquivo.  |  
| HTTP417 | FALHA NA EXPECTATIVA | O servidor não consegue atender aos requisitos do campo Espera de cabeçalho da solicitação.  |  
| HTTP418 | SOU UMA CHALEIRA | O servidor é uma chaleira. Não pode fazer café.  |  
| HTTP419 | TEMPO LIMITE DE AUTENTICAÇÃO | A autenticação válida anteriormente expirou.  |  
| HTTP422 | ENTIDADE NÃO PROCESSÁVEL | A solicitação foi bem formada, mas não pôde ser processada devido a erros semânticos.  |  
| HTTP423 | BLOQUEADO | O recurso que está sendo acessado está bloqueado.  |  
| HTTP424 | DEPENDÊNCIA FALHOU | A solicitação falhou devido a uma solicitação anterior.  |  
| HTTP426 | ATUALIZAÇÃO NECESSÁRIA | O cliente deve mudar para outro protocolo.  |  
| HTTP428 | PRÉ-CONDIÇÃO OBRIGATÓRIA | O servidor de origem exige que a solicitação seja condicional.  |  
| HTTP429 | NÚMERO EXCESSIVO DE SOLICITAÇÕES | O servidor está se recusando a atender à solicitação porque muitas solicitações foram enviadas pelo cliente.  |  
| HTTP431 | CAMPOS DE CABEÇALHO DA SOLICITAÇÃO MUITO GRANDES | O servidor está se recusando a atender à solicitação porque um campo de cabeçalho, ou todos os campos de cabeçalho coletivamente, são maiores do que o servidor está disposto ou poderá processar.  |  
| HTTP449 | TENTE NOVAMENTE COM | A solicitação deve ser repetida após executar a ação adequada.  |  
| HTTP500 | ERRO DO SERVIDOR | O servidor encontrou uma condição inesperada que impediu que ele atendesse à solicitação.  |  
| HTTP501 | SEM SUPORTE | O servidor não oferece suporte à funcionalidade necessária para atender à solicitação.  |  
| HTTP502 | GATEWAY INCORRETO | O servidor, ao atuar como gateway ou proxy, recebeu uma resposta inválida do servidor upstream que ele acessou ao tentar atender à solicitação.  |  
| HTTP503 | SERVIÇO INDISPONÍVEL | O serviço está temporariamente sobrecarregado.  |  
| HTTP504 | TEMPO LIMITE DO GATEWAY | A solicitação atingiu o tempo limite ao aguardar um gateway.  |  
| HTTP505 | VERSÃO NÃO SUPORTADA | O servidor não tem suporte ou se recusa a dar suporte à versão do protocolo HTTP que foi usada na mensagem de solicitação.  |  
| HTTP506 | A VARIANTE TAMBÉM NEGOCIA | A negociação de conteúdo transparente da solicitação resultou em referências circulares.  |  
| HTTP507 | ARMAZENAMENTO INSUFICIENTE | O servidor não pode armazenar a representação necessária para concluir a solicitação.  |  
| HTTP508 | LOOP DETECTADO | O servidor detectou um loop infinito enquanto atende à solicitação.  |  
| HTTP510 | NÃO ESTENDIDO | As extensões posteriores à solicitação são necessárias para o servidor atendê-la.  |  
| HTTP511 | AUTENTICAÇÃO DE REDE NECESSÁRIA | O cliente deve ser autenticado para obter acesso à rede.  |  

## Erros de sintaxe de JavaScript  

Erros de sintaxe ocorrem quando a estrutura de uma das instruções de JavaScript viola uma ou mais das regras sintáticas.  

| Número do erro | Descrição |  
| --- | --- |  
| 1019 | [Não pode haver 'intervalo' fora de loop](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | [Não pode haver 'continuação' fora de loop](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [Compilação condicional está desabilitada](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | ["default" só pode aparecer uma vez em uma instrução "switch"](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [Esperado '\('](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [Esperado '\)'](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | [Esperado '/'](/scripting/javascript/misc/expected-minus) |  
| 1003 | [Esperado '.'](/scripting/javascript/misc/expected-colon) |  
| 1004 | [Esperado ';'](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | [Esperado '@'](/scripting/javascript/misc/expected-at) |  
| 1029 | [Esperado '@end'](/scripting/javascript/misc/expected-at-end) |  
| 1007 | [Esperado '\]'](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | [Esperado '{'](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | [Esperado '}'](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [Esperado '='](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | [Esperado 'catch'](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Constante esperada](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Dígito hexadecimal esperado](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Identificador esperado](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Identificador, cadeia de caracteres ou número esperado](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | [Esperado 'while'](/scripting/javascript/misc/expected-while) |  
| 1014 | [Caractere inválido](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Rótulo não encontrado](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Rótulo redefinido](/scripting/javascript/misc/label-redefined) |  
| 1018 | [instrução 'return' fora da função](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Erro de sintaxe](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | [Throw deve ser seguido por uma expressão na mesma linha de origem](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Comentário não finalizado](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Constante de cadeia de caracteres não finalizada](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Erros de host de script  

Os seguintes erros referem-se ao host de script, mas você pode vê-los ocasionalmente:  
  
| Erro | HRESULT | Descrição |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Um erro foi gravado e transmitido entre o servidor e o mecanismo de script.  O host precisa passar o código de erro para o chamador.  |  
| SCRIPT_E_REPORTED | 0x80020101 | O mecanismo de script relatou uma exceção não tratada para o host por meio do IActiveScriptSite::OnScriptError.  O host pode ignorar este erro.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Um erro de script que está sendo propagado para o chamador pode estar em outro thread.  O host deve passar o código de erro para o chamador.  |  

## Erros de tempo de execução no JavaScript

Os erros de execução ocorrem quando o seu script tenta executar uma ação que o sistema não consegue executar.  Você pode ver erros de tempo de execução quando as expressões variáveis estão sendo avaliadas ou quando a memória está sendo alocada.

| Número do erro | Descrição |  
| --- | --- |  
| 5 | [Acesso negado](/scripting/javascript/misc/access-is-denied) |  
| 438 | [Objeto não dá suporte a essa propriedade ou método](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Sem memória |  

### Erros do Windows Runtime  

 Se você estiver usando as APIs do Windows Runtime \(WinRT\), você poderá ver erros de JavaScript que foram convertidos de HRESULTs para Windows Runtime.  Os HRESULTs para Windows Runtime no intervalo de 0x80070000s são convertidos em erros de JavaScript, colocando o valor hexadecimal dos bits baixos e convertendo-o em um decimal.  Por exemplo, o HRESULT 0x80070032 é convertido para o valor decimal 50 e o erro de JavaScript é SCRIPT50.  O HRESULT 0x80074005 é convertido para o valor decimal 16389 e o erro de JavaScript é SCRIPT16389.

| Número do erro | Descrição |  
| --- | --- |  
| 5029 | [O comprimento da matriz deve ser um número inteiro positivo finito](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [O comprimento da matriz deve ter um número inteiro positivo finito atribuído a ele](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Objeto array ou arguments esperado](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Booleano esperado](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [Não é possível atribuir um resultado de função](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [Não é possível atribuir a 'this'](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Referências circulares no argumento de valor não têm suporte](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Objeto Date esperado](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Objeto Enumerador esperado](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Exceção lançada e não detectada](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Esperado ')' em expressão regular](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [Esperado '&#93;' em expressão regular](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [Função não tem um objeto prototype válido](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Função esperada](/scripting/javascript/misc/function-expected) |  
| 5008 | [Atribuição ilegal](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Intervalo inválido no conjunto de caracteres](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Argumento de substituição inválido](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [Objeto JavaScript esperado](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Número esperado](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objeto esperado](/scripting/javascript/misc/object-expected) |  
| 5012 | [Objeto membro esperado](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Objeto Expressão Regular esperado](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Cadeia de caracteres esperada](/scripting/javascript/misc/string-expected) |  
| 5017 | [Erro de sintaxe em expressão regular](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [O número de dígitos fracionários está fora do intervalo](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [A precisão está fora do intervalo](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [O URI a ser decodificado não é uma codificação válida](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [O URI a ser codificado contém um caractere inválido](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Identificador indefinido](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Quantificador inesperado](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [VBArray esperado](/scripting/javascript/misc/vbarray-expected) |  

## Códigos de segurança

Os códigos de erro de segurança estão no formato `SEC7xxx`, como `SEC7113`.  Esses erros refletem as condições de segurança que o Microsoft Edge impõe, como conteúdo misto e proteção de rastreamento.

| Código | Mensagem | Descrição | Correção sugerida |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "A segurança de HTTPS está comprometida por [nome do recurso]" | Uma página do protocolo de transferência de hipertexto \(HTTPS\) seguro tem conteúdo de uma fonte não segura.  | Certifique-se de que todo o conteúdo na página, incluindo scripts, objetos de folha de estilo e imagens, seja de fontes HTTPS.  |  
| SEC7112 | "Script de [URL] foi bloqueado devido a um tipo de MIME incompatível" | O cabeçalho de resposta HTTP para o arquivo JavaScript especificado pela URL tem um cabeçalho "X-Content-Type-Type: nosniff" e não tem uma declaração de tipo de conteúdo reconhecida.  | Atualize o servidor para enviar o tipo de conteúdo correto para o arquivo JavaScript \(como texto/javascript, aplicativo/javascript", por exemplo\) no cabeçalho de resposta HTTP.  Para saber mais e obter uma lista completa de tipos de conteúdo, confira [Alterações de manipulação de MIME no Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | "CSS foi ignorada devido a tipo de mime incompatível" | Uma folha de estilos importada não foi usada porque o tipo de MIME errado estava no cabeçalho HTTP.  | Certifique-se de que o arquivo de folha de estilos seja fornecido com o cabeçalho de resposta HTTP correto, que inclui um tipo de conteúdo de texto/CSS.  Para saber mais, confira [Alterações de manipulação de MIME no Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | "Um download desta página foi bloqueado pela Proteção de Rastreamento.[URL fornecida aqui]" | O usuário bloqueou um script ou conteúdo usando a proteção contra rastreamento.  | Nenhum - iniciado pelo usuário.  |  
| SEC7115 | ":visitado e :estilos de link só podem diferir pela cor.  Alguns estilos não foram aplicados a :visitado." | Mais de um atributo, como fonte ou tamanho, foram alterados usando o visitado e estilos de link.  | Alterar apenas o atributo de cor.  |  
| SEC7116 | "Acesso negado.  Falha ao revogar URL entre origens: [URL] ". | Um script que tem um site de origem diferente do que o blob tentou revogar uma URL de blob.  Devido a políticas de origem de blob, a tentativa falhou.  | Certifique-se de que todas as URLs de blob sejam revogadas usando scripts do mesmo local de origem que o documento que criou a URL de blob.  |  
| SEC7120 | "Origem [domínio] não encontrada no cabeçalho Access-Control-Allow-Origin." | Na resposta ao seu XMLHttpRequest, o cabeçalho Access-Control-Allow-Origin era retornado com um valor que não contém ou corresponde ao valor de origem do seu site.  | O recurso está retornando o tipo correto de códigos de cabeçalho, mas não está permitindo o seu site.  Entre em contato com o desenvolvedor responsável pelo recurso e solicite a ele que atualize seus cabeçalhos Access-Control-Allow-Origin, para que o seu site seja permitido.  Você pode apontar para [CORS para XHR no IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) para saber mais sobre o CORS em cabeçalhos de resposta.  |  
| SEC7121 | "Caractere curinga no Access-Control-Allow-Origin não permitido quando o sinalizador de credenciais está definido como verdadeiro." | O servidor está retornando "Access-Control-Allow-Origin-Origin: *" nos cabeçalhos, mas isso não é permitido quando o sinalizador `withCredentials` está definido como **verdadeiro** no XMLHttpRequest.  | O manipulador do lado do servidor deve ser modificado para retornar um cabeçalho Access-Control-Allow-Origin que permita especificamente seu ponto de origem desse tipo de solicitação.  Caso não controle o manipulador do lado do servidor, você precisará falar com o desenvolvedor.  |  
| SEC7122 | "O sinalizador de credenciais foi definido como verdadeiro, mas Access-Control-Allow-Credentials não foi encontrado ou não foi definido como "true." | Um XMLHttpRequest foi feito usando o sinalizador `withCredentials`.  Um cabeçalho Access-Control-Allow-credenciais não foi retornado ou foi retornado com um valor diferente de **verdadeiro**.  | Pode haver um problema com as credenciais ou com a resposta do servidor.  Confira a [especificação XMLHttpRequest nível 2](https://w3.org/TR/XMLHttpRequest2/) para obter informações sobre solicitações credenciadas.  |  
| SEC7123 | "O cabeçalho da solicitação [cabeçalho] não estava presente na lista Access-Control-Allow-Headers." | Um tipo de cabeçalho personalizado foi incluído na solicitação, mas a lista do Access-Control-Allow-Headers não o inclui.  | Verifique se o servidor permite cabeçalhos personalizados e permite que ele seja enviado na solicitação.  |  
| SEC7124 | "O método da solicitação [método] não estava presente na lista Access-Control-Allow-Headers." | Um método de solicitação, como POST, foi usado em XMLHttpRequest, mas a resposta retornou um cabeçalho Access-Control-Allow-Methods que não o inclui.  | Verifique se o servidor permite esse tipo de método de solicitação e se você está usando o `withCredentials` corretamente caso esse método tenha acesso restrito.  |  
| SEC7125 | "XMLHttpRequest para [URL] causou uma falha na análise de cabeçalhos de resposta". | Os cabeçalhos de resposta do servidor não puderam ser analisados e a solicitação falhou.  | Use a [ferramenta de rede](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspecionar os cabeçalhos da resposta para garantir que eles atendam às [especificações CORS](https://w3.org/TR/cors/).  |  
| SEC7126 | "Redirecionamentos não são permitidos para solicitações de simulação de CORS." | Um redirecionamento foi detectado no cabeçalho de origem e o agente do usuário não acompanhará os redirecionamentos durante uma simulação.  | Use a [ferramenta de rede](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspecionar os cabeçalhos da solicitação e verifique se há uma única origem direta.  |  
| SEC7127 | "Redirecionamento bloqueado para requisição CORS". | O caminho para o recurso CORS continha um redirecionamento que violou as regras de segurança.  | Verifique se você tem o caminho mais direto para o recurso CORS em seu XMLHttpRequest.  |  
| SEC7128 | "Vários cabeçalhos Access-Control-Allow-Origin não são permitidos para a resposta CORS". | O cabeçalho de resposta continha vários cabeçalhos Access-Control-Allow-Origin.  | Esse é um erro do lado do servidor.  O servidor deve retornar um único cabeçalho Access-Control-Allow-Origin.  Relatar esse erro para o desenvolvedor responsável pelo recurso do lado do servidor.
| SEC7129 | "Vários cabeçalhos Access-Control-Allow-Credentials não são permitidos para a resposta CORS". | O cabeçalho de resposta continha vários cabeçalhos Access-Control-Allow-Credentials.  | Esse é um erro do lado do servidor.  O servidor deve retornar um único cabeçalho Access-Control-Allow-Credentials.  Relatar esse erro para o desenvolvedor responsável pelo recurso do lado do servidor.  |  
| SEC7130 | "Possível script entre sites detectado em [URL].  O conteúdo foi modificado pelo filtro XSS. " | O [filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx) detectado conteúdo potencialmente mal-intencionado na resposta do recurso e removeu o conteúdo ofensivo.  | Saiba mais sobre o [filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx).  |  
| SEC7131 | "A segurança de um iframe na área restrita fica potencialmente comprometida ao permitir script e acesso de mesma origem." | Se o conteúdo em um iframe na área restrita vier de uma fonte não confiável ou desprotegida, ele pode escapar da área restrita quando script e acesso de mesma origem forem permitidos.  | Esta é uma mensagem de aviso informativo e não deve afetar a funcionalidade.  Recomendamos evitar a combinação dessas permissões, a menos que você tenha certeza do que será executado no iframe.  |  
| SEC7132 | "O certificado de proteção deste site usa criptografia precária" | O certificado de segurança TLS usado por este site usa criptografia precária | Atualizar o certificado TLS do servidor |  

> [!NOTE]
> Para os sites da zona de segurança confiável de um usuário, o Microsoft Edge não verifica o tipo de MIME de uma folha de estilos.

## Códigos SVG  

DevTools atualmente não oferece suporte para a depuração de Gráficos Vetoriais Escalonáveis \(SVG\), mas algumas mensagens de console são fornecidas para ajudar com a depuração.

| Código | Mensagem | Descrição | Correção sugerida |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | "Dados do caminho SVG têm formato incorreto e não podem ser completamente analisados". | A cadeia de caracteres do [Caminho](https://msdn.microsoft.com/library/ff972086.aspx) SVG não está formatada corretamente ou contém comandos não reconhecidos.  | Verifique o formato dos comandos.  |  
| SVG5602 | "Lista do Ponto SVG têm formato incorreto e não pode ser completamente analisada". | A lista de pontos usados para um elemento, como uma [polilinha](https://msdn.microsoft.com/library/ff972113.aspx), está formatada incorretamente.  | Certifique-se de que os pontos estejam completos e formatados corretamente para o sistema de coordenadas usuários.  |  

## Códigos XML  

Os códigos XML estão na forma de XML5xxx, como XML5603.  

| Código | Mensagem |  
|:--- |:--- |  
| XML5001 | "Aplicação do Controle XSLT Integrado". |  
| XML5601 | "MX_E_MX" |  
| XML5602 | "Final de entrada inesperado". |  
| XML5603 | "Codificação desconhecida". |  
| XML5604 | "Não é possível mudar a codificação". |  
| XML5605 | "Assinatura de codificação de entrada não reconhecida". |  
| XML5606 | "WC_E_WC" |  
| XML5607 | “Espaço em branco esperado." |  
| XML5608 | "Ponto e vírgula esperado." |  
| XML5609 | "Esperado ">"." |  
| XML5610 | "Caractere de citação esperado". |  
| XML5611 | "Esperado "="." |  
| XML5612 | "O caractere < não é permitido em valores de atributos." |  
| XML5613 | “Dígito hexadecimal esperado.” |  
| XML5614 | “Dígito decimal esperado.” |  
| XML5615 | "Esperado "["." |  
| XML5616 | "Esperado "("." |  
| XML5617 | "Caractere XML ilegal." |  
| XML5618 | "Caractere de nome ilegal." |  
| XML5619 | "Sintaxe de documento incorreta." |  
| XML5620 | "Sintaxe da seção CDATA incorreta." |  
| XML5621 | "Sintaxe de comentário incorreta." |  
| XML5622 | "Sintaxe de seção condicional incorreta." |  
| XML5623 | "Sintaxe da declaração ATTLIST incorreta." |  
| XML5624 | "Sintaxe da declaração DOCTYPE incorreta." |  
| XML5625 | "Sintaxe da declaração ELEMENT incorreta." |  
| XML5626 | "Sintaxe da declaração ENTITY incorreta." |  
| XML5627 | "Sintaxe da declaração NOTATION incorreta." |  
| XML5628 | "Esperado "NDATA"." |  
| XML5629 | “Esperado "PUBLIC"." |  
| XML5630 | "Esperado "SYSTEM"." |  
| XML5631 | "Nome inválido." |  
| XML5632 | "Só é permitido um elemento raiz." |  
| XML5633 | "O nome da marca de término não corresponde ao nome de marca inicial correspondente". |  
| XML5634 | "Já existe um atributo com o mesmo nome neste elemento." |  
| XML5635 | "Uma declaração XML só é permitida no início do arquivo." |  
| XML5636 | ""xml" principal." |  
| XML5637 | "Sintaxe da declaração de texto incorreta". |  
| XML5638 | "Sintaxe da declaração XML incorreta". |  
| XML5639 | "Sintaxe do nome da codificação incorreta". |  
| XML5640 | "Sintaxe de identificador público incorreta". |  
| XML5641 | "Referências de entidade de parâmetro não são permitidas em declarações de marcação em um subconjunto DTD interno." |  
| XML5642 | "O texto de substituição para as referências de entidade de parâmetro usado entre as declarações de marcação deve conter uma série de declarações de marcação completas." |  
| XML5643 | "Uma entidade analisada não deve conter uma referência direta ou indireta a si mesma". |  
| XML5644 | "O conteúdo da entidade especificada não está bem formado". |  
| XML5645 | "A entidade especificada não foi declarada". |  
| XML5646 | "A referência de entidade não pode conter o nome de uma entidade não analisada". |  
| XML5647 | "Os valores de atributo não devem conter referências diretas ou indiretas a entidades externas". |  
| XML5648 | "Sintaxe da instrução de processamento incorreta". |  
| XML5649 | "Sintaxe de identificador do sistema incorreta". |  
| XML5650 | "Esperado um ponto de interrogação \(\?\)." |  
| XML5651 | "O delimitador de fechamento de seção CDATA "]]>" não deve ser usado no conteúdo de elemento." |  
| XML5652 | "Nem todas as partes de dados foram lidas." |  
| XML5653 | "O DTD foi encontrado, mas está proibido." |  
| XML5654 | "Encontrado atributo xml:space com valor inválido.  Os valores válidos são "preserve" ou "default"." |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Caractere de nome qualificado ilegal." |  
| XML5657 | "Vários dois-pontos ":" não devem ocorrer em um nome qualificado". |  
| XML5658 | "Dois pontos ":" não deve ocorrer em um nome". |  
| XML5659 | "Prefixo declarado." |  
| XML5660 | "O prefixo especificado não foi declarado." |  
| XML5661 | "Declarações de namespace não padrão não devem ter um URI vazio." |  
| XML5662 | "O prefixo" xml" está reservado e deve ter o URI "<https://w3.org/XML/1998/namespace/>"." |  
| XML5663 | "O prefixo "xmlns" está reservado para ser usado por XML." |  
| XML5664 | "O URI do namespace XML \(\<https://w3.org/XML/1998/namespace/\>\) só deve ser atribuído ao prefixo "xml"." |  
| XML5665 | "O URI do namespace xmlns \(\<https://w3.org/2000/xmlns/\>\) está reservado e não deve ser usado." |  
| XML5666 | "SC_E_SC" |  
| XML5667 | "Profundidade máxima de elementos aninhados excedida." |  
| XML5668 | "Número máximo de expansões de entidade excedido". |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: writer: a cadeia de caracteres especificada não é espaço em branco." |  
| XML5671 | "WR_E_NSPREFIXDECLARED: writer: o prefixo do namespace já está declarado com um namespace diferente." |  
| XML5672 | "WR_E_NSPREFIXWITHEMPTYNSURI: writer: não é possível usar prefixo com um URI de namespace vazio." |  
| XML5673 | "WR_E_DUPLICATEATTRIBUTE: writer: atributo duplicado." |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: writer: não é possível redefinir o prefixo xmlns." |  
| XML5675 | "WR_E_XMLPREFIXDECLARATION: writer: o prefixo xml deve ter o URI \<https://w3.org/XML/1998/namespace/\>". |  
| XML5676 | "WR_E_XMLURIDECLARATION: writer: o URI de namespace xml \(\<https://w3.org/XML/1998/namespace/\>\) deve ser atribuído somente a prefixo "xml"." |  
| XML5677 | "WR_E_XMLNSURIDECLARATION: writer: o URI do namespace xmlns \(\<https://w3.org/2000/xmlns/\>\) está reservado e não deve ser usado." |  
| XML5678 | "WR_E_NAMESPACEUNDECLARED: writer: namespace não declarado". |  
| XML5679 | "WR_E_INVALIDXMLSPACE: writer: valor inválido do atributo xml:space \(os valores permitidos são "default" e "preserve"\)." |  
| XML5680 | "WR_E_INVALIDACTION: writer: executar a ação solicitada resultaria em um documento XML inválido". |  
| XML5681 | "WR_E_INVALIDSURROGATEPAIR: writer: a entrada contém par substituto inválido ou incompleto." |  
| XML5682 | "Caractere inesperado na entidade do caractere.  Esperado um dígito decimal.” |  
| XML5683 | "Caractere inesperado na entidade do caractere.  Esperado dígito hexadecimal.” |  
| XML5684 | "O valor Unicode da entidade de caractere especificada é inválido". |  
| XML5685 | "Codificação inválida." |  
| XML5686 | "Erro XML não especificado." |  
