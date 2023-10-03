# Dev_Web_Lista03
Lista 3 de atividade de Desenvolvimento Web - 4° Período Uniaraxá

<div>
    <h1>Lista 3 de atividades:</h1>
    <h3>Questão 1: Em sala no início da disciplina criamos e comentamos que nossa API estava com muitas responsabilidades( regras de negócio , validações, persistência) , ferindo assim qual princípio? Descreva o princípio e o que a partir de então começamos a fazer para corrigir isso?.</h3>
      <p>A situação em que a API possui muitas responsabilidades, incluindo regras de negócio, validações e persistência, está ferindo o princípio da Responsabilidade Única, que faz parte do conjunto de princípios conhecido como SOLID. O Princípio da Responsabilidade Única (Single Responsibility Principle - SRP) afirma que uma classe deve ter apenas um motivo para mudar, ou seja, ela deve ter apenas uma responsabilidade.</p>

<p>Para corrigir isso, começamos a adotar o padrão de arquitetura em camadas, onde cada camada tem uma responsabilidade bem definida. As regras de negócio foram movidas para a camada de Domain, as operações de persistência para a camada de Data, e as responsabilidades relacionadas à lógica da aplicação e à interação com as camadas inferiores foram separadas na camada de Application. A camada de API passou a ser responsável principalmente pela exposição dos serviços através de endpoints HTTP e pela manipulação de requisições e respostas, sem carregar a lógica de negócios ou persistência.</p>
	
  <br>
  <br>
    <h3>Questão 2: Em sala no início da disciplina criamos e comentamos que nossa API estava com muitas responsabilidades( regras de negócio , validações, persistência) , ferindo assim qual princípio? Descreva o princípio e o que a partir de então começamos a fazer para corrigir isso?:</h3>
	  <p>Camada de Domain: Nessa camada, definimos e implementamos as entidades de negócio e as regras de domínio da aplicação. É onde as classes com propriedades de set privado são comuns, garantindo a encapsulação dos dados e fornecendo uma interface controlada para acessá-los.</p>
	<p>Camada de Data: Responsável pela interação com o banco de dados ou qualquer mecanismo de armazenamento de dados. Aqui, definimos os repositórios e as classes de acesso aos dados.</p>
	<p>Camada de Application: É onde reside a lógica da aplicação, incluindo serviços que coordenam as operações e interagem com as camadas de Domain e Data. Também é onde os DTOs (Data Transfer Objects) podem ser usados para transferir dados entre a camada de API e a camada de Domain sem expor detalhes desnecessários.</p>
	<p>Camada de API: A camada de API é responsável por lidar com as solicitações HTTP, gerenciar autenticação e autorização, e expor os endpoints para os clientes. Ela utiliza os serviços da camada de Application para atender às solicitações e fornecer respostas adequadas.</p>
	
  <br>
  <br>
    <h3>Questão 3: Na camada de Domain criamos classes cujas propriedades são com set privado. Descreva, vantagem de usar dessa forma destacando como fizemos em sala com o produto..</h3>
	<p>A vantagem de criar classes no Domain com propriedades de set privado está relacionada à encapsulação e controle sobre os dados. Ao tornar as propriedades privadas e disponibilizar apenas métodos públicos para modificar essas propriedades (métodos conhecidos como getters e setters), você ganha controle sobre como os dados são acessados e modificados. Isso oferece benefícios, como:</p>
	<p>Controle: Você pode aplicar lógica de validação, garantindo que os dados estejam sempre em um estado válido antes de serem modificados.</p>
	<p>Encapsulação: Os detalhes de implementação dos campos de dados são ocultos, tornando mais fácil realizar mudanças na estrutura interna da classe sem afetar os consumidores da classe.</p>
	<p>Manutenibilidade: Facilita a manutenção do código, pois você sabe exatamente onde os dados são alterados e quem é responsável por isso.</p>
	<p>Um exemplo disso, que pode ter sido discutido em sala com o produto, é ter um método SetPrice(decimal price) em vez de uma propriedade pública Price. Isso permite que você execute validações e lógica de negócios sempre que o preço for definido, garantindo que ele esteja dentro dos limites apropriados.</p>
 
  <br>
  <br>
    <h3>Questão 4: Na camada de applicattion na classe service (de serviço) fizemos o que chamamos de injeção de dependência, descreva por que utilizamos essa técnica e como isso pode ser uma vantagem?</h3>
      <p>A técnica de injeção de dependência é utilizada na camada de Application para promover a separação de responsabilidades e facilitar a manutenção e teste do código. Ela envolve a passagem das dependências necessárias para uma classe ou serviço de fora da classe, em vez de a classe criá-las internamente.</p>
<p>As vantagens da injeção de dependência incluem:</p>
<p>Desacoplamento: As classes não precisam mais criar suas próprias dependências, reduzindo o acoplamento entre as classes. Isso torna o código mais flexível e mais fácil de modificar.</p>
<p>Testabilidade: Facilita a criação de testes unitários, pois você pode injetar facilmente objetos de simulação ou objetos mock para testar o comportamento da classe.</p>
<p>Reutilização: As dependências podem ser reutilizadas em várias partes do código sem duplicação de instâncias.</p>
<p>Facilidade de configuração: Você pode configurar as dependências externamente, tornando mais fácil a troca de implementações de dependências sem alterar o código da classe que as utiliza.</p>
<p>Em resumo, a injeção de dependência é uma técnica que promove um código mais limpo, flexível e testável, facilitando o desenvolvimento e a manutenção de software.</p>
      
  <br>
  <br>     
</div>
