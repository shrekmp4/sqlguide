
# 💉SQL Full Guide 🛀

 Guía de como usar **SQL**
## INDEX
- [XAMPP INSTALL](#XAMPP)
- [BASICOS DE CODIGO](#BÁSICOS-DE-CÓDIGO)
- [SELECIONES](#SELECIONES)
- [AÑADIR DATOS](#AÑADIR-DATOS)
- [ELIMINAR DATOS](#ELIMINAR-DATOS)


## XAMPP

Despúes de descargar en [Instalar Runner](https://www.apachefriends.org/es/download.html)
```bash
cd Descargas
```
Agrega permisos de ejecución al instalador
```bash
cd chmod +x xampp-linux-x64-7.2.12-0-installer.run
```
Inicia el instalador
```bash
sudo ./xampp-linux-x64-7.2.12-0-installer.run
```
Una vez lo instales puedes iniciar los servicios a través de su ruta.
```bash
cd /opt/lampp
sudo ./manager-linux-x64.run
```

## BÁSICOS-DE-CÓDIGO 
[Vuelve arriba 👆](#INDEX)

Crear una base de datos.  **[+]🟢**
```sql
CREATE DATABASE DB1;
```
Crear una tabla con columnas. **[+]🟢**
```sql
CREATE TABLE ejemplo (
    id INT,
    nombre VARCHAR(50)
);
```
Eliminar una columa. **[-]🔴**
```sql
DROP TABLE ejemplo;
```
Eliminar una _base de datos._ **[-]🔴**
```sql
DROP DATABASE ejemplo;
```
Agregar columnas a una tabla. **(Sigue la estructura)** **[+]🟢**
```sql
ALTER TABLE ejemplo
ADD correo VARCHAR(100),
    edad INT NULL DEFAULT 18;
```

Renombrar una tabla.
```sql
ALTER TABLE usuarios
RENAME TO clientes;
```

Renombrar una tabla VARIANTE Nº2
```sql
ALTER TABLE usuarios
RENAME AS clientes;
```

Renombrar una tabla VARIANTE Nº3
```sql
ALTER TABLE usuarios,
RENAME TO clientes;
```


Eliminar Columnas de una tabla. **[-]🔴**
```sql
ALTER TABLE ejemplo
DROP COLUMN correo;
```

## SELECCIONES 
[Vuelve arriba 👆](#INDEX)

Como selecionar datos en nuestras tablas/columnas. Si no sabes agregar datos debes leer [AÑADIR DATOS](#AÑADIR-DATOS)


Seleccionar TODOS los datos de una columna.  **(  *  )**
```sql
SELECT * FROM usuarios
```

Selecionar con un condicional. **(Seleciona todos los usuarios mayores de 18 años.)**

```sql
SELECT * FROM usuarios WHERE edad > 18; 
```

Seleciona datos específicos de una columna.
```sql
SELECT nombre FROM usuarios;
```

Seleccionar datos de múltiples columnas.

```sql
SELECT nombre, edad FROM usuarios;
```

Selecionar con un orden específicos.  **(DESC, ASC)**

```sql
SELECT * FROM usuarios ORDER BY edad DESC;
```

Seleccionar datos con una limitación en la cantidad de resultados. **(LIMIT)**

```sql
SELECT * FROM usuarios LIMIT 10;
```

Seleccionar datos con una condición compuesta. **(AND)**
```sql
SELECT * FROM usuarios WHERE edad > 18 AND ciudad = 'Madrid';
```

Seleccionar datos con una condición utilizando el operador **LIKE.**
```sql
SELECT * FROM usuarios WHERE nombre LIKE 'A%';
```

Seleccionar datos con una condición utilizando el operador **IN.**
```sql
SELECT * FROM usuarios WHERE ciudad IN ('Madrid', 'Barcelona', 'Valencia');
```

## AÑADIR-DATOS

Para poder añadir datos a una tabla en SQL tienes que usar **INSERT INTO**

Añadir datos a tabla en sus columnas. **[+]🟢**
```sql
INSERT INTO usuarios (nombre, edad, correo)
VALUES ('María', 25, 'maria@example.com'),
       ('Pedro', 35, 'pedro@example.com'),
       ('Ana', 28, 'ana@example.com');
```

## ELIMINAR-DATOS

[Vuelve arriba 👆](#INDEX)

Para eliminar datos debes usar **DELETE** **[-]🔴**

Eliminar datos de una tabla siguiendo una condición.
```sql
DELETE FROM nombre_de_la_tabla WHERE condición;
```

- Posibles condiciones para estos casos pueden ser, la **edad**, **ID**, **Apellidos**..
  Una manera práctica de aplicar esto es. **[-]🔴**
  ```sql
  DELETE FROM usuarios WHERE edad = 18;
  ```
- Para eliminar todos los registros de una tabla. **[-]🔴**
    ```sql
  DELETE FROM usuarios;
  ```
