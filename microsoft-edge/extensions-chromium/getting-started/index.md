---
description: Saiba mais sobre as extensões do Chromium e conceitos centrais para criar extensões.
title: Arquitetura e conceitos de extensões do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 8ffdd19e1a1e36a4d10fdd80bd7dd5654d543527
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104725"
---
# Arquitetura e conceitos de extensão

Este artigo fornece uma breve introdução aos conceitos que ajudam ao criar extensões. Para entender as extensões do Microsoft Edge \ (Chromium \), primeiro discutimos como funcionam os navegadores com várias guias.


## Entender como os navegadores funcionam

A lista a seguir descreve as informações úteis a serem compreendidas antes de criar a extensão.

1.  Cada guia do navegador é isolada de todas as outras guias.  Cada guia é executada em seu próprio thread isolado de outras guias do navegador e threads.

    ![Uma thread por guia do navegador](media/index-image1-browsertabs.png)  

2.  Cada guia manipula uma solicitação GET.  Cada guia usa uma URL para obter um único fluxo de dados, que normalmente é um documento HTML.  Esse único fluxo ou página, contém instruções como JavaScript incluem marcas, referências de imagem, referências CSS e muito mais.  Todos os recursos são baixados para uma única página da guia e, em seguida, a página é renderizada na guia.  

3.  A comunicação ocorre entre cada guia e os servidores remotos.  Cada guia é executada em um ambiente isolado. Ele ainda está conectado à Internet, mas está isolado de outras guias.  As guias podem executar JavaScript para se comunicar com servidores. Esses servidores são o servidor de origem da primeira solicitação GET inserida na barra de URL da guia.  

4.  O modelo de extensão usa um modelo de comunicação diferente.  Da mesma forma que as páginas da guia, as extensões são executadas em threads individuais que são isolados de todos os threads da página da guia.  As guias emitems únicas solicitações GET para servidores remotos e renderizam a página. No entanto, as funções de extensão são semelhantes a um servidor remoto. A instalação de extensões no navegador cria um servidor Web autônomo no navegador. A extensão é isolada de todas as páginas da guia.  

    ![Extensões usam um modelo de comunicação diferente](media/index-image3-upsidedown.png)  

## Arquitetura de extensão

A lista a seguir descreve as informações úteis relacionadas à arquitetura de uma extensão.  

1.  O pacote do servidor Web de extensão.  Uma extensão é um pacote de recursos da Web. Esses recursos da Web são semelhantes aos outros recursos publicados pelos desenvolvedores da Web em servidores Web. Os desenvolvedores agrupam esses recursos da Web em um arquivo zip ao criar uma extensão.
    
    O arquivo zip inclui arquivos HTML, CSS, JavaScript e image.  Há um arquivo adicional que é necessário na raiz do arquivo zip. Esse arquivo é o arquivo de manifesto e é nomeado `manifest.json` .  É o esquema da extensão e inclui a versão de sua extensão, o título, as permissões necessárias para que a extensão seja executada e assim por diante.

2.  Iniciando o servidor de extensão.  Os servidores Web contêm seu pacote da Web. Os navegadores navegam para URLs no servidor e baixam o arquivo para renderização no navegador. Navegadores navegam usando certificados, arquivos de configuração e assim por diante.  Se houver um `index.html` arquivo, ele será armazenado em um local especial no servidor Web.  

    Quando usamos extensões, a página da guia do seu navegador se obtém ao pacote da Web da extensão usando o tempo de execução de extensão.  O tempo de execução de extensão serve os arquivos da URL `extension://{some-long-unique-identifier}/index.html` , onde `{some-long-unique-identifier}` é um identificador exclusivo atribuído à extensão quando ele é instalado.  Cada extensão usa um identificador exclusivo diferente. Cada identificador aponta para o pacote da Web que está instalado no seu navegador.   

3.  As extensões podem se comunicar com guias e com a barra de ferramentas do navegador.   As extensões podem interagir com a barra de ferramentas do navegador. Cada extensão gerencia as páginas da guia em execução em threads separados, e a manipulação DOM em cada página da guia é isolada.  As extensões usam a API de extensões para se comunicar entre as páginas de extensão e guia.  Essa API de extensão fornece recursos adicionais que incluem gerenciamento de notificações, gerenciamento de armazenamento e assim por diante.  

    Da mesma forma que os servidores Web, as extensões aguardam notificações quando o navegador está aberto.  As extensões e as páginas da guia são executadas em threads isolados uns dos outros. No entanto, os desenvolvedores podem usar a API de extensões e permissões no arquivo de manifesto para permitir que uma extensão funcione com qualquer página da guia.  

4. As extensões fornecem permissões de consentimento no momento da instalação.  As permissões de extensão são especificadas pelo desenvolvedor no `manifest.json` arquivo. Ao instalar extensões, os usuários recebem informações sobre as permissões que a extensão precisa executar. Com base no tipo de permissão necessária, a extensão pode extrair e usar as informações do navegador.


## Próximas etapas

 Para obter informações sobre como começar a usar extensões, consulte [criar um tutorial de extensão][CreateAnExtensionPart1]. 



<!-- image links -->  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Criar um tutorial de extensão-parte 1 | Documentos da Microsoft"  