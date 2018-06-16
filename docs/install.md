

## Requistos de Instalação

A instalação do CS precisa de uma conexão com a Internet para download de softwares e parametrização atualizada do sistema conforme dados do governo, o processo de instalação faz consulta a bancos de dados na Internet para validar por exemplo a cidade no qual você está instalando o sistema, também importa algumas tabelas importantes para que tenha sucesso na emissão de nota fiscal eletrônica.

Com base em divesos instalados e ambientes, desenvolvemos a seguinte abordagem de instalação que garantimos ser a mais simples e que será bem sucedida.

## Instalação do SQL Express

Somente é preciso instalar o SQL Express se não houver uma instalação funcionando da versão 2014 ou superior. Caso tenha o servidor instalado em outra máquina e acessível remotamente, você pode usa-lo sem problemas desde que possa se conectar ao usuário "sa".

Para instalar o SQL Express é preciso ficar atento aos requisitos e parâmetros de configuração do acesso:

* E preciso de 512MB ea 1GB de RAM, mais que um 1GB não fará diferença.
* 6.7GB de espaço livre em disco no C: no mínimo
* Usando o SQL Express nosso banco fica limitado a 10GB

Lembre-se que se você já tiver o SQL Express instalado e configurado para outra aplicação basta verificar se esta configuração atendem as necessidades do Comercial Simples, que são:

* Conexão por TCP/IP ativada
* Conexão pela pela porta 1433
* Usuário sa disponível
* Ter em mãos a senha do usuário "sa" ou então cria-las na instalação abaixo;

> Qualquer dúvida quantos as informações acima ou com o processo abaixo, entre em contato com (85) 985205490 para suporte.

Primeiro instale o SSMS (MicroSoft SQL Server Manager Studio), pois através dele iremos fazer a parametrização do SQL Express para receber as conexões do Comercial Simples. [Clique aqui e veja instruções em português no próprio site da Microsoft de como baixar e instalar o SSMS](https://docs.microsoft.com/pt-br/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017).

[Se desejar baixar diretamente o SSMS 2017 em português clique aqui.](https://go.microsoft.com/fwlink/?linkid=873126)

> A instalação do SSMS é bastante simples, basta seguir as instruções apresentada pelo software.

----

[Agora vamos baixar o *SQL Server 2017 Express com Advanced Services*, clicando aqui](https://www.microsoft.com/pt-br/sql-server/sql-server-editions-express), é importante observar que deve ser baixado a versão completa "Advance Serviuces", se quiser baixar a [versão em português diretamente clique aqui](https://go.microsoft.com/fwlink/?linkid=853017), repetindo, vc deve baixar a versão com serviços avançados: **SQL Server 2017 Express com Advanced Services**.

SE você optou pelo primeiro link e baixo o instalador generico ele irá lhe eprguntar qual tipo de instalação deseja fazer, então basta selecionar " SQL SErver 2017 Express com Advanced Services", lembrando que o SQL Server é uma instalação demorada, portanto tenha paciência e escolha um horário que você não terá que fazer outras instalações ou reiniciar seu computador.

Ele irá fazer um download de apróximadamente 800MB, e depois instalar automáticamente seu SQL Express.

CAso venha a ter algum erro durante o processo de instalação, certifique-se que seu windows está completamente atualizado e seja uma isntalação licenciada. E tente novamente.

A autenticação do SQL Express deve ser no modo  "Mixed", pois usaremos o usuário "sa", e nossa senha do banco de dados em instalação genêricas e didáticas como esta será "fullsrvadmin". 

Se já tem o SQL Express Instalado ou está usando o banco de dados em outro servidor, você precisa saber qual usuário usar e qual a senha. Veja que este usuário precisa ter autorização para criar e apagar seu próprio banco de dados.

Quando a tela da Central de Instalação do SQL Server abrir, selecione a primeira opção **"Nova Instalação Autonoma do SQL Server ou adicionar recursos a uma instalação existente"**.

Siga a instalção com o padrão ao chegar em "Seleção de Recursos", selecione "Serviços de Mecanismos de Banco de Dados", e clique em avançar.

Em configuração da Instância, apenas crie uma nova se não existir uma instância como nome **"SQL Express"**, clique em avançar.





### Configuração Instância 


## A Senha de Suporte

A senha de suporte é usada apenas na instalação, ela é importante para evitar que sejam feitas instalações sobre sistemas que já estão em funcionamento, ela é muito simples de ser obtida basta fazer o seguinte cálculo:

$$
primeira parte da senha de suporte = (dia atual + mês atual + 5) * 2
segunda parte da senha de suporte = \frac{dia atual + mês atual}{2}
$$

Por exemplo eu fazendo a instalação no dia 15 de junho, o calculo fica da seguinte forma:

$$
(16 + 6 + 5) * 2 = 54
(16 + 6) / 2 = 11
$$

Como pode ver na segunda parte deu fração para o meu caso, basta remover a parte fracionada, a senha fica então "5210", em caso de dúvida entre em contato pelo whatsapp (85) 985205490.

## A configuração do Banco de Dados

