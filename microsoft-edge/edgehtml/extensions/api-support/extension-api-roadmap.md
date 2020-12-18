---
description: Encontre informações sobre o progresso atual em relação à conclusão da API de extensão do Microsoft Edge.
title: Roteiro de API de extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, API, extensões, JavaScript, desenvolvedor
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3552fede729a37ff83ac4b19cfadf89d6917a75
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231944"
---
# Mapa de API de extensão do Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Além das APIs da Web, a API de extensão permite que as extensões obtenham integração mais profunda com o host do navegador. Essa API proporciona aos desenvolvedores o acesso aos recursos do navegador da Microsoft Edge, como a manipulação de guias e janelas. A tabela a seguir detalha quais APIs têm suporte/em desenvolvimento para versões publicadas do Microsoft Edge lançadas no Windows 10.


|     Classe     |                                                              Descrição                                                              |                Status — número da compilação                 |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
|   indicadores   |                                          Usado para criar, organizar e manipular indicadores.                                          | Com suporte: Microsoft Edge (40)/Windows 10 (15063) |
| BrowserAction |                                 Habilita extensões para adicionar um botão persistente no Microsoft Edge.                                  | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
| comandos      |                                                      Define os atalhos de teclado.                                                      | Em consideração
| contextMenus  |                           Adiciona um item de menu de contexto em uma URL específica, em um contexto específico de uma página da Web.                            | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|    cookies    |                                 Usado para consultar e modificar cookies, bem como notificar quando eles mudam.                                 | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|   downloads   |                           Usado para iniciar, monitorar, manipular e Pesquisar downloads de forma programática.                           |                 Em consideração                  |
|   prorroga   |                                      Contém utilitários que podem ser usados por qualquer página de extensão.                                       | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|    histórico    |                                         Interage com o registro de páginas visitadas do navegador.                                         |                 Em consideração                  |
|     nacional      |                                         Implementa a internacionalização em uma extensão.                                          | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|   identidade    |                                       Usado para obter um código de autorização ou um token de acesso do OAuth2.                                       |                 Em consideração                  |
|     ociosidade      |                                       Usado para detectar quando o estado ocioso da máquina é alterado.                                        | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|  gerencia   |                                              Obtém informações sobre complementos instalados.                                                |                 Em consideração                  |
| notificações |                      Permite a criação de notificações usando modelos a serem exibidos na bandeja do sistema do usuário.                      | Com suporte-Microsoft Edge (42)/Windows 10 (17134) |
|  página de anotações   |                                      Habilita as extensões para adicionar um botão na barra de endereços.                                       | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|  Elas  |                   Permite que os usuários selecionem a quais permissões opcionais você gostaria de conceder acesso a extensão.                   |                 Em consideração                  |
|    classpath    | Recupera a página de plano de fundo, retorna detalhes sobre o manifesto e escuta e responde a eventos no ciclo de vida da extensão. | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|    armazenamento    |                                      Usado pela extensão para ler/gravar dados e sincronizar dados.                                       | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|     efetua      |                Interage com o sistema de guias do Microsoft Edge, criando, modificando e reorganizando as guias no navegador.                | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
| webnavigation |                           Usado para receber notificações sobre o status de solicitações de navegação em-Flight.                            | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|  webRequest   |        Permite o uso da API webRequest para observar e analisar o tráfego e para interceptar, bloquear ou modificar solicitações em trânsito.        | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
|    windows    |                              Interage com o navegador criando, modificando e reorganizando janelas.                              | Com suporte: Microsoft Edge (38)/Windows 10 (14393) |
