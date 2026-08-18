**LISTA DE EXERCÍCIO**

**EVOLUÇÃO DAS PRINCIPAIS LINGUAGENS DE PROGRAMAÇÃO**



**1.	Compare o Short Code, Speedcoding e o sistemas A-0/A-1/A-2 quanto ao problema enfrentado à estratégia adotada. Por que chama-los simplesmente de compiladores modernos seria impreciso?**



R: Os três sistemas buscavam diminuir a dificuldade de programar diretamente em código de máquina, mas utilizaram estratégias diferentes umas das outras.

No Short Code, consistia em uma representação simples para expressar as operações, porém era executada por um interpretador. Assim, não era traduzida previamente para o código de máquina, facilitando a programação, contudo, tornava a execução 50 vezes mais lenta que o código de máquina, segundo o Sabesta.

No Speedcoding, sendo desenvolvido por John Backus para o IBM 701, procurava entender a máquina com operações mais adequadas à computação cientifica, como operações de pontos flutuantes, raiz quadrada, seno e logaritmo. Fazendo com que o computador funcionasse como uma espécie de calculadora virtual de ponto flutuante.

Já no A-0/A-1/A-2, sendo desenvolvidas por uma equipe lidera por Grace Hopper na UNIVAC, entre 1951 e 1953, utilizavam os pseudocódigo que era expandido em subprogramas de código de máquina, de maneira semelhante à expansão de macros de Assembly.

Chamá-los de compiladores modernos atualmente seria impreciso pois seus mecanismos ainda eram primitivos, o Short Code e o Speedcoding eram de certo modo um sistema interpretativo, enquanto o A-0/A-1/A-2 faziam uma forma inicial de tradução por expansão de subprogramas. Elas representam etapas na evolução da programação automática, e não um compilador moderno no sentido atual.



**2.	Explique por que o projeto Fortran precisou convencer programadores de que código traduzido podia competir com código de máquina escrito à mão. Relacione desempenho, custo de programação e adoção.**



R: Muitos programadores acreditavam que um programa escrito manualmente em código máquina ou assembly seria necessariamente mais eficiente que um programa traduzido automaticamente.

Isso tornava o desempenho fundamental para a aceitação do Fortran. A linguagem precisava produzir código suficientemente eficiente para a facilidade de programação compensasse qualquer eventual perda de desempenho.

O ganho estava no custo de programação. Programar diretamente em código de máquina exigia muito esforço e conhecimento detalhado do computador. Com uma linguagem de alto nível e um compilador, o programador podia escrever programas de maneira muito mais produtiva.



Assim, a adoção de Fortran dependia de um equilíbrio: se o compilador produzisse código suficientemente eficiente, a enorme redução no esforço de programação compensaria a preferência tradicional pelo código escrito à mão. Sebesta destaca justamente a transição provocada pelo IBM 704, que possuía hardware para ponto flutuante e indexação, reduzindo a vantagem que os sistemas interpretativos tinham anteriormente.



**3.	Lisp surgiu em um contexto diferente de Fortran. Compare os domínios, a representação de dados e o estilo de computação favorecido pelas duas linguagens.**



R: Fortran e Lisp surgiram para necessidades bastante diferentes.

Fortran estava relacionado principalmente à computação científica, especialmente cálculos numéricos. Seu modelo favorecia operações matemáticas e processamento eficiente de números.

Lisp, por outro lado, surgiu no contexto da inteligência artificial e da computação simbólica. Seu elemento fundamental era a lista, e a linguagem favorecia a manipulação de símbolos e estruturas de dados simbólicas

Outra diferença importante está no paradigma: Sebesta apresenta Lisp como uma das primeiras linguagens de programação funcional. Nesse estilo, a computação é realizada principalmente pela aplicação de funções aos seus parâmetros.

Portanto:

Fortran → computação científica e numérica.

Lisp → computação simbólica e programação funcional.

Essa diferença mostra que linguagens podem evoluir em direções distintas porque são influenciadas pelos domínios de aplicação para os quais são desenvolvidas.



**4.	Avalie três contribuições de ALGOL 60 que ultrapassaram sua adoção comercial. Por que uma linguagem pode ser muito influente sem dominar o mercado?**



