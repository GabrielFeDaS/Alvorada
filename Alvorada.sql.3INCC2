create database alvorada;
use alvorada;

create table cliente(
id_cli int not null auto_increment,
cli_nome varchar(150),
cpf varchar(14),
primary key(id_cli)
);

create table endereco(
id_end int not null auto_increment,
país varchar(20),
estado char(2),
cidade varchar(50),
cep varchar(11),
complemento varchar(150),
primary key(id_end)
);

create table modificacoes(
id_mod int not null auto_increment,
motor varchar(55),
model_aro varchar(60),
pneu varchar(50),
cor varchar(20),
altura_suspensao varchar(10),
design_interior varchar(599),
bodykits varchar(255),
nitro varchar(69),
primary key(id_mod)
);

create table veiculo(
id_vei int not null auto_increment,
cod_mod int,
modelo varchar(199),
marca varchar(50), 
cor varchar(50),
placa varchar(7),
chassi varchar(17),
primary key(id_vei)
);

alter table veiculo add foreign key (cod_mod) references modificacoes(id_mod);

create table pedido(
id_pedido int not null auto_increment,
cod_cli int,
cod_end int,
cod_vei int,
cod_mod int,
data_entrega date,
valor numeric(10,2),
primary key(id_pedido)
);

alter table pedido add foreign key (cod_cli) references cliente(id_cli);
alter table pedido add foreign key (cod_end) references endereco(id_end);
alter table pedido add foreign key (cod_vei) references veiculo(id_vei);
alter table pedido add foreign key (cod_mod) references modificacoes(id_mod);

