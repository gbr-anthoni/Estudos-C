
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



<h2 align="center">📘 A HISTÓRIA DE C:</h2>

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

> [!TIP]
> Usar funções da biblioteca-padrão de C em vez de escrever suas próprias versões equivalentes pode melhorar
>  o desempenho do programa, porque essas funções foram cuidadosamente escritas para serem executadas de modo eficaz.



<!---------------------------------------------------------------------------------------PART2--------------------------------------------------------------------------------------->



<h2 align="center">💾 INTRODUÇÃO À PROGRAMAÇÃO EM C</h2>

A linguagem C permite uma **programação estruturada e organizada**. Neste capítulo, serão apresentados exemplos
que ilustram suas principais **características**, acompanhados de análises para facilitar o entendimento.

<h3 align="center">Estrutura básica C:</h3>

**`Hello, World!` em C:**
```c
#include <stdio.h>
int main(void) {
   printf("Hello, World!\n");
   return 0;
}
```
Estrutura básica para imprimir a mensagem: `Hello, World!` na tela.

**passo a passo:**

```c
#include <stdio.h>
```
- Linhas que começam com `#` são chamadas de **diretivas** do pré-processador. Elas são processadas antes da compilação do programa.
- A diretiva `#include <stdio.h>` instrui o pré-processador a incluir o **conteúdo do cabeçalho de entrada/saída padrão** no programa. Esse cabeçalho contém informações necessárias para o uso de **funções** como `printf()` e `scanf()` da biblioteca padrão.

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

<h3 align="center">Variáveis em C:</h3>

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

<h3 align="center">Entradas de dados em C:</h3>

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
