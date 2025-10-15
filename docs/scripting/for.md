<line-height=50%><size=40px>Loop For</size>
</line-height>
O loop for funciona como no Python. (Chamado de loop foreach em algumas linguagens, não deve ser confundido com o loop for no estilo C, que é uma coisa diferente).

for i in sequence:
	#faça algo com i

Semelhante ao loop while, o loop for também chama repetidamente um bloco de código. Em vez de fazer um loop com base em uma condição, ele executa o corpo do loop uma vez para cada elemento em uma sequência.

<line-height=50%><size=32px>Sintaxe</size>
</line-height>
Um loop for se parece com isto:

for variable_name in sequence:
	#bloco de código

variable_name pode ser qualquer nome que você escolher. É uma variável que armazena o elemento atual na sequência. sequence precisa ser algum valor que possa ser iterado, como um range ou números. O bloco de código é executado para cada elemento com a variável do loop atribuída a esse elemento.

<line-height=50%><size=32px>Sequências</size>
</line-height>
<u><link="functions/range">Ranges</link></u>      

<line-height=50%><size=32px>Exemplo</size>
</line-height>
for i in range(5):
    harvest()

Este loop executa o corpo um número fixo de vezes. É essencialmente o mesmo que escrever

i = 0
harvest()
i = 1
harvest()
i = 2
harvest()
i = 3
harvest()
i = 4
harvest()

Então ele chama harvest() 5 vezes.

Veja também <u><link="docs/scripting/break.md">Break</link></u> e <u><link="docs/scripting/continue.md">Continue</link></u>