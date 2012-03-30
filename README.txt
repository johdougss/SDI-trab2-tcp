Implementa��o de um Servi�o de Informa��es utilizando
Comunica��o Inter-processos atrav�s de TCP
Prof. Adriano Fiorese

1 Caracteriza��o do Servi�o
O Servi�o de Informa��es � respons�vel por fornecer aos seus clientes as seguintes informa��es, de acordo
com solicita��o espec�fica:
	1. Diret�rio onde atualmente executa o software servidor
	2. Hora atual no servidor e na mesma resposta tempo total de execu��o do servidor

2 Implementa��o
A implementa��o de tal servi�o dever� ser realizada utilizando-se comunica��o Inter-Processos por meio de
streams TCP. O modelo arquitetural a ser utilizado dever� ser o cliente/servidor.
O servidor dever� estar apto a atender \ao mesmo tempo" 10 clientes.
Lembre-se da necessidade da cria��o do protocolo request/reply da camada de aplica��o.
O modelo de desenvolvimento dever� considerar a necessidade de uma intera��o entre cliente e servidor,
iniciada pelo servidor, para autentica��o. Apenas ap�s a autentica��o (pode ser usu�ario e senha). Nesse mo-
mento o servidor dever� enviar sinaliza��o ao cliente informando-o que pode come�ar a transmitir as requisi��es.
O servidor dever� levar em conta threads, n�o s�o pela necessidade de atendimento \ao mesmo tempo" de
at� 10 clientes, mas tamb�m por que uma thread espec�fica ser� respons�vel pelo mecanismo de autentica��o.
Uma segunda Thread dever� ser respons�vel pela intera��o propriamente dita com o cliente. A Fig. 1 ilustra o
modelo de implementa��o.

3 Prazos
Entrega dos execut�veis, do c�digo fonte do cliente e servidor, bem como c�digo impresso dia 10/04/2012.


----------------------------------------------------
- Java 7