# Sistema de Gestão de Cursos
Este projeto é um Sistema de Gestão de Cursos que visa simplificar a administração de cursos, matrículas e pessoas (estudantes e docentes). A estrutura foi desenvolvida com Node.js e Sequelize, proporcionando uma base sólida para o desenvolvimento de aplicativos web.

## Características Principais
- Arquitetura Orientada a Objetos: Os serviços (Services) e controladores (Controllers) foram organizados seguindo princípios de orientação a objetos para maximizar a reutilização de código e facilitar a manutenção.

- Estrutura de Rotas Modulares: As rotas foram divididas por entidade (Pessoas, Categorias, Cursos, Matrículas), proporcionando uma estrutura clara e modular.

- Migrações e Seeders: Utilização de migrações e seeders para facilitar a configuração inicial do banco de dados, permitindo uma fácil reprodução do ambiente.

## Instalação
1. Clone o repositório: git clone https://github.com/seu-usuario/seu-projeto.git
2. Instale as dependências: npm install
3. Configure o banco de dados no arquivo .sequelizerc e src/config/config.json
4. Execute as migrações do banco de dados: npx sequelize-cli db:migrate
5. Execute os seeders para popular o banco de dados: npx sequelize-cli db:seed:all
 
## Estrutura de Diretórios
A estrutura de diretórios foi organizada para fornecer uma visão clara do projeto:

- src/controllers: Controladores responsáveis por receber as requisições HTTP e interagir com os serviços.
- src/models: Modelos Sequelize que definem a estrutura das tabelas do banco de dados.
- src/routes: Rotas organizadas por entidade, conectando os controladores aos endpoints da API.
- src/services: Serviços que encapsulam a lógica de negócios e interagem diretamente com os modelos Sequelize.

## Uso
Para iniciar o servidor, execute o seguinte comando:

```
npm start
```
O servidor estará disponível em http://localhost:3000.

## Endpoints
### Pessoas
- GET /pessoas: Retorna todas as pessoas.
- GET /pessoas/:id: Retorna uma pessoa específica.
- POST /pessoas: Cria uma nova pessoa.
- PUT /pessoas/:id: Atualiza uma pessoa existente.
- DELETE /pessoas/:id: Exclui uma pessoa específica.
- GET /pessoas/:estudanteId/matriculas: Retorna as matrículas de um estudante.
- POST /pessoas/:estudanteId/matriculas: Cria uma nova matrícula para um estudante.
### Categorias
- GET /categorias: Retorna todas as categorias.
- GET /categorias/:id: Retorna uma categoria específica.
- POST /categorias: Cria uma nova categoria.
- PUT /categorias/:id: Atualiza uma categoria existente.
- DELETE /categorias/:id: Exclui uma categoria específica.
### Cursos
- GET /cursos: Retorna todos os cursos.
- GET /cursos/:id: Retorna um curso específico.
- POST /cursos: Cria um novo curso.
- PUT /cursos/:id: Atualiza um curso existente.
- DELETE /cursos/:id: Exclui um curso específico.
### Matrículas
- GET /matriculas: Retorna todas as matrículas.
- GET /matriculas/:id: Retorna uma matrícula específica.
- POST /matriculas: Cria uma nova matrícula.
- PUT /matriculas/:id: Atualiza uma matrícula existente.
- DELETE /matriculas/:id: Exclui uma matrícula específica.

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

