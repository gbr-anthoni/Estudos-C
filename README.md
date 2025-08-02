
<!---------------------------------------------------------------------------------------HEADER--------------------------------------------------------------------------------------->


<p align="center">
   <img src="https://devicons.railway.com/i/c.svg" width="100">
</p>

<div align="center">
   <img src="https://capsule-render.vercel.app/api?type=cylinder&height=35&color=387db8&text=Linguagem%20C&fontSize=25&fontColor=FFFFFF&fontAlignY=53">
</div>

```c
#include <stdio.h>
int main() {
   printf("Hello, World!\n");
   return 0;
}
```

<!---------------------------------------------------------------------------------------PART1--------------------------------------------------------------------------------------->



<h2 align="center">📘 A HISTÓRIA DE C</h2>

A linguagem C evoluiu a partir das linguagens **BCPL** e **B**.**BCPL**, criada em **1967 por Martin Richards**,
foi projetada para desenvolver sistemas operacionais e compiladores.A linguagem B, desenvolvida por **Ken Thompson
em 1970**, baseou-se em BCPL e foi usada nas primeiras versões do UNIX.Ambas eram linguagens "*sem tipo*", nas quais
todos os dados ocupavam uma "*palavra*" na memória , e era bastante trabalhoso tratar um dado como número inteiro ou real.

Já em **1972 A linguagem C foi criada por Dennis Ritchie** no Bell Laboratories, baseada na linguagem B.Ela **incorporou
conceitos de BCPL e B**, adicionando **tipos de dados** e outros recursos poderosos.C ficou conhecida como a linguagem
usada no desenvolvimento do sistema UNIX. Atualmente,é amplamente usada e disponível para diversos sistemas e plataformas,
sendo considerada uma linguagem **portátil** e **independente de hardware**.

No final dos anos **1970**, C evoluiu para o que ficou conhecido como "*C tradicional*".A publicação do livro "*The C
Programming Language*", de **Kernighan e Ritchie, em 1978**, popularizou a linguagem e contribuiu para seu sucesso.
A obra se tornou um dos livros mais influentes da ciência da computação.

A rápida expansão da linguagem C para diversos tipos de computadores — ou **plataformas de hardware** —levou ao surgimento
de muitas **variações da linguagem** que, embora semelhantes, eram frequentemente **incompatíveis entre si**.Isso representava
um problema sério para os programadores que precisavam desenvolver programas portáveis, capazes de ser executados em diferentes sistemas.

Diante dessa necessidade, ficou claro que era fundamental estabelecer uma versão padronizada de C. Em **1983**, 
foi criado o comitê técnico **X3J11**, vinculado ao *American National Standards Committee on Computers and Information
Processing* (X3), com o objetivo de produzir uma **definição precisa da linguagem**, não **ambígua** e **independente de máquina**.

O resultado foi a aprovação do primeiro padrão oficial da linguagem em **1989**, conhecido como *ANSI C* (ou C89).
Esse padrão foi posteriormente revisado e atualizado em **1999**, dando origem ao **C99**.

<h3 align="center">Bibliotecas C</h3>

Como veremos mais adiante, C possui diversas **bibliotecas padrão** com **funções muito úteis**. Ao aprender a 
programar em C, é possível dividir o processo em **duas fases**. A primeira consiste em **dominar a linguagem C
em si** — sua sintaxe, tipos de dados, estruturas de controle, operadores e funções. A segunda fase envolve 
**aprender a utilizar a biblioteca padrão da linguagem**, que oferece um conjunto essencial de funções prontas realizar certas tarefas.

**Algumas bibliotecas em C:**

| Biblioteca   | Descrição                                                    |
| ------------ | -------------------------------------------------------------|
| `stdio.h`    | **Entrada e saída** (*ex: `printf()`, `scanf()`, `fgets()`*) |
| `math.h`     | **Funções matemáticas** (*ex: `sqrt()`, `pow()`, `sin()`*)   |

