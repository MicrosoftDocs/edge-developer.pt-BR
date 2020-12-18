---
description: Use a ferramenta de console para depuração interativa e testes ad hoc.
title: DevTools-console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472aafa9e6c6fd98ea952804f0e92ed0b774f59c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231508"
---
# Console

A ferramenta de desenvolvedor de console no Microsoft Edge registra informações que estão associadas a uma página da Web, como JavaScript, solicitações de rede e erros de segurança. Você pode usar o console para depuração interativa e testes ad hoc. 

Para abrir a ferramenta de console no Microsoft Edge, pressione a tecla F12 para acessar a janela da ferramenta de desenvolvedor (ou clique com o botão direito do mouse na página e selecione **inspecionar elemento**). Em seguida, selecione a guia **console** na parte superior da janela. 

Você também pode usar a ferramenta de console para se comunicar com uma página da Web em execução e a partir dela. Você pode usar o console para:

- Poste [códigos de erro e de status](./console/error-and-status-codes.md) padrão e mensagens informativas à medida que seu código é executado.
- Gere logs de depuração personalizados nas chamadas de [API do console](./console/console-api.md) que você incluir no seu código.
- Fornecer uma [linha de comando](./console/command-line.md) e uma exibição de árvore interativa para inspecionar os valores de retorno atuais de variáveis e funções chave.

## Partes do console

A imagem a seguir mostra as partes principais do console:

![O console do Microsoft Edge DevTools](./media/console.png)

1. **Erros**  /  de **Avisos**  /  **Informações**  /  Botões de **log** : filtra a saída do console pelo tipo especificado. Você pode selecionar vários botões mantendo pressionada a tecla **Ctrl** . O botão **todos** limpa todos os filtros.

2. Botão **limpar** (**Ctrl + L**): o botão **limpar** limpa a exibição atual do console.

3. Caixa de seleção **preservar log** : marcar a caixa de seleção **preservar log** persiste a saída do seu console nas atualizações da página e fechar e reabrir o devtools. O histórico do console é limpo apenas quando a guia é fechada ou você limpa manualmente o console.

4. **Destino**: Use o menu suspenso de **destino** para alternar para um contexto de execução diferente, como `<iframe>` em sua página ou em uma extensão em execução. Por padrão, o quadro de nível superior da sua página é selecionado. Passar o mouse sobre um quadro selecionado exibe uma dica de ferramenta que mostra a URL completa desse recurso.

5. **Mostrar console**  /  Botão **ocultar console** (**Ctrl** +  **&grave;** ): além do painel do console, você pode usar o console na parte inferior de qualquer outro painel do devtools pressionando o botão **Mostrar**console  /  **ocultar console** . O botão não tem efeito quando o DevTools está aberto no painel do console.
 
6. **Filtrar logs** (**Ctrl + F**): você também pode filtrar logs usando uma cadeia de texto específica na caixa de pesquisa.

7. **Depurador**: selecione qualquer link de fonte azul para abrir o depurador devtools para essa linha de código específica para inspeção adicional.

## Atalhos

Ação                                            | Atalho               
:-------------------------------------------------| :----------------------
Iniciar o DevTools com o console em foco             | **Ctrl +**  +  **Alterar**  +  **J** 
Alternar para o console                                 | **Ctrl +**  +  **2**           
Mostrar/ocultar o console a partir de outra guia DevTools       | **Ctrl +**  +  **&grave;** (Back-Tick)  
Executar (comando de linha única)                     | **Tecla Enter**                
Quebra de linha sem execução (comando de várias linhas) | **Alterar**  +  **Enter** ou **Ctrl +**  +  **Enter**      
Limpar o console de todas as mensagens                 | **Ctrl +**  +  **L**           
Filtrar logs (definir o foco para a caixa de pesquisa)             | **Ctrl +**  +  **L**           
Aceitar sugestão de preenchimento automático (quando estiver em foco) | **Enter** ou **Tab**       
Sugestão de preenchimento automático anterior/seguinte          | Tecla de seta **para cima** / **Tecla de seta para baixo**   
