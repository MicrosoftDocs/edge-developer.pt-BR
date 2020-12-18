---
description: O protocolo Microsoft Edge DevTools versão 0,1 dá suporte aos seguintes clientes de ferramentas.
title: DevTools Protocol versão 0,1 clients (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb7355524ec6dab5cf0275538c5b0c030891d4a9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231323"
---
# DevTools Protocol versão 0,1 clients (EdgeHTML)  

> [!NOTE]
> O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

O **protocolo DevTools 0,1** dá suporte aos seguintes clientes de ferramentas.

[ ![ Microsoft Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ Microsoft Visual Studio 15,7 Preview 2](../media/visual-studio-2017.png)](#microsoft-visual-studio-preview)

## Visualização do Microsoft Edge DevTools

Você pode usar o aplicativo autônomo do [**Microsoft Edge devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) para Windows 10 da Microsoft Store para depurar remotamente um dispositivo host executando o Microsoft Edge ([EdgeHTML 17](../../dev-guide/index.md) ou posterior).

Este lançamento preliminar da versão 0,1 do protocolo DevTools fornece a funcionalidade de depuração básica, como a configuração de pontos de interrupção, a depuração do código e a exploração de rastreamentos de pilha. Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis no painel do [**depurador**](../../devtools-guide/debugger.md) , subtração inspeção de cache (para armazenamento da Web, trabalho de serviço, API de cache e IndexedDB). Atualmente a depuração remota do Microsoft Edge está limitada aos hosts da área de trabalho, com suporte a outros dispositivos Windows 10 em lançamentos futuros.

Confira aqui como configurar a depuração remota com o aplicativo Microsoft Edge DevTools Preview. O protocolo DevTools está em visualização e requer a [atualização do Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) ou uma versão mais recente do Windows Insider Preview no computador host (depurador). O aplicativo Edge DevTools Preview (usado na máquina do depurador) será executado na atualização dos criadores de outono (versão 1709) e compilações do Windows Insider Preview.

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

## Microsoft Visual Studio Preview

Usando a compilação mais recente do [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual Studio 15,7 Preview 1 ou posterior), você pode iniciar e depurar o Microsoft Edge a partir do IDE em qualquer projeto do ASP.net ou do .NET Core. No momento, o protocolo DevTools está no modo de visualização e requer que você execute uma compilação do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

Veja aqui como configurar a depuração do Microsoft Edge com o Visual Studio:

1.  Instale e inicie a versão [**prévia do Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual Studio 15,7 Preview 1 ou posterior).

2. Abra um projeto existente do ASP.NET ou do .NET Core ou **crie um novo projeto...** usando um dos modelos do **Visual C#** .net.

3. No Gerenciador de **soluções**de projeto, abra os arquivos JavaScript que você deseja depurar e defina pontos de interrupção dentro do IDE da mesma forma que faria com o código do lado do servidor.

4. Pressione `F5` para iniciar o Microsoft Edge executando o servidor devtools. Quando um ponto de interrupção é atingido, você pode invadir o Visual Studio e pode inspecionar e percorrer o código aqui.
