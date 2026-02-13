### Estruturas de Seleção

Estruturas de seleção permitem que o programa tome decisões com base em condições lógicas.
Elas controlam o fluxo de execução do código, executando diferentes blocos conforme o resultado de uma expressão booleana (True ou False).

## If / Elif / Else

A estrutura de decisão em Python pode ser composta por:

`if` → obrigatório (inicia a estrutura)

`elif` → opcional (pode haver nenhum ou vários)

`else` → opcional (executado caso nenhuma condição anterior seja verdadeira)

Exemplo:


    numero = 5

    if numero > 5:
        print("Maior que 5")
    elif numero == 5:
        print("Igual a 5")
    else:
        print("Menor que 5")

## O que acontece nesse exemplo?

O Python avalia numero > 5.

Como a condição é False, ele passa para a próxima verificação.

Avalia numero == 5.

Como essa condição é True, executa o bloco correspondente.

As demais verificações são ignoradas.

## Sobre o elif

O elif (abreviação de else if) permite adicionar múltiplas condições intermediárias.
Ele é opcional e pode aparecer várias vezes dentro da mesma estrutura.

Se nenhuma condição for verdadeira e houver um else, o bloco do else será executado.

## Observação Importante

A condição sempre precisa resultar em um valor booleano:

print(numero == 5)


Saída:

True


A estrutura de seleção utiliza esse resultado para decidir qual bloco de código será executado.
