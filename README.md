# UC10

CREATE TABLE veiculo (
Id int(11) NOT NULL AUTO_INCREMENT,
Placa varchar(09) NOT NULL,
Marca varchar(20) NOT NULL,
Modelo varchar(20) NOT NULL,
PRIMARY KEY (Id)
);

CREATE TABLE funcionario (
Id int(11) NOT NULL AUTO_INCREMENT,
Nome varchar(60) NOT NULL,
Matricula int(08) NOT NULL,
VeiculoId int(11) NOT NULL,
PRIMARY KEY (Id),
FOREIGN KEY (VeiculoId) REFERENCES veiculo (Id)
);

INSERT INTO veiculo (Placa, Marca, Modelo) VALUES
('REG0365', 'RENAULT', 'SANDERO'),
('REG6390', 'FIAT', 'ARGO'),
('FGT8996', 'FORD', 'FORD KA'),
('JOK3396', 'VW', 'POLO'),
('LIP4752', 'FIAT', 'SIENA');

INSERT INTO funcionario (Nome, Matricula, VeiculoId) VALUES
('MATEUS', '7777', 1),
('JOYCE', '2202', 2),
('MARIA', '5632', 2),
('JOSE', '5212', 3),
('JOEL', '0101', 5),
('PAULA', '9632', 4),
('JOAO', '7412', 1);