> [!TIP]
> Usar funções da biblioteca-padrão de C em vez de escrever suas próprias versões equivalentes pode melhorar
>  o desempenho do programa, porque essas funções foram cuidadosamente escritas para serem executadas de modo eficaz.



<!---------------------------------------------------------------------------------------PART2--------------------------------------------------------------------------------------->



<h2 align="center">💾 INTRODUÇÃO À PROGRAMAÇÃO EM C</h2>

A linguagem C permite uma **programação estruturada e organizada**. Neste capítulo, serão apresentados exemplos
que ilustram suas principais **características**, acompanhados de análises para facilitar o entendimento.

<h3 align="center">Estrutura básica C</h3>

**`Hello, World!` em C:**
```c
#include <stdio.h>
int main(void) {
   printf("Hello, World!\n");
   return 0;
}
```

**Saída:**
```
Hello, World!
```

Estrutura básica para imprimir a mensagem: `Hello, World!` na tela.

**passo a passo:**

```c
#include <stdio.h>
```
- Linhas que começam com `#` são chamadas de **diretivas** do pré-processador. Elas são processadas antes da compilação do programa.
- A diretiva `#include <stdio.h>` instrui o pré-processador a incluir o **conteúdo do cabeçalho/biblioteca de entrada e saída padrão** no programa. Esse cabeçalho contém informações necessárias para o uso de **funções** como `printf()` e `scanf()` da biblioteca padrão.

```c
int main(void) { ... }
```
- `main` é uma **função**, ou seja, um **bloco de construção** de programa.
  - Todo programa em C começa sua **execução pela função** `main`.
- A **palavra-chave** `int` à esquerda de `main` indica que essa função retorna um **valor inteiro**.
- A **palavra-chave** `void` indica que a função não recebe nenhum argumento.
- As chaves `{ ... }` delimitam o **corpo da função:**
  - `{` marca o início do bloco de código.
  - `}` indica o fim do bloco.


```c
printf("Hello, World!\n");
```
- A função `printf()` instrui o computador a **imprimir uma mensagem na tela.**
- A linha completa — `printf("Hello, World!\n");` — é chamada de uma **instrução** (*ou comando*).
- Toda instrução em C deve terminar com um ponto e vírgula `;`, que é chamado de **terminador de instrução**.

