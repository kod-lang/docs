
# A Linguagem de Programação Kod

Bem-vindo à documentação oficial da linguagem de programação Kod!

> **Nota:** Este projeto ainda está em desenvolvimento.

## Por que mais uma linguagem de programação?

Kod visa atingir um equilíbrio único: é projetada para ser fácil de aprender e prática de usar. Além disso, sua arquitetura é simples, tornando-a um excelente recurso educacional para aqueles interessados em aprender sobre design de compiladores e implementação de linguagens. No entanto, não a confunda com um simples brinquedo educativo; Kod é uma linguagem de programação totalmente funcional, capaz de alimentar aplicações do mundo real. Ela se inspira em linguagens bem estabelecidas como Lua, Python e JavaScript, mas tem seus próprios méritos.

## Como ela é?

Para lhe dar uma ideia de como é Kod, aqui está um simples script "Olá, Mundo!":

```js
println("Hello, World!");
```

Para um exemplo mais complexo, considere esta função para calcular fatoriais:

```js
function factorial(n) {
  if (n == 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
```

Como você pode ver, a sintaxe de Kod lembra a de JavaScript, enquanto suas semânticas compartilham similaridades com Python. No entanto, Kod não pretende ser um clone de qualquer uma dessas linguagens; ela visa criar seu próprio espaço, completo com seus recursos exclusivos.

## Quais são suas características?

Aqui estão algumas das características notáveis de Kod:

- **Leve:** Projetada para uma implementação leve e sintaxe simples, Kod é leve em termos de recursos do sistema.

- **Incorporável:** Kod pode ser facilmente incorporada em outras aplicações, ostentando uma simples API em C que lembra o modelo líder do setor de Lua.

- **Interoperabilidade:** A comunicação perfeita entre Kod e C é possível graças aos recursos de interoperabilidade, permitindo que os dados sejam trocados sem esforço.

- **Multiplataforma:** Escrita em C, Kod oferece suporte para Windows, macOS e Linux, e pode ser facilmente portada para outras plataformas.

- **Imperativa com toque funcional:** Primariamente uma linguagem imperativa, Kod também suporta paradigmas de programação funcional, oferecendo flexibilidade na escolha da abordagem mais adequada para cada tarefa.

- **Tipagem dinâmica:** Kod emprega tipagem dinâmica, permitindo que as variáveis sejam atribuídas a um tipo em tempo de execução para maior flexibilidade. No entanto, isso vem com uma troca de desempenho.

- **Anotações de tipo opcionais:** Você pode anotar opcionalmente os tipos de variáveis, bem como os tipos de parâmetro e retorno, para melhorar a segurança de tipo.

- **Escopo lexical:** O escopo da variável é determinado por sua colocação no código-fonte, permitindo funções aninhadas e facilitando a criação de closures.

- **Interfaces:** A linguagem inclui suporte para interfaces, permitindo que você defina um conjunto de métodos que um tipo deve implementar. Isso fornece uma forma de polimorfismo sem depender de herança.

- **Cidadãos de primeira classe:** Funções, classes e interfaces são todos cidadãos de primeira classe em Kod. Essa escolha de design permite que eles sejam passados e manipulados como qualquer outro tipo de dado.

- **Semântica de Valor Mutável:** Kod emprega semântica de valor mutável, que restringe o compartilhamento de estados mutáveis entre variáveis e entre diferentes escopos.

- **Geradores:** A linguagem suporta funções especializadas que podem pausar e retomar sua execução. Essa funcionalidade permite a criação de iteradores personalizados.

- **Contagem de Referência:** O gerenciamento de memória é tratado por meio da contagem de referência, liberando a memória assim que ela não é mais necessária e evitando a necessidade de um coletor de lixo de rastreamento.

## Licença

Kod está licenciada sob a licença [MIT](https://choosealicense.com/licenses/mit).  Para mais informações, consulte o arquivo [LICENSE](LICENSE).
