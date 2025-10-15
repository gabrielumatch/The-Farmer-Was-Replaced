Melhoria de Velocidade</size>
</line-height>
A velocidade de execução foi dobrada. O problema é que o drone agora colhe mais rápido do que a grama pode crescer, resultando em nenhuma colheita. Para lidar com isso, o <u><link="docs/scripting/if.md">if</link></u> e a função <u><link="functions/can_harvest">can_harvest</link></u> agora estão desbloqueados.

<line-height=50%><size=32px>Verificando Antes de Colher</size>
</line-height>
Até agora, só tínhamos True e False como condições, o que, claro, não é muito útil com if. 

A nova função can_harvest() fornece uma condição melhor. can_harvest() retorna True se a planta sob o drone puder ser colhida e False caso contrário.

if can_harvest():
	#faça algo

A razão pela qual você pode usar esta função como uma condição assim é porque ela retorna um valor booleano.

Um valor de retorno essencialmente significa que, após a funcionalidade ser executada, a expressão de chamada da função é avaliada para o valor retornado.

O que acontece quando o código acima é executado:
	-o if é executado
	-can_harvest() é chamada
	-can_harvest() faz o que tem que fazer
	-can_harvest() retorna True ou False
	-a instrução agora é if True: ou if False:
	-o bloco de código só é executado se for possível colher

Agora podemos usar if para impedir que o drone colha cedo demais.