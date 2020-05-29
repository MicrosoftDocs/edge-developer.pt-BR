# Documentação do Microsoft Edge

## Código de conduta do Microsoft Open Source

Este projeto adotou o [código de conduta do Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/).
Para obter mais informações, consulte o [código de conduta frequente](https://opensource.microsoft.com/codeofconduct/faq/) ou entre em contato com a [opencode@microsoft.com](mailto:opencode@microsoft.com) de contato com perguntas ou comentários adicionais.

## Avisos legais
A Microsoft e qualquer colaborador concede a você uma licença para a documentação da Microsoft e outros conteúdos neste repositório em [Licença pública internacional da Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode), consulte o arquivo [LICENÇA](LICENSE), and e concede a você uma licença para qualquer código no repositório em [Licença de MIT](https://opensource.org/licenses/MIT), consulte o arquivo [CÓDIGO DE LICENÇA](LICENSE-CODE).

Microsoft, Windows, Microsoft Azure e/ou outros produtos e serviços da Microsoft mencionados na documentação podem ser marcas comerciais ou registradas da Microsoft nos Estados Unidos e/ou em outros países/regiões.
As licenças deste projeto não concedem direitos de uso de quaisquer qualquer nomes, logotipos ou marcas registradas da Microsoft.
As diretrizes de marca-s gerais da Microsoft podem ser encontradas em https://go.microsoft.com/fwlink/?LinkID=254653 .

As informações de privacidade podem ser encontradas emhttps://privacy.microsoft.com

A Microsoft e qualquer colaborador se reserva todos os demais direitos, sob seus respectivos direitos autorais, patentes e marcas comerciais, seja por dedução, preclusão ou de outra forma.

## Ricoh

Este é o repositório para a **documentação** do Microsoft Edge hospedado em [https://docs.microsoft.com/microsoft-edge/](https://docs.microsoft.com/microsoft-edge/) .

Se você quiser ver a nova cobertura ou tiver comentários, pense em [**colaborar**](/CONTRIBUTING.md).  Você pode editar o conteúdo existente, adicionar novo conteúdo ou simplesmente criar novos [problemas](https://github.com/MicrosoftDocs/edge-developer/issues). Vamos dar uma olhada em suas sugestões e trabalhar em conjunto para incorporá-las aos documentos.

Encontre os dados para a [`Status`](https://dev.windows.com/microsoft-edge/platform/status/) página em: https://github.com/MicrosoftEdge/Status . A `Status` página fornece o status de implementação mais recente e os planos futuros para recursos da plataforma Web no Microsoft Edge.

### Convention

- Ao adicionar uma página, você deve adicionar uma entrada para ela em [TOC.MD](microsoft-edge/toc.md) para que ela seja exibida.
- Uma pasta pode conter mais pastas ou `readme.md` s
- Os nomes de pasta/diretório são separados por traço (por exemplo, `f12-tools` ) e em minúsculas. Elas são usadas em URLs no site do docs.microsoft.com. Não use sublinhados ou PascalCase/camelCase.

### Outros elementos de texto

Esses outros elementos de texto têm estilo disponível:

* Listas não ordenadas
* Ter marcadores normais
   * Você também pode aninhar marcadores.
   * Listas de marcadores devem ter mais de uma entrada.
* Excelente padrão

1. Listas ordenadas.
2. Use a numeração de estilo oeste "OL" comum.
3. Deve ser usado apenas quando uma lista realmente tem ordem.

_________________________

As réguas horizontais estão disponíveis. Sugerimos usá-las com moderação para reduzir o lixo.
Não combine as réguas horizontais com as marcas de título; alguns estilos de linha já usados para hierarquia visual.

### Exibir código

Você pode usar `code` a sintaxe de redução embutida (com o backticks).

Ou você pode exibir blocos de código como:

```css
body {
    background: #fff;
}
```

### Tabelas

| É possível     | usar cabeçalhos | em tabelas    |
|-------------|-------------|-------------:|
| Alinhado à esquerda| A menos que um #  | 456          |
| Valor de texto  | Mais texto   | $0        |

### Observações

Use anotações com moderação. Eles são blocos projetados para destacar as informações "não perca".

No momento, há quatro versões diferentes de anotações em estilo:
- OBSERVAÇÃO
- Avisa
- TAMPA
- IMPORTANTE

Respectivamente, eles são semelhantes a:

![Padrões de nota](./media/notes.png)

```
> [!WARNING]
> Hello. Yes. I am a warning note that has been automagically created. My text may wrap to more than one line when the Markdown is parsed, but I must include all my information within a single (sometimes very long line) in the Markdown itself.```

For multi-line blockquote notes, use a > in front of each line of the notes as seen in the example below.

```


### Images

As imagens devem ser armazenadas em uma `media` pasta e referenciadas com um caminho relativo:

`![Note patterns](media/notes.png)`
