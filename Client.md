# Client_md

### Creacion de la Tabla
El sigueinte codigo crea la tabla **client**
```
CREATE TABLE IF NOT EXIST client(
id SERIAL,
nui VARCGAR(10) NOT NULL
fullname VARCHAR(100),
phone VARCHAR(10),
type_of_client VARCHAR(50) DEFAULT 'BASIC',
city VARCHAR(50),
credit_limit DECIMAL (7,2)
);

```
Aqui se puede como se crea la tabla client
## Captura
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/7ac8b7f0-c98a-4fc4-81bb-62d3f1efccaa)

### Insercion de Datos
Insertar datos a la tabla **client**
```

INSERT INTO client (nui, fullname, phone,type_of_client, city, credit_limit) VALUES 
('1234567890', 'John Doe', '0987654321','VIP', 'Quito', 500.00),
('2345678901', 'Jane Smith', '1234567890','VIP', 'Guayaquil', 1000.00),
('3456789012', 'Michael Johnson', '2345678901','BASIC', 'Cuenca', 750.00),
('4567890123', 'Emily Brown', '3456789012','VIP', 'Manta', 600.00),
('5678901234', 'David Lee', '4567890123','BASIC', 'Quito', 800.00),
('1234567890', 'John Doe', '0987654321', 'BASIC','Quito', 500.00),
('2345678901', 'Jane Smith', '1234567890','VIP', 'Guayaquil', 1000.00),
('3456789012', 'Michael Johnson', '2345678901','VIP', 'Cuenca', 750.00),
('4567890123', 'Emily Brown', '3456789012','BASIC', 'Manta', 600.00),
('5678901234', 'David Lee', '4567890123','BASIC', 'Quito', 800.00);
INSERT INTO client (nui, fullname,type_of_client, city, credit_limit) VALUES 
('1234567890', 'John Doe','BASIC', 'Quito', 500.00),
('2345678901', 'Jane Smith','VIP', 'Guayaquil', 1000.00),
('3456789012', 'Michael Johnson','BASIC', 'Cuenca', 750.00),
('4567890123', 'Emily Brown','BASIC', 'Manta', 600.00),
('5678901234', 'David Lee','VIP', 'Quito', 800.00);
```
aqui se puede ver como se Insertan los datos a los registros de la tabla
### Captura
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/e738831f-40e4-4f59-8e31-feda99f3e133)

## Total Nombres
```
SELECT COUNT (fullname) AS total_names
FROM client;
```
Con este sentencia se Pueden ver todos los registros que tengas los nombres completos
### Captura 
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/65cbbe28-5f5f-4ac4-a255-5c9b83b86497)

## Total numeros Telefono
```
SELECT COUNT (phone) AS total_phones
FROM client;
```
Con este sentencia se Pueden ver todos los registros que tengan los numeros de telefono
### Captura
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/16ae0506-b6fa-4f92-9774-650b49cf349f)

## Total Nombres,Telefonos
```
SELECT COUNT (phone) AS total_phones, COUNT (fullname) AS total_names
FROM client;
```
Con este sentencia se Pueden ver todos los registros que tengan los numeros de telefono y los nombres completos
### Captura
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/80eb9f50-1a6a-4581-8fd8-135445f217e2)

## Total Nombres,Telefonos,Total
```
SELECT COUNT (phone) AS total_phones, COUNT (fullname) AS total_names, COUNT (*) AS total
FROM client;
```
Con este sentencia se Pueden ver todos los registros que tengan los numeros de telefono y los nombres completos y *
### Captura
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/6aa9b4c4-f200-4e49-8478-607affdbb67d)

## Total Ciudades
```
SELECT COUNT (city) AS total_citys
FROM client;
```
Con esta sentencia se pueden ver todos los regsitros que tengas ciudad 
### Captura
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/eebd1f79-9e45-4b02-b3c2-d5e63cb0128f)
## Total Ciudades sin repetir
```
SELECT COUNT (DISTINCT city) AS total_citys
FROM client;
```
Con esta sentencia se pueden ver todos lkos registros que tengan las 4 ciudades sin repetirse
### Captura 
![image](https://github.com/ByMatius28/Tarea-Events/assets/146010494/4c207fac-a10f-47a4-bad8-3ab712b9f354)