R: ALGOL 60 teve grande importância histórica mesmo sem alcançar grande sucesso comercial. Três de suas contribuições destacadas por Sebesta são:

1\. Estrutura de blocos: permitiu dividir o programa em partes com seus próprios ambientes de dados ou escopos. Isso influenciou fortemente linguagens posteriores.

2\. Recursão: ALGOL 60 permitia que procedimentos fossem recursivos. Sebesta observa que a recursão já existia em Lisp, mas foi uma novidade importante para as linguagens imperativas.

3\. BNF para descrição da sintaxe: a descrição formal de ALGOL 60 utilizou a Forma de Backus-Naur (BNF), que se tornou uma maneira extremamente importante de especificar formalmente a sintaxe das linguagens de programação.

ALGOL 60 mostra que influência não é a mesma coisa que sucesso comercial. Uma linguagem pode não dominar o mercado e ainda assim introduzir conceitos que serão incorporados por linguagens futuras.



**5.	COBOL foi desenhada para processamento comercial. Mostre como domínio e público influenciaram sua legibilidade, seus registros e sua relação com FLOW-MATIC.**



R: COBOL foi projetada especificamente para o processamento de registros comerciais. Por isso, seu projeto foi influenciado diretamente pelo domínio e pelo público que pretendia atingir.

Uma das metas do projeto era usar o inglês o máximo possível, tornar a linguagem fácil de usar e ampliar a base de usuários de computadores, mesmo que isso significasse sacrificar parte do poder da linguagem.

COBOL também precisava representar informações típicas de sistemas comerciais, como registros de funcionários, clientes, produtos e transações. Por isso, a descrição de dados e registros recebeu grande importância.

A relação com FLOW-MATIC foi direta. Sebesta destaca que COBOL foi baseada em FLOW-MATIC. Esta já utilizava nomes longos, palavras em inglês para operações, separação entre dados e código e sentenças iniciadas por verbos.

Assim, o domínio comercial e o público-alvo explicam por que COBOL privilegiou legibilidade, descrição de dados e proximidade com a linguagem natural.





**6.	Compare o papel dos objetos em Smalltalk, C++ e Java. Inclua na resposta o compromisso de C++ com C e a estratégia de portabilidade de Java.**



R: O Papel dos Objetos: Smalltalk, C++ e Java

Smalltalk: Considerada a linguagem puramente orientada a objetos (onde "tudo é um objeto", inclusive números e classes), popularizou a passagem de mensagens dinâmicas e o ambiente de desenvolvimento integrado (IDE).



C++: Desenvolvida por Bjarne Stroustrup para adicionar orientação a objetos ao C, mantendo o compromisso de compatibilidade com C ("zero-overhead principle"). Isso permitiu alto desempenho e adoção gradual, mas herdou complexidades e vulnerabilidades de gerenciamento de memória do C.



Java: Adotou uma orientação a objetos híbrida (com tipos primitivos por eficiência), mas eliminou o suporte a múltiplos heranças de implementação (usando interfaces) e ponteiros explícitos. Sua estratégia de portabilidade baseia-se na Máquina Virtual Java (JVM) e no bytecode intermediário ("Write Once, Run Anywhere").



**7. 	A primeira aplicação de Java não foi a Web, mas a Web impulsionou sua adoção. Explique como mudanças de contexto podem reposicionar uma linguagem.**



R: A primeira aplicação comercial e o projeto inicial de Java focavam em dispositivos eletrônicos de consumo interativos (set-top boxes). No entanto, o mercado para essa tecnologia não era maduro o suficiente na época.



Com a explosão da World Wide Web em meados dos anos 90, a equipe liderada por James Gosling percebeu que os applets de navegador e, posteriormente, a segurança e a portabilidade do lado do servidor (servlets/enterprise Java), encaixavam-se perfeitamente nas necessidades da internet. Essa mudança de contexto redirecionou o propósito original da linguagem para se tornar um padrão dominante no desenvolvimento Web corporativo.



**8.	C# foi apresentada como evolução no ambiente .NET. Compare duas decisões de C# com suas correspondentes em Java ou C++ e explique o problema que pretendem resolver.**



R: Propriedades Automáticas (get/set):

