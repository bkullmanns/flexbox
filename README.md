# O que é Flexbox?
O **Flexbox** *(Flexible Box)* nos permite organizar, alinhar e distribuir itens dentro de um container. Com ele fica mais simples definir o tamanho e o alinhamento vertical e horizontal de itens.

Primeiro de tudo temos que saber que teremos propriedades CSS para trabalhar com o elemento que possui nossos itens (container ou elemento pai) e propriedades para os nossos itens (elementos filhos).

<br />

## Propriedades "container / elemento pai"

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
    flex-flow: row wrap;
  }
```