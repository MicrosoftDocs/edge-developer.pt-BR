---
description: Os recursos experimentais mais recentes no Microsoft Edge para Aplicativos Web
title: Recursos experimentais | Aplicativos Web Progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474947"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a>Recursos experimentais em PWAs (Progressive Web Apps)  

O Microsoft Edge fornece acesso a recursos experimentais que ainda estão em desenvolvimento.  Para determinar se cada recurso está pronto e quando lançar cada um, teste e [forneça comentários.](#providing-feedback-on-experimental-features)  

Os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, mas os recursos experimentais mais recentes estão disponíveis apenas no canal Canary do Microsoft Edge.  

## <a name="turn-on-experimental-features"></a>Ativar recursos experimentais  

Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.  
  
1.  Abra o Microsoft Edge.   
    
    > [!NOTE]
    > Certifique-se de usar uma versão do Microsoft Edge que tenha o Experimento listado neste artigo.  Navegue até [Recursos Experimentais](#features-that-are-available-to-test).  
    
1.  Navegue até `edge://flags` .  
1.  Navegue até o experimento relevante.  
1.  Escolha o menu suspenso ao lado da descrição do experimento e escolha `Enabled` .  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Escolha Habilitado para ativar um experimento" lightbox="../media/turn-on-experimental-flag.png":::
       Escolha **Habilitado para** ativar um experimento  
    :::image-end:::  
    
    > [!NOTE]
    > Cada experimento geralmente tem um menu suspenso para escolher os seguintes valores.  Se um recurso experimental não tiver uma entrada em **Experimentos,** serão fornecidas instruções para iniciar o Microsoft Edge com esse recurso usando a linha de comando.
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  Reinicie o Microsoft Edge.  
    
### <a name="origin-trials"></a>Avaliações de Origem  

O Microsoft Edge às vezes usa testes de origem para testar recursos para domínios ou sites específicos.  Talvez você queira usar uma avaliação de origem para seu site para aplicar um recurso específico.  Se você for um proprietário de site, poderá se inscrever em uma avaliação de origem.  Uma avaliação de origem fornece recursos para uma porcentagem de usuários do Microsoft Edge que visitam seu site.

Para obter mais informações sobre as avaliação de origem, navegue até [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].  
    
> [!NOTE]
> Os recursos experimentais são constantemente atualizados e podem causar problemas de desempenho.  Para desativar um recurso experimental, navegue até [Ativar recursos experimentais,](#turn-on-experimental-features)navegue até o experimento e escolha `Disabled` .  

## <a name="features-that-are-available-to-test"></a>Recursos disponíveis para teste  

A lista a seguir descreve os novos recursos experimentais do aplicativo Web que estão disponíveis para testar e validar no Microsoft Edge.  

| Recurso | Versão do Microsoft Edge | Plataforma |  
|:--- |:--- |:--- |  
| [Tratamento de protocolo URI](#uri-protocol-handling) | 91 ou posterior | Windows |    
| [Manipulação de link de URL](#url-link-handling) | 91 ou posterior | Windows|  
| [Executar no logon do sistema operacional](#run-on-os-login) | 88 ou posterior | Todas |  
| [Atalhos](#shortcuts) | 87 ou posterior | Todas |  
| [Tratamento de arquivos](#file-handling) | 83 ou posterior | Toda a área de trabalho |  


## <a name="uri-protocol-handling"></a>Tratamento de protocolo URI  

Um identificador de recurso uniforme \(URI\) pode ser usado para definir mais do que apenas links para páginas da Web e conteúdo da Web usando o protocolo HTTP ou FTP.  URIs podem ser usadas para descrever links para qualquer coisa que você codificar em um esquema.  Por exemplo, o protocolo é usado para descrever um link de email e o sistema operacional \(OS\) ou navegador decide qual página da Web ou `mailto://` aplicativo deve lidar com esse protocolo.  

Para obter mais informações sobre o suporte baseado em navegador existente, navegue até manipuladores de protocolo [baseados na Web.][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]  

Esse recurso permite que você conclua as seguintes ações.  

*   Registrar seu PWA com o sistema operacional host usando o manifesto do seu aplicativo Web
*   Declare que um PWA lida com um protocolo URI específico  
     
Depois de registrar um PWA como um manipulador de protocolo, quando um usuário escolhe um hiperlink com um esquema específico, como ou de um navegador ou um aplicativo nativo, o PWA registrado é ativado pelo sistema operacional e recebe o `mailto://` `web+music://` URI.  

Esse recurso exige que você atualize o manifesto do aplicativo Web para incluir uma matriz, na matriz que você `protocol_handlers` precisa especificar dois campos:  

*   `protocol`: O protocolo para lidar com a solicitação, por exemplo `mailto` ou `web+jngl` .  
*   `url`: O URI HTTPS no escopo do aplicativo que lida com o protocolo.  No futuro, o URI começando com o esquema de manipuladores de protocolo é planejado para substituir o `%s` token.  
    
Atualize seu manifesto para dar suporte ao protocolo que você deseja registrar.  Depois de ativar esse recurso, o Microsoft Edge conclui as seguintes ações.  

1.  Detecta alterações no manifesto  
1.  Registra o aplicativo para o protocolo  
    
Se mais de um aplicativo registrar um protocolo, o usuário será apresentado com um prompt.  O usuário escolhe o aplicativo apropriado na lista apresentada pelo sistema operacional ou navegador.  

Para visualizar a manipulação de protocolo no Microsoft Edge no Windows, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e ause o Suporte a Manipuladores de Protocolo de **Desktop Web Apps.**  

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

Um localizador de recursos uniforme \(URL\) é um tipo de URI.  Crie uma experiência mais envolvente quando os Aplicativos Web Progressivos \(PWAs\) se registrarem como manipuladores para URIs https.  PWAs podem solicitar o lançamento quando URIs associados são ativados.  Por exemplo, se um usuário escolher um link para uma notícia de uma mensagem de email.  Um PWA associado para exibir notícias é automaticamente lançado para manipular a ativação do link.  

Esse recurso permite que você registre um PWA com o navegador usando o manifesto do aplicativo Web e declare que o navegador lida com links específicos.  Para registrar um PWA com o navegador, adicione o `url_handlers` membro opcional ao arquivo de manifesto.  O `url_handlers` membro é um que grupos as `object[]` origens de URIs que o aplicativo deseja manipular.  

A manipulação de links é validada pelo navegador usando um arquivo JSON localizado `web-app-origin-association` na origem.  O arquivo de origem ajusta ainda mais os caminhos incluídos ou excluídos na origem.  Para obter instruções detalhadas sobre como testar o manipulador de URL, navegue até [PWAs como Manipuladores de URL.][GithubWicgPwaUrlHandlerBlobMainExplainerMd]  

Para visualizar a manipulação de link de URL no Microsoft Edge no Windows, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e ause a **Manipulação de URL do PWA da Área**de Trabalho.  

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

O membro contém uma origem que abrange o escopo e também outras origens não `url_handlers` relacionadas do PWA solicitando.  Não restringir URIs ao mesmo escopo ou domínio que o PWA solicitante permite usar nomes de domínio diferentes para o mesmo conteúdo, mas lidar com eles com o mesmo PWA.  

#### <a name="wildcard-matching"></a>Correspondência de caracteres curinga  

Use o caractere curinga \( `*` \) para corresponder a um ou mais caracteres.  

Um prefixo curinga é usado nas cadeias de caracteres de origem do `url_handlers` membro para corresponder a subdomas diferentes.  O prefixo deve `*.` ser para esse uso.  O `https` esquema é assumido quando você usa um prefixo curinga.  

Por exemplo, o `url_handlers` valor do membro é definido como corresponde e , mas não corresponde `*.contoso.com` `tenant.contoso.com` `www.tenant.contoso.com` `contoso.com` .  

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

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

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

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
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

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

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

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

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

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

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

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
-->  

## <a name="run-on-os-login"></a>Executar logon no sistema operacional  

Esse recurso permite configurar seu aplicativo para iniciar automaticamente quando o usuário faz logor no Microsoft Windows.  Várias classes de aplicativos aproveitam a funcionalidade.  As classes de aplicativos incluem email, chat, painel de monitoramento e aplicativos de exibição de dados em tempo real.  A funcionalidade permite que um usuário se envolva com os aplicativos assim que o usuário faz logor no sistema operacional.  Esse recurso inicia automaticamente o PWA da mesma maneira que é iniciado manualmente.  

> [!IMPORTANT]
> **Executar no logon do sistema** operacional é um [recurso poderoso.][GithubW3cPermissionsPowerfulFeature]  Os usuários devem decidir se ativarão o recurso para o aplicativo Web instalado.  

### <a name="turn-on-run-on-os-login"></a>Ativar o logon do sistema operacional  

Para ativar os **recursos de Logon** do [](#turn-on-experimental-features) sistema operacional Run On para o seu PWA, navegue até Ativar recursos experimentais e a ativar PWAs da Área de Trabalho **executados no logon do sistema operacional.**  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Ativar os PWAs da Área de Trabalho executados no experimento de logon do sistema operacional" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   Ativar os **PWAs da Área de Trabalho executados no experimento de logon do sistema** operacional  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a>Ativar o recurso para o aplicativo Web instalado  

Para ativar o `Start app when you sign in` recurso de um PWA instalado, 

1.  Abra o Microsoft Edge.   
1.  Navegue até `edge://apps` .  
1.  Passe o mouse em seu aplicativo.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Iniciar aplicativo ao entrar**.  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Use o menu contextual para ativar o aplicativo Iniciar ao entrar no recurso no Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       Use o menu contextual para ativar o aplicativo **Iniciar ao entrar no** recurso no Microsoft Edge  
    :::image-end:::  
    
## <a name="shortcuts"></a>Atalhos  

`Shortcuts` é um novo membro do arquivo de manifesto.  Ele permite definir links para partes, páginas da Web principais ou ações em seu aplicativo Web.  O Microsoft Windows o integra como **Jumplists.**  **As listas de opções** definem menus pop-up que aparecem quando você em um dos seguintes elementos da interface do usuário e abre um menu contextual \(clique com o botão direito do mouse\).  

*   Um tile no Menu Iniciar  
*   Um ícone na barra de tarefas  
    
Quando um usuário invoca um atalho, o usuário navega até o endereço especificado pelo `url` membro do atalho.  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Um exemplo de Listas de Saltos no Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   Um exemplo de **Listas de Saltos** no Windows 10  
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

Os navegadores baseados em Chromium estão testando e moldando esse recurso.  Para obter mais informações, incluindo exemplos de código, navegue até [Permitir que os aplicativos Web sejam manipuladores de arquivos][WebDevFileHandling].  

Para visualizar o tratamento de arquivos no Microsoft Edge para OSs da área de trabalho, navegue até Ativar recursos [experimentais](#turn-on-experimental-features) e a api **de manipulação de arquivos.**  
    
## <a name="providing-feedback-on-experimental-features"></a>Fornecendo comentários sobre recursos experimentais  

Para fornecer comentários sobre experimentos de aplicativo Web do Microsoft Edge.  

*   Envie seus comentários **usando Configurações e Mais** \( `...` \) > Enviar comentários para a **Microsoft**.  
*   Selecione `Alt` + `Shift` + `I` .  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentários do seu PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   Enviar comentários do seu PWA  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Testes de origem | Desenvolvedor do Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registre-se no Registro do Manipulador de Protocolo do Aplicativo Web | Desenvolvedor da Microsoft"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Manipuladores de protocolo baseados na Web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Recurso poderoso - Permissões | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PWAs como manipuladores de URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que os aplicativos Web sejam manipuladores de arquivos | web.dev"  