A barra invertida `\` é chamada de **caractere de escape**. Ela indica que a função printf deve executar uma **ação especial**, diferente de imprimir um caractere comum.
Quando o compilador encontra uma barra invertida dentro de uma string, ele combina ela com o **próximo caractere** para formar uma sequência de escape.
Por exemplo, a sequência `\n` representa uma **nova linha (*newline*)**, ou seja, faz o cursor pular para o início da linha seguinte na saída.

```c
return 0;
```
- A instrução `return` em C é usada para encerrar a execução de uma função e retornar um valor para o ponto onde a função foi chamada.
- No caso da função `main`, o comando `return 0;` indica que o programa terminou com sucesso.

<h3 align="center">Variáveis em C</h3>

Uma variável é um **espaço nomeado na memória** do computador usado para **armazenar dados** que podem ser usados durante a execução do programa.

**Estrutura de variáveis C:**
Uma variável precisa ser **declarada antes de ser usada**. A declaração especifica o **tipo** e o **nome** da variável.
```c
[tipo] [nome];
```
**Tipos de variáveis C:**
| Tipo         | Descrição                          | Valor guardado                                             | Especificador |
| ------------ | ---------------------------------- | ---------------------------------------------------------- | --------------|
| `int`        | Número Inteiro                     | `0`, `3456`, `-23`                                         | `%d` e `%i`   |
| `float`      | Número decimal (menos preciso)     | `3.14`, `0.45`, `-4.5`                                     | `%f`          |
| `double`     | Número decimal (mais preciso)      | `3.1415`, `-0.00001`, `42.0`                               | `%lf`         |
| `char`       | Um caractere (entre aspas simples) | `'a'`, `'Z'`, `'1'`, `'#'`                                 | `%c`          |

**Nomes de variáveis C:**

Um nome de variável é como você chama uma variável no seu programa. Ele deve seguir algumas regras e boas práticas.

1. **Podem conter:**
  - Letras minúsculas (a-z)
  - Letras maiúsculas (A-Z)
  - Dígitos (0-9)
  - Underscore (_)
2. **Não podem começar com um número:**
  - ✅ `numero1`
  - ❌ `1numero` (*inválido*)
3. **Não podem conter espaços ou símbolos especiais:**
  - ✅ `nota_final`,`salario`,`nome`
  - ❌ `nota final`,`salário$`,`@nome` (*inválidos*)
4. **Não podem ser palavras reservadas da linguagem C:**
  - ❌ `int`, `return`, `while`, `if`, etc... (*inválidos*)

**Atribuir dado a variável em C:**

A atribuição em C é o processo de dar um valor a uma variável usando o operador de atribuição `=`.

**atribuição direta:**
```c
int idade = 18;
```
Aqui, a variável idade é declarada e recebe o valor 18 no mesmo momento.

**atribuição separada:**
```c
int idade;
idade = 18;
```
Primeiro a variável é criada, depois recebe o valor.

<h3 align="center">Entradas de dados em C</h3>

**Entradas de dados** em C são os valores fornecidos pelo usuário durante a execução do programa, normalmente **digitados pelo teclado**. Esses dados são **armazenados em variáveis** para serem usados no programa.

**Exemplo simples:**

```c
#include <stdio.h>
int main(void) {
   int idade;

   printf("Digite sua idade: ");
   scanf("%d", &idade);

   printf("Você tem %d anos.\n", idade);
   return 0;
}
```
Estrutura básica para imprimir a mensagem: `Você tem _ anos.` no qual `_` será o valor colocado pelo usuário na variável `idade`.

```c
scanf("%d", &idade);
```
A função `scanf()`, pertencente à biblioteca `stdio.h`, lê um dado fornecido pelo usuário por meio da **entrada padrão** (*normalmente, o teclado*).

<h3 align="center">Operações aritméticas em C</h3>

A linguagem C permite a execução de **operações matemáticas** que manipulam e processam **valores numéricos com precisão**.

**Operações em C:**

| Operação        | Símbolo | Exemplo | Resultado |
| --------------- | ------- | ------- | --------- |
| Adição          | `+`     | `5 + 3` | `8`       |
| Subtração       | `-`     | `5 - 3` | `2`       |
| Multiplicação   | `*`     | `5 * 3` | `15`      |
| Divisão inteira | `/`     | `5 / 2` | `2`       |
| Módulo (resto)  | `%`     | `5 % 2` | `1`       |

> [!IMPORTANT]
> Quando você escreve uma expressão com vários operadores, a linguagem segue uma ordem de prioridade para decidir qual operação será feita primeiro, assim como na matemática.
```c
int conta1 = 5 + 2 * 3; // 11
int conta2 = ( 5 + 2 ) * 3; // 21
```
- Variável `conta1`: `2 * 3 = 6` ⮕ `6 + 5 = 11`.

- Variável `conta2`: `5 + 2 = 7` ⮕ `7 * 3 = 21`.

**Tabela prioridade:**

| Prioridade | Operadores    | Descrição                              |
| ---------- | ------------- | -------------------------------------- |
| **1**      | `()`          | Parênteses: forçam a ordem da operação |
| **2**      | `*`, `/`, `%` | Multiplicação, Divisão, Módulo         |
| **3**      | `+`, `-`      | Soma e Subtração                       |

**operadores de atribuição:**

Esses operadores são atalhos para fazer uma operação aritmética e já **armazenar o resultado na própria variável**.

```c
int a = 5;
a += 5; // 10
```
- `a += 5;` é o mesmo que: `a = a += 5;`

**Tabela dos operadores de atribuição:**

| Operador | Significado                       | Exemplo                |
| -------- | --------------------------------- | ---------------------- |
| `+=`     | Soma e atribui                    | `a += 3;`              |
| `-=`     | Subtrai e atribui                 | `a -= 2;`              | 
| `*=`     | Multiplica e atribui              | `a *= 4;`              |
| `/=`     | Divide e atribui                  | `a /= 2;`              |  
| `%=`     | Módulo (resto) e atribui          | `a %= 3;`              | 

**Operadores de incremento e decremento:**

Estes operadores são usados para **aumentar** `++` ou **diminuir** `--` o valor de uma variável em 1 — de forma simples e rápida.

```c
int numero = 3;
++numero // 4
```

**Tabela operadores de incremento e decremento:**

| Operador | Expressão | Descrição                                       |
| -------- | --------- | ----------------------------------------------- |
| `++`     | `i++`     | Incrementa `i` em 1, e então usa o novo valor   |
| `++`     | `++i`     | Usa o valor de `i`, e então incrementa `i` em 1 |
| `--`     | `i--`     | Decrementa `i` em 1, e então usa o novo valor   |
| `--`     | `--i`     | Usa o valor de `i`, e então decrementa `i` em 1 |

**Biblioteca `math.h`:**

A biblioteca `math.h` é usada para realizar **operações matemáticas avançadas** em C.

```c
int conta = pow(5, 3); // 125
```
- `pow(5, 3)` é o mesmo que: `5³`

**Principais funções de `math.h`:**

| Função       | Descrição                | Exemplo          | Resultado   |
| ------------ | ------------------------ | ---------------- | ----------- |
| `sqrt(x)`    | Raiz quadrada            | `sqrt(25)`       | `5.0`       |
| `pow(x,y)`   | Potência (x elevado a y) | `pow(2,3)`       | `8.0`       |
| `fmod(x, y)` | Resto da divisão (float) | `fmod(7.3, 2.0)` | `1.3`       |
| `ceil(x)`    | Arredonda para cima      | `ceil(2.3)`      | `3.0`       |
| `floor(x)`   | Arredonda para baixo     | `floor(2.9)`     | `3.0`       |

<h3 align="center">Operações e estruturas condicionais em C</h3>

**Operações condicionais em C**, que são usadas para tomar decisões no código, dependendo de uma condição ser **verdadeira** ou **falsa**.

**Operadores relacionais e de igualdade:**

Estes operadores são usados para **comparar valores** em C e retornam um resultado:

```c
int condicao2 = 5 != 5; // 0
int condicao1 = 5 == 5; // 1
```

`0` - para falso.

`1` - para verdadeiro.

**Tabela de operadores relacionais e de igualdade:**

| Operadores de igualdade    | Significado      | Exemplo  | Resultado se                  |
| -------------------------- | ---------------- | -------- | ----------------------------- |
| `==`                       | Igual a          | `5 == 7` | `0` (*falso*)                 |
| `!=`                       | Diferente de     | `5 != 5` | `1` (*verdadeiro*)            |
| **Operadores relacionais** |                  |          |                               |
| `>`                        | Maior que        | `7 > 5`  | `1`                           |
| `<`                        | Menor que        | `7 < 5`  | `0`                           |
| `>=`                       | Maior ou igual a | `5 >= 5` | `1`                           |
| `<=`                       | Menor ou igual a | `7 <= 5` | `0`                           |

**Operadores lógicos:**

Operadores lógicos permitem combinar ou inverter condições.

```c
int condicao1 = (5 == 5 && 5 > 5); // 0
int condicao2 = (5 == 5 || 5 > 5); // 1
```

**Tabelas de operadores lógicos:**

<table>
   <tr>
      <th>Operador</th>
      <th>Descrição</th>
      <th>Lógica</th>
   </tr>
   <tr>
      <td><code>&&</code> <i>And/E</i></td>
      <td>Analisa se <strong>ambas as condições são verdadeiras.</strong></td>
      <td>
         <table>
            <tr><th>A</th><th>B</th><th>R</th></tr>
            <tr><td>1</td><td>1</td><td>1</td></tr>
            <tr><td>0</td><td>1</td><td>0</td></tr>
            <tr><td>1</td><td>0</td><td>0</td></tr>
            <tr><td>0</td><td>0</td><td>0</td></tr>
         </table>
      </td>
   </tr>
   <tr>
      <td><code>||</code> <i>Or/Ou</i></td>
      <td>Analisa se <strong>uma as condições é verdadeira.</strong></td>
      <td>
         <table>
            <tr><th>A</th><th>B</th><th>R</th></tr>
            <tr><td>1</td><td>1</td><td>1</td></tr>
            <tr><td>0</td><td>1</td><td>1</td></tr>
            <tr><td>1</td><td>0</td><td>1</td></tr>
            <tr><td>0</td><td>0</td><td>0</td></tr>
         </table>
      </td>
   </tr>
   <tr>
      <td><code>!</code> <i>Not/Não</i></td>
      <td>Analisa se <strong>a condição é falsa.</strong></td>
      <td>
         <table align="center">
            <tr><th>A</th><th>R</th></tr>
            <tr><td>0</td><td>1</td></tr>
            <tr><td>1</td><td>0</td></tr>
         </table>
      </td>
   </tr>
   
</table>

**Estruturas condicionais em C:**

São comandos que permitem ao programa verificar se uma condição é **verdadeira** ou **falsa** e, com base nisso, **executar diferentes instruções**.

**Exemplo simples:**

```c
if ( condição ) {
   // bloco de código
} else if ( outra condição ) {
   // bloco de código
} else {
   // bloco de código
}
```

- `if` – condição primária que é executada se for **verdadeira**.
- `else if` – condições alternativas, avaliadas se o `if` for **falso**.
- `else` – executado caso nenhuma das condições anteriores seja **verdadeira**.

<h3 align="center">Estruturas de repetição em C</h3>

As **estruturas de repetição** em C são usadas quando você precisa executar um **bloco de código várias vezes**, de forma **controlada** ou até que uma **condição seja satisfeita**.

```c
while (condição) {
    // Bloco de código
}
```
`while` exeulta um bloco de código até a condição dele seja **falsa**.

> [!WARNING]
>  Cuidado para não criar um **loop infinito!** ( *Garanta que a condição do while possa se tornar falsa* ).

```c
do {
    // Bloco de código
} while (condição);
```

`do...while` é uma **estrutura de repetição** parecida com o `while`, mas com uma **diferença importante:** O bloco de código é executado pelo menos uma vez, mesmo que a condição seja **falsa** logo no início.

**Diferença entre `while` e `do...while`:**

| Característica        | `while`                         | `do...while`                      |
| --------------------- | ------------------------------- | --------------------------------- |
| Avaliação da condição | **Antes** de executar o bloco   | **Depois** de executar o bloco    |
| Execução garantida?   | Só se a condição for verdadeira | Sempre **executa ao menos 1 vez** |

```c
for (inicialização; condição; incremento) {
    // Bloco de código
}
```

A função `for` é usada para executar um bloco de **código várias vezes**, geralmente quando se **sabe quantas vezes o código deve ser repetido**.

- `iniciaçização` ⮕ É feita quando uma **variável de controle** (um "*contador*") é declarada e inicializada com algum valor.
- `condição` ⮕ É a **condição lógica** que será verificada antes de cada repetição. Se for **verdadeira**, o loop continua; se for **falsa**, o loop termina.
- `incremento` ⮕  É a **modificação da variável de controle** após cada repetição.Normalmente, serve para aproximar a condição de ser **falsa**, encerrando o loop.

**Comandos `break` e `continue`:**

- O `break` serve para encerrar um loop, para sair dele mesmo que a condição seja verdadeira.
```c
#include <stdio.h>
int main(){
   int i = 5;
   while( i > 0 ){
      printf("i = %d\n",i);
      i--;
      if ( i == 2 ){
         break;
      }
   }
   return 0;
}
```

**Saída:**
```
i = 5
i = 4
i = 3
```

Mesmo que a condição do `while` (`i > 0`) ainda seja **verdadeira**, o `break` força a saída imediata do laço.

**Tabela de execução:**
| Repetição     | Valor de `i` (antes do `printf`) | Valor de `i` após `i--` | `i == 2`?   | Condição `i > 0` na próxima iteração |
| --------------| -------------------------------- | ----------------------- | ----------- | ------------------------------------ |
| **1**         | 5                                | 4                       | `0` *False* | Sim                                  |
| **2**         | 4                                | 3                       | `0` *False* | Sim                                  |
| **3**         | 3                                | 2                       | `1` *True*  | Não (*break*)                        |


- O `continue` pula o restante do corpo do laço atual e vai **direto para a próxima iteração**, sem **sair do laço**.

```c
#include <stdio.h>
int main(){
   int i = 5;
   while( i > 0 ){
      i--;
      if ( i == 2 ){
         continue;
      }
      printf("i = %d\n",i);
   }
   return 0;
}
```

**Saída:**
```
i = 4
i = 3
i = 1
i = 0
```

O `continue` pula para a **próxima iteração**, por isso o valor `2` não é exibido.


**Tabela de execução:**
| Repetição | `i` antes do `i--` | `i` após `i--` | `i == 2`?   | `printf` é executado? | Condição `i > 0` na próxima iteração |
| --------- | ------------------ | -------------- | ----------- | --------------------- | ------------------------------------ |
| **1**     | 5                  | 4              | `0` *false* | Sim (`i = 4`)         | Sim                                  |
| **2**     | 4                  | 3              | `0` *false* | Sim (`i = 3`)         | Sim                                  |
| **3**     | 3                  | 2              | `1` *True*  | Não (*pulado*)        | Sim                                  |
| **4**     | 2                  | 1              | `0` *false* | Sim (`i = 1`)         | Sim                                  |
| **5**     | 1                  | 0              | `0` *false* | Sim (`i = 0`)         | Não (*laço termina*)                 |

<h3 align="center">Pré-processador em C</h3>

O **pré-processador** é uma parte do compilador C que **executa tarefas no código-fonte antes da compilação começar**. Ele é responsável por preparar o código, **processando diretivas especiais que começam com o caractere** `#`.

