Atividade: Derivação de um Código a partir da Gramática de uma Linguagem de Programação

**1. Linguagem escolhida e fonte da gramática**
Consultando as bases da internet, acabou-se por escolher o Python para a resolução desse trabalho. A gramática sendo consultada nas documentações oficiais da linguaguem Python, especificamente na seção Full Grammar Specification, disponível no site oficial da Python Software Foundation.
Fonte: https://docs.python.org/3/reference/grammar.html
A gramática oficial do Python utiliza uma notação baseada em PEG (Parsing Expression Grammar). Ela descreve as regras utilizadas pelo analisador sintático do Python para reconhecer a estrutura dos programas escritos na linguagem.

**2. Produções selecionadas**
O código escolhido para a derivação será:
resultado = 2 + 3

file: [statements] ENDMARKER

statements: statement+

statement:
    | compound_stmt
    | simple_stmts

simple_stmts:
    | simple_stmt !';' NEWLINE
    | ';'.simple_stmt+ [';'] NEWLINE

simple_stmt:
    | assignment

assignment:
    | (star_targets '=')+ annotated_rhs !'=' [TYPE_COMMENT]

annotated_rhs:
    | star_expressions

star_expressions:
    | star_expression

star_expression:
    | expression

expression:
    | disjunction

disjunction:
    | conjunction

conjunction:
    | inversion

inversion:
    | comparison

comparison:
    | bitwise_or

bitwise_or:
    | bitwise_xor

bitwise_xor:
    | bitwise_and

bitwise_and:
    | shift_expr

shift_expr:
    | sum

sum:
    | sum '+' term
    | term

term:
    | factor

factor:
    | power

power:
    | await_primary

await_primary:
    | primary

primary:
    | atom

atom:
    | NAME
    | NUMBER

Essas regras permitem representar uma instrução de atribuição e uma expressão matemática de adição.

A regra file representa o programa ou entrada completa. A regra statements representa uma ou mais instruções. A regra simple_stmt permite representar uma instrução simples, como uma atribuição. A regra assignment representa a atribuição de um valor a uma variável.

Para representar a expressão 2 + 3, são utilizadas principalmente as regras sum, term, factor, power, primary e atom. A regra sum permite representar uma soma utilizando o operador +.

**3. Código que será derivado**
O código escolhido é:
resultado = 2 + 3

Esse código possui uma atribuição. A variável resultado recebe o valor da expressão 2 + 3.
Matematicamente, essa expressão resulta em 5, mas o objetivo da atividade é analisar a estrutura sintática do código, e não seu resultado matemático.

**4. Derivação passo a passo**
A derivação começa pelo símbolo inicial file.

Primeiramente:

file
⇒ statements ENDMARKER

A partir de statements, podemos gerar uma instrução:

⇒ statement ENDMARKER

A instrução pode ser uma instrução simples:

⇒ simple_stmts ENDMARKER

Aplicando a regra de simple_stmts:

⇒ simple_stmt NEWLINE ENDMARKER

Agora utilizamos a regra que permite uma atribuição:

⇒ assignment NEWLINE ENDMARKER

A regra de atribuição pode ser representada como:

⇒ star_targets '=' annotated_rhs NEWLINE ENDMARKER

O lado esquerdo da atribuição será a variável resultado:

⇒ NAME '=' annotated_rhs NEWLINE ENDMARKER

Substituindo NAME pelo identificador escolhido:

⇒ resultado '=' annotated_rhs NEWLINE ENDMARKER

Agora precisamos gerar a expressão que ficará do lado direito do sinal de igualdade.

Aplicando as regras:

annotated_rhs
⇒ star_expressions
⇒ star_expression
⇒ expression
⇒ disjunction
⇒ conjunction
⇒ inversion
⇒ comparison
⇒ bitwise_or
⇒ bitwise_xor
⇒ bitwise_and
⇒ shift_expr
⇒ sum

Assim, chegamos a:

resultado '=' sum NEWLINE ENDMARKER

Para representar a soma 2 + 3, utilizamos a produção:

sum → sum '+' term

Então:

resultado '=' sum '+' term NEWLINE ENDMARKER

O primeiro sum pode ser reduzido para term:

resultado '=' term '+' term NEWLINE ENDMARKER

Cada term pode ser reduzido para factor:

resultado '=' factor '+' factor NEWLINE ENDMARKER

Depois:

resultado '=' power '+' power NEWLINE ENDMARKER

Depois:

