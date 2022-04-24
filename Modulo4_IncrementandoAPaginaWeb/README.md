# Módulo 4 - Incrementando a Página *Web*

### A *Tag* **META** e seus atributos

**Metadados** são informações sobre seus dados. Neste caso, a *tag* `<META>` fornece dados sobre seu documento HTML.

Estes dados servem para descrever as definições da página, palavra-chave, informações sobre o autor, quando foi a última modificação e outras informações.

A *tag* `<META>` deve ser inserida entre as *tags* `<HEAD></HEAD>`.

### O Atributo **CONTENT**

#### NAME

O atributo **NAME** fornece um **nome** para a informação no atributo **CONTENT**.

`<META NAME="valor relativo a name">`

Os valores do atributo **NAME** podem ser:

- **AUTHOR**: Informa o autor do documento.
- **DESCRIPTION**: Descreve o documento.
- **KEYWORDS**: Define as palavras-chave que descrevem o documento.
- **GENERATOR**: Define o programa utilizado para gerar o documento.
- **ROBOTS**: Define regras para os robôs (programas utilizados em sistemas de busca).
- **COPYRIGHT**: Define informações de direitos autorais do documento.

#### HTTP-EQUIV

O atributo **HTTP-EQUIV** fornece um cabeçalho **HTTP** para a informação no atributo **CONTENT**.

`<META HTTP-EQUIV="valor">`

Os valores do atributo **HTTP-EQUIV** podem ser:

- **CONTENT TYPE**: Define o tipo do documento (text/html).
- **EXPIRES**: Define quando o documento será considerado obsoleto.
- **REFRESH**: Define o tempo para a página *web* seja recarregada.
- **SET-COOKIE**: Define o valor de um *cookie*.

Por exemplo, a sintaxe para recarregar uma página automaticamente é `<META HTTP-EQUIV="REFRESH" CONTENT="segundos" URL="novo_URL">`