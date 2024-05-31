# API Voll Med
***
## Índice
- [Introdução](#introdução)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Configurações e Dependências](#configurações-e-dependências)
- [Funcionalidades da API](#funcionalidades-da-api)
- [Validações e Padrões de Projeto](#validações-e-padrões-de-projeto)
- [Documentação da API](#documentação-da-api)
- [Testes Automatizados](#testes-automatizados)
- [Segurança com Spring Security](#segurança-com-spring-security)
- [Gerenciamento de Build e Deploy](#gerenciamento-de-build-e-deploy)
- [Conclusão](#conclusão)
- [Agradecimentos](#agradecimentos)
***

## Introdução
A API da Voll Med foi desenvolvida para atender as necessidades de uma clínica médica fictícia. A empresa Voll Med possui uma clínica que precisa de um aplicativo para monitorar o cadastro de médicos, pacientes, além do agendamento e cancelamento de consultas.

## Estrutura do Projeto
A aplicação foi organizada em três principais pacotes:
- **Controller**
- **Domain**
- **Infra**

No pacote `domain`, temos classes relacionadas aos médicos e pacientes. No pacote `infra`, estão as configurações de infraestrutura, incluindo frameworks e bibliotecas usadas no projeto.

## Configurações e Dependências
Utilização de módulos como Web, Validação e Spring Data JPA. Bibliotecas adicionais como o driver do MySQL, Flyway e Lombok. Configurações do projeto Spring Boot.

## Funcionalidades da API
- **Cadastro de Médicos:** Permite criar, ler, atualizar e deletar informações de médicos.
- **Cadastro de Pacientes:** Permite criar, ler, atualizar e deletar informações de pacientes.
- **Agendamento de Consultas:** Permite agendar consultas médicas.
- **Cancelamento de Consultas:** Permite cancelar consultas agendadas.

Este aplicativo foi projetado para ser fácil de usar, permitindo que os usuários realizem operações de CRUD tanto para médicos quanto para pacientes, além de gerenciar o agendamento e cancelamento das consultas de forma eficiente.


Padronização dos retornos dos métodos da API com `ResponseEntity`, aplicando boas práticas do protocolo HTTP.

## Validações e Padrões de Projeto
Isolamento de validações usando validadores injetados por polimorfismo com interface e List. Aplicação dos princípios do SOLID para manter o código fácil de entender e de manter.

No pacote `infra > exception`, foi criada a classe `TratadorDeErros` seguindo o conceito de Controller Advice do Spring Boot para tratamento de erros, simplificando o manejo de exceções.

## Documentação da API
Aplicado com SpringDoc ao projeto para gerar documentação. Com a utilização do Swagger para acessar a interface gráfica, simular requisições e incluir cabeçalhos de autenticação JWT. A documentação gerada é útil para equipes de desenvolvimento de front-end e mobile.

## Testes Automatizados
Testes automatizados para componentes do Spring, como Repository e Controller. Criamos testes para `MedicoRepositoryTeste`, configurando um banco de dados real (MySQL) para testes.

Para testes de Controller, utilizamos `MockMvc` e `JacksonTester` para validar JSONs na API, criando cenários de teste e garantindo a qualidade do código.

## Segurança com Spring Security
Adicionamos o Spring Security ao projeto, implementando autenticação e autorização por tokens JWT. Configuramos o Spring Security para usar autenticação stateless e hashing de senha com BCrypt.

## Gerenciamento de Build e Deploy
Gerando o build da aplicação via Maven, criando um arquivo `.jar` na pasta `target > test-classes`. Configuração dos arquivos de properties para produção e simulamos um deploy em ambiente de produção, incluindo comandos e parâmetros necessários.

## Conclusão
Habilidades adquiridas com esta API:
- Criação de uma API do zero com o Spring usando o Spring Initializr.
- Implementação de funcionalidades, controller e repository.
- Uso do Flyway para migrations.
- Implementação de CRUD com validações.
- Aplicação de testes automatizados.

## Agradecimentos
Gostaria de agradecer à [Alura](https://www.alura.com.br) e à [Oracle Next Education](https://www.oracle.com/br/education/oracle-next-education/) pelo suporte e pelos recursos fornecidos durante todo o curso. O conhecimento adquirido foi inestimável para o meu desenvolvimento como desenvolvedora.
