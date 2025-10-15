<line-height=50%><size=40px>Funções</size>
</line-height>
Use a palavra-chave def para definir uma nova função:
def f(arg1, arg2 = False):
	#código da função

Você pode usar o operador de chamada () para chamar a função:
f(42)

Veja também <u><link="docs/scripting/scopes.md">Escopos</link></u> para aprender sobre variáveis locais e globais em funções.

<line-height=50%><size=32px>Introdução</size>
</line-height>
Você já viu funções nativas como harvest().
Você também pode definir suas próprias funções, o que permite estruturar seu código de forma modular. Basicamente, permite que você dê um nome a um bloco de código para que possa chamá-lo de onde quiser.

<line-height=50%><size=32px>Definições de Funções</size>
</line-height>
Por exemplo, você poderia definir uma função que move o drone várias vezes.

def move_n_dir(n, dir):
	for i in range(n):
		move(dir)

A palavra-chave def sinaliza que esta é uma definição de função. 
move_n_dir é o nome ao qual a função é vinculada. Pode ser qualquer nome de variável válido e será usado para chamar a função.
n e dir são parâmetros. São variáveis que guardam os valores que são passados para a função (esses valores também são chamados de argumentos). Você pode adicionar quantos parâmetros quiser a uma definição de função.
Após o : vem o bloco de código que será executado quando a função for chamada.

Com a definição acima, o código a seguir move o drone 10 casas para North e 2 casas para West.

move_n_dir(10, North)
move_n_dir(2, West)

Quando você vê def function():, você realmente deveria pensar nisso como uma atribuição de variável como esta:
function = create_new_function_object()
Como em todas as atribuições, você não pode usar a variável antes que ela seja atribuída!
A declaração def tem que ser executada antes de qualquer chamada de função.
Este código lançará um erro:

func()
def func():
	pass

<line-height=50%><size=32px>Valores de Retorno</size>
</line-height>
Use a palavra-chave return para fazer uma função retornar um valor. 
Por exemplo, a seguinte função define a operação ou exclusivo. O ou exclusivo retorna True se um valor for True e o outro for False:

def xor(a, b):
	return a != b

if xor(True, False):
	do_a_flip()

<u><link="docs/scripting/tuples.md">Tuplas</link></u> permitem retornar múltiplos valores.

<line-height=50%><size=32px>Argumentos Padrão</size>
</line-height>
Você também pode atribuir valores padrão que serão usados se nenhum argumento for passado.

def f(a = False):
	if a:
		do_a_flip()

f()

f(True)

Um argumento que tem um valor padrão não pode ser seguido por um argumento que não tem um valor padrão.

<line-height=50%><size=32px>Uso Avançado de Funções</size>
</line-height>
Funções são valores como qualquer outro valor, e a declaração def age como uma declaração de atribuição, atribuindo a função a qualquer nome que você lhe der.
Isso permite fazer coisas como esta:

def f():
	def d():
		do_a_flip()
	return d

f()()

Aqui, f() chama a função f que define e retorna uma nova função d. O segundo () então executa a função retornada e realiza a pirueta.
(Fazer esse tipo de coisa geralmente não é uma boa ideia porque é difícil ver o que está acontecendo)

Funções que recebem outras funções como argumentos permitem que você seja realmente criativo:

def f(g, arg):
	for _ in range(10):
		g(arg)

f(move, North)
f(use_item, Items.Fertilizer)

Este código move o drone North 10 vezes e depois usa fertilizante 10 vezes.