drop database restaurante;

create database restaurante;

use restaurante;

create table Clientes
(IDcliente int auto_increment primary key,
nome varchar(100) not null,
telefone varchar(15) not null 
);

create table Pratos
(IDprato int auto_increment primary key,
nome varchar(100) not null,
preco decimal(10,2)
);

create table Pedidos
(IDpedido int auto_increment primary key,
IDcliente int,
dados_pedido text,
foreign key (IDcliente) references Clientes(IDcliente) on delete cascade
);

create table Quantidades
(IDitem int auto_increment primary key,
IDpedido int,
IDprato int,
quantidade int,
foreign key (IDpedido) references Pedidos(IDpedido) on delete cascade,
foreign key (IDprato) references Pratos(IDprato) on delete cascade
);

insert into Clientes(IDcliente,nome,telefone) values
('1','pessoaA','111111111111111'),
('2','pessoaB','222222222222222'),
('3','pessoaC','333333333333333'),
('4','pessoaD','444444444444444'),
('5','PessoaE','555555555555555');

insert into Pratos(IDprato,nome,preco) values
('11','rabanada','10.0'),
('12','feijoada','15.0'),
('13','macarronada','12.0'),
('14','frango frito','10.0'),
('15','sopa de batata','15.0');

insert into Pedidos(IDpedido,IDcliente,dados_pedido) values
('100','1','para pessoaA'),
('101','2','para pessoaB'),
('102','3','para pessoaC');