resultado '=' await_primary '+' await_primary NEWLINE ENDMARKER

Depois:

resultado '=' primary '+' primary NEWLINE ENDMARKER

Depois:

resultado '=' atom '+' atom NEWLINE ENDMARKER

A regra atom permite gerar um NUMBER:

resultado '=' NUMBER '+' NUMBER NEWLINE ENDMARKER

Escolhendo os números 2 e 3:

resultado '=' 2 '+' 3 NEWLINE ENDMARKER

Retirando os elementos utilizados internamente pela gramática, chegamos ao código:

resultado = 2 + 3

Portanto, a derivação completa pode ser resumida da seguinte maneira:

file
⇒ statements ENDMARKER
⇒ statement ENDMARKER
⇒ simple_stmts ENDMARKER
⇒ simple_stmt NEWLINE ENDMARKER
⇒ assignment NEWLINE ENDMARKER
⇒ star_targets '=' annotated_rhs NEWLINE ENDMARKER
⇒ NAME '=' annotated_rhs NEWLINE ENDMARKER
⇒ resultado '=' star_expressions NEWLINE ENDMARKER
⇒ resultado '=' expression NEWLINE ENDMARKER
⇒ resultado '=' disjunction NEWLINE ENDMARKER
⇒ resultado '=' conjunction NEWLINE ENDMARKER
⇒ resultado '=' inversion NEWLINE ENDMARKER
⇒ resultado '=' comparison NEWLINE ENDMARKER
⇒ resultado '=' bitwise_or NEWLINE ENDMARKER
⇒ resultado '=' bitwise_xor NEWLINE ENDMARKER
⇒ resultado '=' bitwise_and NEWLINE ENDMARKER
⇒ resultado '=' shift_expr NEWLINE ENDMARKER
⇒ resultado '=' sum NEWLINE ENDMARKER
⇒ resultado '=' sum '+' term NEWLINE ENDMARKER
⇒ resultado '=' term '+' term NEWLINE ENDMARKER
⇒ resultado '=' factor '+' factor NEWLINE ENDMARKER
⇒ resultado '=' power '+' power NEWLINE ENDMARKER
⇒ resultado '=' await_primary '+' await_primary NEWLINE ENDMARKER
⇒ resultado '=' primary '+' primary NEWLINE ENDMARKER
⇒ resultado '=' atom '+' atom NEWLINE ENDMARKER
⇒ resultado '=' NUMBER '+' NUMBER NEWLINE ENDMARKER
⇒ resultado = 2 + 3

**5. Símbolos terminais e não terminais**
Os símbolos não terminais são aqueles que podem ser substituídos por outras regras da gramática. Alguns dos principais não terminais utilizados nesta derivação são:

file
statements
statement
simple_stmts
simple_stmt
assignment
star_targets
annotated_rhs
star_expressions
star_expression
expression
disjunction
conjunction
inversion
comparison
bitwise_or
bitwise_xor
bitwise_and
shift_expr
sum
term
factor
power
await_primary
primary
atom
Os símbolos terminais são aqueles que aparecem na sequência final do código ou representam tokens reconhecidos pelo analisador léxico. Neste exemplo, temos:

resultado, que é reconhecido como NAME;
=, que representa o operador de atribuição;
2, que é um NUMBER;
+, que representa o operador de soma;
3, que é um NUMBER;
NEWLINE, que representa o final da linha;
ENDMARKER, que representa o final da entrada.

**6. Resultado final**
O resultado da derivação é o seguinte código Python:

resultado = 2 + 3

A derivação mostra como um código simples pode ser construído a partir de regras de uma gramática formal. O processo começa pelo símbolo inicial file e, por meio de sucessivas aplicações das produções, chega aos elementos que formam a instrução de atribuição.

A variável resultado é representada por um NAME, enquanto os valores 2 e 3 são representados por NUMBER. O operador = representa a atribuição e o operador + representa a soma. A regra sum é especialmente importante porque permite formar uma expressão utilizando o operador de adição.

Dessa forma, é possível perceber a relação entre os conceitos de gramáticas formais, símbolos terminais, símbolos não terminais, produções e derivação e uma linguagem de programação real. A gramática formal define como os elementos da linguagem podem ser organizados para formar construções sintaticamente válidas.

**7. Referência**
PYTHON SOFTWARE FOUNDATION. Full Grammar specification. Python Documentation. Disponível em: https://docs.python.org/3/reference/grammar.html. Acesso em: 25 ago. 2026.