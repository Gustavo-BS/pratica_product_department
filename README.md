# Practice product-department

Project made in Java 17, using the SpringBoot framework to create a web application for product registration, using SQL commands, JPA and H2 database.

Example of department, where ID is the primary key:

![image](https://user-images.githubusercontent.com/106408316/236623572-bc1f75c7-e91d-449b-8853-87141513145c.png)

Example of products, where ID is the primary key and DEPARTMENT_ID is the foreign key of the department table:

![image](https://user-images.githubusercontent.com/106408316/236623689-bf052bc0-fc07-4d7c-8fbf-c29a2212a01f.png)

## Maven Dependencies

To use JPA it was necessary to import JPA from SpringBoot and the H2 database:

```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>

<dependency>
	<groupId>com.h2database</groupId>
	<artifactId>h2</artifactId>
	<scope>runtime</scope>
</dependency>
```

## H2 Database Configuration

To access the database, you must access

http://localhost:8080/h2-console

where username = sa

password = (empty)

```
# H2 Connection
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

# H2 Client
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# Show SQL
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

## SQL Commands


```
INSERT INTO tb_department (name) VALUES ('Tech');
INSERT INTO tb_department (name) VALUES ('Pet');

INSERT INTO tb_product (name, price, department_id) VALUES ('Macbook Pro', 4000.0, 1);
INSERT INTO tb_product (name, price, department_id) VALUES ('PC Gamer', 5000.0, 1);
INSERT INTO tb_product (name, price, department_id) VALUES ('Cadeira Gamer', 1500.0, 1);
INSERT INTO tb_product (name, price, department_id) VALUES ('Pet House', 300.0, 2);
INSERT INTO tb_product (name, price, department_id) VALUES ('Ração', 100.0, 2);


```




# Pratica produto-departamento
Projeito feito no Java 17, utilizando o framework SpringBoot para criação de uma aplicação web para cadastro de produtos, utilizando comandos SQL, JPA e banco de dados H2.

Exemplo de departamento, onde ID é chave primaria:

![image](https://user-images.githubusercontent.com/106408316/236623572-bc1f75c7-e91d-449b-8853-87141513145c.png)


Exemplo de produtos, onde ID é chave primaria e DEPARTMENT_ID é chave estrangeira da tabela departamento:

![image](https://user-images.githubusercontent.com/106408316/236623689-bf052bc0-fc07-4d7c-8fbf-c29a2212a01f.png)



## Dependências Maven

Para utilizar o JPA foi necessário importar o JPA do SpringBoot e o banco H2:

```xml
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>

<dependency>
	<groupId>com.h2database</groupId>
	<artifactId>h2</artifactId>
	<scope>runtime</scope>
</dependency>
```

## Configuração do Banco de Dados H2

Para entrar no banco de dados é necessario acessar

http://localhost:8080/h2-console

Onde username = sa

passoword = (vazio)

```
# H2 Connection
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

# H2 Client
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# Show SQL
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

## Comandos SQL

```
INSERT INTO tb_department (name) VALUES ('Tech');
INSERT INTO tb_department (name) VALUES ('Pet');

INSERT INTO tb_product (name, price, department_id) VALUES ('Macbook Pro', 4000.0, 1);
INSERT INTO tb_product (name, price, department_id) VALUES ('PC Gamer', 5000.0, 1);
INSERT INTO tb_product (name, price, department_id) VALUES ('Cadeira Gamer', 1500.0, 1);
INSERT INTO tb_product (name, price, department_id) VALUES ('Pet House', 300.0, 2);
INSERT INTO tb_product (name, price, department_id) VALUES ('Ração', 100.0, 2);


```
