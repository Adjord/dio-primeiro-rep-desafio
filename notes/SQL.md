# SQL

## Três pilares:

- DDL: Data Definition Language
- DML: Data Manipulation Language
- DQL: Data Query Language

#### • DDL:
Mecanismo utilizado para criar ou definir o bando de dados fisicamente (não de dados)

*Ex:*
_Criação de tabela ***Cliente***._


```sql
Create Table Cliente
(
Codigo number(10) Not Null Primary Key,    /*Codigo aceita 10 numeros.*/
Nome varchar(50) Not Null,                 /*Nome aceita 50 de qualquer caractere.*/
Telefone varchar(15)                       /*Telefone aceita 15 de qualquer caractere.*/
)
```


#### • DML:

Utilizado para ter ação sobre os dados fisicamente, responsável pela manipulação e alteração de tabelas.

*Ex:* 
_Inserção, remoção e atualização de parametros respectivamente._


```sql
insert into Cliente(Codigo, Nome, Telefone)
values(1,"Lorem ipsum", "(88) 9999999")
/*Insere na tabela Cliente o codigo, nome e telefone, onde, os valores estão explicitos em values()*/

Delete from Cliente
Where Codigo = 1
/*Deleta tudo da tabela Cliente que tenha Codigo 1.*/

Update Cliente
set Nome = "Lorem Ipsum"
Where Codigo = 1
/*Atualiza o valor "Nome" onde na tabela o coódigo for 1*/
```



#### • DQL:

Linguagem de consulta aos dados. Apenas extração e exibição dessa extração.

*Ex:*



```sql
Select Codigo,
		Nome
from Cliente
/*Selecione das colunas Codigo e Nome da tablea Cliente*/
<Where> Codigo = 1 /*Filtro*/
	<Group by> Profissao
	<Having> Count(1) > 0
<Order by> Nome, Codigo
```