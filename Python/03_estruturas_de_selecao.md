### Estruturas de Seleção

Estruturas de seleção permitem que o programa tome decisões com base em condições lógicas.
Elas controlam o fluxo de execução do código, executando diferentes blocos conforme o resultado de uma expressão booleana (`True` ou `False`).

## If / Elif / Else

A estrutura de decisão em Python pode ser composta por:

`if` → obrigatório (inicia a estrutura)

`elif` → opcional (pode haver nenhum ou vários)

`else` → opcional (executado caso nenhuma condição anterior seja verdadeira)

Exemplo:

```python
numero = 5

if numero > 5:
    print("Maior que 5")
elif numero == 5:
    print("Igual a 5")
else:
    print("Menor que 5")
```

## O que acontece nesse exemplo?

O Python avalia `numero > 5`.

Como a condição é `False`, ele passa para a próxima verificação.

Avalia `numero == 5`.

Como essa condição é `True`, executa o bloco correspondente.

As demais verificações são ignoradas.

## Sobre o `elif`

O `elif` (abreviação de else if) permite adicionar múltiplas condições intermediárias.
Ele é opcional e pode aparecer várias vezes dentro da mesma estrutura.

Se nenhuma condição for verdadeira e houver um `else`, o bloco do `else` será executado.

## Observação Importante

A condição precisa resultar em um valor que possa ser interpretado como `True` ou `False`.

```python
print(numero == 5)
```

Saída:

```python
True
```


A estrutura de seleção utiliza esse resultado para decidir qual bloco de código será executado.

## Operadores de Comparação

Os operadores de comparação são utilizados para construir condições dentro das estruturas de seleção.

| Operador | Significado |
|----------|------------|
| `==` | Igual |
| `!=` | Diferente de |
| `>` | Maior que |
| `<` | Menor que |
| `>=` | Maior ou igual a |
| `<=` | Menor ou igual a |

Exemplo:
```python
numero = 10

print(numero > 5)   # True
print(numero == 10) # True
print(numero < 3)   # False
```

Esses operadores retornam valores booleanos (`True` ou `False`), que são utilizados pelas estruturas de decisão.

## Operadores Lógicos

Os operadores lógicos permitem combinar múltiplas condições em uma mesma expressão.

### `and`

Retorna `True` somente se todas as condições forem verdadeiras.
```python
idade = 20
tem_carteira = True

if idade >= 18 and tem_carteira:
    print("Pode dirigir")
```
### `or`

Retorna `True` se pelo menos uma das condições for verdadeira.
```python

dia = "sábado"

if dia == "sábado" or dia == "domingo":
    print("Final de semana")
```
### `not`

Inverte o valor lógico da condição.
```python
logado = False

if not logado:
    print("Usuário não está logado")
```

## Como isso funciona na prática?

O Python avalia cada expressão da esquerda para a direita, resolve primeiro as comparações, depois aplica os operadores lógicos conforme a precedência, e por fim utiliza o resultado final para decidir qual bloco será executado.