**`#include` – Inclusão de arquivos**

```c
#include <arquivo>
#include "arquivo"
```
- `<arquivo>`: O compilador procura o arquivo nas **pastas padrão do sistema** (*diretórios de bibliotecas do compilador*).
- `"arquivo"`: Usado para incluir **arquivos criados por você**, geralmente no **mesmo diretório do projeto**.

**`#define` – Definição de constantes e macros**

```c
#define PI 3.1415
float valor = PI;
```
- O pré-processador **substitui** `PI` por `3.1415` **antes de compilar**.

**`#undef` – Desfaz uma definição**

```c
#undef PI
```
- Se você quiser "*apagar*" a definição anterior de `PI`.

**`#if`,`#elif`,`#else` — Condições com valores lógicos / `#endif` — Finaliza um bloco condicional**

```c
#define VERSAO 3

#if   VERSAO == 1
    // Versão
#elif VERSAO == 2
    // Versão
#else
    // Outra versão
#endif
```
- `#if`
  - Verifica se `VERSAO` é **igual** a `1`.
- `#elif`
  - Verifica se `VERSAO` é **igual** a `2`.
  - Só será testado se o `#if` acima for **falso**.
- `#else`
  - Executado se **nenhuma condição acima foi verdadeira**.
- `#endif`
  - **Fecha o bloco condicional** iniciado com `#if`.

