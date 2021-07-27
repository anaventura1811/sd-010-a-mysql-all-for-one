### MySQL All For One Project 

Este é o primeiro projeto do Módulo de Desenvolvimento Back-End da Trybe. 

# Sumário

- [Habilidades](#habilidades)
- [Data de entrega](#data-de-entrega)
- [Requisitos do projeto](#requisitos-do-projeto)
  - [Lista de requisitos](#lista-de-requisitos)
    - [Desafios Iniciais](#desafios-iniciais)
    - [Desafios sobre filtragem de dados](#desafios-sobre-filtragem-de-dados)
    - [Desafios de manipulação de tabelas](#desafios-de-manipulação-de-tabelas)

---

# Habilidades
Nesse projeto, foram desenvolvidas e avaliadas as seguintes habilidades:

- Compreensão do que são bancos de dados
- Compreensão de como a linguagem de consulta estruturada (SQL) é usada
- Compreensão de como as tabelas se encaixam no conceito de banco de dados
- Montagem de um ambiente de desenvolvimento local para praticar SQL
- Entendimento de como usar o MySQL Workbench
- Compreensão do que é uma query SQL e quais são seus tipos de comando
- Geração de valores com `SELECT`
- Seleção de colunas individualmente com `SELECT`
- Renomeação e geração de colunas em uma consulta com `AS`
- Concatenação de colunas e valores com `CONCAT`
- Remoção de dados duplicados em uma consulta com `DISTINCT`
- Contagem da quantidade de resultados em uma consulta com `COUNT`
- Limite da quantidade de resultados em uma consulta com `LIMIT`
- Controle de paginação de resultados em uma consulta com `OFFSET`
- Ordernação dos resultados de uma consulta com `ORDER BY`
- Filtragem de resultados de consultas com o `WHERE`
- Utilização de operadores booleanos e relacionais em consultas
- Criação de consultas mais dinâmicas e maleáveis com `LIKE`
- Construção de consultas que englobam uma faixa de resultados com `IN` e `BETWEEN`
- Encontre e separação de resultados que incluem datas.
- Inserção de dados em tabelas com `INSERT`
- Atualização de dados em tabelas com `UPDATE`
- Remoção de dados em tabelas com `DELETE`

---

## Data de entrega

- Projeto individual.

- Ao todo, 1 dia de projeto.

- Data de entrega para avaliação final do projeto: `29/07/2021 - 14:00h`.


## Instruções para acessar a branch do Projeto

1. Clone o repositório
  * `git clone https://github.com/tryber/sd-010-a-mysql-all-for-one.git`.
  * Entre na pasta do repositório que você acabou de clonar:
    * `cd sd-010-a-mysql-all-for-one`

2. Instale as dependências [**Caso existam**]
  * `npm install` [**exemplo**]

3. Vá para a branch do projeto
  * Verifique que você está na branch `master`
    * Exemplo: `git branch`
  * Se estiver, mude para a branch `anaventura1811-mysql-all-for-one`
    * Exemplo: `git checkout anaventura1811-mysql-all-for-one`

---

# Detalhes do desenvolvimento do projeto

## Instruções para restauração do banco de dados `Northwind`

1. Faça o download do arquivo de backup [aqui](northwind.sql) clicando em "Raw", depois clicando com botão direito e selecionando "Salvar como" para salvar o arquivo em seu computador.
2. Abra o arquivo com algum editor de texto, e selecione todo o conteúdo do arquivo usando `CTRL-A`.
3. Abra o MySQL Workbench.
4. Abra uma nova janela de query e cole dentro dela todo o conteúdo do arquivo `northwind.sql`.
5. Selecione todo o código com o atalho `CTRL-A` e depois clique no icone de trovão para executar a query.

    ![Restaurando o banco Northwind](images/restore_northwind.png)
6. Aguarde alguns segundos (espere em torno de 30 segundos antes de tentar fazer algo).
7. Clique no botão apontado na imagem a seguir para atualizar a listagem de banco de dados.

    ![Tabelas do banco Northwind](images/refresh_databases.png)
7. Verifique se o banco restaurado possui todas as seguintes tabelas:

    ![Tabelas do banco Northwind](images/northwind.png)
8. Clique com botão direito em cada tabela e selecione "Select Rows" e certifique-se que todas as tabelas possuem registros. Caso tenha alguma faltando, faça o passo a seguir. Caso contrário, pode ir para próxima seção.
9. Caso existam tabelas faltando, drope o banco de dados, clicando com o botão direito em cima do banco de dados northwind e selecionando "Drop Schema", e refaça os passos novamente, dessa vez aguardando um tempo maior quando executar o script de restauração.

    ![Drop Schema](images/drop_database.png)

---

## Instruções para teste das queries

Para executar localmente os testes, é preciso escrever o seguinte no seu terminal:
```sh
MYSQL_USER=<SEU_NOME_DE_PESSOA_USUARIA> MYSQL_PASSWORD=<SUA SENHA> HOSTNAME=<NOME_DO_HOST> npm test
```

Ou seja, suponha que para poder acessar a base de dados feita neste projeto você tenha `root` como seu nome de pessoa usuária, `password` como senha e `localhost` como host. Logo, você executaria:
```sh
MYSQL_USER=root MYSQL_PASSWORD=password HOSTNAME=localhost npm test
```

Usando o exemplo anterior de base, suponha que você não tenha setado uma senha para `root`. Neste caso, você executaria:
```sh
MYSQL_USER=root MYSQL_PASSWORD= HOSTNAME=localhost npm test
  ```
---

# Requisitos do projeto

Monte queries para encontrar as informações esperadas pelos desafios:

## Lista de Requisitos

## Desafios Iniciais

 - [x] 1 - Exiba apenas os nomes do produtos na tabela `products`.

 - [x] 2 - Exiba os dados de todas as colunas da tabela `products`.

 - [x] 3 - Escreva uma query que exiba os valores da coluna que representa a primary key da tabela `products`.

 - [x] 4 - Conte quantos registros existem em `product_name` de `products`.
 - [x] 5 - Monte uma query que exiba os dados da tabela `products` a partir do quarto registro até o décimo terceiro, incluindo tanto um quanto o outro. Obs.: não use `where` ou `order by`.

 - [x] 6 - Exiba os dados das colunas `product_name` e `id` da tabela `products` de maneira que os resultados estejam em ordem alfabética dos nomes.

 - [x] 7 - Mostre apenas os ids dos 5 últimos registros da tabela `products` (a ordernação deve ser baseada na coluna `id`).
 - [x] 8 - Faça uma consulta que retorne três colunas. Na primeira coluna, exiba a soma de `5 + 6` (essa soma deve ser realizada pelo SQL). Na segunda coluna deve haver a palavra \"de\". E por fim, na terceira coluna, exiba a soma de `2 + 8` (essa soma deve ser realizada pelo SQL). A primeira coluna deve se chamar \"A\", a segunda coluna deve se chamar \"Trybe\" e a terceira coluna deve se chamar \"eh\". Não use colunas pre-existentes, apenas o que for criado na hora.

---

## Desafios sobre filtragem de dados

 - [x] 9 - Mostre todos os valores de `notes` da tabela `purchase_orders` que não são nulos.

 - [x] 10 - Mostre todos os dados da tabela `purchase_orders` em ordem decrescente ordenados por `created_by` em que o `created_by` é maior ou igual a 3. E como critério de desempate para a ordenação, ordene também os resultados pelo `id` de forma crescente.

 - [x] 11 - Exiba os dados de `notes` da tabela `purchase_orders` em que seu valor de \"Purchase generated based on Order\" está entre 30 e 39, incluindo tanto o valor de 30 quanto de 39.

 - [x] 12 - Mostre as `submitted_date` de `purchase_orders` em que a `submitted_date` é do dia 26 de abril de 2006.

 - [x] 13 - Mostre o `supplier_id` das `purchase_orders` em que o `supplier_id` seja 1 ou 3.

 - [x] 14 - Mostre os `supplier_id` da `purchase_orders` em que o `supplier_id` seja de 1 a 3, incluindo tanto o 1 quanto o 3.

 - [x] 15 - Mostre somente as horas (sem os minutos e os segundos) da `submitted_date` de todos registros de `purchase_orders`. Chame essa coluna de `submitted_hour`.

 - [x] 16 - Exiba a `submitted_date` das `purchase_orders` que estão entre `2006-01-26 00:00:00` e `2006-03-31 23:59:59`.

 - [x] 17 - Mostre os registros das colunas `id` e `supplier_id` das `purchase_orders` em que os `supplier_id` sejam tanto 1, ou 3, ou 5, ou 7.

 - [x] 18 - Mostre todos os registros de `purchase_orders` que tem o `supplier_id` igual a 3 e `status_id` igual a 2.

 - [x] 19 - Mostre a quantidade de pedidos que foram feitos na tabela `orders` pelo `employee_id` igual a 5 ou 6, e que foram enviados através do método `shipper_id` igual a 2. Chame a coluna de orders_count.

---

## Desafios de manipulação de tabelas

 - [x] 20 - Adicione ao `order_details` uma linha com os seguintes dados: `order_id`: 69, `product_id`: 80, `quantity`: 15.0000, `unit_price`: 15.0000, `discount`: 0, `status_id`: 2, `date_allocated`: NULL, `purchase_order_id`: NULL e `inventory_id`: 129. Obs.: o `id` deve ser incrementado automaticamente.

 - [x] 21 - Adicione, com um único `INSERT`, duas linhas ao `order_details` com os mesmos dados. Esses dados são novamente `order_id`: 69, `product_id`: 80, `quantity`: 15.0000, `unit_price`: 15.0000, `discount`: 0, `status_id`: 2, `date_allocated`: NULL, `purchase_order_id`: NULL e `inventory_id`: 129 (o `ìd` deve ser incrementado automaticamente).

 - [x] 22 - Atualize os dados de `discount` do `order_details` para 15. (Não é necessário utilizar o SAFE UPDATE em sua query).

 - [x] 23 - Atualize os dados de `discount` da tabela `order_details` para 30 cuja `unit_price` seja menor que 10.0000. (Não é necessário utilizar o SAFE UPDATE em sua query).

 - [x] 24 - Atualize os dados de `discount` da tabela `order_details` para 45 cuja `unit_price` seja maior que 10.0000 e o id seja um número entre 30 a 40. (Não é necessário utilizar o SAFE UPDATE em sua query).

 - [x] 25 - Delete todos os dados em que a `unit_price` da tabela `order_details` seja menor que 10.0000.

 - [x] 26 - Delete todos os dados em que a `unit_price` da tabela `order_details` seja maior que 10.0000.

 - [x] 27 - Delete todos os dados da tabela `order_details`.

