# 🇳 Boas-vindas ao repositório do projeto All For One! 1️⃣

<!-- # Como ficou o projeto ?

# Link da Aplicação -->

# Habilidades necessárias

<details>
  <summary><strong>:memo: Habilidades</strong></summary><br />

  Neste projeto pude desenvolver consultas que envolvem:

1. SELECT, DISTINCT, LIMIT e OFFSET
2. ORDER BY, COUNT, WHERE
3. Operadores Matemáticos, Operadores Lógicos, IS, NOT
4. LIKE, BETWEEN, IN, Datas, INSERT, UPDATE, DELETE

</details>

# O que é a aplaicação ?

<details>
  <summary><strong>:convenience_store: Desenvolvimento </strong></summary><br />

  Fiz um projeto com o codinome All For One em que pratiquei todos os conceitos de SQL já ensinados até aqui. Porém, usei um banco de dados totalmente diferente, então dei tchau para o sakila e fiz boas vindas ao Northwind, que foi usado neste projeto.
</details>

# Orientações

<details>
  <summary><strong>:whale: Rodando no Docker vs Localmente</strong></summary><br />

  ## Com Docker

  **:warning: Antes de começar, seu docker-compose precisa estar na versão 1.29 ou superior. [Veja aqui](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04-pt) ou [na documentação](https://docs.docker.com/compose/install/) como instalá-lo. No primeiro artigo, você pode substituir onde está com `1.26.0` por `1.29.2`.**

  > :information_source: Rode os serviços `node` e `db` com o comando `docker-compose up -d`.
  - Lembre-se de parar o `mysql` se estiver usando localmente na porta padrão (`3306`), ou adapte, caso queria fazer uso da aplicação em containers
  - Esses serviços irão inicializar um container chamado `all_for_one` e outro chamado `all_for_one_db`.
  - A partir daqui você pode rodar o container `all_for_one` via CLI ou abri-lo no VS Code.

  > :information_source: Use o comando `docker exec -it all_for_one bash`.
  - Ele te dará acesso ao terminal interativo do container criado pelo compose, que está rodando em segundo plano.
  - As credencias de acesso ao banco de dados estão definidas no arquivo `docker-compose.yml`, e são acessíveis no container através das variáveis de ambiente `MYSQL_USER` e `MYSQL_PASSWORD`. 💡

  > :information_source: Instale as dependências [**Caso existam**] com `npm install`. (Instale dentro do container)

  - **:warning: Atenção:** Caso opte por utilizar o Docker, **TODOS** os comandos disponíveis no `package.json` (npm start, npm test, npm run dev, ...) devem ser executados **DENTRO** do container, ou seja, no terminal que aparece após a execução do comando `docker exec` citado acima.

  - **:warning: Atenção:** O **git** dentro do container não vem configurado com suas credenciais. Ou faça os commits fora do container, ou configure as suas credenciais do git dentro do container.
  
  - **:warning: Atenção:** Caso você esteja usando macOS e ao executar o `docker-compose up -d` se depare com o seguinte erro:

  ~~~bash
  The Compose file './docker-compose.yml' is invalid because:
  Unsupported config option for services.db: 'platform'
  Unsupported config option for services.node: 'platform'
  ~~~

> Foram encontradas 2 possíveis soluções para este problema:
> 1. Você pode adicionar manualmente a option `platform: linux/amd64` no service do banco de dados no arquivo docker-compose.yml do projeto, mas essa é uma solução local e você deverá reproduzir isso para os outros projetos.
> 2. Você pode adicionar manualmente nos arquivos .bashrc, .zshenv ou .zshrc do seu computador a linha `export DOCKER_DEFAULT_PLATFORM=linux/amd64`, essa é uma solução global.
> As soluções foram com base [nesta fonte](https://stackoverflow.com/a/69636473).

  - ✨ **Dica:** A extensão `Remote - Containers` (que estará na seção de extensões recomendadas do VS Code) é indicada para que você possa desenvolver sua aplicação no container Docker direto no VS Code, como você faz com seus arquivos locais.

  ![remote-containers](./images/remote-container.png)

  <br />

  ## Sem Docker

  > :information_source: Instale as dependências [**Caso existam**] com `npm install`

  - **:warning: Atenção:** Não rode o comando npm audit fix! Ele atualiza várias dependências do projeto, e essa atualização gera conflitos com o avaliador.

  - **✨ Dica:** Para rodar o projeto desta forma, obrigatoriamente você deve ter o `node` instalado em seu computador.
  - **✨ Dica:** O avaliador espera que a versão do `node` utilizada seja a 16.

  <br/>
</details>

# Como rodar na sua máquina ? 

<details>
  <summary><strong>‼️ Teste em sua máquina</strong></summary><br />

  1. Clone o repositório

  - Use o comando: `git clone git@github.com:Matheusfull/Project-18-Back-end-all-for-one.git`.
  - Entre na pasta do repositório que você acabou de clonar:
    - `cd Project-18-Back-end-all-for-one`

  2. Instale as dependências

  - `npm install`.

  3. Testando os Comandos :

  - `Os comandos estão na raiz do projeto, com isso, só utilizá-los no seu banco de dados para testar`.

  </details>

<!-- Olá, Tryber!
Esse é apenas um arquivo inicial para o README do seu projeto no qual você pode customizar e reutilizar todas as vezes que for executar o trybe-publisher.

Para deixá-lo com a sua cara, basta alterar o seguinte arquivo da sua máquina: ~/.student-repo-publisher/custom/_NEW_README.md

É essencial que você preencha esse documento por conta própria, ok?
Não deixe de usar nossas dicas de escrita de README de projetos, e deixe sua criatividade brilhar!
:warning: IMPORTANTE: você precisa deixar nítido:
- quais arquivos/pastas foram desenvolvidos por você; 
- quais arquivos/pastas foram desenvolvidos por outra pessoa estudante;
- quais arquivos/pastas foram desenvolvidos pela Trybe.
-->

<!--
1 - Boas vindas
2 - imagem/gif da aplicação
3 - link do deploy
4 - Habilidades necessárias para realizar o projeto
5 - O que é aquele projeto
6 - Como baixar e rodar na máquina
-->