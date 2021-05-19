---
description: Os recursos experimentais mais recentes no Microsoft Edge para Aplicativos Web
title: Recursos experimentais | Aplicativos Web Progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 4a50b925e002746357b2b770b199d84772b456f5
ms.sourcegitcommit: bbbf722067f1d255f59ab384e66798f8b77ef609
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2021
ms.locfileid: "11574586"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a>Recursos experimentais em PWAs (Progressive Web Apps)  

Microsoft Edge fornece acesso a recursos experimentais que ainda estão em desenvolvimento.  Para determinar se cada recurso está pronto e quando lançar cada um, teste e [forneça comentários.](#providing-feedback-on-experimental-features)  

Os recursos experimentais estão disponíveis em todos os canais de Microsoft Edge, mas os recursos experimentais mais recentes estão disponíveis apenas no canal Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Ativar recursos experimentais  

Para ativar \(ou desativar\) recursos experimentais Microsoft Edge, conclua as etapas a seguir.  
  
1.  Abra o Microsoft Edge.   
    
    > [!NOTE]
    > Certifique-se de usar uma Microsoft Edge que tenha o Experimento listado neste artigo.  Navegue até [Recursos Experimentais](#features-that-are-available-to-test).  
    
1.  Navegue até `edge://flags`.  
1.  Navegue até o experimento relevante.  
1.  Escolha o menu suspenso ao lado da descrição do experimento e escolha `Enabled` .  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Escolha Habilitado para ativar um experimento" lightbox="../media/turn-on-experimental-flag.png":::
       Escolha **Habilitado para** ativar um experimento  
    :::image-end:::  
    
    > [!NOTE]
    > Cada experimento geralmente tem um menu suspenso para escolher os seguintes valores.  Se um recurso experimental não tiver uma entrada em **Experimentos,** serão fornecidas instruções para iniciar Microsoft Edge com esse recurso usando a linha de comando.
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  Reinicie o Microsoft Edge.  
    
### <a name="origin-trials"></a>Avaliações de Origem  

Microsoft Edge às vezes usa testes de origem para testar recursos para domínios ou sites específicos.  Talvez você queira usar uma avaliação de origem para seu site para aplicar um recurso específico.  Se você for um proprietário de site, poderá se inscrever em uma avaliação de origem.  Uma avaliação de origem fornece recursos para uma porcentagem Microsoft Edge usuários que visitam seu site.

Para obter mais informações sobre as avaliação de origem, navegue até Microsoft Edge Console de Desenvolvedor [de Avaliação de Origem.][MicrosoftDeveloperMicrosoftEdgeOriginTrials]  
    
> [!NOTE]
> Os recursos experimentais são constantemente atualizados e podem causar problemas de desempenho.  Para desativar um recurso experimental, navegue até [Ativar recursos experimentais,](#turn-on-experimental-features)navegue até o experimento e escolha `Disabled` .  

## <a name="features-that-are-available-to-test"></a>Recursos disponíveis para teste  

A lista a seguir descreve os novos recursos experimentais do aplicativo Web que estão disponíveis para testar e validar em Microsoft Edge.  

| Recurso | Microsoft Edge versão | Plataforma |  
|:--- |:--- |:--- |  
| [Tratamento de protocolo URI](#uri-protocol-handling) | 91 ou posterior | Windows e Linux |    
| [Manipulação de link de URL](#url-link-handling) | 91 ou posterior | Windows|
| [Sobreposição de Controles de Janela para Aplicativos de Área de Trabalho](#window-controls-overlay-for-installed-desktop-web-apps) | 91 ou posterior | Windows 10|   
| [Executar no logon do sistema operacional](#run-on-os-login) | 88 ou posterior | Todas |  
| [Atalhos](#shortcuts) | 87 ou posterior | Todas |  
| [Tratamento de arquivos](#file-handling) | 83 ou posterior | Toda a área de trabalho |  

## <a name="uri-protocol-handling"></a>Tratamento de protocolo URI  

Um identificador de recurso uniforme \(URI\) pode ser usado para definir mais do que apenas links para páginas da Web e conteúdo da Web usando o protocolo HTTP ou FTP.  URIs podem ser usadas para descrever links para qualquer coisa que você codificar em um esquema.  Por exemplo, o protocolo é usado para descrever um link de email e o sistema operacional \(OS\) ou navegador decide qual página da Web ou `mailto://` aplicativo deve lidar com esse protocolo.  

Para obter mais informações sobre o suporte baseado em navegador existente, navegue até manipuladores de protocolo [baseados na Web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]  

Esse recurso permite que você conclua as seguintes ações.  

*   Registre sua PWA com o sistema operacional host usando o manifesto do seu aplicativo Web
*   Declare que um PWA lida com um protocolo URI específico  
    
Depois de registrar um PWA como um manipulador de protocolo, quando um usuário escolhe um hiperlink com um esquema específico, como ou de um navegador ou um aplicativo nativo, o PWA registrado é ativado pelo sistema operacional e recebe o `mailto://` `web+music://` URI.  

Esse recurso exige que você atualize o manifesto do aplicativo Web para incluir uma matriz, na matriz que você `protocol_handlers` precisa especificar dois campos:  

*   `protocol`: O protocolo para lidar com a solicitação, por exemplo `mailto` ou `web+jngl` .  
*   `url`: O URI HTTPS no escopo do aplicativo que lida com o protocolo.  No futuro, o URI começando com o esquema de manipuladores de protocolo é planejado para substituir o `%s` token.  
    
Atualize seu manifesto para dar suporte ao protocolo que você deseja registrar.  Depois de ativar esse recurso, Microsoft Edge concluir as seguintes ações.  

1.  Detecta alterações no manifesto  
1.  Registra o aplicativo para o protocolo  
    
Se mais de um aplicativo registrar um protocolo, o usuário será apresentado com um prompt.  O usuário escolhe o aplicativo apropriado na lista apresentada pelo sistema operacional ou navegador.  

Para visualizar o tratamento de protocolo Microsoft Edge no Windows, navegue até Ativar recursos **experimentais**e ause a Área de Trabalho PWA Tratamento de Protocolo . [](#turn-on-experimental-features)  

Para obter mais informações sobre a avaliação de origem em execução para manipuladores de protocolo, navegue até Registrar para Registro para Registro do Manipulador [de Protocolo web][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].  

### <a name="example-manifest"></a>Manifesto de Exemplo

Neste exemplo, um manifesto do aplicativo Web declara que o aplicativo deve ser registrado para lidar com os protocolos `web+jngl` e `web+jnglstore` .

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a>Manipulação de link de URL  

Um localizador de recursos uniforme \(URL\) é um tipo de URI.  Crie uma experiência mais envolvente quando os Aplicativos Web Progressivos \(PWAs\) se registrarem como manipuladores para URIs https.  PWAs podem solicitar o lançamento quando URIs associados são ativados.  Por exemplo, se um usuário escolher um link para uma notícia de uma mensagem de email.  Uma PWA para exibir notícias é automaticamente lançada para manipular a ativação do link.  

Esse recurso permite que você registre uma PWA com o navegador usando o manifesto do aplicativo Web e declare que o navegador lida com links específicos.  Para registrar uma PWA com o navegador, adicione o `url_handlers` membro opcional ao arquivo de manifesto.  O `url_handlers` membro é um que grupos as `object[]` origens de URIs que o aplicativo deseja manipular.  

A manipulação de links é validada pelo navegador usando um arquivo JSON localizado `web-app-origin-association` na origem.  O arquivo de origem ajusta ainda mais os caminhos incluídos ou excluídos na origem.  Para obter instruções detalhadas sobre como testar o manipulador de URL, navegue até [PWAs como Manipuladores de URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]  

Para visualizar o tratamento de link de URL [](#turn-on-experimental-features) no Microsoft Edge no Windows, navegue até Ativar recursos experimentais e ause o **Desktop PWA URL Handling**.  

### <a name="example-of-the-url_handlers-in-the-manifest"></a>Exemplo do url_handlers no manifesto  

O trecho de código a seguir é um exemplo de manifesto do aplicativo Web com o `url_handlers` membro.  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

Um PWA corresponde a um URI para manipulação de URL se o URI corresponde a uma das cadeias de caracteres de origem e o navegador valida que a origem concorda em permitir que esse aplicativo manipular esse `url_handlers` URI.  

O membro contém uma origem que abrange o escopo e outras origens não `url_handlers` relacionadas da PWA.  Não restringir URIs ao mesmo escopo ou domínio que o PWA solicitante permite usar nomes de domínio diferentes para o mesmo conteúdo, mas lidar com eles com o mesmo PWA.  

#### <a name="wildcard-matching"></a>Correspondência de caracteres curinga  

Use o caractere curinga \( `*` \) para corresponder a um ou mais caracteres.  

Um prefixo curinga é usado nas cadeias de caracteres de origem do `url_handlers` membro para corresponder a subdomas diferentes.  O prefixo deve `*.` ser para esse uso.  O `https` esquema é assumido quando você usa um prefixo curinga.  

Por exemplo, o `url_handlers` valor do membro é definido como corresponde e , mas não corresponde `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` `contoso.com` .  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a>Sobreposição de Controles de Janela para aplicativos Web da área de trabalho instalados  

Para criar uma barra de título imersiva como um aplicativo nativo **** para seu aplicativo Web instalado na área de trabalho, o recurso Sobreposição de Controles de Janela conclui as seguintes ações.  
    
1.  Remove a barra de título reservada do sistema.  Geralmente, ela abrange a largura do quadro do cliente.  
1.  Substitui-o por uma sobreposição.  Ele contém apenas os controles críticos de janela necessários para que um usuário controle a própria janela.  
    
Depois que ele fornece uma sobreposição, toda a área do cliente Web estará disponível para você usar.  Esse recurso inclui uma atualização de manifesto.  Ele fornece maneiras de determinar o tamanho e a posição da sobreposição para ajudá-lo a organizar o conteúdo.  

Para visualizar as Sobreposições de Controles de Janela no [](#turn-on-experimental-features) Microsoft Edge para Windows 10, navegue até Ativar recursos experimentais e navegue até **Desktop PWA Sobreposição**de Controles de Janela .   

### <a name="examples-of-title-bar-area-customization"></a>Exemplos de personalização da área da barra de títulos  

Esse recurso se baseia na capacidade em aplicativos nativos de personalizar a barra de título.  Você pode personalizar uma barra de título para ações ou notificações importantes do aplicativo.  Revise os exemplos a seguir para Microsoft Visual Studio Código e Microsoft Teams.  

#### <a name="visual-studio-code"></a>Visual Studio Code  

Microsoft Visual Studio Code é um editor popular criado em Eletrônica que acompanha várias plataformas de área de trabalho.  

O exemplo a seguir exibe como o Visual Studio Code usa a barra de título para maximizar a propriedade da tela disponível para incluir o nome do arquivo atual e a estrutura de menu de nível superior na barra de título.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Um exemplo da barra de título no Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   Um exemplo da barra de título no Visual Studio Code  
:::image-end:::  

#### <a name="microsoft-teams"></a>Microsoft Teams  

A ferramenta de colaboração e comunicação do local de trabalho Microsoft Teams também é criada com o Eletrônica e disponível em várias plataformas de área de trabalho.  No exemplo a seguir, Microsoft Teams e botões de navegação, uma caixa de pesquisa `back` `forward` e controles de perfil de usuário.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Um exemplo da barra de título no Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   Um exemplo da barra de título no Microsoft Teams  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a>Controles de janela de sobreposição em uma janela sem quadros  

Para maximizar a área acessível para conteúdo da Web, o navegador cria uma janela sem quadros.  Uma janela sem quadros remove toda a interface do usuário do navegador, exceto os controles de janela fornecidos como uma sobreposição.  A sobreposição de controles de janela permite que os usuários ainda minimizem, maximizem, restaurem e fechem o aplicativo.  Ele também fornece acesso a controles relevantes do navegador usando o menu do aplicativo Web.  Para Chromium navegadores baseados em Chromium, a sobreposição inclui os seguintes controles.  

*   Uma região arrastável com a mesma largura e altura de cada um dos botões de controle de janela  
*   O **Configurações e mais** \(...\) botão  
*   Os botões de controle de janela minimizam, maximizam, restauram e fecham  
    
Além dos controles listados anteriormente, a interface do usuário exibida na sobreposição é resized dinamicamente nos seguintes cenários.  

*   Quando um aplicativo Web instalado é lançado, a origem da página da Web é exibida à esquerda do menu **Configurações** e mais \(...\) por alguns segundos e desaparece.  
*   Se um usuário interagir com uma extensão usando o menu **Configurações** e mais \(...\), o ícone da extensão será exibido na sobreposição à esquerda do menu de três pontos.  Depois de sair de qualquer caixa de diálogo de extensão, o ícone será removido da sobreposição.  
    
| Direção do idioma | Local de sobreposição | Detalhes |  
|:--- |:--- |:--- |  
| Da esquerda para a direita \(LTR\) | Superior esquerdo da área do cliente | Os controles são invertida |  
| Da direita para a esquerda \(RTL\) | Canto superior direito da área do cliente |  |  

> [!IMPORTANT]
> A sobreposição está sempre sobre o índice Z do conteúdo da Web e aceita todas as entradas do usuário sem fluí-la para o conteúdo da Web.  

### <a name="working-around-the-window-controls-overlay"></a>Trabalhando ao redor da Sobreposição de Controles de Janela  

O conteúdo da Web deve estar ciente da área reservada para a sobreposição de controles.  Verifique se a área reservada não espera interação do usuário.  Consulte o navegador para o retângulo delimitador e a visibilidade da sobreposição de controles.  As informações são fornecidas por meio de APIs JavaScript e variáveis de ambiente CSS.  

#### <a name="javascript-apis"></a>JavaScript APIs  

Um novo objeto na propriedade permite consultar o `windowControlsOverlay` `window.navigator` retângulo delimitante da sobreposição de controles.  

O `windowControlsOverlay` objeto tem os dois objetos a seguir.  

*   `getBoundingClientRect()` retorna um `DOMRect` objeto.  O `DOMRect` objeto representa a área sob a sobreposição de controles da janela.  
*   `visible` é um booleano que indica que a sobreposição de controles é renderizada e exibida.  
    
> [!IMPORTANT]
> Por motivos de privacidade, `windowControlsOverlay` o não está acessível a elementos no `iframe` conteúdo da Web.  

Sempre que a sobreposição é ressada, um evento é executado no objeto para notificar o cliente para `geometrychange` `navigator.windowControlsOverlay` recalcular o layout de conteúdo.  O layout de conteúdo recalculado baseia-se no novo retângulo delimitante da sobreposição.  

#### <a name="css-environment-variables"></a>Variáveis de ambiente CSS  

Além da API JavaScript, você pode usar CSS para consultar o retângulo delimitante da sobreposição de controles.  Use as quatro novas variáveis de ambiente CSS a seguir para realizar a consulta.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a>Definir regiões arrastáveis no conteúdo da Web  

Os usuários esperam pegar e arrastar a região superior de uma janela.  Para acomodar a expectativa, declare partes específicas do conteúdo da Web como arrastáveis.  
Para especificar que um elemento é arrastável, use a propriedade CSS proprietária do `-webkit-app-region` WebKit.  O grupo de trabalho CSS continua os esforços para padronizar a `app-region` propriedade.  

### <a name="custom-title-bar-example"></a>Exemplo da barra de título personalizada  

O exemplo a seguir exibe como os novos recursos criam um aplicativo Web com uma barra de título personalizada.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Exemplo de uma barra de título personalizada no Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Exemplo de uma barra de título personalizada no Microsoft Teams  
:::image-end:::  

#### <a name="manifestwebmanifest"></a>manifest.webmanifest  

No manifesto, de definir `display_override` matriz como  `window-controls-overlay` .  De definir `theme_color` a para sua escolha de cor para a barra de título.  De definir o modo de exibição como um fallback apropriado para quando ou `display_override` `window-controls-overlay` não for suportado.  

O trecho de código a seguir inclui as atualizações de manifesto recomendadas.  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### <a name="indexhtml"></a>index.html  

As IDs a seguir representam as duas principais regiões da página da Web.  

*   `titleBarContainer`  
*   `mainContent`  
    
O `div` elemento com a `titleBar` ID é definido como e o elemento filho da caixa de pesquisa `draggable` é definido como `input` `nonDraggable` .  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

No elemento `div` com a ID, o com a ID representa a parte visível da área da barra de `titleBarContainer` `div` `titleBar` título.  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a>style.css  

As regiões arrastáveis e não arrastáveis são definidas usando `-webkit-app-region: drag` e `-webkit-app-region: no-drag` .  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

Para o `body` elemento, as margens são definidas para garantir que a barra de título atinja `0` as bordas da janela.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

A ID usa e define como , que anexa o contêiner à `titleBarContainer` parte superior da página da `position: absolute` `top` `titlebar-area-inset-top` Web.  O será definido como e retornará para se a sobreposição de controles de janela `bottom` não estiver `titlebar-area-inset-bottom` `100% - var(--fallback-title-bar-height)` visível.  A cor de plano de fundo `titleBarContainer` da ID é a mesma que `theme_color` a .  A largura é definida como , para que o elemento preencha a largura da página da Web e flua sob a sobreposição quando estiver visível para uma `100%` `div` aparência contígua.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

A `titleBar` ID também usa `position: absolute` e a anexa à parte superior da `top: titlebar-area-inset-top` janela.  Por padrão, ele consome a largura total da janela.  As `left` bordas e são `right` definidas como e, respectivamente, ambas voltam para quando os valores não são `titlebar-area-inset-left` `titlebar-area-inset-right` `0` definidos.  Ele também define para impedir qualquer tentativa de arrastar a janela consumida, em vez disso, `user-select: none` realça o texto no `div` elemento.  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

O contêiner para a ID também é fixo e anexado `mainContent` à parte inferior da página da `position: absolute` Web.  O `height` é definido como e recua para preencher o espaço restante abaixo da barra de `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` título.  Ele define `overflow-y: scroll` para permitir que o conteúdo role verticalmente no contêiner.  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

Para os casos em que o navegador não dá suporte à sobreposição de controles de janela, uma variável CSS é adicionada para definir uma altura padrão para a barra de título.  Os limites das IDs e são definidos inicialmente para preencher toda a área do cliente, e você não precisa alterá-la se a sobreposição não for `titleBarContainer` `mainContent` suportada.  

O trecho de código a seguir inclui todas as atualizações CSS recomendadas.

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  

Chromium navegadores baseados em dados estão testando e moldando esse recurso.  Para obter mais informações, incluindo exemplos de código, navegue até Personalizar a sobreposição de controles de janela da barra de título do seu [PWA.][WebDevWindowControlsOverlay]  

## <a name="run-on-os-login"></a>Executar logon no sistema operacional  

Esse recurso permite configurar seu aplicativo para iniciar automaticamente quando o usuário entrar no Microsoft Windows.  Várias classes de aplicativos aproveitam a funcionalidade.  As classes de aplicativos incluem email, chat, painel de monitoramento e aplicativos de exibição de dados em tempo real.  A funcionalidade permite que um usuário se envolva com os aplicativos assim que o usuário faz logor no sistema operacional.  Esse recurso inicia automaticamente o PWA da mesma forma que é iniciado manualmente.  

> [!IMPORTANT]
> **Executar no logon do sistema** operacional é um [recurso poderoso.][GithubW3cPermissionsPowerfulFeature]  Os usuários devem decidir se ativarão o recurso para o aplicativo Web instalado.  

### <a name="turn-on-run-on-os-login"></a>Ativar o logon do sistema operacional  

Para visualizar os **recursos de Logon** do sistema [](#turn-on-experimental-features) operacional Run On para sua PWA, navegue até Ativar recursos experimentais e a ativar PWAs da Área de Trabalho **executados no logon do sistema operacional**.  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Ativar os PWAs da Área de Trabalho executados no experimento de logon do sistema operacional" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   Ativar os **PWAs da Área de Trabalho executados no experimento de logon do sistema** operacional  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a>Ativar o recurso para o aplicativo Web instalado  

Para ativar o `Start app when you sign in` recurso para um PWA, 

1.  Abra o Microsoft Edge.   
1.  Navegue até `edge://apps`.  
1.  Passe o mouse em seu aplicativo.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Iniciar aplicativo ao entrar**.  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Use o menu contextual para ativar o aplicativo Iniciar quando você entrar no recurso Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       Use o menu contextual para ativar o aplicativo Iniciar quando **você entrar** no recurso Microsoft Edge  
    :::image-end:::  
    
## <a name="shortcuts"></a>Atalhos  

`Shortcuts` é um novo membro do arquivo de manifesto.  Ele permite definir links para partes, páginas da Web principais ou ações em seu aplicativo Web.  O Microsoft Windows o integra como **Jumplists**.  **As listas de opções** definem menus pop-up que aparecem quando você em um dos seguintes elementos da interface do usuário e abre um menu contextual \(clique com o botão direito do mouse\).  

*   Um tile no Menu Iniciar  
*   Um ícone na barra de tarefas  
    
Quando um usuário invoca um atalho, o usuário navega até o endereço especificado pelo `url` membro do atalho.  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Um exemplo de listas de Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   Um exemplo de **listas de Windows 10**  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a>Atalhos no arquivo De manifesto  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a>Propriedades de atalhos  

As propriedades a seguir definem cada atalho.  

| Propriedade | Detalhes |  
|:--- |:--- |  
| `name` | Uma cadeia de caracteres que é exibida para o usuário em **Listas de saltos** ou no menu contextual. |  
| `short_name` | Uma cadeia de caracteres exibida quando há espaço insuficiente para exibir o nome completo do atalho. |  
| `description` | Uma cadeia de caracteres que descreve a finalidade do atalho.  Ele pode ser acessado por tecnologia assistida. |  
| `url` | O URI no aplicativo Web que é aberto quando o atalho é ativado. |  
| `icons` | Um conjunto de ícones que representa o atalho. |  

## <a name="file-handling"></a>Tratamento de arquivos  

A capacidade de se registrar como um manipulador de tipo de arquivo está na fase de experimentação.  Você pode especificar os tipos de arquivo que seu aplicativo lida em uma entrada de manifesto.  Durante a instalação, o sistema operacional host do usuário registra seu aplicativo como um manipulador de arquivos para os tipos de arquivo listados.  Verifique a existência do recurso no código de inicialização de seus aplicativos e `launchQueue` que ele lida com o arquivo.  

Chromium navegadores baseados em dados estão testando e moldando esse recurso.  Para obter mais informações, incluindo exemplos de código, navegue até [Permitir que os aplicativos Web sejam manipuladores de arquivos][WebDevFileHandling].  

Para visualizar o tratamento de arquivos Microsoft Edge para Windows 10, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e a api **de manipulação de arquivos.**  
    
## <a name="providing-feedback-on-experimental-features"></a>Fornecendo comentários sobre recursos experimentais  

Para fornecer comentários sobre Microsoft Edge experimentos de aplicativo Web.  

*   Envie seus comentários usando **Configurações e Mais** \( `...` \) > Enviar comentários para a **Microsoft**.  
*   Selecione `Alt` + `Shift` + `I` .  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentários de sua PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   Enviar comentários de sua PWA  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Testes de origem | Microsoft Edge Desenvolvedor"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registre-se no Registro do Manipulador de Protocolo do Aplicativo Web | Desenvolvedor da Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Manipuladores de protocolo baseados na Web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Recurso poderoso - Permissões | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs como manipuladores de URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que os aplicativos Web sejam manipuladores de arquivos | web.dev"  
[WebDevWindowControlsOverlay]: https://web.dev/window-controls-overlay "Personalizar a sobreposição de controles de janela da barra PWA de título do seu | web.dev"  
