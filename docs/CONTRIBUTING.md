# Guia de Contribuição

Este é o guia geral de contribuição para todos os repositórios do [ArapucaJS](https://github.com/arapucajs). Por favor, leia este guia com atenção antes de contribuir 🙏

Código não é a única forma de contribuir! Veja outras maneiras de participar e fazer parte da comunidade:

- Corrigir erros de digitação na documentação
- Melhorar a documentação existente
- Escrever tutoriais ou artigos para ajudar outras pessoas
- Triar issues
- Compartilhar sua opinião em discussões e issues
- Ajudar a comunidade no Discord e nos fóruns de discussão

## Reportando bugs

Muitos problemas relatados em projetos open source são dúvidas ou configurações incorretas. Por isso, recomendamos que você tente resolver o problema antes de abrir uma issue.

Ao relatar um bug, inclua o máximo de informações possível, incluindo exemplos de código. Veja como avaliamos a qualidade das issues:

- **ISSUE PERFEITA**: Você isola o bug, cria um teste que falha no repositório e abre uma issue detalhada.
- **BOA ISSUE**: Você isola o bug e fornece uma reprodução mínima em um repositório no GitHub. Veja [Por que reproduções são importantes](https://antfu.me/posts/why-reproductions-are-required).
- **ISSUE DECENTE**: Você descreve corretamente o problema, compartilha o código que o produz, arquivos de configuração e a versão dos pacotes.
- **ISSUE RUIM**: Você apenas faz uma pergunta esperando que alguém resolva para você. Essas issues podem ser fechadas sem explicação.

Formate sempre seus blocos de código seguindo o [guia de sintaxe Markdown do GitHub](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

## Discussões

Se quiser discutir um tema ou compartilhar ideias, crie uma discussão no fórum, na categoria **💡Ideias**.

## Educando a comunidade

Ensinar é uma das melhores formas de contribuir e ganhar reconhecimento. Use a categoria **📚 Tutoriais** no fórum para compartilhar artigos. O conteúdo deve ser relevante para o projeto.

## Criando Pull Requests

Para evitar frustrações, recomendamos que você [abra uma discussão](#) antes de começar a trabalhar em algo novo.

Explique o que pretende contribuir:

- **Correção de bug**: PRs para bugs geralmente são aceitos após confirmação do problema.
- **Nova funcionalidade**: Explique por que ela é necessária e compartilhe materiais de referência.

> Nota: Esteja disponível para abrir PRs adicionais para documentar a funcionalidade ou melhoria que você contribuiu.

## Configuração do repositório

1. Clone o repositório em sua máquina local:

    ```sh
    git clone <REPO_URL>
    ```

2. Instale as dependências. Não atualize dependências junto com uma feature. Se encontrar dependências desatualizadas, crie um PR separado para isso.

    Usamos o [Bun](https://bun.sh/) para gerenciar dependências. Não use npm, yarn ou outros.

    ```sh
    bun install
    ```

3. Rode os testes com o comando:

    ```sh
    bun test
    ```

## Ferramentas utilizadas

| Ferramenta | Uso |
|------------|-----|
| TypeScript | Todos os repositórios são escritos em TypeScript. O JavaScript compilado e os tipos são publicados no npm. |
| Bun | Usamos o [Bun](https://bun.sh/) para rodar scripts, testes e gerenciar dependências, proporcionando mais velocidade no desenvolvimento. |
| SWC | [SWC](https://swc.rs/) é um compilador TypeScript baseado em Rust, utilizado para ganho de performance na compilação. |
| NP | Usamos [np](https://github.com/sindresorhus/np) para publicar pacotes no npm e GitHub. A configuração está no `package.json`. |
| ESLint | O ESLint garante um estilo de código consistente entre todos os contribuidores. As regras estão no repositório. |
| Prettier | Usamos o Prettier para formatar o código de forma consistente. Veja [Prettier vs. Linters](https://prettier.io/docs/en/comparison.html) para entender a diferença entre eles. |
| EditorConfig | O arquivo `.editorconfig` configura o editor para regras de indentação e espaços. O Prettier faz a formatação final. |
| Conventional Changelog | Todos os commits seguem o padrão [commitlint](https://github.com/conventional-changelog/commitlint/#what-is-commitlint) para mensagens consistentes. |
| Husky | Usamos [husky](https://typicode.github.io/husky/#/) para aplicar convenções de commit via hooks do Git. |

## Comandos

| Comando | Descrição |
|---------|-----------|
| `bun test` | Executa os testes do projeto |
| `bun run build` | Compila o projeto TypeScript para JavaScript, gerando a saída na pasta `build` |
| `bun run release` | Inicia o processo de release usando o np |
| `bun run lint` | Faz a análise do código com ESLint |
| `bun run format` | Formata o código com Prettier |
| `bun run sync-labels` | Sincroniza os labels definidos em `.github/labels.json` com o GitHub (apenas para admins) |

## Estilo de código

Todos os projetos do ArapucaJS são escritos em TypeScript e, gradualmente, estão migrando para ESM puro.

- Siga o padrão de código do projeto e consulte os arquivos de configuração para detalhes.
- Antes de enviar código, execute:

```sh
# Formata com Prettier
bun run format

# Lint com ESLint
bun run lint
```

## Reconhecimento de contribuidores

O GitHub lista todos os contribuidores no painel lateral do repositório.

Também usamos o recurso de [notas de release automáticas](https://docs.github.com/pt/repositories/releasing-projects-on-github/automatically-generated-release-notes#about-automatically-generated-release-notes), que referencia o perfil do contribuidor nas notas de cada release.

---

Dúvidas? Abra uma discussão ou entre em contato pelo Discord oficial do ArapucaJS.

ArapucaJS © Jefte Costa