Problema resolvido: Em C++ e nas primeiras versões de Java, o encapsulamento exigia a criação manual de métodos getters e setters repetitivos (boilerplate code). O C# introduziu propriedades nativas na linguagem, mantendo a segurança do encapsulamento sem a verbosidade.



Delegais (Delegates) e Expressões Lambda Nativas:

Problema resolvido: Em C++, ponteiros para funções são complexos de declarar e propensos a erros de tipo. Em Java antigo, callbacks exigiam classes anônimas verbosas. O C# introduziu delegates seguros e suporte nativo à programação funcional, simplificando a manipulação de eventos e fluxos assíncronos.



**9.	Crie uma linha do tempo com oito linguagens de pelo menos quatro paradigmas. Para cada ligação, escreva o tipo de influência; não use apenas setas cronológicas.**



R: FORTRAN (Imperativa): Paradigma Procedural/Imperativo inicial para computação numérica.

Tipo de influência (Fundacional): Estabeleceu o conceito de variáveis, atribuição e estruturas de controle repetitivas baseadas no fluxo de hardware.



ALGOL 60 (Imperativa):

Tipo de influência (Estrutural e Sintática): Influenciou diretamente a sintaxe por blocos e o escopo léxico de quase todas as linguagens imperativas subsequentes.



Simula 67 (Orientada a Objetos):

Tipo de influência (Conceitual): Introduziu os conceitos fundamentais de classes, objetos e herança para simulações discretas, gerando a base para a OO moderna.



Smalltalk (Orientada a Objetos):

Tipo de influência (Refinamento de Paradigma): Consolidou a orientação a objetos pura baseada em mensagens e ambientes dinâmicos de desenvolvimento.



C (Imperativa / Sistemas): Influenciada pelo ALGOL/BCPL.

Tipo de influência (Eficiência de Baixo Nível): Forneceu o modelo de acesso direto à memória via ponteiros e tipagem fraca controlada.



C++ (Multiparadigma): Derivada diretamente de C e Simula 67.

Tipo de influência (Extensão de Paradigma): Proveu a fusão entre eficiência procedimental de baixo nível e abstração orientada a objetos baseada em classes.



Prolog (Declarativa / Lógica):

Tipo de influência (Inversão de Controle): Introduziu a computação baseada em resolução lógica e busca em árvore de inferência em vez de algoritmos procedimentais.



Haskell (Funcional Pura): Influenciada pelo cálculo lambda e Miranda.

Tipo de influência (Imutabilidade e Segurança de Tipos): Consolidou a avaliação preguiçosa (lazy evaluation) e tipagem estática avançada com inferência de tipos.



**10.	Estudo de caso: uma equipe precisa escolher tecnologias para cálculo científico, regras declarativas, aplicação Web interativa e firmware restrito. Proponha famílias de linguagens, justifique historicamente cada escolha e explicite dois trade-offs.**



R: Proposta de Famílias de Linguagens:

Cálculo Científico: Python (com bibliotecas otimizadas em C/Fortran como NumPy) ou Fortran / C++.

Regras Declarativas: Prolog ou motores de regras baseados em lógica de predicados.

Aplicação Web Interativa: JavaScript / TypeScript (Ecossistema Node.js / React).

Firmware Restrito: C ou Rust.



Justificativa Histórica:

Cálculo Científico (C++ / Python): O Fortran inaugurou o cálculo numérico de alta performance, mas o C++ modernizou a abstração sem perda de velocidade. Python integrou-se perfeitamente a esse ecossistema devido à facilidade de encapsular rotinas numéricas de baixo nível.



Firmware Restrito (C): Herdeiro direto da necessidade de criar sistemas operacionais eficientes (Unix), o C oferece controle total de hardware e consumo mínimo de recursos, essencial para microcontroladores.



Dois Trade-offs Principais:

Desempenho vs. Produtividade: Escolher Python/JavaScript acelera o desenvolvimento de aplicações web e científicas, mas sacrifica o controle estrito de memória e o desempenho em tempo de execução comparado a C/C++.



Segurança de Baixo Nível vs. Flexibilidade: O uso de C em firmware garante acesso irrestrito ao hardware com overhead mínimo, mas abre margem para falhas críticas de segurança relacionadas a ponteiros e vazamentos de memória que linguagens modernas (como Rust) tentam mitigar.

