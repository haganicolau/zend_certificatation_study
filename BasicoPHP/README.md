
#Básico PHP

## Descrição

>Concentra-se nos detalhes essenciais do PHP como uma linguagem.

## Básico da linguagem

- Todas as instruções em PHP devem terminar com um ponto e vírgula. 
  - Uma exceção a isso é se o declaração passa a ser a última declaração antes de uma tag de fechamento.
- O espaço em branco não tem significado semântico em PHP.
  - Não há necessidade de alinhar o código (padrões de codificação)
- Os blocos de código são denotados pelos símbolos de chave { }.
- Nomes de funções não fazem distinção entre maiúsculas e minúsculas, mas variáveis e nomes de constantes fazem.
- Embora o PHP seja uma linguagem de script geral e possa ser usado para outros fins, é mais comumente implantado como 
uma linguagem de script do lado do servidor usada para construir paginas web.
- O interpretador PHP não analisa nada que não esteja incluído entre tags que indiquem script PHP
  - PHP para ser embutido em HTML.
- É bastante comum em programas PHP omitir a tag de fechamento?> Em um arquivo.
  - forma útil de evitar problemas com caracteres de nova linha aparecendo após a tag de fechamento.
  - É um padrão de codificação exigir que a tag de fechamento seja omitida em arquivos incluídos, mas isso não é um requisito do PHP.

### Script Tag PHP

| Type | Open | Close | Note |
|--- |--- |--- |--- | 
| Standard | <?php | ?> | --- |
| Echo | <?= | ?> | --- |
| Short | <? | ?> | Deprecated |
| Script | <script language="php>  | </ script> | Do not use |
| Asp | <%  | %> | Deprecated |

### Echo tag
- A tag echo permite que use o valor de uma variável mais facilmente, facilitando leitura do html.
```php
/** Fazem a mesma coisa */
<?= $variable ?>
<?php echo $variable ?>
```

### Lógica de tags
- Lógica PHP entre abrir e fechar as tags,
```php
/** 
 * A tag PHP então verifica se o saldo é maior que zero e termina. A tag <p class = "black"> é produzida apenas se
 * condição é verdadeira; caso contrário, a tag <p class = "red"> é gerada. 
 */
<?php if ($bankBalance > 0): ?>
    <p class="black">
<?php else: ?>
    <p class="red">
<?php endif; ?>
    <?= $bankBalance?>
</p>
```

## Language Constructs (Construção da própria linguagem)

- Language Constructs podem ser entendidas diretamente pelo analisador
- Funções, por outro lado, são mapeadas e simplificadas para um conjunto de construções de linguagem antes de serem analisadas.
- Language Constructs não são funções e, portanto, não podem ser usadas como uma função de retorno de chamada.
- Eles seguem regras que são diferentes das funções no uso de parâmetros
  - Por exemplo: echo nem sempre precisa de parênteses não se pode usar parênteses
- Além disso, echo não retorna um valor, enquanto cada função sempre retornará um valor (ou nulo).

###Exemplo:
```php
<?php
/** one parameter, no brackets */
echo "hello\r\n";
/** two parameters, brackets (syntax error)
 * echo('hello', 'world');
 * two parameters, no brackets */
echo 'hello', 'world';
```

>[Lista completa de palavras chaves](https://www.php.net/manual/en/reserved.php)
###Algumas das mais usadas e explicação de uso:
- **assert**: Comando de depuração para testar uma condição.
- **echo**: Enviando um valor para stdout.
- **print**: Enviando um valor para stdout.
- **exit**: Opcional envio de uma mensagem e encerrar o programa.
- **die**: Este é um alias para sair.
- **return**: Termina uma função e retorna o controle ao escopo do invodador da função, ou se chamado no escopo global, 
termina o programa.
- **include**: Inclui um arquivo e o avalia. O PHP irá emitir warning se o arquivo não foi encontrado ou não pode ser lido.
- **include_once**:  o PHP irá certificar-se de que inclui o arquivo apenas uma vez.
- **require**: O PHP inclui um arquivo e o avalia. Se o arquivo não for encontrado ou não pode ser lido, então um erro 
fatal é gerado.
- **require_once**: Inclui um arquivo e o avalia, mas um erro fatal será gerado em vez de um aviso se arquivo não puder ser lido.
- **eval**: O argumento é avaliado como PHP e afeta o escopo da chamada.
- **empty**: Retorna um valor booleano dependendo se a variável está vazio ou não. 
  - Variáveis vazias incluem variáveis nulas, vazias strings, matrizes sem elementos, valores numéricos de 0, uma string
    valor de 0 e valores booleanos de falso.
- **isset**: Retorno booleano, se variável foi setada, true se variável setada e false caso contrário.
- **unset**: Limpa uma variável.
- **list**: É usada para criar uma lista de variáveis em apenas uma operação.

## Exame

> Diferença entre print e echo:
> - Echo não retorna valor nem mesmo null
> - Print retorna um valor
> 
> A razão de **não** usar include_onde() e require_once():
> - Problema de desempenho do PHP. 
>   Rastreiar uma lista de arquivos que foram incluídos para apoiar o  funcionalidade dessas funções. 
> -  Isso requer memória, então essas funções são bastante usadas quando eles são necessários e não a favor de incluir 
>    ou exigir.
> 
> 
## Copyrights

>Documentação criada e mantida por [Hagamenon Oliveira](https://github.com/haganicolau) - [haganicolau@gmail.com](https://mailto:haganicolau@gmail.com)