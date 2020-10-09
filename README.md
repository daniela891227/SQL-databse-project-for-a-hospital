# SQL databse project for a hospital
## Project description
This is a database is meant to save information for a Hospital in Uruguay. 

## Technology used
*MySQL

*MySQL Workbench

## Features
The database contained entities defined for doctors, nurses, cleaners, types of treatments, types of services, rooms, providers, medicine, etc and the relationships between them to make the Entity/Relationship diagram.

## Code sample
'''sql
SELECT P.Nombre, count(*) as Cantidad_de_medicamentos_suministrados
FROM proyecto_final.suministran SM INNER JOIN proyecto_final.proveedores as P ON
SM.Codigo_del_proveedor = P.Codigo_del_proveedor INNER JOIN proyecto_final.medicamentos as M ON
SM.Codigo_medicamento = M.Codigo_medicamento
GROUP BY P.Nombre
ORDER BY Cantidad_de_medicamentos_suministrados DESC
Limit 1;
'''


