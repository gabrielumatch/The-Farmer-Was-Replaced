<line-height=50%><size=40px>Tuplas</size>
</line-height>
Tuplas são uma ótima maneira de combinar múltiplos valores em um único valor.
Para criar uma tupla, basta separar os valores com vírgulas:

tuple = 1, 2

Você também pode desempacotá-las em várias variáveis novamente. No código abaixo, a tupla (1,2) é desempacotada em duas variáveis a e b.

a, b = 1, 2

Tuplas podem ser indexadas como listas, mas são imutáveis e não podem ser alteradas após a criação.

tuple = 1, 2

print(tuple[1])
imprime 2

tuple[0] = 3
lança um erro


Elas também podem ser úteis para retornar múltiplos valores em uma função.

def f():
    return 1, 2

a, b = f()