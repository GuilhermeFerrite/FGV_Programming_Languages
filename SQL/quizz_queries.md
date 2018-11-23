Sobre o banco de dados "classicmodels", indique as queries para obter as seguintes informações:

- Quantos registros há na tabela "customers"? 122

- Na tabela "customers", quantos clientes ("customerName") têm nome iniciado pela letra "M"? 14 

select count(*) from customers where customerName like "m%";

- Na tabela "customers", crie uma saída que concatene nomes e sobrenomes em uma única coluna.

select concat(contactFirstName," ", contactLastName) from customers;

- Agora repita a query acima, mas com todas as letras em maiúsculo, e ordene pelo sobrenome.

select UPPER(concat(contactFirstName," ", contactLastName)) from customers ORDER BY contactLastName;

- Na tabela "payments", selecione os registros ordenados por volume ("amount") e data de pagamento ("paymentDate")

select amount, paymentDate from payments order by amount , paymentDate;

- Na tabela "employees", indique quantos nomes de cargos ("jobTitle") únicos existem? 7

select count(DISTINCT jobTitle) from employees;

- Qual destes cargos ("jobTitle") possuem mais funcionários? SalesRep

select count(*), jobTitle from employees group by jobTitle;




