GerenciadorLivro
================

Estudo Spring Security

A segurança para aplicações web é considerada um tópico de extrema criticidade atualmente, principalmente com o surgimento de vírus e formas de exploração de software cada vez mais sofisticada. A segurança é um elemento chave em qualquer projeto.

Leia mais em: Spring Security 3.1: Configuração e utilização em um exemplo web http://www.devmedia.com.br/spring-security-3-1-configuracao-e-utilizacao-em-um-exemplo-web/30112#ixzz38pAntQPv

Autenticação
A autenticação é um dos dois conceitos chaves quando estamos desenvolvendo aplicações seguras. O outro conceito é o de autorização que será visto posteriormente. A autenticação basicamente identifica quem está tentando solicitar um recurso.

No dia a dia estamos sempre lidando com a autenticação. Por exemplo, quando acessamos nosso e-mail precisamos fornecer um username e uma senha para acessá-lo. O e-mail, por sua vez, bate as informações conferindo se o username está na base de dados e confere a senha de acordo com o username. Algumas aplicações ao invés de usarem uma base de dados utilizam um servidor de diretório como o Microsoft Active Directory. Outra forma de autenticação que podemos encontrar é quando sacamos dinheiro numa máquina de autoatendimento no banco. Nesse caso precisamos inserir o nosso cartão e depois prover uma senha. Esse tipo de autenticação é bastante similar com a autenticação do e-mail com username e senha, porém o username está codificado no cartão magnético. Outra forma de autenticação é quando ligamos o carro. Apesar de ser diferente dos outros exemplos, essa também é uma forma de autenticação. Existem ainda diversas outras formas de autenticação que podem ser aplicadas a software ou hardware, cada um tem seus prós e contras que devem ser avaliados dependendo do tipo de aplicação que devemos desenvolver.

Um sistema de software pode ser dividido em dois tipos de nível de autenticação: autenticado ou não autenticado, este último também chamado de anônimo.

Em uma aplicação onde o usuário está anônimo, isto é o usuário não possui uma identidade no sistema, normalmente esse usuário não poderá solicitar um log no sistema, o que se torna importante, por exemplo, quando necessitamos saber quando fizemos uso de um serviço ou para descobrir se alguém está se aproveitando de algo que não a pertence. Usuários anônimos também não podem visualizar informações mais sensíveis como nome, endereço, cartões de crédito, ou possuir permissão para funcionalidades que possam manipular o estado ou informações do sistema.

Autorização
================
Autorização é o segundo conceito chave que é crucial na implementação e para o entendimento sobre a segurança de aplicações. Basicamente a autorização usa a informação que foi validada durante a autenticação para determinar se o acesso deveria ser concedido para um recurso em particular. Assim, as aplicações definem papéis aos usuários e baseando-se nos papéis desses usuários eles tem acesso a determinados recursos. Também devemos notar que para um usuário ter um papel ele deve estar autenticado, portanto deve passar pela autenticação no sistema.

Dessa forma a autorização envolve dois aspectos separados que devem ser combinados para descrever a acessibilidade do sistema. O primeiro é o mapeamento de um usuário autenticado para uma ou mais autorizações, chamado de papel. Por exemplo, um administrador de uma aplicação tem um nível de autorização, enquanto que um publicador dessa mesma aplicação tem outro nível de autorização. Provavelmente um publicador não conseguirá autorização para acessar um painel de administração. O segundo aspecto é a atribuição de autoridade para os recursos do sistema. Normalmente isso é feito quando o sistema está sendo desenvolvido através de uma declaração explicita no código ou através de parâmetros de configuração.

Os recursos que podem estar seguros são páginas web individuais, porções inteiras de um website ou porções de páginas individuais. Além disso, métodos de negócio também podem ser seguros.

Dizemos que quando um usuário tem permissão de acesso a um determinado recurso ele tem o acesso concedido, caso contrário o acesso é negado (denied).

Segurança na Base de Dados
================
Alguns desenvolvedores insistem com velhas práticas perigosas como gravar em arquivos de texto puro as senhas dos usuários. Este tipo de prática facilita o acesso à aplicação por usuários maliciosos.

As aplicações possuem desde dados pessoais até informações financeiras. Usuários não autorizados capaz de acessos a esses dados podem expor a empresa a roubo de identidade ou a adulteração, o que pode provocar danos aos usuários e também sérias complicações à empresa.

Por isso torna-se essencial entendermos a camada de acesso a base de dados do Spring Security para o armazenamento de credenciais. O Spring Security usa conectividade com JDBC.

SSL
================
O Spring Security oferece o protocolo SSL aos desenvolvedores. Este garante que a comunicação entre o browser do cliente e o servidor de aplicação está seguro contra muitos tipos de adulteração e espionagem.

Spring Security 3.1
================
Spring Security é um framework para Java ou JavaEE que provê autenticação, autorização e diversas outras funcionalidades para aplicações corporativas. Iniciado em 2003 por Ben Alex o Spring Security é distribuído sob a licença Apache Licence. Ele oferece diversos recursos que permitem muitas práticas comuns de segurança serem declaradas ou configuradas de uma forma direta.

Utilizando Spring Security 3.1 podemos aumentar a segurança da nossa aplicação das seguintes formas:

Segmentar os usuários do sistema em classes de usuário;
Atribuir níveis de autorização à papéis de usuário;
Atribuir papéis de usuário à classes de usuário;
Aplicar regras de autenticação globais para recursos de aplicação;
Aplicar regras de autorização à todos os níveis da arquitetura da aplicação;
Previnir tipos de ataques comuns que manipulam ou roubam sessões do usuário.
O Spring Security foi criado com o intuito de preencher uma grande lacuna que existia nas bibliotecas de segurança do Java. As bibliotecas para segurança mais conhecidas para Java, tais como Java Authentication and Authorization Service (JAAS) ou Java EE Security, são excelentes bibliotecas que oferecem funções de autorização e autenticação. No entanto, Spring Security empacota tudo numa única solução. Além disso, o Spring Security pode ser integrado com diferentes soluções corporativas.



Leia mais em: Spring Security 3.1: Configuração e utilização em um exemplo web http://www.devmedia.com.br/spring-security-3-1-configuracao-e-utilizacao-em-um-exemplo-web/30112#ixzz38pAxflMz