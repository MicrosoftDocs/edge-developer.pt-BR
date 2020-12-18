---
description: O protocolo Microsoft Edge DevTools versão 0,2 dá suporte aos seguintes clientes de ferramentas.
title: Microsoft Edge DevTools Protocol versão 0,2 clientes (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b471ff5a4051411fc205a269d811524c38acac72
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231311"
---
# Microsoft Edge DevTools Protocol versão 0,2 clientes (EdgeHTML)  

> [!NOTE]
> A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .  

O **protocolo DevTools 0,2** dá suporte aos seguintes clientes de ferramentas.

[ ![ Código do Visual Studio](../media/visual-studio-code.png)](#visual-studio-code) Microsoft [ ![ Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ do Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)

## Visualização do Microsoft Edge DevTools

Você pode usar o aplicativo autônomo do [**Microsoft Edge devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) para Windows 10 da Microsoft Store para depurar remotamente um dispositivo host executando o Microsoft Edge ([EdgeHTML 17](../../dev-guide/index.md) ou posterior).

A versão 0,2 do protocolo DevTools fornece novos domínios para a depuração de estilo e de layout e APIs de console, além da funcionalidade de depuração de script principal introduzida na versão 0,1. Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis nos painéis de [**elementos**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) e [**depurador**](../../devtools-guide/debugger.md) . Atualmente a depuração remota do Microsoft Edge está limitada aos hosts da área de trabalho, com suporte a outros dispositivos Windows 10 em lançamentos futuros.

Confira aqui como configurar a depuração remota com o aplicativo Microsoft Edge DevTools Preview. A 0,2 versão do protocolo DevTools requer a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) ou uma compilação mais recente do Windows Insider Preview na máquina do host (depurador). O aplicativo Edge DevTools Preview (usado na máquina do depurador) será executado no Windows 10 versão 16299 (atualização do Windows 10 para criadores de outono, 10/2017) ou superior.

**Na máquina do host (depurador)...**

1. Se você estiver em uma rede WiFi, verifique se a rede está marcada como **Domain** ou **Private**. Você pode verificar isso abrindo o aplicativo da [**central de segurança do Windows Defender**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , clicando em **Firewall & proteção de rede** e verificando se sua rede está listada como uma rede *privada*ou de *domínio* . 

    Se ele estiver listado como *público*, acesse **configurações**  >  **rede & Internet**  >  **Wi-Fi**, clique em sua rede e alterne o botão do *perfil de rede* para **particular**.

2. Abra o painel **de controle para desenvolvedores** nas *configurações* do Windows (procure *desenvolvedor* e clique em *usar recursos de desenvolvedor*) e: 

    a. Ative o **modo de desenvolvedor**. Isso vai instalar o pacote do *modo de desenvolvedor* , permitindo ferramentas remotas para área de trabalho.

    b. Habilite o Device [**portal**](/windows/uwp/debug-test-perf/device-portal) (*ative o diagnóstico remoto em conexões de rede local*) e a **descoberta de dispositivo** (*torne seu dispositivo visível para conexões USB e sua rede local*).

    c. Ative a **autenticação** e forneça um nome de usuário/senha.

    d. Observação: o endereço IP do computador e a porta de conexão (50443) são exibidos.

3. Abra as guias no Microsoft Edge que você deseja depurar do computador cliente.

**Na máquina cliente (depurador)...**

1.  Instale e inicie o aplicativo autônomo de [visualização do Microsoft Edge devtools](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) na Microsoft Store.

2. Abra o painel **remoto** e insira o local de rede (URL e porta) do computador host e clique em **conectar**.

3. **Instale** o certificado do computador host a partir da caixa de diálogo *certificado não confiável* exibida.

4. Forneça o nome de usuário/senha designado para a autenticação do Device Portal.

5. O painel *remoto* carregará uma lista de destinos de página do debuggable no computador host. Selecione um para iniciar a depuração.

6. Use o botão **Atualizar** para atualizar e recarregar a lista de destinos de página remotas no computador host. Clique no botão **Desconectar** para retornar à tela *conectar-se a um dispositivo remoto e conectar-se* a um host diferente.

## Visual Studio Code

Com o [depurador para Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, você pode depurar o script executado no Microsoft Edge diretamente no código do Visual Studio. A extensão exige que você esteja servindo seu aplicativo Web do localhost, que pode ser iniciado a partir de uma linha de comando ou de uma [tarefa](https://code.visualstudio.com/docs/editor/tasks).

Para começar:

1. Instale o [depurador para Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código.

2. Reinicie o código VS, abra a pasta que contém o projeto que você deseja depurar e defina os pontos de interrupção no código.

3. Configure uma [tarefa de inicialização](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) do localhost para abrir a página desejada do seu projeto: **depurar**  >  **Adicionar configuração..**.. Por exemplo:

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    [*Usar o depurador*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) tem mais opções de configuração de inicialização. 

4. Inicie o servidor no localhost e pressione o botão **Iniciar Depuração** (Play) ou `F5` iniciar o Microsoft Edge. Quando um ponto de interrupção é atingido, você se divide no código VS e pode inspecionar ainda mais e percorrer o código.

Para saber mais, confira a documentação do [vs-Debugger para Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .

## Microsoft Visual Studio

Usando a versão do [**Visual Studio**](https://www.visualstudio.com) mais recente (visual Studio 15,8 ou posterior) em execução na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763), você pode iniciar e depurar o Microsoft Edge a partir do IDE em qualquer projeto do ASP.net ou do .NET Core.

Veja aqui como configurar a depuração do Microsoft Edge com o Visual Studio:

1.  Instale e inicie o [**Visual Studio**](https://www.visualstudio.com/) (visual Studio 15,8 ou posterior) mais recente.

2. Abra um projeto existente do ASP.NET ou do .NET Core ou **crie um novo projeto...** usando um dos modelos do **Visual C#** .net.

3. No Gerenciador de **soluções**de projeto, abra os arquivos JavaScript que você deseja depurar e defina pontos de interrupção dentro do IDE da mesma forma que faria com o código do lado do servidor.

4. Pressione `F5` para iniciar o Microsoft Edge executando o servidor devtools. Quando um ponto de interrupção é atingido, você pode invadir o Visual Studio e pode inspecionar e percorrer o código aqui.
