# O que é Flexbox?
O **Flexbox** *(Flexible Box)* nos permite organizar, alinhar e distribuir itens dentro de um container. Com ele fica mais simples definir o tamanho e o alinhamento vertical e horizontal de itens.

Primeiro de tudo temos que saber que teremos propriedades CSS para trabalhar com o elemento que possui nossos itens (container ou elemento pai) e propriedades para os nossos itens (elementos filhos).

<br />

## Propriedades para itens "container / elemento pai"
- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content


### 1 - dispplay
Primeiro precisamos definir que o nosso container é do tipo **“flex”**; Fazemos isso com a propriedade **“display”**.
No exemplo abaixo, utilize o checkbox para ligar/desligar o Flexbox.

```css
.container{
   display: flex;  
}
```

> **Ver exemplo:** [Link](https://marcelopoars.github.io/flexbox/app/01-display/)


<br />


### 2 - flex-direction
Indica a direção dos itens, definindo o que vamos chamar de eixo principal (main-axis).

- **row (padrão):** da esquerda para direita
- **row-reverse:** inverso de row
- **column:** de cima para baixo
- **column-reverse:** inverso de column

```css
.container{
   display: flex;
   flex-direction: row;  
}
```

> **Ver exemplo:** [Link](https://marcelopoars.github.io/flexbox/app/02-flex-direction/)


<br />


### 3 - flex-wrap
O comportamento padrão dos itens de um elemento flex é ficar em uma única linha. Se a largura total de todos os itens for maior do que o espaço disponível, os itens continuarão na mesma linha.

Esta propriedade permite que os itens sejam jogados em outra linha caso não haja mais espaço na linha.

- **nowrap (padrão):** todos os itens ficam em uma única linha
- **wrap:** os itens que não cabem na linha são jogados para baixo
- **wrap-reverse:** os itens que não cabem na linha são jogados para cima

```css
.container{
   display: flex;
   flex-wrap: wrap;  
}

.item{
   width: 40%;  
}
```

> **Ver exemplo:** [Link](https://marcelopoars.github.io/flexbox/app/03-flex-wrap/)


<br />


### 4 - flex-flow
Esta propriedade é apenas um atalho para flex-direction e flex-wrap, nos permitindo declarar o valor de ambos em uma única propriedade.

```css
.container {
    display: flex;
    flex-flow: row wrap; /* flex-direction / flex-wrap */
  }
```


<br />


### 5 - justify-content
Define o alinhamento dos itens ao longo do **eixo principal**.

- **flex-start (padrão):** os itens ficam junto no começo da linha
- **flex-end:** os itens ficam juntos no final da linha
- **center:** os itens ficam centralizados na linha
- **space-between:** os itens são distribuídos igualmente no espaço disponível. O primeiro item fica no começo da linha e o último fica no final.
- **space-around:** os itens são distribuídos igualmente no espaço disponível ao redor deles.
- **space-evenly:** os itens são distribuídos igualmente no espaço disponível.

```css
.container{
   display: flex;
   justify-content: space-around;  
}
```

> **Ver exemplo (row):** [Link](https://marcelopoars.github.io/flexbox/app/04-justify-content/row)

<br />

### flex-direction: column
Lembre-se que esta propriedade alinha os itens em relação ao **eixo principal**. Isso significa que se você mudar o valor de **flex-direction**, a direção do posicionamento será outra.

```css
.container{
   display: flex;
   flex-direction: column;
   justify-content: flex-start;  
}
```

> **Ver exemplo (column):** [Link](https://marcelopoars.github.io/flexbox/app/04-justify-content/column)


<br />


### 6 - align-items
Define o alinhamento dos itens perpendicularmente em relação ao **eixo principal**. Pense nele como um **justify-content**, mas que alinhará os itens no outro eixo.

- **stretch (padrão):** estica os elementos para preencherem o container.
- **flex-start:** os itens ficam junto no começo do eixo perpendicular
- **flex-end:** os itens ficam juntos no final do eixo perpendicular
- **center:** os itens ficam centralizados no eixo perpendicular
- **baseline:** parecido com o center, mas usando a base da linha como referência. No exemplo abaixo, note como os textos dos itens ficam alinhados.

```css
.container{
   display: flex;
   align-items: flex-start;  
}
```

> **Ver exemplo (row):** [Link](https://marcelopoars.github.io/flexbox/app/05-align-items/row)

<br />

### flex-direction: column
Lembre-se que esta propriedade alinha os itens em relação ao **eixo principal**. Isso significa que se você mudar o valor de **flex-direction**, a direção do posicionamento será outra.

```css
.container{
   display: flex;
   flex-direction: column;
   align-items: flex-start; 
}
```

> **Ver exemplo (column):** [Link](https://marcelopoars.github.io/flexbox/app/05-align-items/column)


<br />


### 6 - align-content
Alinha as linhas do container.
Por alinhar as linhas, esta propriedade só tem efeito quando há mais de uma linha.

- **stretch (padrão):** estica as linhas para preencherem o espaço restante.
- **flex-start: as linhas** ficam juntas no começo do container
- **flex-end:** as linhas ficam juntas no final do container
- **center:** as linhas ficam centralizadas no container
- **space-between:** as linhas são distribuídas igualmente. A primeira linha fica no começo do container e a última fica no final.
- **space-around:** as linhas são distribuídas igualmente no espaço disponível ao redor delas.

```css
.container{
   display: flex;
   flex-wrap: wrap;
   align-content: flex-start;   
}
```

> **Ver exemplo (row):** [Link](https://marcelopoars.github.io/flexbox/app/06-align-content/row)

<br />

### flex-direction: column
Lembre-se que esta propriedade alinha os itens em relação ao **eixo principal**. Isso significa que se você mudar o valor de **flex-direction**, a direção do posicionamento será outra.

```css
.container{
   display: flex;
   flex-wrap: wrap;
   flex-direction: column;
   align-content: flex-start;  
}
```

> **Ver exemplo (column):** [Link](https://marcelopoars.github.io/flexbox/app/06-align-content/column)


<br /><br />
<hr />
<br /><br />




## Propriedades para itens "elemento pai"
Agora veremos as propriedades que ficam nos elementos filhos. Teremos basicamente um container com alguns itens dentro.

- order
- flex-grow
- flex-basis
- flex-shrink
- flex
- align-self

Para vermos a diferença das propriedades aplicadas em um item específico, vamos adicionar a este item a classe **.selected**.


```html
<div class="container" >
    <div class="item" ></div>
    <div class="item selected" ></div>
    <div class="item" ></div>
</div>
```
