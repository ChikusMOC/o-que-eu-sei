## Variáveis

Variáveis são utilizadas para armazenar valores na memória.

Exemplo:

    nome = 'Francisco'
    idade = 25


Podemos observar que, neste exemplo, a variável nome recebeu uma string, enquanto a variável idade recebeu um valor numérico inteiro (int).

Em Python, não é necessário declarar explicitamente o tipo da variável. A linguagem utiliza tipagem dinâmica, ou seja, o tipo é definido automaticamente no momento em que o valor é atribuído.

Podemos verificar o tipo de cada variável utilizando a função type():

    print(type(nome))
    print(type(idade))


Saída esperada:

    <class 'str'>
    <class 'int'>


A função type() retorna o tipo do objeto armazenado na variável, permitindo confirmar como o Python interpretou o valor atribuído.
