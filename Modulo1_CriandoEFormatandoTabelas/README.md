# Módulo 1 - Criando e Formatando Tabelas

### Por que utilizar tabelas em HTML?

Tabelas possibilitam um alinhamento e organização de informações.

Uma tabela é constituída por **linhas** e **colunas**.

### Criando uma Tabela

A *tag* utilizada é `<TABLE></TABLE>`

- `<TD></TD>`: responsável por criar as células.
- `<TR>`: responsável por criar as linhas.

```html
<HTML>
	<HEAD>
		<TITLE>Criando tabela</TITLE>
	</HEAD>

	<BODY>
		<TABLE>
			<TR>
				<TD> Nome </TD>
				<TD> Sobrenome </TD>
			<TR>
				<TD> Anna </TD>
				<TD> Santos </TD>
			<TR>
				<TD> Vanessa </TD>
				<TD> Medeiros </TD>
		</TABLE>
	</BODY>

</HTML>
```

### Atributos da *tag* **<TABLE>**

#### Atributo **BORDER**

Para determinar a espessura da borda em *pixels*.

`<TABLE BORDER="n° pixels">`

```html
<HTML>
	<HEAD>
		<TITLE>Inserindo borda na tabela</TITLE>
	</HEAD>

<BODY>
	<TABLE BORDER="1">
		<TR>
			<TD>Nome</TD>
			<TD>Sobrenome</TD>
		<TR>
			<TD>Anna</TD>
			<TD>Santos</TD>
		<TR>
			<TD>Vanessa</TD>
			<TD>Medeiros</TD>
	</TABLE>
</BODY>

</HTML>
```

Para determinar a cor da borda.

`<TABLE BORDERCOLOR="cor">`

```html
<HTML>
	<HEAD>
		<TITLE>Inserindo borda colorida</TITLE>
	</HEAD>

<BODY>
	<TABLE BORDER="3" 
	BORDERCOLOR="FF6600">
		<TR>
			<TD>Nome</TD>
			<TD>Sobrenome</TD>
		<TR>
			<TD>Anna</TD>
			<TD>Santos</TD>
		<TR>
			<TD>Vanessa</TD>
			<TD>Medeiros</TD>
	</TABLE>
</BODY>

</HTML>
```

#### Atributo **BGCOLOR**

Define a cor de fundo da tabela toda, quando usada na *tag* `<TABLE>`.

`<TABLE = BGCOLOR="cor">`

```html
<HTML>
	<HEAD>
		<TITLE>Cor de fundo na tabela</TITLE>
	</HEAD>

	<BODY>
		<TABLE BORDER="3" BORDERCOLOR="FF6600" BGCOLOR="CCFFFF">
			<TR>
				<TD> Nome </TD>
				<TD> Sobrenome </TD>
			<TR>
				<TD> Anna </TD>
				<TD> Santos </TD>
			<TR>
				<TD> Vanessa </TD>
				<TD> Medeiros </TD>
		</TABLE>
	</BODY>

</HTML>
```

Para especificar uma célula, o atributo pode ser usado nas tags `<TR>` ou `<TD>`.

`<TR BGCOLOR="cor">` ou `<TD BGCOLOR="cor">`

```html
<HTML >
	<HEAD>
		<TITLE>Cor de fundo na linha/célula</TITLE>
	</HEAD>

<BODY>
	<TABLE BORDER="3" 
	BORDERCOLOR="FF6600">
		<TR BGCOLOR="CCFFFF">
			<TD> Nome </TD>
			<TD> Sobrenome </TD>
		<TR>
			<TD> Anna </TD>
			<TD> Santos </TD>
		<TR>
			<TD> Vanessa </TD>
			<TD BGCOLOR="CCFFFF"> Medeiros </TD>
	</TABLE>
</BODY>

</HTML >
```

#### Atributo **BACKGROUND**

Permite definir uma imagem como fundo da tabela.

`<TABLE BACKGROUND="imagem">`

```html
<HTML>
	<HEAD>
		<TITLE>Inserindo imagem de fundo</TITLE>
	</HEAD>

	<BODY>
		<TABLE BORDER="3" BORDERCOLOR="000066" BACKGROUND="fb.png">
			<TR>
				<TD><B>Nome</B></TD>
				<TD><B>Sobrenome</B></TD>
			<TR>
				<TD>Anna</TD>
				<TD>Santos</TD>
			<TR>
				<TD>Vanessa</TD>
				<TD>Medeiros</TD>
		</TABLE>
		<BR>
		<TABLE BACKGROUND="fb.png">
			<TR>
				<TD><B>Nome</B></TD>
				<TD><B>Sobrenome</B></TD>
			<TR>
				<TD>Anna</TD>
				<TD>Santos</TD>
			<TR>
				<TD>Vanessa</TD>
				<TD>Medeiros</TD>
		</TABLE>
	</BODY>

</HTML>
```

