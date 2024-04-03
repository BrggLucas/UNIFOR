# UNIFOR
**Nome**: Lucas Gabriel Brigagão <br>
**Disciplina**: Raciocínio lógico algorítm

## Exercício exemplo
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular o adicional de salário de funcionário por cargo de uma empresa fictícia. Sabe-se que os funcionários de cargo técnico receberão reajuste de 50%, cargo de gerência, um reajuste de 30% e demais, um reajuste de 10%. 

#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o salário e profissão}}
B --> C[\sal, prof\]
C --> D{prof == 'Tecnico'}
D --FALSE--> E{prof == 'Gerente'}
D --TRUE--> F[sal_reaj = 1.5 * sal]
E --FALSE--> H[sal_reaj = 1.1 * sal]
E --TRUE--> G[sal_reaj = 1.3 * sal]
G --> I([FIM])
F --> I
H --> J{{'Salário Reajustado = ', sal_reaj}}
J --> I
```

#### Pseudocódigo
```java
ALGORITMO calReajuste
DECLARE  sal, sal_reaj: real, prof: caractere

INICIO
	// Exibe a mensagem para receber os dados "sal" e "prof"
	ESCREVA "Digite sua profissão e o salário que você recebe"

    // Armazena o número escrito como "sal" e a profissão como "prof"
    LEIA sal, prof

    // Verifica a variável "prof"
    ESCOLHA

        // Executa a condição se "prof" for igual a técnico e realiza o cálculo
        CASO prof == “Técnico”		
            sal_reaj ← 1.5 * sal

        // Executa a condição se "prof" for igual a gerente e realiza o cálculo
        CASO prof = “Gerente”		
            sal_reaj ← 1.3 * sal

    // Realiza o cálculo se nenhuma das condições forem verdadeiras
    SENÃO
        sal_reaj ← 1.1 * sal

    FIM_ESCOLHA

    // Exibe a mensagem com o salário reajustado
    ESCREVA “Salário Reajustado = “, sal_reaj

FIM
```

#### Teste
| sal | prof | prof == “Técnico” | prof = “Gerente” | sal_reaj | Saída |
| -- | -- | -- | -- | -- | -- |
| 1000 | Técnico | V | F | 1500 | “Salário Reajustado = 1500“ |
| 2000 | Gerente | F | V | 2600 | “Salário Reajustado = 2600“ |
| 9000 | Diretor | F | F | 9900 | “Salário Reajustado = 9900“ |

## Lista de exercícios 02

### Exercício 01 (2.5 pontos)
Calcule a média de quatro números inteiros dados.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite o número 1:"}}
B --> C[/num1/]
C --> D{{"Digite o número 2:"}}
D --> E[/num2/]
E --> F{{"Digite o número 3:"}}
F --> G[/num3/]
G --> H{{"Digite o número 2:"}}
H --> I[/num4/]
I --> J["media = (num1 + num2 + num3 + num4)/4"]
J --> K{{A média é, media}}
K --> L([FIM]) 
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORTIMO Media
DECLARE num1, num2, num3, num4: REAL

INICIO

    // Exibe a mensagem para receber o dado de entrada
    ESCREVA "Digite o número 1:"

    // Armazena dado de entrada como "num1"
    LEIA num1

    // Exibe a mensagem para receber o dado de entrada
    ESCREVA "Digite o número 2:"

    // Armazena dado de entrada como "num2"
    LEIA num2

    // Exibe a mensagem para receber o dado de entrada
    ESCREVA "Digite o número 3:"

    // Armazena dado de entrada como "num3"
    LEIA num3

    // Exibe a mensagem para receber o dado de entrada
    ESCREVA "Digite o número 4:"

    // Armazena dado de entrada como "num4"
    LEIA num4

    // Realiza o cálculo atribuindo o resultado a "média"
    media <- (num1 + num2 + num3 + num4)/4
    
    // Exibe a mensagem com a média
    ESCREVA "A média é", media

FIM
```

#### Teste de mesa (0.5 ponto)

| num1 | num2 | num3 | num4 | saída | 
| --   | --   | --   | --   | --    | 
| 0.25 | 0.25 | 2.50 | 1.00 | 1.00  | 

