![descrição](./img/logo.png)

# Projeto de Documentação

## :memo: Descrição do Projeto
<p id="descricaoprojeto" align="left">Um arquivo README é uma parte essencial de qualquer projeto de software, oferecendo informações cruciais para desenvolvedores, colaboradores, PO's entre outros. Ele atua como um guia seja incial para entender o projeto, sua finalidade e como utilizá-lo. Neste guia, discutiremos como criar ou melhorar a documentação em seu projeto, abordando cada seção considerada necessária do arquivo README de maneira clara e eficaz.

Lembre-se de que um README bem elaborado não apenas torna o projeto mais acessível, mas também ajuda novos integrantes, expões padrões e sua organização. Invista tempo na criação de um README informativo e organizado para maximizar o valor do projeto em que você atual.
</p>

![Badge](https://img.shields.io/badge/README-%237159c1?style=for-the-badge&logo=ghost)

## :bookmark_tabs: Tabela de Conteúdo

<ul id="tabelaconteudo" align="left">
  <li><a href="#descricaoprojeto">Descrição do Projeto</a></li>
  <li><a href="#statusprojeto">Status do Projeto</a></li>
  <li><a href="#tabelaconteudo">Tabela de Conteúdo</a></li>
  <li><a href="#tecnologias">Tecnologias</a></li>
</ul>

## :rocket: Status do Projeto
<h4 id="statusprojeto" align="left"> 
    Em construção... 
</h4>

## :white_check_mark: Features
- [x] Cadastro de usuário
- [x] Cadastro de cliente
- [ ] Cadastro de produtos

## Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:
[Git](https://git-scm.com) e [Dotnet 6](https://dotnet.microsoft.com/pt-br/download/dotnet/6.0). 

Além disto é bom ter um editor para trabalhar com o código como [VSCode](https://code.visualstudio.com/)

### 🔨 Rodando o Back End (servidor)

```bash
# Clone este repositório
$ git clone <path do repositório >

# Acesse a pasta raiz do projeto no terminal/cmd
$ cd meu-projeto

# Instale as dependências
$ dotnet restore

# Execute a aplicação de api em modo de desenvolvimento
$ dotnet run --project src/adapter/provider/meu-projeto-api/meu-projeto-api.csproj

# O servidor inciará na porta:8080 - acesse <http://localhost:8080>
```
### :globe_with_meridians: Mapa do Projeto
<p id="mapaprojeto" align="left">Abaixo segue a estrutura de pastas e suas definições:</p>
 
```bash
├── src					                      // Pasta raiz com a estrutura do projeto
│  └── Adapter                        // Pasta para criar os serviços de comunicação / Ports & Adpters
│       └── Provider                  // Pasta com o projeto de API
│   └── Core                         	// Pasta com os princípais serviços do projeto
│       └── Application               // Pasta com o projeto para o mapeamento das entidades entre domain e serviços
│          └── Mapper                	// Pasta com os mappers entre viewmodel e entidade
│          └── ViewModel              // Pasta com os objetos de ViewModel / DTO
│       └── Domain                  	// Pasta com organização das entidades Domínio do projeto
│          └── Interfaces             // Pasta com os contratos expostos pelo Domínio
│          └── Models                	// Pasta com organização das Entidades e Serviços usando CQRS
│          	└── Commands              // Pasta com os comandos e handler CQRS
│          	└── Entities              // Pasta com entidades
│          	└── Events                // Pasta com os eventos
│          └── Query                	// Pasta com as querys e handler CQRS
│   └── Infrastructure                // Pasta com projeto de infrastructure e configurações de acesso a banco
│       └── Mappings                  // Pasta com Mappings usando fluent das entidades para o banco
│       └── Migrations                // Pasta com as Migrations aplicadas / a serem aplicadas
│       └── Repository                // Pasta com contexto e configuração do objeto de repository das entidades
├── tests				                      // Pasta com projeto de testes unitários do microserviço
```
### 🛠 Tecnologias
As seguintes ferramentas foram usadas na construção do projeto:

- [Dotnet](https://dotnet.microsoft.com/pt-br/download/dotnet/6.0)
- [C#](https://dotnet.microsoft.com/pt-br/download/dotnet/6.0)
- [RabbitMQ](https://www.rabbitmq.com/)
- [SQL Server](https://www.microsoft.com/pt-br/sql-server/sql-server-downloads)
