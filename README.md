# SQL databse project for a hospital
## Project description 
The hospital called "SALUD_URUGUAY" is dedicated to the care of patients.
It has numerous doctors, nurses, cleaning services, patients, etc.
Each patient attends the hospital to request a diagnosis, repeat medications and / or receive treatment. This hospital has a bed service for patients who have undergone surgery.
Since they do not have a database to organize their business, they asked me to help them with this work.

## Technology used
* MySQL
* MySQL Workbench

## Features
The database contained entities defined for doctors, nurses, cleaners, types of treatments, types of services, rooms, providers, medicine, patients, etc and the relationships between them to make the Entity/Relationship model. 
It also features the Relational model, the database object creation queries (tables, indexes, fk) and the data insertion queries in each of them.

## Code sample
SQL query: The supplier that provided the most medicines to the hospital
```sql

SELECT P.Nombre, count(*) as Cantidad_de_medicamentos_suministrados
FROM proyecto_final.suministran SM INNER JOIN proyecto_final.proveedores as P ON
SM.Codigo_del_proveedor = P.Codigo_del_proveedor INNER JOIN proyecto_final.medicamentos as M ON
SM.Codigo_medicamento = M.Codigo_medicamento
GROUP BY P.Nombre
ORDER BY Cantidad_de_medicamentos_suministrados DESC
Limit 1;

```