### Exercício 02 (2.5 pontos)
Leia uma temperatura dada em Celsius (C) e imprima o equivalente em Fahrenheit (F). (Fórmula de conversão: F = (9/5) * C + 32)

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a temperatura em Celisus:"}}
B --> C[/C/]
C --> D["F = (9/5) * C + 32"]
D --> E{{A temperatura em Fahrenheit é, F, graus}}
E --> F([FIM])
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORTIMO ConverteCelsiusFarenheit
DECLARE C, F: REAL

INICIO

    // Exibe a mensagem para receber os dados de entrada
    ESCREVA "Digite a temperatura em Celsius:"

    // Armazena o valor de entrada como "C"
    LEIA C

    // Realiza o cálculo e armazena o resultado como variável "F"
    F <- (9/5) * C + 32

    // Exibe a mensagem com a variável "F"
    ESCREVA "A temperatura em Fahrenheit é", F, "graus"

FIM
```

#### Teste de mesa (0.5 ponto)

| C  | F  | saída                                  | 
| -- | -- | --                                     |
| 0  | 32 | A temperatura em Fahrenheit é 32 graus |

### Exercício 03 (2.5 pontos)
Receba dois números reais e um operador e efetue a operação correspondente com os valores recebidos (operandos). 
O algoritmo deve retornar o resultado da operação selecionada simulando todas as operações de uma calculadora simples.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Operações válidas: 1(soma), 2(subtração), 3(multiplicação) e 4(divisão)"}}
B --> C{{Digite uma operação:}}
C --> D[/op/]
D --> E{{Digite um número:}}
E --> F[/num1/]
F --> G{{Digite outro número:}}
G --> H[/num2/]
H --> I{op == 1}
I --FALSE--> J{op == 2}
J --FALSE--> L{op == 3}
L --FALSE--> O{op == 4}
O --FALSE--> Q{{Operação inválida!}}
Q --> R([FIM])
I --TRUE--> M[res = num1 + num2]
M --> S{{num1, + , num2, =, res}}
J --TRUE--> K[res = num1 - num2]
K --> T{{num1, - , num2, =, res}}
L --TRUE--> N[res = num1 * num2]
N --> U{{num1, * , num2, =, res}}
O --TRUE--> P{num2 != 0}
P --FALSE--> X{{Impossível dividir!}}
P --TRUE--> Z[res = num1 / num2]
Z --> V{{num1, / , num2, =, res}}
X --> R
S --> R
T --> R
U --> R
V --> R
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORITMO CalculadoraSimples
DECLARE op: INTEIRO; num1,num2,res: REAL

INICIO

    // Exibe ao usuário as operações válidas
    ESCREVA "Operações válidas: 1(soma), 2(subtração), 3(multiplicação) e 4(divisão)"

    // Exibe a mensagem solicitando uma operação
    ESCREVA "Digite uma operação:"

    // Armazena o dado de entrada como "op"
    LEIA op

    // Exibe a mensagem para receber o valor de entrada
    ESCREVA "Digite um número:"
    
    // Armazena valor recebido como "num1"
    LEIA num1

    // Exibe a mensagem para receber outro valor de entrada
    ESCREVA "Digite outro número:"
    
    // Armazena valor recebido como "num2"
    LEIA num2

    // Verifica a variável "op"
    ESCOLHA

        // Executa a condição se "op" for igual a 1
        CASO op == 1

            // Realiza o cálculo e atribui o resultado a "res"
            res = num1 + num2

            // Exibe a mensagem de acordo com suas variáveis
            ESCREVA num1, "+", num2, "=", res

        // Executa a condição se "op" for igual a 2
        CASO op == 2

            // Realiza o cálculo e atribui o resultado a "res"
            res = num1 - num2

            // Exibe a mensagem de acordo com suas variáveis
            ESCREVA num1, "-", num2, "=", res

        // Executa a condição se "op" for igual a 3
        CASO op == 3

            // Realiza o cálculo e atribui o resultado a "res"
            res = num1 * num2

            // Exibe a mensagem de acordo com suas variáveis
            ESCREVA num1, "*", num2, "=", res

        // Executa a condição se "op" for igual a 4
        CASO op == 4

            // Executa a condição se "num2" for diferente de 0
            SE num2 != 0 ENTAO

                // Realiza o cálculo e atribui o resultado a "res"
                res = num1 / num2

                // Exibe a mensagem de acordo com suas variáveis
                ESCREVA num1, "/", num2, "=", res

            // Exibe a mensagem se "num2" for igual a 0
            SENAO
                ESCREVA "Impossível dividir!"

            FIM_SE

    // Exibe a mensagem se "op" for diferente de todas as condições
    SENAO
        ESCREVA "Operação inválida!"

    FIM_ESCOLHA

FIM
```

