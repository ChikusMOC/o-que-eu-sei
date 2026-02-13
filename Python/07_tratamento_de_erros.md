## Tratamento de Erros

Durante a execução de um programa, podem ocorrer erros inesperados.

Esses erros são chamados de exceções (exceptions).

O tratamento de erros permite que o programa lide com essas situações de forma controlada, evitando que ele seja encerrado abruptamente.

---

### Erro sem Tratamento

Exemplo:

```python
numero = int(input("Digite um número: "))
print(numero)
```
Se o usuário digitar algo que não seja um número, ocorrerá um erro (`ValueError`) e o programa será interrompido.

### Utilizando `try` e `except`

Para evitar que o programa pare inesperadamente, podemos utilizar a estrutura `try` e `except`.

```python
try:
    numero = int(input("Digite um número: "))
    print(numero)
except ValueError:
    print("Você não digitou um número válido.")
```
#### O que acontece aqui?
- O bloco `try` contém o código que pode gerar erro.

- Se ocorrer um erro do tipo `ValueError`, o bloco `except` será executado.

- O programa continua executando normalmente após o tratamento.

### Capturando Diferentes Tipos de Erro
Podemos tratar diferentes tipos de exceção.

```python
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Não é possível dividir por zero.")
```
Cada tipo de erro possui uma classe específica.

### Capturando o Erro em uma Variável
Podemos capturar informações sobre o erro:

```python
try:
    numero = int("abc")
except ValueError as erro:
    print("Ocorreu um erro:", erro)
```
A variável `erro` contém detalhes sobre a exceção ocorrida.

### Utilizando `else`
O bloco `else` é executado quando nenhum erro ocorre.

```python
try:
    numero = int("10")
except ValueError:
    print("Erro na conversão.")
else:
    print("Conversão realizada com sucesso.")
```
### Utilizando `finally`
O bloco `finally` sempre será executado, independentemente de erro.

```python
try:
    print("Executando operação")
except Exception:
    print("Ocorreu um erro")
finally:
    print("Finalizando operação")
```
Ele é frequentemente utilizado para liberar recursos, como fechar arquivos ou conexões.

### Estrutura Completa
```python
try:
    # código que pode gerar erro
except TipoDeErro:
    # tratamento do erro
else:
    # executado se não houver erro
finally:
    # sempre executado
```
### Observação Importante
Evite utilizar `except:` de forma genérica.

Capturar exceções de maneira ampla pode ocultar erros inesperados e dificultar a depuração.

O ideal é tratar exceções específicas, tornando o código mais seguro, previsível e fácil de manter.

### Por que tratar erros é importante?
O tratamento de erros:

- Evita que o programa seja encerrado inesperadamente

- Permite controlar falhas

- Melhora a experiência do usuário

- Torna o código mais robusto e profissional
