## Módulos e Bibliotecas

Em Python, um módulo é um arquivo que contém código Python, como funções, classes ou variáveis, que podem ser reutilizados em outros programas.

Uma biblioteca é um conjunto de módulos relacionados, prontos para serem usados, que fornecem funcionalidades extras.

O uso de módulos e bibliotecas permite:

- Reutilizar código

- Organizar projetos de forma mais clara

- Acessar funcionalidades já prontas sem precisar reinventar a roda

---

### Criando e Utilizando um Módulo

Suponha que temos um arquivo chamado `meu_modulo.py`:
```python
# meu_modulo.py

def saudacao(nome):
    print(f"Olá, {nome}!")

def soma(a, b):
    return a + b
```

Podemos usar esse módulo em outro arquivo usando a palavra-chave `import`:

```python
import meu_modulo

meu_modulo.saudacao("Francisco")
resultado = meu_modulo.soma(5, 3)
print(resultado)
```


Saída:

```python
Olá, Francisco!
8
```

### Importando Funções Específicas

Também é possível importar apenas funções ou variáveis específicas:
```python
from meu_modulo import soma

resultado = soma(10, 5)
print(resultado)
```
### Renomeando Módulos

Podemos usar um **apelido** (alias) para facilitar o uso do módulo:
```python
import meu_modulo as mm

mm.saudacao("Ana")
```
### Bibliotecas Padrão do Python

Python possui várias bibliotecas prontas para uso, como:

- `math` → funções matemáticas

- `random` → geração de números aleatórios

- `datetime` → manipulação de datas e horários

Exemplo usando `math`:
```python
import math

print(math.sqrt(16))  # calcula a raiz quadrada
print(math.pi)        # valor de pi
```
### Instalando Bibliotecas Externas

Para utilizar bibliotecas que não fazem parte da instalação padrão do Python, usamos o `pip`:
```python
pip install nome_da_biblioteca
```


Exemplo com `requests`:
```python
import requests

resposta = requests.get("https://api.github.com")
print(resposta.status_code)
```
### Observações Importantes

- Mantenha seus módulos organizados em pastas, se o projeto crescer.

- Evite nomes de módulos que já existem na biblioteca padrão.

- Prefira importar apenas o que é necessário para evitar poluir o espaço de nomes.
