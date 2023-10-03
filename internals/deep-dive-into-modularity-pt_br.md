
# Um guia detalhado sobre modularidade

Esse texto guiará você para uma compreensão mais profunda sobre como funciona modularidade na linguagem Kod, incluindo detalhes de implementação e exemplos de uso.

## O que é modularidade?

Antes de começarmos, vamos definir o que é modularidade. Modularidade é a capacidade de um sistema ser dividido em partes menores, chamadas de módulos, que podem ser combinadas para formar um sistema maior.

## Módulos no Kod

No Kod, um módulo é um arquivo de código-fonte (arquivo `.kod`) que contém definições de funções, classes, interfaces, variáveis, etc. Um módulo pode ser importado por outros módulos, permitindo que eles acessem as definições contidas nele.

## Como importar um módulo?

Para importar um módulo, use a palavra-chave `import` seguida pelo caminho do arquivo do módulo. Por exemplo, para importar o módulo `foo.kod` localizado no diretório `bar` dentro do diretório atual, você pode fazer o seguinte:

```js
import "bar/foo.kod";
```

Essa é forma é chamada de "importação de módulo local". Existem mais duas formas de importar um módulo: importação de módulo global e importação de pacote.

### Importação de módulo global

A linguagem carrega consigo um conjunto de módulos no escopo global chamado de __Core Modules__. Esses módulos são importados simplesmente especificando o nome do módulo, como no exemplo abaixo:

```js
import io;
```

> Repare na ausência de aspas em torno do nome do módulo.

O mecanismo de importação depende da variável de ambiente `KOD_HOME` que deve apontar para o diretório raiz da instalação do Kod. Se essa variável não for customizada, ocorrera um erro em tempo de execução: "unable to find modules".

### Importação de pacote

Um pacote é um diretório que contém um ou mais módulos (arquivos `.kod`). A importação de um pacote é semelhante à importação de um módulo local quanto ao uso de aspas, mas o caminho do pacote é precedido por um `@`:

```js
import "@foo";
```

Nesse caso, o mecanismo de importação de módulo será regido pela variável de ambiente `KOD_PATH`. Se essa variável não for customizada, será importado o `módulo principal` do pacote `foo` no `diretório de dependências` dentro do diretório atual.

O valor padrão para `KOD_PATH` é `deps/?/main.kod`. Isso significa que o módulo principal é `main.kod` e o diretório de dependências é `deps`. O `?` é um caractere curinga que será substituído pelo nome do pacote. 

Então o caminho completo para o módulo principal do pacote `foo` será `deps/foo/main.kod`.
