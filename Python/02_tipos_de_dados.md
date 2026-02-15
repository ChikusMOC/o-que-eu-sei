## Tipos de Dados

Em Python, todo valor possui um tipo.
O tipo de dado define quais operações podem ser realizadas com aquele valor e como ele se comporta durante a execução do programa.

Como Python utiliza tipagem dinâmica, o tipo é definido automaticamente no momento da atribuição.

---

## Tipos Numéricos
### `int` — Inteiros

Representam números inteiros (positivos ou negativos), sem parte decimal.
```python
idade = 25
temperatura = -3
```
### `float` — Números de ponto flutuante

Representam números com parte decimal.
```python
altura = 1.75
pi = 3.1415
```
## Tipo Texto
### `str` — String

Representa sequências de caracteres (texto).
```python
nome = "Francisco"
mensagem = 'Olá, mundo'
```

Strings podem ser escritas com aspas simples ou duplas.

## Tipo Booleano
### `bool`

Representa valores lógicos:

- `True`

- `False`
```python
maior_de_idade = True
aprovado = False
```

Valores booleanos são frequentemente utilizados em estruturas de seleção.

## Tipo Lista
### `list` 

Estrutura utilizada para armazenar múltiplos valores em uma única variável.
```python
numeros = [1, 2, 3, 4]
nomes = ["Ana", "Carlos", "Maria"]
```

Listas são mutáveis, ou seja, podem ser alteradas após a criação.

## Tipo Tupla
### `tuple`

Semelhante à lista, porém imutável.
```python
coordenadas = (10, 20)
```

Após criada, uma tupla não pode ser modificada.

## Tipo Dicionário
### `dict`

Estrutura que armazena dados em formato de chave e valor.
```python
pessoa = {
    "nome": "Francisco",
    "idade": 25
}
```

Cada chave está associada a um valor.

## Verificando Tipos

Podemos utilizar a função `type()` para verificar o tipo de um valor:
```python
print(type(10))
print(type("Python"))
print(type([1, 2, 3]))
```
## Observação Importante

Como Python é dinamicamente tipado, uma variável pode receber valores de tipos diferentes ao longo do programa:
```python
valor = 10
valor = "dez"
```

O tipo será redefinido automaticamente na nova atribuição.