#### Atributos **WIDTH** e **HEIGHT**

Os atributos ***WIDTH*** e ***HEIGHT*** são utilizados para definir a largura e altura da tabela em *pixels* ou porcentagem, uma vez que, por padrão, a célula da tabela assume o tamanho do maior dado inserido:

- ***WIDTH***: largura

- ***HEIGHT***: altura

`<TABLE WIDTH="valor" HEIGHT="valor">`

Os atributos ***WIDTH*** e ***HEIGHT*** também podem ser utilizados para alterar a altura e largura das células.

> Se os valores definidos nestes atributos forem menores que o espaço necessário para visualização dos dados da tabela, o navegador os ignora para garantir a apresentação adequada dos dados.

Neste exemplo, a largura da tabela foi definida em **300 *pixels*** (WIDTH="300") e sua altura ocupará **20%** (HEIGHT="20%") da altura do navegador.

```html
<HTML>
	<HEAD>
		<TITLE>Definindo dimensão da tabela</TITLE>
	</HEAD>

<BODY>
	<TABLE WIDTH="300" HEIGHT="20%" BORDER="2">
		<TR BGCOLOR= #E0EEEE>
			<TD><FONT FACE= "Comic Sans MS"><B>Nome</B></TD>
			<TD><FONT FACE= "Comic Sans MS"><B>Sobrenome</B></TD>
		<TR>
			<TD><FONT FACE= "Calibri">Anna</FONT></TD>
			<TD><FONT FACE= "Calibri">Santos</FONT></TD>
		<TR BGCOLOR = #E0EEEE>
			<TD><FONT FACE= "Calibri">Vanessa</FONT></TD>
			<TD><FONT FACE= "Calibri">Medeiros</FONT></TD>
	</TABLE>
</BODY>

</HTML>
```

#### Atributo **ALIGN**

`<TABLE ALIGN="alinhamento">`

##### **LEFT**

Alinha a tabela à **esquerda** (padrão).

`<TABLE ALIGN="left">Tabela.</TABLE>`

```html
<HTML>
	<BODY>
		<TABLE BORDER="2" ALIGN="left">
			<TR BGCOLOR="#E0EEEE">
				<TD>Nome</TD>
				<TD>Sobrenome</TD>
			<TR>
				<TD>Anna</TD>
				<TD>Santos</TD>
		</TABLE>
	</BODY>
</HTML>
```

##### **CENTER**

Alinha a tabela ao **centro**.

`<TABLE ALIGN="center">Tabela.</TABLE>`

```html
<HTML>
	<BODY>
		<TABLE BORDER="2" ALIGN="center">
			<TR BGCOLOR="#E0EEEE">
				<TD>Nome</TD>
				<TD>Sobrenome</TD>
			<TR>
				<TD>Anna</TD>
				<TD>Santos</TD>
		</TABLE>
	</BODY>
</HTML>
```

##### **RIGHT**

Alinha a tabela à **direita**.

`<TABLE ALIGN="right">Tabela.</TABLE>`

```html
<HTML>
	<BODY>
		<TABLE BORDER="2" ALIGN="right">
			<TR BGCOLOR="#E0EEEE">
				<TD>Nome</TD>
				<TD>Sobrenome</TD>
			<TR>
				<TD>Anna</TD>
				<TD>Santos</TD>
		</TABLE>
	</BODY>
</HTML>
```

#### Atributo **CELLSPACING**

Especifica **o espaço entre a borda da tabela e as células**, sempre em *pixels*.

`<TABLE CELLSPACING="valor">`

```html
<HTML>

	<HEAD>
		<TITLE>Alterando espaçamentos</TITLE>
	</HEAD>

	<BODY>
		<TABLE WIDTH="300" HEIGHT="25%" BORDER="4" CELLSPACING="10">
			<TR BGCOLOR= #E0F8E0>
				<TD ALIGN="center" VALIGN ="center" HEIGHT="40" COLSPAN="2">
					<FONT FACE= "Comic Sans MS"><B>CADASTRO DE CLIENTES</B></FONT>
				</TD>
			<TR BGCOLOR= #E0EEEE>
				<TD>
					<FONT FACE= "Calibri"><B>Nome</B></FONT>
				</TD>
				<TD>
					<FONT FACE= "Calibri"><B>Sobrenome</B></FONT>
				</TD>
			<TR>
				<TD>
					<FONT FACE= "Calibri">Anna</FONT>
				</TD>
				<TD>
					<FONT FACE= "Calibri">Santos</FONT>
				</TD>
			<TR BGCOLOR = #E0EEEE>
				<TD>
					<FONT FACE= "Calibri">Vanessa</FONT>
				</TD>
				<TD>
					<FONT FACE= "Calibri">Medeiros</FONT>
				</TD>
		</TABLE>
	</BODY>

</HTML>
```

