-------------------------------------------------
M�dulo de integra��o PagSeguro para PrestaShop 
v1.1
-------------------------------------------------


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
	- url de redirecionamento: url utilizada para se fazer redirecionamento ap�s o cliente realizar a efetiva��o da compra no ambiente do PagSeguro. Pode ser uma url do pr�prio sistema ou uma outra qualquer de interesse do vendedor.
	- charset: codifica��o do sistema (ISO-8859-1 ou UTF-8)
	- log: diret�rio a partir da ra�z do sistema, onde se deseja criar o arquivo de log . Ex.: /logs/log_pagseguro.log
	
	Notifica��es de Transa��o
	
		- Essa funcionalidade tem por objetivo persistir no sistema as atualiza��es de status das compras realizadas atrav�s do PagSeguro. Essa atualiza��o � transparente para o sistema. � necess�rio somente que seja ativada a funcionalidade de Notifica��es de Transa��o no PagSeguro e informar a url que � exibida no ambiente de configura��o do m�dulo do PagSeguro dentro do sistema.
		- Para configurar esses dados no PagSeguro, acesse https://pagseguro.uol.com.br/integracao/notificacao-de-transacoes.jhtml.
		- Uma vez configuradas essas informa��es no PagSeguro, o sistema passar� a receber e processar automaticamente os novos status das transa��es com o PagSeguro, o que d� ao vendedor e ao comprador, uma maior facilidade para acompanhar os status de suas vendas e compras respectivamente, dentro do pr�prio site.

		
= Changelog =

	- Vers�o 1.1
	- Integra��o com API de Notifica��o do PagSeguro.
	- Adequa��o da licen�a.
	- Adi��o da funcionalidade de notifica��o.
	- Adi��o de tratamento para duplo espa�o no nome do comprador.
	- Adi��o de link para fazer cadastro no Pagseguro.
	- Altera��o da finaliza��o do pagamento. Agora, realizado dentro do ambiente do PagSeguro.
	- Corre��o de quebra do layout padr�o do Prestashop na confirma��o da compra.
	- Corre��o para recupera��o de valores de embrulho e de descontos.
	- Corre��o de redirecionamento de p�gina para url rewrite do PrestaShop.


= Notas =
	
	- Certifique-se que o email e o token informados estejam relacionados a uma conta que possua o perfil de vendedor ou empresarial;
	- Certifique-se que tenha definido corretamente o charset de acordo com a codifica��o (ISO8859-1 ou UTF8) do seu sistema. Isso ir� prevenir que as transa��es gerem poss�veis erros ou quebras ou ainda que caracteres especiais possam ser apresentados de maneira diferente do habitual.
	- Para que ocorra normalmente a gera��o de logs pelo plugin, certifique-se que o diret�rio e o arquivo de log tenham permiss�es de leitura e escrita.
	- O PagSeguro somente aceita pagamento utilizando a moeda Real brasileiro (BRL).