-------------------------------------------------
M�dulo de integra��o PagSeguro para PrestaShop 
v1.1
-------------------------------------------------


= Descri��o =

Este m�dulo tem por finalidade integrar o PagSeguro como meio de pagamento dentro da plataforma PrestaShop.


= Requisitos =

Dispon�vel para as vers�es 1.5.2 e 1.5.3.1 do PrestaShop.

PHP 5.1.6+
SPL
cURL
DOM


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

	- email: e-mail cadastrado no PagSeguro
	- token: token cadastrado no PagSeguro
	- url de redirecionamento: ao final do fluxo de pagamento no PagSeguro, seu cliente ser� redirecionado de volta para a p�gina de confirma��o em sua loja ou ent�o para a URL que voc� informar neste campo. Para ativar o redirecionamento ao final do pagamento � preciso ativar o servi�o de Pagamentos via API.
		- https://pagseguro.uol.com.br/integracao/pagamentos-via-api.jhtml
	- charset: codifica��o do seu sistema (ISO-8859-1 ou UTF-8)
	- log: ativa/desativa a gera��o de logs
		- diret�rio a partir da ra�z de instala��o do PrestaShop onde se deseja criar o arquivo de log. Ex.: /logs/log_pagseguro.log
	- Notifica��es de Transa��o
		- Para receber e processar automaticamente os novos status das transa��es com o PagSeguro voc� deve ativar o servi�o de Notifica��o de Transa��es. Basta acessar o painel de controle de sua conta PagSeguro e informe a url que aparece nas configura��es do m�dulo;
		- https://pagseguro.uol.com.br/integracao/notificacao-de-transacoes.jhtml

		
= Changelog =

	- v1.1
	- Integra��o com API de Notifica��o do PagSeguro
	- Adequa��o da licen�a
	- Adi��o da funcionalidade de notifica��o
	- Adi��o de tratamento para duplo espa�o no nome do comprador
	- Adi��o de link para fazer cadastro no Pagseguro
	- Altera��o da finaliza��o do pagamento. Agora, realizado dentro do ambiente do PagSeguro
	- Corre��o de quebra do layout padr�o do Prestashop na confirma��o da compra
	- Corre��o para recupera��o de valores de embrulho e de descontos
	- Corre��o de redirecionamento de p�gina para url rewrite do PrestaShop

	- v1.0
	- Vers�o inicial. Integra��o com API de checkout do PagSeguro


= Notas =
	
	- Certifique-se que o email e o token informados estejam relacionados a uma conta que possua o perfil de vendedor ou empresarial
	- Certifique-se que tenha definido corretamente o charset de acordo com a codifica��o (ISO8859-1 ou UTF8) do seu sistema. Isso ir� prevenir que as transa��es gerem poss�veis erros ou quebras ou ainda que caracteres especiais possam ser apresentados de maneira diferente do habitual
	- Para que ocorra normalmente a gera��o de logs pelo plugin, certifique-se que o diret�rio e o arquivo de log tenham permiss�es de leitura e escrita;
	- O PagSeguro somente aceita pagamentos utilizando a moeda Real brasileiro (BRL)
