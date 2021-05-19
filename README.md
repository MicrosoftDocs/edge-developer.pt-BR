# <a name="microsoft-edge-documentation"></a>Documentação do Microsoft Edge  

## <a name="microsoft-open-source-code-of-conduct"></a>Código de Conduta do Microsoft Open Source  

Para obter mais informações sobre o Código de Conduta do Microsoft Open Source, navegue até [Microsoft Open Source Code of Conduct](CODE_OF_CONDUCT.md).  

## <a name="legal-notices"></a>Avisos legais  

A Microsoft e quaisquer colaboradores concedem uma licença à documentação da Microsoft e a outros conteúdos neste repositório sob a Licença Pública Internacional de Atribuição do [Creative Commons 4.0](https://creativecommons.org/licenses/by/4.0/legalcode), navegue até o arquivo [LICENSE](./LICENSE) e conceda a você uma licença para qualquer código no repositório sob a Licença [MIT](https://opensource.org/licenses/MIT), navegue até o arquivo [LICENSE-CODE.](./LICENSE-CODE)  

Microsoft, Windows, Microsoft Azure e/ou outros produtos e serviços da Microsoft mencionados na documentação podem ser marcas comerciais ou registradas da Microsoft nos Estados Unidos e/ou em outros países/regiões.  
As licenças deste projeto não concedem direitos de uso de quaisquer qualquer nomes, logotipos ou marcas registradas da Microsoft.  
As diretrizes gerais de marca comercial da Microsoft podem ser encontradas em [https://go.microsoft.com/fwlink/?LinkID=254653](https://go.microsoft.com/fwlink/?LinkID=254653) .  

Informações de privacidade podem ser encontradas em [https://privacy.microsoft.com](https://privacy.microsoft.com) .  

A Microsoft e qualquer colaborador se reserva todos os demais direitos, sob seus respectivos direitos autorais, patentes e marcas comerciais, seja por dedução, preclusão ou de outra forma.  

## <a name="contributing"></a>Contribuir  

Este é o repositório para Microsoft Edge **documentação** hospedada em [https://docs.microsoft.com/microsoft-edge](https://docs.microsoft.com/microsoft-edge/index) .  

Se você quiser incluir nova cobertura ou ter comentários, considere [contribuir](./CONTRIBUTING.md)com .  Você pode editar o conteúdo existente, adicionar novo conteúdo ou criar novos [problemas.](https://github.com/MicrosoftDocs/edge-developer/issues)  A Microsoft Edge equipe analisa suas sugestões e trabalha para incorporar as sugestões aos documentos.  

Encontre os dados para a [página da](https://developer.microsoft.com/microsoft-edge/status) Web Status em:  [https://github.com/MicrosoftEdge/Status](https://github.com/MicrosoftEdge/Status) .  A página da Web fornece o status de implementação mais recente e `Status` planos futuros para recursos da plataforma Web Microsoft Edge.

### <a name="conventions"></a>Convenções  

*   Ao adicionar uma página da Web, você deve adicionar uma entrada para ela [toc.md](./microsoft-edge/toc.yml) para que ela apareça.
*   Um diretório pode conter mais diretórios ou `readme.md` s
*   Os nomes de pasta/diretório são separados por traço \(por exemplo, `f12-tools` \) e minúsculos.  Diretórios são usados em URLs no `docs.microsoft.com` site.  Evite usar sublinhados, PascalCase ou camelCase.  

### <a name="other-text-elements"></a>Outros elementos de texto  

Esses outros elementos de texto têm estilo disponível:  

*   Listas semordenadas  
*   Ter marcadores regulares  
    *   Você também pode aninhar marcadores.  
    *   As listas de marcadores devem ter mais de uma entrada.  
*   Acordo padrão 
    
1.  Listas ordenadas.  
1.  Use numeração de estilo ocidental regular.  
1.  Deve ser usado somente quando uma lista realmente tem ordem.  
    
---  

Regras horizontais estão disponíveis.  Use regras horizontais com moderação para reduzir a desordem.  
Evite usar regras horizontais com marcas de título; alguns títulos já usam estilos de linha para hierarquia visual.  

### <a name="displaying-code"></a>Exibindo código  

Você pode usar a sintaxe de marcação em linha `code` \(com os backticks\).  

Ou você pode exibir blocos de código.  O trecho de código a seguir é um exemplo css.  

```css
body {
    background: #fff;
}
```  

### <a name="tables"></a>Tabelas  

| Você pode | usar os headers | em tabelas |  
|:--- |:--- |:--- |  
| Alinhado à esquerda | A menos que um # | 456 |  
| Valor de texto | Mais texto | $0,00 |  

### <a name="notes"></a>Observações  

Use anotações com moderação.  Os blocos foram projetados para realçar as informações de "não falhar".  

Quatro versões diferentes de anotações são atualmente estiladas.  

*   OBSERVAÇÃO  
*   AVISO  
*   DICA  
*   IMPORTANTE  
    
Respectivamente, as anotações se parecem com os trechos de código a seguir.  

```md
> [!NOTE]
> This is a NOTE  
```  

```md
> [!WARNING]
> This is a WARNING  
```  

```md
> [!TIP]
> This is a TIP  
```  

```md
> [!IMPORTANT]
> This is IMPORTANT  
```  

![Padrões de anotações](./media/notes.png)

Para notas de blockquote de várias linhas, use um caractere maior do que \( \) na frente de cada linha das anotações, conforme exibido `>` no exemplo a seguir.  

```md
> This is a line in a blockquote.  
> My text may wrap to more than one line when the markdown is parsed, but I must include all my information within a single \(sometimes very long line\) in the markdown.  
> This is another line in a blockquote.  
```  

### <a name="images"></a>Images  

As imagens devem ser armazenadas em `media` um diretório e referenciadas com um caminho relativo usando script de imagem.  

<!--  `![Note patterns](media/notes.png)`  -->  

```md
:::image type="complex" source="./media/notes.png" alt-text="Note patterns" lightbox="./media/notes.png":::
   Note patterns  
:::image-end:::  
```  
