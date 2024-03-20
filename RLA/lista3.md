# UNIFOR
**Nome**: Lucas Gabriel Brigagão <br>
**Disciplina**: Raciocínio lógico algorítmico

### Exercício 01 (2.5 pontos)
Atualize o algoritmo para determinar se um número inteiro e positivo é par ou ímpar, usando uma laço condicional para aceitar apenas números maiores ou iguais a zero.

#### Fluxograma (1.0 ponto)
```mermaid
flowchart TD
A([INICIO])-->B{{Digite um número:}}
B-->C[/numero/]
C-->D{numero < 0}
D--N-->E{{O número deve ser positivo!}}
E-->F{{Digite um número:}}
F-->G[/numero/]
G--LOOP-->D
D--S-->H[resto = numero % 2]
H-->I{resto = 0}
I--N-->J{{O número é impar!}}
I--S-->K{{O número é par!}}
K-->L([FIM])
J-->L
```

#### Pseudocódigo (1.0 ponto)
```
ALGORITMO par_ou_impar
DECLARE numero: INTEIRO
ESCREVA "Digite um número"
LEIA numero
ENQUANTO numero < 0 FAÇA
	ESCREVA "O número deve ser positivo"
	ESCREVA "Digite um número"
	LEIA numero
FIM_ENQUANTO
resto = numero % 2
SE resto = 0
ENTAO
	ESCREVA "O número é par"
SENAO
	ESCREVA "O número é impar"
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)
| numero | numero < 0 | resto = 0 | Saída 
| -- | -- | -- | -- |
| 6 | N | S | O número é par
| 9 | N | N | O número é impar
| -1 | S |  | O número deve ser positivo

### Exercício 02 (2.5 pontos)
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.

#### Fluxograma (1.0 ponto)
```mermaid
flowchart TD
A([INICIO])-->B{{O programa vai mostrar os multiplos de 3 até o número 30}}
B-->C[/numero = 30/]
C-->D[[i = 0 ATÉ numero PASSO 3]]
D-->E{{i}}
E-->D
E-->F([FIM])
```
#### Pseudocódigo (1.0 ponto)
```
ALGORITMO multiplo_de_três
DECLARE numero,i
numero = 30
LEIA numero
PARA i DE 0 ATÉ numero FAÇA
	ESCREVA "i"
FIM_PARA
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)
| i | n | Saída      
| -- | -- | --        
| 0 | 30 | 0   
| 3| 30 | 3   
| 6 | 30 | 6  
| 9 | 30 | 9
| 12 | 30 | 12
| 15 | 30 | 15
| 18 | 30 | 18
| 21 | 30 | 21
| 24 | 30 | 24
| 27 | 30 | 27
| 30 | 30 | 30       

### Exercício 03 (2.5 pontos)
Dada uma sequência de números inteiros, calcular a sua soma. 
Por exemplo, para a sequência {12, 17, 4, -6, 8, 0}, o seu programa deve escrever o número 35.

#### Fluxograma (1.0 ponto)
```mermaid
flowchart TD
```

#### Pseudocódigo (1.0 ponto)
```

```

#### Teste de mesa (0.5 ponto)

### Exercício 04 (2.5 pontos)
Escreva um programa que leia a nota de diversos alunos, até que seja digitada uma nota negativa. 
Nesse momento, ele mostra a média aritmética de todas as notas lidas e quantas notas foram lidas. 
Ex. Foram lidas 14 notas. A média aritmética é 6.75!

#### Fluxograma (1.0 ponto)
```mermaid
flowchart TD
```

#### Pseudocódigo (1.0 ponto)
```
```

#### Teste de mesa (0.5 ponto)
