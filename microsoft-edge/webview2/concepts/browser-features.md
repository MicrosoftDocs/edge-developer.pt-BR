---
description: Diferenças de recursos entre o título Microsoft Edge e WebView2: Diferenças de recursos entre o autor Microsoft Edge e WebView2: MSEdgeTeam ms.author: msedgedevrel ms.date: 05/06/2021 ms.topic: conceptual ms.prod: microsoft-edge ms.technology: webview keywords: IWebView2, IWebView2WebView, WebView2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda no-loc:
- "Autofill for Addresses"
- "Autofill for Passwords"
- "Autofill for Payments""
- "Browser Extensions""
- "Browser Task Manager"
- "Collections"
- "Continue-where-I-left-off prompt"
- "Downloads"
- "Edge Shopping"
- "Family Safety"
- "Favorites"
- "Hotkeys"
- "IE Mode"
- "Immersive Reader"
- "Intrusive Ads"
- "Read Aloud"
- "Smart Screen"
- "Translate"
- "Tracking Prevention"
- "Profile and Identity"
- "Web Payment API"
- "Windows Defender Application Guard"
- "edge:// URLs"

---
# <a name="browser-feature-differences-between-microsoft-edge-and-webview2"></a>Diferenças de recursos do navegador entre Microsoft Edge e WebView2  

WebView2 se baseia no novo navegador Microsoft Edge.  Você tem a oportunidade de estender recursos do navegador para aplicativos baseados em WebView2, o que é útil.  No entanto, como o WebView2 não está limitado a aplicativos parecidos com navegador, há alguns recursos do navegador que precisam ser modificados ou removidos.  Este artigo fornece as informações a seguir.  

*   Os recursos modificados do navegador e informações de suporte.   
*   A capacidade de ativar ou desativar o recurso.  
*   Diretrizes sobre atalhos de teclado.  
    
## <a name="design-guidelines"></a>Diretrizes de design  

No contexto do WebView2, os recursos do navegador seguem as seguintes diretrizes de design.  

*   A maioria dos recursos funciona da mesma forma no WebView2 e Microsoft Edge.  Se um recurso não fizer sentido no contexto do WebView2 ou por outros motivos, o recurso será modificado ou desligado. 
*   Os recursos do WebView2 não incluem Microsoft Edge identidade visual.  
    
## <a name="features"></a>Recursos  

A tabela a seguir exibe os recursos WebView2 que diferem do Microsoft Edge navegador.   

*   **O estado** padrão indica que o recurso faz parte da experiência padrão em uma nova instância do WebView2.  
*   **Configurável** indica que você pode ativar ou desativar o recurso usando APIs WebView2 ou comutadores de linha de comando.  
    
> [!NOTE]  
> Este artigo não abrange a modificação de recursos usando comutadores de linha de comando.  Para obter mais informações sobre como ligar e desligar recursos com opções de linha de comando, navegue até [Lista de][PeterExperimentsChromiumCommandLineSwitches]opções de linha de comando Chromium comando .  
    
