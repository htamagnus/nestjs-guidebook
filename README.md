<h2>Layer Architecture (arquitetura em camadas)</h2>

![image](https://github.com/user-attachments/assets/69754e3f-9c01-4833-bbe9-7174190eba7e)


1. Controllers (Routes):
- Função: São responsáveis por lidar com as requisições HTTP que chegam. Um controller interpreta a requisição, identifica qual rota foi chamada e direciona a lógica para o serviço adequado.
- Exemplo: Quando uma rota como /users é acessada, o controller correspondente recebe a requisição, lida com parâmetros e body (se necessário) e, então, chama os serviços relacionados.

---

2. 