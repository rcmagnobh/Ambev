🧾 API de Gestão de Vendas
Este projeto é uma API RESTful desenvolvida em .NET Core, com arquitetura modular seguindo os princípios de Clean Code , SOLID , Clean Architecture e CQRS . 
Ele permite o gerenciamento de vendas, incluindo cadastro de clientes, itens vendidos, aplicação de regras de desconto e cancelamento de vendas ou itens.

Desenvolvido como parte de um projeto de avaliação técnica para desenvolvedores back-end.

✅ Funcionalidades da API
A API fornece um CRUD completo para gerenciamento de vendas, incluindo:

✅ Cadastro de vendas
📄 Lista de todas as vendas
🔍 Consulta de vendas por ID
🎯 Consulta com filtros
✏️ Atualização de itens de venda
🗑️ Remoção de uma venda inteira
🧹 Remoção de itens específicos da venda
🚫 Cancelamento de venda ou item
🧰 Tecnologias Utilizadas
ASP.NET Core (.NET 8)
PostgreSQL
Núcleo do Entity Framework
Mapeador automático
MediatR
Docker / Docker Compose
Arrogância
Serilog
xUnidade

🚀 Como Executar o Projeto
✅ Pré-requisitos

Docker
Docker Compose
📥 1. Clonar o Repositório
git clone https://github.com/rcmagnobh/Ambev.git
cd Ambev/src

🐳 2. Iniciar o Containers Docker
docker-compose up -d
Isso iniciará o banco de dados PostgreSQL na porta 5432.

🛠️ 3. Aplicar como Migrações
dotnet ef database update --project src/Ambev.DeveloperEvaluation.ORM
Esse comando criará automaticamente todas as tabelas no banco com base nas migrações existentes.

▶️4. Executar a API
Abra o projeto no Visual Studio, Rider ou VS Code e execute o projeto principal (geralmente o da WebApi).

📂 5. Acessar a documentação (Swagger)
Acesse no navegador:

http://localhost:8080/swagger

🧪 Testes
A lógica de criação de vendas e regras de negócio solicitadas no teste foram totalmente cobertas por testes unitários.

Para rodar os test:

dotnet test
As pastas de testes seguem esta organização:

Tests.Unit: Cobertura de regras de negócio
🗂️ Estrutura do Projeto
src/
├── Adapters/
│   ├── Drivers/          # Interfaces externas (WebApi)
│   └── Driven/           # Infraestrutura e repositórios (ORM)
├── Core/
│   ├── Application/      # Casos de uso, comandos, handlers
│   └── Domain/           # Entidades, enums, serviços e validações
├── Crosscutting/         # IoC, utilitários e configurações comuns
└── Tests/                # Testes unitários, funcionais e de integração

📌 Observações
A estrutura do banco de dados é criada automaticamente por meio de migrações.
JWT, MongoDB e Redis não foram utilizados neste projeto.

Todas as respostas da API seguem um padrão comum (envolvendo ApiResponsee ApiResponseWithData).

👨‍💻 Autor
Desenvolvido por Rodrigo Magno, como parte de um processo seletivo técnico.
