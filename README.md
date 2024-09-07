<h2>Layer Architecture (arquitetura em camadas):</h2>

![image](https://github.com/user-attachments/assets/69754e3f-9c01-4833-bbe9-7174190eba7e)


**1. Controllers (Routes)**:
- **Função:** São responsáveis por lidar com as requisições HTTP que chegam. Um controller interpreta a requisição, identifica qual rota foi chamada e direciona a lógica para o serviço adequado.

- **Exemplo:** Quando uma rota como `/users` é acessada, o controller correspondente recebe a requisição, lida com parâmetros e body (se necessário) e, então, chama os serviços relacionados.

---

**2. Service Layer (Business Logic):**
- **Função:** Contém a lógica de negócios da aplicação. É aqui que estão as regras e processamentos principais que não estão diretamente ligados ao gerenciamento de dados ou ao tráfego de requisições. A Service Layer faz a ponte entre os Controllers e o Data Access Layer.

- **Exemplo:** Ao receber a requisição de um controller, o service executa as regras de negócio, como validação de dados, cálculos ou transformações, antes de chamar a camada de acesso a dados para obter ou salvar informações.