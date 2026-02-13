## Funções

Funções são blocos de código reutilizáveis que executam uma tarefa específica.

Elas ajudam a organizar o código, evitar repetições e tornar o programa mais legível e modular.

## Definindo uma Função

Em Python, utilizamos a palavra-chave `def` para criar uma função.
```python
def saudacao():
    print("Olá!")
```

Nesse exemplo:

- `def` indica que estamos definindo uma função.

- `saudacao` é o nome da função.

- Os parênteses `()` podem receber parâmetros (veremos abaixo).

- O bloco indentado contém o código que será executado.

Para executar a função, precisamos chamá-la:

```python
saudacao()
```

## Função com Parâmetros

Parâmetros permitem que a função receba informações externas.

```python
def saudacao(nome):
    print(f"Olá, {nome}!")
```


Chamando a função:

```python
saudacao("Francisco")
```


Saída:

```python
Olá, Francisco!
```

## Retornando Valores com `return`

Funções podem devolver um valor utilizando a palavra-chave `return`.

```python
def soma(a, b):
    return a + b
```


Utilizando o retorno:

```python
resultado = soma(5, 3)
print(resultado)
```


Saída:

```python
8
```

## O que acontece aqui?

- A função recebe dois valores (`a` e `b`).

- Calcula a soma.

- Retorna o resultado.

- O valor retornado é armazenado na variável `resultado`.

## Diferença entre `print` e `return`

- `print` → Exibe algo na tela.
- `return` → Envia um valor de volta para quem chamou a função.

Exemplo:

```python
def exemplo():
    print("Executando função")
    return 10
```


O `print` apenas mostra algo.
O `return` permite reutilizar o valor em outras partes do código.

## Parâmetros com Valor Padrão

Podemos definir valores padrão para parâmetros:

```python
def saudacao(nome="Visitante"):
    print(f"Olá, {nome}!")
```


Se nenhum argumento for passado:

```python
saudacao()
```


Saída:

```python
Olá, Visitante!
```

## Importância das Funções

Funções:

- Evitam repetição de código

- Melhoram a organização

- Facilitam manutenção

- Tornam o código mais reutilizável
