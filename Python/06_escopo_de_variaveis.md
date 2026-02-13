## Escopo de Variáveis

Escopo define onde uma variável pode ser acessada dentro do programa.

Em Python, o escopo determina em quais partes do código uma variável é visível e pode ser utilizada.

Compreender escopo é fundamental para evitar erros e comportamentos inesperados.

---

## Variável Local

Uma variável criada dentro de uma função é chamada de variável local.

Ela só pode ser acessada dentro da própria função.

```python
def exemplo():
    mensagem = "Olá"
    print(mensagem)

exemplo()
```

Se tentarmos acessar `mensagem` fora da função:

```python
print(mensagem)
```


Ocorre um erro (`NameError`), pois a variável não existe fora daquele escopo.

### O que acontece aqui?

- A variável `mensagem` é criada dentro da função.

- Ela existe apenas durante a execução da função.

- Após o término da execução da função, ela deixa de existir naquele escopo.

## Variável Global

Uma variável definida fora de qualquer função é chamada de variável global.

Ela pode ser acessada dentro das funções para leitura, desde que não haja uma variável local com o mesmo nome.

```python
nome = "Francisco"

def mostrar_nome():
    print(nome)

mostrar_nome()
```


Nesse caso, a função consegue acessar a variável global `nome`.

## Modificando Variáveis Globais

Para alterar o valor de uma variável global dentro de uma função, é necessário utilizar a palavra-chave `global`.

```python
contador = 0

def incrementar():
    global contador
    contador += 1

incrementar()
print(contador)
```

### O que acontece aqui?

- A variável `contador` foi definida fora da função.

- A palavra-chave `global` informa ao Python que estamos usando a variável global.

- O valor é alterado corretamente.

Sem o uso de `global`, o Python criaria uma nova variável local com o mesmo nome.

## Escopo Enclosing (Função dentro de Função)

Python permite funções dentro de outras funções.

Nesse caso, a função interna pode acessar variáveis da função externa.
```python
def externa():
    mensagem = "Olá"

    def interna():
        print(mensagem)

    interna()

externa()
```

A função `interna` consegue acessar `mensagem` porque ela está no escopo da função externa (escopo enclosing).

## Regra de Busca (LEGB)

O Python procura variáveis seguindo esta ordem:

- L → Local

- E → Enclosing

- G → Global

- B → Built-in (nomes internos do Python, como `print`, `type`, etc.)

Se a variável não for encontrada nessa sequência, ocorre um erro.

## Observação Importante

Evitar o uso excessivo de variáveis globais é uma boa prática.

Manter variáveis no menor escopo possível:

- Torna o código mais organizado

- Reduz efeitos colaterais

- Facilita manutenção

- Torna funções mais independentes

## Por que entender escopo é importante?

Compreender escopo:

- Evita erros como `NameError`

- Ajuda a entender como o Python resolve nomes de variáveis

- Permite escrever código mais seguro e previsível
