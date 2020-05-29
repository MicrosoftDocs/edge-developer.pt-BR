---
description: Saiba o que é uma extensão Chromium e crie progressivamente uma extensão de visualização de imagem completa que inclui opções, injeção de conteúdo, scripts em segundo plano, armazenamento e muito mais.
title: Introdução às extensões do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: a271514f39ed8bbe379116c33e23c973d3eb6adb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561308"
---
# Introdução às extensões do Microsoft Edge \ (Chromium \)  

Se quiser saltar diretamente para criar sua primeira extensão, vá para a parte 1 da construção de uma imagem da NASA da extensão do dia.  

Se você não estiver familiarizado com os conceitos e a arquitetura da extensão, continue a ler e saiba tudo sobre quais extensões estão.  Essas informações ajudam você a criar extensões muito mais fáceis, pois você compreende as motivações e a arquitetura por trás delas.  

## Criar uma imagem da NASA da extensão do dia  

Cada seção tem o pacote de instalação de origem de extensão concluído referenciado.  

*   [Criar uma extensão simples que é exibida na imagem de NASA do dia](part1-simple-extension.md)  
    *   Criando um manifesto  
    *   Atribuir ícones de extensão  
    *   Exibindo uma janela pop-up  
    *   Executar a extensão localmente no navegador \ (carregando \)  

*   [Inserir dinamicamente a imagem da NASA abaixo da marca de corpo da página](part2-content-scripts.md)  
    *   Criar JavaScript que insere o script de conteúdo dinâmico  
    *   Definir no manifesto quais páginas recebem o script de conteúdo  
    *   Injetar script de conteúdo declarativamente  
    *   Adicionar um botão ao pop-up para enviar uma mensagem para um script de conteúdo  
    *   Receber uma mensagem dentro de um script de conteúdo  

## Noções básicas sobre o navegador antes de as extensões serem introduzidas  

### Cada guia do navegador é isolada de todas as outras guias  

Para entender o que é uma extensão do Microsoft Edge \ (Chromium \), primeiro precisamos compreender completamente o que é um navegador de várias guias, como o Microsoft Edge, principalmente.  Para começar, cada guia do navegador é executada em um thread individual que o isola efetivamente de outras guias do navegador \ (ou threads \).  

![Uma thread por guia do navegador](media/index-image1-browsertabs.png)  

### Cada guia manipula uma solicitação GET  

Cada guia basicamente usa a URL \ (também conhecida como o localizador de recursos uniforme \) para obter um único fluxo de dados, que normalmente é um documento HTML.  Esse único fluxo \ (ou página \), muitas vezes inclui instruções \ (como JavaScript incluem marcas, referências de imagem, referências CSS e mais \).  Em última análise, todos os recursos necessários são baixados para uma única página da guia e normalmente é exibida uma visualização que vemos na guia do navegador completamente renderizada.  

### Todas as comunicações de cada guia são para servidores remotos  

Entender que cada guia é executada em um ambiente isolado significa que essas guias são isoladas uma da outra, mas não a Internet mais recente.  Geralmente, essas guias, que executam JavaScript, são uma linguagem de programação, comunicam-se de volta para o servidor, que deve ser pensada como o servidor de origem dessa primeira solicitação que foi inserida na barra de URL na parte superior da guia do navegador.  

## O modelo de extensão transforma tudo de cabeça para baixo  

Uma extensão, exatamente como as páginas da guia, é executada em um thread individual que é completamente isolado de todos os threads de página da guia que são abordados.  Ao contrário das guias cujo trabalho geralmente emite uma única solicitação GET para um servidor remoto e, em seguida, exibe uma visualização desses dados no navegador, a extensão, por outro lado, é o servidor, que anteriormente residau na outra extremidade da conexão à Internet feita a partir de uma guia do navegador.  

![O modelo de extensão transforma o modelo de servidor de cabeça para baixo](media/index-image3-upsidedown.png)  

Isso é muito importante compreender.  Depois de criar uma extensão e instalá-la no seu navegador, você criou um servidor Web autônomo que está morando e livrendo dentro do seu navegador, mas ainda isolado de cada página da guia em execução nesse navegador.  

### O pacote do servidor Web de extensão  

Então, o que é uma extensão? É um pacote \ (ou conhecido como um arquivo zip \) de recursos da Web que não são diferentes dos que um desenvolvedor da Web publica em um servidor Web.  

Esse arquivo zip inclui HTML, CSS, JavaScript, imagens e todos os ativos necessários para criar uma página da Web.  No entanto, há um arquivo extra que é necessário na raiz desse arquivo zip e esse arquivo é nomeado `manifest.json` .  É o esquema da extensão que inclui itens como qual é a versão de sua extensão, qual é o título, em que privilégios ele precisa ser executado e muito mais.  

![Exibição de arquivos em zip](media/index-image5-filemanager-view.png)  

### Iniciando o servidor de extensão  

Quando você implanta em um servidor Web, esse servidor Web, seja o Apache, o IIS, o NGINX ou qualquer outro, contém seu pacote da Web.  Quando um navegador navega para uma URL em um servidor, o `index.html` arquivo no servidor Web é baixado.  O navegador navegou usando certificados, arquivos de configuração e muito mais.  O `index.html` arquivo armazenado em um local especial no servidor Web.   Como a extensão faz a mesma coisa?  Em especial, como as páginas da guia do seu navegador podem acessar este arquivo zip \ (sua extensão \)?  Isso é o que o tempo de execução de extensão faz para você.  

A extensão serve para os arquivos a partir da URL \ (Uniform Resource Locator \) no nome `extension://{some-long-unique-identifier}/index.html` .  O nome que coloquei em colchetes `{some-long-unique-identifier}` é um identificador exclusivo atribuído à extensão instalada.  Isso significa que, se você tiver 10 ramais exclusivos instaladas em seu navegador, cada extensão tem um identificador exclusivo que aponta para o arquivo zip \ (ou pacote de extensão \) instalado dentro do seu navegador.  

<!--![Unique URLS for Extensions](media/index-image4-uniqueurls.png)  -->  

<!--todo: add image for unique URLs  -->  

### Extensões gerenciar e se comunicar com guias e a barra de ferramentas do navegador  

As extensões interagem com a barra de ferramentas navegadores, cada uma pode gerenciar todas as outras páginas da guia em execução de maneira segura, além de manipular o DOM de todas essas páginas da guia.  Integrado ao navegador Chromium é uma API de mensagens que permite comunicações entre as extensões e as páginas da guia para permitir que isso aconteça normalmente.  Essa API, também conhecida como a API de extensões fornece vários recursos, incluindo gerenciamento de notificações, gerenciamento de armazenamento e muito mais.  

Da mesma forma que os servidores Web, as extensões podem executar continuamente \ (ou aguardando notificações \) o tempo que o navegador está executando.  Você pode pensar em uma extensão como um orquestrador para o navegador.  Novamente, a extensão é executada completamente isolada das páginas da guia, mas por meio da API de extensões e as permissões de consentimento concedidas à extensão, cada extensão é capaz de controlar virtualmente todas as páginas da guia e de todas as páginas em execução no navegador.  

### As extensões fornecem um modelo de segurança de consentimento no momento da instalação  

Cada extensão, por meio de uma declaração no `manifest.json` arquivo permite que a pessoa que está instalando a extensão a forneça diferentes níveis de autoridade.  Essa autoridade permite que as extensões sejam instaladas por um usuário, para que a extensão seja capaz de extrair qualquer informação e processar os dados por meio da extensão.  

<!-- image links -->  

<!-- links -->  
