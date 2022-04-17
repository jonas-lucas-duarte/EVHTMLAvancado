# Módulo 2 - Criando e Formatando Formulários

### Criando um Formulário

`<FORM artibutos>(conteudo do formulario)</FORM>`

### Atributo **ACTION**

Especifica a URL do *script* que processará os dados do formulário.

`<FORM ACTION="URL">`

- `<FORM ACTION="mailto:endereco@eletronico.com.br">`: Os dados serão enviados ao endereço de *e-mail* especificado.

- `<FORM ACTION="processa.php">`: Os dados serão processados por meio de um código PHP.

### Atributo **METHOD**

Especifica a maneira de envio dos dados do formulário.

Os métodos utilizados são: **POST** e **GET**.

#### **METHOD="POST"**

O navegador enviará diretamente o fluxo de dados para o script CGI no servidor *web*.

> *script Common Gateway Interface (CGI)* é um padrão utilizado por servidores *web* para transmitir o pedido de um usuário para um programa de aplicação e repassar os dados de resposta de volta ao usuário.
>
>Funciona como uma ponte entre o usuário e a aplicação *web*.

#### **METHOD="GET"**

O fluxo de dados será anexado à *URL* especificada no atributo **ACTION** e enviado ao servidor como uma única *URL*.

É utilizados únicas, como uma *string* de texto.

`<FORM ACTION="url" METHOD="get" ou "post">`

### Objetivos do Formulário

Tipos de entrada:

- Texto

- Senha

- Única escolha

- Múltipla escolha

### Tag **INPUT** e seus atributos

Principais atributos:

- *type*

Especifica o tipo de controle a ser criado. Se nada por especificado, o padão é "*text*".

- *value*

Especifica o valor inicial do controle. É opcional, com exceção de quando o TYPE é "*radio*" ou "*checkbox*".

- *name*

Nomeia cada campo do formulário, para que o *script* possa manipular os dados.

- *maxlenght*

Quando o valor de TYPE for "*text*" ou "*password*", eles estabelecem o número máximo de caracteres do campo. O valor padrão é ilimitado.

- *src*

Quando o valor de TYPE for "*image*", este atributo especifica a localização da imagem usada para decorar o botão de enviar.

- *checked*

Quando TYPE tem o valor "*radio*" ou "*checkbox*", este atributo especifica significa que o botão está selecionado.

- *size*

Especifica o tamanho inicial do controle. A largura é dada em *pixels*, com exceção de quando o valor for "*text*" ou "*password*". Nestes casos, o valor refere-se ao número de caracteres.

### Os Possíveis Valores de TYPE

**TYPE**: especifica o **tipo de controle** ou **campo** que será criado.

- *image*

Criar um botão de enviar baseado em uma imagem específica, cuja URL deve ser fornecida.

- *button*

Cria um botão para ser pressionado. O atributo deve ter o nome do botão.

- *radio*

Cria um botão de escolha única.

- *file*

Criar um controle para seleção de arquivo. O valor do atributo deve ser configurado como o nome do arquivo.

- *submit*

Cria um botão de enviar.

- *text*

Cria um campo de texto de uma linha.

- *checkbox*

Cria caixa de seleção.

- *reset*

Cria um botão de *reset*, que limpa todos os campos.

- *password*

Cria um campo texto sem exibir o que está sendo digitado.

- *hidden*

Cria controle oculto.

> Valor padrão: *text*

### Inserindo um Campo de Texto

`<INPUT TYPE=text NAME="Nome" SIZE="20" MAXLENGHT="50">`

- `TYPE=text`: **TYPE** valor que especifica o tipo de entrada como texto.

- `NAME="Nome"`: **NAME** nome da variável que armazena os dados.

- `SIZE="20"`: **SIZE** tamanho do campo, em número de caracteres.

- `MAXLENGHT="50"`: **MAXLENGHT** número máximo de caracteres que podem ser inseridos pelo usuário.

### Atributo **VALUE**

Padrão vazio.

`<INPUT TYPE=text NAME="uf" SIZE="2" VALUE="SP">`

```html
<HTML>
	<HEAD>
		<TITLE>Valor padrão</TITLE>
	</HEAD>

<BODY>
	<FORM ACTION="email@email.com" METHOD="get">
		<P>
			<FONT FACE="CALIBRI">Nome: <INPUT TYPE=TEXT  NAME="nome" SIZE="25" MAXLENGHT="50"></FONT>
		</P>
		<P>
			<FONT FACE="CALIBRI">Estado: <INPUT TYPE =text NAME="uf" SIZE="2" VALUE="SP"></FONT>
		</P>
	</FORM>
</BODY>

</HTML>
```

### Inserindo Campo com Senha

Usado para que ninguém veja os dados que estão sendo inseridos.

`<INPUT TYPE=password NAME="cartao" SIZE="16">`

```html
<HTML>
	<HEAD>
		<TITLE>Campo senha</TITLE>
	</HEAD>

<BODY>
	<FORM ACTION="email@email.com" METHOD="get">
		<P>
			<FONT FACE="Calibri">
				Nome:
				<INPUT TYPE=text NAME="nome" SIZE="25" MAXLENGHT="50">
			</FONT>
		</P>
		<P>
			<FONT FACE="Calibri">
				N° do Cartão:
				<INPUT TYPE=text NAME="num_cartao" SIZE="25" MAXLENGHT="50">
			</FONT>
		</P>
		<P>
			<FONT FACE="Calibri">
				Senha:
				<INPUT TYPE=password NAME="senha" SIZE="6">
			</FONT>
		</P>
	</FORM>
</BODY>

</HTML>
```