| Recurso | Estado padrão | Configurável | Detalhes |  
|:--- |:--- |:--- | :--- |  
| Autofill for Addresses | Ativado | Sim | Esse recurso é ligado por padrão, você pode autá-lo ou desativar usando APIs de Preenchimento Automático webView2.  |  
| Autofill for Passwords | Ativado | Sim | Esse recurso é ligado por padrão, você pode autá-lo ou desativar usando APIs de Preenchimento Automático webView2.  |  
| Preenchimento automático para pagamentos | Desativado | Não | Esse recurso está desligado.  |  
| Extensões do Navegador | Desativado | Não | Esse recurso está desligado.  |  
| Browser Task Manager | Desativado | Não | Esse recurso está desligado.  |  
| Collections | Desativado | Não | Esse recurso está desligado.  |  
| Continue-where-I-left-off prompt | Desativado | Não | Esse recurso está desligado.  |  
| Downloads | Ativado | Sim | WebView2 fornece uma API que permite personalizar a interface do usuário de download para manipular downloads. Por exemplo, você pode bloquear, redirecionar, salvar, pausar e assim por diante.  <!--For more information, navigate to [download API][Webview2ReferenceDownloadApi].--> |  
| Edge Shopping | Desativado | Não | Esse recurso está desligado.  |  
| Family Safety | Desativado | Não | Esse recurso está desligado.  |  
| Favorites | Desativado | Não | Esse recurso está desligado.  |  
| IE Mode | Desativado | Não | Esse recurso está desligado.  |  
| Immersive Reader | Desativado | Não | Esse recurso depende da interface do usuário do navegador para interação.  Esse recurso está desligado.  |  
| Intrusive Ads | Desativado | Não | Esse recurso está desligado.  |  
| Atalhos de teclado | Revisar detalhes | Revisar detalhes | Os atalhos de teclado que estão desligados por padrão não fazem sentido ou causam problemas no WebView2.  Você pode não ativar ou desativar esses atalhos.  Em vez disso, você pode escutar uma combinação de teclas usando o `AcceleratorKeyPressed` evento e criar uma resposta personalizada, se necessário.  Para obter mais informações, navegue [até Informações adicionais de atalhos de teclado.](#additional-keyboard-shortcuts-information) |  
| Notificações por push | Desativado | Não | Esse recurso não é implementado no WebView2.  Para obter mais informações, navegue até Adicionar suporte à API de Notificação [html5 (#308)][GithubMicrosoftedgeWebview2feedbackIssues308]. |  
| Read Aloud | Desativado | Não | Esse recurso está desligado.  |  
| Smart Screen | Ativado`*` | Não | `*` A interface do usuário para esse recurso foi removida, no entanto, a funcionalidade subjacente ainda está disponível.  Além disso, você pode desativar Smart Screen usando uma opção de linha de comando.  |  
| Translate | Desativado | Não | Esse recurso está desligado.  |  
| Tracking Prevention | Ativado`*` | Não | `*` A interface do usuário para esse recurso foi removida, no entanto, a funcionalidade subjacente ainda está disponível.  A prevenção de rastreamento sempre é definida como equilibrada.|  
| Profile and Identity | Desativado | Não | O recurso que sincroniza seus favoritos, cookies e assim por diante está desligado.  |  
| Web Payment API | Desativado | Não | Esse recurso está desligado.  | 
| Windows Defender Application Guard | Desativado | Não | Esse recurso está desligado.  |  
| edge:// URLs | Revisar detalhes | Não | Configurações para o Microsoft Edge navegador estão em `edge://` URLs.  Como a maioria dessas páginas da Web Microsoft Edge a identidade visual ou não faz sentido no contexto do WebView2, algumas dessas URLs são desligadas.  Para obter mais informações, navegue até [URLs internas bloqueadas.](#blocked-internal-urls)  |  

## <a name="blocked-internal-urls"></a>URLs internas bloqueadas  

As páginas Microsoft Edge e as configurações do Google Chrome não estão disponíveis no WebView2.  

*   `chrome-search://local-ntp/local-ntp.html`  
*   `edge://application-guard-internals`  
*   `edge://apps`  
*   `edge://compat`  
*   `edge://extensions`  
*   `edge://favorites`  
*   `edge://help`  
*   `edge://management`  
*   `edge://network-error`  
*   `edge://new-tab-page`  
*   `edge://newtab`  
*   `edge://omnibox`  
*   `edge://settings`  
*   `edge://supervised-user-internals`  
*   `edge://version`  
    
## <a name="additional-keyboard-shortcuts-information"></a>Informações adicionais de atalhos de teclado  

Atalhos de teclado ou vinculações de teclas são suportados Microsoft Edge WebView2.  Quando Microsoft Edge atualizações, as vinculações de teclas padrão podem mudar.  Além disso, um atalho de teclado que está desligado por padrão pode ativar se o recurso agora tiver suporte no WebView2.  Para evitar alterações nos atalhos de teclado, você pode definir como , que desliga todas as teclas que acessam os recursos do navegador, mas mantém todos os atalhos básicos de edição de texto e movimento `AreBrowserAcceleratorKeysEnabled` `FALSE` ativas.  

A tabela a seguir lista os atalhos que estão sempre desligados no WebView2.  Um caractere asterisco \( \) indica que o atalho não está desligado, mas o recurso que ele acessa está desligado ou não se aplica `*` ao WebView2.  

| Ação | Windows |  
|:--- |:--- |  
| Adicionar ao Favorites | `Ctrl`+`D` |  
| Adicionar Todas as Guias Favorites | `Ctrl`+`Shift`+`D` |  
| Local de foco | `Ctrl`+`L, Alt`+`D` |  
| Colar e Ir | `Ctrl`+`Shift`+`L` |  
| Abrir Arquivo | `Ctrl`+`O` |  
| Read Aloud `*` | `Ctrl`+`Shift`+`U` |  
| Captura da Web `*` | `Ctrl`+`Shift`+`S` |  
| Barra lateral `*` | `Ctrl`+`Shift`+`E` |  
| Salvar Página | `Ctrl`+`S` |  
| Selecione Última Guia | `Ctrl`+`9` |  
| Selecionar Próxima Guia | `Ctrl`+`Tab` |  
| Selecionar Guia Anterior | `Ctrl`+`Shift`+`Tab` |  
| Selecione Guia \(1 - 8\) | `Ctrl`+`(1-8)` |  
| Mostrar Favorites Barra `*` | `Ctrl`+`Shift`+`B` |  
| Ajuda | `F1` |  
| Painel de Foco Próximo `*` | `F6` |  
| Painel Anterior de Foco `*` | `Shift`+`F6` |  
| Navegação de caret `*` | `F7` |  
| Modo de Leitura `*` | `F9` |  
| Barra de menus de foco | `F10` |  
| Mostrar Menu Identidade `*` | `Ctrl`+`Shift`+`M` |  
| Browser Task Manager `*` | `Shift`+`Escape` |  
| Comentários de Borda `*` | `Shift`+`Alt`+`I` |  
| Guia Mudo `*` | `Ctrl`+`M` |  
| Nova Janela Incógnita | `Ctrl`+`Shift`+`N` |  
| Nova Guia | `Ctrl`+`T` |  
| Nova Janela | `Ctrl`+`N` |  
| Restaurar a última guia fechada | `Ctrl`+`Shift`+`T` |  
| Foco Favorites | `Alt`+`Shift`+`B` |  
| Foco Pop-up Inativo | `Alt`+`Shift`+`A` |  
| Pesquisa de Foco | `Ctrl`+`E`, `Ctrl`+`K`, `Search Key` |  
| Guia Duplicado | `Ctrl`+`Shift`+`K` |  
| Barra de Ferramentas de Foco `*` | `Alt`+`Shift`+`T` |  
| Início | `Alt`+`Home`, `Browser Home Key` |  
| Mostrar Menu do aplicativo | `Alt`+`E, Alt`+`F` |  
| Mostrar Favorites | `Ctrl`+`Shift`+`O` |  
| Mostrar Downloads | `Ctrl`+`J` |  
| Mostrar Histórico | `Ctrl`+`H` |  
| Mostrar Barra de Modo de Leitura `*` | `Shift`+`Alt`+`R` |  
| Mostrar Collections `*` | `Ctrl`+`Shift`+`Y` |  

Os atalhos de teclado a seguir estão sempre desligados, exceto nas janelas que são exibidas quando `NewWindowRequested` o evento não é manipulado.

| Ação | Windows |  
|:--- |:--- |  
| Guia Fechar | `Ctrl`+`W, Ctrl`+`F4` |  
| Fechar Janela | `Ctrl`+`Shift`+`W` |  
| Tela inteira | `F11` |  

Se você definir `AreBrowserAcceleratorKeysEnabled` como , os seguintes `FALSE` atalhos de teclado adicionais serão desligados.  

| Ação | Windows |  
|:--- |:--- |  
| Parar | `Escape` |  
| Encontrar na página | `Ctrl`+`F` |  
| Find Next | `Ctrl`+`G` |  
| Encontrar Anterior | `Ctrl`+`Shift`+`G` |  
| Print | `Ctrl`+`P` |  
| Atualizar | `Ctrl`+`R`, `F5`, `Reload Key` |  
| Atualizar sem cache | `Ctrl`+`Shift`+`R`, `Ctrl`+`F5`, `Shift`+`F5`, `Ctrl`+`Refresh`, `Shift`+`Refresh` |  
| Diminuir o zoom | `Ctrl`+`-` |  
| Ampliar | `Ctrl`+`+` |  
| Redefinir Zoom | `Ctrl`+`0` |  
| Find Next | `F3` |  
| Encontrar Anterior | `Shift`+`F3` |  
| Voltar | `Alt`+`Left, Browser Back Key` |  
| Avançar | `Alt`+`Right`, `Browser Forward Key` |  
| Print | `Ctrl`+`P` |  
| Abrir / Fechar DevTools | `Ctrl`+`Shift`+`I` |  
| Abrir Console do DevTools | `Ctrl`+`Shift`+`J` |  
| Abrir DevTools Inspect | `Ctrl`+`Shift`+`C` |  

> [!Note] 
> Para personalizar qualquer uma das teclas individualmente, use o [evento AcceleratorKeyPressed.][DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview2-team"></a>Entrar em contato com a equipe Microsoft Edge WebView2  

[!INCLUDE [contact WebView2 team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

<!--[Webview2ReferenceDownloadApi]: ./download-api.md "download API | Microsoft Docs"  -->  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2controller.acceleratorkeypressed?view=webview2-dotnet-1.0.774.44&preserve-view=true "Evento CoreWebView2Controller.AcceleratorKeyPressed | Microsoft Docs"  

[DevtoolsShortcutsIndex]: ../../devtools-guide-chromium/shortcuts/index.md "Microsoft Edge Atalhos de teclado do DevTools | Microsoft Docs"  

[GithubMicrosoftedgeWebview2feedbackIssues308]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/308 "Adicionar suporte para a API de Notificação de HTML5 (#308) | GitHub"  

[PeterExperimentsChromiumCommandLineSwitches]: https://peter.sh/experiments/chromium-command-line-switches "Lista de opções Chromium linha de comando | Pedro Beverloo"  
