## Estruturas de Repetição

Estruturas de repetição permitem executar um bloco de código múltiplas vezes, enquanto uma determinada condição for satisfeita ou para cada elemento de uma sequência.

Elas são utilizadas quando precisamos automatizar tarefas repetitivas dentro de um programa.

## Laço `for`

O laço `for` é utilizado para percorrer sequências, como listas, strings ou intervalos numéricos.

### Exemplo com `range()`
```python
for i in range(5):
    print(i)
```
O que acontece nesse exemplo?

- A função `range(5)` cria um objeto iterável que representa os números de 0 até 4.

- A cada iteração, o valor é armazenado na variável `i`.

- O bloco dentro do `for` é executado para cada valor da sequência.

Saída esperada:

```python
0
1
2
3
4
```
### Ainda sobre `range()`
Podemos definir o início, o fim e o passo, que determina como os valores avançam do início até o fim.
```python
range(inicio, fim, passo)
```
Exemplo:

```python
for i in range(1, 10, 2):
    print(i)
```
Neste exemplo, a saída será:
```python
1
3
5
7
9
```

### Percorrendo uma lista
```python
nomes = ["Ana", "Carlos", "Maria"]
for nome in nomes:
    print(nome)
```

Nesse caso, o laço percorre cada elemento da lista e executa o bloco para cada item.

## Laço `while`

O laço `while` executa um bloco de código enquanto uma condição for verdadeira.

```python
contador = 0

while contador < 5:
    print(contador)
    contador += 1
```
### O que acontece nesse exemplo?

- A condição `contador < 5` é avaliada.

- Enquanto for `True`, o bloco será executado.

- O valor de `contador` é incrementado a cada repetição.

- Quando a condição se torna `False`, o laço é encerrado.

## Controle de Fluxo em Laços
### `break`

Interrompe o laço imediatamente.
```python
for numero in range(10):
    if numero == 5:
        break
    print(numero)
```

O laço será encerrado quando `numero` for igual a 5.

### `continue`

Interrompe apenas a iteração atual e continua para a próxima.
```python
for numero in range(5):
    if numero == 2:
        continue
    print(numero)
```

Nesse caso, o número 2 não será exibido.
## Importante

É fundamental garantir que a condição do `while` eventualmente se torne `False`.
Caso contrário, o programa entrará em um loop infinito, consumindo recursos indefinidamente.

Exemplo de loop infinito:

```python
contador = 0

while contador < 5:
    print(contador)
```


Nesse exemplo, `contador` nunca é incrementado.
A condição `contador < 5` será sempre `True`, fazendo com que o laço nunca termine.

Forma correta:

```python
contador = 0

while contador < 5:
    print(contador)
    contador += 1
```

## Diferença entre `for` e `while`

`for` → usado quando sabemos quantas vezes queremos repetir ou quando percorremos uma sequência.

`while` → usado quando a repetição depende de uma condição que pode variar.

## Como isso funciona na prática?

O Python executa o bloco de código repetidamente, avaliando a condição (no caso do `while`) ou percorrendo cada elemento da sequência (no caso do `for`), até que o critério de parada seja atingido.
