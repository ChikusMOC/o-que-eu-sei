## Funções Lambda

Funções `lambda` são funções anônimas (ou seja, não possuem nome explícito) criadas por meio de uma expressão.

Elas são utilizadas principalmente para operações simples e pontuais, especialmente quando uma função precisa ser passada como argumento para outra função.

Uma função `lambda`:

- É definida sem usar `def`

- Não possui nome obrigatório

- Aceita parâmetros normalmente

- É limitada a uma única expressão

- Retorna automaticamente o resultado dessa expressão

Importante:
Uma expressão é algo que produz um valor. Por isso, `lambda` não permite múltiplas instruções como `for`, `while`, `if` com bloco, ou várias linhas de código.

### Sintaxe
```python
lambda parametros: expressao
```

### Exemplo
```python
soma = lambda a, b: a + b
print(soma(5, 3))
```

Saída:
```python
8
```

### Nesse exemplo:

- `a` e `b` são os parâmetros

- `a + b` é a expressão

- O valor da expressão é retornado automaticamente

### Quando usar?

Funções `lambda` são comuns quando precisamos passar uma função como argumento, por exemplo em `map`, `filter` ou `sorted`.
```python
numeros = [1, 2, 3, 4]

dobrados = list(map(lambda x: x * 2, numeros))
print(dobrados)
```

Saída:
```python
[2, 4, 6, 8]
```
## `*args`

O parâmetro `*args` permite que uma função receba uma quantidade variável de argumentos posicionais.

Exemplo:
```python
def somar(*args):
    print(args)

somar(1, 2, 3, 4)
```

Saída:
```python
(1, 2, 3, 4)
```
### O que acontece aqui?

- Todos os argumentos são agrupados em uma **tupla**.

- Podemos percorrer esses valores normalmente.

Exemplo prático:
```python
def somar(*args):
    total = 0
    for numero in args:
        total += numero
    return total

print(somar(1, 2, 3))
```

Saída:
```python
6
```

O nome `args` é apenas uma convenção.

O importante é o uso do asterisco (`*`).

Exemplo:
```python
def exemplo(*valores):
    print(valores)
```
## `**kwargs`

O parâmetro `**kwargs` permite receber uma quantidade variável de argumentos nomeados.

Exemplo:
```python
def mostrar_dados(**kwargs):
    print(kwargs)

mostrar_dados(nome="Ana", idade=25)
```

Saída:
```python
{'nome': 'Ana', 'idade': 25}
```
### O que acontece aqui?

- Os argumentos são agrupados em um **dicionário**.

- As chaves são os nomes dos parâmetros.

- Os valores são os dados passados.

Exemplo percorrendo:
```python
def mostrar_dados(**kwargs):
    for chave, valor in kwargs.items():
        print(chave, ":", valor)

mostrar_dados(nome="Carlos", cidade="SP")
```

O nome `kwargs` também é apenas uma convenção.

O importante é o uso de dois asteriscos (`**`).

Exemplo:
```python
def exemplo(**valores):
    print(valores)
```

## Uso conjunto de `*args` e `**kwargs`

Também é possível utilizar `*args` e `**kwargs` juntos na mesma função.

Exemplo:
```python
def exemplo(*args, **kwargs):
    print("Argumentos posicionais:", args)
    print("Argumentos nomeados:", kwargs)

exemplo(1, 2, 3, nome="Ana", idade=25)
```

Saída:
```python
Argumentos posicionais: (1, 2, 3)
Argumentos nomeados: {'nome': 'Ana', 'idade': 25}
```
### O que acontece aqui?

- Os valores `1`, `2`, `3` são capturados por `*args` e armazenados em uma tupla.

- Os argumentos nomeados (`nome` e `idade`) são capturados por `**kwargs` e armazenados em um dicionário.

- Podemos usar ambos quando queremos criar funções mais flexíveis.

### Ordem obrigatória dos parâmetros

É importante destacar que a ordem deve ser obrigatoriamente:

```python
def funcao(parametros_normais, *args, **kwargs):
    pass
```

Ou seja:

1. Parâmetros comuns

2. `*args`

3. `**kwargs`

### `*args` deve vir antes de `**kwargs`. 
### Se inverter a ordem, o Python gerará erro de sintaxe.

## List Comprehension

List comprehension é uma forma compacta e legível de criar listas a partir de iteráveis.

Forma tradicional:
```python
quadrados = []
for x in range(5):
    quadrados.append(x**2)

print(quadrados)
```

Forma com list comprehension:
```python
quadrados = [x**2 for x in range(5)]
print(quadrados)
```

Saída:
```python
[0, 1, 4, 9, 16]
```

Também pode conter condição:
```python
pares = [x for x in range(10) if x % 2 == 0]
print(pares)
```

Saída:
```python
[0, 2, 4, 6, 8]
```

## Dictionary Comprehension

Assim como listas, também podemos criar dicionários de forma compacta.

Exemplo:
```python
quadrados = {x: x**2 for x in range(5)}
print(quadrados)
```

Saída:
```python
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

Com condição:
```python
pares = {x: x**2 for x in range(10) if x % 2 == 0}
print(pares)
```

Saída:
```python
{0: 0, 2: 4, 4: 16, 6: 36, 8: 64}
```
## Observação Importante

Esses recursos tornam o código:

- Mais compacto
- Mais flexível
- Mais expressivo

No entanto, é importante não sacrificar a legibilidade.

Um código claro e fácil de entender deve sempre ser prioridade,
mesmo que ele não seja o mais curto possível.
