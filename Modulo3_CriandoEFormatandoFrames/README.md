# Módulo 3 - Criando e Formatando *Frames*

### *Frames*: O que são e para que servem

*Frames* ou molduras são utilizados para **dividir** a janela do navegador em diferentes partes e, cada uma delas pode ser atualizada separadamente.

O *Frame Document* ou *Frameset* é o arquivo que define a estrutura e a distribuição dos *frames* do *site*.

### A *Tag* **FRAMESET**

```html
<HTML>
<HEAD>
	<TITLE>Frames</TITLE>
</HEAD>

<BODY>

	<!--FRAMESET não é suportado por HTML5-->

	<FRAMESET COLS="25%, *, 25%">
		<FRAME SRC="frame_a.html">
		<FRAME SRC="frame_b.html">
		<FRAME SRC="frame_c.html">
	</FRAMESET>
</BODY>
</HTML>
```

O tamanho de cada um dos *frames* com os atributos **COLS** e **ROWS** que especificam, respectivamente, a largura e a altura dos *frames*.

### A *Tag* **FRAME**

#### SRC

Especifica a **URL** que você deseja carregar em um *frame*.

#### MARGINWIDTH

Especifica as **margens direita e esquerda (largura)** do conteúdo em um *frame*. Seu valor é especificado em ***pixels***.

#### MARGINHEIGHT

Especifica as **margens superior e inferior** do conteúdo em um *frame*. Seu valor é especificado em ***pixels***.

#### SCROLLING

Adiciona uma **barra de rolagem** a um *frame*.

#### NORESIZE

Impede que o usuário **redimensione** um *frame*.

### O atributo NAME

Direcionar o *link* para abrir no *frame* desejado.

`<FRAME SRC="phil" NAME="main">`

### Apontando um *frame*

`<A HREF="URL" TARGET="nome_frame">`

Valores para **TARGET**:

- \_balnk: Abre o *link* em uma nova janela.

- \_self: Abre o *link* no mesmo *frame*.

- \_parent: Carrega a página no *frame* principal.

- \_top: Carrega a página no *frame* mais alto da página.

`<A HREF="exemplo.html" TARGET="_blank">Clique aqui</A>`