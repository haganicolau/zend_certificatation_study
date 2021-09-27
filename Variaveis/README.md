
# Variáveis

## Descrição

>Entendimento das variáveis em php.

## Lembrar

- PHP é uma linguagem de programação não tipada

- Permite armazenar qualquer tipo de valor: escalar, composto ou especial

- Toda e qualquer variável no PHP deve começar com **$**

- Após o sinal de **$** , deve ser seguido por uma letra e não número;

- Toda e qualquer variável no PHP pode possuir underscores, números e letras.

- Variáveis são case sensitive, ou seja **$variavel** é diferente de **$VaRiAvEl**

- Pode-se definir variáveis com caracteres especiais, tais como ç ,~ , ^.
  - **A única forma de invalidar a sintaxe de uma variável é utilizando números no começo**
  - **Não é recomendado, vai contra boas práticas e recomendações**

- Espaços em branco não podem aparecer entre nomes de variáveis ou palavras-chave.

- Possui dois tipos de passagem de variáveis por valor e por referência.
  - Passagem de parâmetros por valor é o padrão
  - Passagem de parâmetros é usado **&** para sinalizar que a variável é referência, e não uma cópia.
  - Um objeto sempre será passado por referência.

### Variáveis são case sensitives
```php
<?php
ECHO "Hello World"; // works
$variable = "Hello World";
echo $VARIABLE; // won't work
```

### Exemplo variável por valor
```php
$a = 10;
$b = $a;
$b = 20;

echo $a; // 10
echo $b; // 20
```

### Exemplo variável por referencia
```php
$a = 'Por valor';
$b = &$a; // Criando a referência para $a

$a = 'E agora ?';

echo $a; // E agora ?
echo $b; // E agora ?
```

### Strings
- Pode-se usar aspas duplas e asplas simples, com algumas considerações

```php
$simples = 'Olá';
$dupla = "Olá";

/**  Aspas Simples */
$ano = 1990;
echo 'Eu nasci em $ano' // Eu nasci em $ano;

/**  Aspas duplas */
$ano = 1990;
echo "Eu nasci em $ano" // Eu nasci em 1990;
```

## Copyrights
>Documentação criada e mantida por [Hagamenon Oliveira](https://github.com/haganicolau) - [haganicolau@gmail.com](https://mailto:haganicolau@gmail.com)
