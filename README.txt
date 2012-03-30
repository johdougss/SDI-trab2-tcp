Implementação de um Serviço de Informações utilizando
Comunicação Inter-processos através de TCP
Prof. Adriano Fiorese

1 Caracterização do Serviço
O Serviço de Informações é responsável por fornecer aos seus clientes as seguintes informações, de acordo
com solicitação específica:
	1. Diretório onde atualmente executa o software servidor
	2. Hora atual no servidor e na mesma resposta tempo total de execução do servidor

2 Implementação
A implementação de tal serviço deverá ser realizada utilizando-se comunicação Inter-Processos por meio de
streams TCP. O modelo arquitetural a ser utilizado deverá ser o cliente/servidor.
O servidor deverá estar apto a atender \ao mesmo tempo" 10 clientes.
Lembre-se da necessidade da criação do protocolo request/reply da camada de aplicação.
O modelo de desenvolvimento deverá considerar a necessidade de uma interação entre cliente e servidor,
iniciada pelo servidor, para autenticação. Apenas após a autenticação (pode ser usuáario e senha). Nesse mo-
mento o servidor deverá enviar sinalização ao cliente informando-o que pode começar a transmitir as requisições.
O servidor deverá levar em conta threads, não são pela necessidade de atendimento \ao mesmo tempo" de
até 10 clientes, mas também por que uma thread específica será responsável pelo mecanismo de autenticação.
Uma segunda Thread deverá ser responsável pela interação propriamente dita com o cliente. A Fig. 1 ilustra o
modelo de implementação.

3 Prazos
Entrega dos executáveis, do código fonte do cliente e servidor, bem como código impresso dia 10/04/2012.


----------------------------------------------------
- Java 7