#### Atributo **CELLSPACING**

Especifica **o espaço entre os dados e de uma célula**, sempre em *pixels*.

`<TABLE CELLPADDING="valor">`

```html
<HTML>

	<HEAD>
		<TITLE>Alterando espaçamentos</TITLE>
	</HEAD>

	<BODY>
		<TABLE WIDTH="300" HEIGHT="25%" BORDER="4" CELLSPACING="10" CELLPADDING="7">
			<TR BGCOLOR= #E0F8E0>
				<TD ALIGN="center" VALIGN ="center" HEIGHT="40" COLSPAN="2">
					<FONT FACE= "Comic Sans MS"><B>CADASTRO DE CLIENTES</B></FONT>
				</TD>
			<TR BGCOLOR= #E0EEEE>
				<TD>
					<FONT FACE= "Calibri"><B>Nome</B></FONT>
				</TD>
				<TD>
					<FONT FACE= "Calibri"><B>Sobrenome</B></FONT>
				</TD>
			<TR>
				<TD>
					<FONT FACE= "Calibri">Anna</FONT>
				</TD>
				<TD>
					<FONT FACE= "Calibri">Santos</FONT>
				</TD>
			<TR BGCOLOR = #E0EEEE>
				<TD>
					<FONT FACE= "Calibri">Vanessa</FONT>
				</TD>
				<TD>
					<FONT FACE= "Calibri">Medeiros</FONT>
				</TD>
		</TABLE>
	</BODY>

</HTML>
```

### Atributos da *tag* **TD**

#### **ALIGN**

Além de alinhar a tabela em relação à página *web*, o atributo **ALIGN** alinha horizontalmente os dados da célula. Seu valor pode ser especificado como: **LEFT** (esquerda), **RIGHT** (direita) e **CENTER** (centralizado).

`<TD ALIGN="alinhamento">`

```html
<TABLE WIDTH="300" HEIGHT="20%" BORDER="2">
	<TR BGCOLOR="#E0EEEE">
		<TD ALIGN="left"><B>Nome</B></TD>
		<TD ALIGN="left"><B>Sobrenome</B></TD>
	<TR>
		<TD ALIGN="center">Anna</TD>
		<TD ALIGN="right">Santos</TD>
</TABLE>
```

#### **VALIGN**

O atributo **VALIGN** alinha verticalmente os dados da célula. Seu valor pode ser especificado como: **TOP** (cima), **BOTTOM** (baixo) e **CENTER** (centralizado).

`<TD VALIGN="alinhamento">`

```html
<TABLE WIDTH="300" HEIGHT="20%" BORDER="2">
	<TR BGCOLOR="#E0EEEE">
		<TD VALIGN="bottom"><B>Nome</B></TD>
		<TD VALIGN="top"><B>Sobrenome</B></TD>
	<TR>
		<TD VALIGN="center">Anna</TD>
		<TD VALIGN="center">Santos</TD>
</TABLE>
```

#### **COLSPAN**

O atributo **COLSPAN** é utilizado para mesclar células em uma linha.

`<TD COLSPAN="numero">`

```html
<TABLE WIDTH="300" HEIGHT="20%" BORDER="2">
	<TR BGCOLOR="#E0EEEE">
		<TD COLSPAN="2"><B>Dados</B></TD>
	<TR>
		<TD>Anna</TD>
		<TD>Santos</TD>
</TABLE>
```

#### **ROWSPAN**

O atributo **ROWSPAN** é utilizado para mesclar células em uma coluna.

`<TD ROWSPAN="numero">`

```html
<TABLE WIDTH="300" HEIGHT="20%" BORDER="2">
	<TR BGCOLOR="#E0EEEE">
		<TD><B>Nome</B></TD>
		<TD><B>Sobrenome</B></TD>
	<TR>
		<TD>Anna</TD>
		<TD ROWSPAN="2">Santos</TD>
	<TR>
		<TD>Vanessa</TD>
</TABLE>
```