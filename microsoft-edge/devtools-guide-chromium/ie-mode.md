---
description: Modo IE e o Microsoft Edge (Chromium) DevTools
title: Modo Internet Explorer e o DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, ie11, Internet Explorer 11, modo IE
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003955"
---
# Modo Internet Explorer e o DevTools  

Este artigo descreve como o modo \ (IE Mode \) do Internet Explorer integra-se com o DevTools Microsoft Edge \ (Chromium \).  

## Noções básicas sobre o modo IE  

O modo IE permite que as empresas especifiquem uma lista de sites da Web que só funcionam no Internet Explorer 11.  Quando você navegar para esses sites no Microsoft Edge \ (Chromium \), uma instância do Internet Explorer 11 será executada e renderizará o site em uma guia.  A funcionalidade permite às empresas gerenciar a compatibilidade com tecnologias que atualmente não são compatíveis com qualquer navegador da Web moderno.  O suporte para as seguintes tecnologias está incluído no modo IE.  

*   Modos de documento do IE  
*   Controles ActiveX  
*   outros componentes herdados  

No modo IE, o processo de renderização é baseado no Internet Explorer 11.  O Gerenciador de processos do Microsoft Edge \ (Chromium \) manipula o tempo de vida do processo de renderização.  Ele é restrito ao tempo de vida da guia para um site específico \ (ou app \).  Quando uma guia é renderizada no modo IE, um emblema é exibido na barra de endereços para a guia específica.  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="Selo do modo do IE na barra de endereços" lightbox="./media/ie-mode-badge.msft.png":::
   Selo do modo do IE na barra de endereços  
:::image-end:::  

No momento, o modo do IE está disponível no Windows 10 versão 1903 \ (atualização de maio de 2019), mas estará disponível em breve para todas as plataformas do Windows com suporte.  

## Iniciando o DevTools em uma guia no modo IE  

Se você estiver tentando exibir o modo de documento de um site no modo IE, escolha o selo na barra de endereços.  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Exibir o modo de documento usando o selo do modo IE" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   Exibir o modo de documento usando o selo do modo IE  
:::image-end:::  

Se uma guia estiver usando o modo IE, o DevTools não funcionará e as seguintes condições ocorrerão.

*   Se você selecionar `F12` ou selecionar `Ctrl` + `Shift` + `I` uma instância em branco do Microsoft Edge \ (Chromium \) devtools será inicializada exibirá a mensagem a seguir.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Se você abrir um menu contextual \ (clique com o botão direito do mouse \) e escolher **Exibir fonte**, o bloco de notas será iniciado.  
*   Se você abrir um menu contextual \ (clique com o botão direito do mouse \), o **elemento inspecionar** não ficará visível.  

O motivo pelo qual um número de ferramentas na DevTools \ (como as ferramentas de **rede** e **desempenho** \) não funciona é o mecanismo de renderização switches do Chromium para o Internet Explorer 11 no modo IE.  Para enviar comentários, navegue até entrar [em contato com a equipe do Microsoft Edge devtools](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="DevTools iniciado no modo IE" lightbox="./media/ie-mode-devtools.msft.png":::
   DevTools iniciado no modo IE  
:::image-end:::  

Para testar seu site baseado no Internet Explorer 11 (ou app \) no Internet Explorer 11 e no modo IE, siga as etapas a seguir.  

1.  Abra o Internet Explorer 11.  
    *   No Windows 10, localize o atalho para o Internet Explorer 11.
        1.  **Menu iniciar**  >  **Acessórios**  >  do Windows **Internet Explorer 11**.  
    *   No Windows 7, localize o Internet Explorer 11.
        1.  **Menu iniciar**  >  **Internet Explorer 11**.  
1.  No Internet Explorer 11, abra a mesma página da Web.  
1.  Inicie o Internet Explorer DevTools.  
    *   Selecione `F12` .  
    *   Passe o mouse em qualquer lugar, abra um menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar elemento**.  Para obter mais informações sobre como usar essas ferramentas, navegue até [usando as ferramentas de desenvolvedor F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

## Depuração remota e modo IE  

Inicie o Microsoft Edge \ (Chromium \) com a depuração remota ativada na interface de linha de comando.  O Visual Studio, o código do Visual Studio e outras ferramentas de desenvolvimento normalmente executam um comando para iniciar o Microsoft Edge.  O comando a seguir inicia o Microsoft Edge com a porta de depuração remota definida como `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

Depois de iniciar o Microsoft Edge \ (Chromium \) usando um argumento de linha de comando, o modo IE não está disponível.  Você ainda pode navegar para os sites \ (ou aplicativos \) que, de outra forma, seriam exibidos no modo IE. O conteúdo do site \ (ou app \) é renderizado usando Chromium, não o Internet Explorer 11.  Espere as partes das páginas que dependem do IE11, como os controles ActiveX, não sejam renderizadas corretamente.  O selo do modo do IE não aparece na barra de endereços.  

O modo IE permanecerá indisponível até você fechar completamente e reiniciar o Microsoft Edge \ (Chromium \).  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Usar as ferramentas de desenvolvedor F12 | Documentos da Microsoft"  