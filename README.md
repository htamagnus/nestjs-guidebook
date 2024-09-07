<h2>Layer Architecture (arquitetura em camadas):</h2>

![image](https://github.com/user-attachments/assets/69754e3f-9c01-4833-bbe9-7174190eba7e)


**1. Controllers (Routes)**:
- **Função:** São responsáveis por lidar com as requisições HTTP que chegam. Um controller interpreta a requisição, identifica qual rota foi chamada e direciona a lógica para o serviço adequado.

- **Exemplo:** Quando uma rota como `/users` é acessada, o controller correspondente recebe a requisição, lida com parâmetros e body (se necessário) e, então, chama os serviços relacionados.


**2. Service Layer (Business Logic):**
- **Função:** Contém a lógica de negócios da aplicação. É aqui que estão as regras e processamentos principais que não estão diretamente ligados ao gerenciamento de dados ou ao tráfego de requisições. A Service Layer faz a ponte entre os Controllers e o Data Access Layer.

- **Exemplo:** Ao receber a requisição de um controller, o service executa as regras de negócio, como validação de dados, cálculos ou transformações, antes de chamar a camada de acesso a dados para obter ou salvar informações.

**3. Data Access Layer (ODM):**

- **Função:** Esta camada é responsável pela interação direta com o banco de dados. Em uma aplicação NestJS, essa camada geralmente faz uso de Object-Document Mapping (ODM) ou Object-Relational Mapping (ORM) para comunicar-se com o banco de dados, seja ele NoSQL ou SQL.

- **Exemplo:** Se um serviço precisa acessar um usuário do banco de dados, ele chama o repositório responsável por essa entidade na Data Access Layer, que se comunica com o banco de dados para buscar, salvar ou atualizar os dados.

## Como as camadas se conectam:

- **Controllers** chamam os Services para lidar com as requisições e lógica de negócios.

- **Services** acessam a Data Access Layer para manipular os dados no banco de dados.

A **Data Access Layer** executa as operações diretamente no banco de dados e retorna os dados para a Service Layer, que, por sua vez, os envia de volta ao Controller, fechando o ciclo.

---