#### Teste de mesa (0.5 ponto)

| num1 | num2 | op | num2 != 0 | res | saída               | 
| --   | --   | -- | --        | --  | --                  |
| 1    | 0    | 1  |           | 1   | 1 + 0 = 1           |
| 1    | 0    | 2  |           | 1   | 1 - 0 = 1           |
| 1    | 0    | 3  |           | 0   | 1 * 0 = 0           |
| 1    | 0    | 4  | False     |     | Impossível dividir! |
| 1    | 2    | 4  | True      | 0.5 | 1 / 2 = 0,5         |
| 1    | 2    | 5  |           |     | Operação inválida!  |

### Exercício 04 (2.5 pontos)
Elaborar um algoritmo que, dada a idade, classifique nas categorias: infantil A (5 - 7 anos), infantil B (8 -10 anos), juvenil A (11 - 13 anos), juvenil B (14 -17 anos) e adulto (maiores que 18 anos).

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a idade do aluno:"}}
B --> C[/idade/]
C --> D{idade >=5 <br>E <br>idade <= 7}
D --FALSE--> F{idade >=8 <br>E <br>idade <= 10}
F --FALSE--> G{idade >=11 <br>E <br>idade <= 13}
G --FALSE--> H{idade >=14 <br>E <br>idade <= 17}
H --FALSE--> I{idade >=18}
I --FALSE--> P{{"Digite uma idade válida!"}}
P --> Z([FIM])
D --TRUE--> Q{{Infantial A}}
F --TRUE--> K{{"Infantial B"}}
G --TRUE--> L{{Juvenil A}}
H --TRUE--> M{{Juvenil B}}
I --TRUE--> N{{Adulto}}
Q --> Z
K --> Z
L --> Z
M --> Z
N --> Z
```

#### Pseudocódigo (1.0 ponto)

```java
ALGORTIMO ClassificaCategoria
DECLARE idade: INTEIRO

INICIO

    // Exibe a mensagem pedindo o dado de entrada
    ESCREVA "Digite a idade do aluno:"

    // Armazena o valor como idade "idade"
    LEIA idade

    // Verifica a variável "idade"
    ESCOLHA

        // Executa a condição se "idade" for maior ou igual a 5 e menor ou igual a 7
        CASO idade >=5 E idade <= 7

            // Exibe a mensagem "Infantial A"
            ESCREVA "Infantial A"

        // Executa a condição se "idade" for maior ou igual a 8 e menor ou igual a 10
        CASO idade >=8 E idade <= 10

            // Exibe a mensagem "Infantial B"
            ESCREVA "Infantial B"

        // Executa a condição se "idade" for maior ou igual a 11 e menor ou igual a 13
        CASO idade >=11 E idade <= 13

            // Exibe a mensagem "Juvenil A"
            ESCREVA "Juvenil A"

        // Executa a condição se "idade" for maior ou igual a 14 e menor ou igual a 17
        CASO idade >=14 E idade <= 17

            // Exibe a mensagem "Juvenil B"
            ESCREVA "Juvenil B"

        // Executa a condição se "idade" for maior ou igual a 18
        CASO idade >=18

            // Exibe a mensagem "Adulto"
            ESCREVA "Adulto"

    // Executa a proxima linha se código se "idade" for menor que 5
    SENAO

        // Exibe a mensagem "Digite uma idade válida!"
        ESCREVA "Digite uma idade válida!"

    FIM_ESCOLHA

FIM
```

#### Teste de mesa (0.5 ponto)

| idade | idade >=8 E idade <= 10 | idade >=11 E idade <= 13 | idade >=14 E idade <= 17 | idade >=18 | saída                       | 
| --    | --                      | --                       | --                       | --         | --                          |
| 4     | False                   | False                    | False                    | False      | Digite uma idade válida!    |
| -4    | False                   | False                    | False                    | False      | Digite uma idade válida!    |
| 8     | True                    | False                    | False                    | False      | Infantial A                 |
| 11    | False                   | True                     | False                    | False      | Infantial B                 |
| 17    | False                   | False                    | True                     | False      | Infantial C                 |
| 21    | False                   | False                    | False                    | True       | Adulto                      |
