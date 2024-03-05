# UNIFOR
**Disciplina:** Raciocínio Lógico Algorítmico 
**Orientador:** Prof. Ricardo Carubbi

## Lista 1 de Exercícios

### Exercício 3
Represente, em fluxograma e pseudocódigo, um algoritmo para determinar se um número inteiro e positivo é par ou impar.

#### Fluxograma

```mermaid
flowchart TD
A([INÍCIO])-->B{{Digite um número:}}
B-->C[/numero/]
C-->D{numero > 0}
D--N-->E{{O número deve ser positivo!}}
E-->J
D--S-->F[resto = numero % 2]
F-->G{resto == 0}
G--N-->H{{O número é impar!}}
G--S-->I{{O número é par!}}
H-->J([FIM])
I-->J
```


```
ALGORITMO verifica_par_impar
DECLARE numero,resto INTEIRO
ESCREVA "Digite um número"
LEIA número
SE numero > 0 ENTAO
	resto = numero % 2
	SE resto == 0 ENTAO
		ESCREVA "O número é par!"
	SENAO
		ESCREVA"O número é impar!"
SENAO
	ESCREVA"O número deve ser positivo"
FIM_ALGORITMO
```
