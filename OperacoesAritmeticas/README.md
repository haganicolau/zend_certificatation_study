# Operadores

## Descrição

>Entendimento dos operadores

## Short Forms

- Sintase mais enxuta, dos operadores ariméticos

### Apresentando código

```php
/** soma **/
$soma += 10;

/** subtração **/
$subtracao -= 10;

/** divisão **/
$divisao /=2;

/** multiplicação **/
$multiplicacao *= 10;

/** módul **/
$modulo %=2;
```

## Operadores de atribuição

```php
/** atribuir valor a uma variável usando o = **/
$variavel = 0;

/** atribuir um valor a um índice de um array usando o => **/
$array[
    0 => 1,
    1 => 2
];
```

## Comparações

- O PHP é uma linguagem não tipada, desta forma existem algumas formas de comparar valores e tipos:
  - usa-se **==** para comparar apenas valores
  - usa-se **===** para comparar valores e tipos  

```php

$variavel1 = 0;
$variavel2 = '0';

/** Compara apenas valores, desconsidera o tipo, a condição é verdadeira, entra no if. **/ 
if($variavel1 == $variavel2) {
    echo "São iguais";
}

/** Compara valores e tipos, a condição é falsa, por que apesar de ambos serem 0, um é inteiro e o 
 * outro string/caracter. 
 **/
if($variavel1 === $variavel2) {
    echo "São iguais";
}

```

## Copyrights

>Documentação criada e mantida por [Hagamenon Oliveira](https://github.com/haganicolau) - [haganicolau@gmail.com](https://mailto:haganicolau@gmail.com)
