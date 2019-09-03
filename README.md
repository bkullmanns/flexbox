# O que é Flexbox?
O **Flexbox** *(Flexible Box)* nos permite organizar, alinhar e distribuir itens dentro de um container. Com ele fica mais simples definir o tamanho e o alinhamento vertical e horizontal de itens.

Primeiro de tudo temos que saber que teremos propriedades CSS para trabalhar com o elemento que possui nossos itens (container ou elemento pai) e propriedades para os nossos itens (elementos filhos).

<br />

## Propriedades "container / elemento pai"
- flex-direction
- flex-wrap
- flex-flow
- justify-content



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

> **Ver exemplo:** [Link](https://marcelopoars.github.io/flexbox/app/04-justify-content/)


<br />


### 6 - align-items
Define o alinhamento dos itens perpendicularmente em relação ao eixo principal. Pense nele como um justify-content, mas que alinhará os itens no outro eixo.

- **stretch (padrão):** estica os elementos para preencherem o container.
- **flex-start:** os itens ficam junto no começo do eixo perpendicular
- **flex-end:** os itens ficam juntos no final do eixo perpendicular
- **center:** os itens ficam centralizados no eixo perpendicular
- **baseline:** parecido com o center, mas usando a base da linha como referência. No exemplo abaixo, note como os textos dos itens ficam alinhados.

```css
.container{
   display: flex;
   align-items: center;  
}
```

> **Ver exemplo:** [Link](https://marcelopoars.github.io/flexbox/app/05-align-items/)


[embed url=http://jsfiddle.net/62kduo09/9/embedded/css,result/dark/]

<br />
