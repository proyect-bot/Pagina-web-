CREATE database colegio_db;
use colegio_db;
/*creacion de tablas */
/*tablas deestudiantes */
create table estudiantes (
id int auto_increment  primary key ,
nombre varchar(50), 
apellido varchar (50),
curso varchar (5)


);
 /*tablas asistencia */
 
 create table asistencia (
 id  int auto_increment primary key,
 estudiante_id int ,
 fecha date , 
 estado enum ("presente" ," falla" ),
 foreign key (estudiante_id) references  estudiantes(id)
 );
 /*subir  datos */ 
 
 insert into ESTUDIANTES (nombres, apellidos, curso) VARIABLES
("MARIA", "PEREZ", 1104), ("JUAN", "LOPEZ", "1104"), ("ANA", "MARTINEZ", "1104");

insert INTO asistencia (estudiantes_id, fecha, estado) values
(10001, '2025-08-27', 'presente'),
(10002, '2025-08-27', 'falla'),
(10003, '2025-08-27', 'presente');
