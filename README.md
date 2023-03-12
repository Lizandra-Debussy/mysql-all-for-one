# Repositório do projeto mysql All For One

Projeto desenvolvido durante o módulo de Back-End no curso de Desenvolvimento WEB da Trybe .

Com o codinome All For One, este projeto teve como objetivo praticar todos os conceitos de SQL ensinados durante o módulo de Back-End. O banco de dados utilizado foi o Northwind.

## Habilidades

* Criar dados;
* Filtrar dados;
* Manipular tabelas;

## Tecnologias e Ferramentas

* SQL
* Docker
* Node

## Requisitos do projeto
<details>
  <summary><strong>Desafios Iniciais</strong></summary><br />

1. Exiba apenas os nomes dos produtos na tabela products.
2. Exiba os dados de todas as colunas da tabela products.
3. Escreva uma query que exiba os valores da coluna que representa a primary key da tabela products.
4. Conte quantos registros existem na coluna product_name da tabela products.
5. Monte uma query que exiba os dados da tabela products a partir do quarto registro até o décimo terceiro.
6. Exiba os dados das colunas product_name e id da tabela products de maneira que os resultados estejam em ordem alfabética dos nomes.
7. Mostre apenas os ids dos 5 últimos registros da tabela products (a ordernação deve ser baseada na coluna id).
8. Faça uma consulta que retorne três colunas, respectivamente, com os nomes 'A', 'Trybe' e 'eh', e com valores referentes a soma de '5 + 6', a string 'de', a soma de '2 + 8'.
</details>
<details>
  <summary><strong>Desafios sobre filtragem de dados</strong></summary><br />

9. Mostre todos os valores de notes da tabela purchase_orders que não são nulos.
10. Mostre todos os dados da tabela purchase_orders em ordem decrescente, ordenados por created_by em que o created_by é maior ou igual a 3.
Ordene também os resultados pelo id de forma crescente, como critério de desempate para a ordenação.
11. Exiba os dados da coluna notes da tabela purchase_orders em que seu valor de Purchase generated based on Order é maior ou igual a 30 e menor ou igual a 39.
12. Mostre as submitted_date de purchase_orders em que a submitted_date é do dia 26 de abril de 2006.
13. Mostre o supplier_id das purchase_orders em que o supplier_id seja 1 ou 3.
14. Mostre os resultados da coluna supplier_id da tabela purchase_orders em que o supplier_id seja maior ou igual a 1 e menor ou igual 3.
15. Mostre somente as horas (sem os minutos e os segundos) da coluna submitted_date de todos registros da tabela purchase_orders. No resultado, a hora extraída da coluna submitted_date deve ser chamada de submitted_hour.
16. Exiba a submitted_date das purchase_orders que estão entre 2006-01-26 00:00:00 e 2006-03-31 23:59:59.
17. Mostre os registros das colunas id e supplier_id das purchase_orders em que os supplier_id sejam tanto 1, ou 3, ou 5, ou 7.
18. Mostre todos os registros de purchase_orders que tem o supplier_id igual a 3 e status_id igual a 2.
19. Mostre a quantidade de pedidos que foram feitos na tabela orders pelo employee_id igual a 5 ou 6, e que foram enviados através do método(coluna) shipper_id igual a 2. No resultado, a coluna que contém a contagem de pedidos deve ser chamada de orders_count.
 </details>

<details>
  <summary><strong>Desafios de manipulação de tabelas</strong></summary><br />

20. Adicione à tabela order_details um registro com order_id: 69, product_id: 80, quantity: 15.0000, unit_price: 15.0000, discount: 0, status_id: 2, date_allocated: NULL, purchase_order_id: NULL e inventory_id: 129.
21. Adicione com um único INSERT, duas linhas à tabela order_details com os mesmos dados do requisito 20.
22. Atualize todos os dados de discount do order_details para 15.
23. Atualize os dados da coluna discount da tabela order_details para 30, onde o valor na coluna unit_price seja menor que 10.0000.
24. Atualize os dados da coluna discount da tabela order_details para 45, onde o valor na coluna unit_price seja maior que 10.0000 e o id seja um número entre 30 e 40.
25. Delete todos os dados em que a unit_price da tabela order_details seja menor que 10.0000.
26. Delete todos os dados em que a unit_price da tabela order_details seja maior que 10.0000.
27. Delete todos os dados da tabela order_details.ção em segundo plano com o docker-compose de forma que backend, frontend e tests consigam se comunicar
</details>

  
## Como utilizar

* Clone o repositório:
```
  git@github.com:Lizandra-Debussy/mysql-all-for-one.git
```
* Acesse a pasta do repositório:
```
  cd mysql-all-for-one.git
```
* Instale as dependências:
```
  npm install
```

<details>
  <summary><strong>Com Docker</strong></summary><br />
  
 Antes de começar, seu docker-compose precisa estar na versão 1.29 ou superior.<br />
   
* Rode os serviços node e db com o comando:
 ```
   docker-compose up -d
 ```
* Lembre-se de parar o mysql se estiver usando localmente na porta padrão (3306), ou adapte, caso queria fazer uso da aplicação em containers.
* Esses serviços irão inicializar um container chamado all_for_one e outro chamado all_for_one_db.
* A partir daqui você pode rodar o container all_for_one via CLI ou abri-lo no VS Code.

* Use o comando:
```
  docker exec -it all_for_one bash
```
* Ele te dará acesso ao terminal interativo do container criado pelo compose, que está rodando em segundo plano.
* As credencias de acesso ao banco de dados estão definidas no arquivo docker-compose.yml, e são acessíveis no container através das variáveis de ambiente MYSQL_USER e MYSQL_PASSWORD.
* Instale as dependências:
```
  npm install
```

 </details>
