
# 💉SQL Full Guide 

Guía de como usar **SQL**
- [XAMPP INSTALL](#XAMPP)
- [BASICOS DE CODIGO](#BÁSICOS-DE-CÓDIGO)
- [SELECIONES](#SELECIONES)
- [AÑADIR DATOS](#AÑADIR-DATOS)



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

Eliminar Columnas de una tabla. **[-]🔴**
```sql
ALTER TABLE ejemplo
DROP COLUMN correo;
```

## SELECCIONES 

Como selecionar datos en nuestras tablas/columnas. Si no sabes agregar datos debes leer


Seleccionar TODOS los datos de una columna.
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

Selecionar con un orden específicos.

```sql
SELECT * FROM usuarios ORDER BY edad DESC;
```

Seleccionar datos con una limitación en la cantidad de resultados.

```sql
SELECT * FROM usuarios LIMIT 10;
```

Seleccionar datos con una condición compuesta:
```sql
SELECT * FROM usuarios WHERE edad > 18 AND ciudad = 'Madrid';
```

Seleccionar datos con una condición utilizando el operador LIKE.
```sql
SELECT * FROM usuarios WHERE nombre LIKE 'A%';
```

Seleccionar datos con una condición utilizando el operador IN.
```sql
SELECT * FROM usuarios WHERE ciudad IN ('Madrid', 'Barcelona', 'Valencia');
```

## AÑADIR-DATOS
