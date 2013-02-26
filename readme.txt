***********
M�dulo de integra��o PagSeguro para PrestaShop
v.1.0
***********


= Descri��o =

Este m�dulo tem por finalidade integrar o PagSeguro como meio de pagamento dentro da plataforma PrestaShop.


= Requisitos =

Dispon�vel para as vers�es 1.5.2 e 1.5.3.1 do PrestaShop.


= Instala��o =

1a. Certifique-se de que n�o h� instala��o de outros m�dulos para o PagSeguro em seu sistema;
2a. Para instalar esse m�dulo, v� at� a op��o M�dulos, na �rea administrativa, clique em Adicionar novo m�dulo e importe esse m�dulo compactado;
3a. Acesse a categoria Pagamentos & Gateways, procure pelo m�dulo PagSeguro e fa�a a instala��o.

Alternativamente, � poss�vel fazer a instala��o da seguinte maneira:

1b. Certifique-se de que n�o h� instala��o de outros m�dulos para o PagSeguro em seu sistema;
2b. Descompacte o conte�do do arquivo zip e copie a pasta 'pagseguro' para dentro da pasta 'modules' em sua instala��o PrestaShop;
3b. Acesse a categoria Pagamentos & Gateways, procure pelo m�dulo PagSeguro e fa�a a instala��o;

= Configura��o =

Ap�s instalado o m�dulo, � necess�rio que se fa�a algumas configura��es para que efetivamente seja poss�vel utilizar-se dele. Essas configura��es est�o dispon�veis na op��o Configurar do m�dulo.

	- email: E-mail cadastrado no PagSeguro
	- token: Token cadastrado no PagSeguro
	- url de redirecionamento: url utilizada para se fazer redirecionamento ap�s o cliente realizar a efetiva��o da compra no ambiente do PagSeguro. Pode ser uma url do pr�prio sistema ou uma outra qualquer de interesse do vendedor
	- charset: codifica��o do sistema (ISO-8859-1 ou UTF-8)
	- log: diret�rio a partir da ra�z do sistema, onde se deseja criar o arquivo de log . Ex.: /logs/log_pagseguro.log


= Changelog =

v1.0
Vers�o inicial. Integra��o com API de checkout do PagSeguro.


= NOTAS =
	
	- Certifique-se que o email e o token informados estejam relacionados a uma conta que possua o perfil de vendedor ou empresarial.
	- Certifique-se que tenha definido corretamente o charset de acordo com a codifica��o (ISO-8859-1 ou UTF-8) do seu sistema. Isso ir� prevenir que as transa��es gerem poss�veis erros ou quebras ou ainda que caracteres especiais possam ser apresentados de maneira diferente do habitual.
	- Para que ocorra normalmente a gera��o de logs pelo plugin, certifique-se que o diret�rio e o arquivo de log tenham permiss�es de leitura e escrita.
	- O PagSeguro somente aceita pagamento utilizando a moeda Real brasileiro (BRL).