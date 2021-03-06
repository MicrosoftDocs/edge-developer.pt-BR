---
description: Saiba mais sobre Extensões de Chromium e conceitos principais para criar extensões.
title: Conceitos e arquitetura de extensões do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: 05732287bc1a782ed5830d5e7028cf5580f3b605
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397921"
---
# <a name="extension-concepts-and-architecture"></a>Conceitos de extensão e arquitetura  

Este artigo fornece uma breve introdução aos conceitos que ajudam você a criar uma extensão.  Para entender as extensões do Microsoft Edge \(Chromium\) siga em frente para entender como os navegadores de várias guias funcionam.  

## <a name="understand-how-browsers-work"></a>Entender como os navegadores funcionam  

A lista a seguir descreve informações úteis para entender antes de criar sua extensão.  

1.  Cada guia do navegador é isolada de todas as outras guias.  Cada guia é executado em um thread separado isolado de outras guias e threads do navegador.  
    
    :::image type="complex" source="./media/index-image1-browsertabs.png" alt-text="Um thread por guia do navegador" lightbox="./media/index-image1-browsertabs.png":::
       Um thread por guia do navegador  
    :::image-end:::  
    
1.  Cada guia lida com uma solicitação GET.  Cada guia usa uma URL para obter um único fluxo de dados, que normalmente é um documento HTML.  Esse único fluxo ou página inclui instruções como JavaScript incluem marcas, referências de imagem, referências CSS e muito mais.  Todos os recursos são baixados para essa página de uma guia e, em seguida, a página é renderizada na guia.  
1.  A comunicação ocorre entre cada guia e um servidor remoto.  Cada guia é executado em um ambiente isolado.  Cada guia ainda está conectada à Internet, mas cada uma é isolada de outras guias.  Uma guia pode executar JavaScript para se comunicar com um servidor.  O servidor é o servidor de origem da primeira solicitação GET que foi inserida na barra de URL da guia.  
1.  O modelo de extensão usa um modelo de comunicação diferente.  Semelhante a uma página de tabulação, uma extensão é executado em um thread individual isolado de outros threads de página de tabulação.  Uma guia envia solicitações GET simples para servidores remotos e renderiza a página.  No entanto, uma extensão funciona semelhante a um servidor remoto.  Instalar uma extensão em um navegador cria um servidor Web autônomo no navegador.  A extensão é isolada de todas as páginas de tabulação.  
    
    :::image type="complex" source="./media/index-image3-upsidedown.png" alt-text="As extensões usam um modelo de comunicação diferente" lightbox="./media/index-image3-upsidedown.png":::
       As extensões usam um modelo de comunicação diferente  
    :::image-end:::  
    
## <a name="extension-architecture"></a>Arquitetura de extensão  

A lista a seguir descreve informações úteis relacionadas à arquitetura de uma extensão.  

1.  O pacote do servidor Web extension.  Uma extensão é um pacote de recursos da Web.  Os recursos da Web são semelhantes a outros recursos que você \(o desenvolvedor da Web\) publica em servidores Web.  Você agrupa os recursos da Web em um arquivo zip ao criar uma extensão.  
    
    O arquivo zip inclui arquivos HTML, CSS, JavaScript e imagem.  Mais um arquivo é necessário na raiz do arquivo zip.  O outro arquivo é o arquivo de manifesto chamado `manifest.json` .  O arquivo de manifesto é o modelo da extensão e inclui a versão da extensão, o título, as permissões necessárias para a extensão ser executado e assim por diante.  
    
1.  Iniciando o servidor de extensão.  Os servidores Web contêm seu pacote da Web.  Um navegador navega até URLs no servidor e baixa o arquivo para renderizar no navegador.  Um navegador navega usando certificados, arquivos de configuração e assim por diante.  Se um `index.html` arquivo for especificado, o arquivo será armazenado em um local especial no servidor Web.  
    
    Quando você usa uma extensão, a página de tabulação do navegador chega ao pacote da Web da extensão usando o tempo de execução da extensão.  O tempo de execução da extensão atende aos arquivos da URL , onde é um identificador exclusivo atribuído à extensão `extension://{some-long-unique-identifier}/index.html` `{some-long-unique-identifier}` durante a instalação.  Cada extensão usa um identificador exclusivo diferente.  Cada identificador aponta para o pacote da Web instalado no navegador.  
    
1.  Uma extensão pode se comunicar com as guias e a barra de ferramentas do navegador.  Uma extensão pode interagir com a barra de ferramentas do navegador.  Cada extensão gerencia páginas de tabulação em threads separados e a manipulação dom em cada página de tabulação é isolada.  Uma extensão usa a API de extensões para se comunicar entre as páginas de extensão e de tabulação.  A API de extensões fornece recursos extras que incluem gerenciamento de notificações, gerenciamento de armazenamento e assim por diante.  
    
    Assim como os servidores Web, uma extensão aguarda notificações quando o navegador está aberto.  Uma extensão e páginas de tabulação são executados em threads isolados uns dos outros.  Para permitir que uma extensão funcione com qualquer página de guia, use a API de extensões e de definir as permissões no arquivo de manifesto.  
    
1.  Uma extensão fornece permissões de aceitação no momento da instalação.  Você especifica as permissões de extensão no `manifest.json` arquivo.  Quando um usuário instala uma extensão, as informações sobre as permissões que a extensão exige são exibidas.  Com base no tipo de permissão necessário, a extensão pode extrair e usar informações do navegador.  
    
## <a name="next-steps"></a>Próximas etapas  

Para obter informações sobre como começar com sua extensão, navegue até [Criar um tutorial de extensão.][CreateAnExtensionPart1]  

<!-- links -->  

[CreateAnExtensionPart1]: ./part1-simple-extension.md "Criar um tutorial de extensão - Parte 1 | Microsoft Docs"  
