## Pandas

Pandas é uma biblioteca Python para **análise e manipulação de dados**.

Ela facilita trabalhar com tabelas, séries temporais e dados estruturados de forma geral.

Importando a biblioteca
```python
import pandas as pd
```

Por convenção, renomeamos como `pd` para facilitar o uso.

Essa é a forma padrão utilizada pela maioria dos tutoriais e documentação.

### DataFrame

Um **DataFrame** é a estrutura principal do Pandas:

- Funciona como uma **tabela de dados**, com **linhas e colunas**.

- Cada coluna pode ter **um tipo diferente de dado** (números, texto, datas etc.).

- Permite fácil acesso, filtragem, agregação e manipulação de dados.

Exemplo de DataFrame:

| Nome	| Idade | Cidade |
|------|------|------|
| Ana	| 25 |	SP |
| Carlos |	30 |	RJ |
| Maria |	28 |	MG |

### Lendo  arquivos

```python
arquivo_df = pd.read_csv('nome_do_arquivo.csv')
```

Por convenção, usamos `_df` para indicar que a variável é um DataFrame.

### Parâmetros importantes:

- `sep` → define o separador de colunas (padrão `,`)

- `decimal` → define o símbolo decimal (padrão `.`)

É importante verificar como os dados foram lidos para garantir consistência.

```python
print(arquivo_df.info())
```

O método `info()` mostra:

- Número de linhas e colunas

- Tipos de dados de cada coluna (`int`, `float`, `object` etc.)

- Quantidade de valores nulos

Isso ajuda a planejar o tratamento dos dados antes de analisá-los.

### Visualizando os dados

```python
# Mostrar as primeiras linhas
print(arquivo_df.head())

# Mostrar as últimas linhas
print(arquivo_df.tail())
```

- `head()` exibe as 5 primeiras linhas por padrão

- `tail()` exibe as 5 últimas linhas por padrão

### Resumo

- Pandas é a biblioteca essencial para análise de dados em Python.

- Um DataFrame é como uma tabela com linhas e colunas, permitindo manipulação fácil.

- Sempre verifique os dados lidos (`info()`, `head()`) antes de iniciar a análise.
